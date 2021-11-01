# Diga "Olá" ao mundo na arte ASCII

------

14



**Desafio:** Produza a seguinte saída usando o menor número possível de caracteres:

```
 _   _      _ _                             _     _ _
| | | | ___| | | ___    __      _____  _ __| | __| | |
| |_| |/ _ \ | |/ _ \   \ \ /\ / / _ \| '__| |/ _` | |
|  _  |  __/ | | (_) |   \ V  V / (_) | |  | | (_| |_|
|_| |_|\___|_|_|\___( )   \_/\_/ \___/|_|  |_|\__,_(_)
                    |/
```

**Regras e restrições:**

- Você não pode usar o [FIGLet](http://www.figlet.org/) ou qualquer ferramenta similar. (Caso contrário, `figlet Hello, world!`seria uma solução trivial e praticamente imbatível.)
- Seu programa deve consistir inteiramente de caracteres [ASCII](http://en.wikipedia.org/wiki/ASCII) imprimíveis - especificamente, pontos de código 9 (TAB), 10 (LF) e 32 - 126. (Se o seu idioma / SO exigir quebras de linha CRLF, você poderá usá-los em vez de LFs simples). , isso desqualifica lamentavelmente qualquer idioma que exija caracteres não ASCII (ou dados não textuais) como parte de sua sintaxe.
- A saída deve ser exatamente igual ao exemplo acima. Você pode, no entanto, incluir espaço em branco extra ao redor da saída, se desejar. Você pode assumir o [espaçamento da guia de](http://en.wikipedia.org/wiki/Tab_key#Tab_characters) 8 caracteres (ou a configuração padrão nativa da plataforma escolhida, se houver uma consistente).

Ps. Para definir o par, criei uma solução Perl de 199 caracteres. No entanto, ainda não vou publicá-lo, caso alguém o faça independentemente. (Além disso, é meio extravagante.) Obviamente, isso não deve desencorajá-lo a postar sua própria solução, mesmo que seja mais longa.

------

**Atualização:** Agora que o [han o venceu](https://qastack.com.br/codegolf//a/4378/3191) em um caractere, aqui está a minha solução Perl de 199 caracteres:

```
use Compress'Zlib;say uncompress unpack u,'M>-I]BT$*`S$,`^]YQ=R:0,&_Z<DP?8@?WVQJ]E2J"%E$$@)R(/(/MCJ*\U!OM`Z#=5`4Y>6M=L\L%DMP&DB0V.4GQL&OOGB$4:%`4TT4!R8O-Z(^BTZWNV?>F86K:9+""-35*-LNC:T^D:_$#%^`";"DD0'
```

É muito semelhante à [solução da DC](https://qastack.com.br/codegolf//a/4361/3191) (e a todas as outras soluções baseadas em zlib / gzip em vários idiomas), exceto que eu usei a [uuencoding em](http://en.wikipedia.org/wiki/Uuencoding) vez da [base64](http://en.wikipedia.org/wiki/Base64) para o texto compactado e alguns outros pequenos truques de golfe.

------

**Atualização 2** : Acho que é hora de aceitar oficialmente um vencedor. O primeiro lugar vai para o código PHP do [konsolenfreddy](https://qastack.com.br/codegolf//users/3307/konsolenfreddy) , pois, embora você conte os caracteres, *é* o mais curto enviado até o momento. De fato, combiná-lo com o fluxo DEFLATE otimizado do meu código Perl de 199 caracteres produz uma solução ainda mais curta de 176 caracteres:

```
<?=gzinflate(base64_decode("fYtBCgMxDAPvecXcmkDBv+nJMH2IH99savZUqghZRBICciDyD7Y6ivNQbwOg3VQFOXlrXbPLBZLcBpIkNjlJ8bBr754hFGhQFNNFAcmLzeiPotOt7tn3plq2mSwgjU1SjbLo2tPpGvxAxfgA"));
```

No entanto, acho que [han](https://qastack.com.br/codegolf//users/3031/han) merece uma menção honorária especial por estar tão perto sem usar nenhuma ferramenta de descompressão pré-escrita. Parabéns a vocês dois e um feliz ano novo para todos!

[code-golf](https://qastack.com.br/codegolf/tagged/code-golf/) [ascii-art](https://qastack.com.br/codegolf/tagged/ascii-art/) [kolmogorov-complexity](https://qastack.com.br/codegolf/tagged/kolmogorov-complexity/) [printable-ascii](https://qastack.com.br/codegolf/tagged/printable-ascii/) [hello-world](https://qastack.com.br/codegolf/tagged/hello-world/) 
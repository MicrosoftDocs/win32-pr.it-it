---
title: '\#Direttiva define (macro)'
description: Direttiva del preprocessore che crea una macro simile a una funzione.
ms.assetid: 73c19cf8-fbc5-444b-a51f-dc9f881f397b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49f89847a47a173f8f7d3bcbb22464fecad658068031f62559bde6ec0735f7f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118514812"
---
# <a name="define-directive-macro"></a>\#Direttiva define (macro)

Direttiva del preprocessore che crea una macro simile a una funzione.



| \#define *identifier*( *argument0*, ... , *argumentN-1* ) *token-string* |
|--------------------------------------------------------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                                                                                                                                                                                          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*Identificatore*<br/>                                                                                                                                                                             | Identificatore della macro. <br/> Una seconda [ \# definizione](dx-graphics-hlsl-appendix-pre-define.md) per una macro con un identificatore già esistente nel contesto corrente genera un errore, a meno che la seconda sequenza di token non sia identica alla prima. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="___________argument0___...___argumentN-1_________"></span><span id="___________argument0___...___argumentn-1_________"></span><span id="___________ARGUMENT0___...___ARGUMENTN-1_________"></span> ( *argument0*, ... , *argumentN-1* ) <br/> | Elenco di argomenti per la macro. L'elenco di argomenti è delimitato da virgole, può essere di qualsiasi lunghezza e deve essere racchiuso tra parentesi. Ogni nome di argomento nell'elenco deve essere univoco. Il parametro identifier  e la parentesi di apertura non possono essere separati da spazi vuoti. <br/> Usare la concatenazione di righe posiziona una barra rovesciata ( ) immediatamente prima del carattere di nuova riga per suddividere le direttive lunghe \\ in più righe di origine. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="token-string__optional________"></span><span id="TOKEN-STRING__OPTIONAL________"></span>*token-string* \[ Opzionale\] <br/>                                                                                                                     | Valore della macro. Questo parametro è costituito da una serie di token, ad esempio parole chiave, costanti o istruzioni complete. Uno o più spazi vuoti devono separare questo parametro dal parametro *identifier.* questo spazio vuoto non viene considerato parte del testo sostituito, né lo spazio vuoto dopo l'ultimo token del testo. Usare le parentesi per assicurarsi che gli argomenti complessi vengano interpretati correttamente. <br/> Se il valore del parametro *identifier* si trova all'interno del *parametro token-string* (anche in seguito a un'altra espansione della macro), non viene espanso. <br/> Se si esclude questo parametro, tutte le istanze del parametro *identifier* vengono rimosse dal file di origine. L'identificatore rimane definito e può essere testato usando le direttive [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md)e \# \# ifndef definite. <br/> |



 

## <a name="remarks"></a>Commenti

Tutte le istanze del parametro *identifier* che si verificano dopo la direttiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) nel file di origine costituiscono una chiamata macro e l'identificatore verrà sostituito da una versione del parametro *token-string* con argomenti effettivi sostituiti da parametri formali. Il numero di parametri nella chiamata deve corrispondere al numero di parametri nella definizione della macro. L'identificatore viene sostituito solo quando costituisce un token. Ad esempio, l'identificatore non viene sostituito se viene visualizzato in un commento, all'interno di una stringa o come parte di un identificatore più lungo.

La [ \# direttiva undef](dx-graphics-hlsl-appendix-pre-undef.md) indica al preprocessore di dimenticare la definizione di un identificatore. Per altre informazioni, vedere Direttiva \# undef (DirectX HLSL).

La definizione di costanti con l'opzione del compilatore /D ha lo stesso effetto dell'uso della direttiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) all'inizio del file. Con l'opzione /D è possibile definire fino a 30 macro.

Gli argomenti effettivi nella chiamata di macro vengono abbinati agli argomenti formali corrispondenti nella definizione della macro. Ogni argomento formale nella stringa del token viene sostituito dall'argomento effettivo corrispondente, a meno che l'argomento non sia preceduto da un operatore stringizing ( \# ), charizing ( @) o \# token-pasting ( ) o seguito da un \# \# \# \# operatore . Eventuali macro presenti nell'argomento effettivo vengono espanse prima che la direttiva sostituisca il parametro formale.

L'incollamento di token nel compilatore HLSL è leggermente diverso rispetto all'incollamento di token nel compilatore C, perché i token incollati devono essere token validi. Si consideri ad esempio la definizione di macro seguente:


```
#define MERGE(a, b) a##b
MERGE(float, 4x4) test;
```



Nel compilatore C il risultato è il seguente:


```
float4x4 test
```



Nel compilatore HLSL, tuttavia, ciò comporta quanto segue:


```
float4 x4 test
```



È possibile aggirare questo comportamento usando invece la definizione di macro seguente.


```
MERGE(MERGE(float, 4), x4) test;
```



## <a name="examples"></a>Esempio

Nell'esempio seguente viene utilizzata una macro per definire le righe del cursore.


```
#define CURSOR(top, bottom) (((top) << 8) | (bottom))
```



Nell'esempio seguente viene definita una macro che recupera un numero intero pseudocasuale nell'intervallo specificato.


```
#define getrandom(min, max) \
((rand()%(int)(((max) + 1)-(min)))+ (min))
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Direttive per il preprocessore (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#definire gli overload](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[\#Direttiva undef (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 






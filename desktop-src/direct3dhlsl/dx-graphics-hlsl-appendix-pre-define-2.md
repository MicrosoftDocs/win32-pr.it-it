---
title: '\#define (direttiva) (macro)'
description: Direttiva per il preprocessore che crea una macro simile a una funzione.
ms.assetid: 73c19cf8-fbc5-444b-a51f-dc9f881f397b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a8de5a47fc92c02e9f565c80f600359e8e5b32f9
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104993277"
---
# <a name="define-directive-macro"></a>\#define (direttiva) (macro)

Direttiva per il preprocessore che crea una macro simile a una funzione.



| \#define *Identifier*( *argument0*,..., *argumentn-1* ) *token-String* |
|--------------------------------------------------------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                                                                                                                                                                                          | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*identificatore*<br/>                                                                                                                                                                             | Identificatore della macro. <br/> Una seconda [ \# definizione](dx-graphics-hlsl-appendix-pre-define.md) per una macro con un identificatore già esistente nel contesto corrente genera un errore a meno che la seconda sequenza di token non sia identica alla prima. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="___________argument0___...___argumentN-1_________"></span><span id="___________argument0___...___argumentn-1_________"></span><span id="___________ARGUMENT0___...___ARGUMENTN-1_________"></span> ( *argument0*,..., *argomento-1* ) <br/> | Elenco di argomenti per la macro. L'elenco di argomenti è delimitato da virgole, può essere di qualsiasi lunghezza e deve essere racchiuso tra parentesi. Ogni nome di argomento nell'elenco deve essere univoco. Nessuno spazio vuoto può separare il parametro *Identifier* e la parentesi di apertura. <br/> Utilizzare la concatenazione di righe per inserire una barra rovesciata ( \) immediatamente prima del carattere di nuova riga per suddividere le direttive Long su più righe di origine <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="token-string__optional________"></span><span id="TOKEN-STRING__OPTIONAL________"></span>*stringa* \[ di token opzionale\] <br/>                                                                                                                     | Valore della macro. Questo parametro è costituito da una serie di token, ad esempio parole chiave, costanti o istruzioni complete. Uno o più caratteri di spazio vuoto devono separare questo parametro dal parametro *Identifier* . Questo spazio vuoto non è considerato parte del testo sostituito, né lo spazio vuoto dopo l'ultimo token del testo. Usare le parentesi per assicurarsi che gli argomenti complessi vengano interpretati correttamente. <br/> Se il valore del parametro *Identifier* si verifica all'interno del parametro della *stringa del token* (anche come risultato di un'altra espansione di una macro), non viene espanso. <br/> Se si esclude questo parametro, tutte le istanze del parametro *Identifier* verranno rimosse dal file di origine. L'identificatore rimane definito e può essere testato utilizzando le direttive [ \# if defined](dx-graphics-hlsl-appendix-pre-ifdef.md), \# ifdef e \# ifndef. <br/> |



 

## <a name="remarks"></a>Commenti

Tutte le istanze del parametro *Identifier* che si verificano dopo la direttiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) nel file di origine costituiscono una chiamata di macro e l'identificatore verrà sostituito da una versione del parametro della *stringa di token* con argomenti effettivi sostituiti per i parametri formali. Il numero di parametri nella chiamata deve corrispondere al numero di parametri nella definizione della macro. L'identificatore viene sostituito solo quando costituisce un token. l'identificatore, ad esempio, non viene sostituito se viene visualizzato in un commento, all'interno di una stringa o come parte di un identificatore più lungo.

La direttiva [ \# undef](dx-graphics-hlsl-appendix-pre-undef.md) indica al preprocessore di dimenticare la definizione di un identificatore. per ulteriori informazioni, vedere la \# direttiva undef (DirectX HLSL).

La definizione di costanti con l'opzione del compilatore/D ha lo stesso effetto dell'uso della direttiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) all'inizio del file. Con l'opzione/D è possibile definire fino a 30 macro.

Gli argomenti effettivi nella chiamata della macro vengono associati agli argomenti formali corrispondenti nella definizione della macro. Ogni argomento formale nella stringa del token viene sostituito dall'argomento effettivo corrispondente, a meno che l'argomento non sia preceduto da un operatore per ( \# ), charizing ( \# @) o da un token-Pasting ( \# \# ) o sia seguito da un \# \# operatore. Eventuali macro presenti nell'argomento effettivo vengono espanse prima che la direttiva sostituisca il parametro formale.

Il token incollato nel compilatore HLSL è leggermente diverso da quello del token incollato nel compilatore C, in quanto i token incollati devono essere token validi. Si consideri, ad esempio, la seguente definizione di macro:


```
#define MERGE(a, b) a##b
MERGE(float, 4x4) test;
```



Nel compilatore C, il risultato è il seguente:


```
float4x4 test
```



Nel compilatore HLSL, tuttavia, si ottiene quanto segue:


```
float4 x4 test
```



È possibile ovviare a questo comportamento usando invece la definizione di macro seguente.


```
MERGE(MERGE(float, 4), x4) test;
```



## <a name="examples"></a>Esempio

Nell'esempio seguente viene utilizzata una macro per definire le linee del cursore.


```
#define CURSOR(top, bottom) (((top) << 8) | (bottom))
```



Nell'esempio seguente viene definita una macro che recupera un Integer pseudocasuale nell'intervallo specificato.


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

 

 






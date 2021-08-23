---
title: '\#Direttiva define (costante)'
description: Direttiva del preprocessore che assegna un nome significativo a una costante nell'applicazione.
ms.assetid: cc9b34a3-4c83-4999-99ec-e6261ecb2785
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 06e3992dd81d2ffcc32a672e2d524fa51c1372c02ab90d8b6b8a905100ac9afb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855051"
---
# <a name="define-directive-constant"></a>\#Direttiva define (costante)

Direttiva del preprocessore che assegna un nome significativo a una costante nell'applicazione.



| \#definire *identifiertoken-string* |
|-----------------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*Identificatore*<br/>                                          | Identificatore della costante. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="token-string__optional_"></span><span id="TOKEN-STRING__OPTIONAL_"></span>*token-string* \[ Opzionale\]<br/> | Valore della costante. Questo parametro è costituito da una serie di token, ad esempio parole chiave, costanti o istruzioni complete. Uno o più spazi vuoti devono separare questo parametro dal parametro *identifier.* questo spazio vuoto non viene considerato parte del testo sostituito, né lo spazio vuoto dopo l'ultimo token del testo. <br/> Se si esclude questo parametro, tutte le istanze del parametro *identifier* vengono rimosse dal file di origine. L'identificatore rimane definito e può essere testato usando le direttive [ \# ifdefined](dx-graphics-hlsl-appendix-pre-ifdef.md), \# ifdef e \# ifndef. <br/> |



 

## <a name="remarks"></a>Commenti

Tutte le istanze del *parametro identifier* che si verificano dopo la [ \# direttiva define](dx-graphics-hlsl-appendix-pre-define.md) nel file di origine verranno sostituite dal valore del parametro *token-string.* L'identificatore viene sostituito solo quando forma un token. Ad esempio, l'identificatore non viene sostituito se viene visualizzato in un commento, all'interno di una stringa o come parte di un identificatore più lungo.

La [ \# direttiva undef](dx-graphics-hlsl-appendix-pre-undef.md) indica al preprocessore di dimenticare la definizione di un identificatore. Per altre informazioni, vedere Direttiva \# undef (DirectX HLSL).

La definizione di costanti con l'opzione del compilatore /D ha lo stesso effetto dell'uso della direttiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) all'inizio del file. È possibile definire fino a 30 costanti con l'opzione /D. Per un esempio di come può essere usato, vedere la sezione Esempi di [ \# ifdef e ).](dx-graphics-hlsl-appendix-pre-ifdef.md)

## <a name="examples"></a>Esempio

L'esempio seguente definisce l'identificatore WIDTH come costante integer 80 e quindi definisce LENGTH in termini di WIDTH e la costante integer 10.


```
#define WIDTH       80
#define LENGTH      ( WIDTH + 10 )
```



Ogni istanza successiva di LENGTH viene sostituita da (WIDTH + 10) e ogni istanza successiva di WIDTH + 10 viene sostituita dall'espressione (80 + 10). Le parentesi intorno a WIDTH + 10 sono importanti perché controllano l'interpretazione in istruzioni come le seguenti.


```
var = LENGTH * 20;
```



Dopo la fase di pre-elaborazione, l'istruzione diventa la seguente, che restituisce 1.800.


```
var = ( 80 + 10 ) * 20;
```



Senza parentesi, il risultato sarà il seguente, che restituisce 280.


```
var = 80 + 10 * 20;
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Direttive per il preprocessore (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#definire gli overload](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[\#Direttiva undef (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-undef.md)
</dt> </dl>

 

 






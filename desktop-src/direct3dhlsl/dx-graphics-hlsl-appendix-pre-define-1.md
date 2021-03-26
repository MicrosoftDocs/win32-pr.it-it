---
title: '\#define (direttiva) (costante)'
description: Direttiva per il preprocessore che assegna un nome significativo a una costante nell'applicazione.
ms.assetid: cc9b34a3-4c83-4999-99ec-e6261ecb2785
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: deae1ca92c2280cd31cbec2bf3482c61fcf2b88a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104046132"
---
# <a name="define-directive-constant"></a>\#define (direttiva) (costante)

Direttiva per il preprocessore che assegna un nome significativo a una costante nell'applicazione.



| \#definire *identifiertoken-String* |
|-----------------------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*identificatore*<br/>                                          | Identificatore della costante. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="token-string__optional_"></span><span id="TOKEN-STRING__OPTIONAL_"></span>*stringa* \[ di token opzionale\]<br/> | Valore della costante. Questo parametro è costituito da una serie di token, ad esempio parole chiave, costanti o istruzioni complete. Uno o più caratteri di spazio vuoto devono separare questo parametro dal parametro *Identifier* . Questo spazio vuoto non è considerato parte del testo sostituito, né lo spazio vuoto dopo l'ultimo token del testo. <br/> Se si esclude questo parametro, tutte le istanze del parametro *Identifier* verranno rimosse dal file di origine. L'identificatore rimane definito e può essere testato utilizzando le direttive [ \# if defined](dx-graphics-hlsl-appendix-pre-ifdef.md), \# ifdef e \# ifndef. <br/> |



 

## <a name="remarks"></a>Commenti

Tutte le istanze del parametro *Identifier* che si verificano dopo la direttiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) nel file di origine verranno sostituite dal valore del parametro della *stringa di token* . L'identificatore viene sostituito solo quando costituisce un token. l'identificatore, ad esempio, non viene sostituito se viene visualizzato in un commento, all'interno di una stringa o come parte di un identificatore più lungo.

La direttiva [ \# undef](dx-graphics-hlsl-appendix-pre-undef.md) indica al preprocessore di dimenticare la definizione di un identificatore. per ulteriori informazioni, vedere la \# direttiva undef (DirectX HLSL).

La definizione di costanti con l'opzione del compilatore/D ha lo stesso effetto dell'uso della direttiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) all'inizio del file. Con l'opzione/D è possibile definire fino a 30 costanti. Per un esempio di come è possibile usarlo, vedere la sezione Esempi di [ \# ifdef e](dx-graphics-hlsl-appendix-pre-ifdef.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene definita la larghezza dell'identificatore come costante Integer 80, quindi viene definita la lunghezza in termini di larghezza e la costante Integer 10.


```
#define WIDTH       80
#define LENGTH      ( WIDTH + 10 )
```



Ogni istanza successiva di LENGTH viene sostituita da (WIDTH + 10) e ogni istanza successiva di WIDTH + 10 viene sostituita dall'espressione (80 + 10). Le parentesi attorno alla larghezza + 10 sono importanti perché controllano l'interpretazione nelle istruzioni come le seguenti.


```
var = LENGTH * 20;
```



Dopo la fase di pre-elaborazione l'istruzione diventa la seguente, che restituisce 1.800.


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

 

 






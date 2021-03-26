---
title: " undef (direttiva)"
description: Direttiva per il preprocessore che rimuove la definizione corrente di una costante o di una macro definita in precedenza mediante la direttiva \ define.
ms.assetid: ba6bbe6b-ecfa-40cb-887f-e42b6e22c7bd
keywords:
- Direttiva undef HLSL
topic_type:
- apiref
api_name:
- undef Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7358dc60d002e784394f64773934a18f7413e493
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334031"
---
# <a name="undef-directive"></a>\#undef (direttiva)

Direttiva per il preprocessore che rimuove la definizione corrente di una costante o di una macro definita in precedenza mediante la direttiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) .



| \#*identificatore* undef |
|----------------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                                              | Descrizione                                                                                                                                                      |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*identificatore*<br/> | Identificatore della costante o della macro per cui rimuovere la definizione. Se si sta annientendo la definizione di una macro, fornire solo l'identificatore, non l'elenco di parametri. <br/> |



 

## <a name="remarks"></a>Commenti

È possibile applicare la \# direttiva undef a un identificatore privo di definizione precedente, in modo da garantire che l'identificatore non sia definito. La sostituzione della macro non viene eseguita nelle \# istruzioni undef.

La \# direttiva undef viene in genere abbinata a una direttiva [ \# define](dx-graphics-hlsl-appendix-pre-define.md) per creare un'area in un programma di origine in cui un identificatore ha un significato speciale. Ad esempio, una funzione specifica del programma di origine può utilizzare le costanti manifesto per definire valori specifici dell'ambiente che non influiscono sul resto del programma. La \# direttiva undef funziona anche con la direttiva [) per controllare la compilazione condizionale del programma di origine.

Le costanti e le macro possono essere indefinite dalla riga di comando usando l'opzione/U, seguite dagli identificatori come indefiniti. Questa operazione equivale all'aggiunta di una sequenza di \# direttive undef all'inizio del file di origine.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come utilizzare la \# direttiva undef per rimuovere le definizioni di una costante simbolica e di una macro.


```
#define WIDTH           80
#define ADD( X, Y )     (X) + (Y)

#undef WIDTH
#undef ADD
```



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Direttive per il preprocessore (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#define (direttiva) (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[\#Se,)](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 






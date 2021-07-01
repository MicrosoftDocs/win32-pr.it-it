---
title: Istruzione if
description: Eseguire in modo condizionale una serie di istruzioni in base alla valutazione dell'espressione condizionale.
ms.assetid: ed4e347b-b5ee-40bc-a3f8-36e83ccf45b8
keywords:
- Istruzione if HLSL
topic_type:
- apiref
api_name:
- if Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df4a1f049526422f39c3529395481548943c7e84
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118956"
---
# <a name="if-statement"></a>Istruzione if

Eseguire in modo condizionale una serie di istruzioni in base alla valutazione dell'espressione condizionale.

\[*Attributo* \] if ( *condizionale* ) { *Blocco di istruzioni*; }



 

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Attributo*
</dt> <dd>

Parametro facoltativo che controlla la modalità di compilazione dell'istruzione.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ramo</td>
<td>Valutare solo un lato dell'istruzione if a seconda della condizione specificata.
<blockquote>
[!Note]<br />
Quando si usa <a href="dx-graphics-hlsl-sm2.md">il modello shader 2.x</a> o il modello <a href="dx-graphics-hlsl-sm3.md">shader 3.0,</a>ogni volta che si usa la diramazione dinamica si usano le risorse. Pertanto, se si usa la diramazione dinamica in modo eccessivo quando si usano questi profili come destinazione, è possibile ricevere errori di compilazione.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>rendere bidimensionale</td>
<td>Valutare entrambi i lati dell'istruzione if e scegliere tra i due valori risultanti.</td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span id="Conditional"></span><span id="conditional"></span><span id="CONDITIONAL"></span>*Condizionale*
</dt> <dd>

Espressione [condizionale](dx-graphics-hlsl-expressions.md). L'espressione viene valutata e, se true, viene eseguito il blocco di istruzioni.

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Blocco di istruzioni*
</dt> <dd>

Una o più [istruzioni HLSL](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando il compilatore usa il metodo branch per compilare un'istruzione if, genererà codice che valuterà solo un lato dell'istruzione if a seconda della condizione specificata. Ad esempio, nell'istruzione if:


```
[branch] if(x)
{
    x = sqrt(x);
}
```



**L'istruzione if** ha un blocco else implicito, che equivale a x = x. Poiché è stato detto al compilatore di usare il metodo branch con l'attributo branch precedente, il codice compilato valuterà x ed eseguirà solo il lato che deve essere eseguito; Se x è zero, verrà eseguito il lato **else** e se è diverso da zero verrà eseguito il **lato then.**

Viceversa, se viene usato l'attributo **flatten,** il codice compilato valuterà entrambi i lati dell'istruzione **if** e sceglierà tra i due valori risultanti usando il valore originale di x. Di seguito è riportato un esempio di utilizzo dell'attributo flat:


```
[flatten] if(x)
{
    x = sqrt(x);
}
```



In alcuni casi l'uso del ramo o dell'appiattimento degli attributi può generare un errore di compilazione. L'attributo branch può avere esito negativo se entrambi i lati dell'istruzione if contengono una funzione di sfumatura, ad esempio [**tex2D.**](dx-graphics-hlsl-tex2d.md) L'attributo flat può avere esito negativo se entrambi i lati dell'istruzione if contengono un'istruzione di accodamento del flusso o qualsiasi altra istruzione con effetti collaterali.

**Un'istruzione if** può anche usare un blocco else facoltativo. Se **l'espressione if** è true, viene elaborato il codice nel blocco di istruzioni associato all'istruzione if. In caso contrario, viene elaborato il blocco di istruzioni associato al blocco else facoltativo.

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Controllo di flusso](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 






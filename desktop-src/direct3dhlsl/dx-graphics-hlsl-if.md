---
title: Istruzione if
description: Eseguire in modo condizionale una serie di istruzioni, in base alla valutazione dell'espressione condizionale.
ms.assetid: ed4e347b-b5ee-40bc-a3f8-36e83ccf45b8
keywords:
- Istruzione If HLSL
topic_type:
- apiref
api_name:
- if Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e8a3c20e73b9783d39b4f4cbdb7c0be5b75fcda
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "104046242"
---
# <a name="if-statement"></a>Istruzione if

Eseguire in modo condizionale una serie di istruzioni, in base alla valutazione dell'espressione condizionale.



|                                                               |
|---------------------------------------------------------------|
| \[*Attributo* \] if ( *Conditional* ) { *Block Statement*;} |



 

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
Quando si usa il modello di <a href="dx-graphics-hlsl-sm2.md">shader 2. x</a> o <a href="dx-graphics-hlsl-sm3.md">Shader 3,0</a>, ogni volta che si usa la creazione di rami dinamici si utilizzano le risorse. Quindi, se si usa una diramazione dinamica eccessivamente quando si hanno come destinazione questi profili, è possibile ricevere errori di compilazione.
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

[Espressione](dx-graphics-hlsl-expressions.md)condizionale. L'espressione viene valutata e, se true, viene eseguito il blocco di istruzioni.

</dd> <dt>

<span id="Statement_Block"></span><span id="statement_block"></span><span id="STATEMENT_BLOCK"></span>*Blocco di istruzioni*
</dt> <dd>

Una o più [istruzioni HLSL](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando il compilatore usa il metodo Branch per la compilazione di un'istruzione if, verrà generato codice che valuterà solo un lato dell'istruzione if a seconda della condizione specificata. Ad esempio, nell'istruzione if:


```
[branch] if(x)
{
    x = sqrt(x);
}
```



L'istruzione **if** ha un blocco Else implicito, equivalente a x = x. Poiché è stato indicato al compilatore di usare il metodo Branch con l'attributo Branch precedente, il codice compilato valuterà x ed eseguirà solo il lato che deve essere eseguito. Se x è zero, verrà eseguito il lato **else** e se è diverso da zero, verrà eseguito il lato **then** .

Viceversa, se viene usato l'attributo **Flat** , il codice compilato valuterà entrambi i lati dell'istruzione **if** e sceglierà tra i due valori risultanti usando il valore originale di x. Di seguito è riportato un esempio di utilizzo dell'attributo Flat:


```
[flatten] if(x)
{
    x = sqrt(x);
}
```



In alcuni casi, l'utilizzo degli attributi Branch o flat può generare un errore di compilazione. L'attributo Branch può non riuscire se uno dei lati dell'istruzione if contiene una funzione Gradient, ad esempio [**tex2D**](dx-graphics-hlsl-tex2d.md). L'attributo flat può non riuscire se entrambi i lati dell'istruzione If contengono un'istruzione di Accodamento del flusso o qualsiasi altra istruzione con effetti collaterali.

Un'istruzione **if** può inoltre utilizzare un blocco else facoltativo. Se l'espressione **if** è true, il codice nel blocco di istruzioni associato all'istruzione if viene elaborato. In caso contrario, il blocco di istruzioni associato al blocco else facoltativo viene elaborato.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Controllo di flusso](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

 






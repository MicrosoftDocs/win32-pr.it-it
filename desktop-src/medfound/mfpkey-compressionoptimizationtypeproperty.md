---
description: Specifica le impostazioni di qualità visiva ottimali da usare per il codificatore Windows Media Video 9 Advanced Profile.
ms.assetid: 9449b5fa-4f13-4c33-bfdf-611720e8dd77
title: MFPKEY_COMPRESSIONOPTIMIZATIONTYPE proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7171990280fe004b12c306a09af3b617ba2de0a7cfa274edb3d9191b16a886
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118242880"
---
# <a name="mfpkey_compressionoptimizationtype-property"></a>Proprietà MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE

Specifica le impostazioni di qualità visiva ottimali da usare per il codificatore Windows Media Video 9 Advanced Profile.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCCompressionOptimizationType

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="remarks"></a>Commenti

Questa proprietà consente di configurare rapidamente diverse opzioni di codifica video. Può essere impostato su uno dei valori seguenti.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>Il codec non forza l'ottimizzazione e userà tutte le funzionalità specificate da altre proprietà. In molti casi, il codec userà la logica interna per determinare le impostazioni se non sono specificate. Rappresenta il valore predefinito.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Abilita le funzionalità che produrranno la migliore qualità visiva. L'uso di questo valore consente di configurare il codec come se si fosse impostata la proprietà seguente:<br/>
<ul>
<li><a href="mfpkey-bdeltaqpproperty.md">MFPKEY_BDELTAQP</a> = 1</li>
<li><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a> = 3</li>
<li><a href="mfpkey-loopfilterproperty.md">MFPKEY_LOOPFILTER</a> = 1</li>
<li><a href="mfpkey-motionmatchmethodproperty.md">MFPKEY_MOTIONMATCHMETHOD</a> = -1</li>
<li><a href="mfpkey-motionsearchlevelproperty.md">MFPKEY_MOTIONSEARCHLEVEL</a> = 1</li>
<li><a href="mfpkey-motionsearchrangeproperty.md">MFPKEY_MOTIONSEARCHRANGE</a> = -1</li>
<li><a href="mfpkey-numbframesproperty.md">MFPKEY_NUMBFRAMES</a> = 1</li>
</ul>
Se si imposta una delle proprietà nell'elenco precedente, il valore impostato sostituisce i valori associati a questa impostazione, ad eccezione di MFPKEY_COMPLEXITYEX <a href="mfpkey-complexityexproperty.md">.</a><br/></td>
</tr>
</tbody>
</table>



 

L'impostazione del valore della proprietà MFPKEY COMPRESSIONOPTIMIZATIONTYPE su 1 ha anche l'effetto di impostare l'impostazione del Registro di sistema Dquant Option su 2 e l'impostazione del Registro di sistema \_ Motion Vector Cost Method su 1. Per altre informazioni, vedere l'articolo Web [Using the Advanced Impostazioni of the Windows Media Video 9 Advanced Profile Codec](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 





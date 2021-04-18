---
description: Specifica le impostazioni ottimali per la qualità visiva da usare per il codificatore di profili avanzato Windows Media Video 9.
ms.assetid: 9449b5fa-4f13-4c33-bfdf-611720e8dd77
title: Proprietà MFPKEY_COMPRESSIONOPTIMIZATIONTYPE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3000caa10aa7db7d201cd11fd9a189fd6ac33591
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310647"
---
# <a name="mfpkey_compressionoptimizationtype-property"></a>\_Proprietà COMPRESSIONOPTIMIZATIONTYPE di MFPKEY

Specifica le impostazioni ottimali per la qualità visiva da usare per il codificatore di profili avanzato Windows Media Video 9.

## <a name="constant-for-ipropertybag"></a>Costante per IPropertyBag

g \_ wszWMVCCompressionOptimizationType

## <a name="data-type"></a>Tipo di dati

VT \_ I4

## <a name="default-value"></a>Valore predefinito

0

## <a name="remarks"></a>Commenti

Questa proprietà fornisce un modo rapido per configurare una serie di opzioni di codifica video. Può essere impostato su uno dei valori seguenti.



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
<td>Il codec non forza l'ottimizzazione e utilizzerà tutte le funzionalità specificate da altre proprietà. In molti casi, il codec userà la logica interna per determinare le impostazioni se non sono specificate. Rappresenta il valore predefinito.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Abilita le funzionalità che produrranno la qualità visiva migliore. L'uso di questo valore consente di configurare il codec come se fossero state impostate le proprietà seguenti:<br/>
<ul>
<li><a href="mfpkey-bdeltaqpproperty.md">MFPKEY_BDELTAQP</a> = 1</li>
<li><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a> = 3</li>
<li><a href="mfpkey-loopfilterproperty.md">MFPKEY_LOOPFILTER</a> = 1</li>
<li><a href="mfpkey-motionmatchmethodproperty.md">MFPKEY_MOTIONMATCHMETHOD</a> =-1</li>
<li><a href="mfpkey-motionsearchlevelproperty.md">MFPKEY_MOTIONSEARCHLEVEL</a> = 1</li>
<li><a href="mfpkey-motionsearchrangeproperty.md">MFPKEY_MOTIONSEARCHRANGE</a> =-1</li>
<li><a href="mfpkey-numbframesproperty.md">MFPKEY_NUMBFRAMES</a> = 1</li>
</ul>
Se si imposta una delle proprietà nell'elenco precedente, il valore impostato sostituisce i valori associati a questa impostazione, ad eccezione di <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.<br/></td>
</tr>
</tbody>
</table>



 

Impostando il valore della \_ Proprietà COMPRESSIONOPTIMIZATIONTYPE di MFPKEY su 1, l'impostazione dell'opzione DQuant del registro di sistema è impostata su 2 e l'impostazione del registro di sistema del metodo di costo del vettore di movimento su 1. Per altre informazioni, vedere l'articolo relativo all' [uso delle impostazioni avanzate del codec del profilo avanzato Windows Media video 9](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 





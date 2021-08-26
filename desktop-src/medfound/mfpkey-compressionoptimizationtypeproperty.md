---
description: Specifica le impostazioni di qualità visiva ottimali da usare per il codificatore Windows Media Video 9 Advanced Profile.
ms.assetid: 9449b5fa-4f13-4c33-bfdf-611720e8dd77
title: MFPKEY_COMPRESSIONOPTIMIZATIONTYPE proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e140a854999a5c634620d98958e40832acbe9439
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471727"
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




| valore | Descrizione | 
|-------|-------------|
| 0 | Il codec non forza l'ottimizzazione e userà tutte le funzionalità specificate da altre proprietà. In molti casi, il codec userà la logica interna per determinare le impostazioni se non vengono specificate. Rappresenta il valore predefinito. | 
| 1 | Abilita le funzionalità che produrranno la migliore qualità visiva. L'uso di questo valore consente di configurare il codec come se si impostano le proprietà seguenti:<br /><ul><li><a href="mfpkey-bdeltaqpproperty.md">MFPKEY_BDELTAQP</a> = 1</li><li><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a> = 3</li><li><a href="mfpkey-loopfilterproperty.md">MFPKEY_LOOPFILTER</a> = 1</li><li><a href="mfpkey-motionmatchmethodproperty.md">MFPKEY_MOTIONMATCHMETHOD</a> = -1</li><li><a href="mfpkey-motionsearchlevelproperty.md">MFPKEY_MOTIONSEARCHLEVEL</a> = 1</li><li><a href="mfpkey-motionsearchrangeproperty.md">MFPKEY_MOTIONSEARCHRANGE</a> = -1</li><li><a href="mfpkey-numbframesproperty.md">MFPKEY_NUMBFRAMES</a> = 1</li></ul>Se si imposta una delle proprietà nell'elenco precedente, il valore impostato sostituisce i valori associati a questa impostazione, ad eccezione di <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.<br /> | 




 

L'impostazione del valore della proprietà MFPKEY COMPRESSIONOPTIMIZATIONTYPE su 1 ha anche l'effetto dell'impostazione del Registro di sistema Dquant Option su 2 e dell'impostazione del Registro di sistema \_ Motion Vector Cost Method su 1. Per altre informazioni, vedere l'articolo Web [Using the Advanced Impostazioni of the Windows Media Video 9 Advanced Profile Codec](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx).

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> </dl>

 

 





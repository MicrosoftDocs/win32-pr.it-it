---
description: Specifica i limiti dell'area di interesse, che indica l'area del frame che richiede una qualità diversa.
ms.assetid: F06CACF0-AE75-4707-8CD0-7BA7D51BB80A
title: Attributo MFSampleExtension_ROIRectangle (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71d84d2054caa96feaf7bfb4ccc7a91ecf4ac9f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310233"
---
# <a name="mfsampleextension_roirectangle-attribute"></a>\_Attributo ROIRectangle di MFSampleExtension

Specifica i limiti dell'area di interesse, che indica l'area del frame che richiede una qualità diversa.

## <a name="data-type"></a>Tipo di dati

**[**ROI \_ AREA**](/windows/desktop/api/mfapi/ns-mfapi-roi_area)** archiviata come **BLOB**

## <a name="remarks"></a>Commenti

Dopo aver impostato correttamente [CODEcapis \_ AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) su un valore diverso da zero in un codificatore MFT, l'applicazione può impostare questo attributo sugli esempi di input e aspettarsi che venga rispettato.

Se [CODEcapis \_ AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) non è impostato su un valore diverso da zero, l' \_ attributo MFSampleExtension ROIRectangle viene ignorato negli esempi di input.

MFSampleExtension \_ ROIRectangle è impostato su un esempio di input e viene applicato solo all'esempio di input corrente.

Il campo **QPDelta** nella struttura [**dell' \_ area del ROI**](/windows/desktop/api/mfapi/ns-mfapi-roi_area) specifica il Delta del parametro di quantizzazione per l'area specificata dal resto del frame. Se **QPDelta** è un valore positivo, significa che l'applicazione desidera che il rettangolo abbia una qualità inferiore rispetto al resto del frame.

**Codificatori H. 264/AVC:** **QPDelta** deve essere compreso tra \[ -25, + 25 \] . Il codificatore deve garantire che la versione QP finale sia in un intervallo valido per il video standard.

Non è necessario che l'area specificata sia MB allineata. I codificatori hanno la possibilità di decidere il limite effettivo. Si consiglia di coprire l'intera area specificata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App \[ desktop di Windows 8.1 app \| UWP\]<br/>                                |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 R2 \[ \| UWP\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 





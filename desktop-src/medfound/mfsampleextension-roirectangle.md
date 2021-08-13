---
description: Specifica i limiti dell'area di interesse che indica l'area del frame che richiede una qualità diversa.
ms.assetid: F06CACF0-AE75-4707-8CD0-7BA7D51BB80A
title: MFSampleExtension_ROIRectangle attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 311b17cab20de16a83d145563e8ba0b8ead6f055428ffc6a3823c99deab05fc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118240326"
---
# <a name="mfsampleextension_roirectangle-attribute"></a>Attributo ROIRectangle di MFSampleExtension \_

Specifica i limiti dell'area di interesse che indica l'area del frame che richiede una qualità diversa.

## <a name="data-type"></a>Tipo di dati

**[**ROI \_ AREA**](/windows/desktop/api/mfapi/ns-mfapi-roi_area)** archiviata come **BLOB**

## <a name="remarks"></a>Commenti

Dopo aver impostato [correttamente CODECAPI \_ AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) su un valore diverso da zero in un codificatore MFT, l'applicazione può impostare questo attributo sugli esempi di input e aspettarsi che venga rispettato.

Se [CODECAPI \_ AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md) non è impostato su un valore diverso da zero, l'attributo ROIRectangle di MFSampleExtension viene ignorato sugli esempi \_ di input.

MFSampleExtension ROIRectangle è impostato su un esempio di input e \_ viene applicato solo all'esempio di input corrente.

Il **campo QPDelta** nella [**struttura ROI \_ AREA**](/windows/desktop/api/mfapi/ns-mfapi-roi_area) specifica il delta del parametro di quantizzazione per l'area specificata rispetto al resto del frame. Se **QPDelta** è positivo, significa che l'applicazione vuole che il rettangolo abbia una qualità inferiore rispetto al resto del frame.

**Codificatori H.264/AVC:** **QPDelta** deve essere compreso tra \[ -25 e +25 \] . Il codificatore deve assicurarsi che il QP finale sia in un intervallo valido per lo standard video.

L'area specificata non deve essere allineata in MB. I codificatori hanno la flessibilità di decidere il limite effettivo. È consigliabile coprire l'intera area specificata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 app desktop \| app UWP\]<br/>                                |
| Server minimo supportato<br/> | Windows Server 2012 App \[ UWP per app desktop \| R2\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 





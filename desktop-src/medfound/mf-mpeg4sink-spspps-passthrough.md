---
description: Specifica se il sink di file MPEG-4 filtra i set di parametri di sequenza (SPS) e il set di parametri immagine (PPS) NALUs.
ms.assetid: B2574BE5-6334-4ED2-A008-86326CDC13B8
title: Attributo MF_MPEG4SINK_SPSPPS_PASSTHROUGH (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3c02f4f1cdcac17a104b5061c8899c92e0ad824
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754274"
---
# <a name="mf_mpeg4sink_spspps_passthrough-attribute"></a>\_ \_ Attributo passthrough MPEG4SINK SPSPPS MF \_

Specifica se il [**sink di file MPEG-4**](mpeg-4-file-sink.md) filtra i set di parametri di sequenza (SPS) e il set di parametri immagine (PPS) NALUs.

## <a name="data-type"></a>Tipo di dati

**Bool** archiviato come **UInt32**

## <a name="applies-to"></a>Si applica a

[**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="remarks"></a>Commenti

Il [**sink di file MPEG-4**](mpeg-4-file-sink.md) scrive i parametri SPS e PPS nella casella Descrizione di esempio del file MP4. Per impostazione predefinita, filtra i NALUs SPS e PPS dal flusso video. Per eseguire l'override di questo comportamento, impostare l' \_ \_ attributo passthrough MF MPEG4SINK SPSPPS \_ su **true**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 





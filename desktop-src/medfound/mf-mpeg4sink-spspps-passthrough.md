---
description: Specifica se il sink di file MPEG-4 filtra i set di parametri di sequenza (SPS) e le unità NALU del set di parametri immagine (PPS).
ms.assetid: B2574BE5-6334-4ED2-A008-86326CDC13B8
title: MF_MPEG4SINK_SPSPPS_PASSTHROUGH attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b939302999fc7e095abbc97aed5910976972c860440a2c865248949e0f052aa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104627"
---
# <a name="mf_mpeg4sink_spspps_passthrough-attribute"></a>Attributo \_ MF MPEG4SINK \_ SPSPPS \_ PASSTHROUGH

Specifica se il sink di [**file MPEG-4**](mpeg-4-file-sink.md) filtra i set di parametri di sequenza (SPS) e le unità NALU del set di parametri immagine (PPS).

## <a name="data-type"></a>Tipo di dati

**BOOL** archiviato come **UINT32**

## <a name="applies-to"></a>Si applica a

[**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="remarks"></a>Commenti

Il [**sink di file MPEG-4**](mpeg-4-file-sink.md) scrive i parametri SPS e PPS nella casella di descrizione di esempio del file MP4. Per impostazione predefinita, filtra le unità NALU SPS e PPS dal flusso video. Per eseguire l'override di questo comportamento, impostare l'attributo \_ MF MPEG4SINK \_ SPSPPS \_ PASSTHROUGH su **TRUE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                  |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 





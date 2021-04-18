---
description: Imposta la priorità di base per i thread di elaborazione audio creati dal reader di origine o dal writer del sink.
ms.assetid: C0E3A472-959F-4F74-8906-03630DE4CB8C
title: Attributo MF_READWRITE_MMCSS_PRIORITY_AUDIO (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c33f3e4cab26a448c3b5a28c6f3cfe631a7c1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308463"
---
# <a name="mf_readwrite_mmcss_priority_audio-attribute"></a>\_ \_ \_ Attributo audio Priority ReadWrite MMCSS MF \_

Imposta la priorità di base per i thread di elaborazione audio creati dal reader di origine o dal writer del sink.

## <a name="data-type"></a>Tipo di dati

**Int32** archiviato come **UInt32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="remarks"></a>Commenti

Facoltativamente, impostare questo attributo quando si crea un'istanza di [Reader di origine](source-reader.md) o di [sink writer](sink-writer.md). Se si imposta questo attributo, impostare anche l' [attributo \_ \_ audio della \_ classe \_ MF ReadWrite MMCSS](mf-readwrite-mmcss-class-audio.md) . In caso contrario, questo attributo viene ignorato.

Quando l'utilità di lettura di origine o il writer di sink registra i thread di elaborazione audio con il [servizio Utilità di pianificazione classi multimediali](../procthread/multimedia-class-scheduler-service.md), il valore di questo attributo specifica la priorità del thread di base. Se questo attributo non è impostato, il valore predefinito è zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 

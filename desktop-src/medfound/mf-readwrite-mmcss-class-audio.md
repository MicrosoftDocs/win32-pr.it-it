---
description: Specifica una classe di servizio Utilità di pianificazione classi multimediali (MMCSS) per i thread di elaborazione audio nel Reader di origine o nel writer del sink.
ms.assetid: F1B8A8C8-2E41-4321-A94D-C50447C69941
title: Attributo MF_READWRITE_MMCSS_CLASS_AUDIO (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa35db710c6b72c103855fa2c0a9f169f49c4511
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308464"
---
# <a name="mf_readwrite_mmcss_class_audio-attribute"></a>\_ \_ \_ Attributo audio della classe MF ReadWrite MMCSS \_

Specifica una classe di [servizio Utilità di pianificazione classi multimediali](../procthread/multimedia-class-scheduler-service.md) (MMCSS) per i thread di elaborazione audio nel Reader di origine o nel writer del sink.

## <a name="data-type"></a>Tipo di dati

**LPWSTR**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Per impostare questo attributo, chiamare [**IMFAttributes:: sestring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Commenti

Facoltativamente, impostare questo attributo quando si crea un'istanza di [Reader di origine](source-reader.md) o di [sink writer](sink-writer.md). Il valore dell'attributo deve essere un nome di classe MMCSS valido.

Se questo attributo è impostato, il writer di origine o il writer di sink registra i thread di elaborazione audio con la classe MMCSS specificata. Il MMCSS garantisce che l'elaborazione dei dati in Reader di origine o writer di sink abbia la priorità rispetto ad altre attività di sistema.

Per specificare la priorità di base per i thread audio, impostare l'attributo [MF \_ ReadWrite \_ MMCSS \_ Priority \_ audio](mf-readwrite-mmcss-priority-audio.md) . Se tale attributo non è impostato, la priorità di base per i thread audio è zero.

Questo attributo sostituisce l'attributo della [ \_ \_ \_ classe MF ReadWrite MMCSS](mf-readwrite-mmcss-class.md) per i thread di elaborazione audio. Se non è impostato alcun attributo, i thread audio non vengono registrati con MCSS.

Per la maggior parte delle applicazioni, la glitching audio è molto più evidente all'utente rispetto alla glitch video e pertanto meno accettabile. Per questo motivo, un'applicazione deve in genere impostare \_ l' \_ \_ audio della classe MF ReadWrite MMCSS \_ su una classe MMCSS con priorità superiore rispetto alla [ \_ classe MF ReadWrite \_ MMCSS \_ ](mf-readwrite-mmcss-class.md). In questo modo si garantisce che l'elaborazione audio disponga di una priorità più elevata rispetto ad altre attività.

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

 

 

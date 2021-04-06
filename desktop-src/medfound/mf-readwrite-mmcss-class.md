---
description: Specifica una classe di servizio Utilità di pianificazione classi multimediali (MMCSS) per il writer del sink o del lettore di origine.
ms.assetid: A3A295E8-AC9C-4641-ADDA-B97D5AB13A9A
title: Attributo MF_READWRITE_MMCSS_CLASS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d2088ba09bf4f8ad9516d9b2117ab54161d7ac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759077"
---
# <a name="mf_readwrite_mmcss_class-attribute"></a>\_Attributo della classe MF ReadWrite \_ MMCSS \_

Specifica una classe di [servizio Utilità di pianificazione classi multimediali](../procthread/multimedia-class-scheduler-service.md) (MMCSS) per il writer del sink o del lettore di origine.

## <a name="data-type"></a>Tipo di dati

**LPWSTR**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Per impostare questo attributo, chiamare [**IMFAttributes:: sestring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Commenti

Facoltativamente, impostare questo attributo quando si crea un'istanza di [Reader di origine](source-reader.md) o di [sink writer](sink-writer.md). Il valore dell'attributo deve essere un nome di classe MMCSS valido.

Se questo attributo è impostato, il writer di origine o di sink registra tutti i relativi thread con la classe MMCSS specificata. Il MMCSS garantisce che l'elaborazione dei dati in Reader di origine o writer di sink abbia la priorità rispetto ad altre attività di sistema.

Per specificare la priorità di base, impostare l'attributo di [ \_ \_ \_ Priorità MF ReadWrite MMCSS](mf-readwrite-mmcss-priority.md) . Se tale attributo non è impostato, la priorità di base è zero.

Per i thread di elaborazione audio, l'attributo [ \_ audio della classe MF ReadWrite \_ MMCSS \_ \_ ](mf-readwrite-mmcss-class-audio.md) (se impostato) esegue l'override di questo attributo.

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

 

 

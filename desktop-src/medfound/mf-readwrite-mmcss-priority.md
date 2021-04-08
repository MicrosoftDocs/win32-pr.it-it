---
description: Imposta la priorità del thread di base per il writer del sink o del lettore di origine.
ms.assetid: 9513AE28-2AF4-45EC-AC19-C0718540E26F
title: Attributo MF_READWRITE_MMCSS_PRIORITY (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad7b83485b49e6ae584a38024e180f37c878d27d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058211"
---
# <a name="mf_readwrite_mmcss_priority-attribute"></a>\_Attributo di \_ priorità MMCSS MF ReadWrite \_

Imposta la priorità del thread di base per il writer del sink o del lettore di origine.

## <a name="data-type"></a>Tipo di dati

**Int32** archiviato come **UInt32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="remarks"></a>Commenti

Facoltativamente, impostare questo attributo quando si crea un'istanza di [Reader di origine](source-reader.md) o di [sink writer](sink-writer.md). Se si imposta questo attributo, impostare anche l'attributo della [ \_ \_ \_ classe MF ReadWrite MMCSS](mf-readwrite-mmcss-class.md) . In caso contrario, questo attributo viene ignorato.

Quando i thread vengono registrati con il [servizio Utilità di pianificazione classi multimediali](../procthread/multimedia-class-scheduler-service.md), il valore di questo attributo viene specificato dalla priorità del thread di base. Se questo attributo non è impostato, il valore predefinito è zero.

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

 

 

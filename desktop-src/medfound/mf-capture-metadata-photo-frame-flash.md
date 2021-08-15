---
description: Indica se è stata attivata una memoria flash per il frame acquisito.
ms.assetid: CF900CB4-8967-40F3-B60C-867192A641E9
title: MF_CAPTURE_METADATA_PHOTO_FRAME_FLASH attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a885786674c524b382912100171502dba78a010b2169738233b5aaad88ed701a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973920"
---
# <a name="mf_capture_metadata_photo_frame_flash-attribute"></a>Attributo MF \_ CAPTURE METADATA PHOTO FRAME \_ \_ \_ \_ FLASH

Indica se è stata attivata una memoria flash per il frame acquisito.

## <a name="data-type"></a>Tipo di dati

**UINT32**



| Valore                                                                               | Significato                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>        | In questo frame non è stata attivata una memoria flash.<br/>                                                                                                   |
| <dl> <dt>non zero</dt> </dl> | È stata attivata una memoria flash in questo frame.<br/>                                                                                                       |
| <dl> <dt>1</dt> </dl>        | Riservato<br/> Non verificare in modo esplicito il valore 1. Le applicazioni devono controllare solo !=0 per indicare se è stata attivata una memoria flash.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                       |
| Server minimo supportato<br/> | Windows Server 2012 Solo \[ app desktop R2\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 





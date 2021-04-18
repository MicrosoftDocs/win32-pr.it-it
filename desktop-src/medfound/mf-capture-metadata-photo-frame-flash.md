---
description: Indica se è stato attivato un flash per il frame acquisito.
ms.assetid: CF900CB4-8967-40F3-B60C-867192A641E9
title: Attributo MF_CAPTURE_METADATA_PHOTO_FRAME_FLASH (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ff5e9a47c07c8d7a2cec4e7dbf7b34669301122
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309575"
---
# <a name="mf_capture_metadata_photo_frame_flash-attribute"></a>\_ \_ \_ \_ Attributo fotogramma Flash per \_ l'acquisizione di metadati MF

Indica se è stato attivato un flash per il frame acquisito.

## <a name="data-type"></a>Tipo di dati

**UINT32**



| Valore                                                                               | Significato                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>        | Un flash non è stato attivato in questo frame.<br/>                                                                                                   |
| <dl> <dt>non zero</dt> </dl> | Un flash è stato attivato su questo frame.<br/>                                                                                                       |
| <dl> <dt>1</dt> </dl>        | Riservato<br/> Non verificare in modo esplicito il valore 1. Le applicazioni devono verificare solo! = 0 per indicare se è stato attivato un flash.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                       |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 





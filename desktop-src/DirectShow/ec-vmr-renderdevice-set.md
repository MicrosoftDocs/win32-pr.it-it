---
description: Inviato quando VMR ha selezionato il meccanismo di rendering.
ms.assetid: 815d1254-c6e3-4a6c-ba4a-bf3da7d35d1f
title: EC_VMR_RENDERDEVICE_SET (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9855b23e25a2c3b955c1499b9505efffcc5637e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329482"
---
# <a name="ec_vmr_renderdevice_set"></a>\_set di \_ RENDERDEVICE \_ VMR EC

Inviato quando VMR ha selezionato il meccanismo di rendering.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Può essere uno dei valori seguenti:



| Valore                        | Significato                                                  |
|------------------------------|----------------------------------------------------------|
| \_ \_ sovrimpressione del dispositivo di rendering VMR \_ | VMR eseguirà il rendering nella superficie della sovrimpressione (solo VMR-7). |
| \_VIDMEM del \_ dispositivo di rendering VMR \_  | Il VMR eseguirà il rendering nella memoria video.                     |
| \_SYSMEM del \_ dispositivo di rendering VMR \_  | Il VMR eseguirà il rendering nella memoria di sistema (solo VMR-7).       |



 

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo evento viene inviato sia da VMR-7 che da VMR-9 e viene inoltrato alle applicazioni. Si noti che VMR-9 supporta solo le destinazioni di rendering della memoria video.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di notifica degli eventi](event-notification-codes.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 





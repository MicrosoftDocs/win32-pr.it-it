---
description: Inviato quando la macchina virtuale ha selezionato il meccanismo di rendering.
ms.assetid: 815d1254-c6e3-4a6c-ba4a-bf3da7d35d1f
title: EC_VMR_RENDERDEVICE_SET (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc2c8bef78156c4438e1e4e7aea45326562002ed8f4a3786377d7ee43a00a57c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015859"
---
# <a name="ec_vmr_renderdevice_set"></a>EC \_ VMR \_ RENDERDEVICE \_ SET

Inviato quando la macchina virtuale ha selezionato il meccanismo di rendering.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Può essere uno dei valori seguenti:



| Valore                        | Significato                                                  |
|------------------------------|----------------------------------------------------------|
| VMR \_ RENDER \_ DEVICE \_ OVERLAY | Il rendering della macchina virtuale verrà eseguito sulla superficie di sovrapposizione (solo VMR-7). |
| VMR \_ RENDER \_ DEVICE \_ VIDMEM  | Il rendering della macchina virtuale verrà eseguito nella memoria video.                     |
| VMR \_ RENDER \_ DEVICE \_ SYSMEM  | Il rendering della macchina virtuale verrà eseguito nella memoria di sistema (solo VMR-7).       |



 

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo evento viene inviato sia da VMR-7 che da VMR-9 e viene inoltrato alle applicazioni. Si noti che VMR-9 supporta solo destinazioni di rendering della memoria video.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di notifica degli eventi](event-notification-codes.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 





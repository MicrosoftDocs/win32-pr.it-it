---
description: Inviato quando viene avviato un set di comandi di spostamento su DVD.
ms.assetid: 9cdcb211-a9e3-4a15-81bd-7ada2b9d823a
title: EC_DVD_BeginNavigationCommands (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BeginNavigationCommands
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: cda904c4fcc0b1acdd16c8fc4596eef332140ec4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331286"
---
# <a name="ec_dvd_beginnavigationcommands"></a>\_BeginNavigationCommands DVD \_ EC

Inviato quando viene avviato un set di comandi di spostamento su DVD.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valore dell'enumerazione [**\_ NavCmdType DVD**](/windows/win32/api/strmif/ne-strmif-dvd_navcmdtype) .

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo evento è disabilitato per impostazione predefinita. Per abilitare questo evento, chiamare [**IDVDControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) e impostare l'opzione **DVD \_ EnableLoggingEvents** su **true**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdevcode. h (include dshow. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> <dt>

[Codici di notifica degli eventi DVD](dvd-notification-codes.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 





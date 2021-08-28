---
description: Inviato quando cambia il set di titoli video (VTS) corrente.
ms.assetid: 7b8849c8-c71e-44d6-b33a-8e80247bdb22
title: EC_DVD_TITLE_SET_CHANGE (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_TITLE_SET_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: a2e6c1dcc60b0b0ef74e40f235ba0b3d16b4288e0225e0ca92270d2d03f3ccd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965551"
---
# <a name="ec_dvd_title_set_change"></a>MODIFICA \_ DEL SET DI TITOLI DEL DVD \_ \_ \_ EC

Inviato quando cambia il set di titoli video (VTS) corrente.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Nuovo numero di set di titoli video (VTSN).

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo evento è disabilitato per impostazione predefinita. Per abilitare questo evento, chiamare [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) e impostare l'opzione **DVD \_ NotifyPositionChange** su **TRUE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dvdevcode.h (includere Dshow.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> <dt>

[Codici di notifica degli eventi DVD](dvd-notification-codes.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 





---
description: Inviato quando lo strumento di navigazione DVD elabora un comando di navigazione DVD.
ms.assetid: 95e502b6-330f-4bc7-8adc-851913987370
title: EC_DVD_NavigationCommand (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_NavigationCommand
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 6fbca42d3a9f0056bfd040b49e1426275a71bd7e6aaa8a71032389ab636f4cfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119303361"
---
# <a name="ec_dvd_navigationcommand"></a>EC \_ DVD \_ NavigationCommand

Inviato quando lo strumento [di navigazione DVD](dvd-navigator-filter.md) elabora un comando di navigazione DVD.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

32 bit inferiori del comando di navigazione non elaborato.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

32 bit superiori del comando di navigazione non elaborato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo evento è disabilitato per impostazione predefinita. Per abilitare questo evento, chiamare [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) e impostare l'opzione **\_ DVD EnableLoggingEvents** su **TRUE.**

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

 

 





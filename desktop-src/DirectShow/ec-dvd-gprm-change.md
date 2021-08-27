---
description: Inviato quando il valore di un registro di parametri generali (GPRM) cambia.
ms.assetid: 3e0c400e-9ea5-458c-9eca-97d66a440590
title: EC_DVD_GPRM_Change (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_GPRM_Change
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: b1d6613475a3c61640a7b6b5f5c53bc1baab52c1a69ec3d3c8b7a0e32f91928c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079151"
---
# <a name="ec_dvd_gprm_change"></a>Modifica \_ \_ GPRM del DVD \_ EC

Inviato quando il valore di un registro di parametri generali (GPRM) cambia.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Indice in base zero del valore GPRM modificato.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

I 16 bit inferiori contengono il nuovo valore GPRM.

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
</dt> <dt>

[**IDvdInfo2::GetAllGPRMs**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallgprms)
</dt> </dl>

 

 





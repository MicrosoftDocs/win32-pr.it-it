---
description: Segnala che il numero di angoli disponibili è cambiato o che il numero di angolo corrente è cambiato.
ms.assetid: 0564b0e3-6434-448b-80fb-5362ab67fef7
title: EC_DVD_ANGLE_CHANGE (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ANGLE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: a9a94b9940f58dc26de1c1ba6133e4d5a66a2f34ef96b8aaf59b1a7815a08122
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148594"
---
# <a name="ec_dvd_angle_change"></a>EC \_ DVD \_ ANGLE \_ CHANGE

Segnala che il numero di angoli disponibili è cambiato o che il numero di angolo corrente è cambiato.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**Valore DWORD** che indica il numero di angoli disponibili. Quando il numero di angoli disponibili è 1, il video corrente non è multiangle.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

**Valore DWORD** che indica il numero di angolo corrente.

</dd> </dl>

## <a name="remarks"></a>Commenti

I numeri di angolo sono compreso tra 1 e 9.

Il numero di angolo corrente può cambiare automaticamente con un comando di navigazione creato sul disco e tramite il controllo dell'applicazione tramite [**l'interfaccia IDvdControl2.**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)

Questo evento viene generato in tutti i domini.

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

 

 





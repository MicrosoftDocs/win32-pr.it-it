---
description: Segnala una condizione di errore DVD.
ms.assetid: 2cd3e0c4-e2b7-4aa1-9f3c-9003eabfb08a
title: EC_DVD_ERROR (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ERROR
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c0afa9ce750016001ddbe054d8cb9a589a2c68d8856e8e4db5c59043eb881129
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820528"
---
# <a name="ec_dvd_error"></a>ERRORE \_ DEL DVD \_ EC

Segnala una condizione di errore DVD.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**Valore DWORD** che indica la condizione di errore. Membro del tipo [**di dati enumerato \_ DVD ERROR.**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error)

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Il significato dipende dal valore di *lParam1*. Per [**altre \_ informazioni, vedere ERRORE DVD.**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_error)

</dd> </dl>

## <a name="remarks"></a>Commenti

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

 

 





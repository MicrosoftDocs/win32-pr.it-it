---
description: Segnala che è stato inserito un disco DVD nell'unità.
ms.assetid: ce233c94-2eae-457c-919b-7c4d8334979a
title: EC_DVD_DISC_INSERTED (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_DISC_INSERTED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: c98d32960e2ab6a21633899164b3ff84525f2aaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327430"
---
# <a name="ec_dvd_disc_inserted"></a>\_disco DVD \_ EC \_ inserito

Segnala che è stato inserito un disco DVD nell'unità.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Zero.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="remarks"></a>Commenti

La riproduzione inizia automaticamente quando viene inserito un disco. L'applicazione non deve eseguire alcuna azione speciale in risposta a questo evento.

Questo evento viene generato in tutti i domini.

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

 

 





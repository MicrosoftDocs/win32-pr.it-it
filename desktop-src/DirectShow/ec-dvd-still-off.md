---
description: Segnala la fine di qualsiasi oggetto (PGC, Cell o VOBU).
ms.assetid: 459464b1-3085-4ad7-8eb3-960cee89d395
title: EC_DVD_STILL_OFF (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_STILL_OFF
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 406f51ebe380490affd618c3af0a3d2a0e428f8ffbeb0685eb0e0693a6f01132
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906021"
---
# <a name="ec_dvd_still_off"></a>EC \_ DVD \_ STILL \_ OFF

Segnala la fine di qualsiasi oggetto (PGC, Cell o VOBU).

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

Questo evento indica che tutti gli oggetti attualmente attivi sono ancora stati rilasciati.

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

 

 





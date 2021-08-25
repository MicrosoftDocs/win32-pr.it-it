---
description: Indica il nuovo dominio del lettore DVD.
ms.assetid: 4faa46d6-2ba2-44a3-b237-acac3b32f8b1
title: EC_DVD_DOMAIN_CHANGE (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_DOMAIN_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: a43c44e779d8ad64852b673fb053467687c50daec85acb9bc87999675200d5f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965661"
---
# <a name="ec_dvd_domain_change"></a>MODIFICA DEL \_ DOMINIO DEL DVD \_ \_ EC

Indica il nuovo dominio del lettore DVD.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**Valore DWORD** che indica il nuovo dominio. Membro del tipo [**di dati enumerato \_ DVD DOMAIN.**](/windows/win32/api/strmif/ne-strmif-dvd_domain)

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il lettore DVD segnala questo evento ogni volta che cambia dominio.

Questo evento viene generato in tutti i domini DVD.

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

 

 





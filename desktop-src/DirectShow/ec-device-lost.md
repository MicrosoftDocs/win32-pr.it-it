---
description: Un Plug and Play dispositivo è stato rimosso o è stato nuovamente disponibile.
ms.assetid: 0640ba96-22a5-4b82-bd9f-117b67dee311
title: EC_DEVICE_LOST (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4868890967d6448226c1f000ab06b7ccbcf7a06e3062d1cdef03e0ad960bc7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998161"
---
# <a name="ec_device_lost"></a>DISPOSITIVO \_ EC \_ PERSO

Un Plug and Play dispositivo è stato rimosso o è stato nuovamente disponibile.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**IUnknown** \* ) Puntatore **all'interfaccia IUnknown** del filtro che rappresenta il dispositivo.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero se il dispositivo è stato rimosso oppure 1 se il dispositivo è nuovamente disponibile.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

No.

## <a name="remarks"></a>Osservazioni

Quando il dispositivo diventa nuovamente disponibile, lo stato precedente del filtro di dispositivo non è più valido. L'applicazione deve ricompilare il grafo per poter usare il dispositivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Notifica di rimozione del dispositivo](device-removal-notification.md)
</dt> <dt>

[Codici di notifica degli eventi](event-notification-codes.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 





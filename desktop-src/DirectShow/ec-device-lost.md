---
description: Un dispositivo Plug and Play è stato rimosso o è stato nuovamente disponibile.
ms.assetid: 0640ba96-22a5-4b82-bd9f-117b67dee311
title: EC_DEVICE_LOST (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81fa3f6368e85f8dc54ca6fd8cc2e0eee21262a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331117"
---
# <a name="ec_device_lost"></a>\_dispositivo EC \_ perso

Un dispositivo Plug and Play è stato rimosso o è stato nuovamente disponibile.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**IUnknown** \* ) Puntatore all'interfaccia **IUnknown** del filtro che rappresenta il dispositivo.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero se il dispositivo è stato rimosso oppure 1 se il dispositivo è nuovamente disponibile.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

No.

## <a name="remarks"></a>Osservazioni

Quando il dispositivo diventa nuovamente disponibile, lo stato precedente del filtro di dispositivo non è più valido. Per usare il dispositivo, l'applicazione deve ricompilare il grafo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Notifica di rimozione del dispositivo](device-removal-notification.md)
</dt> <dt>

[Codici di notifica degli eventi](event-notification-codes.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 





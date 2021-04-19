---
description: Una richiesta di sospensione è stata completata.
ms.assetid: 32acad47-65bd-42f0-987e-3690bb824b05
title: EC_PAUSED (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fa25a2f32f191519e55e286dac52542bcef949a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324165"
---
# <a name="ec_paused"></a>EC \_ sospeso

Una richiesta di sospensione è stata completata.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Stato del operazione di sospensione.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

No.

## <a name="remarks"></a>Osservazioni

Il gestore del grafico dei filtri Invia questo evento quando completa un comando di sospensione asincrona.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di notifica degli eventi](event-notification-codes.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 





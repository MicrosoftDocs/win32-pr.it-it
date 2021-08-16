---
description: Una richiesta di sospensione è stata completata.
ms.assetid: 32acad47-65bd-42f0-987e-3690bb824b05
title: EC_PAUSED (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebc16eefcf88402ccf0a6173bcfa22e3100c33985469b7372ad6bb2ea97c572d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820052"
---
# <a name="ec_paused"></a>EC \_ PAUSED

Una richiesta di sospensione è stata completata.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Stato dell'operazione di sospensione.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

No.

## <a name="remarks"></a>Osservazioni

Il gestore del grafico dei filtri invia questo evento quando completa un comando di sospensione asincrono.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di notifica degli eventi](event-notification-codes.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 





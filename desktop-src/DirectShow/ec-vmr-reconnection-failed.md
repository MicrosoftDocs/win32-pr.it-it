---
description: Inviato da VMR-7 e VMR-9 quando non è stato in grado di accettare una richiesta di modifica del formato dinamico dal decodificatore upstream.
ms.assetid: 0c865853-2484-4833-9c92-3d6452b655f1
title: EC_VMR_RECONNECTION_FAILED (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4dae6b2735d1ae21576591055aff9dc007f447660f5c96cf13239e5f420f81f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819961"
---
# <a name="ec_vmr_reconnection_failed"></a>\_RICONNESSIONE EC VMR \_ NON \_ RIUSCITA

Inviato da VMR-7 e VMR-9 quando non è stato in grado di accettare una richiesta di modifica del formato dinamico dal decodificatore upstream.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Codice di stato restituito [**da IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) sul pin di input della macchina virtuale che non ha superato la riconnessione.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Non usato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo evento viene inoltrato alle applicazioni.

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

 

 





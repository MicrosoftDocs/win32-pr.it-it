---
description: Si è verificato un errore in un flusso, ma il flusso è ancora in riproduzione.
ms.assetid: ff155c01-22ba-46dd-85b8-05eabf956908
title: EC_STREAM_ERROR_STILLPLAYING (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf78f1fba25316155e36eef1ed469a32bba1ce7c194a6dffb200f1fce5ede3ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819998"
---
# <a name="ec_stream_error_stillplaying"></a>ERRORE \_ EC STREAM \_ \_ STILLPLAYING

Si è verificato un errore in un flusso, ma il flusso è ancora in riproduzione.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Codice di errore dell'operazione non riuscita.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**DWORD**) Codice di errore secondario. Questo valore è in genere zero.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

Nessuno. L'applicazione deve decidere se arrestare il grafo.

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

 

 





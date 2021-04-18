---
description: Si è verificato un errore in un flusso, ma il flusso è ancora in riproduzione.
ms.assetid: ff155c01-22ba-46dd-85b8-05eabf956908
title: EC_STREAM_ERROR_STILLPLAYING (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db74a9f16a0ca01ce74e6d94df50cc402221aaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327114"
---
# <a name="ec_stream_error_stillplaying"></a>\_errore di flusso EC \_ \_ STILLPLAYING

Si è verificato un errore in un flusso, ma il flusso è ancora in riproduzione.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Codice di errore dell'operazione non riuscita.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**DWORD**) Codice di errore secondario. Questo valore è in genere pari a zero.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

Nessuna. L'applicazione deve decidere se arrestare il grafo.

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

 

 





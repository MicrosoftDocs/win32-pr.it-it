---
description: Invia una notifica a un filtro della finestra del renderer video.
ms.assetid: 65d2f40e-c42c-4d71-b9b3-7662a8be0953
title: EC_NOTIFY_WINDOW (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3165247f05e2fb945f02fee43149b84480bd4b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332195"
---
# <a name="ec_notify_window"></a>\_finestra notifica \_ EC

Invia una notifica a un filtro della finestra del renderer video.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HWND**) Handle per la finestra.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

Questo evento viene utilizzato internamente da DirectShow. Il gestore del grafico del filtro non passa questo evento all'applicazione. Le applicazioni non possono eseguire l'override dell'azione predefinita per questo evento.

## <a name="remarks"></a>Commenti

Quando un renderer video è connesso, verifica se il pin di output upstream supporta l'interfaccia [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) . In tal caso, il renderer Invia questo evento al filtro upstream.

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

 

 





---
description: Notifica un filtro della finestra del renderer video.
ms.assetid: 65d2f40e-c42c-4d71-b9b3-7662a8be0953
title: EC_NOTIFY_WINDOW (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 355d4ec8b5b6bea55a2f32f01cc2f83aabeab84443b28e431e5b0d6155acc6d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820113"
---
# <a name="ec_notify_window"></a>FINESTRA \_ DI NOTIFICA \_ EC

Notifica un filtro della finestra del renderer video.

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

Questo evento viene usato internamente da DirectShow. Il gestore del grafico del filtro non passa questo evento all'applicazione. Le applicazioni non possono eseguire l'override dell'azione predefinita per questo evento.

## <a name="remarks"></a>Commenti

Quando un renderer video è connesso, controlla se il pin di output upstream supporta [**l'interfaccia IMediaEventSink.**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) In tal caso, il renderer invia questo evento al filtro upstream.

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

 

 





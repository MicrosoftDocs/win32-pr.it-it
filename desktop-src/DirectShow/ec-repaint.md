---
description: Un renderer video richiede un oggetto Repaint.
ms.assetid: 2e756dea-366c-4024-8fc8-6feabaef1954
title: EC_REPAINT (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba86b54d6d465330ec1635ed7301ce774ef7cb27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324157"
---
# <a name="ec_repaint"></a>ridisegno EC \_

Un renderer video richiede un oggetto Repaint.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**IUnknown** \* ) Puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN di input del renderer video o **null**.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

Il parametro *lParam1* potrebbe specificare il pin di input del renderer video. In tal caso, il gestore del grafico del filtro trova il pin di output connesso al pin e lo interroga per l'interfaccia [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) . Se il pin di output supporta **IMediaEventSink**, il gestore del grafo dei filtri chiama [**IMediaEventSink:: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) con il \_ codice dell'evento EC Repaint. Ciò consente al filtro upstream di inviare nuovamente l'ultimo esempio.

Se *lParam1* è **null** o se il PIN non supporta [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)o se il metodo [**Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) ha esito negativo, il gestore del grafico del filtro gestisce l' \_ evento di ridisegno EC da solo. Il relativo comportamento dipende dallo stato del grafo:

-   Running: ignora l'evento. Il renderer riceverà l'esempio successivo nel flusso.
-   Paused: Cerca il grafico nella posizione corrente, scaricando quindi il filtro e riaccodando i dati.
-   Arrestato: sospende e arresta il grafico, riaccodando quindi i dati.

Per impostazione predefinita, il gestore del grafico del filtro non passa questo evento all'applicazione.

## <a name="remarks"></a>Commenti

I renderer video inviano questo messaggio quando ricevono un messaggio di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) e non contengono dati da visualizzare.

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

 


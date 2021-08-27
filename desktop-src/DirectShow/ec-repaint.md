---
description: Un renderer video richiede un ridisegno.
ms.assetid: 2e756dea-366c-4024-8fc8-6feabaef1954
title: EC_REPAINT (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7edd498d84aaace460a10c88d5579c2f5a87bba42e1a5f393786134bbe727af3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102791"
---
# <a name="ec_repaint"></a>EC \_ REPAINT

Un renderer video richiede un ridisegno.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**IUnknown** \* ) Puntatore [**all'interfaccia IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin di input del renderer video o **NULL.**

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

Il *parametro lParam1* può specificare il pin di input del renderer video. In tal caso, il gestore del grafico dei filtri trova il pin di output connesso a tale pin ed esegue una query per [**l'interfaccia IMediaEventSink.**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) Se il pin di output supporta **IMediaEventSink,** il gestore del grafico dei filtri chiama [**IMediaEventSink::Notify con**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) il codice evento EC \_ REPAINT. In questo modo il filtro upstream ha la possibilità di inviare nuovamente l'ultimo campione.

Se *lParam1* è **NULL** o se il pin non supporta [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)o se il [**metodo Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) ha esito negativo, il gestore del grafico del filtro gestisce l'evento EC \_ REPAINT da solo. Il comportamento dipende dallo stato del grafo:

-   In esecuzione: ignora l'evento. Il renderer riceverà l'esempio successivo nel flusso.
-   In pausa: cerca il grafico nella posizione corrente, scaricando il filtro e riaspendendo i dati.
-   Arrestato: sospende e arresta il grafo, rieliguendo così l'accodamento dei dati.

Per impostazione predefinita, il gestore del grafico del filtro non passa questo evento all'applicazione.

## <a name="remarks"></a>Commenti

I renderer video inviano questo messaggio quando ricevono un [**messaggio WM \_ PAINT**](/windows/desktop/gdi/wm-paint) e non hanno dati da visualizzare.

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

 


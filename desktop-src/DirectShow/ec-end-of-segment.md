---
description: È stata raggiunta la fine di un segmento.
ms.assetid: 07f141b1-2e96-49e2-9cf7-581690e245b5
title: EC_END_OF_SEGMENT (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a779b0f46a031ad694bd3fed3fe29536424a3a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327830"
---
# <a name="ec_end_of_segment"></a>\_fine \_ del \_ segmento EC

È stata raggiunta la fine di un segmento.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**const** **Reference \_ Time** \* ) puntatore a un valore di **\_ ora di riferimento** che specifica il tempo di flusso accumulato dopo l'avvio del segmento, in unità 100-nanosecondi.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**DWORD**) Numero di segmento (in base zero).

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

Il gestore del grafico del filtro controlla il numero di eventi **\_ \_ della fine del \_ segmento EC** rispetto al numero di eventi [**\_ \_ avviati del segmento EC**](ec-segment-started.md) . Se corrispondono, l'evento della **\_ fine \_ del \_ segmento EC** viene inviato all'applicazione. Le applicazioni non possono eseguire l'override dell'azione predefinita per questo evento.

## <a name="remarks"></a>Commenti

Questo codice di evento supporta il loop senza problemi. Quando una chiamata al metodo [**IMediaSeeking:: Sepositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) include il flag del \_ \_ segmento di ricerca am, il filtro di origine invia questo codice evento anziché [**chiamare Ipin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream).

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

 

 





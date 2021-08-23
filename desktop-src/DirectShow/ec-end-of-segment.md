---
description: È stata raggiunta la fine di un segmento.
ms.assetid: 07f141b1-2e96-49e2-9cf7-581690e245b5
title: EC_END_OF_SEGMENT (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13bbc55ab316a56264c9c0b66196a53181d0abd72bfdddf3315523b8c387a1d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639751"
---
# <a name="ec_end_of_segment"></a>FINE \_ \_ DEL SEGMENTO \_ EC

È stata raggiunta la fine di un segmento.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**const** **REFERENCE \_ TIME**) Puntatore a un valore REFERENCE TIME che specifica il tempo del flusso accumulato dall'inizio del \* segmento, in unità da 100 nanosecondi. **\_**

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**DWORD**) Numero di segmento (in base zero).

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

Il gestore del grafico filtri controlla il numero di **eventi EC END OF \_ \_ \_ SEGMENT** rispetto al numero di [**eventi EC SEGMENT \_ \_ STARTED.**](ec-segment-started.md) Se corrispondono, inoltra l'evento **\_ EC END OF \_ \_ SEGMENT** all'applicazione. Le applicazioni non possono eseguire l'override dell'azione predefinita per questo evento.

## <a name="remarks"></a>Commenti

Questo codice evento supporta il ciclo continuo. Quando una chiamata al metodo [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) include il flag AM SEEKING Segment, il filtro di origine invia questo codice evento anziché chiamare \_ \_ [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream).

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

 

 





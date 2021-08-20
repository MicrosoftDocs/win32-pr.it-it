---
description: È stato avviato un nuovo segmento.
ms.assetid: 9742436a-e233-4641-a0d5-aa240cde5f28
title: EC_SEGMENT_STARTED (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b33d9f75dc4fa8e86b13e61c78b98a19248c16f2f627e1c1b09e536b31a73f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015919"
---
# <a name="ec_segment_started"></a>EC \_ SEGMENT \_ STARTED

È stato avviato un nuovo segmento.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**const** **REFERENCE \_ TIME**) Puntatore a un valore REFERENCE TIME che specifica il tempo di flusso accumulato dall'inizio del segmento, in unità di \* 100 nanosecondi. **\_**

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**DWORD**) Numero di segmento (in base zero).

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

Questo evento non viene inviato all'applicazione. Le applicazioni non possono eseguire l'override dell'azione predefinita per questo evento.

## <a name="remarks"></a>Commenti

Se un filtro invierà [**\_ un'end \_ OF \_ SEGMENT EC**](ec-end-of-segment.md) alla fine di un segmento, invia questo evento all'inizio del segmento. Il gestore del grafico dei filtri usa questa notifica degli eventi per calcolare il numero di notifiche EC END OF SEGMENT previste \_ \_ alla fine del \_ segmento.

Per impostazione predefinita, i filtri non inviano eventi [**\_ EC END OF \_ \_ SEGMENT**](ec-end-of-segment.md) alla fine dei segmenti e pertanto non devono inviare questo evento. Per altre informazioni, vedere [**IMediaSeeking::SetPositions.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions)

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

 

 





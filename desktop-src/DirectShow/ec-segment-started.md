---
description: Un nuovo segmento è stato avviato.
ms.assetid: 9742436a-e233-4641-a0d5-aa240cde5f28
title: EC_SEGMENT_STARTED (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7e7df85bddb78fe2687a017b481e6db62ba37c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325042"
---
# <a name="ec_segment_started"></a>\_segmento EC \_ avviato

Un nuovo segmento è stato avviato.

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

Questo evento non viene inviato all'applicazione. Le applicazioni non possono eseguire l'override dell'azione predefinita per questo evento.

## <a name="remarks"></a>Commenti

Se un filtro invierà una [**\_ fine \_ del \_ segmento EC**](ec-end-of-segment.md) alla fine di un segmento, invierà questo evento all'inizio del segmento. Filter Graph Manager usa questa notifica degli eventi per calcolare \_ \_ il numero di notifiche della fine del \_ segmento EC che dovrebbe aspettarsi alla fine del segmento.

Per impostazione predefinita, i filtri non inviano eventi [**\_ \_ di fine \_ segmento EC**](ec-end-of-segment.md) alla fine dei segmenti e pertanto non devono inviare questo evento. Per altre informazioni, vedere [**IMediaSeeking:: Sepositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions).

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

 

 





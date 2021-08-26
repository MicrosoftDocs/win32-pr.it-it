---
description: È stato eseguito il rendering di tutti i dati di un determinato flusso.
ms.assetid: 46037d53-085d-4fd0-91a0-408702cbfce5
title: EC_COMPLETE (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a3bb02275862e2cfaea88de5bad0ae545a257efc4d352506d284b83150032f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998201"
---
# <a name="ec_complete"></a>EC \_ COMPLETE

È stato eseguito il rendering di tutti i dati di un determinato flusso.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Stato del flusso al completamento. Se non si sono verificati errori durante la riproduzione, il valore è S \_ OK.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**IUnknown** \* ) Zero o un puntatore all'interfaccia [**IBaseFilter del**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) renderer.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

Per impostazione predefinita, il gestore del grafo del filtro non inoltra questo evento all'applicazione. Tuttavia, dopo che tutti i flussi nel report del grafo **EC \_ COMPLETE,** il gestore del grafo dei filtri pubblica un evento **EC \_ COMPLETE** separato per l'applicazione.

Se l'azione predefinita è disabilitata per questo evento, l'applicazione riceve tutti gli eventi **EC \_ COMPLETE** dai renderer.

## <a name="remarks"></a>Commenti

Un filtro renderer invia questo evento quando riceve un avviso di fine flusso. La fine del flusso viene segnalata tramite il [**metodo IPin::EndOfStream.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) Il filtro invia esattamente un **evento EC \_ COMPLETE** per ogni flusso. Il filtro deve elaborare eventuali campioni in sospeso prima di inviare l'evento. L'arresto di un renderer reimposta qualsiasi stato di fine flusso memorizzato nella cache.

Se il renderer viene sospeso, non invia **EC \_ COMPLETE** fino a quando non viene chiamato il metodo [**IMediaFilter::Run.**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) Continua inoltre a inviare eventi **EC \_ COMPLETE** per ogni transizione dalla sospensione all'esecuzione, fino a quando il filtro non viene arrestato o scaricato.

I filtri impostano *il parametro lParam2* su un [**puntatore IBaseFilter.**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) Se l'azione predefinita è abilitata, il gestore del grafico del filtro imposta questo parametro su zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di notifica degli eventi](event-notification-codes.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[Renderer video alternativi](alternative-video-renderers.md)
</dt> </dl>

 

 





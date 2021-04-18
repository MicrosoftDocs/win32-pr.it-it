---
description: È stato eseguito il rendering di tutti i dati di un flusso specifico.
ms.assetid: 46037d53-085d-4fd0-91a0-408702cbfce5
title: EC_COMPLETE (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cd6d548a56173b9c6ea83426ddab3fa8556e312
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328459"
---
# <a name="ec_complete"></a>EC \_ completato

È stato eseguito il rendering di tutti i dati di un flusso specifico.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**HRESULT**) Stato del flusso al termine dell'esecuzione. Se non si sono verificati errori durante la riproduzione, il valore è \_ OK.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**IUnknown** \* ) Zero o un puntatore all'interfaccia [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del renderer.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

Per impostazione predefinita, il gestore del grafico del filtro non trasmette questo evento all'applicazione. Tuttavia, dopo il **\_ completamento** di tutti i flussi nel report grafico EC, il gestore del grafico del filtro pubblica un evento di **\_ completamento EC** separato nell'applicazione.

Se l'azione predefinita è disabilitata per questo evento, l'applicazione riceve tutti gli **eventi \_ completi EC** dai renderer.

## <a name="remarks"></a>Commenti

Un filtro renderer Invia questo evento quando riceve una notifica di fine flusso. (La fine del flusso viene segnalata tramite il metodo [**Ipin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) ). Il filtro Invia esattamente un evento **EC \_ complete** per ogni flusso. Il filtro deve elaborare tutti gli esempi in sospeso prima di inviare l'evento. L'arresto di un renderer Reimposta lo stato della fine del flusso memorizzato nella cache.

Se il renderer è sospeso, non invia la funzione **EC \_ completa** fino a quando non viene chiamato il metodo [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) . Continua inoltre a inviare eventi **EC \_ completi** per ogni transizione dalla pausa per l'esecuzione, fino a quando il filtro non viene interrotto o scaricato.

I filtri impostano il parametro *lParam2* su un puntatore [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) . Se l'azione predefinita è abilitata, il gestore del grafico del filtro imposta questo parametro su zero.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Dshow. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di notifica degli eventi](event-notification-codes.md)
</dt> <dt>

[Notifica degli eventi in DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[Renderer video alternativi](alternative-video-renderers.md)
</dt> </dl>

 

 





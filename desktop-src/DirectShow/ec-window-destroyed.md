---
description: Il renderer video è stato eliminato definitivamente o rimosso dal grafo.
ms.assetid: facf35c2-d6a2-4373-bce5-171fd9325116
title: EC_WINDOW_DESTROYED (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d7b26224fee4e18d92d16d8f3bfe277c70cf2b260a19c9c7d6438477266c3e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686031"
---
# <a name="ec_window_destroyed"></a>EC \_ WINDOW \_ DESTROYED

Il renderer video è stato eliminato definitivamente o rimosso dal grafo.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**IUnknown** \* ) Puntatore all'interfaccia [**IBaseFilter del**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) renderer video.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

Il gestore del grafico del filtro rilascia questa finestra come stato attivo, tramite [**l'interfaccia IResourceManager.**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) Non invia la notifica degli eventi all'applicazione.

## <a name="remarks"></a>Commenti

Il renderer video invia questo evento quando esce dal grafico del filtro, nel relativo [**metodo IBaseFilter::JoinFilterGraph.**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) L'invio dell'evento quando il filtro viene eliminato potrebbe essere troppo tardi, perché a quel punto anche il gestore del grafo del filtro potrebbe essere eliminato.

Questo evento consente ad altri filtri di acquisire risorse che dipendono dalla finestra attiva, ad esempio i dispositivi audio.

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

 

 





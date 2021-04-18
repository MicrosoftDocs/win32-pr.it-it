---
description: Il renderer video è stato eliminato o rimosso dal grafico.
ms.assetid: facf35c2-d6a2-4373-bce5-171fd9325116
title: EC_WINDOW_DESTROYED (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdd3e641c7fb911a8da10a4c89682fa266e862de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325496"
---
# <a name="ec_window_destroyed"></a>\_finestra EC \_ distrutta

Il renderer video è stato eliminato o rimosso dal grafico.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**IUnknown** \* ) Puntatore all'interfaccia [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del renderer video.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

Il gestore del grafico del filtro rilascia questa finestra come stato attivo, tramite l'interfaccia [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) . Non invia la notifica degli eventi all'applicazione.

## <a name="remarks"></a>Commenti

Il renderer video Invia questo evento quando lascia il grafico del filtro, nel metodo [**IBaseFilter:: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) . Inviando l'evento quando il filtro viene eliminato definitivamente potrebbe essere troppo tardi, perché a questo punto è possibile che anche il gestore del grafo del filtro venga eliminato.

Questo evento consente ad altri filtri di acquisire risorse che dipendono dallo stato attivo della finestra, ad esempio i dispositivi audio.

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

 

 





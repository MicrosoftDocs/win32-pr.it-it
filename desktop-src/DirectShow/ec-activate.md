---
description: È in corso l'attivazione o la disattivazione di una finestra video.
ms.assetid: 2e004899-bb2b-4127-b606-e2a979275836
title: EC_ACTIVATE (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b14d9b0ad192045f179d9f0f366eed6a32efb0e6cc6f61b47255f118b7f55258
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966061"
---
# <a name="ec_activate"></a>EC \_ ACTIVATE

È in corso l'attivazione o la disattivazione di una finestra video.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**BOOL**) **TRUE** se la finestra è attivata oppure **FALSE** se la finestra è disattivata.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**IUnknown** \* ) Puntatore all'interfaccia [**IBaseFilter del**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) renderer.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

Il gestore del grafico dei filtri imposta lo stato attivo tramite [**l'interfaccia IResourceManager.**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) Non invia la notifica degli eventi all'applicazione.

## <a name="remarks"></a>Commenti

Un renderer video invia questo evento ogni volta che la finestra viene attivata o disattivata, ovvero quando riceve un messaggio WM \_ ACTIVATEAPP. L'attivazione o la disattivazione della finestra può verificarsi perché la finestra ha acquisito o perso lo stato attivo o perché il renderer è passata dalla modalità schermo intero alla modalità finestra.

Questo evento consente al gestore del grafo del filtro di allocare risorse che dipendono dalla finestra attiva, ad esempio i dispositivi audio.

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

 

 





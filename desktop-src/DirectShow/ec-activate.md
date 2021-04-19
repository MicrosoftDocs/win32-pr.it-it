---
description: È in corso l'attivazione o la disattivazione di una finestra video.
ms.assetid: 2e004899-bb2b-4127-b606-e2a979275836
title: EC_ACTIVATE (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81e48adb3ae98af172664b807386c615d34b6b22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328474"
---
# <a name="ec_activate"></a>\_attivazione EC

È in corso l'attivazione o la disattivazione di una finestra video.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**Bool**) **True** se la finestra è attivata oppure **false** se la finestra è disattivata.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**IUnknown** \* ) Puntatore all'interfaccia [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del renderer.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

Il gestore del grafico del filtro imposta lo stato attivo tramite l'interfaccia [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) . Non invia la notifica degli eventi all'applicazione.

## <a name="remarks"></a>Commenti

Un renderer video Invia questo evento ogni volta che la finestra viene attivata o disattivata, ovvero quando riceve un \_ messaggio ACTIVATEAPP WM. L'attivazione o la disattivazione della finestra può verificarsi perché la finestra ha acquisito o perso lo stato attivo oppure perché il renderer è stato spostato tra la modalità a schermo intero e la modalità finestra.

Questo evento consente a Filter Graph Manager di allocare risorse che dipendono dallo stato attivo della finestra, ad esempio i dispositivi audio.

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

 

 





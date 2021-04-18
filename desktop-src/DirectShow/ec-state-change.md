---
description: Lo stato del grafico filtro è stato modificato.
ms.assetid: f77b4c06-46a5-4912-adb0-0fa8cb7769aa
title: EC_STATE_CHANGE (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf64cc62ba15f77370e52821c3335f9a22f573d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327429"
---
# <a name="ec_state_change"></a>\_modifica dello stato EC \_

Lo stato del grafico filtro è stato modificato.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**DWORD**) Membro del tipo enumerato [**\_ dello stato del filtro**](/windows/win32/api/strmif/ne-strmif-filter_state) , che indica il nuovo stato del grafico.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

Nessuna azione predefinita. L'evento non viene inviato all'applicazione.

> [!Note]  
> Questo evento può verificarsi quando il grafico si arresta. Se si sostituisce l'azione predefinita e si è in ascolto di questo evento, è necessario prestare particolare attenzione a non elaborare gli eventi dopo aver rilasciato il gestore del grafico dei filtri. In caso contrario, l'applicazione potrebbe fare riferimento a un puntatore [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) non valido e un arresto anomalo. Per altre informazioni, vedere [rispondere agli eventi](responding-to-events.md).

 

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

 

 





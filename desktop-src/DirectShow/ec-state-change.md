---
description: Lo stato del grafico del filtro è cambiato.
ms.assetid: f77b4c06-46a5-4912-adb0-0fa8cb7769aa
title: EC_STATE_CHANGE (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2b476c923f0b812196a5697444433ea0be65b8d3f46bd0388261b2a67a66881
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905731"
---
# <a name="ec_state_change"></a>EC \_ STATE \_ CHANGE

Lo stato del grafico del filtro è cambiato.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**DWORD**) Membro del tipo [**enumerato FILTER \_ STATE,**](/windows/win32/api/strmif/ne-strmif-filter_state) che indica il nuovo stato del grafico.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zero.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

Nessuna azione predefinita. L'evento non viene inviato all'applicazione.

> [!Note]  
> Questo evento può verificarsi all'arresto del grafico. Se si esegue l'override dell'azione predefinita e si è in ascolto di questo evento, è necessario prestare particolare attenzione a non elaborare gli eventi dopo il rilascio di Filter Graph Manager. In caso contrario, l'applicazione potrebbe fare riferimento a un puntatore [**IMediaEvent non**](/windows/desktop/api/Control/nn-control-imediaevent) valido e arrestarsi in modo anomalo. Per altre informazioni, vedere [Risposta agli eventi.](responding-to-events.md)

 

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

 

 





---
description: La modalità di visualizzazione è stata modificata.
ms.assetid: 1f5b066b-6d5d-44bb-851a-424b2bd389c0
title: EC_DISPLAY_CHANGED (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee75517c1927d7f819565d796d9f15fb21050ef7b4ead86d98f582018cc66b7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965921"
---
# <a name="ec_display_changed"></a>EC \_ DISPLAY \_ CHANGED

La modalità di visualizzazione è stata modificata.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**IUnknown** \* ) Puntatore a una matrice [**di interfacce IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) per i pin di input del renderer video. Se *lParam2* è zero, questo parametro può essere **NULL.**

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Se *lParam2 è* zero, *lParam1 contiene* un singolo puntatore **IPin** o è uguale a **NULL.** Se *lParam2* è maggiore di zero, *lParam1* contiene una matrice di puntatori **IPin** e il numero di elementi nella matrice viene fornito da *lParam2*.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

Il gestore del grafico del filtro arresta temporaneamente il grafico e quindi disconnette e riconnette il renderer video. Non passa l'evento all'applicazione.

## <a name="remarks"></a>Commenti

I renderer video possono inviare questo evento in risposta a un [**messaggio \_ DISPLAYCHANGE WM.**](/windows/desktop/gdi/wm-displaychange) Il **messaggio WM \_ DISPLAYCHANGE** indica che l'utente ha modificato la risoluzione dello schermo.

Durante la connessione pin, la maggior parte dei renderer video seleziona un formato in base alla modalità di visualizzazione corrente. Se la modalità di visualizzazione cambia, il renderer video potrebbe dover scegliere un altro formato. Inviando questo messaggio, il renderer segnala al gestore del grafico del filtro che deve essere riconnesso. Durante la riconnessione, il renderer può selezionare un nuovo formato. Se la riconnessione non riesce, il gestore del grafico dei filtri invia un evento [**\_ EC ERRORABORT**](ec-errorabort.md) all'applicazione.

### <a name="enhanced-video-renderer"></a>Renderer video avanzato

Un presentatore personalizzato per [**il renderer**](enhanced-video-renderer-filter.md) video avanzato (EVR) deve inviare questo evento all'EVR se il dispositivo Direct3D del presentatore cambia. Impostare *lParam1* e *lParam2* su zero; EVR ignora i parametri dell'evento.

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

 


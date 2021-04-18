---
description: La modalità di visualizzazione è cambiata.
ms.assetid: 1f5b066b-6d5d-44bb-851a-424b2bd389c0
title: EC_DISPLAY_CHANGED (dshow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 549a4c5201906b692a1bd726e65269679705e9a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331114"
---
# <a name="ec_display_changed"></a>visualizzazione di EC \_ \_ modificata

La modalità di visualizzazione è cambiata.

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**IUnknown** \* ) Puntatore a una matrice di interfacce [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) per i pin di input del renderer video. Se *lParam2* è zero, questo parametro può essere **null**.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Se *lParam2* è zero, *lParam1* contiene un solo puntatore **Ipin** o è uguale a **null**. Se *lParam2* è maggiore di zero, *lParam1* contiene una matrice di puntatori **Ipin** e il numero di elementi nella matrice viene fornito da *lParam2*.

</dd> </dl>

## <a name="default-action"></a>Azione predefinita

Filter Graph Manager Arresta temporaneamente il grafo, quindi disconnette e riconnette il renderer video. L'evento non viene passato all'applicazione.

## <a name="remarks"></a>Commenti

I renderer video possono inviare questo evento in risposta a un messaggio [**WM \_ DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) . Il messaggio **WM \_ DISPLAYCHANGE** indica che l'utente ha modificato la risoluzione dello schermo.

Durante la connessione pin, la maggior parte dei renderer video sceglie un formato basato sulla modalità di visualizzazione corrente. Se la modalità di visualizzazione cambia, il renderer video potrebbe dover scegliere un altro formato. Inviando questo messaggio, il renderer segnala al gestore del grafico dei filtri che è necessario riconnetterlo. Durante la riconnessione, il renderer può selezionare un nuovo formato. Se la riconnessione ha esito negativo, il gestore del grafico dei filtri Invia un evento [**\_ ERRORABORT EC**](ec-errorabort.md) all'applicazione.

### <a name="enhanced-video-renderer"></a>Renderer video migliorato

Un presentatore personalizzato per il [**renderer video migliorato**](enhanced-video-renderer-filter.md) (EVR) deve inviare questo evento al EVR se il dispositivo Direct3D del Presenter viene modificato. Impostare *lParam1* e *lParam2* su zero; EVR ignora i parametri dell'evento.

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

 


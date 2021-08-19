---
title: Specifica della proprietà Name
description: Gli sviluppatori di server devono fare attenzione durante la creazione di controlli predefiniti e comuni per garantire Microsoft Active Accessibility possibile esporre la proprietà Name per il controllo.
ms.assetid: 2b4ec5ae-bda1-41e6-9387-6ee3cb6c3163
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c93205430f3063b993c49a7145658d7748aac0e697257789c31ac0653d6189
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052549"
---
# <a name="providing-the-name-property"></a>Specifica della proprietà Name

Gli sviluppatori di server devono fare attenzione durante la creazione di controlli predefiniti e comuni per garantire Microsoft Active Accessibility possibile esporre la [proprietà Name](name-property.md) per il controllo. A seconda del tipo di controllo, il testo per la proprietà Name deriva da uno degli elementi seguenti:

-   Testo (o didascalia) della finestra del controllo
-   Testo statico che etichetta il controllo

Per trovare il testo della finestra del controllo, Microsoft Active Accessibility invia il [**messaggio WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext) al controllo. Questo testo corrisponde al parametro di testo nell'istruzione di definizione della risorsa del controllo. Per alcuni controlli, ad esempio i pulsanti, si tratta dello stesso testo visualizzato con il controllo . Per altri controlli, ad esempio le barre degli strumenti, questo testo non viene visualizzato. Pertanto, gli sviluppatori di server devono fornire testo significativo nell'istruzione di definizione delle risorse del controllo per consentire agli utenti delle utilità client di identificare il controllo.

Per trovare l'etichetta del controllo, Microsoft Active Accessibility cerca un controllo di testo statico chiamando [**GetWindow**](/windows/desktop/api/winuser/nf-winuser-getwindow) con il \_ flag HWNDPREV GW. La ricerca viene interrotta se viene trovato un controllo di testo statico o se viene rilevato un controllo con gli stili della finestra WS \_ GROUP \| WS \_ TABSTOP. Questo ordine di ricerca corrisponde all'ordine di tabulazione inverso in una finestra di dialogo. Gli sviluppatori di server devono osservare l'ordine di tabulazione durante la creazione di controlli in modo che un controllo di testo statico preceda immediatamente il controllo etichettato.

Per altre informazioni sulle tecniche che Microsoft Active Accessibility per esporre la proprietà [Name](name-property.md), vedere riferimento [Interfaccia utente'elemento](user-interface-element-reference.md).

 

 
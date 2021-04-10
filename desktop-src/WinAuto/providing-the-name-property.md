---
title: Specifica della proprietà Name
description: Gli sviluppatori di server devono prestare attenzione durante la creazione di controlli predefiniti e comuni per garantire che Microsoft Active Accessibility possa esporre la proprietà Name per il controllo.
ms.assetid: 2b4ec5ae-bda1-41e6-9387-6ee3cb6c3163
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d7a4c30c6bc228785a886d9a41717f8cdb8dda
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963179"
---
# <a name="providing-the-name-property"></a>Specifica della proprietà Name

Gli sviluppatori di server devono prestare attenzione durante la creazione di controlli predefiniti e comuni per garantire che Microsoft Active Accessibility possa esporre la [proprietà Name](name-property.md) per il controllo. A seconda del tipo di controllo, il testo per la proprietà Name deriva da uno dei seguenti elementi:

-   Testo della finestra del controllo (o didascalia)
-   Testo statico che etichetta il controllo

Per trovare il testo della finestra del controllo, Microsoft Active Accessibility invia il messaggio [**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext) al controllo. Questo testo corrisponde al parametro di testo nell'istruzione di definizione di risorsa del controllo. Per alcuni controlli, ad esempio pulsanti, si tratta dello stesso testo visualizzato con il controllo. Per gli altri controlli, ad esempio le barre degli strumenti, questo testo non viene visualizzato. Pertanto, gli sviluppatori di server devono fornire testo significativo nell'istruzione di definizione della risorsa del controllo per consentire agli utenti delle utilità client di identificare il controllo.

Per trovare l'etichetta del controllo, Microsoft Active Accessibility Cerca un controllo testo statico chiamando [**GetWindow**](/windows/desktop/api/winuser/nf-winuser-getwindow) con il \_ flag GW HWNDPREV. La ricerca viene interrotta se viene trovato un controllo di testo statico o se viene rilevato un controllo con gli stili della finestra WS del \_ gruppo \| WS \_ TABSTOP. Questo ordine di ricerca corrisponde all'ordine di tabulazione inverso in una finestra di dialogo. Gli sviluppatori di server devono osservare l'ordine di tabulazione durante la creazione di controlli in modo che un controllo testo statico preceda immediatamente il controllo che etichetta.

Per ulteriori informazioni sulle tecniche utilizzate da Microsoft Active Accessibility per esporre la [proprietà Name](name-property.md), vedere informazioni di [riferimento sugli elementi dell'interfaccia utente](user-interface-element-reference.md).

 

 
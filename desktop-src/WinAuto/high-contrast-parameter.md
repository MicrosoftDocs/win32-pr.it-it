---
title: Parametro a contrasto elevato
description: Il parametro High Contrast indica se l'utente desidera un contrasto elevato tra i colori utilizzati per gli oggetti visivi in primo piano e in background.
ms.assetid: ec89c4ce-4e8b-4e1f-a349-fbd47431d675
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f1255e8a99b3cb253146e2fa2c019a879c4a1b6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963216"
---
# <a name="high-contrast-parameter"></a>Parametro a contrasto elevato

Il parametro High Contrast indica se l'utente desidera un contrasto elevato tra i colori utilizzati per gli oggetti visivi in primo piano e in background.

L'utente controlla l'impostazione del parametro a contrasto elevato usando il centro di accesso facilitato nel pannello di controllo o un'altra applicazione per la personalizzazione dell'ambiente. Le applicazioni usano i flag **SPI \_ GETHIGHCONTRAST** e **SPI \_ SETHIGHCONTRAST** con la funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) per ottenere e impostare il parametro a contrasto elevato.

Durante l'inizializzazione e durante l'elaborazione dei messaggi [**WM \_ SYSCOLORCHANGE**](/windows/desktop/gdi/wm-syscolorchange) , le applicazioni devono determinare lo stato del parametro ad alto contrasto. Per eseguire questa determinazione, le applicazioni devono chiamare [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) con il flag **\_ GETHIGHCONTRAST di SPI** per ottenere una struttura [**HIGHCONTRAST**](/windows/win32/api/winuser/ns-winuser-highcontrasta) . Se per il membro **dwFlags** della struttura **HIGHCONTRAST** è impostato il bit **HCF \_ contrasto elevato** , la funzionalità a contrasto elevato è abilitata e le applicazioni devono eseguire le operazioni seguenti:

-   Mappare tutti i colori a una singola coppia di colori di primo piano e di sfondo. Utilizzare la funzione [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) per determinare i colori di primo piano e di sfondo appropriati, utilizzando una combinazione di **\_ WINDOWTEXT colore** e **\_ finestra colori** o una combinazione di colore **\_ BTNTEXT** e **colore \_ BTNFACE**. La funzione **GetSysColor** restituisce i colori selezionati dall'utente tramite il pannello di controllo.
-   Omettere tutte le immagini bitmap che in genere vengono visualizzate dietro il testo. Queste immagini sono distracting visivamente a un utente che necessita di un contrasto elevato.
-   Le immagini che vengono in genere disegnate in più colori devono essere disegnate usando i colori di primo piano e di sfondo selezionati per il testo.

Inoltre, le applicazioni usano i flag **SPI \_ GETDISABLEOVERLAPPEDCONTENT** e **SPI \_ SETDISABLEOVERLAPPEDCONTENT** con la funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) per ottenere e impostare il parametro di contenuto sovrapposto. Le funzionalità di visualizzazione, quali immagini di sfondo, sfondi con trama, segni d'acqua sui documenti, fusione alfa e trasparenza, possono ridurre il contrasto tra il primo piano e lo sfondo, rendendo più difficile per gli utenti con visione bassa visualizzare gli oggetti sullo schermo. Questo flag consente alle applicazioni di determinare se tale contenuto sovrapposto è stato disabilitato

 

 
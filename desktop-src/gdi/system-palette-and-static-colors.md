---
description: In genere, le voci della tavolozza di sistema riservate dal sistema per i colori statici non possono essere modificate.
ms.assetid: be258151-36cc-42ba-8005-ff9d8e59b894
title: Tavolozza di sistema e colori statici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 537bdc87fecdd055334b83a56b0a53f9999be94c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979423"
---
# <a name="system-palette-and-static-colors"></a>Tavolozza di sistema e colori statici

In genere, le voci della tavolozza di sistema riservate dal sistema per i colori statici non possono essere modificate. Un'applicazione può eseguire l'override di questo comportamento predefinito utilizzando la funzione [**SetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-setsystempaletteuse) per ridurre il numero di voci di colore statiche e, pertanto, aumentare il numero di voci della tavolozza di sistema inutilizzate. Tuttavia, poiché la modifica dei colori statici può avere un effetto immediato e significativo su tutte le finestre sullo schermo, un'applicazione non deve chiamare **SetSystemPaletteUse**, a meno che non disponga di una finestra ingrandita e dello stato attivo per l'input.

Quando un'applicazione chiama [**SetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-setsystempaletteuse) con il \_ valore Nostatic SYSPAL, il sistema libera tutte le voci riservate, consentendo a tali voci di ricevere nuovi valori di colore quando l'applicazione realizza successivamente la relativa tavolozza logica. Le rimanenti due voci di colore statiche rimangono riservate e sono impostate su bianco e nero. Un'applicazione può ripristinare le voci riservate chiamando **SetSystemPaletteUse** con il \_ valore statico SYSPAL. Consente di individuare l'utilizzo corrente della tavolozza di sistema tramite la funzione [**GetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-getsystempaletteuse) .

Inoltre, dopo aver impostato l'utilizzo della tavolozza di sistema su SYSPAL \_ Nostatic, è necessario che l'applicazione realizzi immediatamente la relativa tavolozza logica, chiami la funzione [**GetSysColor**](/windows/win32/api/winuser/nf-winuser-getsyscolor) per salvare le impostazioni correnti relative ai colori del sistema, chiami la funzione [**SetSysColors**](/windows/win32/api/winuser/nf-winuser-setsyscolors) per impostare i colori di sistema su valori ragionevoli usando il nero e il bianco e infine invia il messaggio [**WM \_ SYSCOLORCHANGE**](wm-syscolorchange.md) ad altre finestre di primo livello per Quando si impostano i colori di sistema utilizzando il nero e il bianco, l'applicazione deve verificare che gli elementi adiacenti o sovrapposti, ad esempio i bordi e i frame della finestra, siano impostati rispettivamente su nero e bianco.

Prima che l'applicazione perda lo stato attivo per l'input, chiude la finestra o termina, deve chiamare immediatamente [**SetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-setsystempaletteuse) con il \_ valore statico SYSPAL, realizzare la relativa tavolozza logica, ripristinare i colori di sistema nei valori precedenti e inviare il messaggio [**WM \_ SYSCOLORCHANGE**](wm-syscolorchange.md) . Il sistema invia un messaggio di [**\_ disegno WM**](wm-paint.md) a qualsiasi finestra interessata da una modifica del colore di sistema. Le applicazioni che hanno pennelli che usano i colori di sistema esistenti devono eliminare tali pennelli e ricrearli usando i nuovi colori di sistema.

 

 

---
description: In genere, le voci della tavolozza di sistema che il sistema riserva per i colori statici non possono essere modificate.
ms.assetid: be258151-36cc-42ba-8005-ff9d8e59b894
title: Tavolozza di sistema e colori statici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ffc555331ea7ad14675b4155a76d14cc61f3bef3fa7e92b331ad89449b97884
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119613381"
---
# <a name="system-palette-and-static-colors"></a>Tavolozza di sistema e colori statici

In genere, le voci della tavolozza di sistema che il sistema riserva per i colori statici non possono essere modificate. Un'applicazione può eseguire l'override di questo comportamento predefinito usando la funzione [**SetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-setsystempaletteuse) per ridurre il numero di voci di colore statico e, di conseguenza, aumentare il numero di voci della tavolozza di sistema inutilizzate. Tuttavia, poiché la modifica dei colori statici può avere un effetto immediato e notevole su tutte le finestre sullo schermo, un'applicazione non deve chiamare **SetSystemPaletteUse,** a meno che non abbia una finestra ingrandita e lo stato attivo per l'input.

Quando un'applicazione chiama [**SetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-setsystempaletteuse) con il valore \_ SYSPAL NOSTATIC, il sistema libera tutte le voci riservate, ad eccezione di due, consentendo a tali voci di ricevere nuovi valori di colore quando l'applicazione si rende conto successivamente della tavolozza logica. Le due voci di colore statiche rimanenti rimangono riservate e sono impostate su bianco e nero. Un'applicazione può ripristinare le voci riservate chiamando **SetSystemPaletteUse** con il valore SYSPAL \_ STATIC. Può individuare l'utilizzo corrente della tavolozza di sistema usando la [**funzione GetSystemPaletteUse.**](/windows/desktop/api/Wingdi/nf-wingdi-getsystempaletteuse)

Inoltre, dopo aver impostato l'utilizzo della tavolozza di sistema su SYSPAL NOSTATIC, l'applicazione deve immediatamente realizzare la tavolozza logica, chiamare la \_ [**funzione GetSysColor**](/windows/win32/api/winuser/nf-winuser-getsyscolor) per salvare le impostazioni correnti del colore di sistema, chiamare la funzione [**SetSysColors**](/windows/win32/api/winuser/nf-winuser-setsyscolors) per impostare i colori di sistema su valori ragionevoli usando il bianco e nero e infine inviare il messaggio [**\_ SYSCOLORCHANGE WM**](wm-syscolorchange.md) ad altre finestre di primo livello per consentirne il ridisegno con i nuovi colori di sistema. Quando si impostano i colori di sistema usando il nero e il bianco, l'applicazione deve assicurarsi che gli elementi adiacenti o sovrapposti, ad esempio i bordi e le cornice della finestra, siano impostati rispettivamente su nero e bianco.

Prima che l'applicazione perda lo stato attivo per l'input, chieda la finestra o termini, deve chiamare immediatamente [**SetSystemPaletteUse**](/windows/desktop/api/Wingdi/nf-wingdi-setsystempaletteuse) con il valore SYSPAL STATIC, realizzare la tavolozza logica, ripristinare i colori di sistema ai valori precedenti e inviare il messaggio \_ [**WM \_ SYSCOLORCHANGE.**](wm-syscolorchange.md) Il sistema invia un [**messaggio WM \_ PAINT**](wm-paint.md) a qualsiasi finestra interessata da una modifica del colore di sistema. Le applicazioni con pennelli che usano i colori di sistema esistenti devono eliminare tali pennelli e crearli di nuovo usando i nuovi colori di sistema.

 

 

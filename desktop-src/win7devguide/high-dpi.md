---
title: Valori DPI alti
description: Valori DPI alti
ms.assetid: 476fe65c-2acd-4a7a-8a76-72d9f010b772
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5006d5bdf1c9e90745ef8e3571e64e729dbf5dff54338280789f39c6d0027e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118203962"
---
# <a name="high-dpi"></a>Valori DPI alti

Con l'avanzare delle tecnologie di visualizzazione, i produttori hanno aumentato il numero di pixel supportati dai relativi schermi. Anche se testo, immagini ed elementi dell'interfaccia utente hanno un aspetto molto più nitido e leggibile su schermi ad alta risoluzione, il sistema operativo deve aumentare le prestazioni per supportare l'esperienza visiva; in caso contrario, tutto sembra più piccolo.

Windows 7 supporta schermi *DPI* elevati. I dati di mercato suggeriscono che le distribuzioni di schermi *DPI* elevati (120-144 punti per pollice (dpi)) aumenteranno nell'intervallo di tempo Windows 7. Quando si eseguono risoluzioni native in queste schermate, molte applicazioni appaiono molto piccole a meno che non *usino valori DPI elevati.* Alcune applicazioni , ad esempio Windows Internet Explorer, dispongono di funzionalità di ridimensionamento dei caratteri che consentono agli utenti di eseguire lo zoom avanti e indietro, ma molte applicazioni no. La *funzionalità DPI* elevata in Windows 7:

-   Garantisce che Windows e le esperienze dell'applicazione siano ottimali nell'hardware standard ( le impostazioni *DPI* sono ottimizzate in modo da corrispondere alle funzionalità dell'hardware).
-   Consente alla Windows Shell e ad altre Windows basate su applicazioni basate su Windows avere un aspetto positivo con impostazioni *DPI* diverse.
-   Rispetta le impostazioni *DPI* predefinite in base alle specifiche e alle funzionalità dell'hardware.
-   Consente agli utenti di personalizzare *le impostazioni DPI* senza riavvio.
-   Garantisce che lo schermo sia sempre impostato sulla risoluzione nativa.

La Windows di ridimensionamento *DPI* ridimensiona i tipi di carattere e gli elementi dell'interfaccia utente (ad esempio pulsanti, icone e campi di input) in base a una percentuale calcolata, come specificato dall'impostazione *DPI.* Questo comportamento è diverso dal ridimensionamento che si verifica quando la risoluzione dello schermo viene abbassata. Nel caso del ridimensionamento *DPI,* Windows fornisce tipi di carattere ed elementi dell'interfaccia utente che vengono disegnati con più pixel, con conseguente maggiore fedeltà e maggiore Windows grafica. Le applicazioni Windows di terze parti possono sfruttare le impostazioni *DPI* elevate e regolare l'interfaccia utente di conseguenza, dichiarandosi in grado di riconoscere *il valore DPI* alto. Gli sviluppatori di applicazioni non devono più presupporre che 96 dpi sia la risoluzione ideale per tutte le applicazioni.

Per altre informazioni su *High DPI* e sulla scrittura di applicazioni che sono in grado di riconoscere *DPI* elevato, vedere [High DPI](../hidpi/high-dpi-desktop-application-development-on-windows.md).

 

 

---
title: Valori DPI alti
description: Valori DPI alti
ms.assetid: 476fe65c-2acd-4a7a-8a76-72d9f010b772
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc7c70e44c497f116348e7b42b260f056d593524
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114699"
---
# <a name="high-dpi"></a>Valori DPI alti

Con l'avanzare delle tecnologie di visualizzazione, i produttori hanno aumentato il numero di pixel supportati dai display. Anche se il testo, le immagini e gli elementi dell'interfaccia utente hanno un aspetto molto più nitido e leggibile su schermi ad alta risoluzione, il sistema operativo deve aumentare le prestazioni per supportare l'esperienza visiva; in caso contrario, tutto sembra più piccolo.

Windows 7 supporta schermi *DPI* elevati. I dati di mercato suggeriscono che le distribuzioni di schermi *DPI* elevati (120-144 punti per pollice (dpi)) aumenteranno nell'intervallo di tempo di Windows 7. Quando si eseguono risoluzioni native su queste schermate, molte applicazioni vengono visualizzate molto piccole a meno che non usino *valori DPI alti.* Alcune applicazioni, ad esempio Windows Internet Explorer, hanno funzionalità di ridimensionamento dei caratteri che consentono agli utenti di eseguire lo zoom avanti e indietro, ma molte applicazioni no. La *funzionalità High DPI (Valori DPI* alti) in Windows 7:

-   Garantisce che le esperienze di Windows e delle applicazioni siano ottimali nell'hardware standard ( le *impostazioni DPI* sono ottimizzate in modo da corrispondere alle funzionalità dell'hardware).
-   Consente alla shell di Windows e ad altre applicazioni basate su Windows di avere un aspetto positivo con impostazioni *DPI* diverse.
-   Rispetta le impostazioni *DPI* predefinite in base alle specifiche e alle funzionalità hardware.
-   Consente agli utenti di personalizzare *le impostazioni DPI* senza riavvio.
-   Assicura che lo schermo sia sempre impostato sulla risoluzione nativa.

La funzionalità *di ridimensionamento DPI* di Windows ridimensiona i tipi di carattere e gli elementi dell'interfaccia utente (ad esempio pulsanti, icone e campi di input) in base a una percentuale calcolata, come specificato dall'impostazione *DPI.* Questo comportamento è diverso dal ridimensionamento che si verifica quando la risoluzione dello schermo viene abbassata. Nel caso del ridimensionamento *DPI,* Windows offre tipi di carattere ed elementi dell'interfaccia utente che vengono disegnati con più pixel, con un'esperienza Windows più grande, più fedeltà e più nitida. Le applicazioni Windows di terze parti possono sfruttare le impostazioni *high DPI* e regolare l'interfaccia utente di conseguenza, dichiarandosi in grado di riconoscere *i valori DPI* alti. Gli sviluppatori di applicazioni non devono più presupporre che 96 dpi sia la risoluzione ideale per tutte le applicazioni.

Per altre informazioni su *High DPI* e sulla scrittura di applicazioni che sono in grado di riconoscere *DPI* elevato, vedere [High DPI](../hidpi/high-dpi-desktop-application-development-on-windows.md).

 

 

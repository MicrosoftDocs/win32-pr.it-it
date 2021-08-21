---
title: Architettura (Framework servizi di testo)
description: Architettura
ms.assetid: 6ef6ba1f-fcbb-4ede-bc6f-3da66135ea69
keywords:
- Framework servizi di testo (TSF), architettura
- TSF (Framework servizi di testo),architettura
- servizi di testo, architettura
- applicazioni abilitate per TSF, architettura
- Framework servizi di testo (TSF), componenti
- TSF (Framework servizi di testo), componenti
- servizi di testo, componenti
- applicazioni abilitate per TSF, componenti
- Framework servizi di testo (TSF), applicazioni
- TSF (Framework servizi di testo),applicazioni
- servizi di testo, applicazioni
- Applicazioni abilitate per TSF, informazioni
- Framework servizi di testo (TSF), servizi di testo
- TSF (Framework servizi di testo), servizi di testo
- servizi di testo, informazioni
- applicazioni abilitate per TSF, servizi di testo
- Framework servizi di testo (TSF), TSF manager
- TSF (Framework servizi di testo),Gestione TSF
- servizi di testo, gestione TSF
- Applicazioni abilitate per TSF, gestione TSF
- Gestione TSF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192c7e6694b4e6a0883cfe44a7251e089e13a855fc4bc266c21dfb2ea1b0e43e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118880151"
---
# <a name="architecture-text-services-framework"></a>Architettura (Framework servizi di testo)

Framework servizi di testo include tre componenti primari:

-   **Applicazioni:** Le operazioni dell'applicazione includono in genere la visualizzazione, la modifica diretta e l'archiviazione del testo. Un'applicazione fornisce l'accesso al testo implementando un server COM che supporta determinate interfacce e comunica con TSF usando le interfacce estense dal gestore TSF. In questa documentazione, il termine applicazione si riferisce a un'applicazione abilitata per TSF, se non diversamente specificato.
-   **Servizi di testo:** Un servizio di testo funziona come provider di testo per un'applicazione. Un servizio di testo può ottenere testo da e scrivere testo in un'applicazione. Un servizio di testo può anche associare dati e proprietà a un blocco di testo. Un servizio di testo viene implementato come server COM in-process che si registra con TSF. Dopo la registrazione, l'utente interagisce con il servizio di testo usando la barra della lingua o i tasti di scelta rapida. È possibile installare più servizi di testo.
-   **Gestione TSF:** Il gestore TSF funziona come mediatore tra un'applicazione e uno o più servizi di testo. Un servizio di testo non interagisce mai direttamente con un'applicazione. Tutte le comunicazioni passano attraverso il gestore TSF. Il gestore TSF viene implementato dal sistema operativo e non può essere sostituito. In questa documentazione, il termine manager fa riferimento al gestore TSF, se non diversamente specificato.

La figura seguente mostra gli elementi principali dell'architettura di TSF.

![architettura del framework dei servizi di testo](images/tsf-arch.gif)

Con questa architettura, gestione TSF offre un livello di astrazione tra applicazioni e servizi di testo. Questo livello di astrazione consente a un'applicazione e a uno o più servizi di testo di condividere testo e consente a TSF Manager di gestire i servizi di testo.

 

 





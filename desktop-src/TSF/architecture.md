---
title: Architettura (Framework dei servizi di testo)
description: Architettura
ms.assetid: 6ef6ba1f-fcbb-4ede-bc6f-3da66135ea69
keywords:
- Framework servizi di testo (TSF), architettura
- TSF (Framework di servizi di testo), architettura
- Servizi di testo, architettura
- Applicazioni abilitate per TSF, architettura
- Framework servizi di testo (TSF), componenti
- TSF (Framework di servizi di testo), componenti
- Servizi di testo, componenti
- Applicazioni abilitate per TSF, componenti
- Framework servizi di testo (TSF), applicazioni
- TSF (Framework di servizi di testo), applicazioni
- Servizi di testo, applicazioni
- Applicazioni abilitate per TSF, informazioni
- Framework servizi di testo (TSF), servizi di testo
- TSF (Text Services Framework), servizi di testo
- Servizi di testo, informazioni
- Applicazioni abilitate per TSF, servizi di testo
- Framework servizi di testo (TSF), gestione TSF
- TSF (Text Services Framework), gestione TSF
- Servizi di testo, gestione TSF
- Applicazioni abilitate per TSF, gestione TSF
- Gestione TSF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0a300307b3099b4a28a883d5c830c4078cd0bb
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104565282"
---
# <a name="architecture-text-services-framework"></a>Architettura (Framework dei servizi di testo)

Il Framework di servizi di testo include tre componenti principali:

-   **Applicazioni:** Le operazioni dell'applicazione includono in genere la visualizzazione, la modifica diretta e l'archiviazione del testo. Un'applicazione fornisce l'accesso al testo implementando un server COM che supporta determinate interfacce e comunica con TSF usando le interfacce esposte dal gestore TSF. In questa documentazione, il termine applicazione si riferisce a un'applicazione abilitata per TSF, salvo diversa indicazione.
-   **Servizi di testo:** Un servizio di testo funziona come provider di testo per un'applicazione. Un servizio di testo può ottenere testo da e scrivere testo in un'applicazione. Un servizio di testo può inoltre associare dati e proprietà a un blocco di testo. Un servizio di testo viene implementato come un server COM in-process che si registra con TSF. Quando viene registrato, l'utente interagisce con il servizio di testo utilizzando la barra della lingua o i tasti di scelta rapida. È possibile installare più servizi di testo.
-   **Gestione TSF:** Il gestore di TSF funziona come Mediator tra un'applicazione e uno o più servizi di testo. Un servizio di testo non interagisce mai direttamente con un'applicazione. Tutte le comunicazioni passano attraverso gestione TSF. Il gestore TSF viene implementato dal sistema operativo e non può essere sostituito. In questa documentazione, il termine gestione si riferisce al gestore di TSF, salvo diversa indicazione.

La figura seguente Mostra gli elementi architetturali principali di TSF.

![architettura del Framework dei servizi di testo](images/tsf-arch.gif)

Con questa architettura, gestione TSF fornisce un livello di astrazione tra le applicazioni e i servizi di testo. Questo livello di astrazione consente a un'applicazione e uno o più servizi di testo di condividere il testo e consente al gestore di TSF di gestire i servizi di testo.

 

 





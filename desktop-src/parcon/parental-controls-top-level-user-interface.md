---
description: Controllo genitori Top-Level Interfaccia utente
ms.assetid: c6dfd3bc-191f-42d1-b9de-cc85a2da0a99
title: Controllo genitori Top-Level Interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221c989a1c4aed25a15fe0942bb5f1f540246a40d349e452ce4efe518454d523
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869178"
---
# <a name="parental-controls-top-level-user-interface"></a>Controllo genitori Top-Level Interfaccia utente

Il forte collegamento tra gli account utente Family Safety e Windows ha guidato una categoria combinata visualizzata come Account utente e **Family Safety** in Pannello di controllo per gli SKU orientati ai consumer di Windows Vista.

> [!Note]  
> La categoria verrà visualizzata come **Account utente quando** viene aggiunto un computer con funzionalità di aggiunta a un dominio.

 

Se non è ancora stato configurato un account utente standard per l'utente controllato, un collegamento in Pannello di controllo fornisce un flusso di lavoro semplice per l'aggiunta di un nuovo account controllato dai genitori.

Dopo la creazione di un account, il Pannello di controllo controllo genitori espone la funzionalità di primo livello per l'utente controllato. Elementi:

-   Restrizioni generali di Controllo genitori per i pulsanti di opzione.
-   I Rapporto attività pulsanti di opzione di controllo indipendenti.
-   Una Impostazioni con il collegamento Restrizioni Web implementate da Microsoft visualizzato in modo condizionale e i tipi di restrizioni principali implementati da Microsoft offline disponibili.
-   Area più Impostazioni visualizzata se Interfaccia utente estensioni sono registrate da Microsoft o da terze parti.
-   Un'area di stato di riepilogo che mostra il nome utente e il riquadro, il collegamento View activity reports (Visualizza report attività) e lo stato delle impostazioni di Controllo genitori. Se attivata, la visualizzazione include il livello di impostazione Filtro contenuto Web (se il filtro Microsoft è attivo) o il nome del filtro se sottoposto a override da un'estensione di terze parti e lo stato delle impostazioni offline per l'utente.

Il pulsante di opzione Abilita controllo genitori generale viene inizialmente impostato sullo stato disattivato. Se attivata da un amministratore, Rapporto attività è attivata anche per impostazione predefinita, ma può essere disattivata in modo indipendente. Come per quasi tutte le impostazioni in Controllo genitori, la configurazione può essere eseguita a livello di codice tramite le API disponibili.

 

 




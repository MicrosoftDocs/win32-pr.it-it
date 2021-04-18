---
description: Controlli padre Top-Level interfaccia utente
ms.assetid: c6dfd3bc-191f-42d1-b9de-cc85a2da0a99
title: Controlli padre Top-Level interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 321475097e25b812aca8d1e65f8b88843ebb1055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313029"
---
# <a name="parental-controls-top-level-user-interface"></a>Controlli padre Top-Level interfaccia utente

Il collegamento forte tra la sicurezza della famiglia e gli account utente di Windows ha guidato una categoria combinata che appare come **account utente e Family Safety** nel pannello di controllo per gli SKU orientati agli utenti di Windows Vista.

> [!Note]  
> La categoria verrà visualizzata come **account utente** quando viene aggiunto un computer con funzionalità di aggiunta al dominio.

 

Se un account utente standard non è stato ancora configurato per l'utente controllato, un collegamento nel pannello di controllo fornisce un semplice flusso di lavoro per l'aggiunta di un nuovo account controllato dal padre.

Dopo la creazione di un account, il pannello di controllo Parental Controls espone la funzionalità di primo livello per l'utente controllato. Elementi

-   Le restrizioni generali dei controlli padre sono i pulsanti di opzione.
-   Pulsante di opzione per la segnalazione di attività indipendenti.
-   Una sezione delle impostazioni con le restrizioni Web implementate da Microsoft viene collegata in modo condizionale e vengono visualizzati i tipi di restrizioni implementate da Microsoft non in linea di base disponibili.
-   Una maggiore area Impostazioni visualizzata se le estensioni dell'interfaccia utente sono registrate da Microsoft o da terze parti.
-   Area di riepilogo dello stato che mostra il nome utente e il riquadro, il collegamento Visualizza report attività e lo stato delle impostazioni dei controlli padre. Se attivata, la visualizzazione include il livello di impostazione del filtro contenuto Web (se il filtro Microsoft è attivo) o il nome del filtro se sottoposto a override da un'estensione di terze parti e lo stato delle impostazioni offline per l'utente.

I controlli padre generali abilitano il pulsante di opzione inizialmente impostato sullo stato disattivato. Una volta attivato da un amministratore, il servizio di report delle attività sarà attivato per impostazione predefinita, ma può essere disattivato in modo indipendente. Come per quasi tutte le impostazioni dei controlli padre, la configurazione può essere eseguita a livello di codice tramite le API disponibili.

 

 




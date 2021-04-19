---
description: Un'estensione dello snap-in allegati fornisce un'interfaccia che gli utenti possono utilizzare per modificare le impostazioni di configurazione specifiche del servizio.
ms.assetid: 6f2dc372-dee4-4793-b943-395c0587ed5e
title: Creazione di un'estensione dello snap-in allegati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513c982acc7e5285f3b4d1510f18b7eb6c9fe1d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315354"
---
# <a name="creating-an-attachment-snap-in-extension"></a>Creazione di un'estensione dello snap-in allegati

Un'estensione dello snap-in allegati fornisce un'interfaccia che gli utenti possono utilizzare per modificare le impostazioni di configurazione specifiche del servizio. L'estensione dello snap-in allegati deve soddisfare i requisiti di MMC per essere un'estensione di snap-in valida. Per ulteriori informazioni su questi requisiti, vedere la documentazione di [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) .

Oltre alle interfacce richieste da MMC, un'estensione dello snap-in allegati deve implementare l'interfaccia COM [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo). Gli snap-in di configurazione della sicurezza chiamano i metodi di questa interfaccia per determinare se i dati di configurazione sono stati modificati e, in caso affermativo, per aggiornare il database di sicurezza. Lo snap-in allegati deve archiviare tutte le modifiche alla configurazione fino a quando gli snap-in Configurazione sicurezza non recuperano i dati.

Un'estensione dello snap-in allegati deve fornire le funzionalità seguenti:

-   [Visualizzazione delle informazioni di configurazione e analisi](displaying-configuration-and-analysis-information.md)
-   [Modificare le informazioni di configurazione nell'interfaccia utente](modifying-configuration-information-in-the-user-interface.md)
-   [Modificare le informazioni di configurazione nel database di sicurezza](modifying-configuration-information-in-the-database.md)

Per supportare l'estensione dello snap-in durante l'esecuzione di queste attività, gli snap-in di configurazione della sicurezza implementano un'interfaccia COM, [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata), che fornisce i metodi che possono essere chiamati dall'estensione dello snap-in per inizializzare se stesso ed eseguire query sulle informazioni dal database di sicurezza.

Dopo aver creato l'estensione dello snap-in allegato, è necessario registrarla con gli snap-in di configurazione della sicurezza, come descritto in [registrazione di un'estensione dello snap-in allegato](registering-an-attachment-snap-in-extension.md).

 

 

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
# <a name="creating-an-attachment-snap-in-extension"></a><span data-ttu-id="e2a5d-103">Creazione di un'estensione dello snap-in allegati</span><span class="sxs-lookup"><span data-stu-id="e2a5d-103">Creating an Attachment Snap-in Extension</span></span>

<span data-ttu-id="e2a5d-104">Un'estensione dello snap-in allegati fornisce un'interfaccia che gli utenti possono utilizzare per modificare le impostazioni di configurazione specifiche del servizio.</span><span class="sxs-lookup"><span data-stu-id="e2a5d-104">An attachment snap-in extension provides an interface that users can use to change service-specific configuration settings.</span></span> <span data-ttu-id="e2a5d-105">L'estensione dello snap-in allegati deve soddisfare i requisiti di MMC per essere un'estensione di snap-in valida.</span><span class="sxs-lookup"><span data-stu-id="e2a5d-105">The attachment snap-in extension must fulfill the MMC requirements to be a valid snap-in extension.</span></span> <span data-ttu-id="e2a5d-106">Per ulteriori informazioni su questi requisiti, vedere la documentazione di [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) .</span><span class="sxs-lookup"><span data-stu-id="e2a5d-106">For more information on those requirements, see the [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) documentation.</span></span>

<span data-ttu-id="e2a5d-107">Oltre alle interfacce richieste da MMC, un'estensione dello snap-in allegati deve implementare l'interfaccia COM [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo).</span><span class="sxs-lookup"><span data-stu-id="e2a5d-107">In addition to the interfaces required by MMC, an attachment snap-in extension must implement the COM interface [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo).</span></span> <span data-ttu-id="e2a5d-108">Gli snap-in di configurazione della sicurezza chiamano i metodi di questa interfaccia per determinare se i dati di configurazione sono stati modificati e, in caso affermativo, per aggiornare il database di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="e2a5d-108">The Security Configuration snap-ins call methods of this interface to determine whether the configuration data has changed, and if so, to update the security database.</span></span> <span data-ttu-id="e2a5d-109">Lo snap-in allegati deve archiviare tutte le modifiche alla configurazione fino a quando gli snap-in Configurazione sicurezza non recuperano i dati.</span><span class="sxs-lookup"><span data-stu-id="e2a5d-109">The attachment snap-in must store any configuration changes until the Security Configuration snap-ins retrieves that data.</span></span>

<span data-ttu-id="e2a5d-110">Un'estensione dello snap-in allegati deve fornire le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="e2a5d-110">An attachment snap-in extension must provide the following functionality:</span></span>

-   [<span data-ttu-id="e2a5d-111">Visualizzazione delle informazioni di configurazione e analisi</span><span class="sxs-lookup"><span data-stu-id="e2a5d-111">Display Configuration and Analysis Information</span></span>](displaying-configuration-and-analysis-information.md)
-   [<span data-ttu-id="e2a5d-112">Modificare le informazioni di configurazione nell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="e2a5d-112">Modify Configuration Information in the User Interface</span></span>](modifying-configuration-information-in-the-user-interface.md)
-   [<span data-ttu-id="e2a5d-113">Modificare le informazioni di configurazione nel database di sicurezza</span><span class="sxs-lookup"><span data-stu-id="e2a5d-113">Modify Configuration Information in the Security Database</span></span>](modifying-configuration-information-in-the-database.md)

<span data-ttu-id="e2a5d-114">Per supportare l'estensione dello snap-in durante l'esecuzione di queste attività, gli snap-in di configurazione della sicurezza implementano un'interfaccia COM, [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata), che fornisce i metodi che possono essere chiamati dall'estensione dello snap-in per inizializzare se stesso ed eseguire query sulle informazioni dal database di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="e2a5d-114">To assist your snap-in extension in performing these tasks, the Security Configuration snap-ins implement a COM interface, [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata), which provides methods your snap-in extension can call in order to initialize itself and query information from the security database.</span></span>

<span data-ttu-id="e2a5d-115">Dopo aver creato l'estensione dello snap-in allegato, è necessario registrarla con gli snap-in di configurazione della sicurezza, come descritto in [registrazione di un'estensione dello snap-in allegato](registering-an-attachment-snap-in-extension.md).</span><span class="sxs-lookup"><span data-stu-id="e2a5d-115">After you have created your attachment snap-in extension, you must register it with the Security Configuration snap-ins as described in [Registering an Attachment Snap-in Extension](registering-an-attachment-snap-in-extension.md).</span></span>

 

 

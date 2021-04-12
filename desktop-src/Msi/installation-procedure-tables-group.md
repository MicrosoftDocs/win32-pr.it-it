---
description: Le tabelle del gruppo procedura di installazione controllano le attività eseguite durante l'installazione mediante azioni standard e azioni personalizzate.
ms.assetid: dff7cf4a-89a2-47b0-9038-93b79c0d915a
title: Gruppo tabelle procedure di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbb3c5eb0306941d3cdd02bf7f994270ca0d6490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349756"
---
# <a name="installation-procedure-tables-group"></a><span data-ttu-id="5bad2-103">Gruppo tabelle procedure di installazione</span><span class="sxs-lookup"><span data-stu-id="5bad2-103">Installation Procedure Tables Group</span></span>

<span data-ttu-id="5bad2-104">Le tabelle del gruppo procedura di installazione controllano le attività eseguite durante l'installazione mediante [azioni standard](standard-actions.md) e [azioni personalizzate](custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="5bad2-104">The tables in the Installation Procedure group control tasks performed during the installation by [standard actions](standard-actions.md) and [custom actions](custom-actions.md).</span></span>

<span data-ttu-id="5bad2-105">Alcune tabelle in questo gruppo controllano un'azione di alto livello fornendo una sequenza di azioni.</span><span class="sxs-lookup"><span data-stu-id="5bad2-105">Some of the tables in this group control a high level action by providing a sequence of actions.</span></span> <span data-ttu-id="5bad2-106">Ognuna delle tabelle di sequenza seguenti controlla una parte di un'azione di alto livello.</span><span class="sxs-lookup"><span data-stu-id="5bad2-106">Each of the following sequence tables controls a portion of a high level action.</span></span>

-   [<span data-ttu-id="5bad2-107">Tabella InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="5bad2-107">InstallUISequence table</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="5bad2-108">Tabella InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="5bad2-108">InstallExecuteSequence table</span></span>](installexecutesequence-table.md)
-   [<span data-ttu-id="5bad2-109">Tabella AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="5bad2-109">AdminUISequence table</span></span>](adminuisequence-table.md)
-   [<span data-ttu-id="5bad2-110">Tabella AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="5bad2-110">AdminExecuteSequence table</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="5bad2-111">Tabella AdvtUISequence</span><span class="sxs-lookup"><span data-stu-id="5bad2-111">AdvtUISequence table</span></span>](advtuisequence-table.md)
-   [<span data-ttu-id="5bad2-112">Tabella AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="5bad2-112">AdvtExecuteSequence table</span></span>](advtexecutesequence-table.md)

<span data-ttu-id="5bad2-113">In alcune situazioni è necessario che un'installazione esegua operazioni che non è possibile utilizzare solo le [azioni standard](standard-actions.md).</span><span class="sxs-lookup"><span data-stu-id="5bad2-113">There may be situations in which an installation needs to do something that is not possible using only [standard actions](standard-actions.md).</span></span> <span data-ttu-id="5bad2-114">Per fornire il massimo livello di flessibilità, il programma di installazione fornisce agli autori di installazione la possibilità di creare azioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="5bad2-114">To provide the greatest degree of flexibility, the installer provides setup authors the ability to create their own custom actions.</span></span> <span data-ttu-id="5bad2-115">Se si dispone di azioni personalizzate, è necessario registrarle con il programma di installazione popolando la tabella CustomAction.</span><span class="sxs-lookup"><span data-stu-id="5bad2-115">If you have any custom actions, you should register them with the installer by populating the CustomAction Table.</span></span>

<span data-ttu-id="5bad2-116">La [tabella CustomAction](customaction-table.md) fornisce i mezzi per integrare il codice personalizzato e i dati nel processo di installazione.</span><span class="sxs-lookup"><span data-stu-id="5bad2-116">The [CustomAction table](customaction-table.md) provides the means of integrating custom code and data into the installation process.</span></span> <span data-ttu-id="5bad2-117">Il codice eseguito può essere un flusso contenuto all'interno del database, un file installato di recente o un eseguibile esistente.</span><span class="sxs-lookup"><span data-stu-id="5bad2-117">The code that is executed can be a stream contained within the database, a recently installed file, or an existing executable.</span></span>

<span data-ttu-id="5bad2-118">Le tabelle seguenti estendono le funzionalità del programma di installazione per modificare file e cartelle durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="5bad2-118">The following tables extend the installer's capabilities to manipulate files and folders during the installation.</span></span>

-   <span data-ttu-id="5bad2-119">La [tabella RemoveFile](removefile-table.md) contiene un elenco di file che vengono rimossi durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="5bad2-119">The [RemoveFile table](removefile-table.md) contains a list of files that are removed during the installation.</span></span>
-   <span data-ttu-id="5bad2-120">La [tabella RemoveIniFile](removeinifile-table.md) contiene le informazioni che un'applicazione deve rimuovere dai file ini.</span><span class="sxs-lookup"><span data-stu-id="5bad2-120">The [RemoveIniFile table](removeinifile-table.md) contains the information an application needs to remove from .ini files.</span></span>
-   <span data-ttu-id="5bad2-121">La [tabella RemoveRegistry](removeregistry-table.md) contiene le informazioni che vengono eliminate dal registro di sistema quando viene selezionato il componente corrispondente da installare.</span><span class="sxs-lookup"><span data-stu-id="5bad2-121">The [RemoveRegistry table](removeregistry-table.md) contains the information which is deleted from the system registry when the corresponding component is selected to be installed.</span></span>
-   <span data-ttu-id="5bad2-122">La [tabella CreateFolder](createfolder-table.md) elenca le cartelle che devono essere create durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="5bad2-122">The [CreateFolder table](createfolder-table.md) lists the folders that must be created during the installation.</span></span> <span data-ttu-id="5bad2-123">Sebbene il programma di installazione crei le cartelle non appena sono necessarie, queste vengono rimosse non appena sono vuote.</span><span class="sxs-lookup"><span data-stu-id="5bad2-123">Although the installer creates folders as they are needed, these are removed as soon as they are empty.</span></span> <span data-ttu-id="5bad2-124">L'elenco di cartelle nella tabella CreateFolder non viene eliminato fino a quando il componente non viene disinstallato.</span><span class="sxs-lookup"><span data-stu-id="5bad2-124">Folders list in the CreateFolder table are not deleted until the component is uninstalled.</span></span>
-   <span data-ttu-id="5bad2-125">La [tabella MoveFile](movefile-table.md) contiene un elenco di file da spostare o copiare da una directory di origine specificata nel computer dell'utente in una directory di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5bad2-125">The [MoveFile table](movefile-table.md) contains a list of files to be moved or copied from a specified source directory on the user's computer to a destination directory.</span></span> <span data-ttu-id="5bad2-126">Non è necessario usare la tabella MoveFile per descrivere i file associati ai componenti da installare.</span><span class="sxs-lookup"><span data-stu-id="5bad2-126">It is not necessary to use the MoveFile table to describe the files associated with the components you are installing.</span></span>

<span data-ttu-id="5bad2-127">Per configurare le condizioni necessarie che devono essere soddisfatte per avviare l'installazione, popolare la tabella LaunchCondition.</span><span class="sxs-lookup"><span data-stu-id="5bad2-127">To set up necessary conditions that must be met to initiate the installation, populate the LaunchCondition table.</span></span>

<span data-ttu-id="5bad2-128">La [tabella LaunchCondition](launchcondition-table.md) contiene un elenco di condizioni che devono essere soddisfatte affinché l'azione abbia esito positivo.</span><span class="sxs-lookup"><span data-stu-id="5bad2-128">The [LaunchCondition table](launchcondition-table.md) contains a list of conditions, all of which must be satisfied for the action to succeed.</span></span>

 

 




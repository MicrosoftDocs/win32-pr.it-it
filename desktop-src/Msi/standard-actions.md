---
description: Un'azione incapsula una funzione tipica eseguita durante l'installazione o la manutenzione di un'applicazione. Windows Installer dispone di molte azioni standard predefinite. Gli sviluppatori di pacchetti di installazione possono anche creare azioni personalizzate.
ms.assetid: 33651988-e371-4258-96a7-bcd7d6762161
title: Azioni standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ed4f9c2a7fc6671442f6b72cd10889e2fcf5e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227056"
---
# <a name="standard-actions"></a><span data-ttu-id="e7989-105">Azioni standard</span><span class="sxs-lookup"><span data-stu-id="e7989-105">Standard Actions</span></span>

<span data-ttu-id="e7989-106">Un'azione incapsula una funzione tipica eseguita durante l'installazione o la manutenzione di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e7989-106">An action encapsulates a typical function performed during the installation or maintenance of an application.</span></span> <span data-ttu-id="e7989-107">Windows Installer dispone di molte azioni standard predefinite.</span><span class="sxs-lookup"><span data-stu-id="e7989-107">Windows Installer has many built-in standard actions.</span></span> <span data-ttu-id="e7989-108">Gli sviluppatori di pacchetti di installazione possono anche creare [azioni personalizzate](custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="e7989-108">Developers of installation packages can also author their own [custom actions](custom-actions.md).</span></span>

<span data-ttu-id="e7989-109">Esempi di azioni standard del programma di installazione includono:</span><span class="sxs-lookup"><span data-stu-id="e7989-109">Examples of installer standard actions include:</span></span>

-   <span data-ttu-id="e7989-110">[Azione CreateShortcuts](createshortcuts-action.md): gestisce la creazione di collegamenti ai file installati con l'applicazione corrente.</span><span class="sxs-lookup"><span data-stu-id="e7989-110">[CreateShortcuts action](createshortcuts-action.md): Manages the creation of shortcuts to files installed with the current application.</span></span> <span data-ttu-id="e7989-111">Questa azione utilizza la [tabella dei collegamenti](shortcut-table.md) per i relativi dati.</span><span class="sxs-lookup"><span data-stu-id="e7989-111">This action uses the [Shortcut table](shortcut-table.md) for its data.</span></span>
-   <span data-ttu-id="e7989-112">[Azione InstallFiles](installfiles-action.md): copia i file selezionati dalla directory di origine alla directory di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e7989-112">[InstallFiles action](installfiles-action.md): Copies selected files from the source directory to the destination directory.</span></span> <span data-ttu-id="e7989-113">Questa azione utilizza la [tabella file](file-table.md) per i relativi dati.</span><span class="sxs-lookup"><span data-stu-id="e7989-113">This action uses the [File table](file-table.md) for its data.</span></span>
-   <span data-ttu-id="e7989-114">[Azione WriteRegistryValori consente](writeregistryvalues-action.md): configura le informazioni del registro di sistema richieste dall'applicazione nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e7989-114">[WriteRegistryValues action](writeregistryvalues-action.md): Sets up registry information the application requires in the registry.</span></span> <span data-ttu-id="e7989-115">Questa azione utilizza la [tabella del registro di sistema](registry-table.md) per i relativi dati.</span><span class="sxs-lookup"><span data-stu-id="e7989-115">This action uses the [Registry table](registry-table.md) for its data.</span></span>

<span data-ttu-id="e7989-116">Le sezioni seguenti illustrano le azioni standard.</span><span class="sxs-lookup"><span data-stu-id="e7989-116">The following sections discuss standard actions.</span></span>

-   [<span data-ttu-id="e7989-117">Informazioni sulle azioni standard</span><span class="sxs-lookup"><span data-stu-id="e7989-117">About Standard Actions</span></span>](about-standard-actions.md)
-   [<span data-ttu-id="e7989-118">Uso di azioni standard</span><span class="sxs-lookup"><span data-stu-id="e7989-118">Using Standard Actions</span></span>](using-standard-actions.md)
-   [<span data-ttu-id="e7989-119">Guida di riferimento alle azioni standard</span><span class="sxs-lookup"><span data-stu-id="e7989-119">Standard Actions Reference</span></span>](standard-actions-reference.md)

 

 




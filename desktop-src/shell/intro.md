---
description: L'interfaccia utente di Windows consente agli utenti di accedere a un'ampia gamma di oggetti necessari per eseguire le applicazioni e gestire il sistema operativo.
title: Guida per gli sviluppatori della shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8f88ef25-3645-4f54-9453-41f919c0fc0a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1be17ca90b7138294be3e1b34fa3fcb4dcb4227a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993853"
---
# <a name="shell-developers-guide"></a><span data-ttu-id="4f35d-103">Guida per gli sviluppatori della shell</span><span class="sxs-lookup"><span data-stu-id="4f35d-103">Shell Developer's Guide</span></span>

<span data-ttu-id="4f35d-104">L'interfaccia utente di Windows consente agli utenti di accedere a un'ampia gamma di oggetti necessari per eseguire le applicazioni e gestire il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4f35d-104">The Windows UI provides users with access to a wide variety of objects necessary to run applications and manage the operating system.</span></span> <span data-ttu-id="4f35d-105">I più numerosi e familiari di questi oggetti sono le cartelle e i file che risiedono in unità disco del computer.</span><span class="sxs-lookup"><span data-stu-id="4f35d-105">The most numerous and familiar of these objects are the folders and files that reside on computer disk drives.</span></span> <span data-ttu-id="4f35d-106">Sono inoltre disponibili numerosi oggetti virtuali che consentono all'utente di eseguire attività quali l'invio di file alle stampanti remote o l'accesso al Cestino.</span><span class="sxs-lookup"><span data-stu-id="4f35d-106">There are also a number of virtual objects that allow the user to do tasks such as sending files to remote printers or accessing the Recycle Bin.</span></span> <span data-ttu-id="4f35d-107">La shell organizza questi oggetti in uno spazio dei nomi gerarchico e fornisce agli utenti e alle applicazioni un modo coerente ed efficiente per accedere e gestire gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="4f35d-107">The Shell organizes these objects into a hierarchical namespace, and provides users and applications with a consistent and efficient way to access and manage objects.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4f35d-108">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="4f35d-108">In this section</span></span>

-   [<span data-ttu-id="4f35d-109">Considerazioni sulla sicurezza: shell Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="4f35d-109">Security Considerations: Microsoft Windows Shell</span></span>](sec-shell.md)
-   [<span data-ttu-id="4f35d-110">Linee guida per l'implementazione di estensioni In-Process</span><span class="sxs-lookup"><span data-stu-id="4f35d-110">Guidance for Implementing In-Process Extensions</span></span>](shell-and-managed-code.md)
-   [<span data-ttu-id="4f35d-111">Versioni di Shell e controlli comuni</span><span class="sxs-lookup"><span data-stu-id="4f35d-111">Shell and Common Controls Versions</span></span>](versions.md)
-   [<span data-ttu-id="4f35d-112">Implementazione delle interfacce di oggetti della cartella di base</span><span class="sxs-lookup"><span data-stu-id="4f35d-112">Implementing the Basic Folder Object Interfaces</span></span>](nse-implement.md)
-   [<span data-ttu-id="4f35d-113">Implementazione di un formato di file personalizzato</span><span class="sxs-lookup"><span data-stu-id="4f35d-113">Implementing a Custom File Format</span></span>](customizing-file-types-bumper.md)
-   [<span data-ttu-id="4f35d-114">Estendibilità della shell (creazione di un'origine dati)</span><span class="sxs-lookup"><span data-stu-id="4f35d-114">Shell Extensibility (Creating a Data Source)</span></span>](shell-extensibility-bumper.md)
-   [<span data-ttu-id="4f35d-115">Implementazione degli elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="4f35d-115">Implementing Control Panel Items</span></span>](control-panel-applications.md)
-   [<span data-ttu-id="4f35d-116">Supporto delle applicazioni shell</span><span class="sxs-lookup"><span data-stu-id="4f35d-116">Supporting Shell Applications</span></span>](application-support-bumper.md)
-   [<span data-ttu-id="4f35d-117">Argomenti della shell legacy</span><span class="sxs-lookup"><span data-stu-id="4f35d-117">Legacy Shell Topics</span></span>](miscellaneous-topics-bumper.md)

## <a name="document-conventions"></a><span data-ttu-id="4f35d-118">Convenzioni documento</span><span class="sxs-lookup"><span data-stu-id="4f35d-118">Document Conventions</span></span>

<span data-ttu-id="4f35d-119">La guida per gli sviluppatori della shell segue le normali convenzioni dei documenti Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="4f35d-119">The Shell Developers's Guide follows the usual Windows Software Development Kit (SDK) document conventions.</span></span> <span data-ttu-id="4f35d-120">Si noti che in particolare è necessario tenere presente due convenzioni:</span><span class="sxs-lookup"><span data-stu-id="4f35d-120">Two conventions in particular should be noted:</span></span>

-   <span data-ttu-id="4f35d-121">Il codice di esempio omette il normale codice di correzione degli errori.</span><span class="sxs-lookup"><span data-stu-id="4f35d-121">Sample code omits normal error-correction code.</span></span> <span data-ttu-id="4f35d-122">Questo codice è stato rimosso solo per rendere il codice più leggibile.</span><span class="sxs-lookup"><span data-stu-id="4f35d-122">This code has been removed only to make the code more readable.</span></span> <span data-ttu-id="4f35d-123">È necessario includere tutto il codice di correzione degli errori appropriato nelle proprie applicazioni.</span><span class="sxs-lookup"><span data-stu-id="4f35d-123">You should include all appropriate error-correction code in your own applications.</span></span>
-   <span data-ttu-id="4f35d-124">Per rendere evidenti le voci del registro di sistema, la chiave, la sottochiave e i nomi di voce, nonché i valori, vengono visualizzati con un tipo di carattere standard.</span><span class="sxs-lookup"><span data-stu-id="4f35d-124">To make sample registry entries clear, key, subkey, and entry names as well as values are displayed with a standard font.</span></span> <span data-ttu-id="4f35d-125">I nomi degli elementi definiti dall'utente o dall'applicazione sono in corsivo.</span><span class="sxs-lookup"><span data-stu-id="4f35d-125">User or application-defined item names are italicized.</span></span>

 

 




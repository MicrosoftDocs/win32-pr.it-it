---
description: .
ms.assetid: 80b97bfc-4212-4401-a4a9-d96e2f39be60
title: La libreria di file sostituisce la cartella del documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15431f5fb5fb5e73dbaf171625a0a6582fa7add2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884785"
---
# <a name="file-library-replaces-document-folder"></a><span data-ttu-id="11a4a-103">La libreria di file sostituisce la cartella del documento</span><span class="sxs-lookup"><span data-stu-id="11a4a-103">File Library Replaces Document Folder</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="11a4a-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="11a4a-104">Affected Platforms</span></span>

<span data-ttu-id="11a4a-105">**Client** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="11a4a-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="11a4a-106">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="11a4a-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="11a4a-107">Effetto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="11a4a-107">Feature Impact</span></span>

<span data-ttu-id="11a4a-108">**Gravità** -medio</span><span class="sxs-lookup"><span data-stu-id="11a4a-108">**Severity** - Medium</span></span>  
<span data-ttu-id="11a4a-109">**Frequenza** -alta</span><span class="sxs-lookup"><span data-stu-id="11a4a-109">**Frequency** - High</span></span>  











## <a name="description"></a><span data-ttu-id="11a4a-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11a4a-110">Description</span></span>

<span data-ttu-id="11a4a-111">Le librerie offrono un'esperienza centralizzata simile a una cartella per l'archiviazione di file, la ricerca e l'accesso in più posizioni, sia locali che remote.</span><span class="sxs-lookup"><span data-stu-id="11a4a-111">Libraries provide a centralized folder-like experience for file storage, search, and access across multiple locations, both local and remote.</span></span>

<span data-ttu-id="11a4a-112">I percorsi predefiniti usati dalle finestre di dialogo file comuni (ad esempio, Apri e Salva) sono stati modificati dalla cartella documenti alla raccolta documenti.</span><span class="sxs-lookup"><span data-stu-id="11a4a-112">The default locations used by common file dialogs (for example, Open, and Save) have been changed from the Document Folder to the Documents Library.</span></span> <span data-ttu-id="11a4a-113">L'interfaccia utente è invariata, ma ora l'utente sarà in grado di visualizzare, esplorare ed eseguire ricerche nella libreria usando varie visualizzazioni di disposizione.</span><span class="sxs-lookup"><span data-stu-id="11a4a-113">The User Interface is unchanged, but the user will now be able to view, browse, and search the Library using various arrangement views.</span></span> <span data-ttu-id="11a4a-114">I file verranno salvati nel percorso di salvataggio predefinito della libreria, a meno che l'utente non modifichi il percorso di salvataggio predefinito o scelga un'altra cartella.</span><span class="sxs-lookup"><span data-stu-id="11a4a-114">Files will be saved into the Library default save location unless the user changes the default save location or chooses a different folder.</span></span>

<span data-ttu-id="11a4a-115">Gli sviluppatori possono creare librerie personalizzate o aggiungere percorsi alle librerie esistenti usando l'interfaccia IShellLibrary.</span><span class="sxs-lookup"><span data-stu-id="11a4a-115">Developers could create their own libraries or add locations to existing libraries using the IShellLibrary interface.</span></span> <span data-ttu-id="11a4a-116">Gli utenti possono trovare le librerie usando il sistema di cartelle note, ad esempio FOLDERID \_ documentsLibrary.</span><span class="sxs-lookup"><span data-stu-id="11a4a-116">Users can find libraries by using the Known Folder system (for example, FOLDERID\_DocumentsLibrary).</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="11a4a-117">Manifesto di effetto</span><span class="sxs-lookup"><span data-stu-id="11a4a-117">Manifestation of Impact</span></span>

<span data-ttu-id="11a4a-118">La libreria è a sua volta un file e non una cartella.</span><span class="sxs-lookup"><span data-stu-id="11a4a-118">The Library is itself a file, and not a folder.</span></span> <span data-ttu-id="11a4a-119">Le manipolazioni del percorso potrebbero pertanto causare errori dovuti al tentativo da parte dell'applicazione di concatenare i file ai file.</span><span class="sxs-lookup"><span data-stu-id="11a4a-119">Therefore, path manipulations could result errors due to the attempt by the application to concatenate files to files.</span></span>

## <a name="solution"></a><span data-ttu-id="11a4a-120">Soluzione</span><span class="sxs-lookup"><span data-stu-id="11a4a-120">Solution</span></span>

<span data-ttu-id="11a4a-121">Quando si usa IFileDialog, è necessario usare il metodo GetResult invece della combinazione di GetFolder e GetFileName come nelle versioni precedenti del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="11a4a-121">When using IFileDialog, you must use GetResult method instead of combination of GetFolder and GetFilename as you would in the previous operating system versions.</span></span> <span data-ttu-id="11a4a-122">Usare le API della shell laddove possibile per interagire con gli elementi nello spazio dei nomi della shell, ad esempio IShellItem, e modificarli.</span><span class="sxs-lookup"><span data-stu-id="11a4a-122">Use the Shell APIs where possible to interact with and manipulate items in the Shell Namespace (for example, IShellItem).</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="11a4a-123">Sfruttando le funzionalità</span><span class="sxs-lookup"><span data-stu-id="11a4a-123">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="11a4a-124">Se si vuole creare librerie personalizzate o aggiungere percorsi alle librerie esistenti, è necessario usare l'API IShellLibrary.</span><span class="sxs-lookup"><span data-stu-id="11a4a-124">If you want to create your own libraries or add locations to existing libraries, you must use IShellLibrary API.</span></span> <span data-ttu-id="11a4a-125">Le librerie sono stesse cartelle della shell, in modo che sia possibile enumerarle come qualsiasi altra cartella della shell.</span><span class="sxs-lookup"><span data-stu-id="11a4a-125">Libraries are themselves Shell Folders so you can enumerate them just like any other Shell Folder.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="11a4a-126">Compatibilità, prestazioni, affidabilità e test di usabilità</span><span class="sxs-lookup"><span data-stu-id="11a4a-126">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="11a4a-127">Utilizzando la finestra di dialogo file comune si garantisce che gli utenti possano salvare direttamente le proprie raccolte.</span><span class="sxs-lookup"><span data-stu-id="11a4a-127">Using the common file dialog will ensure that users can save directly to their libraries.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="11a4a-128">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="11a4a-128">Links to Other Resources</span></span>

-   <span data-ttu-id="11a4a-129">**Librerie di Windows:**https://msdn.microsoft.com/library/dd758096(VS.85).aspx</span><span class="sxs-lookup"><span data-stu-id="11a4a-129">**Windows Libraries:** https://msdn.microsoft.com/library/dd758096(VS.85).aspx</span></span>
-   <span data-ttu-id="11a4a-130">**Mantenimento della sincronizzazione con una libreria:**https://msdn.microsoft.com/library/dd758094(VS.85).aspx\#library\_keeping\_in\_sync</span><span class="sxs-lookup"><span data-stu-id="11a4a-130">**Keeping in sync with a library:** https://msdn.microsoft.com/library/dd758094(VS.85).aspx\#library\_keeping\_in\_sync</span></span>

 

 




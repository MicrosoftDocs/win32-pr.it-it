---
description: La raccolta file sostituisce la cartella del documento
ms.assetid: 80b97bfc-4212-4401-a4a9-d96e2f39be60
title: La raccolta file sostituisce la cartella del documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699c645d574012a419f77538bcc58d61a4938120
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088379"
---
# <a name="file-library-replaces-document-folder"></a><span data-ttu-id="8ec41-103">La raccolta file sostituisce la cartella del documento</span><span class="sxs-lookup"><span data-stu-id="8ec41-103">File Library Replaces Document Folder</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="8ec41-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="8ec41-104">Affected Platforms</span></span>

<span data-ttu-id="8ec41-105">**Client** - Windows 7</span><span class="sxs-lookup"><span data-stu-id="8ec41-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="8ec41-106">**Server** - Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8ec41-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="8ec41-107">Impatto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="8ec41-107">Feature Impact</span></span>

<span data-ttu-id="8ec41-108">**Gravità** - Media</span><span class="sxs-lookup"><span data-stu-id="8ec41-108">**Severity** - Medium</span></span>  
<span data-ttu-id="8ec41-109">**Frequenza** - Alta</span><span class="sxs-lookup"><span data-stu-id="8ec41-109">**Frequency** - High</span></span>  











## <a name="description"></a><span data-ttu-id="8ec41-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ec41-110">Description</span></span>

<span data-ttu-id="8ec41-111">Le librerie offrono un'esperienza centralizzata simile a una cartella per l'archiviazione di file, la ricerca e l'accesso in più posizioni, sia locali che remote.</span><span class="sxs-lookup"><span data-stu-id="8ec41-111">Libraries provide a centralized folder-like experience for file storage, search, and access across multiple locations, both local and remote.</span></span>

<span data-ttu-id="8ec41-112">I percorsi predefiniti usati dalle finestre di dialogo comuni dei file, ad esempio Apri e Salva, sono stati modificati da Cartella documento a Raccolta documenti.</span><span class="sxs-lookup"><span data-stu-id="8ec41-112">The default locations used by common file dialogs (for example, Open, and Save) have been changed from the Document Folder to the Documents Library.</span></span> <span data-ttu-id="8ec41-113">Il Interfaccia utente è invariato, ma l'utente sarà ora in grado di visualizzare, esplorare ed eseguire ricerche nella libreria usando diverse visualizzazioni di disposizione.</span><span class="sxs-lookup"><span data-stu-id="8ec41-113">The User Interface is unchanged, but the user will now be able to view, browse, and search the Library using various arrangement views.</span></span> <span data-ttu-id="8ec41-114">I file verranno salvati nel percorso di salvataggio predefinito della libreria, a meno che l'utente non cambi il percorso di salvataggio predefinito o sceva una cartella diversa.</span><span class="sxs-lookup"><span data-stu-id="8ec41-114">Files will be saved into the Library default save location unless the user changes the default save location or chooses a different folder.</span></span>

<span data-ttu-id="8ec41-115">Gli sviluppatori possono creare librerie personalizzate o aggiungere percorsi alle librerie esistenti usando l'interfaccia IShellLibrary.</span><span class="sxs-lookup"><span data-stu-id="8ec41-115">Developers could create their own libraries or add locations to existing libraries using the IShellLibrary interface.</span></span> <span data-ttu-id="8ec41-116">Gli utenti possono trovare le librerie usando il sistema cartella nota (ad esempio, FOLDERID \_ DocumentsLibrary).</span><span class="sxs-lookup"><span data-stu-id="8ec41-116">Users can find libraries by using the Known Folder system (for example, FOLDERID\_DocumentsLibrary).</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="8ec41-117">Impatto significativo</span><span class="sxs-lookup"><span data-stu-id="8ec41-117">Manifestation of Impact</span></span>

<span data-ttu-id="8ec41-118">La libreria è di per sé un file e non una cartella.</span><span class="sxs-lookup"><span data-stu-id="8ec41-118">The Library is itself a file, and not a folder.</span></span> <span data-ttu-id="8ec41-119">Di conseguenza, le modifiche al percorso potrebbero causare errori a causa del tentativo da parte dell'applicazione di concatenare i file ai file.</span><span class="sxs-lookup"><span data-stu-id="8ec41-119">Therefore, path manipulations could result errors due to the attempt by the application to concatenate files to files.</span></span>

## <a name="solution"></a><span data-ttu-id="8ec41-120">Soluzione</span><span class="sxs-lookup"><span data-stu-id="8ec41-120">Solution</span></span>

<span data-ttu-id="8ec41-121">Quando si usa IFileDialog, è necessario usare il metodo GetResult anziché la combinazione di GetFolder e GetFilename come nelle versioni precedenti del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8ec41-121">When using IFileDialog, you must use GetResult method instead of combination of GetFolder and GetFilename as you would in the previous operating system versions.</span></span> <span data-ttu-id="8ec41-122">Usare le API shell laddove possibile per interagire con gli elementi nello spazio dei nomi della shell e modificarli, ad esempio IShellItem.</span><span class="sxs-lookup"><span data-stu-id="8ec41-122">Use the Shell APIs where possible to interact with and manipulate items in the Shell Namespace (for example, IShellItem).</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="8ec41-123">Sfruttare le funzionalità delle funzionalità</span><span class="sxs-lookup"><span data-stu-id="8ec41-123">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="8ec41-124">Se si vogliono creare librerie personalizzate o aggiungere percorsi a librerie esistenti, è necessario usare l'API IShellLibrary.</span><span class="sxs-lookup"><span data-stu-id="8ec41-124">If you want to create your own libraries or add locations to existing libraries, you must use IShellLibrary API.</span></span> <span data-ttu-id="8ec41-125">Le librerie sono a loro volta cartelle shell, quindi è possibile enumerarle esattamente come qualsiasi altra cartella shell.</span><span class="sxs-lookup"><span data-stu-id="8ec41-125">Libraries are themselves Shell Folders so you can enumerate them just like any other Shell Folder.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="8ec41-126">Test di compatibilità, prestazioni, affidabilità e usabilità</span><span class="sxs-lookup"><span data-stu-id="8ec41-126">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="8ec41-127">L'uso della finestra di dialogo file comune garantisce che gli utenti possano salvare direttamente nelle librerie.</span><span class="sxs-lookup"><span data-stu-id="8ec41-127">Using the common file dialog will ensure that users can save directly to their libraries.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="8ec41-128">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="8ec41-128">Links to Other Resources</span></span>

-   <span data-ttu-id="8ec41-129">**Librerie di Windows:**https://msdn.microsoft.com/library/dd758096(VS.85).aspx</span><span class="sxs-lookup"><span data-stu-id="8ec41-129">**Windows Libraries:** https://msdn.microsoft.com/library/dd758096(VS.85).aspx</span></span>
-   <span data-ttu-id="8ec41-130">**Mantenere la sincronizzazione con una libreria:**https://msdn.microsoft.com/library/dd758094(VS.85).aspx\#library\_keeping\_in\_sync</span><span class="sxs-lookup"><span data-stu-id="8ec41-130">**Keeping in sync with a library:** https://msdn.microsoft.com/library/dd758094(VS.85).aspx\#library\_keeping\_in\_sync</span></span>

 

 




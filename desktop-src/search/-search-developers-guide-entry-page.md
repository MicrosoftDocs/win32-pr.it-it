---
description: Le terze parti possono creare applicazioni che eseguono query sull'indice per i dati a livello di programmazione e possono estendere la ricerca di Windows per indicizzare i dati da formati di file personalizzati e archivi dati.
ms.assetid: 70046df0-ce48-472d-b24b-8231ea3a43c0
title: Guida per gli sviluppatori di Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61593f47e081059966936a99a7d2baea114df92a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484444"
---
# <a name="windows-search-developers-guide"></a><span data-ttu-id="3c072-103">Guida per gli sviluppatori di Windows Search</span><span class="sxs-lookup"><span data-stu-id="3c072-103">Windows Search Developer's Guide</span></span>

<span data-ttu-id="3c072-104">Le terze parti possono creare applicazioni che eseguono query sull'indice per i dati a livello di programmazione e possono estendere la ricerca di Windows per indicizzare i dati da formati di file personalizzati e archivi dati.</span><span class="sxs-lookup"><span data-stu-id="3c072-104">Third parties can create applications that query the index for data programmatically and can extend Windows Search to index data from custom file formats and data stores.</span></span> <span data-ttu-id="3c072-105">Per creare applicazioni Windows Search, gli sviluppatori di terze parti devono implementare prima di tutto un archivio dati Shell per ottenere un'esperienza utente ragionevole.</span><span class="sxs-lookup"><span data-stu-id="3c072-105">To create Windows Search applications, third-party developers must first implement a Shell data store to a achieve a reasonable user experience.</span></span> <span data-ttu-id="3c072-106">Per ulteriori informazioni, vedere [implementazione delle interfacce di oggetti della cartella di base](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3c072-106">For more information, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

<span data-ttu-id="3c072-107">È inoltre necessario scaricare il [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) per le librerie di ricerca di Windows.</span><span class="sxs-lookup"><span data-stu-id="3c072-107">You must also download the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) for the Windows Search libraries.</span></span> <span data-ttu-id="3c072-108">Gli [esempi di Windows Search SDK](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) contengono esempi di codice utili e un assembly di interoperabilità per lo sviluppo con codice gestito.</span><span class="sxs-lookup"><span data-stu-id="3c072-108">The [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) contains useful code samples and an interopability assembly for developing with managed code.</span></span> <span data-ttu-id="3c072-109">Per ulteriori informazioni sull'utilizzo degli esempi di codice, vedere [esempi di codice di Windows Search](-search-3x-wds-sampleentry.md).</span><span class="sxs-lookup"><span data-stu-id="3c072-109">For more information on using the code samples, see [Windows Search Code Samples](-search-3x-wds-sampleentry.md).</span></span>

<span data-ttu-id="3c072-110">Questa sezione è organizzata nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="3c072-110">This section is organized as follows:</span></span>

- [<span data-ttu-id="3c072-111">Gestione dell'indice</span><span class="sxs-lookup"><span data-stu-id="3c072-111">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)
- [<span data-ttu-id="3c072-112">Esecuzione di query sull'indice a livello di codice</span><span class="sxs-lookup"><span data-stu-id="3c072-112">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
- [<span data-ttu-id="3c072-113">Estensione dell'indice</span><span class="sxs-lookup"><span data-stu-id="3c072-113">Extending the Index</span></span>](-search-3x-wds-extidx-overview.md)
- [<span data-ttu-id="3c072-114">Estensione delle risorse della lingua</span><span class="sxs-lookup"><span data-stu-id="3c072-114">Extending Language Resources</span></span>](extending-language-resources-in-windows-search.md)

## <a name="additional-resources"></a><span data-ttu-id="3c072-115">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="3c072-115">Additional Resources</span></span>

- <span data-ttu-id="3c072-116">Per le bacheche dei messaggi di discussione e domande supportate dalla community sulle tecnologie di ricerca, vedere il [Forum MSDN relativo allo sviluppo per Windows Desktop Search](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).</span><span class="sxs-lookup"><span data-stu-id="3c072-116">For community-supported question and discussion message boards on Search technologies, see [MSDN Forum: Windows Desktop Search Development](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).</span></span>
- <span data-ttu-id="3c072-117">Per scaricare gli esempi di codice di ricerca:</span><span class="sxs-lookup"><span data-stu-id="3c072-117">To download the Search Code Samples:</span></span>
  - [<span data-ttu-id="3c072-118">Esempi di Windows Search</span><span class="sxs-lookup"><span data-stu-id="3c072-118">Windows Search Samples</span></span>](-search-samples-ovw.md)
- <span data-ttu-id="3c072-119">Per scaricare il Windows SDK:</span><span class="sxs-lookup"><span data-stu-id="3c072-119">To download the Windows SDK:</span></span>
  - <span data-ttu-id="3c072-120">Per Windows 10: [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)</span><span class="sxs-lookup"><span data-stu-id="3c072-120">For Windows 10: [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)</span></span>
  - <span data-ttu-id="3c072-121">Per Windows 7: [Windows SDK per Windows 7 e .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="3c072-121">For Windows 7: [Windows SDK for Windows 7 and .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c072-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3c072-122">Related topics</span></span>

[<span data-ttu-id="3c072-123">Panoramica di Windows Search</span><span class="sxs-lookup"><span data-stu-id="3c072-123">Windows Search Overview</span></span>](-search-3x-wds-overview.md)

[<span data-ttu-id="3c072-124">Informazioni di riferimento su Windows Search</span><span class="sxs-lookup"><span data-stu-id="3c072-124">Windows Search Reference</span></span>](-search-reference-entry-page.md)

[<span data-ttu-id="3c072-125">Esempi di codice di Windows Search</span><span class="sxs-lookup"><span data-stu-id="3c072-125">Windows Search Code Samples</span></span>](-search-samples-ovw.md)

[<span data-ttu-id="3c072-126">Ricerca federata in Windows</span><span class="sxs-lookup"><span data-stu-id="3c072-126">Federated Search in Windows</span></span>](-search-federated-search-overview.md)

[<span data-ttu-id="3c072-127">Tecnologie di ricerca correlate</span><span class="sxs-lookup"><span data-stu-id="3c072-127">Related Search Technologies</span></span>](-search-3x-wds-sampleentry.md)

[<span data-ttu-id="3c072-128">Glossario di Windows Search</span><span class="sxs-lookup"><span data-stu-id="3c072-128">Windows Search Glossary</span></span>](search-glossary.md)

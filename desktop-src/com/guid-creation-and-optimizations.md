---
title: Creazione e ottimizzazioni di GUID
description: Creazione e ottimizzazioni di GUID
ms.assetid: 698322f2-db89-4553-90c6-4278e96716dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc113675bae329d862c0b504851d4732243a84c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396778"
---
# <a name="guid-creation-and-optimizations"></a><span data-ttu-id="68aea-103">Creazione e ottimizzazioni di GUID</span><span class="sxs-lookup"><span data-stu-id="68aea-103">GUID Creation and Optimizations</span></span>

<span data-ttu-id="68aea-104">Poiché un CLSID, come un identificatore di interfaccia (IID), è un GUID, nessun'altra classe, indipendentemente da chi lo scrive, presenta un CLSID duplicato.</span><span class="sxs-lookup"><span data-stu-id="68aea-104">Because a CLSID, like an interface identifier (IID), is a GUID, no other class, no matter who writes it, has a duplicate CLSID.</span></span> <span data-ttu-id="68aea-105">Gli implementatori del server in genere ottengono CLSID tramite la funzione [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) .</span><span class="sxs-lookup"><span data-stu-id="68aea-105">Server implementers generally obtain CLSIDs through the [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) function.</span></span> <span data-ttu-id="68aea-106">Questa funzione garantisce la produzione di CLSID univoci, in modo che gli implementatori di server in tutto il mondo possano sviluppare e distribuire il software in modo indipendente senza temere conflitti accidentali con il software scritto da altri.</span><span class="sxs-lookup"><span data-stu-id="68aea-106">This function is guaranteed to produce unique CLSIDs, so server implementers across the world can independently develop and deploy their software without fear of accidental collision with software written by others.</span></span>

<span data-ttu-id="68aea-107">L'utilizzo di CLSID univoci consente di evitare la possibilità di conflitti di nomi tra le classi, perché i CLSID non sono in alcun modo connessi ai nomi utilizzati nell'implementazione sottostante.</span><span class="sxs-lookup"><span data-stu-id="68aea-107">Using unique CLSIDs avoids the possibility of name collisions among classes because CLSIDs are in no way connected to the names used in the underlying implementation.</span></span> <span data-ttu-id="68aea-108">Ad esempio, due fornitori diversi possono scrivere classi denominate "StackClass", ma ognuna avrà un CLSID univoco e pertanto non può essere confusa.</span><span class="sxs-lookup"><span data-stu-id="68aea-108">For example, two different vendors can write classes called "StackClass," but each would have a unique CLSID and therefore could not be confused.</span></span>

<span data-ttu-id="68aea-109">COM spesso deve eseguire il mapping dei GUID (IID e CLSID) a un set arbitrariamente grande di altri valori.</span><span class="sxs-lookup"><span data-stu-id="68aea-109">COM frequently must map GUIDs (IIDs and CLSIDs) to some arbitrarily large set of other values.</span></span> <span data-ttu-id="68aea-110">Gli sviluppatori di applicazioni possono velocizzare le ricerche e migliorare le prestazioni del sistema generando i GUID per l'applicazione come un blocco di valori consecutivi.</span><span class="sxs-lookup"><span data-stu-id="68aea-110">As an application developer, you can help speed up such searches, and thereby enhance system performance, by generating the GUIDs for your application as a block of consecutive values.</span></span>

<span data-ttu-id="68aea-111">Il modo più efficiente per generare un blocco di GUID consecutivi consiste nell'eseguire l'utilità uuidgen usando le opzioni-n e-x, che generano un blocco di UUID, ciascuno dei quali il primo valore DWORD viene incrementato di uno.</span><span class="sxs-lookup"><span data-stu-id="68aea-111">The most efficient way to generate a block of consecutive GUIDs is to run the uuidgen utility using the -n and -x switches, which generates a block of UUIDs, each of whose first DWORD value is incremented by one.</span></span>

<span data-ttu-id="68aea-112">Ad esempio, se si digita</span><span class="sxs-lookup"><span data-stu-id="68aea-112">For example, if you were to type</span></span>

<span data-ttu-id="68aea-113">**uuidgen-N5-x**</span><span class="sxs-lookup"><span data-stu-id="68aea-113">**uuidgen -n5 -x**</span></span>

<span data-ttu-id="68aea-114">l'utilità uuidgen genera un blocco di UUID analogo al seguente:</span><span class="sxs-lookup"><span data-stu-id="68aea-114">the uuidgen utility would generate a block of UUIDs similar to the following:</span></span>

``` syntax
12340001-4980-1920-6788-123456789012
12340002-4980-1920-6788-123456789012
12340003-4980-1920-6788-123456789012
12340004-4980-1920-6788-123456789012
12340005-4980-1920-6788-123456789012
 
```

<span data-ttu-id="68aea-115">Un metodo per generare e tenere traccia dei GUID per un intero progetto inizia con la generazione di un blocco di un numero arbitrariamente elevato di UUID, ad indicare 500.</span><span class="sxs-lookup"><span data-stu-id="68aea-115">One method for generating and tracking GUIDs for an entire project begins with generating a block of some arbitrarily large number of UUIDs, say 500.</span></span> <span data-ttu-id="68aea-116">Ad esempio, se si digita</span><span class="sxs-lookup"><span data-stu-id="68aea-116">For example, if you were to type</span></span>

<span data-ttu-id="68aea-117">**uuidgen-N500-x > guids.txt**</span><span class="sxs-lookup"><span data-stu-id="68aea-117">**uuidgen -n500 -x > guids.txt**</span></span>

<span data-ttu-id="68aea-118">l'utilità genera 500 UUID consecutivi e li scrive nel file di testo specificato.</span><span class="sxs-lookup"><span data-stu-id="68aea-118">the utility would generate 500 consecutive UUIDs and write them to the specified text file.</span></span> <span data-ttu-id="68aea-119">È quindi possibile controllare questo file nell'albero di origine, fornendo un unico repository per tutti i GUID da usare in un progetto.</span><span class="sxs-lookup"><span data-stu-id="68aea-119">You could then check this file into your source tree, providing a single repository for all GUIDs to be used in a project.</span></span> <span data-ttu-id="68aea-120">Poiché gli utenti necessitano di GUID per le parti del progetto, possono estrarre il file, usare tuttavia molti GUID necessari, contrassegnarli come presi e lasciare una nota sul punto in cui si trovano nel codice o "spec".</span><span class="sxs-lookup"><span data-stu-id="68aea-120">As people require GUIDs for their portions of the project, they can check out the file, take however many GUIDs they need, marking them as taken and leaving a note about where in the code or "spec" they are using them.</span></span>

<span data-ttu-id="68aea-121">Oltre a migliorare le prestazioni del sistema, la generazione di blocchi di GUID consecutivi in questo modo presenta i vantaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="68aea-121">In addition to improving system performance, generating blocks of consecutive GUIDs in this way has the following benefits:</span></span>

-   <span data-ttu-id="68aea-122">Un file centrale che contiene tutti i GUID di un'applicazione consente di tenere traccia di quali GUID sono relativi a cosa e quali utenti li usano.</span><span class="sxs-lookup"><span data-stu-id="68aea-122">A central file containing all GUIDs for an application makes it easy to keep track of which GUIDs are for what and which people are using them.</span></span>
-   <span data-ttu-id="68aea-123">Un blocco di GUID consecutivi associati a una particolare applicazione consente agli sviluppatori e ai tester di riconoscere i GUID interni durante il debug e di individuarli più facilmente nel registro di sistema perché vengono archiviati in modo sequenziale.</span><span class="sxs-lookup"><span data-stu-id="68aea-123">A block of consecutive GUIDs associated with a particular application helps developers and testers recognize internal GUIDs during debugging and makes it easier to find them in the system registry because they are stored sequentially.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68aea-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="68aea-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68aea-125">Responsabilità server COM</span><span class="sxs-lookup"><span data-stu-id="68aea-125">COM Server Responsibilities</span></span>](com-server-responsibilities.md)
</dt> </dl>

 

 





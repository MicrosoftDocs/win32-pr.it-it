---
title: Informazioni di riferimento per l'indicizzazione delle risorse dei pacchetti
description: Informazioni di riferimento per l'indicizzazione delle risorse dei pacchetti
ms.assetid: 15f41d83-d729-45e4-a6bb-5f8c6b78293c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef99acafe4fbdadef26c5947145ad734ec44b7bd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117549"
---
# <a name="package-resource-indexing-pri-reference"></a><span data-ttu-id="6872b-103">Informazioni di riferimento per l'indicizzazione delle risorse dei pacchetti</span><span class="sxs-lookup"><span data-stu-id="6872b-103">Package resource indexing (PRI) reference</span></span>

<span data-ttu-id="6872b-104">Set di API per l'uso di un indicizzatore di risorse.</span><span class="sxs-lookup"><span data-stu-id="6872b-104">A set of APIs for working with a resource indexer.</span></span> <span data-ttu-id="6872b-105">Un indicizzatore di risorse viene usato per generare file di indice delle risorse del pacchetto (PRI) per un'app UWP.</span><span class="sxs-lookup"><span data-stu-id="6872b-105">A resource indexer is used to generate package resource index (PRI) files for a UWP app.</span></span> <span data-ttu-id="6872b-106">Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere Api di indicizzazione delle risorse dei pacchetti [(PRI)](/windows/uwp/app-resources/pri-apis-custom-build-systems)e sistemi di compilazione personalizzati.</span><span class="sxs-lookup"><span data-stu-id="6872b-106">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6872b-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="6872b-107">In this section</span></span>

<span data-ttu-id="6872b-108">**Funzioni**</span><span class="sxs-lookup"><span data-stu-id="6872b-108">**Functions**</span></span>

-   <span data-ttu-id="6872b-109">[**Funzione MrmCreateConfig**](mrmcreateconfig.md)</span><span class="sxs-lookup"><span data-stu-id="6872b-109">[**MrmCreateConfig**](mrmcreateconfig.md) function</span></span>
-   <span data-ttu-id="6872b-110">[**Funzione MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md)</span><span class="sxs-lookup"><span data-stu-id="6872b-110">[**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md) function</span></span>
-   <span data-ttu-id="6872b-111">[**Funzione MrmCreateResourceFile**](mrmcreateresourcefile.md)</span><span class="sxs-lookup"><span data-stu-id="6872b-111">[**MrmCreateResourceFile**](mrmcreateresourcefile.md) function</span></span>
-   <span data-ttu-id="6872b-112">[**Funzione MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md)</span><span class="sxs-lookup"><span data-stu-id="6872b-112">[**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) function</span></span>
-   <span data-ttu-id="6872b-113">[**Funzione MrmCreateResourceIndexer**](mrmcreateresourceindexer.md)</span><span class="sxs-lookup"><span data-stu-id="6872b-113">[**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md) function</span></span>
-   <span data-ttu-id="6872b-114">[**Funzione MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md)</span><span class="sxs-lookup"><span data-stu-id="6872b-114">[**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md) function</span></span>
-   <span data-ttu-id="6872b-115">[**Funzione MrmCreateResourceIndexerFromPreviousPriFile**](mrmcreateresourceindexerfrompreviousprifile.md)</span><span class="sxs-lookup"><span data-stu-id="6872b-115">[**MrmCreateResourceIndexerFromPreviousPriFile**](mrmcreateresourceindexerfrompreviousprifile.md) function</span></span>
-   <span data-ttu-id="6872b-116">[**Funzione MrmCreateResourceIndexerFromPreviousSchemaData**](mrmcreateresourceindexerfrompreviousschemadata.md)</span><span class="sxs-lookup"><span data-stu-id="6872b-116">[**MrmCreateResourceIndexerFromPreviousSchemaData**](mrmcreateresourceindexerfrompreviousschemadata.md) function</span></span>
-   <span data-ttu-id="6872b-117">[**Funzione MrmCreateResourceIndexerFromPreviousSchemaFile**](mrmcreateresourceindexerfrompreviousschemafile.md)</span><span class="sxs-lookup"><span data-stu-id="6872b-117">[**MrmCreateResourceIndexerFromPreviousSchemaFile**](mrmcreateresourceindexerfrompreviousschemafile.md) function</span></span>
-   <span data-ttu-id="6872b-118">[**Funzione MrmDestroyIndexerAndMessages**](mrmdestroyindexerandmessages.md)</span><span class="sxs-lookup"><span data-stu-id="6872b-118">[**MrmDestroyIndexerAndMessages**](mrmdestroyindexerandmessages.md) function</span></span>
-   <span data-ttu-id="6872b-119">[**Funzione MrmDumpPriFile**](mrmdumpprifile.md)</span><span class="sxs-lookup"><span data-stu-id="6872b-119">[**MrmDumpPriFile**](mrmdumpprifile.md) function</span></span>
-   <span data-ttu-id="6872b-120">[**Funzione MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md)</span><span class="sxs-lookup"><span data-stu-id="6872b-120">[**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) function</span></span>
-   <span data-ttu-id="6872b-121">[**Funzione MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md)</span><span class="sxs-lookup"><span data-stu-id="6872b-121">[**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md) function</span></span>
-   <span data-ttu-id="6872b-122">[**Funzione MrmFreeMemory**](mrmfreememory.md)</span><span class="sxs-lookup"><span data-stu-id="6872b-122">[**MrmFreeMemory**](mrmfreememory.md) function</span></span>
-   <span data-ttu-id="6872b-123">[**Funzione MrmIndexEmbeddedData**](mrmindexembeddeddata.md)</span><span class="sxs-lookup"><span data-stu-id="6872b-123">[**MrmIndexEmbeddedData**](mrmindexembeddeddata.md) function</span></span>
-   <span data-ttu-id="6872b-124">[**Funzione MrmIndexFile**](mrmindexfile.md)</span><span class="sxs-lookup"><span data-stu-id="6872b-124">[**MrmIndexFile**](mrmindexfile.md) function</span></span>
-   <span data-ttu-id="6872b-125">[**Funzione MrmIndexFileAutoQualifiers**](mrmindexfileautoqualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="6872b-125">[**MrmIndexFileAutoQualifiers**](mrmindexfileautoqualifiers.md) function</span></span>
-   <span data-ttu-id="6872b-126">[**Funzione MrmIndexResourceContainerAutoQualifiers**](mrmindexresourcecontainerautoqualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="6872b-126">[**MrmIndexResourceContainerAutoQualifiers**](mrmindexresourcecontainerautoqualifiers.md) function</span></span>
-   <span data-ttu-id="6872b-127">[**Funzione MrmIndexString**](mrmindexstring.md)</span><span class="sxs-lookup"><span data-stu-id="6872b-127">[**MrmIndexString**](mrmindexstring.md) function</span></span>
-   <span data-ttu-id="6872b-128">[**Funzione MrmPeekResourceIndexerMessages**](mrmpeekresourceindexermessages.md)</span><span class="sxs-lookup"><span data-stu-id="6872b-128">[**MrmPeekResourceIndexerMessages**](mrmpeekresourceindexermessages.md) function</span></span>

<span data-ttu-id="6872b-129">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="6872b-129">**Structures**</span></span>

-   <span data-ttu-id="6872b-130">[**Struttura MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)</span><span class="sxs-lookup"><span data-stu-id="6872b-130">[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) structure</span></span>
-   <span data-ttu-id="6872b-131">[**Struttura MrmResourceIndexerMessage**](mrmresourceindexermessage.md)</span><span class="sxs-lookup"><span data-stu-id="6872b-131">[**MrmResourceIndexerMessage**](mrmresourceindexermessage.md) structure</span></span>

<span data-ttu-id="6872b-132">**Enumerazioni**</span><span class="sxs-lookup"><span data-stu-id="6872b-132">**Enumerations**</span></span>

-   <span data-ttu-id="6872b-133">[**Enumerazione MrmDumpType**](mrmdumptype.md)</span><span class="sxs-lookup"><span data-stu-id="6872b-133">[**MrmDumpType**](mrmdumptype.md) enumeration</span></span>
-   <span data-ttu-id="6872b-134">[**Enumerazione MrmPackagingMode**](mrmpackagingmode.md)</span><span class="sxs-lookup"><span data-stu-id="6872b-134">[**MrmPackagingMode**](mrmpackagingmode.md) enumeration</span></span>
-   <span data-ttu-id="6872b-135">[**Enumerazione MrmPackagingOptions**](mrmpackagingoptions.md)</span><span class="sxs-lookup"><span data-stu-id="6872b-135">[**MrmPackagingOptions**](mrmpackagingoptions.md) enumeration</span></span>
-   <span data-ttu-id="6872b-136">[**Enumerazione MrmPlatformVersion**](mrmplatformversion.md)</span><span class="sxs-lookup"><span data-stu-id="6872b-136">[**MrmPlatformVersion**](mrmplatformversion.md) enumeration</span></span>
-   <span data-ttu-id="6872b-137">[**Enumerazione MrmResourceIndexerMessageSeverity**](mrmresourceindexermessageseverity.md)</span><span class="sxs-lookup"><span data-stu-id="6872b-137">[**MrmResourceIndexerMessageSeverity**](mrmresourceindexermessageseverity.md) enumeration</span></span>

 

 

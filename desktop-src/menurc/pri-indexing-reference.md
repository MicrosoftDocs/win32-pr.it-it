---
title: Guida di riferimento all'indicizzazione delle risorse del pacchetto (PRI)
description: .
ms.assetid: 15f41d83-d729-45e4-a6bb-5f8c6b78293c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b75c0739b4e7673863a21223fbed749c27e65dc4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963085"
---
# <a name="package-resource-indexing-pri-reference"></a><span data-ttu-id="61f14-103">Guida di riferimento all'indicizzazione delle risorse del pacchetto (PRI)</span><span class="sxs-lookup"><span data-stu-id="61f14-103">Package resource indexing (PRI) reference</span></span>

<span data-ttu-id="61f14-104">Set di API per l'utilizzo di un indicizzatore di risorse.</span><span class="sxs-lookup"><span data-stu-id="61f14-104">A set of APIs for working with a resource indexer.</span></span> <span data-ttu-id="61f14-105">Un indicizzatore di risorse viene usato per generare file di indice delle risorse del pacchetto (PRI) per un'app UWP.</span><span class="sxs-lookup"><span data-stu-id="61f14-105">A resource indexer is used to generate package resource index (PRI) files for a UWP app.</span></span> <span data-ttu-id="61f14-106">Per altre informazioni e procedure dettagliate basate su scenari su come usare queste API, vedere [API pri (Package Resource Indexing) e sistemi di compilazione personalizzati](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="61f14-106">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="61f14-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="61f14-107">In this section</span></span>

<span data-ttu-id="61f14-108">**Funzioni**</span><span class="sxs-lookup"><span data-stu-id="61f14-108">**Functions**</span></span>

-   <span data-ttu-id="61f14-109">[**MrmCreateConfig**](mrmcreateconfig.md) (funzione)</span><span class="sxs-lookup"><span data-stu-id="61f14-109">[**MrmCreateConfig**](mrmcreateconfig.md) function</span></span>
-   <span data-ttu-id="61f14-110">[**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md) (funzione)</span><span class="sxs-lookup"><span data-stu-id="61f14-110">[**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md) function</span></span>
-   <span data-ttu-id="61f14-111">[**MrmCreateResourceFile**](mrmcreateresourcefile.md) (funzione)</span><span class="sxs-lookup"><span data-stu-id="61f14-111">[**MrmCreateResourceFile**](mrmcreateresourcefile.md) function</span></span>
-   <span data-ttu-id="61f14-112">[**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (funzione)</span><span class="sxs-lookup"><span data-stu-id="61f14-112">[**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) function</span></span>
-   <span data-ttu-id="61f14-113">[**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md) (funzione)</span><span class="sxs-lookup"><span data-stu-id="61f14-113">[**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md) function</span></span>
-   <span data-ttu-id="61f14-114">[**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md) (funzione)</span><span class="sxs-lookup"><span data-stu-id="61f14-114">[**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md) function</span></span>
-   <span data-ttu-id="61f14-115">[**MrmCreateResourceIndexerFromPreviousPriFile**](mrmcreateresourceindexerfrompreviousprifile.md) (funzione)</span><span class="sxs-lookup"><span data-stu-id="61f14-115">[**MrmCreateResourceIndexerFromPreviousPriFile**](mrmcreateresourceindexerfrompreviousprifile.md) function</span></span>
-   <span data-ttu-id="61f14-116">[**MrmCreateResourceIndexerFromPreviousSchemaData**](mrmcreateresourceindexerfrompreviousschemadata.md) (funzione)</span><span class="sxs-lookup"><span data-stu-id="61f14-116">[**MrmCreateResourceIndexerFromPreviousSchemaData**](mrmcreateresourceindexerfrompreviousschemadata.md) function</span></span>
-   <span data-ttu-id="61f14-117">[**MrmCreateResourceIndexerFromPreviousSchemaFile**](mrmcreateresourceindexerfrompreviousschemafile.md) (funzione)</span><span class="sxs-lookup"><span data-stu-id="61f14-117">[**MrmCreateResourceIndexerFromPreviousSchemaFile**](mrmcreateresourceindexerfrompreviousschemafile.md) function</span></span>
-   <span data-ttu-id="61f14-118">[**MrmDestroyIndexerAndMessages**](mrmdestroyindexerandmessages.md) (funzione)</span><span class="sxs-lookup"><span data-stu-id="61f14-118">[**MrmDestroyIndexerAndMessages**](mrmdestroyindexerandmessages.md) function</span></span>
-   <span data-ttu-id="61f14-119">[**MrmDumpPriFile**](mrmdumpprifile.md) (funzione)</span><span class="sxs-lookup"><span data-stu-id="61f14-119">[**MrmDumpPriFile**](mrmdumpprifile.md) function</span></span>
-   <span data-ttu-id="61f14-120">[**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) (funzione)</span><span class="sxs-lookup"><span data-stu-id="61f14-120">[**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) function</span></span>
-   <span data-ttu-id="61f14-121">[**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md) (funzione)</span><span class="sxs-lookup"><span data-stu-id="61f14-121">[**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md) function</span></span>
-   <span data-ttu-id="61f14-122">[**MrmFreeMemory**](mrmfreememory.md) (funzione)</span><span class="sxs-lookup"><span data-stu-id="61f14-122">[**MrmFreeMemory**](mrmfreememory.md) function</span></span>
-   <span data-ttu-id="61f14-123">[**MrmIndexEmbeddedData**](mrmindexembeddeddata.md) (funzione)</span><span class="sxs-lookup"><span data-stu-id="61f14-123">[**MrmIndexEmbeddedData**](mrmindexembeddeddata.md) function</span></span>
-   <span data-ttu-id="61f14-124">[**MrmIndexFile**](mrmindexfile.md) (funzione)</span><span class="sxs-lookup"><span data-stu-id="61f14-124">[**MrmIndexFile**](mrmindexfile.md) function</span></span>
-   <span data-ttu-id="61f14-125">[**MrmIndexFileAutoQualifiers**](mrmindexfileautoqualifiers.md) (funzione)</span><span class="sxs-lookup"><span data-stu-id="61f14-125">[**MrmIndexFileAutoQualifiers**](mrmindexfileautoqualifiers.md) function</span></span>
-   <span data-ttu-id="61f14-126">[**MrmIndexResourceContainerAutoQualifiers**](mrmindexresourcecontainerautoqualifiers.md) (funzione)</span><span class="sxs-lookup"><span data-stu-id="61f14-126">[**MrmIndexResourceContainerAutoQualifiers**](mrmindexresourcecontainerautoqualifiers.md) function</span></span>
-   <span data-ttu-id="61f14-127">[**MrmIndexString**](mrmindexstring.md) (funzione)</span><span class="sxs-lookup"><span data-stu-id="61f14-127">[**MrmIndexString**](mrmindexstring.md) function</span></span>
-   <span data-ttu-id="61f14-128">[**MrmPeekResourceIndexerMessages**](mrmpeekresourceindexermessages.md) (funzione)</span><span class="sxs-lookup"><span data-stu-id="61f14-128">[**MrmPeekResourceIndexerMessages**](mrmpeekresourceindexermessages.md) function</span></span>

<span data-ttu-id="61f14-129">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="61f14-129">**Structures**</span></span>

-   <span data-ttu-id="61f14-130">Struttura [**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)</span><span class="sxs-lookup"><span data-stu-id="61f14-130">[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) structure</span></span>
-   <span data-ttu-id="61f14-131">Struttura [**MrmResourceIndexerMessage**](mrmresourceindexermessage.md)</span><span class="sxs-lookup"><span data-stu-id="61f14-131">[**MrmResourceIndexerMessage**](mrmresourceindexermessage.md) structure</span></span>

<span data-ttu-id="61f14-132">**Enumerazioni**</span><span class="sxs-lookup"><span data-stu-id="61f14-132">**Enumerations**</span></span>

-   <span data-ttu-id="61f14-133">Enumerazione [**MrmDumpType**](mrmdumptype.md)</span><span class="sxs-lookup"><span data-stu-id="61f14-133">[**MrmDumpType**](mrmdumptype.md) enumeration</span></span>
-   <span data-ttu-id="61f14-134">Enumerazione [**MrmPackagingMode**](mrmpackagingmode.md)</span><span class="sxs-lookup"><span data-stu-id="61f14-134">[**MrmPackagingMode**](mrmpackagingmode.md) enumeration</span></span>
-   <span data-ttu-id="61f14-135">Enumerazione [**MrmPackagingOptions**](mrmpackagingoptions.md)</span><span class="sxs-lookup"><span data-stu-id="61f14-135">[**MrmPackagingOptions**](mrmpackagingoptions.md) enumeration</span></span>
-   <span data-ttu-id="61f14-136">Enumerazione [**MrmPlatformVersion**](mrmplatformversion.md)</span><span class="sxs-lookup"><span data-stu-id="61f14-136">[**MrmPlatformVersion**](mrmplatformversion.md) enumeration</span></span>
-   <span data-ttu-id="61f14-137">Enumerazione [**MrmResourceIndexerMessageSeverity**](mrmresourceindexermessageseverity.md)</span><span class="sxs-lookup"><span data-stu-id="61f14-137">[**MrmResourceIndexerMessageSeverity**](mrmresourceindexermessageseverity.md) enumeration</span></span>

 

 
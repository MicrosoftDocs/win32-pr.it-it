---
description: L'API Filtro cloud offre funzionalità al limite tra la modalità utente e la file system.
ms.assetid: 72bc3e80-babd-4a39-842c-38afe4773a5e
title: Motori di sincronizzazione cloud
ms.topic: article
ms.date: 02/06/2019
ms.custom: project-verbatim
ms.openlocfilehash: d40b195a442859441138ae4e61cb0eb946411623
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549596"
---
# <a name="cloud-sync-engines"></a><span data-ttu-id="72ae8-103">Motori di sincronizzazione cloud</span><span class="sxs-lookup"><span data-stu-id="72ae8-103">Cloud Sync Engines</span></span>

<span data-ttu-id="72ae8-104">Vedere anche [l'esempio cloud mirror](./build-a-cloud-file-sync-engine.md#cloud-mirror-sample).</span><span class="sxs-lookup"><span data-stu-id="72ae8-104">Also see [Cloud Mirror sample](./build-a-cloud-file-sync-engine.md#cloud-mirror-sample).</span></span>

<span data-ttu-id="72ae8-105">A partire da Windows 10 versione 1709, Windows fornisce *l'API dei file cloud*.</span><span class="sxs-lookup"><span data-stu-id="72ae8-105">Starting in Windows 10, version 1709, Windows provides the *cloud files API*.</span></span> <span data-ttu-id="72ae8-106">Questa API è costituita da diverse API Win32 e WinRT native che formalizzano il supporto per i motori di sincronizzazione cloud e gestiscono attività quali la creazione e la gestione di file segnaposto e directory.</span><span class="sxs-lookup"><span data-stu-id="72ae8-106">This API consists of several native Win32 and WinRT APIs that formalize support for cloud sync engines, and handles tasks such as creating and managing placeholder files and directories.</span></span> <span data-ttu-id="72ae8-107">Gli utenti di questa API sono in genere provider di sincronizzazione e, in una certa misura, applicazioni Windows.</span><span class="sxs-lookup"><span data-stu-id="72ae8-107">Users of this API are typically sync providers and to some extent, Windows applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="72ae8-108">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="72ae8-108">In this section</span></span>

| <span data-ttu-id="72ae8-109">Argomento</span><span class="sxs-lookup"><span data-stu-id="72ae8-109">Topic</span></span>                                                                | <span data-ttu-id="72ae8-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72ae8-110">Description</span></span>                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72ae8-111">Creare un motore di sincronizzazione cloud che supporti i file segnaposto</span><span class="sxs-lookup"><span data-stu-id="72ae8-111">Build a Cloud Sync Engine that Supports Placeholder Files</span></span>](build-a-cloud-file-sync-engine.md)<br/> | <span data-ttu-id="72ae8-112">Informazioni su come usare l'API file cloud per creare un motore di sincronizzazione file cloud che include file segnaposto e Esplora file integrazione.</span><span class="sxs-lookup"><span data-stu-id="72ae8-112">Learn how to use the cloud files API to build a cloud file sync engine that includes placeholder files and File Explorer integration.</span></span> <br/> |
| [<span data-ttu-id="72ae8-113">Informazioni di riferimento sul filtro cloud</span><span class="sxs-lookup"><span data-stu-id="72ae8-113">Cloud Filter Reference</span></span>](cloud-filter-reference.md)<br/> | <span data-ttu-id="72ae8-114">L'API di filtro cloud è un'API Win32 nativa che fa parte dell'API di file cloud più ampia.</span><span class="sxs-lookup"><span data-stu-id="72ae8-114">The cloud filter API is a native Win32 API that is part of the broader cloud files API.</span></span> <span data-ttu-id="72ae8-115">L'API filtro cloud fornisce funzionalità al limite tra la modalità utente e l'file system.</span><span class="sxs-lookup"><span data-stu-id="72ae8-115">The cloud filter API provides functionality at the boundary between the user mode and the file system.</span></span> <span data-ttu-id="72ae8-116">Questa API gestisce la creazione e la gestione di file segnaposto e directory.</span><span class="sxs-lookup"><span data-stu-id="72ae8-116">This API handles the creation and management of placeholder files and directories.</span></span> <br/> |
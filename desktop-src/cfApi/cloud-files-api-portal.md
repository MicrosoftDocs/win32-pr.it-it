---
description: L'API di filtro cloud fornisce funzionalità al limite tra la modalità utente e la file system.
ms.assetid: 72bc3e80-babd-4a39-842c-38afe4773a5e
title: Motori di sincronizzazione cloud
ms.topic: article
ms.date: 02/06/2019
ms.custom: project-verbatim
ms.openlocfilehash: debe32a1849a393a067017f90f5405c4b3ba77d1
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/20/2021
ms.locfileid: "106323891"
---
# <a name="cloud-sync-engines"></a><span data-ttu-id="15e76-103">Motori di sincronizzazione cloud</span><span class="sxs-lookup"><span data-stu-id="15e76-103">Cloud Sync Engines</span></span>

<span data-ttu-id="15e76-104">Vedere anche [esempio di mirroring cloud](/windows/win32/cfapi/build-a-cloud-file-sync-engine#cloud-mirror-sample).</span><span class="sxs-lookup"><span data-stu-id="15e76-104">Also see [Cloud Mirror sample](/windows/win32/cfapi/build-a-cloud-file-sync-engine#cloud-mirror-sample).</span></span>

<span data-ttu-id="15e76-105">A partire da Windows 10, versione 1709, Windows fornisce l' *API per i file Cloud*.</span><span class="sxs-lookup"><span data-stu-id="15e76-105">Starting in Windows 10, version 1709, Windows provides the *cloud files API*.</span></span> <span data-ttu-id="15e76-106">Questa API è costituita da diverse API Win32 e WinRT native che formalizzano il supporto per i motori di sincronizzazione cloud e gestisce attività quali la creazione e la gestione di file e directory segnaposto.</span><span class="sxs-lookup"><span data-stu-id="15e76-106">This API consists of several native Win32 and WinRT APIs that formalize support for cloud sync engines, and handles tasks such as creating and managing placeholder files and directories.</span></span> <span data-ttu-id="15e76-107">Gli utenti di questa API sono in genere provider di sincronizzazione e in qualche misura le applicazioni Windows.</span><span class="sxs-lookup"><span data-stu-id="15e76-107">Users of this API are typically sync providers and to some extent, Windows applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="15e76-108">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="15e76-108">In this section</span></span>

| <span data-ttu-id="15e76-109">Argomento</span><span class="sxs-lookup"><span data-stu-id="15e76-109">Topic</span></span>                                                                | <span data-ttu-id="15e76-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15e76-110">Description</span></span>                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15e76-111">Creare un motore di sincronizzazione cloud che supporti i file segnaposto</span><span class="sxs-lookup"><span data-stu-id="15e76-111">Build a Cloud Sync Engine that Supports Placeholder Files</span></span>](build-a-cloud-file-sync-engine.md)<br/> | <span data-ttu-id="15e76-112">Informazioni su come usare l'API file cloud per compilare un motore di sincronizzazione file cloud che include file segnaposto e integrazione con Esplora file.</span><span class="sxs-lookup"><span data-stu-id="15e76-112">Learn how to use the cloud files API to build a cloud file sync engine that includes placeholder files and File Explorer integration.</span></span> <br/> |
| [<span data-ttu-id="15e76-113">Riferimento al filtro cloud</span><span class="sxs-lookup"><span data-stu-id="15e76-113">Cloud Filter Reference</span></span>](cloud-filter-reference.md)<br/> | <span data-ttu-id="15e76-114">L'API di filtro cloud è un'API Win32 nativa che fa parte dell'API file cloud più ampia.</span><span class="sxs-lookup"><span data-stu-id="15e76-114">The cloud filter API is a native Win32 API that is part of the broader cloud files API.</span></span> <span data-ttu-id="15e76-115">L'API di filtro cloud fornisce funzionalità al limite tra la modalità utente e la file system.</span><span class="sxs-lookup"><span data-stu-id="15e76-115">The cloud filter API provides functionality at the boundary between the user mode and the file system.</span></span> <span data-ttu-id="15e76-116">Questa API gestisce la creazione e la gestione di file e directory segnaposto.</span><span class="sxs-lookup"><span data-stu-id="15e76-116">This API handles the creation and management of placeholder files and directories.</span></span> <br/> |


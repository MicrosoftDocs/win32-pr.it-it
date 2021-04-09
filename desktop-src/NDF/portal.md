---
title: Framework di diagnostica di rete
description: Il Framework di diagnostica di rete (NDF) fornisce agli sviluppatori di componenti e applicazioni un modo per semplificare la risoluzione dei problemi di rete per gli utenti.
ms.assetid: 61dfb66b-4bc6-43a9-ad61-698f5cd67f4a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0342ee4cb285f0a0f1c76c74b3bdc5b412b07e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044421"
---
# <a name="network-diagnostics-framework"></a><span data-ttu-id="3a1dd-103">Framework di diagnostica di rete</span><span class="sxs-lookup"><span data-stu-id="3a1dd-103">Network Diagnostics Framework</span></span>

## <a name="purpose"></a><span data-ttu-id="3a1dd-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="3a1dd-104">Purpose</span></span>

<span data-ttu-id="3a1dd-105">Il Framework di diagnostica di rete (NDF) fornisce agli sviluppatori di componenti e applicazioni un modo per semplificare la risoluzione dei problemi di rete per gli utenti.</span><span class="sxs-lookup"><span data-stu-id="3a1dd-105">The Network Diagnostics Framework (NDF) provides a way for component and application developers to simplify network troubleshooting for users.</span></span> <span data-ttu-id="3a1dd-106">Gli utenti possono tentare di diagnosticare e risolvere un problema di rete usando un unico strumento per la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="3a1dd-106">Users can attempt to diagnose and repair a network problem using a single troubleshooting tool.</span></span>

<span data-ttu-id="3a1dd-107">Microsoft fornisce le classi helper NDF, alcune delle quali sono estendibili, in modo che gli sviluppatori possano creare unità di risoluzione dei problemi denominate estensioni della classe helper per fornire diagnosi più dettagliate specifiche di particolari componenti software o hardware.</span><span class="sxs-lookup"><span data-stu-id="3a1dd-107">Microsoft provides NDF helper classes, some of which are extensible so that developers can create troubleshooting units called helper class extensions to provide more detailed diagnoses specific to particular software or hardware components.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="3a1dd-108">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="3a1dd-108">Where applicable</span></span>

<span data-ttu-id="3a1dd-109">NDF può essere usato dal software di qualsiasi fornitore che si basa sulla connettività di rete.</span><span class="sxs-lookup"><span data-stu-id="3a1dd-109">NDF can be used by any vendor's software which relies on network connectivity.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="3a1dd-110">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="3a1dd-110">Developer audience</span></span>

<span data-ttu-id="3a1dd-111">L'API NDF è progettata per gli sviluppatori C/C++.</span><span class="sxs-lookup"><span data-stu-id="3a1dd-111">The NDF API is designed for C/C++ developers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="3a1dd-112">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="3a1dd-112">Run-time requirements</span></span>

<span data-ttu-id="3a1dd-113">NDF è disponibile per i computer che eseguono Windows Vista, Windows Server 2008 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="3a1dd-113">NDF is available for computers running Windows Vista, Windows Server 2008, or later.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3a1dd-114">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="3a1dd-114">In this section</span></span>



| <span data-ttu-id="3a1dd-115">Argomento</span><span class="sxs-lookup"><span data-stu-id="3a1dd-115">Topic</span></span>                                                                       | <span data-ttu-id="3a1dd-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a1dd-116">Description</span></span>                                                                                                                                                                                              |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a1dd-117">Informazioni su NDF</span><span class="sxs-lookup"><span data-stu-id="3a1dd-117">About NDF</span></span>](about-ndf.md)<br/>                                       | <span data-ttu-id="3a1dd-118">Fornisce un riepilogo generale della tecnologia NDF.</span><span class="sxs-lookup"><span data-stu-id="3a1dd-118">Provides a general summary of the NDF technology.</span></span><br/>                                                                                                                                             |
| [<span data-ttu-id="3a1dd-119">Uso di NDF</span><span class="sxs-lookup"><span data-stu-id="3a1dd-119">Using NDF</span></span>](using-ndf.md)<br/>                                       | <span data-ttu-id="3a1dd-120">Vengono fornite informazioni ed esempi sull'utilizzo della funzionalità NDF, oltre a informazioni su come estendere questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="3a1dd-120">Provides information and examples on using NDF functionality, as well as how to extend this functionality.</span></span><br/>                                                                                    |
| [<span data-ttu-id="3a1dd-121">Riferimento a NDF</span><span class="sxs-lookup"><span data-stu-id="3a1dd-121">NDF Reference</span></span>](ndf-reference.md)<br/>                               | <span data-ttu-id="3a1dd-122">Vengono fornite informazioni sulle enumerazioni, le funzioni, le interfacce e le strutture che supportano l'utilizzo di NDF, oltre a informazioni sulle classi helper estendibili fornite da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3a1dd-122">Provides information about enumerations, functions, interfaces, and structures that support the use of NDF, as well as information about the extensible helper classes provided by Microsoft.</span></span><br/> |
| [<span data-ttu-id="3a1dd-123">Traccia di rete in Windows 7</span><span class="sxs-lookup"><span data-stu-id="3a1dd-123">Network Tracing in Windows 7</span></span>](network-tracing-in-windows-7.md)<br/> | <span data-ttu-id="3a1dd-124">Vengono illustrati gli strumenti e la traccia di rete da utilizzare per la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="3a1dd-124">Discusses network tracing and tools to use for troubleshooting.</span></span><br/>                                                                                                                               |



 

 

 






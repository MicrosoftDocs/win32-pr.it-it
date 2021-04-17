---
description: API video Direct3D 9
ms.assetid: 2f5f46a0-f21f-4e57-9297-bad2b791da52
title: API video Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7346741b5e78f052b7c895ca417735614930d35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524554"
---
# <a name="direct3d-9-video-apis"></a><span data-ttu-id="ec0c5-103">API video Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="ec0c5-103">Direct3D 9 Video APIs</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ec0c5-104">Le app di Windows Store devono usare Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="ec0c5-104">Windows Store apps must use Microsoft Direct3D 11.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="ec0c5-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="ec0c5-105">In this section</span></span>



| <span data-ttu-id="ec0c5-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="ec0c5-106">Topic</span></span>                                                                       | <span data-ttu-id="ec0c5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec0c5-107">Description</span></span>                                                                                                                                 |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ec0c5-108">protezione del contenuto basate su GPU</span><span class="sxs-lookup"><span data-stu-id="ec0c5-108">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)<br/> | <span data-ttu-id="ec0c5-109">Descrive il contenuto video: funzionalità di protezione che possono essere fornite da un driver di grafica.</span><span class="sxs-lookup"><span data-stu-id="ec0c5-109">Describes video content–protection capabilities that a graphics driver can provide.</span></span><br/>                                              |
| [<span data-ttu-id="ec0c5-110">Supporto per overlay hardware</span><span class="sxs-lookup"><span data-stu-id="ec0c5-110">Hardware Overlay Support</span></span>](hardware-overlay-support.md)<br/>         | <span data-ttu-id="ec0c5-111">Viene descritto come utilizzare le sovrapposizioni hardware in Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="ec0c5-111">Describes how to use hardware overlays in Direct3D 9.</span></span><br/>                                                                            |
| [<span data-ttu-id="ec0c5-112">Segnalazione di utilizzo intensivo della memoria</span><span class="sxs-lookup"><span data-stu-id="ec0c5-112">Memory Pressure Reporting</span></span>](memory-pressure-reporting.md)<br/>       | <span data-ttu-id="ec0c5-113">La funzionalità di creazione di report con utilizzo intensivo della memoria consente a un'applicazione Direct3D di determinare quando il working set di memoria video è troppo grande.</span><span class="sxs-lookup"><span data-stu-id="ec0c5-113">Memory pressure reporting enables a Direct3D application to determine when its video-memory working set has grown too large.</span></span><br/>     |
| [<span data-ttu-id="ec0c5-114">Interfacce video Direct3D</span><span class="sxs-lookup"><span data-stu-id="ec0c5-114">Direct3D Video Interfaces</span></span>](direct3d-video-interfaces.md)<br/>       | <span data-ttu-id="ec0c5-115">Descrive le interfacce video Microsoft Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="ec0c5-115">Describes the Microsoft Direct3D 9 video interfaces.</span></span><br/>                                                                             |
| [<span data-ttu-id="ec0c5-116">Strutture video Direct3D</span><span class="sxs-lookup"><span data-stu-id="ec0c5-116">Direct3D Video Structures</span></span>](direct3d-video-structures.md)<br/>       | <span data-ttu-id="ec0c5-117">Descrive le strutture utilizzate dalle interfacce video Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="ec0c5-117">Describes the structures used by the Direct3D 9 video interfaces.</span></span><br/>                                                                |
| [<span data-ttu-id="ec0c5-118">Enumerazioni video Direct3D</span><span class="sxs-lookup"><span data-stu-id="ec0c5-118">Direct3D Video Enumerations</span></span>](direct3d-video-enumerations.md)<br/>   | <span data-ttu-id="ec0c5-119">Descrive le enumerazioni utilizzate dalle interfacce video Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="ec0c5-119">Describes the enumerations used by the Direct3D 9 video interfaces.</span></span><br/>                                                              |
| [<span data-ttu-id="ec0c5-120">Comandi protezione del contenuto</span><span class="sxs-lookup"><span data-stu-id="ec0c5-120">Content Protection Commands</span></span>](content-protection-commands.md)<br/>   | <span data-ttu-id="ec0c5-121">Elenca i comandi per il metodo [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) .</span><span class="sxs-lookup"><span data-stu-id="ec0c5-121">Lists the commands for the [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) method.</span></span><br/> |
| [<span data-ttu-id="ec0c5-122">Query di protezione del contenuto</span><span class="sxs-lookup"><span data-stu-id="ec0c5-122">Content Protection Queries</span></span>](content-protection-queries.md)<br/>     | <span data-ttu-id="ec0c5-123">Elenca le query per il metodo [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .</span><span class="sxs-lookup"><span data-stu-id="ec0c5-123">Lists the queries for the [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) method.</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="ec0c5-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ec0c5-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec0c5-125">Guida alla programmazione di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ec0c5-125">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 





---
title: MultiThreading
description: Direct3D 11 implementa il supporto per la creazione e il rendering di oggetti usando più thread.
ms.assetid: 1bf50927-268b-4471-b059-819adf2189a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4de7ca3e7e00ffba0c728aef334f21efc18899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221749"
---
# <a name="multithreading"></a><span data-ttu-id="69320-103">MultiThreading</span><span class="sxs-lookup"><span data-stu-id="69320-103">MultiThreading</span></span>

<span data-ttu-id="69320-104">Direct3D 11 implementa il supporto per la creazione e il rendering di oggetti usando più thread.</span><span class="sxs-lookup"><span data-stu-id="69320-104">Direct3D 11 implements support for object creation and rendering using multiple threads.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="69320-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="69320-105">In this section</span></span>



| <span data-ttu-id="69320-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="69320-106">Topic</span></span>                                                                                                                   | <span data-ttu-id="69320-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69320-107">Description</span></span>                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69320-108">Introduzione al multithreading in Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="69320-108">Introduction to Multithreading in Direct3D 11</span></span>](overviews-direct3d-11-render-multi-thread-intro.md)<br/>         | <span data-ttu-id="69320-109">Il multithreading è progettato per migliorare le prestazioni eseguendo il lavoro utilizzando uno o più thread contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="69320-109">Multithreading is designed to improve performance by performing work using one or more threads at the same time.</span></span> <br/>                                                                                                         |
| [<span data-ttu-id="69320-110">Creazione di oggetti con multithreading</span><span class="sxs-lookup"><span data-stu-id="69320-110">Object Creation with Multithreading</span></span>](overviews-direct3d-11-render-multi-thread-create.md)<br/>                  | <span data-ttu-id="69320-111">Utilizzare l'interfaccia [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) per creare risorse e oggetti, utilizzare [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) per il [rendering](overviews-direct3d-11-render-multi-thread-render.md).</span><span class="sxs-lookup"><span data-stu-id="69320-111">Use the [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface to create resources and objects, use the [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) for [rendering](overviews-direct3d-11-render-multi-thread-render.md).</span></span><br/> |
| [<span data-ttu-id="69320-112">Rendering immediato e posticipato</span><span class="sxs-lookup"><span data-stu-id="69320-112">Immediate and Deferred Rendering</span></span>](overviews-direct3d-11-render-multi-thread-render.md)<br/>                     | <span data-ttu-id="69320-113">Direct3D 11 supporta due tipi di rendering: immediato e posticipato.</span><span class="sxs-lookup"><span data-stu-id="69320-113">Direct3D 11 supports two types of rendering: immediate and deferred.</span></span> <span data-ttu-id="69320-114">Entrambe le implementazioni sono implementate tramite l'interfaccia [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="69320-114">Both are implemented by using the [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) interface.</span></span><br/>                                                      |
| [<span data-ttu-id="69320-115">Elenco comandi</span><span class="sxs-lookup"><span data-stu-id="69320-115">Command List</span></span>](overviews-direct3d-11-render-multi-thread-command-list.md)<br/>                                   | <span data-ttu-id="69320-116">Un elenco di comandi è una sequenza di comandi GPU che possono essere registrati e riprodotti.</span><span class="sxs-lookup"><span data-stu-id="69320-116">A command list is a sequence of GPU commands that can be recorded and played back.</span></span> <span data-ttu-id="69320-117">Un elenco di comandi può migliorare le prestazioni riducendo la quantità di overhead generato dal runtime.</span><span class="sxs-lookup"><span data-stu-id="69320-117">A command list may improve performance by reducing the amount of overhead generated by the runtime.</span></span><br/>                                    |
| [<span data-ttu-id="69320-118">Differenze di threading tra le versioni di Direct3D</span><span class="sxs-lookup"><span data-stu-id="69320-118">Threading Differences between Direct3D Versions</span></span>](overviews-direct3d-11-render-multi-thread-differences.md)<br/> | <span data-ttu-id="69320-119">Molti modelli di programmazione multithread utilizzano le primitive di sincronizzazione (ad esempio, mutex) per creare sezioni critiche e impedire l'accesso al codice da parte di più thread alla volta.</span><span class="sxs-lookup"><span data-stu-id="69320-119">Many multi-threaded programming models make use of synchronization primitives (such as mutexes) to create critical sections and prevent code from being accessed by more than one thread at a time.</span></span><br/>                       |



 

## <a name="related-topics"></a><span data-ttu-id="69320-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="69320-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69320-121">Procedura: verificare il supporto dei driver</span><span class="sxs-lookup"><span data-stu-id="69320-121">How To: Check for Driver Support</span></span>](overviews-direct3d-11-render-multi-thread-support.md)
</dt> <dt>

[<span data-ttu-id="69320-122">Rendering</span><span class="sxs-lookup"><span data-stu-id="69320-122">Rendering</span></span>](overviews-direct3d-11-render.md)
</dt> </dl>

 

 






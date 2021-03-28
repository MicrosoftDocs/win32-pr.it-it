---
title: Creazione di oggetti con multithreading
description: Utilizzare l'interfaccia ID3D11Device per creare risorse e oggetti, utilizzare sul ID3D11DeviceContext per il rendering.
ms.assetid: e1765192-865c-4a62-9be7-6e95280ee8ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28cbfbe73efc96b301216deb5ccbf623354ddbb7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955493"
---
# <a name="object-creation-with-multithreading"></a><span data-ttu-id="52189-103">Creazione di oggetti con multithreading</span><span class="sxs-lookup"><span data-stu-id="52189-103">Object Creation with Multithreading</span></span>

<span data-ttu-id="52189-104">Utilizzare l'interfaccia [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) per creare risorse e oggetti, utilizzare [**sul ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) per il [rendering](overviews-direct3d-11-render-multi-thread-render.md).</span><span class="sxs-lookup"><span data-stu-id="52189-104">Use the [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface to create resources and objects, use the [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) for [rendering](overviews-direct3d-11-render-multi-thread-render.md).</span></span>

<span data-ttu-id="52189-105">Di seguito sono riportati alcuni esempi di come creare le risorse:</span><span class="sxs-lookup"><span data-stu-id="52189-105">Here are some examples of how to create resources:</span></span>

-   [<span data-ttu-id="52189-106">Procedura: creare un vertex buffer</span><span class="sxs-lookup"><span data-stu-id="52189-106">How to: Create a Vertex Buffer</span></span>](overviews-direct3d-11-resources-buffers-vertex-how-to.md)
-   [<span data-ttu-id="52189-107">Procedura: creare un buffer di indice</span><span class="sxs-lookup"><span data-stu-id="52189-107">How to: Create an Index Buffer</span></span>](overviews-direct3d-11-resources-buffers-index-how-to.md)
-   [<span data-ttu-id="52189-108">Procedura: creare un buffer costante</span><span class="sxs-lookup"><span data-stu-id="52189-108">How to: Create a Constant Buffer</span></span>](overviews-direct3d-11-resources-buffers-constant-how-to.md)
-   [<span data-ttu-id="52189-109">Procedura: inizializzare una trama da un file</span><span class="sxs-lookup"><span data-stu-id="52189-109">How to: Initialize a Texture From a File</span></span>](overviews-direct3d-11-resources-textures-how-to.md)

## <a name="multithreading-considerations"></a><span data-ttu-id="52189-110">Considerazioni sul multithreading</span><span class="sxs-lookup"><span data-stu-id="52189-110">Multithreading Considerations</span></span>

<span data-ttu-id="52189-111">La quantità di concorrenza della creazione e del rendering delle risorse che l'applicazione può ottenere dipende dal livello di supporto del multithreading implementato dal driver.</span><span class="sxs-lookup"><span data-stu-id="52189-111">The amount of concurrency of resource creation and rendering that your application can achieve depends on the level of multithreading support that the driver implements.</span></span> <span data-ttu-id="52189-112">Se il driver supporta le operazioni di creazione simultanea, l'applicazione dovrebbe presentare problemi di concorrenza molto inferiori.</span><span class="sxs-lookup"><span data-stu-id="52189-112">If the driver supports concurrent creates, then the application should have much less concurrency concerns.</span></span> <span data-ttu-id="52189-113">Tuttavia, se il driver non supporta la creazione di oggetti simultanei, la quantità di concorrenza è estremamente limitata.</span><span class="sxs-lookup"><span data-stu-id="52189-113">However, if the driver does not support concurrent object creation, the amount of concurrency is extremely limited.</span></span> <span data-ttu-id="52189-114">Per comprendere la quantità di supporto disponibile in un driver, eseguire una query sul driver per il valore del membro **DriverConcurrentCreates** della struttura di [**\_ \_ \_ Threading dei dati della funzionalità d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) .</span><span class="sxs-lookup"><span data-stu-id="52189-114">To understand the amount of support available in a driver, query the driver for the value of the **DriverConcurrentCreates** member of the [**D3D11\_FEATURE\_DATA\_THREADING**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) structure.</span></span> <span data-ttu-id="52189-115">Per ulteriori informazioni sul controllo del supporto dei driver per il multithreading, vedere [procedura: verificare il supporto del driver](overviews-direct3d-11-render-multi-thread-support.md).</span><span class="sxs-lookup"><span data-stu-id="52189-115">For more information about checking for driver support of multithreading, see [How To: Check for Driver Support](overviews-direct3d-11-render-multi-thread-support.md).</span></span>

<span data-ttu-id="52189-116">Le operazioni simultanee non portano necessariamente a prestazioni migliori.</span><span class="sxs-lookup"><span data-stu-id="52189-116">Concurrent operations do not necessarily lead to better performance.</span></span> <span data-ttu-id="52189-117">La creazione e il caricamento di una trama, ad esempio, è in genere limitata dalla larghezza di banda della memoria.</span><span class="sxs-lookup"><span data-stu-id="52189-117">For example, creating and loading a texture is typically limited by memory bandwidth.</span></span> <span data-ttu-id="52189-118">Il tentativo di creare e caricare più trame potrebbe non essere più veloce rispetto a una trama alla volta, anche se questa operazione lascia inattivi più core CPU.</span><span class="sxs-lookup"><span data-stu-id="52189-118">Attempting to create and load multiple textures might be no faster than doing one texture at a time, even if this leaves multiple CPU cores idle.</span></span> <span data-ttu-id="52189-119">Tuttavia, la creazione di più shader che usano più thread può migliorare le prestazioni perché questa operazione è meno dipendente dalle risorse di sistema, ad esempio la larghezza di banda della memoria.</span><span class="sxs-lookup"><span data-stu-id="52189-119">However, creating multiple shaders using multiple threads can increase performance as this operation is less dependent on system resources such as memory bandwidth.</span></span>

<span data-ttu-id="52189-120">Quando il driver e l'hardware grafico supportano il multithreading, è in genere possibile inizializzare in modo più efficiente le risorse appena create passando un puntatore ai dati iniziali nel parametro *pInitialData* , ad esempio in una chiamata al metodo [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) .</span><span class="sxs-lookup"><span data-stu-id="52189-120">When the driver and graphics hardware support multithreading, you can typically initialize newly created resources more efficiently by passing a pointer to initial data in the *pInitialData* parameter (for example, in a call to the [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) method).</span></span>

## <a name="related-topics"></a><span data-ttu-id="52189-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="52189-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52189-122">MultiThreading</span><span class="sxs-lookup"><span data-stu-id="52189-122">MultiThreading</span></span>](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 





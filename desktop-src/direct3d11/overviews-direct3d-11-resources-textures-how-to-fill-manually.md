---
title: Come inizializzare una trama a livello di codice
description: Questo argomento include diversi esempi che illustrano come inizializzare trame create con diversi tipi di utilizzo.
ms.assetid: 65e8ae82-50aa-4303-853e-3457da18f44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5584885b885f6026ee32a3e4c52a24aad78c3c08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856425"
---
# <a name="how-to-initialize-a-texture-programmatically"></a><span data-ttu-id="c863d-103">Procedura: inizializzare una trama a livello di codice</span><span class="sxs-lookup"><span data-stu-id="c863d-103">How to: Initialize a Texture Programmatically</span></span>

<span data-ttu-id="c863d-104">È possibile inizializzare una trama durante la creazione dell'oggetto oppure è possibile compilare l'oggetto a livello di codice dopo che è stato creato.</span><span class="sxs-lookup"><span data-stu-id="c863d-104">You can initialize a texture during object creation, or you can fill the object programmatically after it is created.</span></span> <span data-ttu-id="c863d-105">Questo argomento include diversi esempi che illustrano come inizializzare trame create con diversi tipi di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="c863d-105">This topic has several examples showing how to initialize textures that are created with different types of usages.</span></span> <span data-ttu-id="c863d-106">Questo esempio presuppone che si sappia già come [creare una trama](overviews-direct3d-11-resources-textures-create.md).</span><span class="sxs-lookup"><span data-stu-id="c863d-106">This example assumes you already know how to [Create a Texture](overviews-direct3d-11-resources-textures-create.md).</span></span>

-   [<span data-ttu-id="c863d-107">Utilizzo predefinito</span><span class="sxs-lookup"><span data-stu-id="c863d-107">Default Usage</span></span>](#default-usage)
-   [<span data-ttu-id="c863d-108">Utilizzo dinamico</span><span class="sxs-lookup"><span data-stu-id="c863d-108">Dynamic Usage</span></span>](#dynamic-usage)
-   [<span data-ttu-id="c863d-109">Utilizzo di gestione temporanea</span><span class="sxs-lookup"><span data-stu-id="c863d-109">Staging Usage</span></span>](#staging-usage)
-   [<span data-ttu-id="c863d-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c863d-110">Related topics</span></span>](#related-topics)

## <a name="default-usage"></a><span data-ttu-id="c863d-111">Utilizzo predefinito</span><span class="sxs-lookup"><span data-stu-id="c863d-111">Default Usage</span></span>

<span data-ttu-id="c863d-112">Il tipo di utilizzo più comune è l'utilizzo predefinito.</span><span class="sxs-lookup"><span data-stu-id="c863d-112">The most common type of usage is default usage.</span></span> <span data-ttu-id="c863d-113">Per riempire una trama predefinita (una creata con **l' \_ \_ impostazione predefinita di utilizzo di d3d11**), è possibile eseguire una delle operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c863d-113">To fill a default texture (one created with **D3D11\_USAGE\_DEFAULT**) you can either:</span></span>

-   <span data-ttu-id="c863d-114">Chiamare [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) e inizializzare *pInitialData* per puntare ai dati forniti da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c863d-114">Call [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) and initialize *pInitialData* to point to data provided from an application.</span></span>

    <span data-ttu-id="c863d-115">oppure</span><span class="sxs-lookup"><span data-stu-id="c863d-115">or</span></span>

-   <span data-ttu-id="c863d-116">Dopo la chiamata a [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d), usare [**sul ID3D11DeviceContext:: UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) per riempire la trama predefinita con i dati di un puntatore fornito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c863d-116">After calling [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d), use [**ID3D11DeviceContext::UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) to fill the default texture with data from a pointer provided by the application.</span></span>

## <a name="dynamic-usage"></a><span data-ttu-id="c863d-117">Utilizzo dinamico</span><span class="sxs-lookup"><span data-stu-id="c863d-117">Dynamic Usage</span></span>

<span data-ttu-id="c863d-118">Per riempire una trama dinamica (uno creato con **\_ \_ Dynamic Usage d3d11**):</span><span class="sxs-lookup"><span data-stu-id="c863d-118">To fill a dynamic texture (one created with **D3D11\_USAGE\_DYNAMIC**):</span></span>

1.  <span data-ttu-id="c863d-119">Ottenere un puntatore alla memoria della trama passando il **d3d11 di \_ scrittura della mappa di \_ \_** durante la chiamata a [**sul ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span><span class="sxs-lookup"><span data-stu-id="c863d-119">Get a pointer to the texture memory by passing in **D3D11\_MAP\_WRITE\_DISCARD** when calling [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span></span>
2.  <span data-ttu-id="c863d-120">Scrivere i dati nella memoria.</span><span class="sxs-lookup"><span data-stu-id="c863d-120">Write data to the memory.</span></span>
3.  <span data-ttu-id="c863d-121">Chiamare [**sul ID3D11DeviceContext:: annullare**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) al termine della scrittura dei dati.</span><span class="sxs-lookup"><span data-stu-id="c863d-121">Call [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) when you are finished writing data.</span></span>

## <a name="staging-usage"></a><span data-ttu-id="c863d-122">Utilizzo di gestione temporanea</span><span class="sxs-lookup"><span data-stu-id="c863d-122">Staging Usage</span></span>

<span data-ttu-id="c863d-123">Per riempire una trama di gestione temporanea (uno creato con **\_ \_ gestione temporanea dell'utilizzo di d3d11**):</span><span class="sxs-lookup"><span data-stu-id="c863d-123">To fill a staging texture (one created with **D3D11\_USAGE\_STAGING**):</span></span>

1.  <span data-ttu-id="c863d-124">Ottenere un puntatore alla memoria della trama passando la **scrittura della \_ mappa \_ d3d11** quando si chiama [**sul ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span><span class="sxs-lookup"><span data-stu-id="c863d-124">Get a pointer to the texture memory by passing in **D3D11\_MAP\_WRITE** when calling [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span></span>
2.  <span data-ttu-id="c863d-125">Scrivere i dati nella memoria.</span><span class="sxs-lookup"><span data-stu-id="c863d-125">Write data to the memory.</span></span>
3.  <span data-ttu-id="c863d-126">Chiamare [**sul ID3D11DeviceContext:: annullare**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) al termine della scrittura dei dati.</span><span class="sxs-lookup"><span data-stu-id="c863d-126">Call [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) when you are finished writing data.</span></span>

<span data-ttu-id="c863d-127">Una trama di staging può quindi essere usata come parametro di origine per [**sul ID3D11DeviceContext:: CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) o [**sul ID3D11DeviceContext:: CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) per riempire una risorsa predefinita o dinamica.</span><span class="sxs-lookup"><span data-stu-id="c863d-127">A staging texture can then be used as the source parameter to [**ID3D11DeviceContext::CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) or [**ID3D11DeviceContext::CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) to fill a default or dynamic resource.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c863d-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c863d-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c863d-129">Come usare Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="c863d-129">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="c863d-130">Trame</span><span class="sxs-lookup"><span data-stu-id="c863d-130">Textures</span></span>](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 





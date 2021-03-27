---
title: Come creare una trama
description: In questo argomento viene illustrato come creare una trama.
ms.assetid: dfe88635-b2c2-48f8-a21e-cce845b518fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3d3c4715bb4c790ea772dcbba4834051946747e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712058"
---
# <a name="how-to-create-a-texture"></a><span data-ttu-id="71899-103">Procedura: creare una trama</span><span class="sxs-lookup"><span data-stu-id="71899-103">How to: Create a Texture</span></span>

<span data-ttu-id="71899-104">Il modo più semplice per creare una trama consiste nel descrivere le proprietà e chiamare l'API per la creazione di trame.</span><span class="sxs-lookup"><span data-stu-id="71899-104">The simplest way to create a texture is to describe its properties and call the texture creation API.</span></span> <span data-ttu-id="71899-105">In questo argomento viene illustrato come creare una trama.</span><span class="sxs-lookup"><span data-stu-id="71899-105">This topic shows how to create a texture.</span></span>

<span data-ttu-id="71899-106">**Per creare una trama**</span><span class="sxs-lookup"><span data-stu-id="71899-106">**To create a texture**</span></span>

1.  <span data-ttu-id="71899-107">Compilare una struttura [**d3d11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) con una descrizione dei parametri della trama.</span><span class="sxs-lookup"><span data-stu-id="71899-107">Fill in a [**D3D11\_TEXTURE2D\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) structure with a description of the texture parameters.</span></span>
2.  <span data-ttu-id="71899-108">Creare la trama chiamando [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) con la descrizione della trama.</span><span class="sxs-lookup"><span data-stu-id="71899-108">Create the texture by calling [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) with the texture description.</span></span>

<span data-ttu-id="71899-109">Questo esempio crea una trama 256 x 256, con [**utilizzo dinamico**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), da usare come [**risorsa shader**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) con accesso in [**scrittura alla CPU**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag).</span><span class="sxs-lookup"><span data-stu-id="71899-109">This example creates a 256 x 256 texture, with [**dynamic usage**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), for use as a [**shader resource**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) with [**cpu write access**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag).</span></span>


```
D3D11_TEXTURE2D_DESC desc;
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D11_USAGE_DYNAMIC;
desc.BindFlags = D3D11_BIND_SHADER_RESOURCE;
desc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;
desc.MiscFlags = 0;

ID3D11Device *pd3dDevice; // Don't forget to initialize this
ID3D11Texture2D *pTexture = NULL;
pd3dDevice->CreateTexture2D( &desc, NULL, &pTexture );
```



## <a name="related-topics"></a><span data-ttu-id="71899-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="71899-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71899-111">Come usare Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="71899-111">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="71899-112">Trame</span><span class="sxs-lookup"><span data-stu-id="71899-112">Textures</span></span>](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 





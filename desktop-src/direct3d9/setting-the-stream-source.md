---
description: "Il metodo IDirect3DDevice9:: SetStreamSource associa un buffer vertex a un flusso di dati del dispositivo, creando un'associazione tra i dati dei vertici e una delle diverse porte del flusso di dati che alimentano le funzioni di elaborazione primitive."
ms.assetid: ef317537-3095-435d-b0f2-83cb3b385da2
title: Impostazione dell'origine del flusso (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76d0c296b79d258be6eee2d683979081673d5d04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521913"
---
# <a name="setting-the-stream-source-direct3d-9"></a><span data-ttu-id="3073c-103">Impostazione dell'origine del flusso (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3073c-103">Setting the Stream Source (Direct3D 9)</span></span>

<span data-ttu-id="3073c-104">Il metodo [**IDirect3DDevice9:: SetStreamSource**](/windows/desktop/api) associa un buffer vertex a un flusso di dati del dispositivo, creando un'associazione tra i dati dei vertici e una delle diverse porte del flusso di dati che alimentano le funzioni di elaborazione primitive.</span><span class="sxs-lookup"><span data-stu-id="3073c-104">The [**IDirect3DDevice9::SetStreamSource**](/windows/desktop/api) method binds a vertex buffer to a device data stream, creating an association between the vertex data and one of several data stream ports that feed the primitive processing functions.</span></span> <span data-ttu-id="3073c-105">I riferimenti effettivi ai dati del flusso non si verificano fino a quando non viene chiamato un metodo di disegno, ad esempio [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span><span class="sxs-lookup"><span data-stu-id="3073c-105">The actual references to the stream data do not occur until a drawing method, such as [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), is called.</span></span>

<span data-ttu-id="3073c-106">Un flusso viene definito come una matrice uniforme di dati del componente, dove ogni componente è costituito da uno o più elementi che rappresentano una singola entità, ad esempio posizione, normale, colore e così via.</span><span class="sxs-lookup"><span data-stu-id="3073c-106">A stream is defined as a uniform array of component data, where each component consists of one or more elements representing a single entity such as position, normal, color, and so on.</span></span> <span data-ttu-id="3073c-107">Il parametro stride specifica la dimensione, in byte, del componente.</span><span class="sxs-lookup"><span data-stu-id="3073c-107">The Stride parameter specifies the size of the component, in bytes.</span></span>

<span data-ttu-id="3073c-108">Il codice seguente illustra l'impostazione dell'origine del flusso e il disegno del relativo contenuto.</span><span class="sxs-lookup"><span data-stu-id="3073c-108">The following code demonstrates setting the stream source and drawing its contents.</span></span> <span data-ttu-id="3073c-109">La \_ variabile g pVB è un LPDIRECT3DVERTEXBUFFER9 che contiene i dati dei vertici.</span><span class="sxs-lookup"><span data-stu-id="3073c-109">The g\_pVB variable is a LPDIRECT3DVERTEXBUFFER9 that contains vertex data.</span></span>


```
if( SUCCEEDED( g_pd3dDevice->BeginScene() ) )
{
    // Setup the world, view, and projection matrices
    SetupMatrices();

    // Render the vertex buffer contents
    g_pd3dDevice->SetStreamSource( 0, g_pVB, 0, sizeof(CUSTOMVERTEX) );
    g_pd3dDevice->SetFVF( D3DFVF_CUSTOMVERTEX );
    g_pd3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 1 );

    // End the scene
    g_pd3dDevice->EndScene();
}
```



<span data-ttu-id="3073c-110">Per ulteriori informazioni su questo codice, vedere l'esercitazione [3: utilizzo di matrici](https://msdn.microsoft.com/library/Ee418892(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="3073c-110">For more information about this code see the following tutorial: [Tutorial 3: Using Matrices](https://msdn.microsoft.com/library/Ee418892(v=VS.85).aspx)</span></span>

## <a name="related-topics"></a><span data-ttu-id="3073c-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3073c-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3073c-112">Primitive di rendering</span><span class="sxs-lookup"><span data-stu-id="3073c-112">Rendering Primitives</span></span>](rendering-primitives.md)
</dt> </dl>

 

 

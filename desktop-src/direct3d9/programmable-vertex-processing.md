---
description: Quando si usa un vertex shader programmato, gli elementi aggiornati nel buffer del vertice di destinazione sono controllati dal programma di funzione shader.
ms.assetid: c75564ef-528b-4af5-9ed7-a32b9120bf6a
title: Elaborazione Vertex programmabile (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5108792350aebbca4f58924fde81d191b062591b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304195"
---
# <a name="programmable-vertex-processing-direct3d-9"></a><span data-ttu-id="1fa30-103">Elaborazione Vertex programmabile (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1fa30-103">Programmable Vertex Processing (Direct3D 9)</span></span>

<span data-ttu-id="1fa30-104">Quando si usa un vertex shader programmato, gli elementi aggiornati nel buffer del vertice di destinazione sono controllati dal programma di funzione shader.</span><span class="sxs-lookup"><span data-stu-id="1fa30-104">When using a programmed vertex shader, the elements updated in the destination vertex buffer are controlled by the shader function program.</span></span> <span data-ttu-id="1fa30-105">Quando l'applicazione scrive in uno dei registri dei vertici di destinazione, viene aggiornato l'elemento corrispondente all'interno di ogni vertice del buffer del vertice di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1fa30-105">When the application writes to one of the destination vertex registers, the corresponding element within each vertex of the destination vertex buffer is updated.</span></span> <span data-ttu-id="1fa30-106">Gli elementi nel buffer del vertice di destinazione che non vengono scritti dall'applicazione non vengono modificati.</span><span class="sxs-lookup"><span data-stu-id="1fa30-106">Elements in the destination vertex buffer that are not written to by the application are not modified.</span></span> <span data-ttu-id="1fa30-107">[**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) avrà esito negativo se l'applicazione scrive in elementi che non sono presenti nel buffer del vertice di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1fa30-107">[**IDirect3DDevice9::ProcessVertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) will fail if the application writes to elements that are not present in the destination vertex buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1fa30-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1fa30-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fa30-109">Buffer vertici</span><span class="sxs-lookup"><span data-stu-id="1fa30-109">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> </dl>

 

 

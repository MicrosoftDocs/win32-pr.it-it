---
title: Parametri di creazione dei pool di riquadri
description: Usare i parametri in questa sezione per definire i pool di sezioni tramite l'API CreateBuffer di ID3D11Device.
ms.assetid: 04290AAF-8517-4557-954E-1CAA3A0CA7F6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c22ef3acf1c7b926890d1c5867df55bea4821b90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044235"
---
# <a name="tile-pool-creation-parameters"></a><span data-ttu-id="5462a-103">Parametri di creazione dei pool di riquadri</span><span class="sxs-lookup"><span data-stu-id="5462a-103">Tile pool creation parameters</span></span>

<span data-ttu-id="5462a-104">Usare i parametri in questa sezione per definire i pool di sezioni tramite l'API [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) .</span><span class="sxs-lookup"><span data-stu-id="5462a-104">Use the parameters in this section to define tile pools via the [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) API.</span></span>

<dl> <dt>

<span data-ttu-id="5462a-105"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="5462a-105"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Size**</span></span>
</dt> <dd>

<span data-ttu-id="5462a-106">Dimensioni di allocazione, come un multiplo di 64KB.</span><span class="sxs-lookup"><span data-stu-id="5462a-106">Allocation size, as a multiple of 64KB.</span></span> <span data-ttu-id="5462a-107">0 è valido perché in seguito è possibile usare un'operazione [**ID3D11DeviceContext2:: ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) .</span><span class="sxs-lookup"><span data-stu-id="5462a-107">0 is valid because you can later use a [**ID3D11DeviceContext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) operation.</span></span>

</dd> <dt>

<span data-ttu-id="5462a-108"><span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Flag varie delle risorse supportate**</span><span class="sxs-lookup"><span data-stu-id="5462a-108"><span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Supported Resource Misc Flags**</span></span>
</dt> <dd>

<span data-ttu-id="5462a-109">\_ \_ \_ \_ Il pool di sezioni varie della risorsa d3d11 (identifica la risorsa come pool di sezioni), la \_ risorsa d3d11 \_ varie \_ condivise, \_ \_ KEYEDMUTEX condivise o \_ \_ NTHANDLE condiviso.</span><span class="sxs-lookup"><span data-stu-id="5462a-109">D3D11\_RESOURCE\_MISC\_TILE\_POOL (identifies the resource as a tile pool), D3D11\_RESOURCE\_MISC\_SHARED, \_SHARED\_KEYEDMUTEX, or \_SHARED\_NTHANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="5462a-110"><span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Utilizzo risorse supportato**</span><span class="sxs-lookup"><span data-stu-id="5462a-110"><span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Supported Resource Usage**</span></span>
</dt> <dd>

<span data-ttu-id="5462a-111">\_Solo utilizzo \_ predefinito di d3d11.</span><span class="sxs-lookup"><span data-stu-id="5462a-111">D3D11\_USAGE\_DEFAULT only.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="5462a-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5462a-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5462a-113">Creazione di risorse affiancate</span><span class="sxs-lookup"><span data-stu-id="5462a-113">Creating tiled resources</span></span>](creating-tiled-resources.md)
</dt> </dl>

 

 





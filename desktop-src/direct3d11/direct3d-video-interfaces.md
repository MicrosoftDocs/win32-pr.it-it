---
title: Interfacce video Direct3D
description: Questo argomento elenca le interfacce video Direct3D disponibili in Direct3D 9Ex e supportate in Windows 7 e versioni successive dei sistemi operativi client Windows e in Windows Server 2008 R2 e versioni successive dei sistemi operativi Windows Server.
ms.assetid: 922AC983-B9C0-494C-BADD-CEF20931FC26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d20c86e172308d4be6f4c6218a110f49b033ee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473334"
---
# <a name="direct3d-video-interfaces"></a><span data-ttu-id="f6140-103">Interfacce video Direct3D</span><span class="sxs-lookup"><span data-stu-id="f6140-103">Direct3D Video Interfaces</span></span>

<span data-ttu-id="f6140-104">Questo argomento elenca le interfacce video Direct3D disponibili in Direct3D 9Ex e supportate in Windows 7 e versioni successive dei sistemi operativi client Windows e in Windows Server 2008 R2 e versioni successive dei sistemi operativi Windows Server.</span><span class="sxs-lookup"><span data-stu-id="f6140-104">This topic lists the Direct3D video interfaces that are available in Direct3D 9Ex and that are supported on Windows 7 and later versions of Windows client operating systems and on Windows Server 2008 R2 and later versions of Windows server operating systems.</span></span> <span data-ttu-id="f6140-105">È possibile utilizzare queste interfacce e i relativi metodi per ottenere le funzionalità di protezione del contenuto video del driver grafico e le funzionalità hardware sovrapposte di un dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f6140-105">You can use these interfaces and their methods to obtain the video content protection capabilities of the graphics driver and the overlay hardware capabilities of a Direct3D device.</span></span> <span data-ttu-id="f6140-106">È anche possibile usare queste interfacce e i relativi metodi per proteggere il contenuto video.</span><span class="sxs-lookup"><span data-stu-id="f6140-106">You can also use these interfaces and their methods to protect video content.</span></span> <span data-ttu-id="f6140-107">Queste interfacce e i relativi metodi sono definiti in d3d9. h e descritti nella sezione [Microsoft Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) .</span><span class="sxs-lookup"><span data-stu-id="f6140-107">These interfaces and their methods are defined in D3d9.h and described in the [Microsoft Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) section.</span></span>



| <span data-ttu-id="f6140-108">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="f6140-108">Interface</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="f6140-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6140-109">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6140-110"><span id="IDirect3D9ExOverlayExtension"></span><span id="idirect3d9exoverlayextension"></span><span id="IDIRECT3D9EXOVERLAYEXTENSION"></span>[**IDirect3D9ExOverlayExtension**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9exoverlayextension)</span><span class="sxs-lookup"><span data-stu-id="f6140-110"><span id="IDirect3D9ExOverlayExtension"></span><span id="idirect3d9exoverlayextension"></span><span id="IDIRECT3D9EXOVERLAYEXTENSION"></span>[**IDirect3D9ExOverlayExtension**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9exoverlayextension)</span></span><br/>           | <span data-ttu-id="f6140-111">Esegue una query sulle funzionalità hardware sovrapposte di un dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f6140-111">Queries the overlay hardware capabilities of a Direct3D device.</span></span><br/>                                                     |
| <span data-ttu-id="f6140-112"><span id="IDirect3DAuthenticatedChannel9"></span><span id="idirect3dauthenticatedchannel9"></span><span id="IDIRECT3DAUTHENTICATEDCHANNEL9"></span>[**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9)</span><span class="sxs-lookup"><span data-stu-id="f6140-112"><span id="IDirect3DAuthenticatedChannel9"></span><span id="idirect3dauthenticatedchannel9"></span><span id="IDIRECT3DAUTHENTICATEDCHANNEL9"></span>[**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9)</span></span><br/> | <span data-ttu-id="f6140-113">Fornisce un canale di comunicazione con il driver di grafica o il runtime Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f6140-113">Provides a communication channel with the graphics driver or the Direct3D runtime.</span></span><br/>                                  |
| <span data-ttu-id="f6140-114"><span id="IDirect3DCryptoSession9"></span><span id="idirect3dcryptosession9"></span><span id="IDIRECT3DCRYPTOSESSION9"></span>[**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)</span><span class="sxs-lookup"><span data-stu-id="f6140-114"><span id="IDirect3DCryptoSession9"></span><span id="idirect3dcryptosession9"></span><span id="IDIRECT3DCRYPTOSESSION9"></span>[**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)</span></span><br/>                                    | <span data-ttu-id="f6140-115">Rappresenta una sessione di crittografia utilizzata per accedere a una superficie protetta.</span><span class="sxs-lookup"><span data-stu-id="f6140-115">Represents a cryptographic session that is used to access a protected surface.</span></span><br/>                                      |
| <span data-ttu-id="f6140-116"><span id="IDirect3DDevice9Video"></span><span id="idirect3ddevice9video"></span><span id="IDIRECT3DDEVICE9VIDEO"></span>[**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video)</span><span class="sxs-lookup"><span data-stu-id="f6140-116"><span id="IDirect3DDevice9Video"></span><span id="idirect3ddevice9video"></span><span id="IDIRECT3DDEVICE9VIDEO"></span>[**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video)</span></span><br/>                                              | <span data-ttu-id="f6140-117">Consente a un'applicazione di utilizzare i servizi di crittografia e protezione del contenuto implementati da un driver di grafica.</span><span class="sxs-lookup"><span data-stu-id="f6140-117">Enables an application to use content protection and encryption services that are implemented by a graphics driver.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="f6140-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f6140-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6140-119">Effetti (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="f6140-119">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> <dt>

[<span data-ttu-id="f6140-120">Guida alla programmazione per Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="f6140-120">Programming Guide for Direct3D 11</span></span>](dx-graphics-overviews.md)
</dt> </dl>

 


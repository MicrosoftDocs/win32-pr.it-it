---
description: Oltre alla catena di scambio di proprietà e manipolata tramite l'interfaccia IDirect3DDevice9, un'applicazione può creare altre catene di scambio per presentare più visualizzazioni dallo stesso dispositivo.
ms.assetid: 4fc09b9c-7adb-4f5d-80e0-2d39bc10420e
title: Presentazione di più visualizzazioni in modalità finestra (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 039b02c487e06c7464dc8163c719371dc2b23706
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522769"
---
# <a name="presenting-multiple-views-in-windowed-mode-direct3d-9"></a><span data-ttu-id="4709e-103">Presentazione di più visualizzazioni in modalità finestra (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4709e-103">Presenting Multiple Views in Windowed Mode (Direct3D 9)</span></span>

<span data-ttu-id="4709e-104">Oltre alla catena di scambio di proprietà e manipolata tramite l'interfaccia [**IDirect3DDevice9**](/windows/desktop/api) , un'applicazione può creare altre catene di scambio per presentare più visualizzazioni dallo stesso dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4709e-104">In addition to the swap chain that is owned and manipulated through the [**IDirect3DDevice9**](/windows/desktop/api) interface, an application can create additional swap chains in order to present multiple views from the same device.</span></span> <span data-ttu-id="4709e-105">L'applicazione crea in genere una catena di scambio per ogni visualizzazione usando il metodo [**IDirect3DDevice9:: CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) e associa ogni catena di scambio a una determinata finestra.</span><span class="sxs-lookup"><span data-stu-id="4709e-105">The application typically creates one swap chain per view by using the [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) method, and associates each swap chain with a particular window.</span></span> <span data-ttu-id="4709e-106">L'applicazione esegue il rendering delle immagini nei buffer indietro di ogni catena di scambio e quindi le presenta singolarmente.</span><span class="sxs-lookup"><span data-stu-id="4709e-106">The application renders images into the back buffers of each swap chain, and then presents them individually.</span></span>

<span data-ttu-id="4709e-107">Solo una catena di scambio alla volta può essere a schermo intero in ogni scheda.</span><span class="sxs-lookup"><span data-stu-id="4709e-107">Only one swap chain at a time can be full-screen on each adapter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4709e-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4709e-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4709e-109">Suggerimenti per la programmazione</span><span class="sxs-lookup"><span data-stu-id="4709e-109">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 

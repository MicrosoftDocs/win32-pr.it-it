---
description: "Oltre alla catena di scambio di proprietà e manipolata tramite l'oggetto Direct3DDevice, un'applicazione può usare il metodo IDirect3DDevice9:: CreateAdditionalSwapChain per creare catene di scambio aggiuntive per presentare più visualizzazioni dallo stesso dispositivo."
ms.assetid: f0d01dfb-d1de-4d16-8c64-4ae56d7fed06
title: Visualizzazioni multiple in modalità finestra (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed750472d1816c0365298630cfb426982743b11a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303920"
---
# <a name="multiple-views-in-windowed-mode-direct3d-9"></a><span data-ttu-id="74545-103">Visualizzazioni multiple in modalità finestra (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="74545-103">Multiple Views in Windowed Mode (Direct3D 9)</span></span>

<span data-ttu-id="74545-104">Oltre alla catena di scambio di proprietà e manipolata tramite l'oggetto Direct3DDevice, un'applicazione può usare il metodo [**IDirect3DDevice9:: CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) per creare catene di scambio aggiuntive per presentare più visualizzazioni dallo stesso dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74545-104">In addition to the swap chain that is owned and manipulated through the Direct3DDevice object, an application can use the [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) method to create additional swap chains to present multiple views from the same device.</span></span>

<span data-ttu-id="74545-105">In genere, l'applicazione crea una catena di scambio per ogni visualizzazione e associa ogni catena di scambio a una visualizzazione specifica.</span><span class="sxs-lookup"><span data-stu-id="74545-105">Typically, the application creates one swap chain per view, and it associates each swap chain with a particular view.</span></span> <span data-ttu-id="74545-106">L'applicazione esegue il rendering delle immagini nei buffer indietro di ogni catena di scambio, quindi usa il metodo [**IDirect3DDevice9::P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) reinviato per presentarle singolarmente.</span><span class="sxs-lookup"><span data-stu-id="74545-106">The application renders images in the back buffers of each swap chain, and then uses the [**IDirect3DDevice9::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) method to present them individually.</span></span> <span data-ttu-id="74545-107">Si noti che solo una catena di scambio alla volta può essere a schermo intero in ogni scheda.</span><span class="sxs-lookup"><span data-stu-id="74545-107">Note that only one swap chain at a time can be full-screen on each adapter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74545-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="74545-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74545-109">Presentazione di una scena</span><span class="sxs-lookup"><span data-stu-id="74545-109">Presenting a Scene</span></span>](presenting-a-scene.md)
</dt> </dl>

 

 

---
description: Supporto di VMR per l'accelerazione video DirectX
ms.assetid: 4bb5612d-3841-4920-a5ef-39ce357a6d1c
title: Supporto di VMR per l'accelerazione video DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ed2e9f4907fdc653ccea6b6244c744073a9d157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753810"
---
# <a name="vmr-support-for-directx-video-acceleration"></a><span data-ttu-id="b36af-103">Supporto di VMR per l'accelerazione video DirectX</span><span class="sxs-lookup"><span data-stu-id="b36af-103">VMR Support for DirectX Video Acceleration</span></span>

<span data-ttu-id="b36af-104">L'accelerazione video DirectX è un'API (Application Programming Interface) e un'interfaccia DDI (Device Driver Interface) corrispondente per l'accelerazione hardware dell'elaborazione della decodifica video digitale, con supporto della fusione alfa per tali scopi come supporto per le immagini di DVD.</span><span class="sxs-lookup"><span data-stu-id="b36af-104">DirectX Video Acceleration is an Application Programming Interface (API) and a corresponding Device Driver Interface (DDI) for hardware acceleration of digital video decoding processing, with support of alpha blending for such purposes as DVD subpicture support.</span></span> <span data-ttu-id="b36af-105">DirectX VA documentato nel DDK di Windows.</span><span class="sxs-lookup"><span data-stu-id="b36af-105">DirectX VA is documented in the Windows DDK.</span></span> <span data-ttu-id="b36af-106">L'interfaccia [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) , che fornisce l'accesso in modalità utente alla funzionalità DirectX va in un dispositivo hardware, è documentata in questo SDK.</span><span class="sxs-lookup"><span data-stu-id="b36af-106">The [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) interface, which provides user mode access to DirectX VA functionality on a hardware device, is documented in this SDK.</span></span>

<span data-ttu-id="b36af-107">VMR supporta [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator)e la relativa implementazione è identica a quella del vecchio mixer sovrapposto, ad eccezione di una differenza importante.</span><span class="sxs-lookup"><span data-stu-id="b36af-107">The VMR supports [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator), and its implementation is identical to the old Overlay Mixer except for one important difference.</span></span> <span data-ttu-id="b36af-108">Il mixer di sovrimpressione ha garantito che l'output venga sottoposto a rendering in una superficie sovrapposta, mentre VMR può inviare l'output per un'ulteriore elaborazione, ad esempio un'operazione 3D, oppure inviare l'output a una superficie Offscreen che viene quindi blitted alla superficie primaria.</span><span class="sxs-lookup"><span data-stu-id="b36af-108">The Overlay Mixer guaranteed that the output is rendered into an overlay surface, while the VMR can send the output for further processing, for example a 3D operation, or it might send the output to an offscreen surface which is then blitted to the primary surface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b36af-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b36af-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b36af-110">Informazioni sull'accelerazione video DirectX</span><span class="sxs-lookup"><span data-stu-id="b36af-110">About DirectX Video Acceleration</span></span>](about-directx-video-acceleration.md)
</dt> </dl>

 

 




---
description: "Quando un dispositivo viene reimpostato correttamente (IDirect3DDevice9:: Reset) o creato (IDirect3D9:: CreateDevice) nelle operazioni a schermo intero, l'oggetto Direct3D che ha creato il dispositivo viene contrassegnato come proprietario di tutte le schede nel sistema."
ms.assetid: df3b6ed7-830b-4635-9295-fff05cc35891
title: Operazioni di Multiple-Monitor (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04427db6c91ff85706040589a89f6fdcfb3761e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304068"
---
# <a name="multiple-monitor-operations-direct3d-9"></a><span data-ttu-id="b9f5d-103">Operazioni di Multiple-Monitor (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b9f5d-103">Multiple-Monitor Operations (Direct3D 9)</span></span>

<span data-ttu-id="b9f5d-104">Quando un dispositivo viene reimpostato correttamente ([**IDirect3DDevice9:: Reset**](/windows/desktop/api)) o creato ([**IDirect3D9:: CreateDevice**](/windows/desktop/api)) nelle operazioni a schermo intero, l'oggetto Direct3D che ha creato il dispositivo viene contrassegnato come proprietario di tutte le schede nel sistema.</span><span class="sxs-lookup"><span data-stu-id="b9f5d-104">When a device is successfully reset ([**IDirect3DDevice9::Reset**](/windows/desktop/api)) or created ([**IDirect3D9::CreateDevice**](/windows/desktop/api)) in full-screen operations, the Direct3D object that created the device is marked as owning all adapters on that system.</span></span> <span data-ttu-id="b9f5d-105">Questo stato è noto come modalità esclusiva e l'oggetto Direct3D è proprietario della modalità esclusiva.</span><span class="sxs-lookup"><span data-stu-id="b9f5d-105">This state is known as exclusive mode, and the Direct3D object owns exclusive mode.</span></span> <span data-ttu-id="b9f5d-106">Modalità esclusiva significa che i dispositivi creati da un altro oggetto Direct3D non possono presupporre operazioni a schermo intero né allocare memoria video.</span><span class="sxs-lookup"><span data-stu-id="b9f5d-106">Exclusive mode means that devices created by any other Direct3D object can neither assume full-screen operations nor allocate video memory.</span></span> <span data-ttu-id="b9f5d-107">Inoltre, quando un oggetto Direct3D presuppone la modalità esclusiva, tutti i dispositivi diversi da quello a schermo intero vengono posizionati nello stato perso.</span><span class="sxs-lookup"><span data-stu-id="b9f5d-107">In addition, when a Direct3D object assumes exclusive mode, all devices other than the one that went full-screen are placed in lost state.</span></span> <span data-ttu-id="b9f5d-108">Per informazioni dettagliate, vedere [dispositivi persi (Direct3D 9)](lost-devices.md).</span><span class="sxs-lookup"><span data-stu-id="b9f5d-108">For details, see [Lost Devices (Direct3D 9)](lost-devices.md).</span></span>

<span data-ttu-id="b9f5d-109">Insieme alla modalità esclusiva, l'oggetto Direct3D viene informato della finestra messa a fuoco che verrà usata dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b9f5d-109">Along with exclusive mode, the Direct3D object is informed of the focus window that the device will use.</span></span> <span data-ttu-id="b9f5d-110">La modalità esclusiva viene rilasciata quando il dispositivo finale a schermo intero di proprietà dell'oggetto Direct3D viene reimpostato sulla modalità finestra o eliminato definitivamente.</span><span class="sxs-lookup"><span data-stu-id="b9f5d-110">Exclusive mode is released when the final full-screen device owned by that Direct3D object is either reset to windowed mode or destroyed.</span></span>

<span data-ttu-id="b9f5d-111">I dispositivi possono essere divisi in due categorie quando un oggetto Direct3D è proprietario della modalità esclusiva.</span><span class="sxs-lookup"><span data-stu-id="b9f5d-111">Devices can be divided into two categories when a Direct3D object owns exclusive mode.</span></span> <span data-ttu-id="b9f5d-112">La prima categoria di dispositivi presenta le caratteristiche seguenti.</span><span class="sxs-lookup"><span data-stu-id="b9f5d-112">The first category of devices have the following characteristics.</span></span>

-   <span data-ttu-id="b9f5d-113">Vengono creati dallo stesso oggetto Direct3D che ha creato il dispositivo a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="b9f5d-113">They are created by the same Direct3D object that created the device that is full-screen.</span></span>
-   <span data-ttu-id="b9f5d-114">Hanno la stessa finestra di messa a fuoco del dispositivo a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="b9f5d-114">They have the same focus window as the device that is full-screen.</span></span>
-   <span data-ttu-id="b9f5d-115">Rappresentano un adattatore diverso da qualsiasi dispositivo a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="b9f5d-115">They represent a different adapter from any full-screen device.</span></span>

<span data-ttu-id="b9f5d-116">I dispositivi in questa categoria non sono soggetti ad alcuna restrizione relativa alla possibilità di reimpostarli o crearli e non vengono inseriti nello stato perso.</span><span class="sxs-lookup"><span data-stu-id="b9f5d-116">Devices in this category have no restrictions concerning their ability to be reset or created, and they are not placed in lost state.</span></span> <span data-ttu-id="b9f5d-117">I dispositivi in questa categoria possono anche essere inseriti in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="b9f5d-117">Devices in this category can even be put into full-screen mode.</span></span>

<span data-ttu-id="b9f5d-118">Dispositivi che non rientrino nella prima categoria: i dispositivi creati da un altro oggetto Direct3D, creati con una finestra di stato attivo diversa e creati per un adapter con un dispositivo che è già a schermo intero, non possono essere reimpostati e rimangono nello stato perduto fino a quando non viene persa la modalità esclusiva.</span><span class="sxs-lookup"><span data-stu-id="b9f5d-118">Devices that do not fall in the first category - devices created by another Direct3D object, created with a different focus window, and created for an adapter with a device that is already full-screen - cannot be reset and remain in lost state until the exclusive mode is lost.</span></span> <span data-ttu-id="b9f5d-119">Di conseguenza, un'applicazione con più monitor può collocare più dispositivi in modalità schermo intero, ma solo se tutti questi dispositivi sono per adattatori diversi, sono stati creati dallo stesso oggetto Direct3D e condividono la stessa finestra di stato attivo.</span><span class="sxs-lookup"><span data-stu-id="b9f5d-119">As a result, a multiple-monitor application can place several devices in full-screen mode, but only if all these devices are for different adapters, were created by the same Direct3D object, and share the same focus window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9f5d-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b9f5d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9f5d-121">Presentazione di una scena</span><span class="sxs-lookup"><span data-stu-id="b9f5d-121">Presenting a Scene</span></span>](presenting-a-scene.md)
</dt> </dl>

 

 




---
title: Funzioni DirectComposition
description: In questa sezione vengono descritte le funzioni fornite da Microsoft DirectComposition \ 32; API.
ms.assetid: 750FDFD5-ADD5-43B3-A596-ECDB82C2EF73
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 934e0b7e32f22faaefdf625e0af2a42a03e469d5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117926"
---
# <a name="directcomposition-functions"></a><span data-ttu-id="758ab-103">Funzioni DirectComposition</span><span class="sxs-lookup"><span data-stu-id="758ab-103">DirectComposition functions</span></span>

<span data-ttu-id="758ab-104">Questa sezione descrive le funzioni fornite dall'API Microsoft DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="758ab-104">This section describes the functions provided by the Microsoft DirectComposition API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="758ab-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="758ab-105">In this section</span></span>



| <span data-ttu-id="758ab-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="758ab-106">Topic</span></span>                                                                                       | <span data-ttu-id="758ab-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="758ab-107">Description</span></span>                                                                                                                                          |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="758ab-108">**DCompositionAttachMouseDragToHwnd**</span><span class="sxs-lookup"><span data-stu-id="758ab-108">**DCompositionAttachMouseDragToHwnd**</span></span>](/windows/desktop/api/dcomp/nf-dcomp-dcompositionattachmousedragtohwnd)<br/>   | <span data-ttu-id="758ab-109">Crea un'interazione/InputSink per instradare il pulsante del mouse verso il basso e tutti gli eventi di spostamento e di rilascio successivi nell'HWND specificato.</span><span class="sxs-lookup"><span data-stu-id="758ab-109">Creates an Interaction/InputSink to route mouse button down and any subsequent move and up events to the given HWND.</span></span><br/>                      |
| [<span data-ttu-id="758ab-110">**DCompositionAttachMouseWheelToHwnd**</span><span class="sxs-lookup"><span data-stu-id="758ab-110">**DCompositionAttachMouseWheelToHwnd**</span></span>](/windows/desktop/api/dcomp/nf-dcomp-dcompositionattachmousewheeltohwnd)<br/> | <span data-ttu-id="758ab-111">Crea un'interazione/InputSink per instradare i messaggi della rotella del mouse all'HWND specificato.</span><span class="sxs-lookup"><span data-stu-id="758ab-111">Creates an Interaction/InputSink to route mouse wheel messages to the given HWND.</span></span> <br/>                                                        |
| [<span data-ttu-id="758ab-112">**DCompositionCreateDevice**</span><span class="sxs-lookup"><span data-stu-id="758ab-112">**DCompositionCreateDevice**</span></span>](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatedevice)<br/>                     | <span data-ttu-id="758ab-113">Crea un nuovo oggetto dispositivo che può essere usato per creare altri oggetti DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="758ab-113">Creates a new device object that can be used to create other DirectComposition objects.</span></span><br/>                                                   |
| [<span data-ttu-id="758ab-114">**DCompositionCreateDevice2**</span><span class="sxs-lookup"><span data-stu-id="758ab-114">**DCompositionCreateDevice2**</span></span>](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatedevice2)<br/>                   | <span data-ttu-id="758ab-115">Crea un nuovo oggetto dispositivo che può essere usato per creare altri oggetti DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="758ab-115">Creates a new device object that can be used to create other DirectComposition objects.</span></span><br/>                                                   |
| [<span data-ttu-id="758ab-116">**DCompositionCreateDevice3**</span><span class="sxs-lookup"><span data-stu-id="758ab-116">**DCompositionCreateDevice3**</span></span>](/windows/desktop/api/dcomp/nf-dcomp-dcompositioncreatedevice3)<br/>                   | <span data-ttu-id="758ab-117">Crea un nuovo oggetto dispositivo DirectComposition, che può essere usato per creare altri oggetti DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="758ab-117">Creates a new DirectComposition device object, which can be used to create other DirectComposition objects.</span></span><br/>                               |
| [<span data-ttu-id="758ab-118">**DCompositionCreateSurfaceHandle**</span><span class="sxs-lookup"><span data-stu-id="758ab-118">**DCompositionCreateSurfaceHandle**</span></span>](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatesurfacehandle)<br/>       | <span data-ttu-id="758ab-119">Crea un nuovo oggetto Surface della composizione che può essere associato a una catena di scambio Microsoft DirectX o a un buffer di scambio e associato a un oggetto visivo.</span><span class="sxs-lookup"><span data-stu-id="758ab-119">Creates a new composition surface object that can be bound to a Microsoft DirectX swap chain or swap buffer and associated with a visual.</span></span><br/> |
| <span data-ttu-id="758ab-120">[**DCompositionGetFrameStatistics**](/previous-versions/windows/desktop/legacy/mt589902(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="758ab-120">[**DCompositionGetFrameStatistics**](/previous-versions/windows/desktop/legacy/mt589902(v=vs.85))</span></span><br/>         | <span data-ttu-id="758ab-121">Recupera le informazioni sulle statistiche di composizione.</span><span class="sxs-lookup"><span data-stu-id="758ab-121">Retrieves composition statistics information.</span></span><br/>                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="758ab-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="758ab-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="758ab-123">Riferimento a DirectComposition</span><span class="sxs-lookup"><span data-stu-id="758ab-123">DirectComposition Reference</span></span>](reference.md)
</dt> </dl>

 


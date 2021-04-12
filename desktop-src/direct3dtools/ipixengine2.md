---
description: Estensioni per l'interfaccia IPixEngine originale.
MS-HAID: vspixengine.IPixEngine2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia IPixEngine2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D650FB4C-C332-4E2E-85EB-DDCE3DA87B0C
api_name:
- IPixEngine2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bf8fe4537a6f4c8703482289302ffa8f3a645903
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481253"
---
# <a name="span-idvspixengineipixengine2spanipixengine2-interface"></a><span data-ttu-id="0279e-103"><span id="vspixengine.ipixengine2"></span>Interfaccia IPixEngine2</span><span class="sxs-lookup"><span data-stu-id="0279e-103"><span id="vspixengine.ipixengine2"></span>IPixEngine2 interface</span></span>

<span data-ttu-id="0279e-104">Estensioni per l'interfaccia IPixEngine originale.</span><span class="sxs-lookup"><span data-stu-id="0279e-104">Extensions to the original IPixEngine interface.</span></span>

## <a name="members"></a><span data-ttu-id="0279e-105">Membri</span><span class="sxs-lookup"><span data-stu-id="0279e-105">Members</span></span>

<span data-ttu-id="0279e-106">L'interfaccia **IPixEngine2** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0279e-106">The **IPixEngine2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0279e-107">**IPixEngine2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0279e-107">**IPixEngine2** also has these types of members:</span></span>

-   [<span data-ttu-id="0279e-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="0279e-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="0279e-109"><span id="methods"></span>Metodi</span><span class="sxs-lookup"><span data-stu-id="0279e-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="0279e-110">L'interfaccia **IPixEngine2** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="0279e-110">The **IPixEngine2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="0279e-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="0279e-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="0279e-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0279e-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="0279e-113"><a href="/windows/desktop/direct3dtools/ipixengine2-endexperiment-bstr-ifileiocallback-ptr"><strong>EndExperiment</strong></a></span><span class="sxs-lookup"><span data-stu-id="0279e-113"><a href="/windows/desktop/direct3dtools/ipixengine2-endexperiment-bstr-ifileiocallback-ptr"><strong>EndExperiment</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="0279e-114">Termina il experiement e completa il log di grafica.</span><span class="sxs-lookup"><span data-stu-id="0279e-114">Ends the experiement and completes the graphics log.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="0279e-115"><a href="/windows/desktop/direct3dtools/ipixengine2-getplaybackmachine-bstr-bool-ptr-bstr-ptr"><strong>GetPlaybackMachine</strong></a></span><span class="sxs-lookup"><span data-stu-id="0279e-115"><a href="/windows/desktop/direct3dtools/ipixengine2-getplaybackmachine-bstr-bool-ptr-bstr-ptr"><strong>GetPlaybackMachine</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="0279e-116">Ottiene informazioni sul computer di riproduzione corrente.</span><span class="sxs-lookup"><span data-stu-id="0279e-116">Gets information about the current playback machine.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="0279e-117"><a href="/windows/desktop/direct3dtools/ipixengine2-onnewdataavailable-bool-bool-int64-int64-int32-byte-arr"><strong>OnNewDataAvailable</strong></a></span><span class="sxs-lookup"><span data-stu-id="0279e-117"><a href="/windows/desktop/direct3dtools/ipixengine2-onnewdataavailable-bool-bool-int64-int64-int32-byte-arr"><strong>OnNewDataAvailable</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="0279e-118">Richieste per indicare che nel log di grafica sono contenuti nuovi dati.</span><span class="sxs-lookup"><span data-stu-id="0279e-118">Requests to indicate that the graphics log has new data inside of it.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="0279e-119"><a href="/windows/desktop/direct3dtools/ipixengine2-setplaybackmachine-bstr-bool-bstr"><strong>SetPlaybackMachine</strong></a></span><span class="sxs-lookup"><span data-stu-id="0279e-119"><a href="/windows/desktop/direct3dtools/ipixengine2-setplaybackmachine-bstr-bool-bstr"><strong>SetPlaybackMachine</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="0279e-120">Imposta il computer di riproduzione corrente per il log di grafica specificato.</span><span class="sxs-lookup"><span data-stu-id="0279e-120">Sets the current playback machine for the specified graphics log.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="0279e-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0279e-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="0279e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0279e-122">Header</span></span></p></td><td><span data-ttu-id="0279e-123">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="0279e-123">Vspixengine.h</span></span></td></tr></tbody></table>

 

 

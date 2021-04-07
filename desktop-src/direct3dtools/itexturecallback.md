---
description: Callback per scrivere una trama come file DDS.
MS-HAID: vspixengine.ITextureCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaccia ITextureCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2558C90A-7235-4A36-859C-0E74BD0B712A
api_name:
- ITextureCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 831de15656960cdc72ef2db50c1f3d13b8491e38
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747370"
---
# <a name="span-idvspixengineitexturecallbackspanitexturecallback-interface"></a><span data-ttu-id="f3d91-103"><span id="vspixengine.itexturecallback"></span>Interfaccia ITextureCallback</span><span class="sxs-lookup"><span data-stu-id="f3d91-103"><span id="vspixengine.itexturecallback"></span>ITextureCallback interface</span></span>

<span data-ttu-id="f3d91-104">Callback per scrivere una trama come file DDS.</span><span class="sxs-lookup"><span data-stu-id="f3d91-104">Callback to write a texture as a DDS file.</span></span>

## <a name="members"></a><span data-ttu-id="f3d91-105">Membri</span><span class="sxs-lookup"><span data-stu-id="f3d91-105">Members</span></span>

<span data-ttu-id="f3d91-106">L'interfaccia **ITextureCallback** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f3d91-106">The **ITextureCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f3d91-107">**ITextureCallback** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f3d91-107">**ITextureCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="f3d91-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="f3d91-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="f3d91-109"><span id="methods"></span>Metodi</span><span class="sxs-lookup"><span data-stu-id="f3d91-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="f3d91-110">L'interfaccia **ITextureCallback** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f3d91-110">The **ITextureCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="f3d91-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="f3d91-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="f3d91-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3d91-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="f3d91-113"><a href="/windows/desktop/direct3dtools/itexturecallback-resultcallback"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="f3d91-113"><a href="/windows/desktop/direct3dtools/itexturecallback-resultcallback"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="f3d91-114">Callback che notifica all'host che. Il file DDS (superficie DirectDraw) contenente i risultati della richiesta associata è pronto.</span><span class="sxs-lookup"><span data-stu-id="f3d91-114">A callback that notifies the host that the .DDS (DirectDraw Surface) file containing results from the associated request are ready.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="f3d91-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3d91-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="f3d91-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f3d91-116">Header</span></span></p></td><td><span data-ttu-id="f3d91-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="f3d91-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 

---
description: L'interfaccia ISmartRenderEngine fornisce metodi che supportano la ricompressione intelligente nei servizi di modifica DirectShow (DES). Il motore di rendering intelligente espone questa interfaccia.
ms.assetid: 0e03708f-e471-4188-a212-ec5e951d20fa
title: Interfaccia ISmartRenderEngine (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e82ba73764adc27ff366533c3b5cfdc2eebc7e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327422"
---
# <a name="ismartrenderengine-interface"></a><span data-ttu-id="c4bed-104">Interfaccia ISmartRenderEngine</span><span class="sxs-lookup"><span data-stu-id="c4bed-104">ISmartRenderEngine interface</span></span>

> [!Note]  
> <span data-ttu-id="c4bed-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="c4bed-105">\[Deprecated.</span></span> <span data-ttu-id="c4bed-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c4bed-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c4bed-107">L' `ISmartRenderEngine` interfaccia fornisce metodi che supportano la ricompressione intelligente in [DirectShow editing Services](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="c4bed-107">The `ISmartRenderEngine` interface provides methods that support smart recompression in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="c4bed-108">Il motore di rendering intelligente espone questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="c4bed-108">The smart render engine exposes this interface.</span></span>

## <a name="members"></a><span data-ttu-id="c4bed-109">Membri</span><span class="sxs-lookup"><span data-stu-id="c4bed-109">Members</span></span>

<span data-ttu-id="c4bed-110">L'interfaccia **ISmartRenderEngine** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c4bed-110">The **ISmartRenderEngine** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c4bed-111">**ISmartRenderEngine** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c4bed-111">**ISmartRenderEngine** also has these types of members:</span></span>

-   [<span data-ttu-id="c4bed-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="c4bed-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c4bed-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="c4bed-113">Methods</span></span>

<span data-ttu-id="c4bed-114">L'interfaccia **ISmartRenderEngine** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="c4bed-114">The **ISmartRenderEngine** interface has these methods.</span></span>



| <span data-ttu-id="c4bed-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="c4bed-115">Method</span></span>                                                                | <span data-ttu-id="c4bed-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4bed-116">Description</span></span>                                                                          |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="c4bed-117">**GetGroupCompressor**</span><span class="sxs-lookup"><span data-stu-id="c4bed-117">**GetGroupCompressor**</span></span>](ismartrenderengine-getgroupcompressor.md)   | <span data-ttu-id="c4bed-118">Recupera il filtro di compressione per il gruppo specificato.</span><span class="sxs-lookup"><span data-stu-id="c4bed-118">Retrieves the compression filter for the specified group.</span></span><br/>                 |
| [<span data-ttu-id="c4bed-119">**SetFindCompressorCB**</span><span class="sxs-lookup"><span data-stu-id="c4bed-119">**SetFindCompressorCB**</span></span>](ismartrenderengine-setfindcompressorcb.md) | <span data-ttu-id="c4bed-120">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="c4bed-120">Not implemented.</span></span><br/>                                                          |
| [<span data-ttu-id="c4bed-121">**SetGroupCompressor**</span><span class="sxs-lookup"><span data-stu-id="c4bed-121">**SetGroupCompressor**</span></span>](ismartrenderengine-setgroupcompressor.md)   | <span data-ttu-id="c4bed-122">Specifica un filtro di compressione da usare quando si esegue il rendering del gruppo specificato.</span><span class="sxs-lookup"><span data-stu-id="c4bed-122">Specifies a compression filter to use when rendering the specified group.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c4bed-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4bed-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c4bed-124">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="c4bed-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c4bed-125">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c4bed-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c4bed-126">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c4bed-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c4bed-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4bed-127">Requirements</span></span>



| <span data-ttu-id="c4bed-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4bed-128">Requirement</span></span> | <span data-ttu-id="c4bed-129">Valore</span><span class="sxs-lookup"><span data-stu-id="c4bed-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4bed-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c4bed-130">Header</span></span><br/>  | <dl> <span data-ttu-id="c4bed-131"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4bed-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c4bed-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="c4bed-132">Library</span></span><br/> | <dl> <span data-ttu-id="c4bed-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4bed-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4bed-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4bed-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4bed-135">Rendering di un progetto</span><span class="sxs-lookup"><span data-stu-id="c4bed-135">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 

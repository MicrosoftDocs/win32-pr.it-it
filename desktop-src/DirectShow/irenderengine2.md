---
description: L'interfaccia IRenderEngine2 consente all'applicazione di sostituire il filtro di ridimensionamento video predefinito usato da DirectShow editing Services (DES). Il motore di rendering di base e il motore di rendering intelligente supportano entrambi questa interfaccia.
ms.assetid: 37603c73-e199-431a-9a1e-a40c77755c70
title: Interfaccia IRenderEngine2 (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ed7802cf3d47d745b4e4733bb1fb60c61130b44a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332572"
---
# <a name="irenderengine2-interface"></a><span data-ttu-id="507e1-104">Interfaccia IRenderEngine2</span><span class="sxs-lookup"><span data-stu-id="507e1-104">IRenderEngine2 interface</span></span>

> [!Note]  
> <span data-ttu-id="507e1-105">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="507e1-105">\[Deprecated.</span></span> <span data-ttu-id="507e1-106">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="507e1-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="507e1-107">L' `IRenderEngine2` interfaccia consente all'applicazione di sostituire il filtro di ridimensionamento video predefinito usato da DirectShow editing Services (des).</span><span class="sxs-lookup"><span data-stu-id="507e1-107">The `IRenderEngine2` interface enables the application to replace the default video resizing filter used by DirectShow Editing Services (DES).</span></span> <span data-ttu-id="507e1-108">Il [motore di rendering di base](basic-render-engine.md) e il [motore di rendering intelligente](smart-render-engine.md) supportano entrambi questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="507e1-108">The [Basic Render Engine](basic-render-engine.md) and the [Smart Render Engine](smart-render-engine.md) both support this interface.</span></span>

## <a name="members"></a><span data-ttu-id="507e1-109">Membri</span><span class="sxs-lookup"><span data-stu-id="507e1-109">Members</span></span>

<span data-ttu-id="507e1-110">L'interfaccia **IRenderEngine2** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="507e1-110">The **IRenderEngine2** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="507e1-111">**IRenderEngine2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="507e1-111">**IRenderEngine2** also has these types of members:</span></span>

-   [<span data-ttu-id="507e1-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="507e1-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="507e1-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="507e1-113">Methods</span></span>

<span data-ttu-id="507e1-114">L'interfaccia **IRenderEngine2** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="507e1-114">The **IRenderEngine2** interface has these methods.</span></span>



| <span data-ttu-id="507e1-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="507e1-115">Method</span></span>                                                  | <span data-ttu-id="507e1-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="507e1-116">Description</span></span>                                                                             |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="507e1-117">**SetResizerGUID**</span><span class="sxs-lookup"><span data-stu-id="507e1-117">**SetResizerGUID**</span></span>](irenderengine2-setresizerguid.md) | <span data-ttu-id="507e1-118">Specifica il CLSID di un filtro di ridimensionamento personalizzato fornito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="507e1-118">Specifies the CLSID of a custom resizing filter provided by the application.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="507e1-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="507e1-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="507e1-120">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="507e1-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="507e1-121">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="507e1-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="507e1-122">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="507e1-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="507e1-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="507e1-123">Requirements</span></span>



| <span data-ttu-id="507e1-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="507e1-124">Requirement</span></span> | <span data-ttu-id="507e1-125">Valore</span><span class="sxs-lookup"><span data-stu-id="507e1-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="507e1-126">Versione</span><span class="sxs-lookup"><span data-stu-id="507e1-126">Version</span></span><br/> | <span data-ttu-id="507e1-127">DirectX 9,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="507e1-127">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="507e1-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="507e1-128">Header</span></span><br/>  | <dl> <span data-ttu-id="507e1-129"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="507e1-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="507e1-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="507e1-130">Library</span></span><br/> | <dl> <span data-ttu-id="507e1-131"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="507e1-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="507e1-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="507e1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="507e1-133">Creazione di una ridisposizione video personalizzata</span><span class="sxs-lookup"><span data-stu-id="507e1-133">Providing a Custom Video Resizer</span></span>](providing-a-custom-video-resizer.md)
</dt> </dl>

 

 

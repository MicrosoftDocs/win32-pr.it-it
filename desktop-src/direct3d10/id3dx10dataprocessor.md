---
description: Oggetto di elaborazione dati utilizzato dall'interfaccia ID3DX10ThreadPump per l'elaborazione asincrona dei dati caricati.
ms.assetid: c932f558-10da-45fc-a833-8ed86fa065ab
title: Interfaccia ID3DX10DataProcessor (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: de573e50a1442396df78dd6a3c8f0bd09c1cbf6d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886334"
---
# <a name="id3dx10dataprocessor-interface"></a><span data-ttu-id="d5455-103">Interfaccia ID3DX10DataProcessor</span><span class="sxs-lookup"><span data-stu-id="d5455-103">ID3DX10DataProcessor interface</span></span>

<span data-ttu-id="d5455-104">Oggetto di elaborazione dati utilizzato dall' [**interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md) per l'elaborazione asincrona dei dati caricati.</span><span class="sxs-lookup"><span data-stu-id="d5455-104">Data processing object used by [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) for processing loaded data asynchronously.</span></span>

## <a name="members"></a><span data-ttu-id="d5455-105">Membri</span><span class="sxs-lookup"><span data-stu-id="d5455-105">Members</span></span>

<span data-ttu-id="d5455-106">L'interfaccia **ID3DX10DataProcessor** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d5455-106">The **ID3DX10DataProcessor** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d5455-107">**ID3DX10DataProcessor** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d5455-107">**ID3DX10DataProcessor** also has these types of members:</span></span>

-   [<span data-ttu-id="d5455-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="d5455-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d5455-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="d5455-109">Methods</span></span>

<span data-ttu-id="d5455-110">L'interfaccia **ID3DX10DataProcessor** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="d5455-110">The **ID3DX10DataProcessor** interface has these methods.</span></span>



| <span data-ttu-id="d5455-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="d5455-111">Method</span></span>                                                                | <span data-ttu-id="d5455-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5455-112">Description</span></span>                                                                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5455-113">**CreateDeviceObject**</span><span class="sxs-lookup"><span data-stu-id="d5455-113">**CreateDeviceObject**</span></span>](id3dx10dataprocessor-createdeviceobject.md) | <span data-ttu-id="d5455-114">Creare un oggetto dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d5455-114">Create a device object.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="d5455-115">**Eliminare**</span><span class="sxs-lookup"><span data-stu-id="d5455-115">**Destroy**</span></span>](id3dx10dataprocessor-destroy.md)                       | <span data-ttu-id="d5455-116">Usato da un' [**interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md) per eliminare il processore dopo il completamento di un elemento di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d5455-116">Used by a [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) to destroy the processor after a work item completes.</span></span><br/> |
| [<span data-ttu-id="d5455-117">**Processo**</span><span class="sxs-lookup"><span data-stu-id="d5455-117">**Process**</span></span>](id3dx10dataprocessor-process.md)                       | <span data-ttu-id="d5455-118">Elaborare alcuni dati.</span><span class="sxs-lookup"><span data-stu-id="d5455-118">Process some data.</span></span><br/>                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="d5455-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5455-119">Remarks</span></span>

<span data-ttu-id="d5455-120">Questo oggetto può essere ereditato e i relativi membri ridefiniti.</span><span class="sxs-lookup"><span data-stu-id="d5455-120">This object can be inherited and its members redefined.</span></span> <span data-ttu-id="d5455-121">Questa operazione consente di personalizzare l'API per l'elaborazione di formati di file personalizzati.</span><span class="sxs-lookup"><span data-stu-id="d5455-121">Doing so would enable you to customize the API for processing your own custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5455-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5455-122">Requirements</span></span>



| <span data-ttu-id="d5455-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5455-123">Requirement</span></span> | <span data-ttu-id="d5455-124">Valore</span><span class="sxs-lookup"><span data-stu-id="d5455-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5455-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d5455-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d5455-126"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5455-126"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="d5455-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="d5455-127">Library</span></span><br/> | <dl> <span data-ttu-id="d5455-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5455-128"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5455-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5455-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5455-130">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="d5455-130">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

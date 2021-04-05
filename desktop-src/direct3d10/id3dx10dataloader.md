---
description: Oggetto caricamento dati utilizzato dall'interfaccia ID3DX10ThreadPump per il caricamento asincrono dei dati.
ms.assetid: bda2414c-bbab-47ac-b23a-f58fb86e732d
title: Interfaccia ID3DX10DataLoader (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataLoader
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b0e45d24d663f0ba9a8978bc251a4adf0c7868fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969368"
---
# <a name="id3dx10dataloader-interface"></a><span data-ttu-id="317e1-103">Interfaccia ID3DX10DataLoader</span><span class="sxs-lookup"><span data-stu-id="317e1-103">ID3DX10DataLoader interface</span></span>

<span data-ttu-id="317e1-104">Oggetto caricamento dati utilizzato dall' [**interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md) per il caricamento asincrono dei dati.</span><span class="sxs-lookup"><span data-stu-id="317e1-104">Data loading object used by [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) for loading data asynchronously.</span></span>

## <a name="members"></a><span data-ttu-id="317e1-105">Membri</span><span class="sxs-lookup"><span data-stu-id="317e1-105">Members</span></span>

<span data-ttu-id="317e1-106">L'interfaccia **ID3DX10DataLoader** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="317e1-106">The **ID3DX10DataLoader** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="317e1-107">**ID3DX10DataLoader** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="317e1-107">**ID3DX10DataLoader** also has these types of members:</span></span>

-   [<span data-ttu-id="317e1-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="317e1-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="317e1-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="317e1-109">Methods</span></span>

<span data-ttu-id="317e1-110">L'interfaccia **ID3DX10DataLoader** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="317e1-110">The **ID3DX10DataLoader** interface has these methods.</span></span>



| <span data-ttu-id="317e1-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="317e1-111">Method</span></span>                                             | <span data-ttu-id="317e1-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="317e1-112">Description</span></span>                                                                                                                                                                                                                        |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="317e1-113">**Decomprimere**</span><span class="sxs-lookup"><span data-stu-id="317e1-113">**Decompress**</span></span>](id3dx10dataloader-decompress.md) | <span data-ttu-id="317e1-114">Utilizzato per decomprimere i dati codificati.</span><span class="sxs-lookup"><span data-stu-id="317e1-114">Used to decompress encoded data.</span></span> <span data-ttu-id="317e1-115">Questa operazione viene in genere utilizzata per caricare le risorse da file System, ad esempio file ZIP.</span><span class="sxs-lookup"><span data-stu-id="317e1-115">Typically this would be used to load resources from file systems, such as ZIP files.</span></span> <span data-ttu-id="317e1-116">Quando si esegue il caricamento da una risorsa non compressa, la fase di decompressione non deve eseguire alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="317e1-116">When loading from an uncompressed resource, the decompression stage does not have to do any work.</span></span><br/> |
| [<span data-ttu-id="317e1-117">**Eliminare**</span><span class="sxs-lookup"><span data-stu-id="317e1-117">**Destroy**</span></span>](id3dx10dataloader-destroy.md)       | <span data-ttu-id="317e1-118">Usato da un' [**interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md) per eliminare il caricatore dopo il completamento di un elemento di lavoro.</span><span class="sxs-lookup"><span data-stu-id="317e1-118">Used by a [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) to destroy the loader after a work item completes.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="317e1-119">**Caricamento**</span><span class="sxs-lookup"><span data-stu-id="317e1-119">**Load**</span></span>](id3dx10dataloader-load.md)             | <span data-ttu-id="317e1-120">Usato da un' [**interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md) per caricare i dati da un disco.</span><span class="sxs-lookup"><span data-stu-id="317e1-120">Used by a [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md) to load data from a disk.</span></span><br/>                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="317e1-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="317e1-121">Remarks</span></span>

<span data-ttu-id="317e1-122">Questo oggetto può essere ereditato e i relativi membri ridefiniti.</span><span class="sxs-lookup"><span data-stu-id="317e1-122">This object can be inherited and its members redefined.</span></span> <span data-ttu-id="317e1-123">Questa operazione consente di personalizzare l'API per il caricamento e la decompressione dei formati di file personalizzati.</span><span class="sxs-lookup"><span data-stu-id="317e1-123">Doing so would enable you to customize the API for loading and decompressing your own custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="317e1-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="317e1-124">Requirements</span></span>



| <span data-ttu-id="317e1-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="317e1-125">Requirement</span></span> | <span data-ttu-id="317e1-126">Valore</span><span class="sxs-lookup"><span data-stu-id="317e1-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="317e1-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="317e1-127">Header</span></span><br/>  | <dl> <span data-ttu-id="317e1-128"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="317e1-128"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="317e1-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="317e1-129">Library</span></span><br/> | <dl> <span data-ttu-id="317e1-130"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="317e1-130"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="317e1-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="317e1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="317e1-132">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="317e1-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

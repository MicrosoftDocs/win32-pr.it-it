---
description: Un'applicazione utilizza i metodi di questa interfaccia per implementare un set di animazioni del fotogramma chiave archiviato in un formato dati compresso.
ms.assetid: 858f09b7-c3b6-4e22-8017-ce2d6188ba80
title: Interfaccia ID3DXCompressedAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 33dd1017859be14924d8d40265696cfb552754ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322831"
---
# <a name="id3dxcompressedanimationset-interface"></a><span data-ttu-id="94925-103">Interfaccia ID3DXCompressedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="94925-103">ID3DXCompressedAnimationSet interface</span></span>

<span data-ttu-id="94925-104">Un'applicazione utilizza i metodi di questa interfaccia per implementare un set di animazioni del fotogramma chiave archiviato in un formato dati compresso.</span><span class="sxs-lookup"><span data-stu-id="94925-104">An application uses the methods of this interface to implement a key frame animation set stored in a compressed data format.</span></span>

## <a name="members"></a><span data-ttu-id="94925-105">Membri</span><span class="sxs-lookup"><span data-stu-id="94925-105">Members</span></span>

<span data-ttu-id="94925-106">L'interfaccia **ID3DXCompressedAnimationSet** eredita da [**ID3DXAnimationSet**](id3dxanimationset.md).</span><span class="sxs-lookup"><span data-stu-id="94925-106">The **ID3DXCompressedAnimationSet** interface inherits from [**ID3DXAnimationSet**](id3dxanimationset.md).</span></span> <span data-ttu-id="94925-107">**ID3DXCompressedAnimationSet** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="94925-107">**ID3DXCompressedAnimationSet** also has these types of members:</span></span>

-   [<span data-ttu-id="94925-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="94925-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="94925-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="94925-109">Methods</span></span>

<span data-ttu-id="94925-110">L'interfaccia **ID3DXCompressedAnimationSet** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="94925-110">The **ID3DXCompressedAnimationSet** interface has these methods.</span></span>



| <span data-ttu-id="94925-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="94925-111">Method</span></span>                                                                                  | <span data-ttu-id="94925-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94925-112">Description</span></span>                                                                      |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="94925-113">**GetCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="94925-113">**GetCallbackKeys**</span></span>](id3dxcompressedanimationset--getcallbackkeys.md)                 | <span data-ttu-id="94925-114">Compila una matrice con i dati della chiave di callback utilizzati per l'animazione del fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="94925-114">Fills an array with callback key data used for key frame animation.</span></span><br/>   |
| [<span data-ttu-id="94925-115">**GetCompressedData**</span><span class="sxs-lookup"><span data-stu-id="94925-115">**GetCompressedData**</span></span>](id3dxcompressedanimationset--getcompresseddata.md)             | <span data-ttu-id="94925-116">Ottiene il buffer di dati che archivia i dati di animazione del fotogramma chiave compressi.</span><span class="sxs-lookup"><span data-stu-id="94925-116">Gets the data buffer that stores compressed key frame animation data.</span></span><br/> |
| [<span data-ttu-id="94925-117">**GetNumCallbackKeys**</span><span class="sxs-lookup"><span data-stu-id="94925-117">**GetNumCallbackKeys**</span></span>](id3dxcompressedanimationset--getnumcallbackkeys.md)           | <span data-ttu-id="94925-118">Ottiene il numero di chiavi di callback nel set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="94925-118">Gets the number of callback keys in the animation set.</span></span><br/>                |
| [<span data-ttu-id="94925-119">**GetPlaybackType**</span><span class="sxs-lookup"><span data-stu-id="94925-119">**GetPlaybackType**</span></span>](id3dxcompressedanimationset--getplaybacktype.md)                 | <span data-ttu-id="94925-120">Ottiene il tipo del ciclo di riproduzione del set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="94925-120">Gets the type of the animation set playback loop.</span></span><br/>                     |
| [<span data-ttu-id="94925-121">**GetSourceTicksPerSecond**</span><span class="sxs-lookup"><span data-stu-id="94925-121">**GetSourceTicksPerSecond**</span></span>](id3dxcompressedanimationset--getsourcetickspersecond.md) | <span data-ttu-id="94925-122">Ottiene il numero di cicli del fotogramma chiave di animazione che si verificano al secondo.</span><span class="sxs-lookup"><span data-stu-id="94925-122">Gets the number of animation key frame ticks that occur per second.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="94925-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="94925-123">Remarks</span></span>

<span data-ttu-id="94925-124">Creare un set di animazioni con fotogrammi chiave in formato compresso con [**D3DXCreateCompressedAnimationSet**](d3dxcreatecompressedanimationset.md).</span><span class="sxs-lookup"><span data-stu-id="94925-124">Create a compressed-format key frame animation set with [**D3DXCreateCompressedAnimationSet**](d3dxcreatecompressedanimationset.md).</span></span>

<span data-ttu-id="94925-125">Il tipo LPD3DXCOMPRESSEDANIMATIONSET è definito come puntatore a questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="94925-125">The LPD3DXCOMPRESSEDANIMATIONSET type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXCompressedAnimationSet ID3DXCompressedAnimationSet;
typedef interface ID3DXCompressedAnimationSet *LPD3DXCOMPRESSEDANIMATIONSET;
```



## <a name="requirements"></a><span data-ttu-id="94925-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94925-126">Requirements</span></span>



| <span data-ttu-id="94925-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="94925-127">Requirement</span></span> | <span data-ttu-id="94925-128">Valore</span><span class="sxs-lookup"><span data-stu-id="94925-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="94925-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="94925-129">Header</span></span><br/>  | <dl> <span data-ttu-id="94925-130"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="94925-130"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="94925-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="94925-131">Library</span></span><br/> | <dl> <span data-ttu-id="94925-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="94925-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="94925-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="94925-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94925-134">**ID3DXAnimationSet**</span><span class="sxs-lookup"><span data-stu-id="94925-134">**ID3DXAnimationSet**</span></span>](id3dxanimationset.md)
</dt> <dt>

[<span data-ttu-id="94925-135">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="94925-135">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 





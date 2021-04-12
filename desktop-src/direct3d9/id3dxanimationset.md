---
description: Questa interfaccia incapsula le funzionalità minime necessarie per un'animazione impostata da un controller di animazione.
ms.assetid: vs|directx_sdk|~\id3dxanimationset.htm
title: Interfaccia ID3DXAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b5aa27494931e8b6c528627fa8e96278a6d86b05
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235201"
---
# <a name="id3dxanimationset-interface"></a><span data-ttu-id="24cdb-103">Interfaccia ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="24cdb-103">ID3DXAnimationSet interface</span></span>

<span data-ttu-id="24cdb-104">Questa interfaccia incapsula le funzionalità minime necessarie per un'animazione impostata da un controller di animazione.</span><span class="sxs-lookup"><span data-stu-id="24cdb-104">This interface encapsulates the minimum functionality required of an animation set by an animation controller.</span></span> <span data-ttu-id="24cdb-105">Gli utenti avanzati potrebbero voler implementare questa interfaccia per soddisfare le proprie esigenze specializzate; per la maggior parte degli utenti, tuttavia, devono essere sufficienti le interfacce [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) e [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) derivate.</span><span class="sxs-lookup"><span data-stu-id="24cdb-105">Advanced users might want to implement this interface themselves to suit their specialized needs; for most users, however, the derived [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) and [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) interfaces should suffice.</span></span>

## <a name="members"></a><span data-ttu-id="24cdb-106">Membri</span><span class="sxs-lookup"><span data-stu-id="24cdb-106">Members</span></span>

<span data-ttu-id="24cdb-107">L'interfaccia **ID3DXAnimationSet** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="24cdb-107">The **ID3DXAnimationSet** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="24cdb-108">**ID3DXAnimationSet** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="24cdb-108">**ID3DXAnimationSet** also has these types of members:</span></span>

-   [<span data-ttu-id="24cdb-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="24cdb-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="24cdb-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="24cdb-110">Methods</span></span>

<span data-ttu-id="24cdb-111">L'interfaccia **ID3DXAnimationSet** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="24cdb-111">The **ID3DXAnimationSet** interface has these methods.</span></span>



| <span data-ttu-id="24cdb-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="24cdb-112">Method</span></span>                                                                        | <span data-ttu-id="24cdb-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24cdb-113">Description</span></span>                                                                       |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="24cdb-114">**GetAnimationIndexByName**</span><span class="sxs-lookup"><span data-stu-id="24cdb-114">**GetAnimationIndexByName**</span></span>](id3dxanimationset--getanimationindexbyname.md) | <span data-ttu-id="24cdb-115">Ottiene l'indice di un'animazione, dato il relativo nome.</span><span class="sxs-lookup"><span data-stu-id="24cdb-115">Gets the index of an animation, given its name.</span></span><br/>                        |
| [<span data-ttu-id="24cdb-116">**GetAnimationNameByIndex**</span><span class="sxs-lookup"><span data-stu-id="24cdb-116">**GetAnimationNameByIndex**</span></span>](id3dxanimationset--getanimationnamebyindex.md) | <span data-ttu-id="24cdb-117">Ottiene il nome di un'animazione, dato il relativo indice.</span><span class="sxs-lookup"><span data-stu-id="24cdb-117">Gets the name of an animation, given its index.</span></span><br/>                        |
| [<span data-ttu-id="24cdb-118">**GetCallback**</span><span class="sxs-lookup"><span data-stu-id="24cdb-118">**GetCallback**</span></span>](id3dxanimationset--getcallback.md)                         | <span data-ttu-id="24cdb-119">Ottiene informazioni su un callback specifico nel set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="24cdb-119">Gets information about a specific callback in the animation set.</span></span><br/>       |
| [<span data-ttu-id="24cdb-120">**GetName**</span><span class="sxs-lookup"><span data-stu-id="24cdb-120">**GetName**</span></span>](id3dxanimationset--getname.md)                                 | <span data-ttu-id="24cdb-121">Ottiene il nome del set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="24cdb-121">Gets the animation set name.</span></span><br/>                                           |
| [<span data-ttu-id="24cdb-122">**GetNumAnimations**</span><span class="sxs-lookup"><span data-stu-id="24cdb-122">**GetNumAnimations**</span></span>](id3dxanimationset--getnumanimations.md)               | <span data-ttu-id="24cdb-123">Ottiene il numero di animazioni nel set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="24cdb-123">Gets the number of animations in the animation set.</span></span><br/>                    |
| [<span data-ttu-id="24cdb-124">**GetPeriod**</span><span class="sxs-lookup"><span data-stu-id="24cdb-124">**GetPeriod**</span></span>](id3dxanimationset--getperiod.md)                             | <span data-ttu-id="24cdb-125">Ottiene il periodo del set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="24cdb-125">Gets the period of the animation set.</span></span><br/>                                  |
| [<span data-ttu-id="24cdb-126">**GetPeriodicPosition**</span><span class="sxs-lookup"><span data-stu-id="24cdb-126">**GetPeriodicPosition**</span></span>](id3dxanimationset--getperiodicposition.md)         | <span data-ttu-id="24cdb-127">Restituisce la posizione dell'ora nell'intervallo di tempo locale di un set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="24cdb-127">Returns time position in the local timeframe of an animation set.</span></span><br/>      |
| [<span data-ttu-id="24cdb-128">**GetSRT**</span><span class="sxs-lookup"><span data-stu-id="24cdb-128">**GetSRT**</span></span>](id3dxanimationset--getsrt.md)                                   | <span data-ttu-id="24cdb-129">Ottiene i valori di scala, rotazione e traslazione del set di animazioni.</span><span class="sxs-lookup"><span data-stu-id="24cdb-129">Gets the scale, rotation, and translation values of the animation set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="24cdb-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="24cdb-130">Remarks</span></span>

<span data-ttu-id="24cdb-131">Un set di animazioni è costituito da animazioni per molti nodi per la stessa animazione.</span><span class="sxs-lookup"><span data-stu-id="24cdb-131">An animation set consists of animations for many nodes for the same animation.</span></span>

<span data-ttu-id="24cdb-132">Il tipo LPD3DXANIMATIONSET è definito come puntatore a questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="24cdb-132">The LPD3DXANIMATIONSET type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXAnimationSet ID3DXAnimationSet;
typedef interface ID3DXAnimationSet *LPD3DXANIMATIONSET;
```



## <a name="requirements"></a><span data-ttu-id="24cdb-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24cdb-133">Requirements</span></span>



| <span data-ttu-id="24cdb-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="24cdb-134">Requirement</span></span> | <span data-ttu-id="24cdb-135">Valore</span><span class="sxs-lookup"><span data-stu-id="24cdb-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="24cdb-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="24cdb-136">Header</span></span><br/>  | <dl> <span data-ttu-id="24cdb-137"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="24cdb-137"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="24cdb-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="24cdb-138">Library</span></span><br/> | <dl> <span data-ttu-id="24cdb-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="24cdb-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="24cdb-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24cdb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24cdb-141">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="24cdb-141">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 

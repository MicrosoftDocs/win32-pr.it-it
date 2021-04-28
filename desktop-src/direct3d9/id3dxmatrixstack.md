---
description: "Interfaccia ID3DXMATRIXStack: le applicazioni usano i metodi dell'interfaccia ID3DXMATRIXStack per modificare uno stack di matrici."
ms.assetid: 4d382d39-a9da-4a3b-b7b6-d6890357d467
title: Interfaccia ID3DXMATRIXStack (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 62681c468fa7e78e6fd08c458798d98b467b992e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093319"
---
# <a name="id3dxmatrixstack-interface"></a><span data-ttu-id="ac7af-103">Interfaccia ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="ac7af-103">ID3DXMATRIXStack interface</span></span>

<span data-ttu-id="ac7af-104">Le applicazioni usano i metodi dell'interfaccia ID3DXMATRIXStack per modificare uno stack di matrici.</span><span class="sxs-lookup"><span data-stu-id="ac7af-104">Applications use the methods of the ID3DXMATRIXStack interface to manipulate a matrix stack.</span></span>

## <a name="members"></a><span data-ttu-id="ac7af-105">Membri</span><span class="sxs-lookup"><span data-stu-id="ac7af-105">Members</span></span>

<span data-ttu-id="ac7af-106">**L'interfaccia ID3DXMATRIXStack** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="ac7af-106">The **ID3DXMATRIXStack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ac7af-107">**ID3DXMATRIXStack** include anche questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ac7af-107">**ID3DXMATRIXStack** also has these types of members:</span></span>

-   [<span data-ttu-id="ac7af-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="ac7af-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ac7af-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="ac7af-109">Methods</span></span>

<span data-ttu-id="ac7af-110">**L'interfaccia ID3DXMATRIXStack** include questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ac7af-110">The **ID3DXMATRIXStack** interface has these methods.</span></span>



| <span data-ttu-id="ac7af-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="ac7af-111">Method</span></span>                                                                       | <span data-ttu-id="ac7af-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ac7af-112">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ac7af-113">**GetTop**</span><span class="sxs-lookup"><span data-stu-id="ac7af-113">**GetTop**</span></span>](id3dxmatrixstack--gettop.md)                                   | <span data-ttu-id="ac7af-114">Recupera la matrice corrente all'inizio dello stack.</span><span class="sxs-lookup"><span data-stu-id="ac7af-114">Retrieves the current matrix at the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="ac7af-115">**LoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="ac7af-115">**LoadIdentity**</span></span>](id3dxmatrixstack--loadidentity.md)                       | <span data-ttu-id="ac7af-116">Carica l'identità nella matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="ac7af-116">Loads identity in the current matrix.</span></span><br/>                                                                                           |
| [<span data-ttu-id="ac7af-117">**LoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="ac7af-117">**LoadMatrix**</span></span>](id3dxmatrixstack--loadmatrix.md)                           | <span data-ttu-id="ac7af-118">Carica la matrice specificata nella matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="ac7af-118">Loads the given matrix into the current matrix.</span></span><br/>                                                                                 |
| [<span data-ttu-id="ac7af-119">**MultMatrix**</span><span class="sxs-lookup"><span data-stu-id="ac7af-119">**MultMatrix**</span></span>](id3dxmatrixstack--multmatrix.md)                           | <span data-ttu-id="ac7af-120">Determina il prodotto della matrice corrente e della matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="ac7af-120">Determines the product of the current matrix and the given matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="ac7af-121">**MultMatrixLocal**</span><span class="sxs-lookup"><span data-stu-id="ac7af-121">**MultMatrixLocal**</span></span>](id3dxmatrixstack--multmatrixlocal.md)                 | <span data-ttu-id="ac7af-122">Determina il prodotto della matrice specificata e la matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="ac7af-122">Determines the product of the given matrix and the current matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="ac7af-123">**Pop**</span><span class="sxs-lookup"><span data-stu-id="ac7af-123">**Pop**</span></span>](id3dxmatrixstack--pop.md)                                         | <span data-ttu-id="ac7af-124">Rimuove la matrice corrente dall'inizio dello stack.</span><span class="sxs-lookup"><span data-stu-id="ac7af-124">Removes the current matrix from the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="ac7af-125">**Spingere**</span><span class="sxs-lookup"><span data-stu-id="ac7af-125">**Push**</span></span>](id3dxmatrixstack--push.md)                                       | <span data-ttu-id="ac7af-126">Aggiunge una matrice nello stack.</span><span class="sxs-lookup"><span data-stu-id="ac7af-126">Adds a matrix to the stack.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="ac7af-127">**RotateAxis**</span><span class="sxs-lookup"><span data-stu-id="ac7af-127">**RotateAxis**</span></span>](id3dxmatrixstack--rotateaxis.md)                           | <span data-ttu-id="ac7af-128">Ruota (rispetto allo spazio delle coordinate del mondo) intorno a un asse arbitrario.</span><span class="sxs-lookup"><span data-stu-id="ac7af-128">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="ac7af-129">**RotateAxisLocal**</span><span class="sxs-lookup"><span data-stu-id="ac7af-129">**RotateAxisLocal**</span></span>](id3dxmatrixstack--rotateaxislocal.md)                 | <span data-ttu-id="ac7af-130">Ruota (rispetto allo spazio delle coordinate locale dell'oggetto) intorno a un asse arbitrario.</span><span class="sxs-lookup"><span data-stu-id="ac7af-130">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="ac7af-131">**RotateYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="ac7af-131">**RotateYawPitchRoll**</span></span>](id3dxmatrixstack--rotateyawpitchroll.md)           | <span data-ttu-id="ac7af-132">Ruota (rispetto allo spazio delle coordinate del mondo) intorno a un asse arbitrario.</span><span class="sxs-lookup"><span data-stu-id="ac7af-132">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="ac7af-133">**RotateYawPitchRollLocal**</span><span class="sxs-lookup"><span data-stu-id="ac7af-133">**RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack--rotateyawpitchrolllocal.md) | <span data-ttu-id="ac7af-134">Ruota (rispetto allo spazio delle coordinate locale dell'oggetto) intorno a un asse arbitrario.</span><span class="sxs-lookup"><span data-stu-id="ac7af-134">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="ac7af-135">**Scalabilità**</span><span class="sxs-lookup"><span data-stu-id="ac7af-135">**Scale**</span></span>](id3dxmatrixstack--scale.md)                                     | <span data-ttu-id="ac7af-136">Ridimensionare la matrice corrente sull'origine delle coordinate del mondo.</span><span class="sxs-lookup"><span data-stu-id="ac7af-136">Scale the current matrix about the world coordinate origin.</span></span><br/>                                                                     |
| [<span data-ttu-id="ac7af-137">**ScaleLocal**</span><span class="sxs-lookup"><span data-stu-id="ac7af-137">**ScaleLocal**</span></span>](id3dxmatrixstack--scalelocal.md)                           | <span data-ttu-id="ac7af-138">Ridimensionare la matrice corrente sull'origine dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ac7af-138">Scale the current matrix about the object origin.</span></span><br/>                                                                               |
| [<span data-ttu-id="ac7af-139">**Traduci**</span><span class="sxs-lookup"><span data-stu-id="ac7af-139">**Translate**</span></span>](id3dxmatrixstack--translate.md)                             | <span data-ttu-id="ac7af-140">Determina il prodotto della matrice corrente e la matrice di traslazione calcolata determinata dai fattori (x, y e z) specifici.</span><span class="sxs-lookup"><span data-stu-id="ac7af-140">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span><br/> |
| [<span data-ttu-id="ac7af-141">**TranslateLocal**</span><span class="sxs-lookup"><span data-stu-id="ac7af-141">**TranslateLocal**</span></span>](id3dxmatrixstack--translatelocal.md)                   | <span data-ttu-id="ac7af-142">Determina il prodotto della matrice di traslazione calcolata determinata dai fattori (x, y e z) e dalla matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="ac7af-142">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ac7af-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="ac7af-143">Remarks</span></span>

<span data-ttu-id="ac7af-144">**L'interfaccia ID3DXMATRIXStack** viene ottenuta chiamando la [**funzione D3DXCreateMatrixStack.**](d3dxcreatematrixstack.md)</span><span class="sxs-lookup"><span data-stu-id="ac7af-144">The **ID3DXMATRIXStack** interface is obtained by calling the [**D3DXCreateMatrixStack**](d3dxcreatematrixstack.md) function.</span></span>

<span data-ttu-id="ac7af-145">Il tipo LPD3DXMATRIXSTACK è definito come puntatore **all'interfaccia ID3DXMATRIXStack.**</span><span class="sxs-lookup"><span data-stu-id="ac7af-145">The LPD3DXMATRIXSTACK type is defined as a pointer to the **ID3DXMATRIXStack** interface.</span></span>


```
typedef interface ID3DXMATRIXStack ID3DXMATRIXStack;
typedef interface ID3DXMATRIXStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a><span data-ttu-id="ac7af-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac7af-146">Requirements</span></span>



| <span data-ttu-id="ac7af-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac7af-147">Requirement</span></span> | <span data-ttu-id="ac7af-148">Valore</span><span class="sxs-lookup"><span data-stu-id="ac7af-148">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac7af-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ac7af-149">Header</span></span><br/>  | <dl> <span data-ttu-id="ac7af-150"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="ac7af-150"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="ac7af-151">Libreria</span><span class="sxs-lookup"><span data-stu-id="ac7af-151">Library</span></span><br/> | <dl> <span data-ttu-id="ac7af-152"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac7af-152"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ac7af-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ac7af-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac7af-154">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="ac7af-154">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 

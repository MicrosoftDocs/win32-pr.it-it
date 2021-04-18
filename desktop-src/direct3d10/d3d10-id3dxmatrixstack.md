---
description: Le applicazioni utilizzano i metodi dell'interfaccia ID3DXMATRIXStack per modificare uno stack di matrici.
ms.assetid: 6c76f9e0-5f59-4cf3-b34a-2475536af6c7
title: Interfaccia ID3DXMatrixStack (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMatrixStack
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3d6956a6764683378c732c4ed859bfa13e537422
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355639"
---
# <a name="id3dxmatrixstack-interface"></a><span data-ttu-id="f31bf-103">Interfaccia ID3DXMatrixStack</span><span class="sxs-lookup"><span data-stu-id="f31bf-103">ID3DXMatrixStack interface</span></span>

<span data-ttu-id="f31bf-104">Le applicazioni utilizzano i metodi dell'interfaccia ID3DXMATRIXStack per modificare uno stack di matrici.</span><span class="sxs-lookup"><span data-stu-id="f31bf-104">Applications use the methods of the ID3DXMATRIXStack interface to manipulate a matrix stack.</span></span>

## <a name="members"></a><span data-ttu-id="f31bf-105">Membri</span><span class="sxs-lookup"><span data-stu-id="f31bf-105">Members</span></span>

<span data-ttu-id="f31bf-106">L'interfaccia **ID3DXMatrixStack** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f31bf-106">The **ID3DXMatrixStack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f31bf-107">**ID3DXMatrixStack** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f31bf-107">**ID3DXMatrixStack** also has these types of members:</span></span>

-   [<span data-ttu-id="f31bf-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="f31bf-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f31bf-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="f31bf-109">Methods</span></span>

<span data-ttu-id="f31bf-110">L'interfaccia **ID3DXMatrixStack** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f31bf-110">The **ID3DXMatrixStack** interface has these methods.</span></span>



| <span data-ttu-id="f31bf-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="f31bf-111">Method</span></span>                                                                      | <span data-ttu-id="f31bf-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f31bf-112">Description</span></span>                                                                                                                                |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f31bf-113">**GetTop**</span><span class="sxs-lookup"><span data-stu-id="f31bf-113">**GetTop**</span></span>](id3dxmatrixstack-gettop.md)                                   | <span data-ttu-id="f31bf-114">Recupera la matrice corrente all'inizio dello stack.</span><span class="sxs-lookup"><span data-stu-id="f31bf-114">Retrieves the current matrix at the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="f31bf-115">**LoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="f31bf-115">**LoadIdentity**</span></span>](id3dxmatrixstack-loadidentity.md)                       | <span data-ttu-id="f31bf-116">Carica l'identità nella matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="f31bf-116">Loads identity in the current matrix.</span></span><br/>                                                                                           |
| [<span data-ttu-id="f31bf-117">**LoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="f31bf-117">**LoadMatrix**</span></span>](id3dxmatrixstack-loadmatrix.md)                           | <span data-ttu-id="f31bf-118">Carica la matrice specificata nella matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="f31bf-118">Loads the given matrix into the current matrix.</span></span><br/>                                                                                 |
| [<span data-ttu-id="f31bf-119">**MultMatrix**</span><span class="sxs-lookup"><span data-stu-id="f31bf-119">**MultMatrix**</span></span>](id3dxmatrixstack-multmatrix.md)                           | <span data-ttu-id="f31bf-120">Determina il prodotto della matrice corrente e della matrice specificata.</span><span class="sxs-lookup"><span data-stu-id="f31bf-120">Determines the product of the current matrix and the given matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="f31bf-121">**MultMatrixLocal**</span><span class="sxs-lookup"><span data-stu-id="f31bf-121">**MultMatrixLocal**</span></span>](id3dxmatrixstack-multmatrixlocal.md)                 | <span data-ttu-id="f31bf-122">Determina il prodotto della matrice specificata e della matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="f31bf-122">Determines the product of the given matrix and the current matrix.</span></span><br/>                                                              |
| [<span data-ttu-id="f31bf-123">**Popup**</span><span class="sxs-lookup"><span data-stu-id="f31bf-123">**Pop**</span></span>](id3dxmatrixstack-pop.md)                                         | <span data-ttu-id="f31bf-124">Rimuove la matrice corrente dall'inizio dello stack.</span><span class="sxs-lookup"><span data-stu-id="f31bf-124">Removes the current matrix from the top of the stack.</span></span><br/>                                                                           |
| [<span data-ttu-id="f31bf-125">**Spingere**</span><span class="sxs-lookup"><span data-stu-id="f31bf-125">**Push**</span></span>](id3dxmatrixstack-push.md)                                       | <span data-ttu-id="f31bf-126">Aggiunge una matrice allo stack.</span><span class="sxs-lookup"><span data-stu-id="f31bf-126">Adds a matrix to the stack.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="f31bf-127">**RotateAxis**</span><span class="sxs-lookup"><span data-stu-id="f31bf-127">**RotateAxis**</span></span>](id3dxmatrixstack-rotateaxis.md)                           | <span data-ttu-id="f31bf-128">Ruota (rispetto allo spazio delle coordinate globali) intorno a un asse arbitrario.</span><span class="sxs-lookup"><span data-stu-id="f31bf-128">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="f31bf-129">**RotateAxisLocal**</span><span class="sxs-lookup"><span data-stu-id="f31bf-129">**RotateAxisLocal**</span></span>](id3dxmatrixstack-rotateaxislocal.md)                 | <span data-ttu-id="f31bf-130">Ruota (relativo allo spazio delle coordinate locali dell'oggetto) intorno a un asse arbitrario.</span><span class="sxs-lookup"><span data-stu-id="f31bf-130">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="f31bf-131">**RotateYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="f31bf-131">**RotateYawPitchRoll**</span></span>](id3dxmatrixstack-rotateyawpitchroll.md)           | <span data-ttu-id="f31bf-132">Ruota (rispetto allo spazio delle coordinate globali) intorno a un asse arbitrario.</span><span class="sxs-lookup"><span data-stu-id="f31bf-132">Rotates (relative to world coordinate space) around an arbitrary axis.</span></span><br/>                                                          |
| [<span data-ttu-id="f31bf-133">**RotateYawPitchRollLocal**</span><span class="sxs-lookup"><span data-stu-id="f31bf-133">**RotateYawPitchRollLocal**</span></span>](id3dxmatrixstack-rotateyawpitchrolllocal.md) | <span data-ttu-id="f31bf-134">Ruota (relativo allo spazio delle coordinate locali dell'oggetto) intorno a un asse arbitrario.</span><span class="sxs-lookup"><span data-stu-id="f31bf-134">Rotates (relative to the object's local coordinate space) around an arbitrary axis.</span></span><br/>                                             |
| [<span data-ttu-id="f31bf-135">**Scalabilità**</span><span class="sxs-lookup"><span data-stu-id="f31bf-135">**Scale**</span></span>](id3dxmatrixstack-scale.md)                                     | <span data-ttu-id="f31bf-136">Ridimensiona la matrice corrente sull'origine della coordinata globale.</span><span class="sxs-lookup"><span data-stu-id="f31bf-136">Scale the current matrix about the world coordinate origin.</span></span><br/>                                                                     |
| [<span data-ttu-id="f31bf-137">**ScaleLocal**</span><span class="sxs-lookup"><span data-stu-id="f31bf-137">**ScaleLocal**</span></span>](id3dxmatrixstack-scalelocal.md)                           | <span data-ttu-id="f31bf-138">Ridimensiona la matrice corrente sull'origine dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f31bf-138">Scale the current matrix about the object origin.</span></span><br/>                                                                               |
| [<span data-ttu-id="f31bf-139">**Traduci**</span><span class="sxs-lookup"><span data-stu-id="f31bf-139">**Translate**</span></span>](id3dxmatrixstack-translate.md)                             | <span data-ttu-id="f31bf-140">Determina il prodotto della matrice corrente e della matrice di traslazione calcolata determinata dai fattori specificati (x, y e z).</span><span class="sxs-lookup"><span data-stu-id="f31bf-140">Determines the product of the current matrix and the computed translation matrix determined by the given factors (x, y, and z).</span></span><br/> |
| [<span data-ttu-id="f31bf-141">**TranslateLocal**</span><span class="sxs-lookup"><span data-stu-id="f31bf-141">**TranslateLocal**</span></span>](id3dxmatrixstack-translatelocal.md)                   | <span data-ttu-id="f31bf-142">Determina il prodotto della matrice di traduzione calcolata determinata dai fattori specificati (x, y e z) e dalla matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="f31bf-142">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f31bf-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="f31bf-143">Remarks</span></span>

<span data-ttu-id="f31bf-144">L'interfaccia ID3DX10MATRIXStack viene ottenuta chiamando la funzione [**D3DXCreateMatrixStack**](d3d10-d3dxcreatematrixstack.md) .</span><span class="sxs-lookup"><span data-stu-id="f31bf-144">The ID3DX10MATRIXStack interface is obtained by calling the [**D3DXCreateMatrixStack**](d3d10-d3dxcreatematrixstack.md) function.</span></span>

<span data-ttu-id="f31bf-145">Il tipo LPD3DX10MATRIXSTACK è definito come puntatore all'interfaccia **ID3DXMatrixStack** .</span><span class="sxs-lookup"><span data-stu-id="f31bf-145">The LPD3DX10MATRIXSTACK type is defined as a pointer to the **ID3DXMatrixStack** interface.</span></span>


```
typedef interface ID3DXMatrixStack ID3DXMatrixStack;
typedef interface ID3DXMatrixStack *LPD3DXMATRIXSTACK;
```



## <a name="requirements"></a><span data-ttu-id="f31bf-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f31bf-146">Requirements</span></span>



| <span data-ttu-id="f31bf-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="f31bf-147">Requirement</span></span> | <span data-ttu-id="f31bf-148">Valore</span><span class="sxs-lookup"><span data-stu-id="f31bf-148">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f31bf-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f31bf-149">Header</span></span><br/>  | <dl> <span data-ttu-id="f31bf-150"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="f31bf-150"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f31bf-151">Libreria</span><span class="sxs-lookup"><span data-stu-id="f31bf-151">Library</span></span><br/> | <dl> <span data-ttu-id="f31bf-152"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f31bf-152"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f31bf-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f31bf-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f31bf-154">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="f31bf-154">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 

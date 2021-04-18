---
description: Interfaccia ID3DXTextureShader.
ms.assetid: 48ea307d-857f-4b73-9e13-de391fbce07b
title: Interfaccia ID3DXTextureShader (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureShader
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c1b9581bced9d501800a8a8f3cb5d31a563ac261
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322544"
---
# <a name="id3dxtextureshader-interface"></a><span data-ttu-id="35c08-103">Interfaccia ID3DXTextureShader</span><span class="sxs-lookup"><span data-stu-id="35c08-103">ID3DXTextureShader interface</span></span>

<span data-ttu-id="35c08-104">Interfaccia ID3DXTextureShader.</span><span class="sxs-lookup"><span data-stu-id="35c08-104">The ID3DXTextureShader interface.</span></span>

## <a name="members"></a><span data-ttu-id="35c08-105">Membri</span><span class="sxs-lookup"><span data-stu-id="35c08-105">Members</span></span>

<span data-ttu-id="35c08-106">L'interfaccia **ID3DXTextureShader** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="35c08-106">The **ID3DXTextureShader** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="35c08-107">**ID3DXTextureShader** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="35c08-107">**ID3DXTextureShader** also has these types of members:</span></span>

-   [<span data-ttu-id="35c08-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="35c08-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="35c08-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="35c08-109">Methods</span></span>

<span data-ttu-id="35c08-110">L'interfaccia **ID3DXTextureShader** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="35c08-110">The **ID3DXTextureShader** interface has these methods.</span></span>



| <span data-ttu-id="35c08-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="35c08-111">Method</span></span>                                                                                       | <span data-ttu-id="35c08-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35c08-112">Description</span></span>                                                                 |
|:---------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="35c08-113">**Getcostante**</span><span class="sxs-lookup"><span data-stu-id="35c08-113">**GetConstant**</span></span>](id3dxtextureshader--getconstant.md)                                       | <span data-ttu-id="35c08-114">Ottiene una costante cercando il relativo indice.</span><span class="sxs-lookup"><span data-stu-id="35c08-114">Gets a constant by looking up its index.</span></span><br/>                         |
| [<span data-ttu-id="35c08-115">**GetConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="35c08-115">**GetConstantBuffer**</span></span>](id3dxtextureshader--getconstantbuffer.md)                           | <span data-ttu-id="35c08-116">Ottenere un puntatore alla tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="35c08-116">Get a pointer to the constant table.</span></span><br/>                             |
| [<span data-ttu-id="35c08-117">**GetConstantByName**</span><span class="sxs-lookup"><span data-stu-id="35c08-117">**GetConstantByName**</span></span>](id3dxtextureshader--getconstantbyname.md)                           | <span data-ttu-id="35c08-118">Ottiene una costante cercandone il nome.</span><span class="sxs-lookup"><span data-stu-id="35c08-118">Gets a constant by looking up its name.</span></span><br/>                          |
| [<span data-ttu-id="35c08-119">**GetConstantDesc**</span><span class="sxs-lookup"><span data-stu-id="35c08-119">**GetConstantDesc**</span></span>](id3dxtextureshader--getconstantdesc.md)                               | <span data-ttu-id="35c08-120">Ottiene un puntatore alla matrice di costanti nella tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="35c08-120">Gets a pointer to the array of constants in the constant table.</span></span><br/>  |
| [<span data-ttu-id="35c08-121">**Getconstantelement**</span><span class="sxs-lookup"><span data-stu-id="35c08-121">**GetConstantElement**</span></span>](id3dxtextureshader--getconstantelement.md)                         | <span data-ttu-id="35c08-122">Ottenere una costante dalla tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="35c08-122">Get a constant from the constant table.</span></span><br/>                          |
| [<span data-ttu-id="35c08-123">**Getdesc**</span><span class="sxs-lookup"><span data-stu-id="35c08-123">**GetDesc**</span></span>](id3dxtextureshader--getdesc.md)                                               | <span data-ttu-id="35c08-124">Ottiene una descrizione della tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="35c08-124">Gets a description of the constant table.</span></span><br/>                        |
| [<span data-ttu-id="35c08-125">**GetFunction**</span><span class="sxs-lookup"><span data-stu-id="35c08-125">**GetFunction**</span></span>](id3dxtextureshader--getfunction.md)                                       | <span data-ttu-id="35c08-126">Ottiene un puntatore al flusso DWORD della funzione.</span><span class="sxs-lookup"><span data-stu-id="35c08-126">Gets a pointer to the function DWORD stream.</span></span><br/>                     |
| [<span data-ttu-id="35c08-127">**DiBOOL**</span><span class="sxs-lookup"><span data-stu-id="35c08-127">**SetBool**</span></span>](id3dxtextureshader--setbool.md)                                               | <span data-ttu-id="35c08-128">Imposta un valore BOOL.</span><span class="sxs-lookup"><span data-stu-id="35c08-128">Sets a BOOL value.</span></span><br/>                                               |
| [<span data-ttu-id="35c08-129">**SetBoolArray**</span><span class="sxs-lookup"><span data-stu-id="35c08-129">**SetBoolArray**</span></span>](id3dxtextureshader--setboolarray.md)                                     | <span data-ttu-id="35c08-130">Imposta una matrice di valori BOOL.</span><span class="sxs-lookup"><span data-stu-id="35c08-130">Sets an array of BOOL values.</span></span><br/>                                    |
| [<span data-ttu-id="35c08-131">**SetDefaults**</span><span class="sxs-lookup"><span data-stu-id="35c08-131">**SetDefaults**</span></span>](id3dxtextureshader--setdefaults.md)                                       | <span data-ttu-id="35c08-132">Imposta le costanti sui valori predefiniti dichiarati nello shader.</span><span class="sxs-lookup"><span data-stu-id="35c08-132">Sets the constants to the default values declared in the shader.</span></span><br/> |
| [<span data-ttu-id="35c08-133">**SetFloat**</span><span class="sxs-lookup"><span data-stu-id="35c08-133">**SetFloat**</span></span>](id3dxtextureshader--setfloat.md)                                             | <span data-ttu-id="35c08-134">Imposta un numero a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="35c08-134">Sets a floating-point number.</span></span><br/>                                    |
| [<span data-ttu-id="35c08-135">**SetFloatArray**</span><span class="sxs-lookup"><span data-stu-id="35c08-135">**SetFloatArray**</span></span>](id3dxtextureshader--setfloatarray.md)                                   | <span data-ttu-id="35c08-136">Imposta una matrice di numeri a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="35c08-136">Sets an array of floating-point numbers.</span></span><br/>                         |
| [<span data-ttu-id="35c08-137">**SetInt**</span><span class="sxs-lookup"><span data-stu-id="35c08-137">**SetInt**</span></span>](id3dxtextureshader--setint.md)                                                 | <span data-ttu-id="35c08-138">Imposta un valore integer.</span><span class="sxs-lookup"><span data-stu-id="35c08-138">Sets an integer value.</span></span><br/>                                           |
| [<span data-ttu-id="35c08-139">**SetIntArray**</span><span class="sxs-lookup"><span data-stu-id="35c08-139">**SetIntArray**</span></span>](id3dxtextureshader--setintarray.md)                                       | <span data-ttu-id="35c08-140">Imposta una matrice di numeri interi.</span><span class="sxs-lookup"><span data-stu-id="35c08-140">Sets an array of integers.</span></span><br/>                                       |
| [<span data-ttu-id="35c08-141">**Sematrix**</span><span class="sxs-lookup"><span data-stu-id="35c08-141">**SetMatrix**</span></span>](id3dxtextureshader--setmatrix.md)                                           | <span data-ttu-id="35c08-142">Imposta una matrice non trasposta.</span><span class="sxs-lookup"><span data-stu-id="35c08-142">Sets a non-transposed matrix.</span></span><br/>                                    |
| [<span data-ttu-id="35c08-143">**SetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="35c08-143">**SetMatrixArray**</span></span>](id3dxtextureshader--setmatrixarray.md)                                 | <span data-ttu-id="35c08-144">Imposta una matrice di matrici non transposte.</span><span class="sxs-lookup"><span data-stu-id="35c08-144">Sets an array of non-transposed matrices.</span></span><br/>                        |
| [<span data-ttu-id="35c08-145">**SetMatrixPointerArray**</span><span class="sxs-lookup"><span data-stu-id="35c08-145">**SetMatrixPointerArray**</span></span>](id3dxtextureshader--setmatrixpointerarray.md)                   | <span data-ttu-id="35c08-146">Imposta una matrice di puntatori a matrici non trasposte.</span><span class="sxs-lookup"><span data-stu-id="35c08-146">Sets an array of pointers to non-transposed matrices.</span></span><br/>            |
| [<span data-ttu-id="35c08-147">**SetMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="35c08-147">**SetMatrixTranspose**</span></span>](id3dxtextureshader--setmatrixtranspose.md)                         | <span data-ttu-id="35c08-148">Imposta una matrice trasposta.</span><span class="sxs-lookup"><span data-stu-id="35c08-148">Sets a transposed matrix.</span></span><br/>                                        |
| [<span data-ttu-id="35c08-149">**SetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="35c08-149">**SetMatrixTransposeArray**</span></span>](id3dxtextureshader--setmatrixtransposearray.md)               | <span data-ttu-id="35c08-150">Imposta una matrice di matrici trasposte.</span><span class="sxs-lookup"><span data-stu-id="35c08-150">Sets an array of transposed matrices.</span></span><br/>                            |
| [<span data-ttu-id="35c08-151">**SetMatrixTransposePointerArray**</span><span class="sxs-lookup"><span data-stu-id="35c08-151">**SetMatrixTransposePointerArray**</span></span>](id3dxtextureshader--setmatrixtransposepointerarray.md) | <span data-ttu-id="35c08-152">Imposta una matrice di puntatori a matrici trasposte.</span><span class="sxs-lookup"><span data-stu-id="35c08-152">Sets an array of pointers to transposed matrices.</span></span><br/>                |
| [<span data-ttu-id="35c08-153">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="35c08-153">**SetValue**</span></span>](id3dxtextureshader--setvalue.md)                                             | <span data-ttu-id="35c08-154">Imposta la tabella delle costanti con i dati nel buffer.</span><span class="sxs-lookup"><span data-stu-id="35c08-154">Sets the constant table with the data in the buffer.</span></span><br/>             |
| [<span data-ttu-id="35c08-155">**Sevector**</span><span class="sxs-lookup"><span data-stu-id="35c08-155">**SetVector**</span></span>](id3dxtextureshader--setvector.md)                                           | <span data-ttu-id="35c08-156">Imposta un vettore 4D.</span><span class="sxs-lookup"><span data-stu-id="35c08-156">Sets a 4D vector.</span></span><br/>                                                |
| [<span data-ttu-id="35c08-157">**SetVectorArray**</span><span class="sxs-lookup"><span data-stu-id="35c08-157">**SetVectorArray**</span></span>](id3dxtextureshader--setvectorarray.md)                                 | <span data-ttu-id="35c08-158">Imposta una matrice di vettori 4D.</span><span class="sxs-lookup"><span data-stu-id="35c08-158">Sets an array of 4D vectors.</span></span><br/>                                     |



 

## <a name="remarks"></a><span data-ttu-id="35c08-159">Commenti</span><span class="sxs-lookup"><span data-stu-id="35c08-159">Remarks</span></span>

<span data-ttu-id="35c08-160">L'interfaccia **ID3DXTextureShader** viene ottenuta chiamando la funzione [**D3DXCreateTextureShader**](d3dxcreatetextureshader.md) .</span><span class="sxs-lookup"><span data-stu-id="35c08-160">The **ID3DXTextureShader** interface is obtained by calling the [**D3DXCreateTextureShader**](d3dxcreatetextureshader.md) function.</span></span>

<span data-ttu-id="35c08-161">L'interfaccia **ID3DXTextureShader** , come tutte le interfacce com, eredita l'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="35c08-161">The **ID3DXTextureShader** interface, like all COM interfaces, inherits the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>

<span data-ttu-id="35c08-162">Il tipo LPD3DXTEXTURESHADER è definito come puntatore all'interfaccia **ID3DXTextureShader** .</span><span class="sxs-lookup"><span data-stu-id="35c08-162">The LPD3DXTEXTURESHADER type is defined as a pointer to the **ID3DXTextureShader** interface.</span></span>


```
typedef interface ID3DXTextureShader *LPD3DXTEXTURESHADER;
```



## <a name="requirements"></a><span data-ttu-id="35c08-163">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35c08-163">Requirements</span></span>



| <span data-ttu-id="35c08-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="35c08-164">Requirement</span></span> | <span data-ttu-id="35c08-165">Valore</span><span class="sxs-lookup"><span data-stu-id="35c08-165">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="35c08-166">Intestazione</span><span class="sxs-lookup"><span data-stu-id="35c08-166">Header</span></span><br/>  | <dl> <span data-ttu-id="35c08-167"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="35c08-167"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="35c08-168">Libreria</span><span class="sxs-lookup"><span data-stu-id="35c08-168">Library</span></span><br/> | <dl> <span data-ttu-id="35c08-169"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35c08-169"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="35c08-170">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35c08-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35c08-171">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="35c08-171">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 

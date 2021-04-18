---
description: L'interfaccia ID3DXConstantTable viene utilizzata per accedere alla tabella Constant. Questa tabella contiene le variabili utilizzate dagli shader e dagli effetti dei linguaggi di alto livello.
ms.assetid: 5d412c77-3d35-4913-86e5-8efa0549a2bb
title: Interfaccia ID3DXConstantTable (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bb2b7614c4d6a0e677f71e66ab94abdb89deb973
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322796"
---
# <a name="id3dxconstanttable-interface"></a><span data-ttu-id="2509a-104">Interfaccia ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="2509a-104">ID3DXConstantTable interface</span></span>

<span data-ttu-id="2509a-105">L'interfaccia ID3DXConstantTable viene utilizzata per accedere alla tabella Constant.</span><span class="sxs-lookup"><span data-stu-id="2509a-105">The ID3DXConstantTable interface is used to access the constant table.</span></span> <span data-ttu-id="2509a-106">Questa tabella contiene le variabili utilizzate dagli shader e dagli effetti dei linguaggi di alto livello.</span><span class="sxs-lookup"><span data-stu-id="2509a-106">This table contains the variables that are used by high-level language shaders and effects.</span></span>

## <a name="members"></a><span data-ttu-id="2509a-107">Membri</span><span class="sxs-lookup"><span data-stu-id="2509a-107">Members</span></span>

<span data-ttu-id="2509a-108">L'interfaccia **ID3DXConstantTable** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2509a-108">The **ID3DXConstantTable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2509a-109">**ID3DXConstantTable** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2509a-109">**ID3DXConstantTable** also has these types of members:</span></span>

-   [<span data-ttu-id="2509a-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="2509a-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2509a-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="2509a-111">Methods</span></span>

<span data-ttu-id="2509a-112">L'interfaccia **ID3DXConstantTable** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="2509a-112">The **ID3DXConstantTable** interface has these methods.</span></span>



| <span data-ttu-id="2509a-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="2509a-113">Method</span></span>                                                                                       | <span data-ttu-id="2509a-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2509a-114">Description</span></span>                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2509a-115">**GetBufferPointer**</span><span class="sxs-lookup"><span data-stu-id="2509a-115">**GetBufferPointer**</span></span>](id3dxconstanttable--getbufferpointer.md)                             | <span data-ttu-id="2509a-116">Ottiene un puntatore al buffer che contiene la tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="2509a-116">Gets a pointer to the buffer that contains the constant table.</span></span><br/>                                                          |
| [<span data-ttu-id="2509a-117">**GetBufferSize**</span><span class="sxs-lookup"><span data-stu-id="2509a-117">**GetBufferSize**</span></span>](id3dxconstanttable--getbuffersize.md)                                   | <span data-ttu-id="2509a-118">Ottiene le dimensioni del buffer della tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="2509a-118">Gets the buffer size of the constant table.</span></span><br/>                                                                             |
| [<span data-ttu-id="2509a-119">**Getcostante**</span><span class="sxs-lookup"><span data-stu-id="2509a-119">**GetConstant**</span></span>](id3dxconstanttable--getconstant.md)                                       | <span data-ttu-id="2509a-120">Ottiene una costante cercando il relativo indice.</span><span class="sxs-lookup"><span data-stu-id="2509a-120">Gets a constant by looking up its index.</span></span><br/>                                                                                |
| [<span data-ttu-id="2509a-121">**GetConstantByName**</span><span class="sxs-lookup"><span data-stu-id="2509a-121">**GetConstantByName**</span></span>](id3dxconstanttable--getconstantbyname.md)                           | <span data-ttu-id="2509a-122">Ottiene una costante cercandone il nome.</span><span class="sxs-lookup"><span data-stu-id="2509a-122">Gets a constant by looking up its name.</span></span><br/>                                                                                 |
| [<span data-ttu-id="2509a-123">**GetConstantDesc**</span><span class="sxs-lookup"><span data-stu-id="2509a-123">**GetConstantDesc**</span></span>](id3dxconstanttable--getconstantdesc.md)                               | <span data-ttu-id="2509a-124">Ottiene un puntatore a una matrice di descrizioni di costanti nella tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="2509a-124">Gets a pointer to an array of constant descriptions in the constant table.</span></span><br/>                                              |
| [<span data-ttu-id="2509a-125">**Getconstantelement**</span><span class="sxs-lookup"><span data-stu-id="2509a-125">**GetConstantElement**</span></span>](id3dxconstanttable--getconstantelement.md)                         | <span data-ttu-id="2509a-126">Ottiene una costante da una matrice di costanti.</span><span class="sxs-lookup"><span data-stu-id="2509a-126">Gets a constant from an array of constants.</span></span> <span data-ttu-id="2509a-127">Una matrice è costituita da elementi.</span><span class="sxs-lookup"><span data-stu-id="2509a-127">An array is made up of elements.</span></span><br/>                                            |
| [<span data-ttu-id="2509a-128">**Getdesc**</span><span class="sxs-lookup"><span data-stu-id="2509a-128">**GetDesc**</span></span>](id3dxconstanttable--getdesc.md)                                               | <span data-ttu-id="2509a-129">Ottiene una descrizione della tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="2509a-129">Gets a description of the constant table.</span></span><br/>                                                                               |
| [<span data-ttu-id="2509a-130">**GetSamplerIndex**</span><span class="sxs-lookup"><span data-stu-id="2509a-130">**GetSamplerIndex**</span></span>](id3dxconstanttable--getsamplerindex.md)                               | <span data-ttu-id="2509a-131">Restituisce l'indice del campionatore.</span><span class="sxs-lookup"><span data-stu-id="2509a-131">Returns the sampler index.</span></span><br/>                                                                                              |
| [<span data-ttu-id="2509a-132">**DiBOOL**</span><span class="sxs-lookup"><span data-stu-id="2509a-132">**SetBool**</span></span>](id3dxconstanttable--setbool.md)                                               | <span data-ttu-id="2509a-133">Imposta un valore booleano.</span><span class="sxs-lookup"><span data-stu-id="2509a-133">Sets a Boolean value.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="2509a-134">**SetBoolArray**</span><span class="sxs-lookup"><span data-stu-id="2509a-134">**SetBoolArray**</span></span>](id3dxconstanttable--setboolarray.md)                                     | <span data-ttu-id="2509a-135">Imposta una matrice di valori booleani.</span><span class="sxs-lookup"><span data-stu-id="2509a-135">Sets an array of Boolean values.</span></span><br/>                                                                                        |
| [<span data-ttu-id="2509a-136">**SetDefaults**</span><span class="sxs-lookup"><span data-stu-id="2509a-136">**SetDefaults**</span></span>](id3dxconstanttable--setdefaults.md)                                       | <span data-ttu-id="2509a-137">Imposta le costanti sui rispettivi valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="2509a-137">Sets the constants to their default values.</span></span> <span data-ttu-id="2509a-138">I valori predefiniti sono dichiarati nelle dichiarazioni di variabili nello shader.</span><span class="sxs-lookup"><span data-stu-id="2509a-138">The default values are declared in the variable declarations in the shader.</span></span><br/> |
| [<span data-ttu-id="2509a-139">**SetFloat**</span><span class="sxs-lookup"><span data-stu-id="2509a-139">**SetFloat**</span></span>](id3dxconstanttable--setfloat.md)                                             | <span data-ttu-id="2509a-140">Imposta un numero a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="2509a-140">Sets a floating-point number.</span></span><br/>                                                                                           |
| [<span data-ttu-id="2509a-141">**SetFloatArray**</span><span class="sxs-lookup"><span data-stu-id="2509a-141">**SetFloatArray**</span></span>](id3dxconstanttable--setfloatarray.md)                                   | <span data-ttu-id="2509a-142">Imposta una matrice di numeri a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="2509a-142">Sets an array of floating-point numbers.</span></span><br/>                                                                                |
| [<span data-ttu-id="2509a-143">**SetInt**</span><span class="sxs-lookup"><span data-stu-id="2509a-143">**SetInt**</span></span>](id3dxconstanttable--setint.md)                                                 | <span data-ttu-id="2509a-144">Imposta un valore integer.</span><span class="sxs-lookup"><span data-stu-id="2509a-144">Sets an integer value.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="2509a-145">**SetIntArray**</span><span class="sxs-lookup"><span data-stu-id="2509a-145">**SetIntArray**</span></span>](id3dxconstanttable--setintarray.md)                                       | <span data-ttu-id="2509a-146">Imposta una matrice di numeri interi.</span><span class="sxs-lookup"><span data-stu-id="2509a-146">Sets an array of integers.</span></span><br/>                                                                                              |
| [<span data-ttu-id="2509a-147">**Sematrix**</span><span class="sxs-lookup"><span data-stu-id="2509a-147">**SetMatrix**</span></span>](id3dxconstanttable--setmatrix.md)                                           | <span data-ttu-id="2509a-148">Imposta una matrice nontransposed.</span><span class="sxs-lookup"><span data-stu-id="2509a-148">Sets a nontransposed matrix.</span></span><br/>                                                                                            |
| [<span data-ttu-id="2509a-149">**SetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="2509a-149">**SetMatrixArray**</span></span>](id3dxconstanttable--setmatrixarray.md)                                 | <span data-ttu-id="2509a-150">Imposta una matrice di matrici nontransposed.</span><span class="sxs-lookup"><span data-stu-id="2509a-150">Sets an array of nontransposed matrices.</span></span><br/>                                                                                |
| [<span data-ttu-id="2509a-151">**SetMatrixPointerArray**</span><span class="sxs-lookup"><span data-stu-id="2509a-151">**SetMatrixPointerArray**</span></span>](id3dxconstanttable--setmatrixpointerarray.md)                   | <span data-ttu-id="2509a-152">Imposta una matrice di puntatori alle matrici nontransposed.</span><span class="sxs-lookup"><span data-stu-id="2509a-152">Sets an array of pointers to nontransposed matrices.</span></span><br/>                                                                    |
| [<span data-ttu-id="2509a-153">**SetMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="2509a-153">**SetMatrixTranspose**</span></span>](id3dxconstanttable--setmatrixtranspose.md)                         | <span data-ttu-id="2509a-154">Imposta una matrice trasposta.</span><span class="sxs-lookup"><span data-stu-id="2509a-154">Sets a transposed matrix.</span></span><br/>                                                                                               |
| [<span data-ttu-id="2509a-155">**SetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="2509a-155">**SetMatrixTransposeArray**</span></span>](id3dxconstanttable--setmatrixtransposearray.md)               | <span data-ttu-id="2509a-156">Imposta una matrice di matrici trasposte.</span><span class="sxs-lookup"><span data-stu-id="2509a-156">Sets an array of transposed matrices.</span></span><br/>                                                                                   |
| [<span data-ttu-id="2509a-157">**SetMatrixTransposePointerArray**</span><span class="sxs-lookup"><span data-stu-id="2509a-157">**SetMatrixTransposePointerArray**</span></span>](id3dxconstanttable--setmatrixtransposepointerarray.md) | <span data-ttu-id="2509a-158">Imposta una matrice di puntatori a matrici trasposte.</span><span class="sxs-lookup"><span data-stu-id="2509a-158">Sets an array of pointers to transposed matrices.</span></span><br/>                                                                       |
| [<span data-ttu-id="2509a-159">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="2509a-159">**SetValue**</span></span>](id3dxconstanttable--setvalue.md)                                             | <span data-ttu-id="2509a-160">Imposta il contenuto del buffer sulla tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="2509a-160">Sets the contents of the buffer to the constant table.</span></span><br/>                                                                  |
| [<span data-ttu-id="2509a-161">**Sevector**</span><span class="sxs-lookup"><span data-stu-id="2509a-161">**SetVector**</span></span>](id3dxconstanttable--setvector.md)                                           | <span data-ttu-id="2509a-162">Imposta un vettore 4D.</span><span class="sxs-lookup"><span data-stu-id="2509a-162">Sets a 4D vector.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="2509a-163">**SetVectorArray**</span><span class="sxs-lookup"><span data-stu-id="2509a-163">**SetVectorArray**</span></span>](id3dxconstanttable--setvectorarray.md)                                 | <span data-ttu-id="2509a-164">Imposta una matrice di vettori 4D.</span><span class="sxs-lookup"><span data-stu-id="2509a-164">Sets an array of 4D vectors.</span></span><br/>                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="2509a-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="2509a-165">Remarks</span></span>

<span data-ttu-id="2509a-166">Il tipo LPD3DXCONSTANTTABLE è definito come puntatore all'interfaccia **ID3DXConstantTable** .</span><span class="sxs-lookup"><span data-stu-id="2509a-166">The LPD3DXCONSTANTTABLE type is defined as a pointer to the **ID3DXConstantTable** interface.</span></span>


```
typedef interface ID3DXConstantTable ID3DXConstantTable;
typedef interface ID3DXConstantTable *LPD3DXCONSTANTTABLE;
```



## <a name="requirements"></a><span data-ttu-id="2509a-167">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2509a-167">Requirements</span></span>



| <span data-ttu-id="2509a-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="2509a-168">Requirement</span></span> | <span data-ttu-id="2509a-169">Valore</span><span class="sxs-lookup"><span data-stu-id="2509a-169">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2509a-170">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2509a-170">Header</span></span><br/>  | <dl> <span data-ttu-id="2509a-171"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2509a-171"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="2509a-172">Libreria</span><span class="sxs-lookup"><span data-stu-id="2509a-172">Library</span></span><br/> | <dl> <span data-ttu-id="2509a-173"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2509a-173"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2509a-174">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2509a-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2509a-175">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="2509a-175">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 

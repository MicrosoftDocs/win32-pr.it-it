---
description: L'interfaccia ID3DXEffectCompiler compila un effetto da una funzione o da un vertex shader.
ms.assetid: 2d1dbc63-1eb9-4736-a0b5-7f899c0638be
title: Interfaccia ID3DXEffectCompiler (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectCompiler
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d69cbcd6c14bb3a874a382f46fe5aee6619b8168
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354344"
---
# <a name="id3dxeffectcompiler-interface"></a><span data-ttu-id="cb844-103">Interfaccia ID3DXEffectCompiler</span><span class="sxs-lookup"><span data-stu-id="cb844-103">ID3DXEffectCompiler interface</span></span>

<span data-ttu-id="cb844-104">L'interfaccia **ID3DXEffectCompiler** compila un effetto da una funzione o da un vertex shader.</span><span class="sxs-lookup"><span data-stu-id="cb844-104">The **ID3DXEffectCompiler** interface compiles an effect from a function or from a vertex shader.</span></span>

## <a name="members"></a><span data-ttu-id="cb844-105">Membri</span><span class="sxs-lookup"><span data-stu-id="cb844-105">Members</span></span>

<span data-ttu-id="cb844-106">L'interfaccia **ID3DXEffectCompiler** eredita da [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span><span class="sxs-lookup"><span data-stu-id="cb844-106">The **ID3DXEffectCompiler** interface inherits from [**ID3DXBaseEffect**](id3dxbaseeffect.md).</span></span> <span data-ttu-id="cb844-107">**ID3DXEffectCompiler** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="cb844-107">**ID3DXEffectCompiler** also has these types of members:</span></span>

-   [<span data-ttu-id="cb844-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="cb844-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cb844-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="cb844-109">Methods</span></span>

<span data-ttu-id="cb844-110">L'interfaccia **ID3DXEffectCompiler** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="cb844-110">The **ID3DXEffectCompiler** interface has these methods.</span></span>



| <span data-ttu-id="cb844-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="cb844-111">Method</span></span>                                                      | <span data-ttu-id="cb844-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb844-112">Description</span></span>                                                                                                                                 |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb844-113">**CompileEffect**</span><span class="sxs-lookup"><span data-stu-id="cb844-113">**CompileEffect**</span></span>](id3dxeffectcompiler--compileeffect.md) | <span data-ttu-id="cb844-114">Compilare un effetto.</span><span class="sxs-lookup"><span data-stu-id="cb844-114">Compile an effect.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="cb844-115">**CompileShader**</span><span class="sxs-lookup"><span data-stu-id="cb844-115">**CompileShader**</span></span>](id3dxeffectcompiler--compileshader.md) | <span data-ttu-id="cb844-116">Compila uno shader da un effetto che contiene una o più funzioni.</span><span class="sxs-lookup"><span data-stu-id="cb844-116">Compiles a shader from an effect that contains one or more functions.</span></span><br/>                                                            |
| [<span data-ttu-id="cb844-117">**GetLiteral**</span><span class="sxs-lookup"><span data-stu-id="cb844-117">**GetLiteral**</span></span>](id3dxeffectcompiler--getliteral.md)       | <span data-ttu-id="cb844-118">Ottiene uno stato letterale di un parametro.</span><span class="sxs-lookup"><span data-stu-id="cb844-118">Gets a literal status of a parameter.</span></span> <span data-ttu-id="cb844-119">Un parametro letterale ha un valore che non cambia durante la durata di un effetto.</span><span class="sxs-lookup"><span data-stu-id="cb844-119">A literal parameter has a value that doesn't change during the lifetime of an effect.</span></span><br/>      |
| [<span data-ttu-id="cb844-120">**Valore letterale**</span><span class="sxs-lookup"><span data-stu-id="cb844-120">**SetLiteral**</span></span>](id3dxeffectcompiler--setliteral.md)       | <span data-ttu-id="cb844-121">Consente di abilitare o disabilitare lo stato letterale di un parametro.</span><span class="sxs-lookup"><span data-stu-id="cb844-121">Toggles the literal status of a parameter.</span></span> <span data-ttu-id="cb844-122">Un parametro letterale ha un valore che non cambia durante la durata di un effetto.</span><span class="sxs-lookup"><span data-stu-id="cb844-122">A literal parameter has a value that doesn't change during the lifetime of an effect.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cb844-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb844-123">Remarks</span></span>

<span data-ttu-id="cb844-124">L'interfaccia ID3DXEffectCompiler viene ottenuta chiamando [**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md), [**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md)o [**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md).</span><span class="sxs-lookup"><span data-stu-id="cb844-124">The ID3DXEffectCompiler interface is obtained by calling [**D3DXCreateEffectCompiler**](d3dxcreateeffectcompiler.md), [**D3DXCreateEffectCompilerFromFile**](d3dxcreateeffectcompilerfromfile.md), or [**D3DXCreateEffectCompilerFromResource**](d3dxcreateeffectcompilerfromresource.md).</span></span>

<span data-ttu-id="cb844-125">Il tipo LPD3DXEFFECTCOMPILER è definito come puntatore a questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="cb844-125">The LPD3DXEFFECTCOMPILER type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXEffectCompiler ID3DXEffectCompiler;
typedef interface ID3DXEffectCompiler *LPD3DXEFFECTCOMPILER;
```



## <a name="requirements"></a><span data-ttu-id="cb844-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb844-126">Requirements</span></span>



| <span data-ttu-id="cb844-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb844-127">Requirement</span></span> | <span data-ttu-id="cb844-128">Valore</span><span class="sxs-lookup"><span data-stu-id="cb844-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb844-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cb844-129">Header</span></span><br/>  | <dl> <span data-ttu-id="cb844-130"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb844-130"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="cb844-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="cb844-131">Library</span></span><br/> | <dl> <span data-ttu-id="cb844-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb844-132"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="cb844-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb844-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb844-134">**ID3DXBaseEffect**</span><span class="sxs-lookup"><span data-stu-id="cb844-134">**ID3DXBaseEffect**</span></span>](id3dxbaseeffect.md)
</dt> <dt>

[<span data-ttu-id="cb844-135">Interfacce degli effetti</span><span class="sxs-lookup"><span data-stu-id="cb844-135">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[<span data-ttu-id="cb844-136">**D3DXCreateEffectCompiler**</span><span class="sxs-lookup"><span data-stu-id="cb844-136">**D3DXCreateEffectCompiler**</span></span>](d3dxcreateeffectcompiler.md)
</dt> <dt>

[<span data-ttu-id="cb844-137">**D3DXCreateEffectCompilerFromFile**</span><span class="sxs-lookup"><span data-stu-id="cb844-137">**D3DXCreateEffectCompilerFromFile**</span></span>](d3dxcreateeffectcompilerfromfile.md)
</dt> <dt>

[<span data-ttu-id="cb844-138">**D3DXCreateEffectCompilerFromResource**</span><span class="sxs-lookup"><span data-stu-id="cb844-138">**D3DXCreateEffectCompilerFromResource**</span></span>](d3dxcreateeffectcompilerfromresource.md)
</dt> </dl>

 

 





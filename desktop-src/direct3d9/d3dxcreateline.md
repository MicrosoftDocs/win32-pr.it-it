---
description: Usa un sistema di coordinate a sinistra per creare una riga.
ms.assetid: 0d2ef331-9edf-4b0a-ace4-ecb8bb2f7352
title: Funzione D3DXCreateLine (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateLine
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5cf7d75ca63d64be39733b36a1b7d7a1b464238e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322447"
---
# <a name="d3dxcreateline-function"></a><span data-ttu-id="cec19-103">D3DXCreateLine (funzione)</span><span class="sxs-lookup"><span data-stu-id="cec19-103">D3DXCreateLine function</span></span>

<span data-ttu-id="cec19-104">Usa un sistema di coordinate a sinistra per creare una riga.</span><span class="sxs-lookup"><span data-stu-id="cec19-104">Uses a left-handed coordinate system to create a line.</span></span>

## <a name="syntax"></a><span data-ttu-id="cec19-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cec19-105">Syntax</span></span>


```C++
HRESULT D3DXCreateLine(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXLINE        *ppLine
);
```



## <a name="parameters"></a><span data-ttu-id="cec19-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cec19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cec19-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cec19-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cec19-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="cec19-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="cec19-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo associato alla Mesh Box creata.</span><span class="sxs-lookup"><span data-stu-id="cec19-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created box mesh.</span></span>

</dd> <dt>

<span data-ttu-id="cec19-110">*ppLine* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cec19-110">*ppLine* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cec19-111">Tipo: **[ **LPD3DXLINE**](id3dxline.md)\***</span><span class="sxs-lookup"><span data-stu-id="cec19-111">Type: **[**LPD3DXLINE**](id3dxline.md)\***</span></span>

<span data-ttu-id="cec19-112">Puntatore a un'interfaccia [**ID3DXLine**](id3dxline.md) .</span><span class="sxs-lookup"><span data-stu-id="cec19-112">Pointer to an [**ID3DXLine**](id3dxline.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cec19-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cec19-113">Return value</span></span>

<span data-ttu-id="cec19-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cec19-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cec19-115">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cec19-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="cec19-116">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="cec19-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="cec19-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="cec19-117">Remarks</span></span>

<span data-ttu-id="cec19-118">Questa funzione crea una mesh con l' \_ opzione di creazione gestita D3DXMESH e [D3DFVF \_ xyz \| D3DFVF \_ Normal](d3dfvf.md) Flexible Vertex Format (FVF).</span><span class="sxs-lookup"><span data-stu-id="cec19-118">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) Flexible Vertex Format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="cec19-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cec19-119">Requirements</span></span>



| <span data-ttu-id="cec19-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cec19-120">Requirement</span></span> | <span data-ttu-id="cec19-121">Valore</span><span class="sxs-lookup"><span data-stu-id="cec19-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cec19-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cec19-122">Header</span></span><br/>  | <dl> <span data-ttu-id="cec19-123"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="cec19-123"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="cec19-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="cec19-124">Library</span></span><br/> | <dl> <span data-ttu-id="cec19-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cec19-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cec19-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cec19-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cec19-127">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="cec19-127">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 

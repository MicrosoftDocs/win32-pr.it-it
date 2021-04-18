---
description: Richiede l'allocazione di un oggetto frame.
ms.assetid: 977e40d6-bf49-44b6-ac95-88e7f778ea50
title: 'Metodo ID3DXAllocateHierarchy:: CreateFrame (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.CreateFrame
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d6a3a13dd4d3b3dfaffb26632ff6ad5cc8666f86
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323179"
---
# <a name="id3dxallocatehierarchycreateframe-method"></a><span data-ttu-id="eeee2-103">Metodo ID3DXAllocateHierarchy:: CreateFrame</span><span class="sxs-lookup"><span data-stu-id="eeee2-103">ID3DXAllocateHierarchy::CreateFrame method</span></span>

<span data-ttu-id="eeee2-104">Richiede l'allocazione di un oggetto frame.</span><span class="sxs-lookup"><span data-stu-id="eeee2-104">Requests allocation of a frame object.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeee2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eeee2-105">Syntax</span></span>


```C++
HRESULT CreateFrame(
  [in]          LPCSTR      Name,
  [out, retval] LPD3DXFRAME *ppNewFrame
);
```



## <a name="parameters"></a><span data-ttu-id="eeee2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="eeee2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eeee2-107">*Nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eeee2-107">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eeee2-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eeee2-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eeee2-109">Nome del fotogramma da creare.</span><span class="sxs-lookup"><span data-stu-id="eeee2-109">Name of the frame to be created.</span></span>

</dd> <dt>

<span data-ttu-id="eeee2-110">*ppNewFrame* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="eeee2-110">*ppNewFrame* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="eeee2-111">Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)\***</span><span class="sxs-lookup"><span data-stu-id="eeee2-111">Type: **[**LPD3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="eeee2-112">Restituisce l'oggetto frame creato.</span><span class="sxs-lookup"><span data-stu-id="eeee2-112">Returns the created frame object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eeee2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eeee2-113">Return value</span></span>

<span data-ttu-id="eeee2-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eeee2-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eeee2-115">I valori restituiti da questo metodo sono implementati da un programmatore di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="eeee2-115">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="eeee2-116">In generale, se non si verificano errori, programmare il metodo per restituire D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="eeee2-116">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="eeee2-117">In caso contrario, programmare il metodo per restituire un messaggio di errore appropriato da D3DERR o D3DXERR, in quanto questa operazione causerà l'esito negativo anche di [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) e restituirà l'errore.</span><span class="sxs-lookup"><span data-stu-id="eeee2-117">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="eeee2-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eeee2-118">Requirements</span></span>



| <span data-ttu-id="eeee2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="eeee2-119">Requirement</span></span> | <span data-ttu-id="eeee2-120">Valore</span><span class="sxs-lookup"><span data-stu-id="eeee2-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eeee2-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eeee2-121">Header</span></span><br/>  | <dl> <span data-ttu-id="eeee2-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="eeee2-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="eeee2-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="eeee2-123">Library</span></span><br/> | <dl> <span data-ttu-id="eeee2-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eeee2-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eeee2-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eeee2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeee2-126">ID3DXAllocateHierarchy</span><span class="sxs-lookup"><span data-stu-id="eeee2-126">ID3DXAllocateHierarchy</span></span>](id3dxallocatehierarchy.md)
</dt> </dl>

 

 

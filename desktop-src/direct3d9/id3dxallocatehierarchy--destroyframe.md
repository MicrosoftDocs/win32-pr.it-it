---
description: Richiede la deallocazione di un oggetto frame.
ms.assetid: b2793744-1bba-4a2b-938c-44ed316358fd
title: Metodo ID3DXAllocateHierarchy::D estroyFrame (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.DestroyFrame
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4a394501b9967d3f7cb6d3f6b2f30db168438278
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104402020"
---
# <a name="id3dxallocatehierarchydestroyframe-method"></a><span data-ttu-id="cc252-103">ID3DXAllocateHierarchy::D Metodo estroyFrame</span><span class="sxs-lookup"><span data-stu-id="cc252-103">ID3DXAllocateHierarchy::DestroyFrame method</span></span>

<span data-ttu-id="cc252-104">Richiede la deallocazione di un oggetto frame.</span><span class="sxs-lookup"><span data-stu-id="cc252-104">Requests deallocation of a frame object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc252-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cc252-105">Syntax</span></span>


```C++
HRESULT DestroyFrame(
  [in] LPD3DXFRAME pFrameToFree
);
```



## <a name="parameters"></a><span data-ttu-id="cc252-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cc252-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc252-107">*pFrameToFree* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cc252-107">*pFrameToFree* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc252-108">Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="cc252-108">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="cc252-109">Puntatore al frame da deallocare.</span><span class="sxs-lookup"><span data-stu-id="cc252-109">Pointer to the frame to be deallocated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc252-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cc252-110">Return value</span></span>

<span data-ttu-id="cc252-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cc252-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cc252-112">I valori restituiti da questo metodo sono implementati da un programmatore di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="cc252-112">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="cc252-113">In generale, se non si verificano errori, programmare il metodo per restituire D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cc252-113">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="cc252-114">In caso contrario, programmare il metodo per restituire un messaggio di errore appropriato da D3DERR o D3DXERR, in quanto questa operazione causerà l'esito negativo anche di [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) e restituirà l'errore.</span><span class="sxs-lookup"><span data-stu-id="cc252-114">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc252-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc252-115">Requirements</span></span>



| <span data-ttu-id="cc252-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc252-116">Requirement</span></span> | <span data-ttu-id="cc252-117">Valore</span><span class="sxs-lookup"><span data-stu-id="cc252-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc252-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cc252-118">Header</span></span><br/>  | <dl> <span data-ttu-id="cc252-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc252-119"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="cc252-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="cc252-120">Library</span></span><br/> | <dl> <span data-ttu-id="cc252-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc252-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cc252-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cc252-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc252-123">ID3DXAllocateHierarchy</span><span class="sxs-lookup"><span data-stu-id="cc252-123">ID3DXAllocateHierarchy</span></span>](id3dxallocatehierarchy.md)
</dt> </dl>

 

 





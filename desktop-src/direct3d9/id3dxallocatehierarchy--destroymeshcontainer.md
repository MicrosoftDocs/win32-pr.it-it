---
description: Richiede la deallocazione di un oggetto contenitore mesh.
ms.assetid: 7a976ba8-6972-4857-b0a9-4ea7a88dc8ac
title: Metodo ID3DXAllocateHierarchy::D estroyMeshContainer (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.DestroyMeshContainer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6114c78cefd7415fb11fc30587fa2dc628fb4466
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531069"
---
# <a name="id3dxallocatehierarchydestroymeshcontainer-method"></a><span data-ttu-id="4f992-103">ID3DXAllocateHierarchy::D Metodo estroyMeshContainer</span><span class="sxs-lookup"><span data-stu-id="4f992-103">ID3DXAllocateHierarchy::DestroyMeshContainer method</span></span>

<span data-ttu-id="4f992-104">Richiede la deallocazione di un oggetto contenitore mesh.</span><span class="sxs-lookup"><span data-stu-id="4f992-104">Requests deallocation of a mesh container object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f992-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f992-105">Syntax</span></span>


```C++
HRESULT DestroyMeshContainer(
  [in] LPD3DXMESHCONTAINER pMeshContainerToFree
);
```



## <a name="parameters"></a><span data-ttu-id="4f992-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4f992-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f992-107">*pMeshContainerToFree* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4f992-107">*pMeshContainerToFree* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f992-108">Tipo: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span><span class="sxs-lookup"><span data-stu-id="4f992-108">Type: **[**LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span></span>

<span data-ttu-id="4f992-109">Puntatore all'oggetto contenitore mesh da deallocare.</span><span class="sxs-lookup"><span data-stu-id="4f992-109">Pointer to the mesh container object to be deallocated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f992-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4f992-110">Return value</span></span>

<span data-ttu-id="4f992-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4f992-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4f992-112">I valori restituiti da questo metodo sono implementati da un programmatore di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="4f992-112">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="4f992-113">In generale, se non si verificano errori, programmare il metodo per restituire D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4f992-113">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="4f992-114">In caso contrario, programmare il metodo per restituire un messaggio di errore appropriato da D3DERR o D3DXERR, in quanto questa operazione causerà l'esito negativo anche di [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) e restituirà l'errore.</span><span class="sxs-lookup"><span data-stu-id="4f992-114">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f992-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f992-115">Requirements</span></span>



| <span data-ttu-id="4f992-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f992-116">Requirement</span></span> | <span data-ttu-id="4f992-117">Valore</span><span class="sxs-lookup"><span data-stu-id="4f992-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f992-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4f992-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4f992-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f992-119"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="4f992-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="4f992-120">Library</span></span><br/> | <dl> <span data-ttu-id="4f992-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f992-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4f992-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f992-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f992-123">ID3DXAllocateHierarchy</span><span class="sxs-lookup"><span data-stu-id="4f992-123">ID3DXAllocateHierarchy</span></span>](id3dxallocatehierarchy.md)
</dt> </dl>

 

 





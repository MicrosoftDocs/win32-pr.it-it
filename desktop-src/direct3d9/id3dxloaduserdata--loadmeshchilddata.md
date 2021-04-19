---
description: Caricare i dati figlio della mesh da un file con estensione x.
ms.assetid: 5ed338f9-48a6-44e6-95da-1bed9ecd6ebf
title: 'Metodo ID3DXLoadUserData:: LoadMeshChildData (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData.LoadMeshChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9960f47ac21dad2521f6272c9176e3d895bbd109
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322344"
---
# <a name="id3dxloaduserdataloadmeshchilddata-method"></a><span data-ttu-id="04803-103">Metodo ID3DXLoadUserData:: LoadMeshChildData</span><span class="sxs-lookup"><span data-stu-id="04803-103">ID3DXLoadUserData::LoadMeshChildData method</span></span>

<span data-ttu-id="04803-104">Caricare i dati figlio della mesh da un file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="04803-104">Load mesh child data from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="04803-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04803-105">Syntax</span></span>


```C++
HRESULT LoadMeshChildData(
  [in] LPD3DXMESHCONTAINER pMeshContainer,
  [in] LPD3DXFILEDATA      pXofChildData
);
```



## <a name="parameters"></a><span data-ttu-id="04803-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="04803-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04803-107">*pMeshContainer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04803-107">*pMeshContainer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04803-108">Tipo: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span><span class="sxs-lookup"><span data-stu-id="04803-108">Type: **[**LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)**</span></span>

<span data-ttu-id="04803-109">Puntatore a un contenitore mesh.</span><span class="sxs-lookup"><span data-stu-id="04803-109">Pointer to a mesh container.</span></span> <span data-ttu-id="04803-110">Vedere [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span><span class="sxs-lookup"><span data-stu-id="04803-110">See [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span></span>

</dd> <dt>

<span data-ttu-id="04803-111">*pXofChildData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04803-111">*pXofChildData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04803-112">Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="04803-112">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="04803-113">Puntatore a una struttura di dati del file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="04803-113">Pointer to a .x file data structure.</span></span> <span data-ttu-id="04803-114">Questa operazione è definita in dxfile. h.</span><span class="sxs-lookup"><span data-stu-id="04803-114">This is defined in Dxfile.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04803-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="04803-115">Return value</span></span>

<span data-ttu-id="04803-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="04803-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="04803-117">I valori restituiti da questo metodo sono implementati da un programmatore di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="04803-117">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="04803-118">In generale, se non si verificano errori, programmare il metodo per restituire D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="04803-118">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="04803-119">In caso contrario, programmare il metodo per restituire un messaggio di errore appropriato da D3DERR o D3DXERR, in quanto questa operazione causerà l'esito negativo anche di [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) e restituirà l'errore.</span><span class="sxs-lookup"><span data-stu-id="04803-119">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="04803-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04803-120">Requirements</span></span>



| <span data-ttu-id="04803-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="04803-121">Requirement</span></span> | <span data-ttu-id="04803-122">Valore</span><span class="sxs-lookup"><span data-stu-id="04803-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="04803-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="04803-123">Header</span></span><br/>  | <dl> <span data-ttu-id="04803-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="04803-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="04803-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="04803-125">Library</span></span><br/> | <dl> <span data-ttu-id="04803-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04803-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="04803-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04803-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04803-128">ID3DXLoadUserData</span><span class="sxs-lookup"><span data-stu-id="04803-128">ID3DXLoadUserData</span></span>](id3dxloaduserdata.md)
</dt> </dl>

 

 





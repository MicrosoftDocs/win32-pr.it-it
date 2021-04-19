---
description: Caricare i dati di primo livello da un file con estensione x.
ms.assetid: 0270b923-d524-46c5-bd1a-44c782722635
title: 'Metodo ID3DXLoadUserData:: LoadTopLevelData (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData.LoadTopLevelData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f52d6853b12b666ab64602711a42c3698d6d8032
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323472"
---
# <a name="id3dxloaduserdataloadtopleveldata-method"></a><span data-ttu-id="8a37a-103">Metodo ID3DXLoadUserData:: LoadTopLevelData</span><span class="sxs-lookup"><span data-stu-id="8a37a-103">ID3DXLoadUserData::LoadTopLevelData method</span></span>

<span data-ttu-id="8a37a-104">Caricare i dati di primo livello da un file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="8a37a-104">Load top level data from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a37a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a37a-105">Syntax</span></span>


```C++
HRESULT LoadTopLevelData(
  [in] LPD3DXFILEDATA pXofChildData
);
```



## <a name="parameters"></a><span data-ttu-id="8a37a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8a37a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a37a-107">*pXofChildData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a37a-107">*pXofChildData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a37a-108">Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="8a37a-108">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)**</span></span>

<span data-ttu-id="8a37a-109">Puntatore a una struttura di dati del file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="8a37a-109">Pointer to a .x file data structure.</span></span> <span data-ttu-id="8a37a-110">Questa operazione è definita in dxfile. h.</span><span class="sxs-lookup"><span data-stu-id="8a37a-110">This is defined in Dxfile.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a37a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8a37a-111">Return value</span></span>

<span data-ttu-id="8a37a-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8a37a-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8a37a-113">I valori restituiti da questo metodo sono implementati da un programmatore di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="8a37a-113">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="8a37a-114">In generale, se non si verificano errori, programmare il metodo per restituire D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8a37a-114">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="8a37a-115">In caso contrario, programmare il metodo per restituire un messaggio di errore appropriato da D3DERR o D3DXERR, in quanto questa operazione causerà l'esito negativo anche di [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) e restituirà l'errore.</span><span class="sxs-lookup"><span data-stu-id="8a37a-115">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a37a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a37a-116">Requirements</span></span>



| <span data-ttu-id="8a37a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a37a-117">Requirement</span></span> | <span data-ttu-id="8a37a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="8a37a-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a37a-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8a37a-119">Header</span></span><br/>  | <dl> <span data-ttu-id="8a37a-120"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a37a-120"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="8a37a-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="8a37a-121">Library</span></span><br/> | <dl> <span data-ttu-id="8a37a-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a37a-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8a37a-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a37a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a37a-124">ID3DXLoadUserData</span><span class="sxs-lookup"><span data-stu-id="8a37a-124">ID3DXLoadUserData</span></span>](id3dxloaduserdata.md)
</dt> </dl>

 

 





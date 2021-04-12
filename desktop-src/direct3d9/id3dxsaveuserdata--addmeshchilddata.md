---
description: Aggiungere i dati figlio alla rete.
ms.assetid: cf3e2015-c4b0-4d98-8346-c74fbdd37310
title: 'Metodo ID3DXSaveUserData:: AddMeshChildData (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddMeshChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8a9d6b69e64e0e1eca5d4350125e0955254b6127
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235189"
---
# <a name="id3dxsaveuserdataaddmeshchilddata-method"></a><span data-ttu-id="f1cc2-103">Metodo ID3DXSaveUserData:: AddMeshChildData</span><span class="sxs-lookup"><span data-stu-id="f1cc2-103">ID3DXSaveUserData::AddMeshChildData method</span></span>

<span data-ttu-id="f1cc2-104">Aggiungere i dati figlio alla rete.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-104">Add child data to the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1cc2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1cc2-105">Syntax</span></span>


```C++
HRESULT AddMeshChildData(
  [in] const D3DXMESHCONTAINER    *pMeshContainer,
  [in]       LPD3DXFILESAVEOBJECT pXofSave,
  [in]       LPD3DXFileSaveData   pXofMeshData
);
```



## <a name="parameters"></a><span data-ttu-id="f1cc2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f1cc2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1cc2-107">*pMeshContainer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f1cc2-107">*pMeshContainer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1cc2-108">Tipo: **const [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md) \***</span><span class="sxs-lookup"><span data-stu-id="f1cc2-108">Type: **const [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md)\***</span></span>

<span data-ttu-id="f1cc2-109">Puntatore a un contenitore mesh.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-109">Pointer to a mesh container.</span></span> <span data-ttu-id="f1cc2-110">Vedere [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span><span class="sxs-lookup"><span data-stu-id="f1cc2-110">See [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1cc2-111">*pXofSave* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f1cc2-111">*pXofSave* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1cc2-112">Tipo: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span><span class="sxs-lookup"><span data-stu-id="f1cc2-112">Type: **[**LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span></span>

<span data-ttu-id="f1cc2-113">Puntatore a un oggetto di salvataggio file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-113">Pointer to a .x file save object.</span></span> <span data-ttu-id="f1cc2-114">Usare il puntatore per chiamare [**ID3DXFileSaveObject:: AddDataObject**](id3dxfilesaveobject--adddataobject.md) per aggiungere un oggetto dati figlio.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-114">Use the pointer to call [**ID3DXFileSaveObject::AddDataObject**](id3dxfilesaveobject--adddataobject.md) to add a child data object.</span></span> <span data-ttu-id="f1cc2-115">Non salvare i dati con [**ID3DXFileSaveObject:: Save**](id3dxfilesaveobject--save.md).</span><span class="sxs-lookup"><span data-stu-id="f1cc2-115">Do not save the data with [**ID3DXFileSaveObject::Save**](id3dxfilesaveobject--save.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1cc2-116">*pXofMeshData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f1cc2-116">*pXofMeshData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1cc2-117">Tipo: **[ **LPD3DXFileSaveData**](id3dxfilesavedata.md)**</span><span class="sxs-lookup"><span data-stu-id="f1cc2-117">Type: **[**LPD3DXFileSaveData**](id3dxfilesavedata.md)**</span></span>

<span data-ttu-id="f1cc2-118">Puntatore a un nodo dati del file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-118">Pointer to a .x file data node.</span></span> <span data-ttu-id="f1cc2-119">Usare il puntatore per chiamare [**ID3DXFileSaveData:: AddDataObject**](id3dxfilesavedata--adddataobject.md) per aggiungere un oggetto dati figlio.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-119">Use the pointer to call [**ID3DXFileSaveData::AddDataObject**](id3dxfilesavedata--adddataobject.md) to add a child data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1cc2-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f1cc2-120">Return value</span></span>

<span data-ttu-id="f1cc2-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f1cc2-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f1cc2-122">I valori restituiti da questo metodo sono implementati da un programmatore di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-122">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="f1cc2-123">In generale, se non si verificano errori, programmare il metodo per restituire D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-123">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="f1cc2-124">In caso contrario, programmare il metodo per restituire un messaggio di errore appropriato da [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md), in quanto questa operazione causerà l'esito negativo anche di [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) e restituirà l'errore.</span><span class="sxs-lookup"><span data-stu-id="f1cc2-124">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1cc2-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1cc2-125">Requirements</span></span>



| <span data-ttu-id="f1cc2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1cc2-126">Requirement</span></span> | <span data-ttu-id="f1cc2-127">Valore</span><span class="sxs-lookup"><span data-stu-id="f1cc2-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1cc2-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f1cc2-128">Header</span></span><br/>  | <dl> <span data-ttu-id="f1cc2-129"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1cc2-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="f1cc2-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="f1cc2-130">Library</span></span><br/> | <dl> <span data-ttu-id="f1cc2-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1cc2-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f1cc2-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1cc2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1cc2-133">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="f1cc2-133">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 

---
description: Aggiungere i dati figlio al frame.
ms.assetid: b1e02b2a-628f-49c3-a81c-0e96ba0d5f4a
title: 'Metodo ID3DXSaveUserData:: AddFrameChildData (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddFrameChildData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3e3017ec2dafa9d4188da4f50d14257a09ffe72f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235190"
---
# <a name="id3dxsaveuserdataaddframechilddata-method"></a><span data-ttu-id="c3b98-103">Metodo ID3DXSaveUserData:: AddFrameChildData</span><span class="sxs-lookup"><span data-stu-id="c3b98-103">ID3DXSaveUserData::AddFrameChildData method</span></span>

<span data-ttu-id="c3b98-104">Aggiungere i dati figlio al frame.</span><span class="sxs-lookup"><span data-stu-id="c3b98-104">Add child data to the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3b98-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c3b98-105">Syntax</span></span>


```C++
HRESULT AddFrameChildData(
  [in] const D3DXFRAME            *pFrame,
  [in]       LPD3DXFILESAVEOBJECT pXofSave,
  [in]       LPD3DXFileSaveData   pXofFrameData
);
```



## <a name="parameters"></a><span data-ttu-id="c3b98-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c3b98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3b98-107">*pFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3b98-107">*pFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3b98-108">Tipo: **const [**D3DXFRAME**](d3dxframe.md) \***</span><span class="sxs-lookup"><span data-stu-id="c3b98-108">Type: **const [**D3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="c3b98-109">Puntatore a un contenitore mesh.</span><span class="sxs-lookup"><span data-stu-id="c3b98-109">Pointer to a mesh container.</span></span> <span data-ttu-id="c3b98-110">Vedere [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="c3b98-110">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3b98-111">*pXofSave* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3b98-111">*pXofSave* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3b98-112">Tipo: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span><span class="sxs-lookup"><span data-stu-id="c3b98-112">Type: **[**LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span></span>

<span data-ttu-id="c3b98-113">Puntatore a un oggetto di salvataggio file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="c3b98-113">Pointer to a .x file save object.</span></span> <span data-ttu-id="c3b98-114">Usare il puntatore per chiamare [**ID3DXFileSaveObject:: AddDataObject**](id3dxfilesaveobject--adddataobject.md) per aggiungere un oggetto dati figlio.</span><span class="sxs-lookup"><span data-stu-id="c3b98-114">Use the pointer to call [**ID3DXFileSaveObject::AddDataObject**](id3dxfilesaveobject--adddataobject.md) to add a child data object.</span></span> <span data-ttu-id="c3b98-115">Non salvare i dati con [**ID3DXFileSaveObject:: Save**](id3dxfilesaveobject--save.md).</span><span class="sxs-lookup"><span data-stu-id="c3b98-115">Do not save the data with [**ID3DXFileSaveObject::Save**](id3dxfilesaveobject--save.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3b98-116">*pXofFrameData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3b98-116">*pXofFrameData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3b98-117">Tipo: **[ **LPD3DXFileSaveData**](id3dxfilesavedata.md)**</span><span class="sxs-lookup"><span data-stu-id="c3b98-117">Type: **[**LPD3DXFileSaveData**](id3dxfilesavedata.md)**</span></span>

<span data-ttu-id="c3b98-118">Puntatore a un nodo dati del file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="c3b98-118">Pointer to a .x file data node.</span></span> <span data-ttu-id="c3b98-119">Usare il puntatore per chiamare [**ID3DXFileSaveData:: AddDataObject**](id3dxfilesavedata--adddataobject.md) per aggiungere un oggetto dati figlio.</span><span class="sxs-lookup"><span data-stu-id="c3b98-119">Use the pointer to call [**ID3DXFileSaveData::AddDataObject**](id3dxfilesavedata--adddataobject.md) to add a child data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3b98-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c3b98-120">Return value</span></span>

<span data-ttu-id="c3b98-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c3b98-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c3b98-122">I valori restituiti da questo metodo sono implementati da un programmatore di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="c3b98-122">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="c3b98-123">In generale, se non si verificano errori, programmare il metodo per restituire D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c3b98-123">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="c3b98-124">In caso contrario, programmare il metodo per restituire un messaggio di errore appropriato da [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md), in quanto questa operazione causerà l'esito negativo anche di [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) e restituirà l'errore.</span><span class="sxs-lookup"><span data-stu-id="c3b98-124">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3b98-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="c3b98-125">Remarks</span></span>

<span data-ttu-id="c3b98-126">[**ID3DXSaveUserData:: RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) e [**ID3DXSaveUserData:: SaveTemplates**](id3dxsaveuserdata--savetemplates.md) forniscono un meccanismo per l'aggiunta di un modello a un file con estensione x per il salvataggio dei dati utente.</span><span class="sxs-lookup"><span data-stu-id="c3b98-126">[**ID3DXSaveUserData::RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) and [**ID3DXSaveUserData::SaveTemplates**](id3dxsaveuserdata--savetemplates.md) provide a mechanism for adding a template to a .x file for saving user data.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3b98-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c3b98-127">Requirements</span></span>



| <span data-ttu-id="c3b98-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3b98-128">Requirement</span></span> | <span data-ttu-id="c3b98-129">Valore</span><span class="sxs-lookup"><span data-stu-id="c3b98-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3b98-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c3b98-130">Header</span></span><br/>  | <dl> <span data-ttu-id="c3b98-131"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3b98-131"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="c3b98-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="c3b98-132">Library</span></span><br/> | <dl> <span data-ttu-id="c3b98-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3b98-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c3b98-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c3b98-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3b98-135">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="c3b98-135">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 

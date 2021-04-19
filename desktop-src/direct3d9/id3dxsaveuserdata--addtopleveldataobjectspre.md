---
description: Aggiungere un oggetto di primo livello prima della gerarchia dei frame.
ms.assetid: ab4bfc3e-58eb-4de6-b080-8b3392b801bf
title: 'Metodo ID3DXSaveUserData:: AddTopLevelDataObjectsPre (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.AddTopLevelDataObjectsPre
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d0194c8c9c6806f96cbe75394e6650ca3e7dc74b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323522"
---
# <a name="id3dxsaveuserdataaddtopleveldataobjectspre-method"></a><span data-ttu-id="2a4c7-103">Metodo ID3DXSaveUserData:: AddTopLevelDataObjectsPre</span><span class="sxs-lookup"><span data-stu-id="2a4c7-103">ID3DXSaveUserData::AddTopLevelDataObjectsPre method</span></span>

<span data-ttu-id="2a4c7-104">Aggiungere un oggetto di primo livello prima della gerarchia dei frame.</span><span class="sxs-lookup"><span data-stu-id="2a4c7-104">Add a top level object before the frame hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a4c7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2a4c7-105">Syntax</span></span>


```C++
HRESULT AddTopLevelDataObjectsPre(
  [in] LPD3DXFILESAVEOBJECT pXofSave
);
```



## <a name="parameters"></a><span data-ttu-id="2a4c7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2a4c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a4c7-107">*pXofSave* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2a4c7-107">*pXofSave* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a4c7-108">Tipo: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span><span class="sxs-lookup"><span data-stu-id="2a4c7-108">Type: **[**LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span></span>

<span data-ttu-id="2a4c7-109">Puntatore a un oggetto di salvataggio file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="2a4c7-109">Pointer to a .x file save object.</span></span> <span data-ttu-id="2a4c7-110">Utilizzare questo puntatore per chiamare [**IDirectXFileSaveObject:: CreateDataObject**](idirectxfilesaveobject--createdataobject.md) per creare l'oggetto dati da salvare.</span><span class="sxs-lookup"><span data-stu-id="2a4c7-110">Use this pointer to call [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) to create the data object to be saved.</span></span> <span data-ttu-id="2a4c7-111">Quindi, chiamare [**IDirectXFileSaveObject:: SaveData**](idirectxfilesaveobject--savedata.md) per salvare i dati.</span><span class="sxs-lookup"><span data-stu-id="2a4c7-111">Then call [**IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md) to save the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a4c7-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2a4c7-112">Return value</span></span>

<span data-ttu-id="2a4c7-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2a4c7-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2a4c7-114">I valori restituiti da questo metodo sono implementati da un programmatore di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="2a4c7-114">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="2a4c7-115">In generale, se non si verificano errori, programmare il metodo per restituire D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2a4c7-115">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="2a4c7-116">In caso contrario, programmare il metodo per restituire un messaggio di errore appropriato da [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md), in quanto questa operazione causerà l'esito negativo anche di [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) e restituirà l'errore.</span><span class="sxs-lookup"><span data-stu-id="2a4c7-116">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a4c7-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a4c7-117">Requirements</span></span>



| <span data-ttu-id="2a4c7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a4c7-118">Requirement</span></span> | <span data-ttu-id="2a4c7-119">Valore</span><span class="sxs-lookup"><span data-stu-id="2a4c7-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a4c7-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2a4c7-120">Header</span></span><br/>  | <dl> <span data-ttu-id="2a4c7-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a4c7-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="2a4c7-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="2a4c7-122">Library</span></span><br/> | <dl> <span data-ttu-id="2a4c7-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a4c7-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2a4c7-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a4c7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a4c7-125">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="2a4c7-125">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 

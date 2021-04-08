---
description: Callback che consente all'utente di salvare un modello di file con estensione x.
ms.assetid: c2e29495-5eeb-42b8-826e-1a60c1c6bda2
title: 'Metodo ID3DXSaveUserData:: SaveTemplates (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.SaveTemplates
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 92040629b1b21cbfa1219eee237e357aa056b473
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969502"
---
# <a name="id3dxsaveuserdatasavetemplates-method"></a><span data-ttu-id="97d26-103">Metodo ID3DXSaveUserData:: SaveTemplates</span><span class="sxs-lookup"><span data-stu-id="97d26-103">ID3DXSaveUserData::SaveTemplates method</span></span>

<span data-ttu-id="97d26-104">Callback che consente all'utente di salvare un modello di file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="97d26-104">A callback for the user to save a .x file template.</span></span>

## <a name="syntax"></a><span data-ttu-id="97d26-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="97d26-105">Syntax</span></span>


```C++
HRESULT SaveTemplates(
  [in] LPD3DXFILESAVEOBJECT pXofSave
);
```



## <a name="parameters"></a><span data-ttu-id="97d26-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="97d26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97d26-107">*pXofSave* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97d26-107">*pXofSave* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97d26-108">Tipo: **[ **LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span><span class="sxs-lookup"><span data-stu-id="97d26-108">Type: **[**LPD3DXFILESAVEOBJECT**](id3dxfilesaveobject.md)**</span></span>

<span data-ttu-id="97d26-109">Puntatore a un oggetto di salvataggio file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="97d26-109">Pointer to a .x file save object.</span></span> <span data-ttu-id="97d26-110">Non utilizzare questo parametro per aggiungere oggetti dati.</span><span class="sxs-lookup"><span data-stu-id="97d26-110">Do not use this parameter to add data objects.</span></span> <span data-ttu-id="97d26-111">Vedere [**ID3DXFileSaveObject**](id3dxfilesaveobject.md).</span><span class="sxs-lookup"><span data-stu-id="97d26-111">See [**ID3DXFileSaveObject**](id3dxfilesaveobject.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97d26-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="97d26-112">Return value</span></span>

<span data-ttu-id="97d26-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="97d26-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="97d26-114">I valori restituiti da questo metodo sono implementati da un programmatore di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="97d26-114">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="97d26-115">In generale, se non si verificano errori, programmare il metodo per restituire D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="97d26-115">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="97d26-116">In caso contrario, programmare il metodo per restituire un messaggio di errore appropriato da [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md), in quanto questa operazione causerà l'esito negativo anche di [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) e restituirà l'errore.</span><span class="sxs-lookup"><span data-stu-id="97d26-116">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="97d26-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="97d26-117">Remarks</span></span>

<span data-ttu-id="97d26-118">[**ID3DXSaveUserData:: RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) e **ID3DXSaveUserData:: SaveTemplates** forniscono un meccanismo per l'aggiunta di un modello a un file con estensione x per il salvataggio dei dati utente.</span><span class="sxs-lookup"><span data-stu-id="97d26-118">[**ID3DXSaveUserData::RegisterTemplates**](id3dxsaveuserdata--registertemplates.md) and **ID3DXSaveUserData::SaveTemplates** provide a mechanism for adding a template to a .x file for saving user data.</span></span>

## <a name="requirements"></a><span data-ttu-id="97d26-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97d26-119">Requirements</span></span>



| <span data-ttu-id="97d26-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="97d26-120">Requirement</span></span> | <span data-ttu-id="97d26-121">Valore</span><span class="sxs-lookup"><span data-stu-id="97d26-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="97d26-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="97d26-122">Header</span></span><br/>  | <dl> <span data-ttu-id="97d26-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="97d26-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="97d26-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="97d26-124">Library</span></span><br/> | <dl> <span data-ttu-id="97d26-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="97d26-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="97d26-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97d26-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97d26-127">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="97d26-127">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 

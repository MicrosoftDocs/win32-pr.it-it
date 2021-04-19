---
description: Callback che consente all'utente di registrare un modello di file con estensione x.
ms.assetid: 60568556-704c-4be3-bbde-04887583cf70
title: 'Metodo ID3DXSaveUserData:: RegisterTemplates (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.RegisterTemplates
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c1465b76b758f6a5ed9e7dff4c7126935fb7c5d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323521"
---
# <a name="id3dxsaveuserdataregistertemplates-method"></a><span data-ttu-id="b5cff-103">Metodo ID3DXSaveUserData:: RegisterTemplates</span><span class="sxs-lookup"><span data-stu-id="b5cff-103">ID3DXSaveUserData::RegisterTemplates method</span></span>

<span data-ttu-id="b5cff-104">Callback che consente all'utente di registrare un modello di file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="b5cff-104">A callback for the user to register a .x file template.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5cff-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5cff-105">Syntax</span></span>


```C++
HRESULT RegisterTemplates(
  [in] LPD3DXFILE pXFileApi
);
```



## <a name="parameters"></a><span data-ttu-id="b5cff-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5cff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5cff-107">*pXFileApi* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5cff-107">*pXFileApi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5cff-108">Tipo: **[ **LPD3DXFILE**](id3dxfile.md)**</span><span class="sxs-lookup"><span data-stu-id="b5cff-108">Type: **[**LPD3DXFILE**](id3dxfile.md)**</span></span>

<span data-ttu-id="b5cff-109">Utilizzare questo puntatore per registrare i modelli di file con estensione x definiti dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b5cff-109">Use this pointer to register user-defined .x file templates.</span></span> <span data-ttu-id="b5cff-110">Vedere [**ID3DXFile**](id3dxfile.md).</span><span class="sxs-lookup"><span data-stu-id="b5cff-110">See [**ID3DXFile**](id3dxfile.md).</span></span> <span data-ttu-id="b5cff-111">Non utilizzare questo parametro per aggiungere oggetti dati.</span><span class="sxs-lookup"><span data-stu-id="b5cff-111">Do not use this parameter to add data objects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5cff-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5cff-112">Return value</span></span>

<span data-ttu-id="b5cff-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b5cff-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b5cff-114">I valori restituiti da questo metodo sono implementati da un programmatore di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="b5cff-114">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="b5cff-115">In generale, se non si verificano errori, programmare il metodo per restituire D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b5cff-115">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="b5cff-116">In caso contrario, programmare il metodo per restituire un messaggio di errore appropriato da [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md), in quanto questa operazione causerà l'esito negativo anche di [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) e restituirà l'errore.</span><span class="sxs-lookup"><span data-stu-id="b5cff-116">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md), as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5cff-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5cff-117">Remarks</span></span>

<span data-ttu-id="b5cff-118">**ID3DXSaveUserData:: RegisterTemplates** e [**ID3DXSaveUserData:: SaveTemplates**](id3dxsaveuserdata--savetemplates.md) forniscono un meccanismo per l'aggiunta di un modello a un file con estensione x per il salvataggio dei dati utente.</span><span class="sxs-lookup"><span data-stu-id="b5cff-118">**ID3DXSaveUserData::RegisterTemplates** and [**ID3DXSaveUserData::SaveTemplates**](id3dxsaveuserdata--savetemplates.md) provide a mechanism for adding a template to a .x file for saving user data.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5cff-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5cff-119">Requirements</span></span>



| <span data-ttu-id="b5cff-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5cff-120">Requirement</span></span> | <span data-ttu-id="b5cff-121">Valore</span><span class="sxs-lookup"><span data-stu-id="b5cff-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5cff-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b5cff-122">Header</span></span><br/>  | <dl> <span data-ttu-id="b5cff-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5cff-123"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="b5cff-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="b5cff-124">Library</span></span><br/> | <dl> <span data-ttu-id="b5cff-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5cff-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b5cff-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5cff-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5cff-127">ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="b5cff-127">ID3DXSaveUserData</span></span>](id3dxsaveuserdata.md)
</dt> </dl>

 

 

---
description: Aggiunge un oggetto dati come figlio del nodo dati del file ID3DXFileSaveData.
ms.assetid: 47faad99-3ee8-4ca8-b8d7-413d4cd5b090
title: 'Metodo ID3DXFileSaveData:: AddDataObject (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.AddDataObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b097e63792b32bc1688ce93c8ce32ffaedeae6ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355219"
---
# <a name="id3dxfilesavedataadddataobject-method"></a><span data-ttu-id="95b6e-103">Metodo ID3DXFileSaveData:: AddDataObject</span><span class="sxs-lookup"><span data-stu-id="95b6e-103">ID3DXFileSaveData::AddDataObject method</span></span>

<span data-ttu-id="95b6e-104">Aggiunge un oggetto dati come figlio del nodo dati del file [**ID3DXFileSaveData**](id3dxfilesavedata.md) .</span><span class="sxs-lookup"><span data-stu-id="95b6e-104">Adds a data object as a child of the [**ID3DXFileSaveData**](id3dxfilesavedata.md) file data node.</span></span>

## <a name="syntax"></a><span data-ttu-id="95b6e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="95b6e-105">Syntax</span></span>


```C++
HRESULT AddDataObject(
  [in]               REFGUID           rguidTemplate,
  [in]               LPCSTR            szName,
  [in]         const GUID              *pId,
  [in]               SIZE_T            cbSize,
  [in]               LPCVOID           pvData,
  [in, retval]       ID3DXFileSaveData **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="95b6e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="95b6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95b6e-107">*rguidTemplate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95b6e-107">*rguidTemplate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95b6e-108">Tipo: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="95b6e-108">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="95b6e-109">GUID che rappresenta il modello dell'oggetto dati.</span><span class="sxs-lookup"><span data-stu-id="95b6e-109">GUID representing the data object's template.</span></span>

</dd> <dt>

<span data-ttu-id="95b6e-110">*szName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95b6e-110">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95b6e-111">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95b6e-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95b6e-112">Puntatore al nome dell'oggetto dati da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="95b6e-112">Pointer to the name of the data object to add.</span></span> <span data-ttu-id="95b6e-113">Specificare **null** se l'oggetto non ha un nome.</span><span class="sxs-lookup"><span data-stu-id="95b6e-113">Specify **NULL** if the object does not have a name.</span></span>

</dd> <dt>

<span data-ttu-id="95b6e-114">*PID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95b6e-114">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95b6e-115">Tipo: **[**GUID**](guid.md) \* const**</span><span class="sxs-lookup"><span data-stu-id="95b6e-115">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="95b6e-116">Puntatore a un GUID che rappresenta l'oggetto dati.</span><span class="sxs-lookup"><span data-stu-id="95b6e-116">Pointer to a GUID representing the data object.</span></span> <span data-ttu-id="95b6e-117">L'oggetto dati deve essere stato registrato con [**ID3DXFile:: RegisterTemplates**](id3dxfile--registertemplates.md) o [**ID3DXFile:: RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md).</span><span class="sxs-lookup"><span data-stu-id="95b6e-117">The data object must have been registered with [**ID3DXFile::RegisterTemplates**](id3dxfile--registertemplates.md) or [**ID3DXFile::RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md).</span></span> <span data-ttu-id="95b6e-118">Specificare **null** se l'oggetto non dispone di un GUID.</span><span class="sxs-lookup"><span data-stu-id="95b6e-118">Specify **NULL** if the object does not have a GUID.</span></span>

</dd> <dt>

<span data-ttu-id="95b6e-119">*cbSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95b6e-119">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95b6e-120">Tipo: **[ **size \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95b6e-120">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95b6e-121">Dimensioni dell'oggetto dati, in byte.</span><span class="sxs-lookup"><span data-stu-id="95b6e-121">Size of the data object, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="95b6e-122">*pvData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95b6e-122">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95b6e-123">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95b6e-123">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95b6e-124">Puntatore a un buffer contenente tutti i dati necessari nell'oggetto dati.</span><span class="sxs-lookup"><span data-stu-id="95b6e-124">Pointer to a buffer containing all required data in the data object.</span></span>

</dd> <dt>

<span data-ttu-id="95b6e-125">*ppObj* \[ in, retval\]</span><span class="sxs-lookup"><span data-stu-id="95b6e-125">*ppObj* \[in, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="95b6e-126">Tipo: **[ **ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="95b6e-126">Type: **[**ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***</span></span>

<span data-ttu-id="95b6e-127">Indirizzo di un puntatore a un'interfaccia [**ID3DXFileSaveData**](id3dxfilesavedata.md) , che rappresenta il nodo dati del file a cui verrà aggiunto l'oggetto dati.</span><span class="sxs-lookup"><span data-stu-id="95b6e-127">Address of a pointer to an [**ID3DXFileSaveData**](id3dxfilesavedata.md) interface, representing the file data node to which the data object will be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95b6e-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="95b6e-128">Return value</span></span>

<span data-ttu-id="95b6e-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="95b6e-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="95b6e-130">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="95b6e-130">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="95b6e-131">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DXFERR \_ BADOBJECT, D3DXFERR \_ BADVALUE, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="95b6e-131">If the method fails, the return value can be one of the following: D3DXFERR\_BADOBJECT, D3DXFERR\_BADVALUE, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="95b6e-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95b6e-132">Requirements</span></span>



| <span data-ttu-id="95b6e-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="95b6e-133">Requirement</span></span> | <span data-ttu-id="95b6e-134">Valore</span><span class="sxs-lookup"><span data-stu-id="95b6e-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95b6e-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="95b6e-135">Header</span></span><br/>  | <dl> <span data-ttu-id="95b6e-136"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="95b6e-136"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="95b6e-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="95b6e-137">Library</span></span><br/> | <dl> <span data-ttu-id="95b6e-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95b6e-138"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="95b6e-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="95b6e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95b6e-140">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="95b6e-140">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 

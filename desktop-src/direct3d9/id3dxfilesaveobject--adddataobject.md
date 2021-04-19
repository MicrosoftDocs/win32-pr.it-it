---
description: Aggiunge un oggetto dati come figlio dell'oggetto ID3DXFileSaveData.
ms.assetid: 710a1588-d766-4555-97a3-4b5a517ce805
title: 'Metodo ID3DXFileSaveObject:: AddDataObject (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.AddDataObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d1586035a0d8a81c2210009bad903aac5197bcf7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322622"
---
# <a name="id3dxfilesaveobjectadddataobject-method"></a><span data-ttu-id="fc53a-103">Metodo ID3DXFileSaveObject:: AddDataObject</span><span class="sxs-lookup"><span data-stu-id="fc53a-103">ID3DXFileSaveObject::AddDataObject method</span></span>

<span data-ttu-id="fc53a-104">Aggiunge un oggetto dati come figlio dell'oggetto [**ID3DXFileSaveData**](id3dxfilesavedata.md) .</span><span class="sxs-lookup"><span data-stu-id="fc53a-104">Adds a data object as a child of the [**ID3DXFileSaveData**](id3dxfilesavedata.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc53a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc53a-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="fc53a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc53a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc53a-107">*rguidTemplate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc53a-107">*rguidTemplate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc53a-108">Tipo: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="fc53a-108">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="fc53a-109">GUID che rappresenta il modello dell'oggetto dati.</span><span class="sxs-lookup"><span data-stu-id="fc53a-109">GUID representing the data object's template.</span></span>

</dd> <dt>

<span data-ttu-id="fc53a-110">*szName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc53a-110">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc53a-111">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc53a-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fc53a-112">Puntatore al nome dell'oggetto dati.</span><span class="sxs-lookup"><span data-stu-id="fc53a-112">Pointer to the name of the data object.</span></span> <span data-ttu-id="fc53a-113">Specificare **null** se l'oggetto non ha un nome.</span><span class="sxs-lookup"><span data-stu-id="fc53a-113">Specify **NULL** if the object does not have a name.</span></span>

</dd> <dt>

<span data-ttu-id="fc53a-114">*PID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc53a-114">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc53a-115">Tipo: **[**GUID**](guid.md) \* const**</span><span class="sxs-lookup"><span data-stu-id="fc53a-115">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="fc53a-116">Puntatore a un GUID che rappresenta l'oggetto dati.</span><span class="sxs-lookup"><span data-stu-id="fc53a-116">Pointer to a GUID representing the data object.</span></span> <span data-ttu-id="fc53a-117">Specificare **null** se l'oggetto non dispone di un GUID.</span><span class="sxs-lookup"><span data-stu-id="fc53a-117">Specify **NULL** if the object does not have a GUID.</span></span>

</dd> <dt>

<span data-ttu-id="fc53a-118">*cbSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc53a-118">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc53a-119">Tipo: **[ **size \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc53a-119">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fc53a-120">Dimensioni dell'oggetto dati, in byte.</span><span class="sxs-lookup"><span data-stu-id="fc53a-120">Size of the data object, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="fc53a-121">*pvData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fc53a-121">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc53a-122">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc53a-122">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fc53a-123">Puntatore a un buffer contenente tutti i dati necessari nell'oggetto dati.</span><span class="sxs-lookup"><span data-stu-id="fc53a-123">Pointer to a buffer containing all required data in the data object.</span></span>

</dd> <dt>

<span data-ttu-id="fc53a-124">*ppObj* \[ in, retval\]</span><span class="sxs-lookup"><span data-stu-id="fc53a-124">*ppObj* \[in, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="fc53a-125">Tipo: **[ **ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="fc53a-125">Type: **[**ID3DXFileSaveData**](id3dxfilesavedata.md)\*\***</span></span>

<span data-ttu-id="fc53a-126">Indirizzo di un puntatore a un'interfaccia [**ID3DXFileSaveData**](id3dxfilesavedata.md) , che rappresenta il nodo dati del file a cui verrà aggiunto l'oggetto dati.</span><span class="sxs-lookup"><span data-stu-id="fc53a-126">Address of a pointer to an [**ID3DXFileSaveData**](id3dxfilesavedata.md) interface, representing the file data node to which the data object will be added.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc53a-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fc53a-127">Return value</span></span>

<span data-ttu-id="fc53a-128">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fc53a-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fc53a-129">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fc53a-129">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="fc53a-130">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DXFERR \_ BADOBJECT, DXFILEERR \_ BADVALUE, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="fc53a-130">If the method fails, the return value can be one of the following: D3DXFERR\_BADOBJECT, DXFILEERR\_BADVALUE, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc53a-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc53a-131">Remarks</span></span>

<span data-ttu-id="fc53a-132">Se un oggetto riferimento ai dati fa riferimento all'oggetto dati, il szName o il parametro pId deve essere non **null**.</span><span class="sxs-lookup"><span data-stu-id="fc53a-132">If a data reference object will reference the data object, either the szName or pId parameter must be non-**NULL**.</span></span>

<span data-ttu-id="fc53a-133">Salvare i dati creati su disco usando il metodo [**ID3DXFileSaveObject:: Save**](id3dxfilesaveobject--save.md) .</span><span class="sxs-lookup"><span data-stu-id="fc53a-133">Save the created data to disk by using the [**ID3DXFileSaveObject::Save**](id3dxfilesaveobject--save.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc53a-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc53a-134">Requirements</span></span>



| <span data-ttu-id="fc53a-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc53a-135">Requirement</span></span> | <span data-ttu-id="fc53a-136">Valore</span><span class="sxs-lookup"><span data-stu-id="fc53a-136">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fc53a-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fc53a-137">Header</span></span><br/>  | <dl> <span data-ttu-id="fc53a-138"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc53a-138"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="fc53a-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="fc53a-139">Library</span></span><br/> | <dl> <span data-ttu-id="fc53a-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc53a-140"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="fc53a-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc53a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc53a-142">ID3DXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="fc53a-142">ID3DXFileSaveObject</span></span>](id3dxfilesaveobject.md)
</dt> </dl>

 

 

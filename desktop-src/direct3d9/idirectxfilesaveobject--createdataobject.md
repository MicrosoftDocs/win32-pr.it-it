---
description: Crea un oggetto dati. Deprecato.
ms.assetid: bb0ef2cf-db76-40f6-968f-3599c58459a7
title: 'Metodo IDirectXFileSaveObject:: CreateDataObject (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.CreateDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 7c5a67a72f6ff5a63730167d2fe2d12213a9ab72
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354674"
---
# <a name="idirectxfilesaveobjectcreatedataobject-method"></a><span data-ttu-id="0e224-104">Metodo IDirectXFileSaveObject:: CreateDataObject</span><span class="sxs-lookup"><span data-stu-id="0e224-104">IDirectXFileSaveObject::CreateDataObject method</span></span>

<span data-ttu-id="0e224-105">Crea un oggetto dati.</span><span class="sxs-lookup"><span data-stu-id="0e224-105">Creates a data object.</span></span> <span data-ttu-id="0e224-106">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="0e224-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e224-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e224-107">Syntax</span></span>


```C++
HRESULT CreateDataObject(
  [in]                REFGUID           rguidTemplate,
  [in]                LPCSTR            szName,
  [in]          const GUID              *pguid,
  [in]                DWORD             cbSize,
  [in]                LPVOID            pvData,
  [out, retval]       LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="0e224-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0e224-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e224-109">*rguidTemplate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e224-109">*rguidTemplate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e224-110">Tipo: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="0e224-110">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="0e224-111">GUID che rappresenta il modello dell'oggetto dati.</span><span class="sxs-lookup"><span data-stu-id="0e224-111">GUID representing the data object's template.</span></span>

</dd> <dt>

<span data-ttu-id="0e224-112">*szName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e224-112">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e224-113">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0e224-113">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0e224-114">Puntatore al nome dell'oggetto dati.</span><span class="sxs-lookup"><span data-stu-id="0e224-114">Pointer to the name of the data object.</span></span> <span data-ttu-id="0e224-115">Specificare **null** se l'oggetto non ha un nome.</span><span class="sxs-lookup"><span data-stu-id="0e224-115">Specify **NULL** if the object does not have a name.</span></span>

</dd> <dt>

<span data-ttu-id="0e224-116">*pguid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e224-116">*pguid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e224-117">Tipo: **[**GUID**](guid.md) \* const**</span><span class="sxs-lookup"><span data-stu-id="0e224-117">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="0e224-118">Puntatore a un GUID che rappresenta l'oggetto dati.</span><span class="sxs-lookup"><span data-stu-id="0e224-118">Pointer to a GUID representing the data object.</span></span> <span data-ttu-id="0e224-119">Specificare **null** se l'oggetto non dispone di un GUID.</span><span class="sxs-lookup"><span data-stu-id="0e224-119">Specify **NULL** if the object does not have a GUID.</span></span>

</dd> <dt>

<span data-ttu-id="0e224-120">*cbSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e224-120">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e224-121">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0e224-121">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0e224-122">Dimensioni dell'oggetto dati, in byte.</span><span class="sxs-lookup"><span data-stu-id="0e224-122">Size of the data object, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="0e224-123">*pvData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e224-123">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e224-124">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0e224-124">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0e224-125">Puntatore a un buffer contenente tutti i dati del membro richiesti.</span><span class="sxs-lookup"><span data-stu-id="0e224-125">Pointer to a buffer containing all required member's data.</span></span>

</dd> <dt>

<span data-ttu-id="0e224-126">*ppDataObj* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="0e224-126">*ppDataObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0e224-127">Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="0e224-127">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="0e224-128">Indirizzo di un puntatore a un'interfaccia [**IDirectXFileData**](idirectxfiledata.md) , che rappresenta l'oggetto dati del file creato.</span><span class="sxs-lookup"><span data-stu-id="0e224-128">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the created file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e224-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0e224-129">Return value</span></span>

<span data-ttu-id="0e224-130">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0e224-130">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0e224-131">Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0e224-131">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="0e224-132">Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE</span><span class="sxs-lookup"><span data-stu-id="0e224-132">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="remarks"></a><span data-ttu-id="0e224-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="0e224-133">Remarks</span></span>

<span data-ttu-id="0e224-134">Se un oggetto riferimento ai dati fa riferimento all'oggetto dati, il parametro szName o pguid deve essere non **null**.</span><span class="sxs-lookup"><span data-stu-id="0e224-134">If a data reference object will reference the data object, either the szName or pguid parameter must be non-**NULL**.</span></span>

<span data-ttu-id="0e224-135">Salvare i modelli usando il metodo [**IDirectXFileSaveObject:: SaveTemplates**](idirectxfilesaveobject--savetemplates.md) prima di salvare i dati creati da questo metodo.</span><span class="sxs-lookup"><span data-stu-id="0e224-135">Save any templates by using the [**IDirectXFileSaveObject::SaveTemplates**](idirectxfilesaveobject--savetemplates.md) method before saving the data created by this method.</span></span> <span data-ttu-id="0e224-136">Salvare i dati creati usando il metodo [**IDirectXFileSaveObject:: SaveData**](idirectxfilesaveobject--savedata.md) .</span><span class="sxs-lookup"><span data-stu-id="0e224-136">Save the created data by using the [**IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md) method.</span></span>

<span data-ttu-id="0e224-137">Se è necessario salvare i dati facoltativi, usare il metodo [**IDirectXFileData:: AddDataObject**](idirectxfiledata--adddataobject.md) dopo aver usato questo metodo e prima di usare [**IDirectXFileSaveObject:: SaveData**](idirectxfilesaveobject--savedata.md).</span><span class="sxs-lookup"><span data-stu-id="0e224-137">If you need to save optional data, use the [**IDirectXFileData::AddDataObject**](idirectxfiledata--adddataobject.md) method after using this method and before using [**IDirectXFileSaveObject::SaveData**](idirectxfilesaveobject--savedata.md).</span></span> <span data-ttu-id="0e224-138">Se l'oggetto dispone di oggetti figlio, aggiungerli prima di chiamare **IDirectXFileSaveObject:: SaveData**.</span><span class="sxs-lookup"><span data-stu-id="0e224-138">If the object has child objects, add them before calling **IDirectXFileSaveObject::SaveData**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e224-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e224-139">Requirements</span></span>



| <span data-ttu-id="0e224-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e224-140">Requirement</span></span> | <span data-ttu-id="0e224-141">Valore</span><span class="sxs-lookup"><span data-stu-id="0e224-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e224-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0e224-142">Header</span></span><br/>  | <dl> <span data-ttu-id="0e224-143"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e224-143"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="0e224-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="0e224-144">Library</span></span><br/> | <dl> <span data-ttu-id="0e224-145"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e224-145"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e224-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e224-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e224-147">IDirectXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="0e224-147">IDirectXFileSaveObject</span></span>](idirectxfilesaveobject.md)
</dt> <dt>

[<span data-ttu-id="0e224-148">**IDirectXFileData::AddDataObject**</span><span class="sxs-lookup"><span data-stu-id="0e224-148">**IDirectXFileData::AddDataObject**</span></span>](idirectxfiledata--adddataobject.md)
</dt> <dt>

[<span data-ttu-id="0e224-149">**IDirectXFileSaveObject:: SaveData**</span><span class="sxs-lookup"><span data-stu-id="0e224-149">**IDirectXFileSaveObject::SaveData**</span></span>](idirectxfilesaveobject--savedata.md)
</dt> <dt>

[<span data-ttu-id="0e224-150">**IDirectXFileSaveObject::SaveTemplates**</span><span class="sxs-lookup"><span data-stu-id="0e224-150">**IDirectXFileSaveObject::SaveTemplates**</span></span>](idirectxfilesaveobject--savetemplates.md)
</dt> </dl>

 

 

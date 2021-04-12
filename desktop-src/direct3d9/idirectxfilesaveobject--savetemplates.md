---
description: Salva i modelli in un file DirectX. Deprecato.
ms.assetid: 7a45565a-8c04-4fa1-a424-294b847d3a2f
title: 'Metodo IDirectXFileSaveObject:: SaveTemplates (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.SaveTemplates
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 3c63ae2e0f211aa8e7064161d03a66cafe1e8289
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354669"
---
# <a name="idirectxfilesaveobjectsavetemplates-method"></a><span data-ttu-id="d47e3-104">Metodo IDirectXFileSaveObject:: SaveTemplates</span><span class="sxs-lookup"><span data-stu-id="d47e3-104">IDirectXFileSaveObject::SaveTemplates method</span></span>

<span data-ttu-id="d47e3-105">Salva i modelli in un file DirectX.</span><span class="sxs-lookup"><span data-stu-id="d47e3-105">Saves templates to a DirectX file.</span></span> <span data-ttu-id="d47e3-106">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="d47e3-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="d47e3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d47e3-107">Syntax</span></span>


```C++
HRESULT SaveTemplates(
  [in]       DWORD cTemplates,
  [in] const GUID  **ppguidTemplates
);
```



## <a name="parameters"></a><span data-ttu-id="d47e3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d47e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d47e3-109">*cTemplates* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d47e3-109">*cTemplates* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d47e3-110">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d47e3-110">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d47e3-111">Numero totale di modelli da salvare.</span><span class="sxs-lookup"><span data-stu-id="d47e3-111">Total number of templates to save.</span></span>

</dd> <dt>

<span data-ttu-id="d47e3-112">*ppguidTemplates* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d47e3-112">*ppguidTemplates* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d47e3-113">Tipo: **[**GUID**](guid.md) \* \* const**</span><span class="sxs-lookup"><span data-stu-id="d47e3-113">Type: **const [**GUID**](guid.md)\*\***</span></span>

<span data-ttu-id="d47e3-114">Indirizzo di un puntatore a una matrice di GUID per tutti i modelli da salvare.</span><span class="sxs-lookup"><span data-stu-id="d47e3-114">Address of a pointer to an array of the GUIDs for all templates to save.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d47e3-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d47e3-115">Return value</span></span>

<span data-ttu-id="d47e3-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d47e3-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d47e3-117">Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d47e3-117">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="d47e3-118">Se il metodo ha esito negativo, il valore restituito può essere DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="d47e3-118">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="d47e3-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="d47e3-119">Remarks</span></span>

<span data-ttu-id="d47e3-120">Il seguente frammento di codice fornisce una chiamata di esempio a **IDirectXFileSaveObject:: SaveTemplates** e il contenuto di esempio per la matrice a cui punta ppguidTemplates.</span><span class="sxs-lookup"><span data-stu-id="d47e3-120">The following code fragment provides an example call to **IDirectXFileSaveObject::SaveTemplates** and example contents for the array to which ppguidTemplates points.</span></span>


```
IDirectXFileSaveObject * pDXFileSaveObject;
    
const GUID *aIds[] = {
    &DXFILEOBJ_SimpleData,
    &DXFILEOBJ_ArrayData,
    &DXFILEOBJ_RestrictedData};
    
hr = pDXFileSaveObject->SaveTemplates(3, aIds);
```



<span data-ttu-id="d47e3-121">Dopo aver usato questo metodo per salvare i modelli, usare il metodo [**IDirectXFileSaveObject:: CreateDataObject**](idirectxfilesaveobject--createdataobject.md) per creare un oggetto dati.</span><span class="sxs-lookup"><span data-stu-id="d47e3-121">After using this method to save the templates, use the [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) method to create a data object.</span></span>

## <a name="requirements"></a><span data-ttu-id="d47e3-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d47e3-122">Requirements</span></span>



| <span data-ttu-id="d47e3-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d47e3-123">Requirement</span></span> | <span data-ttu-id="d47e3-124">Valore</span><span class="sxs-lookup"><span data-stu-id="d47e3-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d47e3-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d47e3-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d47e3-126"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="d47e3-126"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="d47e3-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="d47e3-127">Library</span></span><br/> | <dl> <span data-ttu-id="d47e3-128"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d47e3-128"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d47e3-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d47e3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d47e3-130">IDirectXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="d47e3-130">IDirectXFileSaveObject</span></span>](idirectxfilesaveobject.md)
</dt> <dt>

[<span data-ttu-id="d47e3-131">**IDirectXFileSaveObject::CreateDataObject**</span><span class="sxs-lookup"><span data-stu-id="d47e3-131">**IDirectXFileSaveObject::CreateDataObject**</span></span>](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 

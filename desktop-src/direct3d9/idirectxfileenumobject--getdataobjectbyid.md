---
description: Recupera l'oggetto dati con il GUID specificato. Deprecato.
ms.assetid: dd079b5c-18e1-4252-aabd-498c24910a08
title: 'Metodo IDirectXFileEnumObject:: GetDataObjectById (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetDataObjectById
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: a27ac17963d4876a3cb0a26d05b63f4c34bf99fc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322049"
---
# <a name="idirectxfileenumobjectgetdataobjectbyid-method"></a><span data-ttu-id="5e9a3-104">Metodo IDirectXFileEnumObject:: GetDataObjectById</span><span class="sxs-lookup"><span data-stu-id="5e9a3-104">IDirectXFileEnumObject::GetDataObjectById method</span></span>

<span data-ttu-id="5e9a3-105">Recupera l'oggetto dati con il GUID specificato.</span><span class="sxs-lookup"><span data-stu-id="5e9a3-105">Retrieves the data object that has the specified GUID.</span></span> <span data-ttu-id="5e9a3-106">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="5e9a3-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e9a3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5e9a3-107">Syntax</span></span>


```C++
HRESULT GetDataObjectById(
  [in]  REFGUID           rguid,
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="5e9a3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5e9a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e9a3-109">*rguid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5e9a3-109">*rguid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e9a3-110">Tipo: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="5e9a3-110">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="5e9a3-111">Riferimento al GUID richiesto.</span><span class="sxs-lookup"><span data-stu-id="5e9a3-111">Reference to the requested GUID.</span></span>

</dd> <dt>

<span data-ttu-id="5e9a3-112">*ppDataObj* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5e9a3-112">*ppDataObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e9a3-113">Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="5e9a3-113">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="5e9a3-114">Indirizzo di un puntatore a un'interfaccia [**IDirectXFileData**](idirectxfiledata.md) , che rappresenta l'oggetto dati di file restituito.</span><span class="sxs-lookup"><span data-stu-id="5e9a3-114">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e9a3-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5e9a3-115">Return value</span></span>

<span data-ttu-id="5e9a3-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5e9a3-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5e9a3-117">Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5e9a3-117">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="5e9a3-118">Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: DXFILEERR \_ BADVALUE, DXFILEERR \_ NotFound.</span><span class="sxs-lookup"><span data-stu-id="5e9a3-118">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e9a3-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e9a3-119">Requirements</span></span>



| <span data-ttu-id="5e9a3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e9a3-120">Requirement</span></span> | <span data-ttu-id="5e9a3-121">Valore</span><span class="sxs-lookup"><span data-stu-id="5e9a3-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5e9a3-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5e9a3-122">Header</span></span><br/>  | <dl> <span data-ttu-id="5e9a3-123"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e9a3-123"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e9a3-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="5e9a3-124">Library</span></span><br/> | <dl> <span data-ttu-id="5e9a3-125"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e9a3-125"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e9a3-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e9a3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e9a3-127">IDirectXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="5e9a3-127">IDirectXFileEnumObject</span></span>](idirectxfileenumobject.md)
</dt> </dl>

 

 

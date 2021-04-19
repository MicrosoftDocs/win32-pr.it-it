---
description: Recupera l'oggetto dati con il nome specificato. Deprecato.
ms.assetid: d04d5a45-72d9-4256-8700-378e8139ed36
title: 'Metodo IDirectXFileEnumObject:: GetDataObjectByName (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetDataObjectByName
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 858097139702770d148765c4c9a57f6522d9633b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323435"
---
# <a name="idirectxfileenumobjectgetdataobjectbyname-method"></a><span data-ttu-id="64f1d-104">Metodo IDirectXFileEnumObject:: GetDataObjectByName</span><span class="sxs-lookup"><span data-stu-id="64f1d-104">IDirectXFileEnumObject::GetDataObjectByName method</span></span>

<span data-ttu-id="64f1d-105">Recupera l'oggetto dati con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="64f1d-105">Retrieves the data object that has the specified name.</span></span> <span data-ttu-id="64f1d-106">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="64f1d-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="64f1d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="64f1d-107">Syntax</span></span>


```C++
HRESULT GetDataObjectByName(
  [in]  LPCSTR            szName,
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="64f1d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="64f1d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64f1d-109">*szName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="64f1d-109">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64f1d-110">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="64f1d-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="64f1d-111">Puntatore al nome richiesto.</span><span class="sxs-lookup"><span data-stu-id="64f1d-111">Pointer to the requested name.</span></span>

</dd> <dt>

<span data-ttu-id="64f1d-112">*ppDataObj* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="64f1d-112">*ppDataObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64f1d-113">Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="64f1d-113">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="64f1d-114">Indirizzo di un puntatore a un'interfaccia [**IDirectXFileData**](idirectxfiledata.md) , che rappresenta l'oggetto dati di file restituito.</span><span class="sxs-lookup"><span data-stu-id="64f1d-114">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64f1d-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="64f1d-115">Return value</span></span>

<span data-ttu-id="64f1d-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="64f1d-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="64f1d-117">Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="64f1d-117">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="64f1d-118">Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: DXFILEERR \_ BADVALUE, DXFILEERR \_ NotFound.</span><span class="sxs-lookup"><span data-stu-id="64f1d-118">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="64f1d-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64f1d-119">Requirements</span></span>



| <span data-ttu-id="64f1d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="64f1d-120">Requirement</span></span> | <span data-ttu-id="64f1d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="64f1d-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="64f1d-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="64f1d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="64f1d-123"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="64f1d-123"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="64f1d-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="64f1d-124">Library</span></span><br/> | <dl> <span data-ttu-id="64f1d-125"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="64f1d-125"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64f1d-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="64f1d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64f1d-127">IDirectXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="64f1d-127">IDirectXFileEnumObject</span></span>](idirectxfileenumobject.md)
</dt> </dl>

 

 

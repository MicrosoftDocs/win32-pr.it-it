---
description: Crea un oggetto binario e lo aggiunge come oggetto figlio. Deprecato.
ms.assetid: 6164951d-dd87-4318-ac08-b97c22f58d45
title: 'Metodo IDirectXFileData:: AddBinaryObject (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddBinaryObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 8373b9c4328a8683f32c1fe7ab979cb8d7636f87
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234947"
---
# <a name="idirectxfiledataaddbinaryobject-method"></a><span data-ttu-id="42031-104">Metodo IDirectXFileData:: AddBinaryObject</span><span class="sxs-lookup"><span data-stu-id="42031-104">IDirectXFileData::AddBinaryObject method</span></span>

<span data-ttu-id="42031-105">Crea un oggetto binario e lo aggiunge come oggetto figlio.</span><span class="sxs-lookup"><span data-stu-id="42031-105">Creates a binary object and adds it as a child object.</span></span> <span data-ttu-id="42031-106">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="42031-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="42031-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42031-107">Syntax</span></span>


```C++
HRESULT AddBinaryObject(
  [in]       LPCSTR szName,
  [in] const GUID   *pguid,
  [in]       LPCSTR szMimeType,
  [in]       LPVOID pvData,
  [in]       DWORD  cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="42031-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="42031-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42031-109">*szName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42031-109">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42031-110">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="42031-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="42031-111">Puntatore al nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="42031-111">Pointer to the name of the object.</span></span> <span data-ttu-id="42031-112">Specificare **null** se l'oggetto non necessita di un nome.</span><span class="sxs-lookup"><span data-stu-id="42031-112">Specify **NULL** if the object does not need a name.</span></span>

</dd> <dt>

<span data-ttu-id="42031-113">*pguid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42031-113">*pguid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42031-114">Tipo: **[**GUID**](guid.md) \* const**</span><span class="sxs-lookup"><span data-stu-id="42031-114">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="42031-115">Puntatore al GUID che rappresenta l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="42031-115">Pointer to the GUID representing the object.</span></span> <span data-ttu-id="42031-116">Specificare **null** se l'oggetto non necessita di un GUID.</span><span class="sxs-lookup"><span data-stu-id="42031-116">Specify **NULL** if the object does not need a GUID.</span></span>

</dd> <dt>

<span data-ttu-id="42031-117">*szMimeType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42031-117">*szMimeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42031-118">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="42031-118">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="42031-119">Puntatore al tipo MIME dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="42031-119">Pointer to the object's MIME type.</span></span>

</dd> <dt>

<span data-ttu-id="42031-120">*pvData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42031-120">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42031-121">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="42031-121">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="42031-122">Puntatore ai dati dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="42031-122">Pointer to the object's data.</span></span>

</dd> <dt>

<span data-ttu-id="42031-123">*cbSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42031-123">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42031-124">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="42031-124">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="42031-125">Dimensioni del buffer a cui punta pvData in byte.</span><span class="sxs-lookup"><span data-stu-id="42031-125">Size of the buffer pointed to by pvData, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42031-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="42031-126">Return value</span></span>

<span data-ttu-id="42031-127">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="42031-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="42031-128">Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="42031-128">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="42031-129">Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE</span><span class="sxs-lookup"><span data-stu-id="42031-129">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="42031-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42031-130">Requirements</span></span>



| <span data-ttu-id="42031-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="42031-131">Requirement</span></span> | <span data-ttu-id="42031-132">Valore</span><span class="sxs-lookup"><span data-stu-id="42031-132">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="42031-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="42031-133">Header</span></span><br/>  | <dl> <span data-ttu-id="42031-134"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="42031-134"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="42031-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="42031-135">Library</span></span><br/> | <dl> <span data-ttu-id="42031-136"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="42031-136"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42031-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42031-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42031-138">IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="42031-138">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> <dt>

[<span data-ttu-id="42031-139">**IDirectXFileBinary:: GetMimeType**</span><span class="sxs-lookup"><span data-stu-id="42031-139">**IDirectXFileBinary::GetMimeType**</span></span>](idirectxfilebinary--getmimetype.md)
</dt> </dl>

 

 

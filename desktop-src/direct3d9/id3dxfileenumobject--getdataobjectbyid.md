---
description: Recupera l'oggetto dati con il GUID specificato.
ms.assetid: c3d598bd-0646-4f99-8517-4475ef7cd8c9
title: 'Metodo ID3DXFileEnumObject:: GetDataObjectById (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetDataObjectById
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 82a74ca4ff472d678ded92aa01f2c2406560955e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323064"
---
# <a name="id3dxfileenumobjectgetdataobjectbyid-method"></a><span data-ttu-id="45379-103">Metodo ID3DXFileEnumObject:: GetDataObjectById</span><span class="sxs-lookup"><span data-stu-id="45379-103">ID3DXFileEnumObject::GetDataObjectById method</span></span>

<span data-ttu-id="45379-104">Recupera l'oggetto dati con il GUID specificato.</span><span class="sxs-lookup"><span data-stu-id="45379-104">Retrieves the data object that has the specified GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="45379-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="45379-105">Syntax</span></span>


```C++
HRESULT GetDataObjectById(
  [in]  REFGUID        rguid,
  [out] LPD3DXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="45379-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="45379-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45379-107">*rguid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="45379-107">*rguid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45379-108">Tipo: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span><span class="sxs-lookup"><span data-stu-id="45379-108">Type: **[REFGUID](/openspecs/windows_protocols/ms-oaut/6e7d7108-c213-40bc-8294-ac13fe68fd50)**</span></span>

<span data-ttu-id="45379-109">Riferimento al GUID richiesto.</span><span class="sxs-lookup"><span data-stu-id="45379-109">Reference to the requested GUID.</span></span>

</dd> <dt>

<span data-ttu-id="45379-110">*ppDataObj* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="45379-110">*ppDataObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45379-111">Tipo: **[ **LPD3DXFILEDATA**](id3dxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="45379-111">Type: **[**LPD3DXFILEDATA**](id3dxfiledata.md)\***</span></span>

<span data-ttu-id="45379-112">Indirizzo di un puntatore a un'interfaccia [**ID3DXFileData**](id3dxfiledata.md) , che rappresenta l'oggetto dati di file restituito.</span><span class="sxs-lookup"><span data-stu-id="45379-112">Address of a pointer to an [**ID3DXFileData**](id3dxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45379-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="45379-113">Return value</span></span>

<span data-ttu-id="45379-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="45379-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="45379-115">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="45379-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="45379-116">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: DXFILEERR \_ BADVALUE, DXFILEERR \_ NotFound.</span><span class="sxs-lookup"><span data-stu-id="45379-116">If the method fails, the return value can be one of the following:DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="45379-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="45379-117">Remarks</span></span>

<span data-ttu-id="45379-118">Ottenere il GUID rguid dell'oggetto dati del file corrente con il metodo [**ID3DXFileData:: GetId**](id3dxfiledata--getid.md) .</span><span class="sxs-lookup"><span data-stu-id="45379-118">Obtain the GUID rguid of the current file data object with the [**ID3DXFileData::GetId**](id3dxfiledata--getid.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="45379-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45379-119">Requirements</span></span>



| <span data-ttu-id="45379-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="45379-120">Requirement</span></span> | <span data-ttu-id="45379-121">Valore</span><span class="sxs-lookup"><span data-stu-id="45379-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="45379-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="45379-122">Header</span></span><br/>  | <dl> <span data-ttu-id="45379-123"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="45379-123"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="45379-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="45379-124">Library</span></span><br/> | <dl> <span data-ttu-id="45379-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="45379-125"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="45379-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="45379-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45379-127">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="45379-127">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 

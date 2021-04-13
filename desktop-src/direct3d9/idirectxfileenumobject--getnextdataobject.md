---
description: Recupera l'oggetto di primo livello successivo nel file DirectX. Deprecato.
ms.assetid: 91cd3205-5603-4a62-aab2-7ef4adb9e6d1
title: 'Metodo IDirectXFileEnumObject:: GetNextDataObject (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetNextDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: bc50af216eaae1687351d472b7151aaaeae9116f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354229"
---
# <a name="idirectxfileenumobjectgetnextdataobject-method"></a><span data-ttu-id="dd7b1-104">Metodo IDirectXFileEnumObject:: GetNextDataObject</span><span class="sxs-lookup"><span data-stu-id="dd7b1-104">IDirectXFileEnumObject::GetNextDataObject method</span></span>

<span data-ttu-id="dd7b1-105">Recupera l'oggetto di primo livello successivo nel file DirectX.</span><span class="sxs-lookup"><span data-stu-id="dd7b1-105">Retrieves the next top-level object in the DirectX file.</span></span> <span data-ttu-id="dd7b1-106">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="dd7b1-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd7b1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dd7b1-107">Syntax</span></span>


```C++
HRESULT GetNextDataObject(
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="dd7b1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="dd7b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd7b1-109">*ppDataObj* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dd7b1-109">*ppDataObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd7b1-110">Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="dd7b1-110">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="dd7b1-111">Indirizzo di un puntatore a un'interfaccia [**IDirectXFileData**](idirectxfiledata.md) , che rappresenta l'oggetto dati di file restituito.</span><span class="sxs-lookup"><span data-stu-id="dd7b1-111">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd7b1-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dd7b1-112">Return value</span></span>

<span data-ttu-id="dd7b1-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dd7b1-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dd7b1-114">Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dd7b1-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="dd7b1-115">Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: DXFILEERR \_ BADVALUE, DXFILEERR \_ NOMOREOBJECTS</span><span class="sxs-lookup"><span data-stu-id="dd7b1-115">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOMOREOBJECTS</span></span>

## <a name="remarks"></a><span data-ttu-id="dd7b1-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="dd7b1-116">Remarks</span></span>

<span data-ttu-id="dd7b1-117">Gli oggetti di primo livello sono sempre oggetti dati.</span><span class="sxs-lookup"><span data-stu-id="dd7b1-117">Top-level objects are always data objects.</span></span> <span data-ttu-id="dd7b1-118">Gli oggetti di riferimento ai dati e gli oggetti binari possono essere solo elementi figlio di oggetti dati.</span><span class="sxs-lookup"><span data-stu-id="dd7b1-118">Data reference objects and binary objects can only be children of data objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd7b1-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd7b1-119">Requirements</span></span>



| <span data-ttu-id="dd7b1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd7b1-120">Requirement</span></span> | <span data-ttu-id="dd7b1-121">Valore</span><span class="sxs-lookup"><span data-stu-id="dd7b1-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd7b1-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dd7b1-122">Header</span></span><br/>  | <dl> <span data-ttu-id="dd7b1-123"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd7b1-123"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="dd7b1-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="dd7b1-124">Library</span></span><br/> | <dl> <span data-ttu-id="dd7b1-125"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd7b1-125"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd7b1-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dd7b1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd7b1-127">IDirectXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="dd7b1-127">IDirectXFileEnumObject</span></span>](idirectxfileenumobject.md)
</dt> </dl>

 

 





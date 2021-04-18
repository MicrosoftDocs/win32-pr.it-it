---
description: Risolve i riferimenti ai dati. Deprecato.
ms.assetid: e8cf6e5d-c9b2-4a47-b058-24282dc65e74
title: 'Metodo IDirectXFileDataReference:: Resolve (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileDataReference.Resolve
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 1b047245e3f89a618cde83e5c18a323f9364f3ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323228"
---
# <a name="idirectxfiledatareferenceresolve-method"></a><span data-ttu-id="eedd4-104">Metodo IDirectXFileDataReference:: Resolve</span><span class="sxs-lookup"><span data-stu-id="eedd4-104">IDirectXFileDataReference::Resolve method</span></span>

<span data-ttu-id="eedd4-105">Risolve i riferimenti ai dati.</span><span class="sxs-lookup"><span data-stu-id="eedd4-105">Resolves data references.</span></span> <span data-ttu-id="eedd4-106">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="eedd4-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="eedd4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eedd4-107">Syntax</span></span>


```C++
HRESULT Resolve(
  [out, retval] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="eedd4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="eedd4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eedd4-109">*ppDataObj* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="eedd4-109">*ppDataObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="eedd4-110">Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span><span class="sxs-lookup"><span data-stu-id="eedd4-110">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)\***</span></span>

<span data-ttu-id="eedd4-111">Indirizzo di un puntatore a un'interfaccia [**IDirectXFileData**](idirectxfiledata.md) , che rappresenta l'oggetto dati di file restituito.</span><span class="sxs-lookup"><span data-stu-id="eedd4-111">Address of a pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the returned file data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eedd4-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eedd4-112">Return value</span></span>

<span data-ttu-id="eedd4-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eedd4-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eedd4-114">Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="eedd4-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="eedd4-115">Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: DXFILEERR \_ BADVALUE, DXFILEERR \_ NotFound.</span><span class="sxs-lookup"><span data-stu-id="eedd4-115">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOTFOUND.</span></span>

## <a name="requirements"></a><span data-ttu-id="eedd4-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eedd4-116">Requirements</span></span>



| <span data-ttu-id="eedd4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="eedd4-117">Requirement</span></span> | <span data-ttu-id="eedd4-118">Valore</span><span class="sxs-lookup"><span data-stu-id="eedd4-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eedd4-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eedd4-119">Header</span></span><br/>  | <dl> <span data-ttu-id="eedd4-120"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="eedd4-120"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="eedd4-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="eedd4-121">Library</span></span><br/> | <dl> <span data-ttu-id="eedd4-122"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eedd4-122"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eedd4-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eedd4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eedd4-124">IDirectXFileDataReference</span><span class="sxs-lookup"><span data-stu-id="eedd4-124">IDirectXFileDataReference</span></span>](idirectxfiledatareference.md)
</dt> </dl>

 

 





---
description: Recupera il successivo oggetto dati figlio, oggetto riferimento ai dati o oggetto binario nel file DirectX. Deprecato.
ms.assetid: 8232e911-6552-4b2b-a9c2-59e6a13a0d9b
title: 'Metodo IDirectXFileData:: GetNextObject (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetNextObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: e03351068cdc4f8fca28c612b7bb4c546125a4cc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323231"
---
# <a name="idirectxfiledatagetnextobject-method"></a><span data-ttu-id="e4b70-104">Metodo IDirectXFileData:: GetNextObject</span><span class="sxs-lookup"><span data-stu-id="e4b70-104">IDirectXFileData::GetNextObject method</span></span>

<span data-ttu-id="e4b70-105">Recupera il successivo oggetto dati figlio, oggetto riferimento ai dati o oggetto binario nel file DirectX.</span><span class="sxs-lookup"><span data-stu-id="e4b70-105">Retrieves the next child data object, data reference object, or binary object in the DirectX file.</span></span> <span data-ttu-id="e4b70-106">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="e4b70-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4b70-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4b70-107">Syntax</span></span>


```C++
HRESULT GetNextObject(
  [out, retval] LPDIRECTXFILEOBJECT *ppChildObj
);
```



## <a name="parameters"></a><span data-ttu-id="e4b70-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4b70-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4b70-109">*ppChildObj* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e4b70-109">*ppChildObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e4b70-110">Tipo: **[ **LPDIRECTXFILEOBJECT**](idirectxfileobject.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4b70-110">Type: **[**LPDIRECTXFILEOBJECT**](idirectxfileobject.md)\***</span></span>

<span data-ttu-id="e4b70-111">Indirizzo di un puntatore a un'interfaccia [**IDirectXFileObject**](idirectxfileobject.md) , che rappresenta l'interfaccia dell'oggetto del file dell'oggetto figlio restituito.</span><span class="sxs-lookup"><span data-stu-id="e4b70-111">Address of a pointer to an [**IDirectXFileObject**](idirectxfileobject.md) interface, representing the returned child object's file object interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4b70-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e4b70-112">Return value</span></span>

<span data-ttu-id="e4b70-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e4b70-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e4b70-114">Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e4b70-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="e4b70-115">Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: DXFILEERR \_ BADVALUE, DXFILEERR \_ NOMOREOBJECTS.</span><span class="sxs-lookup"><span data-stu-id="e4b70-115">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOMOREOBJECTS.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4b70-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4b70-116">Remarks</span></span>

<span data-ttu-id="e4b70-117">Per determinare il tipo di oggetto recuperato, utilizzare QueryInterface per eseguire una query sull'oggetto recuperato per supportare le interfacce [**IDirectXFileData**](idirectxfiledata.md), [**IDirectXFileDataReference**](idirectxfiledatareference.md)o [**IDirectXFileBinary**](idirectxfilebinary.md) .</span><span class="sxs-lookup"><span data-stu-id="e4b70-117">To determine the type of object retrieved, use QueryInterface to query the retrieved object for support of [**IDirectXFileData**](idirectxfiledata.md), [**IDirectXFileDataReference**](idirectxfiledatareference.md), or [**IDirectXFileBinary**](idirectxfilebinary.md) interfaces.</span></span> <span data-ttu-id="e4b70-118">L'interfaccia supportata indica il tipo di oggetto (dati, riferimento ai dati o binario).</span><span class="sxs-lookup"><span data-stu-id="e4b70-118">The interface supported indicates the type of object (data, data reference, or binary).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4b70-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4b70-119">Requirements</span></span>



| <span data-ttu-id="e4b70-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4b70-120">Requirement</span></span> | <span data-ttu-id="e4b70-121">Valore</span><span class="sxs-lookup"><span data-stu-id="e4b70-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4b70-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e4b70-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e4b70-123"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4b70-123"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="e4b70-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="e4b70-124">Library</span></span><br/> | <dl> <span data-ttu-id="e4b70-125"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4b70-125"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4b70-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4b70-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4b70-127">**IDirectXFileBinary**</span><span class="sxs-lookup"><span data-stu-id="e4b70-127">**IDirectXFileBinary**</span></span>](idirectxfilebinary.md)
</dt> <dt>

[<span data-ttu-id="e4b70-128">**IDirectXFileData**</span><span class="sxs-lookup"><span data-stu-id="e4b70-128">**IDirectXFileData**</span></span>](idirectxfiledata.md)
</dt> <dt>

[<span data-ttu-id="e4b70-129">**IDirectXFileDataReference**</span><span class="sxs-lookup"><span data-stu-id="e4b70-129">**IDirectXFileDataReference**</span></span>](idirectxfiledatareference.md)
</dt> </dl>

 

 





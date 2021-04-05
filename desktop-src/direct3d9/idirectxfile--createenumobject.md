---
description: Crea un oggetto enumeratore. Deprecato.
ms.assetid: 9e72bb2f-143e-4690-baef-ccded21572ec
title: 'Metodo IDirectXFile:: CreateEnumObject (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.CreateEnumObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 3d15738b78299441fe08333a41f0652f1b4224d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762250"
---
# <a name="idirectxfilecreateenumobject-method"></a><span data-ttu-id="3102c-104">Metodo IDirectXFile:: CreateEnumObject</span><span class="sxs-lookup"><span data-stu-id="3102c-104">IDirectXFile::CreateEnumObject method</span></span>

<span data-ttu-id="3102c-105">Crea un oggetto enumeratore.</span><span class="sxs-lookup"><span data-stu-id="3102c-105">Creates an enumerator object.</span></span> <span data-ttu-id="3102c-106">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="3102c-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="3102c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3102c-107">Syntax</span></span>


```C++
HRESULT CreateEnumObject(
  [in]          LPVOID                  pvSource,
  [in]          DXFILELOADOPTIONS       dwLoadOptions,
  [out, retval] LPDIRECTXFILEENUMOBJECT *ppEnumObj
);
```



## <a name="parameters"></a><span data-ttu-id="3102c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3102c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3102c-109">*pvSource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3102c-109">*pvSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3102c-110">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3102c-110">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3102c-111">Puntatore ai dati il cui contenuto dipende dal valore di dwLoadOptions</span><span class="sxs-lookup"><span data-stu-id="3102c-111">Pointer to data whose contents depend on the value of dwLoadOptions</span></span>

</dd> <dt>

<span data-ttu-id="3102c-112">*dwLoadOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3102c-112">*dwLoadOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3102c-113">Tipo: **[ **DXFILELOADOPTIONS**](dxfile.md)**</span><span class="sxs-lookup"><span data-stu-id="3102c-113">Type: **[**DXFILELOADOPTIONS**](dxfile.md)**</span></span>

<span data-ttu-id="3102c-114">Valore che specifica l'origine dei dati.</span><span class="sxs-lookup"><span data-stu-id="3102c-114">Value that specifies the source of the data.</span></span> <span data-ttu-id="3102c-115">Questo valore può essere uno dei flag DXFILELOAD \_ xxx nelle [costanti DXFILE](dxfile.md).</span><span class="sxs-lookup"><span data-stu-id="3102c-115">This value can be one of the DXFILELOAD\_xxx flags in [DXFILE Constants](dxfile.md).</span></span>

</dd> <dt>

<span data-ttu-id="3102c-116">*ppEnumObj* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="3102c-116">*ppEnumObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3102c-117">Tipo: **[ **LPDIRECTXFILEENUMOBJECT**](idirectxfileenumobject.md)\***</span><span class="sxs-lookup"><span data-stu-id="3102c-117">Type: **[**LPDIRECTXFILEENUMOBJECT**](idirectxfileenumobject.md)\***</span></span>

<span data-ttu-id="3102c-118">Indirizzo di un puntatore a un'interfaccia [**IDirectXFileEnumObject**](idirectxfileenumobject.md) , che rappresenta l'oggetto enumeratore creato.</span><span class="sxs-lookup"><span data-stu-id="3102c-118">Address of a pointer to an [**IDirectXFileEnumObject**](idirectxfileenumobject.md) interface, representing the created enumerator object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3102c-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3102c-119">Return value</span></span>

<span data-ttu-id="3102c-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3102c-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3102c-121">Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3102c-121">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="3102c-122">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: DXFILEERR \_ BADALLOC, DXFILEERR \_ BADFILEFLOATSIZE, DXFILEERR \_ BADFILETYPE, DXFILEERR BADFILEVERSION, DXFILEERR BADRESOURCE, DXFILEERR BADVALUE, DXFILEERR FileNotFound, \_ \_ \_ \_ DXFILEERR \_ RESOURCENOTFOUND \_ , DXFILEERR URLNOTFOUND.</span><span class="sxs-lookup"><span data-stu-id="3102c-122">If the method fails, the return value can be one of the following: DXFILEERR\_BADALLOC, DXFILEERR\_BADFILEFLOATSIZE, DXFILEERR\_BADFILETYPE, DXFILEERR\_BADFILEVERSION, DXFILEERR\_BADRESOURCE, DXFILEERR\_BADVALUE, DXFILEERR\_FILENOTFOUND, DXFILEERR\_RESOURCENOTFOUND, DXFILEERR\_URLNOTFOUND.</span></span>

## <a name="remarks"></a><span data-ttu-id="3102c-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="3102c-123">Remarks</span></span>

<span data-ttu-id="3102c-124">Dopo aver utilizzato questo metodo, utilizzare uno dei metodi IDirectXFileEnumObject per recuperare un oggetto dati.</span><span class="sxs-lookup"><span data-stu-id="3102c-124">After using this method, use one of the IDirectXFileEnumObject methods to retrieve a data object.</span></span>

## <a name="requirements"></a><span data-ttu-id="3102c-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3102c-125">Requirements</span></span>



| <span data-ttu-id="3102c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3102c-126">Requirement</span></span> | <span data-ttu-id="3102c-127">Valore</span><span class="sxs-lookup"><span data-stu-id="3102c-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3102c-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3102c-128">Header</span></span><br/>  | <dl> <span data-ttu-id="3102c-129"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="3102c-129"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="3102c-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="3102c-130">Library</span></span><br/> | <dl> <span data-ttu-id="3102c-131"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3102c-131"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3102c-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3102c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3102c-133">IDirectXFile</span><span class="sxs-lookup"><span data-stu-id="3102c-133">IDirectXFile</span></span>](idirectxfile.md)
</dt> </dl>

 

 

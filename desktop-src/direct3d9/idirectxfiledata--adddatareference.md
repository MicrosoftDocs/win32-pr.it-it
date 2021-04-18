---
description: Crea e aggiunge un oggetto riferimento ai dati come oggetto figlio. Deprecato.
ms.assetid: 71a770a2-1502-4b93-b368-990c3318bd33
title: 'Metodo IDirectXFileData:: AddDataReference (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddDataReference
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 44834af51380c3b8bdbb4e9a4b24bf911ea6a07f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322539"
---
# <a name="idirectxfiledataadddatareference-method"></a><span data-ttu-id="15c70-104">Metodo IDirectXFileData:: AddDataReference</span><span class="sxs-lookup"><span data-stu-id="15c70-104">IDirectXFileData::AddDataReference method</span></span>

<span data-ttu-id="15c70-105">Crea e aggiunge un oggetto riferimento ai dati come oggetto figlio.</span><span class="sxs-lookup"><span data-stu-id="15c70-105">Creates and adds a data reference object as a child object.</span></span> <span data-ttu-id="15c70-106">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="15c70-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="15c70-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15c70-107">Syntax</span></span>


```C++
HRESULT AddDataReference(
  [in]       LPCSTR szRef,
  [in] const GUID   *pguidRef
);
```



## <a name="parameters"></a><span data-ttu-id="15c70-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="15c70-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15c70-109">*szRef* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15c70-109">*szRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15c70-110">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="15c70-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="15c70-111">Puntatore al nome dell'oggetto dati a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="15c70-111">Pointer to the name of the referenced data object.</span></span> <span data-ttu-id="15c70-112">Questo parametro può essere **null** se pguidRef fornisce un riferimento al GUID.</span><span class="sxs-lookup"><span data-stu-id="15c70-112">This parameter can be **NULL** if pguidRef provides a reference to the GUID.</span></span>

</dd> <dt>

<span data-ttu-id="15c70-113">*pguidRef* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15c70-113">*pguidRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15c70-114">Tipo: **[**GUID**](guid.md) \* const**</span><span class="sxs-lookup"><span data-stu-id="15c70-114">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="15c70-115">Puntatore al GUID che rappresenta i dati.</span><span class="sxs-lookup"><span data-stu-id="15c70-115">Pointer to the GUID representing the data.</span></span> <span data-ttu-id="15c70-116">Questo parametro può essere **null** se szRef fornisce un riferimento al nome.</span><span class="sxs-lookup"><span data-stu-id="15c70-116">This parameter can be **NULL** if szRef provides a reference to the name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15c70-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="15c70-117">Return value</span></span>

<span data-ttu-id="15c70-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="15c70-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="15c70-119">Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="15c70-119">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="15c70-120">Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE</span><span class="sxs-lookup"><span data-stu-id="15c70-120">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="remarks"></a><span data-ttu-id="15c70-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="15c70-121">Remarks</span></span>

<span data-ttu-id="15c70-122">Affinché questo metodo abbia esito positivo, il parametro szRef o pguidRef deve essere non **null**.</span><span class="sxs-lookup"><span data-stu-id="15c70-122">For this method to succeed, either the szRef or pguidRef parameter must be non-**NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="15c70-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15c70-123">Requirements</span></span>



| <span data-ttu-id="15c70-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="15c70-124">Requirement</span></span> | <span data-ttu-id="15c70-125">Valore</span><span class="sxs-lookup"><span data-stu-id="15c70-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="15c70-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="15c70-126">Header</span></span><br/>  | <dl> <span data-ttu-id="15c70-127"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="15c70-127"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="15c70-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="15c70-128">Library</span></span><br/> | <dl> <span data-ttu-id="15c70-129"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15c70-129"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15c70-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15c70-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15c70-131">IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="15c70-131">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> </dl>

 

 

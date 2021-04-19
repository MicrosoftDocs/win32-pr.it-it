---
description: Recupera i dati per uno dei membri dell'oggetto o i dati per tutti i membri. Deprecato.
ms.assetid: 2a227705-371e-41f1-af5d-20e652cd07f6
title: 'Metodo IDirectXFileData:: GetData (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.GetData
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: ed52aaf0b4c740b675129c81843c0bd49c7f428e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323232"
---
# <a name="idirectxfiledatagetdata-method"></a><span data-ttu-id="5603f-104">Metodo IDirectXFileData:: GetData</span><span class="sxs-lookup"><span data-stu-id="5603f-104">IDirectXFileData::GetData method</span></span>

<span data-ttu-id="5603f-105">Recupera i dati per uno dei membri dell'oggetto o i dati per tutti i membri.</span><span class="sxs-lookup"><span data-stu-id="5603f-105">Retrieves the data for one of the object's members or the data for all members.</span></span> <span data-ttu-id="5603f-106">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="5603f-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="5603f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5603f-107">Syntax</span></span>


```C++
HRESULT GetData(
  [in]  LPCSTR szMember,
  [out] DWORD  *pcbSize,
  [out] void   **ppvData
);
```



## <a name="parameters"></a><span data-ttu-id="5603f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5603f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5603f-109">*szMember* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5603f-109">*szMember* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5603f-110">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5603f-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5603f-111">Puntatore al nome del membro per il quale recuperare i dati.</span><span class="sxs-lookup"><span data-stu-id="5603f-111">Pointer to the name of the member for which to retrieve data.</span></span> <span data-ttu-id="5603f-112">Specificare **null** per recuperare tutti i dati necessari dei membri.</span><span class="sxs-lookup"><span data-stu-id="5603f-112">Specify **NULL** to retrieve all required members' data.</span></span>

</dd> <dt>

<span data-ttu-id="5603f-113">*pcbSize* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5603f-113">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5603f-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5603f-114">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5603f-115">Puntatore per la ricezione della dimensione del buffer ppvData in byte.</span><span class="sxs-lookup"><span data-stu-id="5603f-115">Pointer to receive the ppvData buffer size, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="5603f-116">*ppvData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5603f-116">*ppvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5603f-117">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="5603f-117">Type: **void\*\***</span></span>

<span data-ttu-id="5603f-118">Indirizzo di un puntatore al buffer per ricevere i dati associati a szMember.</span><span class="sxs-lookup"><span data-stu-id="5603f-118">Address of a pointer to the buffer to receive the data associated with szMember.</span></span> <span data-ttu-id="5603f-119">Se szMember è **null**, ppvData è impostato in modo da puntare a un buffer contenente tutti i dati necessari dei membri in un blocco di memoria contiguo.</span><span class="sxs-lookup"><span data-stu-id="5603f-119">If szMember is **NULL**, ppvData is set to point to a buffer containing all required members' data in a contiguous block of memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5603f-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5603f-120">Return value</span></span>

<span data-ttu-id="5603f-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5603f-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5603f-122">Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5603f-122">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="5603f-123">Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: DXFILEERR \_ BADARRAYSIZE, DXFILEERR \_ BADDATAREFERENCE, DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="5603f-123">If the method fails, the return value can be one of the following values: DXFILEERR\_BADARRAYSIZE, DXFILEERR\_BADDataReference, DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="5603f-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="5603f-124">Remarks</span></span>

<span data-ttu-id="5603f-125">Questo metodo recupera i dati per i membri obbligatori di un oggetto dati, ma non i dati per i membri facoltativi (figlio).</span><span class="sxs-lookup"><span data-stu-id="5603f-125">This method retrieves the data for required members of a data object but no data for optional (child) members.</span></span> <span data-ttu-id="5603f-126">Usare [**IDirectXFileData:: GetNextObject**](idirectxfiledata--getnextobject.md) per recuperare oggetti figlio.</span><span class="sxs-lookup"><span data-stu-id="5603f-126">Use [**IDirectXFileData::GetNextObject**](idirectxfiledata--getnextobject.md) to retrieve child objects.</span></span>

## <a name="requirements"></a><span data-ttu-id="5603f-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5603f-127">Requirements</span></span>



| <span data-ttu-id="5603f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5603f-128">Requirement</span></span> | <span data-ttu-id="5603f-129">Valore</span><span class="sxs-lookup"><span data-stu-id="5603f-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5603f-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5603f-130">Header</span></span><br/>  | <dl> <span data-ttu-id="5603f-131"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="5603f-131"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="5603f-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="5603f-132">Library</span></span><br/> | <dl> <span data-ttu-id="5603f-133"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5603f-133"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5603f-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5603f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5603f-135">IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="5603f-135">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> <dt>

[<span data-ttu-id="5603f-136">**IDirectXFileData::GetNextObject**</span><span class="sxs-lookup"><span data-stu-id="5603f-136">**IDirectXFileData::GetNextObject**</span></span>](idirectxfiledata--getnextobject.md)
</dt> </dl>

 

 

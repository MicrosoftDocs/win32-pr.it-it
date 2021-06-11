---
description: Informazioni sul metodo IAMFilterData::P arseFilterData, decomprime i dati binari del Registro di sistema per un filtro. Questa interfaccia è stata deprecata.
ms.assetid: 86095fcf-3364-42a0-95db-08223fa3cc20
title: Metodo IAMFilterData::P arseFilterData (Fil \_ data.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData.ParseFilterData
api_type:
- COM
api_location:
- Quartz.dll
ms.openlocfilehash: 9560280fa6f16699af907cdb5cf682b9c4bb1277
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989446"
---
# <a name="iamfilterdataparsefilterdata-method"></a><span data-ttu-id="8ea20-104">Metodo IAMFilterData::P arseFilterData</span><span class="sxs-lookup"><span data-stu-id="8ea20-104">IAMFilterData::ParseFilterData method</span></span>

> [!Note]  
> <span data-ttu-id="8ea20-105">Questa interfaccia è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="8ea20-105">This interface has been deprecated.</span></span> <span data-ttu-id="8ea20-106">Le nuove applicazioni non devono usarlo.</span><span class="sxs-lookup"><span data-stu-id="8ea20-106">New applications should not use it.</span></span>

 

<span data-ttu-id="8ea20-107">Il `ParseFilterData` metodo decomprime i dati binari del Registro di sistema per un filtro.</span><span class="sxs-lookup"><span data-stu-id="8ea20-107">The `ParseFilterData` method unpacks the binary registry data for a filter.</span></span>

<span data-ttu-id="8ea20-108">In genere non esiste alcun motivo per cui un'applicazione chiami questo metodo.</span><span class="sxs-lookup"><span data-stu-id="8ea20-108">There is typically no reason for an application to call this method.</span></span> <span data-ttu-id="8ea20-109">Il [**metodo IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) offre un modo più pratico per accedere ai dati del Registro di sistema di filtro.</span><span class="sxs-lookup"><span data-stu-id="8ea20-109">The [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method provides a more convenient way to access the filter registry data.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ea20-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8ea20-110">Syntax</span></span>


```C++
HRESULT ParseFilterData(
  [in]  BYTE  *rgbFilterData,
  [in]  ULONG cb,
  [out] BYTE  **prgbRegFilter2
);
```



## <a name="parameters"></a><span data-ttu-id="8ea20-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="8ea20-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ea20-112">*rgbFilterData* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8ea20-112">*rgbFilterData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ea20-113">Puntatore ai dati binari del Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="8ea20-113">Pointer to the binary registry data.</span></span> <span data-ttu-id="8ea20-114">È possibile ottenere questi dati recuperando la proprietà "FilterData" dal moniker di filtro.</span><span class="sxs-lookup"><span data-stu-id="8ea20-114">You can get this data by retrieving the "FilterData" property from the filter moniker.</span></span> <span data-ttu-id="8ea20-115">I dati vengono archiviati come **SAFEARRAY** di byte (VT \_ UI1 \| VT \_ ARRAY).</span><span class="sxs-lookup"><span data-stu-id="8ea20-115">The data is stored as a **SAFEARRAY** of bytes (VT\_UI1 \| VT\_ARRAY).</span></span>

</dd> <dt>

<span data-ttu-id="8ea20-116">*cb* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="8ea20-116">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ea20-117">Specifica le dimensioni dei dati binari, in byte.</span><span class="sxs-lookup"><span data-stu-id="8ea20-117">Specifies the size of the binary data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="8ea20-118">*prgbRegFilter2* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="8ea20-118">*prgbRegFilter2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ea20-119">Indirizzo di una variabile che riceve un puntatore ai dati decompressi.</span><span class="sxs-lookup"><span data-stu-id="8ea20-119">Address of a variable that receives a pointer to the unpacked data.</span></span> <span data-ttu-id="8ea20-120">Quando il metodo viene restituito, eseguire il cast di questo puntatore a [**un tipo REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) per accedere ai dati del filtro.</span><span class="sxs-lookup"><span data-stu-id="8ea20-120">When the method returns, cast this pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) type to access the filter data.</span></span> <span data-ttu-id="8ea20-121">Il chiamante deve rilasciare la memoria chiamando il **metodo CoTaskMemFree.**</span><span class="sxs-lookup"><span data-stu-id="8ea20-121">The caller must release the memory by calling the **CoTaskMemFree** method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ea20-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8ea20-122">Return value</span></span>

<span data-ttu-id="8ea20-123">Se il metodo ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8ea20-123">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="8ea20-124">Se ha esito negativo, viene restituito un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="8ea20-124">If it fails, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ea20-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="8ea20-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8ea20-126">L'intestazione Fil \_ data.h si trova nella directory [Mapper Sample](mapper-sample.md) nella Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="8ea20-126">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8ea20-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ea20-127">Requirements</span></span>



| <span data-ttu-id="8ea20-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ea20-128">Requirement</span></span> | <span data-ttu-id="8ea20-129">Valore</span><span class="sxs-lookup"><span data-stu-id="8ea20-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ea20-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8ea20-130">Header</span></span><br/> | <dl> <span data-ttu-id="8ea20-131"><dt>Fil \_ data.h</dt></span><span class="sxs-lookup"><span data-stu-id="8ea20-131"><dt>Fil\_data.h</dt></span></span> </dl> |
| <span data-ttu-id="8ea20-132">DLL</span><span class="sxs-lookup"><span data-stu-id="8ea20-132">DLL</span></span><br/>    | <dl> <span data-ttu-id="8ea20-133"><dt>Quartz.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ea20-133"><dt>Quartz.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8ea20-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ea20-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ea20-135">**Interfaccia IAMFilterData**</span><span class="sxs-lookup"><span data-stu-id="8ea20-135">**IAMFilterData Interface**</span></span>](iamfilterdata.md)
</dt> </dl>

 

 





---
description: Nota Questa interfaccia è stata deprecata.
ms.assetid: 86095fcf-3364-42a0-95db-08223fa3cc20
title: 'IAMFilterData: metodo:P arseFilterData (Fil \_ Data. h)'
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
ms.openlocfilehash: 18e1367813adff6b0debdfb698644731668bfc5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326817"
---
# <a name="iamfilterdataparsefilterdata-method"></a><span data-ttu-id="96537-103">IAMFilterData::P metodo arseFilterData</span><span class="sxs-lookup"><span data-stu-id="96537-103">IAMFilterData::ParseFilterData method</span></span>

> [!Note]  
> <span data-ttu-id="96537-104">Questa interfaccia è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="96537-104">This interface has been deprecated.</span></span> <span data-ttu-id="96537-105">Le nuove applicazioni non devono utilizzarlo.</span><span class="sxs-lookup"><span data-stu-id="96537-105">New applications should not use it.</span></span>

 

<span data-ttu-id="96537-106">Il `ParseFilterData` Metodo decomprime i dati del registro di sistema binario per un filtro.</span><span class="sxs-lookup"><span data-stu-id="96537-106">The `ParseFilterData` method unpacks the binary registry data for a filter.</span></span>

<span data-ttu-id="96537-107">Non esiste in genere un motivo per cui un'applicazione chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="96537-107">There is typically no reason for an application to call this method.</span></span> <span data-ttu-id="96537-108">Il metodo [**IFilterMapper2:: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) fornisce un modo più pratico per accedere ai dati del registro di sistema del filtro.</span><span class="sxs-lookup"><span data-stu-id="96537-108">The [**IFilterMapper2::EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) method provides a more convenient way to access the filter registry data.</span></span>

## <a name="syntax"></a><span data-ttu-id="96537-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96537-109">Syntax</span></span>


```C++
HRESULT ParseFilterData(
  [in]  BYTE  *rgbFilterData,
  [in]  ULONG cb,
  [out] BYTE  **prgbRegFilter2
);
```



## <a name="parameters"></a><span data-ttu-id="96537-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="96537-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96537-111">*rgbFilterData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96537-111">*rgbFilterData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96537-112">Puntatore ai dati binari del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="96537-112">Pointer to the binary registry data.</span></span> <span data-ttu-id="96537-113">È possibile ottenere questi dati recuperando la proprietà "FilterData" dal moniker del filtro.</span><span class="sxs-lookup"><span data-stu-id="96537-113">You can get this data by retrieving the "FilterData" property from the filter moniker.</span></span> <span data-ttu-id="96537-114">I dati vengono archiviati come **SAFEARRAY** di byte (VT \_ Ui1 \| VT \_ Array).</span><span class="sxs-lookup"><span data-stu-id="96537-114">The data is stored as a **SAFEARRAY** of bytes (VT\_UI1 \| VT\_ARRAY).</span></span>

</dd> <dt>

<span data-ttu-id="96537-115">*CB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96537-115">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96537-116">Specifica le dimensioni in byte dei dati binari.</span><span class="sxs-lookup"><span data-stu-id="96537-116">Specifies the size of the binary data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="96537-117">*prgbRegFilter2* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="96537-117">*prgbRegFilter2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96537-118">Indirizzo di una variabile che riceve un puntatore ai dati decompressi.</span><span class="sxs-lookup"><span data-stu-id="96537-118">Address of a variable that receives a pointer to the unpacked data.</span></span> <span data-ttu-id="96537-119">Quando il metodo restituisce un risultato, eseguire il cast di questo puntatore a un tipo [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) per accedere ai dati del filtro.</span><span class="sxs-lookup"><span data-stu-id="96537-119">When the method returns, cast this pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) type to access the filter data.</span></span> <span data-ttu-id="96537-120">Il chiamante deve rilasciare la memoria chiamando il metodo **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="96537-120">The caller must release the memory by calling the **CoTaskMemFree** method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96537-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96537-121">Return value</span></span>

<span data-ttu-id="96537-122">Se il metodo ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="96537-122">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="96537-123">Se ha esito negativo, viene restituito un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="96537-123">If it fails, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="96537-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="96537-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="96537-125">L'intestazione fil \_ Data. h si trova nella directory degli [esempi del Mapper](mapper-sample.md) nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="96537-125">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="96537-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96537-126">Requirements</span></span>



| <span data-ttu-id="96537-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="96537-127">Requirement</span></span> | <span data-ttu-id="96537-128">Valore</span><span class="sxs-lookup"><span data-stu-id="96537-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="96537-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96537-129">Header</span></span><br/> | <dl> <span data-ttu-id="96537-130"><dt>Fil \_ Data. h</dt></span><span class="sxs-lookup"><span data-stu-id="96537-130"><dt>Fil\_data.h</dt></span></span> </dl> |
| <span data-ttu-id="96537-131">DLL</span><span class="sxs-lookup"><span data-stu-id="96537-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="96537-132"><dt>Quartz.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96537-132"><dt>Quartz.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="96537-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96537-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96537-134">**Interfaccia IAMFilterData**</span><span class="sxs-lookup"><span data-stu-id="96537-134">**IAMFilterData Interface**</span></span>](iamfilterdata.md)
</dt> </dl>

 

 





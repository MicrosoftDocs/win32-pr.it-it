---
description: Nota Questa interfaccia è stata deprecata.
ms.assetid: ab6972ef-7c28-4cd1-b007-eb70f9aeb2cb
title: 'Metodo IAMFilterData:: CreateFilterData (Fil \_ Data. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData.CreateFilterData
api_type:
- COM
api_location:
- Quartz.dll
ms.openlocfilehash: 4c83f19de8e709f9890b23957f730fbbac12dd7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326819"
---
# <a name="iamfilterdatacreatefilterdata-method"></a><span data-ttu-id="b870a-103">Metodo IAMFilterData:: CreateFilterData</span><span class="sxs-lookup"><span data-stu-id="b870a-103">IAMFilterData::CreateFilterData method</span></span>

> [!Note]  
> <span data-ttu-id="b870a-104">Questa interfaccia è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="b870a-104">This interface has been deprecated.</span></span> <span data-ttu-id="b870a-105">Le nuove applicazioni non devono utilizzarlo.</span><span class="sxs-lookup"><span data-stu-id="b870a-105">New applications should not use it.</span></span>

 

<span data-ttu-id="b870a-106">Il `CreateFilterData` metodo crea dati del registro di sistema binari per un filtro.</span><span class="sxs-lookup"><span data-stu-id="b870a-106">The `CreateFilterData` method creates binary registry data for a filter.</span></span> <span data-ttu-id="b870a-107">Questi dati possono essere scritti nel registro di sistema come una \_ sottochiave reg Binary denominata FilterData, sotto la chiave CLSID del filtro.</span><span class="sxs-lookup"><span data-stu-id="b870a-107">This data can be written to the registry as a REG\_BINARY subkey named FilterData, under the filter's CLSID key.</span></span>

<span data-ttu-id="b870a-108">Non esiste in genere un motivo per cui un'applicazione chiama questo metodo.</span><span class="sxs-lookup"><span data-stu-id="b870a-108">There is typically no reason for an application to call this method.</span></span> <span data-ttu-id="b870a-109">Il metodo [**IFilterMapper2:: RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) crea automaticamente i dati binari e li aggiunge alla posizione corretta nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="b870a-109">The [**IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) method automatically creates the binary data and adds it to the correct location in the registry.</span></span> <span data-ttu-id="b870a-110">Per altre informazioni, vedere [How to register DirectShow Filters](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="b870a-110">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b870a-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b870a-111">Syntax</span></span>


```C++
HRESULT CreateFilterData(
  [in]  REGFILTER2 *prf2,
  [out] BYTE       **prgbFilterData,
  [out] ULONG      *pcb
);
```



## <a name="parameters"></a><span data-ttu-id="b870a-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="b870a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b870a-113">*PRF2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b870a-113">*prf2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b870a-114">Puntatore a una struttura [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) che contiene le informazioni sul filtro.</span><span class="sxs-lookup"><span data-stu-id="b870a-114">Pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) structure that contains the filter information.</span></span>

</dd> <dt>

<span data-ttu-id="b870a-115">*prgbFilterData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b870a-115">*prgbFilterData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b870a-116">Indirizzo di una variabile che riceve un puntatore ai dati binari.</span><span class="sxs-lookup"><span data-stu-id="b870a-116">Address of a variable that receives a pointer to the binary data.</span></span> <span data-ttu-id="b870a-117">Il metodo alloca la memoria per i dati.</span><span class="sxs-lookup"><span data-stu-id="b870a-117">The method allocates the memory for the data.</span></span> <span data-ttu-id="b870a-118">Il chiamante deve rilasciare la memoria chiamando il metodo **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="b870a-118">The caller must release the memory by calling the **CoTaskMemFree** method.</span></span>

</dd> <dt>

<span data-ttu-id="b870a-119">*PCB* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b870a-119">*pcb* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b870a-120">Puntatore a una variabile che riceve le dimensioni dei dati binari, in byte.</span><span class="sxs-lookup"><span data-stu-id="b870a-120">Pointer to a variable that receives the size of the binary data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b870a-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b870a-121">Return value</span></span>

<span data-ttu-id="b870a-122">Se il metodo ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b870a-122">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="b870a-123">Se ha esito negativo, viene restituito un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="b870a-123">If it fails, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b870a-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="b870a-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b870a-125">L'intestazione fil \_ Data. h si trova nella directory degli [esempi del Mapper](mapper-sample.md) nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="b870a-125">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b870a-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b870a-126">Requirements</span></span>



| <span data-ttu-id="b870a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b870a-127">Requirement</span></span> | <span data-ttu-id="b870a-128">Valore</span><span class="sxs-lookup"><span data-stu-id="b870a-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b870a-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b870a-129">Header</span></span><br/> | <dl> <span data-ttu-id="b870a-130"><dt>Fil \_ Data. h</dt></span><span class="sxs-lookup"><span data-stu-id="b870a-130"><dt>Fil\_data.h</dt></span></span> </dl> |
| <span data-ttu-id="b870a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b870a-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="b870a-132"><dt>Quartz.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b870a-132"><dt>Quartz.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b870a-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b870a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b870a-134">**Interfaccia IAMFilterData**</span><span class="sxs-lookup"><span data-stu-id="b870a-134">**IAMFilterData Interface**</span></span>](iamfilterdata.md)
</dt> </dl>

 

 





---
description: Informazioni sul metodo IAMFilterData::CreateFilterData, che crea dati binari del Registro di sistema per un filtro. Questa interfaccia è stata deprecata.
ms.assetid: ab6972ef-7c28-4cd1-b007-eb70f9aeb2cb
title: Metodo IAMFilterData::CreateFilterData (Fil \_ data.h)
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
ms.openlocfilehash: 0a0126266fc33dca030abad65ccf9f0d35f6e195
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989456"
---
# <a name="iamfilterdatacreatefilterdata-method"></a><span data-ttu-id="c965b-104">Metodo IAMFilterData::CreateFilterData</span><span class="sxs-lookup"><span data-stu-id="c965b-104">IAMFilterData::CreateFilterData method</span></span>

> [!Note]  
> <span data-ttu-id="c965b-105">Questa interfaccia è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="c965b-105">This interface has been deprecated.</span></span> <span data-ttu-id="c965b-106">Le nuove applicazioni non devono usarlo.</span><span class="sxs-lookup"><span data-stu-id="c965b-106">New applications should not use it.</span></span>

 

<span data-ttu-id="c965b-107">Il `CreateFilterData` metodo crea dati binari del Registro di sistema per un filtro.</span><span class="sxs-lookup"><span data-stu-id="c965b-107">The `CreateFilterData` method creates binary registry data for a filter.</span></span> <span data-ttu-id="c965b-108">Questi dati possono essere scritti nel Registro di sistema come sottochiave REG \_ BINARY denominata FilterData, nella chiave CLSID del filtro.</span><span class="sxs-lookup"><span data-stu-id="c965b-108">This data can be written to the registry as a REG\_BINARY subkey named FilterData, under the filter's CLSID key.</span></span>

<span data-ttu-id="c965b-109">In genere non esiste alcun motivo per cui un'applicazione chiami questo metodo.</span><span class="sxs-lookup"><span data-stu-id="c965b-109">There is typically no reason for an application to call this method.</span></span> <span data-ttu-id="c965b-110">Il [**metodo IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) crea automaticamente i dati binari e li aggiunge al percorso corretto nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="c965b-110">The [**IFilterMapper2::RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) method automatically creates the binary data and adds it to the correct location in the registry.</span></span> <span data-ttu-id="c965b-111">Per altre informazioni, vedere [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="c965b-111">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c965b-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c965b-112">Syntax</span></span>


```C++
HRESULT CreateFilterData(
  [in]  REGFILTER2 *prf2,
  [out] BYTE       **prgbFilterData,
  [out] ULONG      *pcb
);
```



## <a name="parameters"></a><span data-ttu-id="c965b-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="c965b-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c965b-114">*prf2* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c965b-114">*prf2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c965b-115">Puntatore a [**una struttura REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) che contiene le informazioni sul filtro.</span><span class="sxs-lookup"><span data-stu-id="c965b-115">Pointer to a [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) structure that contains the filter information.</span></span>

</dd> <dt>

<span data-ttu-id="c965b-116">*prgbFilterData* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="c965b-116">*prgbFilterData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c965b-117">Indirizzo di una variabile che riceve un puntatore ai dati binari.</span><span class="sxs-lookup"><span data-stu-id="c965b-117">Address of a variable that receives a pointer to the binary data.</span></span> <span data-ttu-id="c965b-118">Il metodo alloca la memoria per i dati.</span><span class="sxs-lookup"><span data-stu-id="c965b-118">The method allocates the memory for the data.</span></span> <span data-ttu-id="c965b-119">Il chiamante deve rilasciare la memoria chiamando il **metodo CoTaskMemFree.**</span><span class="sxs-lookup"><span data-stu-id="c965b-119">The caller must release the memory by calling the **CoTaskMemFree** method.</span></span>

</dd> <dt>

<span data-ttu-id="c965b-120">*pcb* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="c965b-120">*pcb* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c965b-121">Puntatore a una variabile che riceve le dimensioni dei dati binari, in byte.</span><span class="sxs-lookup"><span data-stu-id="c965b-121">Pointer to a variable that receives the size of the binary data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c965b-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c965b-122">Return value</span></span>

<span data-ttu-id="c965b-123">Se il metodo ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c965b-123">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="c965b-124">Se ha esito negativo, viene restituito un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="c965b-124">If it fails, it returns an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c965b-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="c965b-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c965b-126">L'intestazione Fil \_ data.h si trova nella directory [Mapper Sample](mapper-sample.md) nella Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="c965b-126">The header Fil\_data.h is located in the [Mapper Sample](mapper-sample.md) directory in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c965b-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c965b-127">Requirements</span></span>



| <span data-ttu-id="c965b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c965b-128">Requirement</span></span> | <span data-ttu-id="c965b-129">Valore</span><span class="sxs-lookup"><span data-stu-id="c965b-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c965b-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c965b-130">Header</span></span><br/> | <dl> <span data-ttu-id="c965b-131"><dt>Fil \_ data.h</dt></span><span class="sxs-lookup"><span data-stu-id="c965b-131"><dt>Fil\_data.h</dt></span></span> </dl> |
| <span data-ttu-id="c965b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c965b-132">DLL</span></span><br/>    | <dl> <span data-ttu-id="c965b-133"><dt>Quartz.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c965b-133"><dt>Quartz.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c965b-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c965b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c965b-135">**Interfaccia IAMFilterData**</span><span class="sxs-lookup"><span data-stu-id="c965b-135">**IAMFilterData Interface**</span></span>](iamfilterdata.md)
</dt> </dl>

 

 





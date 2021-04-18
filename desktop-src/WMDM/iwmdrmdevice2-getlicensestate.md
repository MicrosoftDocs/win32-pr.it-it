---
title: Metodo IWMDRMDevice2 GetLicenseState
description: Il metodo GetLicenseState ottiene lo stato della licenza.
ms.assetid: a98847f6-00ec-4211-9716-79714d7ba169
keywords:
- Metodo GetLicenseState Windows Media Gestione dispositivi
- Metodo GetLicenseState Windows Media Gestione dispositivi, interfaccia IWMDRMDevice2
- Interfaccia IWMDRMDevice2 Windows Media Gestione dispositivi, metodo GetLicenseState
topic_type:
- apiref
api_name:
- IWMDRMDevice2.GetLicenseState
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d075d123ae99b26767621fb1a958cd172bc9e42c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333857"
---
# <a name="iwmdrmdevice2getlicensestate-method"></a><span data-ttu-id="8043d-106">Metodo IWMDRMDevice2:: GetLicenseState</span><span class="sxs-lookup"><span data-stu-id="8043d-106">IWMDRMDevice2::GetLicenseState method</span></span>

<span data-ttu-id="8043d-107">Il metodo **GetLicenseState** ottiene lo stato della licenza.</span><span class="sxs-lookup"><span data-stu-id="8043d-107">The **GetLicenseState** method gets the license state.</span></span>

## <a name="syntax"></a><span data-ttu-id="8043d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8043d-108">Syntax</span></span>


```C++
HRESULT GetLicenseState(
  [in]  BYTE  *pbStateQueryData,
  [in]  DWORD cbStateQueryData,
  [out] DWORD *pdwCategory,
  [out] DWORD *pcRemainingCounts,
  [out] DWORD *pcRemainingHours,
  [out] DWORD *pdwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="8043d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8043d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8043d-110">*pbStateQueryData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8043d-110">*pbStateQueryData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8043d-111">Puntatore ai dati sottoposti a query dello stato della licenza.</span><span class="sxs-lookup"><span data-stu-id="8043d-111">Pointer to the queried data of the license state.</span></span>

</dd> <dt>

<span data-ttu-id="8043d-112">*cbStateQueryData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8043d-112">*cbStateQueryData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8043d-113">Conteggio dei dati sottoposti a query.</span><span class="sxs-lookup"><span data-stu-id="8043d-113">Count of the queried data.</span></span>

</dd> <dt>

<span data-ttu-id="8043d-114">*pdwCategory* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8043d-114">*pdwCategory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8043d-115">Puntatore alla categoria.</span><span class="sxs-lookup"><span data-stu-id="8043d-115">Pointer to the category.</span></span>

</dd> <dt>

<span data-ttu-id="8043d-116">*pcRemainingCounts* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8043d-116">*pcRemainingCounts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8043d-117">Puntatore ai conteggi rimanenti.</span><span class="sxs-lookup"><span data-stu-id="8043d-117">Pointer to the remaining counts.</span></span>

</dd> <dt>

<span data-ttu-id="8043d-118">*pcRemainingHours* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8043d-118">*pcRemainingHours* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8043d-119">Puntatore alle ore rimanenti.</span><span class="sxs-lookup"><span data-stu-id="8043d-119">Pointer to the remaining hours.</span></span>

</dd> <dt>

<span data-ttu-id="8043d-120">*pdwReserved* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8043d-120">*pdwReserved* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8043d-121">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="8043d-121">Reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8043d-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8043d-122">Return value</span></span>

<span data-ttu-id="8043d-123">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8043d-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8043d-124">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8043d-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8043d-125">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8043d-125">Return code</span></span>                                                                          | <span data-ttu-id="8043d-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8043d-126">Description</span></span>                     |
|--------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="8043d-127"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8043d-127"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8043d-128">Il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="8043d-128">The method succeeds.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8043d-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8043d-129">Requirements</span></span>



| <span data-ttu-id="8043d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="8043d-130">Requirement</span></span> | <span data-ttu-id="8043d-131">Valore</span><span class="sxs-lookup"><span data-stu-id="8043d-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8043d-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8043d-132">Header</span></span><br/>  | <dl> <span data-ttu-id="8043d-133"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8043d-133"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="8043d-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="8043d-134">Library</span></span><br/> | <dl> <span data-ttu-id="8043d-135"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8043d-135"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8043d-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8043d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8043d-137">**Interfaccia IWMDRMDevice2**</span><span class="sxs-lookup"><span data-stu-id="8043d-137">**IWMDRMDevice2 Interface**</span></span>](iwmdrmdevice2.md)
</dt> </dl>

 

 






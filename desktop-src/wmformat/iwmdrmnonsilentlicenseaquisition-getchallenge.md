---
title: Metodo getchallenge IWMDRMNonSilentLicenseAquisition (wmdrmsdk. h)
description: Il metodo getchallenge recupera la richiesta di licenza che deve essere inviata al server licenze.
ms.assetid: f2ff8484-8fe2-4c74-82c1-9bc14f8197e0
keywords:
- Metodo getchallenge-formato Windows Media
- Metodo getchallenge, formato Windows Media, interfaccia IWMDRMNonSilentLicenseAquisition
- Interfaccia IWMDRMNonSilentLicenseAquisition-formato Windows Media, metodo getchallenge
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition.GetChallenge
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa0dc63c63e5d7a62c06cbe791d9a5e5e8d09c5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327462"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongetchallenge-method"></a><span data-ttu-id="27834-106">Metodo IWMDRMNonSilentLicenseAquisition:: getchallenge</span><span class="sxs-lookup"><span data-stu-id="27834-106">IWMDRMNonSilentLicenseAquisition::GetChallenge method</span></span>

<span data-ttu-id="27834-107">Il metodo **getchallenge** recupera la richiesta di licenza che deve essere inviata al server licenze.</span><span class="sxs-lookup"><span data-stu-id="27834-107">The **GetChallenge** method retrieves the license challenge that should be posted to the license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="27834-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="27834-108">Syntax</span></span>


```C++
HRESULT GetChallenge(
  [out] BSTR *pbstrChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="27834-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="27834-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27834-110">*pbstrChallenge* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="27834-110">*pbstrChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27834-111">Indirizzo di una variabile che riceve la richiesta di licenza.</span><span class="sxs-lookup"><span data-stu-id="27834-111">Address of a variable that receives the license challenge.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27834-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="27834-112">Return value</span></span>

<span data-ttu-id="27834-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="27834-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="27834-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="27834-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="27834-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="27834-115">Return code</span></span>                                                                          | <span data-ttu-id="27834-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27834-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="27834-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="27834-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="27834-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="27834-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="27834-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="27834-119">Remarks</span></span>

<span data-ttu-id="27834-120">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="27834-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="27834-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27834-121">Requirements</span></span>



| <span data-ttu-id="27834-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="27834-122">Requirement</span></span> | <span data-ttu-id="27834-123">Valore</span><span class="sxs-lookup"><span data-stu-id="27834-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27834-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="27834-124">Header</span></span><br/>  | <dl> <span data-ttu-id="27834-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="27834-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="27834-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="27834-126">Library</span></span><br/> | <dl> <span data-ttu-id="27834-127"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27834-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27834-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27834-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27834-129">**Interfaccia IWMDRMNonSilentLicenseAquisition**</span><span class="sxs-lookup"><span data-stu-id="27834-129">**IWMDRMNonSilentLicenseAquisition Interface**</span></span>](iwmdrmnonsilentlicenseaquisition.md)
</dt> </dl>

 

 






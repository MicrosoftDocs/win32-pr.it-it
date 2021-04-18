---
title: Metodo IWMDRMNonSilentLicenseAquisition GetURL (wmdrmsdk. h)
description: Il metodo GetURL recupera l'URL a cui deve essere inviata la richiesta di licenza.
ms.assetid: f65f1984-74bc-4cd0-957e-930aa6a6f6a5
keywords:
- Metodo GetURL Windows Media Format
- Metodo GetURL Windows Media Format, interfaccia IWMDRMNonSilentLicenseAquisition
- Interfaccia IWMDRMNonSilentLicenseAquisition-formato Windows Media, Metodo GetURL
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition.GetURL
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79212d19d7dbf4a66e2b72dcbdeba9262a9aeddd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325547"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongeturl-method"></a><span data-ttu-id="d106a-106">Metodo IWMDRMNonSilentLicenseAquisition:: GetURL</span><span class="sxs-lookup"><span data-stu-id="d106a-106">IWMDRMNonSilentLicenseAquisition::GetURL method</span></span>

<span data-ttu-id="d106a-107">Il metodo **getURL** recupera l'URL a cui deve essere inviata la richiesta di licenza.</span><span class="sxs-lookup"><span data-stu-id="d106a-107">The **GetURL** method retrieves the URL to which the license challenge should be posted.</span></span>

## <a name="syntax"></a><span data-ttu-id="d106a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d106a-108">Syntax</span></span>


```C++
HRESULT GetURL(
  [out] BSTR *pbstrURL
);
```



## <a name="parameters"></a><span data-ttu-id="d106a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d106a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d106a-110">*pbstrURL* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d106a-110">*pbstrURL* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d106a-111">Indirizzo di una variabile che riceve l'URL.</span><span class="sxs-lookup"><span data-stu-id="d106a-111">Address of a variable that receives the URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d106a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d106a-112">Return value</span></span>

<span data-ttu-id="d106a-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d106a-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d106a-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d106a-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d106a-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d106a-115">Return code</span></span>                                                                          | <span data-ttu-id="d106a-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d106a-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d106a-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d106a-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d106a-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="d106a-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d106a-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="d106a-119">Remarks</span></span>

<span data-ttu-id="d106a-120">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="d106a-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="d106a-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d106a-121">Requirements</span></span>



| <span data-ttu-id="d106a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d106a-122">Requirement</span></span> | <span data-ttu-id="d106a-123">Valore</span><span class="sxs-lookup"><span data-stu-id="d106a-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d106a-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d106a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d106a-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="d106a-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="d106a-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="d106a-126">Library</span></span><br/> | <dl> <span data-ttu-id="d106a-127"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d106a-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d106a-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d106a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d106a-129">**Interfaccia IWMDRMNonSilentLicenseAquisition**</span><span class="sxs-lookup"><span data-stu-id="d106a-129">**IWMDRMNonSilentLicenseAquisition Interface**</span></span>](iwmdrmnonsilentlicenseaquisition.md)
</dt> </dl>

 

 






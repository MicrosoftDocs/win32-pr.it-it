---
title: Metodo IWMDRMLicenseQuery SetActionAllowedQueryParams (wmdrmsdk. h)
description: Il metodo SetActionAllowedQueryParams imposta le informazioni specifiche dell'ambiente per ottenere risultati di query più accurati quando si usa il metodo QueryActionAllowed.
ms.assetid: 1c8f9d4e-999d-4d7c-87fd-9d30e432350c
keywords:
- Metodo SetActionAllowedQueryParams Windows Media Format
- Metodo SetActionAllowedQueryParams Windows Media Format, interfaccia IWMDRMLicenseQuery
- Interfaccia IWMDRMLicenseQuery-formato Windows Media, metodo SetActionAllowedQueryParams
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.SetActionAllowedQueryParams
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a83a28c4d9f3758b711c43ddd83a509c58f8ea8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325558"
---
# <a name="iwmdrmlicensequerysetactionallowedqueryparams-method"></a><span data-ttu-id="62058-106">Metodo IWMDRMLicenseQuery:: SetActionAllowedQueryParams</span><span class="sxs-lookup"><span data-stu-id="62058-106">IWMDRMLicenseQuery::SetActionAllowedQueryParams method</span></span>

<span data-ttu-id="62058-107">Il metodo **SetActionAllowedQueryParams** imposta le informazioni specifiche dell'ambiente per ottenere risultati di query più accurati quando si usa il metodo [**QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) .</span><span class="sxs-lookup"><span data-stu-id="62058-107">The **SetActionAllowedQueryParams** method sets environment-specific information for more accurate query results when using the [**QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="62058-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="62058-108">Syntax</span></span>


```C++
HRESULT SetActionAllowedQueryParams(
  [in] BOOL  fIsMF,
  [in] DWORD dwAppSecLevel,
  [in] BOOL  fHasSerialNumber,
  [in] BSTR  bstrDeviceCert
);
```



## <a name="parameters"></a><span data-ttu-id="62058-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="62058-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62058-110">*fIsMF* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62058-110">*fIsMF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62058-111">Specifica se verrà eseguito il rendering del contenuto utilizzando gli oggetti di Microsoft Media Foundation SDK.</span><span class="sxs-lookup"><span data-stu-id="62058-111">Specifies whether the content will be rendered by using the objects of the Microsoft Media Foundation SDK.</span></span> <span data-ttu-id="62058-112">**False** indica il rendering da parte degli oggetti di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="62058-112">**FALSE** indicates rendering by the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="62058-113">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="62058-113">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="62058-114">*dwAppSecLevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62058-114">*dwAppSecLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62058-115">Livello di sicurezza dell'applicazione di query.</span><span class="sxs-lookup"><span data-stu-id="62058-115">Security level of the querying application.</span></span> <span data-ttu-id="62058-116">Questo valore è importante solo se verranno usati gli oggetti di Windows Media Format SDK. in questo caso, *fIsMF* deve essere impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="62058-116">This value is only important if the objects of the Windows Media Format SDK will be used, in which case *fIsMF* should be set to **FALSE**.</span></span> <span data-ttu-id="62058-117">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="62058-117">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="62058-118">*fHasSerialNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62058-118">*fHasSerialNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62058-119">Specifica se il dispositivo di destinazione per un'operazione di copia ha un numero di serie.</span><span class="sxs-lookup"><span data-stu-id="62058-119">Specifies whether the target device for a copy operation has a serial number.</span></span> <span data-ttu-id="62058-120">Questo parametro è facoltativo e si applica solo alle query per le operazioni di copia.</span><span class="sxs-lookup"><span data-stu-id="62058-120">This parameter is optional and only applies to queries for copy operations.</span></span>

</dd> <dt>

<span data-ttu-id="62058-121">*bstrDeviceCert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62058-121">*bstrDeviceCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62058-122">Certificato del dispositivo di destinazione quando si usa DRM di Windows Media per i dispositivi portatili.</span><span class="sxs-lookup"><span data-stu-id="62058-122">Device certificate of the target device when using Windows Media DRM for Portable Devices.</span></span> <span data-ttu-id="62058-123">Questo parametro è facoltativo e si applica solo alle query per le operazioni di copia.</span><span class="sxs-lookup"><span data-stu-id="62058-123">This parameter is optional and only applies to queries for copy operations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62058-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="62058-124">Return value</span></span>

<span data-ttu-id="62058-125">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="62058-125">The method returns an **HRESULT**.</span></span> <span data-ttu-id="62058-126">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="62058-126">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="62058-127">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="62058-127">Return code</span></span>                                                                          | <span data-ttu-id="62058-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62058-128">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="62058-129"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="62058-129"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="62058-130">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="62058-130">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="62058-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="62058-131">Remarks</span></span>

<span data-ttu-id="62058-132">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="62058-132">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="62058-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62058-133">Requirements</span></span>



| <span data-ttu-id="62058-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="62058-134">Requirement</span></span> | <span data-ttu-id="62058-135">Valore</span><span class="sxs-lookup"><span data-stu-id="62058-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62058-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62058-136">Header</span></span><br/>  | <dl> <span data-ttu-id="62058-137"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="62058-137"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="62058-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="62058-138">Library</span></span><br/> | <dl> <span data-ttu-id="62058-139"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62058-139"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62058-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62058-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62058-141">**Interfaccia IWMDRMLicenseQuery**</span><span class="sxs-lookup"><span data-stu-id="62058-141">**IWMDRMLicenseQuery Interface**</span></span>](iwmdrmlicensequery.md)
</dt> <dt>

[<span data-ttu-id="62058-142">**Esecuzione di query per informazioni dettagliate sui diritti**</span><span class="sxs-lookup"><span data-stu-id="62058-142">**Querying for Detailed Rights Information**</span></span>](querying-for-detailed-rights-information.md)
</dt> </dl>

 

 






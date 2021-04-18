---
title: Metodo IWMDRMNetTransmitter GetLeafLicenseResponse (wmdrmsdk. h)
description: Il metodo GetLeafLicenseResponse genera un messaggio di risposta di licenza foglia.
ms.assetid: b2893d22-b6f3-44d2-b6db-e2b07fbe098d
keywords:
- Metodo GetLeafLicenseResponse Windows Media Format
- Metodo GetLeafLicenseResponse Windows Media Format, interfaccia IWMDRMNetTransmitter
- Interfaccia IWMDRMNetTransmitter-formato Windows Media, metodo GetLeafLicenseResponse
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.GetLeafLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf2374966abfae4353a72755313c1cbbdfb7287
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325552"
---
# <a name="iwmdrmnettransmittergetleaflicenseresponse-method"></a><span data-ttu-id="910e7-106">Metodo IWMDRMNetTransmitter:: GetLeafLicenseResponse</span><span class="sxs-lookup"><span data-stu-id="910e7-106">IWMDRMNetTransmitter::GetLeafLicenseResponse method</span></span>

<span data-ttu-id="910e7-107">Il metodo **GetLeafLicenseResponse** genera un messaggio di risposta di licenza foglia.</span><span class="sxs-lookup"><span data-stu-id="910e7-107">The **GetLeafLicenseResponse** method generates a leaf license response message.</span></span>

## <a name="syntax"></a><span data-ttu-id="910e7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="910e7-108">Syntax</span></span>


```C++
HRESULT GetLeafLicenseResponse(
  [in]  BSTR            bstrKID,
  [in]  WMDRMNET_POLICY *pPolicy,
  [out] IWMDRMEncrypt   **ppIWMDRMEncrypt,
  [out] BYTE            **ppbLicenseResponse,
  [out] DWORD           *pcbLicenseResponse
);
```



## <a name="parameters"></a><span data-ttu-id="910e7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="910e7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="910e7-110">*bstrKID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="910e7-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="910e7-111">Identificatore di chiave con codifica base64 da usare per la nuova licenza foglia.</span><span class="sxs-lookup"><span data-stu-id="910e7-111">Base64-encoded key identifier to be used for the new leaf license.</span></span> <span data-ttu-id="910e7-112">L'identificatore di chiave deve essere un valore GUID generato in modo casuale.</span><span class="sxs-lookup"><span data-stu-id="910e7-112">The key identifier should be a randomly generated GUID value.</span></span>

</dd> <dt>

<span data-ttu-id="910e7-113">*ppolicy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="910e7-113">*pPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="910e7-114">Puntatore alla struttura [**dei \_ criteri WMDRMNET**](wmdrmnet-policy.md) che definisce i criteri da usare per la licenza foglia.</span><span class="sxs-lookup"><span data-stu-id="910e7-114">Pointer to the [**WMDRMNET\_POLICY**](wmdrmnet-policy.md) structure that defines the policy to use for the leaf license.</span></span>

</dd> <dt>

<span data-ttu-id="910e7-115">*ppIWMDRMEncrypt* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="910e7-115">*ppIWMDRMEncrypt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="910e7-116">Indirizzo di una variabile che riceve un puntatore all'interfaccia [**IWMDRMEncrypt**](iwmdrmencrypt.md) che può essere utilizzata per crittografare i dati per la nuova licenza foglia.</span><span class="sxs-lookup"><span data-stu-id="910e7-116">Address of a variable that receives a pointer to the [**IWMDRMEncrypt**](iwmdrmencrypt.md) interface that can be used to encrypt data for the new leaf license.</span></span>

</dd> <dt>

<span data-ttu-id="910e7-117">*ppbLicenseResponse* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="910e7-117">*ppbLicenseResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="910e7-118">Indirizzo di una variabile che riceve l'indirizzo della risposta di licenza generata.</span><span class="sxs-lookup"><span data-stu-id="910e7-118">Address of a variable that receives the address of the generated license response.</span></span> <span data-ttu-id="910e7-119">Al termine di questi dati, è necessario rilasciare la memoria chiamando **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="910e7-119">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="910e7-120">*pcbLicenseResponse* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="910e7-120">*pcbLicenseResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="910e7-121">Indirizzo di una variabile che riceve le dimensioni della risposta di licenza, in byte.</span><span class="sxs-lookup"><span data-stu-id="910e7-121">Address of a variable that receives the size of the license response, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="910e7-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="910e7-122">Return value</span></span>

<span data-ttu-id="910e7-123">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="910e7-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="910e7-124">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="910e7-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="910e7-125">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="910e7-125">Return code</span></span>                                                                                                | <span data-ttu-id="910e7-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="910e7-126">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="910e7-127"><dt>**NS \_ E \_ DRM di DRM \_ \_ troppo \_ piccoli**</dt></span><span class="sxs-lookup"><span data-stu-id="910e7-127"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="910e7-128">È necessario un elenco di revoche di contenuti aggiornato.</span><span class="sxs-lookup"><span data-stu-id="910e7-128">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="910e7-129"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="910e7-129"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="910e7-130">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="910e7-130">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="910e7-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="910e7-131">Remarks</span></span>

<span data-ttu-id="910e7-132">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="910e7-132">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="910e7-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="910e7-133">Requirements</span></span>



| <span data-ttu-id="910e7-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="910e7-134">Requirement</span></span> | <span data-ttu-id="910e7-135">Valore</span><span class="sxs-lookup"><span data-stu-id="910e7-135">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="910e7-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="910e7-136">Header</span></span><br/> | <dl> <span data-ttu-id="910e7-137"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="910e7-137"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="910e7-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="910e7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="910e7-139">**Interfaccia IWMDRMNetTransmitter**</span><span class="sxs-lookup"><span data-stu-id="910e7-139">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> </dl>

 

 






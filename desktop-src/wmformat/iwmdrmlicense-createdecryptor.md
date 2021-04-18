---
title: Metodo IWMDRMLicense CreateDecryptor (wmdrmsdk. h)
description: Il metodo CreateDecryptor crea un oggetto di decrittografia utilizzando le impostazioni della licenza corrente.
ms.assetid: 69b7f96b-a0d6-455e-8ef9-0faf9690cef1
keywords:
- Metodo CreateDecryptor Windows Media Format
- Metodo CreateDecryptor Windows Media Format, interfaccia IWMDRMLicense
- Interfaccia IWMDRMLicense-formato Windows Media, metodo CreateDecryptor
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateDecryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e987e7ffa3390462889b128f390934f05e64cdff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324285"
---
# <a name="iwmdrmlicensecreatedecryptor-method"></a><span data-ttu-id="dac2f-106">Metodo IWMDRMLicense:: CreateDecryptor</span><span class="sxs-lookup"><span data-stu-id="dac2f-106">IWMDRMLicense::CreateDecryptor method</span></span>

<span data-ttu-id="dac2f-107">Il metodo **CreateDecryptor** crea un oggetto di decrittografia utilizzando le impostazioni della licenza corrente.</span><span class="sxs-lookup"><span data-stu-id="dac2f-107">The **CreateDecryptor** method creates a decryptor object using the settings of the current license.</span></span>

## <a name="syntax"></a><span data-ttu-id="dac2f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dac2f-108">Syntax</span></span>


```C++
HRESULT CreateDecryptor(
  [out] IWMDRMDecrypt **ppDecryptor
);
```



## <a name="parameters"></a><span data-ttu-id="dac2f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="dac2f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dac2f-110">*ppDecryptor* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="dac2f-110">*ppDecryptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dac2f-111">Riceve un puntatore all'interfaccia [**IWMDRMDecrypt**](iwmdrmdecrypt.md) dell'oggetto appena creato.</span><span class="sxs-lookup"><span data-stu-id="dac2f-111">Receives a pointer to the [**IWMDRMDecrypt**](iwmdrmdecrypt.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dac2f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dac2f-112">Return value</span></span>

<span data-ttu-id="dac2f-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="dac2f-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="dac2f-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="dac2f-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="dac2f-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="dac2f-115">Return code</span></span>                                                                                                | <span data-ttu-id="dac2f-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dac2f-116">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="dac2f-117"><dt>**NS \_ E \_ DRM di DRM \_ \_ troppo \_ piccoli**</dt></span><span class="sxs-lookup"><span data-stu-id="dac2f-117"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="dac2f-118">È necessario un elenco di revoche di contenuti aggiornato.</span><span class="sxs-lookup"><span data-stu-id="dac2f-118">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="dac2f-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dac2f-119"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="dac2f-120">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="dac2f-120">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="dac2f-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="dac2f-121">Remarks</span></span>

<span data-ttu-id="dac2f-122">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="dac2f-122">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="dac2f-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dac2f-123">Requirements</span></span>



| <span data-ttu-id="dac2f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="dac2f-124">Requirement</span></span> | <span data-ttu-id="dac2f-125">Valore</span><span class="sxs-lookup"><span data-stu-id="dac2f-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dac2f-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dac2f-126">Header</span></span><br/> | <dl> <span data-ttu-id="dac2f-127"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="dac2f-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dac2f-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dac2f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dac2f-129">**Al CreateDecryptor**</span><span class="sxs-lookup"><span data-stu-id="dac2f-129">**CreateEncryptor**</span></span>](iwmdrmlicense-createencryptor.md)
</dt> <dt>

[<span data-ttu-id="dac2f-130">**Interfaccia IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="dac2f-130">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 






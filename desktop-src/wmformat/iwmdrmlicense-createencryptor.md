---
title: Metodo IWMDRMLicense al CreateDecryptor (wmdrmsdk. h)
description: Il metodo al CreateDecryptor crea un oggetto di crittografia utilizzando le impostazioni della licenza corrente.
ms.assetid: 570ba898-e846-4981-8ea8-ce16f2dad68a
keywords:
- Metodo al CreateDecryptor Windows Media Format
- Metodo al CreateDecryptor Windows Media Format, interfaccia IWMDRMLicense
- Interfaccia IWMDRMLicense-formato Windows Media, metodo al CreateDecryptor
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateEncryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8031f412129f1d02cc4ef37c6af5f49a6c0b7532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328531"
---
# <a name="iwmdrmlicensecreateencryptor-method"></a><span data-ttu-id="71aff-106">Metodo IWMDRMLicense:: al CreateDecryptor</span><span class="sxs-lookup"><span data-stu-id="71aff-106">IWMDRMLicense::CreateEncryptor method</span></span>

<span data-ttu-id="71aff-107">Il metodo **al CreateDecryptor** crea un oggetto di crittografia utilizzando le impostazioni della licenza corrente.</span><span class="sxs-lookup"><span data-stu-id="71aff-107">The **CreateEncryptor** method creates an encryptor object using the settings of the current license.</span></span>

## <a name="syntax"></a><span data-ttu-id="71aff-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71aff-108">Syntax</span></span>


```C++
HRESULT CreateEncryptor(
  [out] IWMDRMEncrypt **ppEncryptor
);
```



## <a name="parameters"></a><span data-ttu-id="71aff-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="71aff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71aff-110">*ppEncryptor* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="71aff-110">*ppEncryptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71aff-111">Riceve un puntatore all'interfaccia [**IWMDRMEncrypt**](iwmdrmencrypt.md) dell'oggetto appena creato.</span><span class="sxs-lookup"><span data-stu-id="71aff-111">Receives a pointer to the [**IWMDRMEncrypt**](iwmdrmencrypt.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71aff-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="71aff-112">Return value</span></span>

<span data-ttu-id="71aff-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="71aff-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="71aff-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="71aff-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="71aff-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="71aff-115">Return code</span></span>                                                                                                | <span data-ttu-id="71aff-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71aff-116">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="71aff-117"><dt>**NS \_ E \_ DRM di DRM \_ \_ troppo \_ piccoli**</dt></span><span class="sxs-lookup"><span data-stu-id="71aff-117"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="71aff-118">È necessario un elenco di revoche di contenuti aggiornato.</span><span class="sxs-lookup"><span data-stu-id="71aff-118">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="71aff-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="71aff-119"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="71aff-120">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="71aff-120">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="71aff-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="71aff-121">Remarks</span></span>

<span data-ttu-id="71aff-122">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="71aff-122">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="71aff-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71aff-123">Requirements</span></span>



| <span data-ttu-id="71aff-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="71aff-124">Requirement</span></span> | <span data-ttu-id="71aff-125">Valore</span><span class="sxs-lookup"><span data-stu-id="71aff-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="71aff-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="71aff-126">Header</span></span><br/> | <dl> <span data-ttu-id="71aff-127"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="71aff-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71aff-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71aff-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71aff-129">**CreateDecryptor**</span><span class="sxs-lookup"><span data-stu-id="71aff-129">**CreateDecryptor**</span></span>](iwmdrmlicense-createdecryptor.md)
</dt> <dt>

[<span data-ttu-id="71aff-130">**Interfaccia IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="71aff-130">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 






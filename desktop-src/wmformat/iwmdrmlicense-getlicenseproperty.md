---
title: Metodo IWMDRMLicense GetLicenseProperty (wmdrmsdk. h)
description: Il metodo GetLicenseProperty recupera una proprietà dalla licenza corrente.
ms.assetid: 5431f849-b37e-40b7-8bdb-ee30948aeff1
keywords:
- Metodo GetLicenseProperty Windows Media Format
- Metodo GetLicenseProperty Windows Media Format, interfaccia IWMDRMLicense
- Interfaccia IWMDRMLicense-formato Windows Media, metodo GetLicenseProperty
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetLicenseProperty
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf7fe91c57b9c69934f093cdd504b5e6d35efb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325567"
---
# <a name="iwmdrmlicensegetlicenseproperty-method"></a><span data-ttu-id="a7200-106">Metodo IWMDRMLicense:: GetLicenseProperty</span><span class="sxs-lookup"><span data-stu-id="a7200-106">IWMDRMLicense::GetLicenseProperty method</span></span>

<span data-ttu-id="a7200-107">Il metodo **GetLicenseProperty** recupera una proprietà dalla licenza corrente.</span><span class="sxs-lookup"><span data-stu-id="a7200-107">The **GetLicenseProperty** method retrieves a property from the current license.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7200-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7200-108">Syntax</span></span>


```C++
HRESULT GetLicenseProperty(
  [in]  BSTR        bstrName,
  [out] PROPVARIANT *ppropVariant
);
```



## <a name="parameters"></a><span data-ttu-id="a7200-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a7200-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7200-110">*bstrName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7200-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7200-111">Nome della proprietà da recuperare.</span><span class="sxs-lookup"><span data-stu-id="a7200-111">Name of the property to retrieve.</span></span> <span data-ttu-id="a7200-112">Impostare su una delle costanti nella tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="a7200-112">Set to one of the constants in the following table:</span></span>



| <span data-ttu-id="a7200-113">Costante</span><span class="sxs-lookup"><span data-stu-id="a7200-113">Constant</span></span>                   | <span data-ttu-id="a7200-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7200-114">Description</span></span>                                                                                                          |
|----------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7200-115">\_revoca g wszWMDRMNet \_</span><span class="sxs-lookup"><span data-stu-id="a7200-115">g\_wszWMDRMNet\_Revocation</span></span> | <span data-ttu-id="a7200-116">Utilizzare per ottenere Windows Media DRM per i dispositivi di rete elenco di revoche per la licenza corrente.</span><span class="sxs-lookup"><span data-stu-id="a7200-116">Use to get the Windows Media DRM for Network Devices revocation list for the current license.</span></span>                        |
| <span data-ttu-id="a7200-117">g \_ wszWMDRM \_ SAPLEVEL</span><span class="sxs-lookup"><span data-stu-id="a7200-117">g\_wszWMDRM\_SAPLEVEL</span></span>      | <span data-ttu-id="a7200-118">Usare per ottenere il livello SAP (Secure Audio Path) necessario per riprodurre il contenuto coperto dalla licenza corrente.</span><span class="sxs-lookup"><span data-stu-id="a7200-118">Use to get the Secure Audio Path (SAP) level required to play content covered by the current license.</span></span>                |
| <span data-ttu-id="a7200-119">g \_ wszWMDRM \_ SAPRequired</span><span class="sxs-lookup"><span data-stu-id="a7200-119">g\_wszWMDRM\_SAPRequired</span></span>   | <span data-ttu-id="a7200-120">Usare per verificare se la licenza corrente richiede l'uso di SAP per riprodurre il contenuto.</span><span class="sxs-lookup"><span data-stu-id="a7200-120">Use to ascertain whether the current license requires SAP be used to play the content.</span></span>                               |
| <span data-ttu-id="a7200-121">g \_ wszWMDRM \_ SOURCEID</span><span class="sxs-lookup"><span data-stu-id="a7200-121">g\_wszWMDRM\_SOURCEID</span></span>      | <span data-ttu-id="a7200-122">Utilizzare per ottenere l'identificatore di origine per la licenza corrente.</span><span class="sxs-lookup"><span data-stu-id="a7200-122">Use to get the source identifier for the current license.</span></span>                                                            |
| <span data-ttu-id="a7200-123">g \_ \_ priorità wszWMDRM</span><span class="sxs-lookup"><span data-stu-id="a7200-123">g\_wszWMDRM\_PRIORITY</span></span>      | <span data-ttu-id="a7200-124">Usare per ottenere la priorità della licenza corrente.</span><span class="sxs-lookup"><span data-stu-id="a7200-124">Use to get the priority of the current license.</span></span> <span data-ttu-id="a7200-125">Le licenze con priorità più alta vengono applicate prima delle licenze con priorità più bassa.</span><span class="sxs-lookup"><span data-stu-id="a7200-125">Higher priority licenses are applied before lower priority licenses.</span></span> |
| <span data-ttu-id="a7200-126">g \_ wszWMDRM- \_ LinkId</span><span class="sxs-lookup"><span data-stu-id="a7200-126">g\_wszWMDRM\_UplinkID</span></span>      | <span data-ttu-id="a7200-127">Usare per ottenere l'ID chiave della licenza radice nella catena di licenze a cui appartiene la licenza corrente.</span><span class="sxs-lookup"><span data-stu-id="a7200-127">Use to get the key ID of the root license in the license chain that the current license belongs to.</span></span>                  |



 

</dd> <dt>

<span data-ttu-id="a7200-128">*ppropVariant* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a7200-128">*ppropVariant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7200-129">Riceve il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="a7200-129">Receives the property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7200-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a7200-130">Return value</span></span>

<span data-ttu-id="a7200-131">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a7200-131">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a7200-132">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a7200-132">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a7200-133">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a7200-133">Return code</span></span>                                                                          | <span data-ttu-id="a7200-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7200-134">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a7200-135"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a7200-135"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a7200-136">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="a7200-136">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a7200-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="a7200-137">Remarks</span></span>

<span data-ttu-id="a7200-138">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="a7200-138">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7200-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7200-139">Requirements</span></span>



| <span data-ttu-id="a7200-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7200-140">Requirement</span></span> | <span data-ttu-id="a7200-141">Valore</span><span class="sxs-lookup"><span data-stu-id="a7200-141">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7200-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a7200-142">Header</span></span><br/>  | <dl> <span data-ttu-id="a7200-143"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7200-143"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="a7200-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="a7200-144">Library</span></span><br/> | <dl> <span data-ttu-id="a7200-145"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7200-145"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7200-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7200-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7200-147">**GetLicense**</span><span class="sxs-lookup"><span data-stu-id="a7200-147">**GetLicense**</span></span>](iwmdrmlicense-getlicense.md)
</dt> <dt>

[<span data-ttu-id="a7200-148">**Interfaccia IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="a7200-148">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 






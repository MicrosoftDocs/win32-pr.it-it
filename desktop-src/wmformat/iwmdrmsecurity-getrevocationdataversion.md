---
title: Metodo IWMDRMSecurity GetRevocationDataVersion (wmdrmsdk. h)
description: Il metodo GetRevocationDataVersion Recupera il numero di versione di un elenco di revoche di certificati nell'archivio locale.
ms.assetid: 2fa13b38-02c2-4c81-938b-409cadca00fb
keywords:
- Metodo GetRevocationDataVersion Windows Media Format
- Metodo GetRevocationDataVersion Windows Media Format, interfaccia IWMDRMSecurity
- Interfaccia IWMDRMSecurity-formato Windows Media, metodo GetRevocationDataVersion
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetRevocationDataVersion
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705f02622b7298134328b513aa038804995eb1c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325536"
---
# <a name="iwmdrmsecuritygetrevocationdataversion-method"></a><span data-ttu-id="8202b-106">Metodo IWMDRMSecurity:: GetRevocationDataVersion</span><span class="sxs-lookup"><span data-stu-id="8202b-106">IWMDRMSecurity::GetRevocationDataVersion method</span></span>

<span data-ttu-id="8202b-107">Il metodo **GetRevocationDataVersion** Recupera il numero di versione di un elenco di revoche di certificati nell'archivio locale.</span><span class="sxs-lookup"><span data-stu-id="8202b-107">The **GetRevocationDataVersion** method retrieves the version number of a certificate revocation list in the local store.</span></span>

## <a name="syntax"></a><span data-ttu-id="8202b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8202b-108">Syntax</span></span>


```C++
HRESULT GetRevocationDataVersion(
  [in]  REFGUID   f_guidRevocationType,
  [out] ULONGLONG *f_pdwCRLVersion
);
```



## <a name="parameters"></a><span data-ttu-id="8202b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8202b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8202b-110">*\_ guidRevocationType f* \[\]</span><span class="sxs-lookup"><span data-stu-id="8202b-110">*f\_guidRevocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8202b-111">GUID che specifica il tipo di elenco di revoche.</span><span class="sxs-lookup"><span data-stu-id="8202b-111">GUID specifying the type of revocation list.</span></span> <span data-ttu-id="8202b-112">Impostare su una delle costanti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8202b-112">Set to one of the constants in the following table.</span></span>



| <span data-ttu-id="8202b-113">Costante GUID</span><span class="sxs-lookup"><span data-stu-id="8202b-113">GUID constant</span></span>                 | <span data-ttu-id="8202b-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8202b-114">Description</span></span>                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8202b-115">\_app WMDRM REVOCATIONTYPE \_</span><span class="sxs-lookup"><span data-stu-id="8202b-115">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="8202b-116">Specifica l'elenco di revoche di certificati dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8202b-116">Specifies the application certificate revocation list.</span></span>                           |
| <span data-ttu-id="8202b-117">\_dispositivo REVOCATIONTYPE \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="8202b-117">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="8202b-118">Specifica l'elenco di revoche di certificati del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8202b-118">Specifies the device certificate revocation list.</span></span>                                |
| <span data-ttu-id="8202b-119">WMDRM \_ REVOCATIONTYPE \_ Cardea</span><span class="sxs-lookup"><span data-stu-id="8202b-119">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="8202b-120">Specifica Windows Media DRM per i dispositivi di rete elenco di revoche di certificati.</span><span class="sxs-lookup"><span data-stu-id="8202b-120">Specifies the Windows Media DRM for Network Devices certificate revocation list.</span></span> |



 

</dd> <dt>

<span data-ttu-id="8202b-121">*f \_ pdwCRLVersion* \[\]</span><span class="sxs-lookup"><span data-stu-id="8202b-121">*f\_pdwCRLVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8202b-122">Variabile che riceve il numero di versione.</span><span class="sxs-lookup"><span data-stu-id="8202b-122">Variable that receives the version number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8202b-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8202b-123">Return value</span></span>

<span data-ttu-id="8202b-124">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8202b-124">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8202b-125">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8202b-125">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8202b-126">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8202b-126">Return code</span></span>                                                                          | <span data-ttu-id="8202b-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8202b-127">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8202b-128"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8202b-128"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8202b-129">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="8202b-129">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8202b-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8202b-130">Requirements</span></span>



| <span data-ttu-id="8202b-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="8202b-131">Requirement</span></span> | <span data-ttu-id="8202b-132">Valore</span><span class="sxs-lookup"><span data-stu-id="8202b-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8202b-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8202b-133">Header</span></span><br/>  | <dl> <span data-ttu-id="8202b-134"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="8202b-134"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="8202b-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="8202b-135">Library</span></span><br/> | <dl> <span data-ttu-id="8202b-136"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8202b-136"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8202b-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8202b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8202b-138">**Revoca e rinnovo automatici dei componenti**</span><span class="sxs-lookup"><span data-stu-id="8202b-138">**Automated Component Revocation and Renewal**</span></span>](automated-component-revocation-and-renewal.md)
</dt> <dt>

[<span data-ttu-id="8202b-139">**GetRevocationData**</span><span class="sxs-lookup"><span data-stu-id="8202b-139">**GetRevocationData**</span></span>](iwmdrmsecurity-getrevocationdata.md)
</dt> <dt>

[<span data-ttu-id="8202b-140">**Interfaccia IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="8202b-140">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> <dt>

[<span data-ttu-id="8202b-141">**SetRevocationData**</span><span class="sxs-lookup"><span data-stu-id="8202b-141">**SetRevocationData**</span></span>](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 






---
title: Metodo IWMDRMSecurity CheckCertForRevocation (wmdrmsdk. h)
description: Il metodo CheckCertForRevocation determina se un certificato è stato revocato.
ms.assetid: 3efde398-f2ba-486e-b017-6787ca402e4c
keywords:
- Metodo CheckCertForRevocation Windows Media Format
- Metodo CheckCertForRevocation Windows Media Format, interfaccia IWMDRMSecurity
- Interfaccia IWMDRMSecurity-formato Windows Media, metodo CheckCertForRevocation
topic_type:
- apiref
api_name:
- IWMDRMSecurity.CheckCertForRevocation
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a2439085c6483720e84956ef9932f4f1ab95535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325540"
---
# <a name="iwmdrmsecuritycheckcertforrevocation-method"></a><span data-ttu-id="d8c1d-106">Metodo IWMDRMSecurity:: CheckCertForRevocation</span><span class="sxs-lookup"><span data-stu-id="d8c1d-106">IWMDRMSecurity::CheckCertForRevocation method</span></span>

<span data-ttu-id="d8c1d-107">Il metodo **CheckCertForRevocation** determina se un certificato è stato revocato.</span><span class="sxs-lookup"><span data-stu-id="d8c1d-107">The **CheckCertForRevocation** method determines whether a certificate has been revoked.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8c1d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d8c1d-108">Syntax</span></span>


```C++
HRESULT CheckCertForRevocation(
  [in]  REFGUID rguidRevocationList,
  [in]  BYTE    *pbCert,
  [in]  DWORD   cbCert,
  [out] BOOL    *fRevoked
);
```



## <a name="parameters"></a><span data-ttu-id="d8c1d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d8c1d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8c1d-110">*rguidRevocationList* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d8c1d-110">*rguidRevocationList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8c1d-111">GUID che identifica l'elenco di revoche da usare.</span><span class="sxs-lookup"><span data-stu-id="d8c1d-111">GUID identifying the revocation list to use.</span></span> <span data-ttu-id="d8c1d-112">Impostare su uno dei valori riportati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d8c1d-112">Set to one of the values in the following table.</span></span>



| <span data-ttu-id="d8c1d-113">Costante GUID</span><span class="sxs-lookup"><span data-stu-id="d8c1d-113">GUID constant</span></span>                 | <span data-ttu-id="d8c1d-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8c1d-114">Description</span></span>                                                                                |
|-------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8c1d-115">\_app WMDRM REVOCATIONTYPE \_</span><span class="sxs-lookup"><span data-stu-id="d8c1d-115">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="d8c1d-116">Specifica l'elenco di revoche di certificati dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d8c1d-116">Specifies the application certificate revocation list.</span></span>                                     |
| <span data-ttu-id="d8c1d-117">\_dispositivo REVOCATIONTYPE \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="d8c1d-117">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="d8c1d-118">Specifica l'elenco di revoche di certificati del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8c1d-118">Specifies the device certificate revocation list.</span></span>                                          |
| <span data-ttu-id="d8c1d-119">WMDRM \_ REVOCATIONTYPE \_ Cardea</span><span class="sxs-lookup"><span data-stu-id="d8c1d-119">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="d8c1d-120">Specifica l'elenco di revoche di certificati per i dispositivi di rete DRM di Microsoft Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d8c1d-120">Specifies the Microsoft Windows Media DRM for Network Devices certificate revocation list.</span></span> |



 

</dd> <dt>

<span data-ttu-id="d8c1d-121">*pbCert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d8c1d-121">*pbCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8c1d-122">Buffer contenente il certificato da ricercare.</span><span class="sxs-lookup"><span data-stu-id="d8c1d-122">Buffer containing the certificate to look up.</span></span>

</dd> <dt>

<span data-ttu-id="d8c1d-123">*cbCert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d8c1d-123">*cbCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8c1d-124">Dimensioni del buffer *pbCert* in byte.</span><span class="sxs-lookup"><span data-stu-id="d8c1d-124">Size of the buffer *pbCert*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="d8c1d-125">*fRevoked* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d8c1d-125">*fRevoked* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8c1d-126">In output indica se il certificato è presente nell'elenco di revoche.</span><span class="sxs-lookup"><span data-stu-id="d8c1d-126">On output, indicates whether the certificate is present in the revocation list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8c1d-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d8c1d-127">Return value</span></span>

<span data-ttu-id="d8c1d-128">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d8c1d-128">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d8c1d-129">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d8c1d-129">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d8c1d-130">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d8c1d-130">Return code</span></span>                                                                          | <span data-ttu-id="d8c1d-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8c1d-131">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d8c1d-132"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d8c1d-132"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d8c1d-133">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="d8c1d-133">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d8c1d-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8c1d-134">Requirements</span></span>



| <span data-ttu-id="d8c1d-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8c1d-135">Requirement</span></span> | <span data-ttu-id="d8c1d-136">Valore</span><span class="sxs-lookup"><span data-stu-id="d8c1d-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8c1d-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d8c1d-137">Header</span></span><br/>  | <dl> <span data-ttu-id="d8c1d-138"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8c1d-138"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="d8c1d-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="d8c1d-139">Library</span></span><br/> | <dl> <span data-ttu-id="d8c1d-140"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8c1d-140"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8c1d-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8c1d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8c1d-142">**Interfaccia IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="d8c1d-142">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 






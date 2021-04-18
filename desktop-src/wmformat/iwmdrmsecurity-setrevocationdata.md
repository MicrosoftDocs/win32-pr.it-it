---
title: Metodo IWMDRMSecurity SetRevocationData (wmdrmsdk. h)
description: Il metodo SetRevocationData imposta un elenco di revoche di certificati nell'archivio locale.
ms.assetid: 7e1c6d50-7a22-41b7-b29f-b1e5809a2097
keywords:
- Metodo SetRevocationData Windows Media Format
- Metodo SetRevocationData Windows Media Format, interfaccia IWMDRMSecurity
- Interfaccia IWMDRMSecurity-formato Windows Media, metodo SetRevocationData
topic_type:
- apiref
api_name:
- IWMDRMSecurity.SetRevocationData
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e3ece5a9285420261add123a61d0b7123896e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325534"
---
# <a name="iwmdrmsecuritysetrevocationdata-method"></a><span data-ttu-id="3688b-106">Metodo IWMDRMSecurity:: SetRevocationData</span><span class="sxs-lookup"><span data-stu-id="3688b-106">IWMDRMSecurity::SetRevocationData method</span></span>

<span data-ttu-id="3688b-107">Il metodo **SetRevocationData** imposta un elenco di revoche di certificati nell'archivio locale.</span><span class="sxs-lookup"><span data-stu-id="3688b-107">The **SetRevocationData** method sets a certificate revocation list in the local store.</span></span>

## <a name="syntax"></a><span data-ttu-id="3688b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3688b-108">Syntax</span></span>


```C++
HRESULT SetRevocationData(
  [in] REFGUID f_guidRevocationType,
  [in] BYTE    *f_pbCRL,
  [in] DWORD   f_cbCRL
);
```



## <a name="parameters"></a><span data-ttu-id="3688b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3688b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3688b-110">*\_ guidRevocationType f* \[\]</span><span class="sxs-lookup"><span data-stu-id="3688b-110">*f\_guidRevocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3688b-111">GUID che specifica il tipo di elenco di revoche.</span><span class="sxs-lookup"><span data-stu-id="3688b-111">GUID specifying the type of revocation list.</span></span> <span data-ttu-id="3688b-112">Impostare su una delle costanti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="3688b-112">Set to one of the constants in the following table.</span></span>



| <span data-ttu-id="3688b-113">Costante GUID</span><span class="sxs-lookup"><span data-stu-id="3688b-113">GUID constant</span></span>                 | <span data-ttu-id="3688b-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3688b-114">Description</span></span>                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3688b-115">\_app WMDRM REVOCATIONTYPE \_</span><span class="sxs-lookup"><span data-stu-id="3688b-115">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="3688b-116">Specifica l'elenco di revoche di certificati dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3688b-116">Specifies the application certificate revocation list.</span></span>                           |
| <span data-ttu-id="3688b-117">\_dispositivo REVOCATIONTYPE \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="3688b-117">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="3688b-118">Specifica l'elenco di revoche di certificati del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3688b-118">Specifies the device certificate revocation list.</span></span>                                |
| <span data-ttu-id="3688b-119">WMDRM \_ REVOCATIONTYPE \_ Cardea</span><span class="sxs-lookup"><span data-stu-id="3688b-119">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="3688b-120">Specifica Windows Media DRM per i dispositivi di rete elenco di revoche di certificati.</span><span class="sxs-lookup"><span data-stu-id="3688b-120">Specifies the Windows Media DRM for Network Devices certificate revocation list.</span></span> |



 

</dd> <dt>

<span data-ttu-id="3688b-121">*\_ pbCRL f* \[\]</span><span class="sxs-lookup"><span data-stu-id="3688b-121">*f\_pbCRL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3688b-122">Buffer contenente l'elenco di revoche di certificati.</span><span class="sxs-lookup"><span data-stu-id="3688b-122">Buffer containing the certificate revocation list.</span></span>

</dd> <dt>

<span data-ttu-id="3688b-123">*\_ cbCRL f* \[\]</span><span class="sxs-lookup"><span data-stu-id="3688b-123">*f\_cbCRL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3688b-124">Dimensioni del buffer, in byte.</span><span class="sxs-lookup"><span data-stu-id="3688b-124">Size of the buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3688b-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3688b-125">Return value</span></span>

<span data-ttu-id="3688b-126">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3688b-126">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3688b-127">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="3688b-127">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3688b-128">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3688b-128">Return code</span></span>                                                                          | <span data-ttu-id="3688b-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3688b-129">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3688b-130"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3688b-130"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3688b-131">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="3688b-131">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3688b-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3688b-132">Requirements</span></span>



| <span data-ttu-id="3688b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="3688b-133">Requirement</span></span> | <span data-ttu-id="3688b-134">Valore</span><span class="sxs-lookup"><span data-stu-id="3688b-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3688b-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3688b-135">Header</span></span><br/>  | <dl> <span data-ttu-id="3688b-136"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="3688b-136"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="3688b-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="3688b-137">Library</span></span><br/> | <dl> <span data-ttu-id="3688b-138"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3688b-138"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3688b-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3688b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3688b-140">**GetRevocationData**</span><span class="sxs-lookup"><span data-stu-id="3688b-140">**GetRevocationData**</span></span>](iwmdrmsecurity-getrevocationdata.md)
</dt> <dt>

[<span data-ttu-id="3688b-141">**GetRevocationDataVersion**</span><span class="sxs-lookup"><span data-stu-id="3688b-141">**GetRevocationDataVersion**</span></span>](iwmdrmsecurity-getrevocationdataversion.md)
</dt> <dt>

[<span data-ttu-id="3688b-142">**Interfaccia IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="3688b-142">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 






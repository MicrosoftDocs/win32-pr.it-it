---
title: Metodo IWMDRMSecurity GetRevocationData (wmdrmsdk. h)
description: Il metodo GetRevocationData recupera un elenco di revoche di certificati dall'archivio locale.
ms.assetid: 218f4f3a-02bc-4b1d-9320-e35ed8cc3b11
keywords:
- Metodo GetRevocationData Windows Media Format
- Metodo GetRevocationData Windows Media Format, interfaccia IWMDRMSecurity
- Interfaccia IWMDRMSecurity-formato Windows Media, metodo GetRevocationData
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetRevocationData
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c38e9e0b428a3922f84141ef855d8468b79b3bb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325538"
---
# <a name="iwmdrmsecuritygetrevocationdata-method"></a><span data-ttu-id="53b0f-106">Metodo IWMDRMSecurity:: GetRevocationData</span><span class="sxs-lookup"><span data-stu-id="53b0f-106">IWMDRMSecurity::GetRevocationData method</span></span>

<span data-ttu-id="53b0f-107">Il metodo **GetRevocationData** recupera un elenco di revoche di certificati dall'archivio locale.</span><span class="sxs-lookup"><span data-stu-id="53b0f-107">The **GetRevocationData** method retrieves a certificate revocation list from the local store.</span></span>

## <a name="syntax"></a><span data-ttu-id="53b0f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53b0f-108">Syntax</span></span>


```C++
HRESULT GetRevocationData(
  [in]      REFGUID f_guidRevocationType,
  [out]     BYTE    *f_pbCRL,
  [in, out] DWORD   *f_pcbCRL
);
```



## <a name="parameters"></a><span data-ttu-id="53b0f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="53b0f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53b0f-110">*\_ guidRevocationType f* \[\]</span><span class="sxs-lookup"><span data-stu-id="53b0f-110">*f\_guidRevocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53b0f-111">GUID che identifica il tipo di elenco di revoche da recuperare.</span><span class="sxs-lookup"><span data-stu-id="53b0f-111">GUID identifying the type of revocation list to retrieve.</span></span> <span data-ttu-id="53b0f-112">Utilizzare una delle costanti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="53b0f-112">Use one of the constants in the following table.</span></span>



| <span data-ttu-id="53b0f-113">Costante GUID</span><span class="sxs-lookup"><span data-stu-id="53b0f-113">GUID constant</span></span>                 | <span data-ttu-id="53b0f-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53b0f-114">Description</span></span>                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="53b0f-115">\_app WMDRM REVOCATIONTYPE \_</span><span class="sxs-lookup"><span data-stu-id="53b0f-115">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="53b0f-116">Specifica l'elenco di revoche di certificati dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="53b0f-116">Specifies the application certificate revocation list.</span></span>                           |
| <span data-ttu-id="53b0f-117">\_dispositivo REVOCATIONTYPE \_ WMDRM</span><span class="sxs-lookup"><span data-stu-id="53b0f-117">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="53b0f-118">Specifica l'elenco di revoche di certificati del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="53b0f-118">Specifies the device certificate revocation list.</span></span>                                |
| <span data-ttu-id="53b0f-119">WMDRM \_ REVOCATIONTYPE \_ Cardea</span><span class="sxs-lookup"><span data-stu-id="53b0f-119">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="53b0f-120">Specifica Windows Media DRM per i dispositivi di rete elenco di revoche di certificati.</span><span class="sxs-lookup"><span data-stu-id="53b0f-120">Specifies the Windows Media DRM for Network Devices certificate revocation list.</span></span> |



 

</dd> <dt>

<span data-ttu-id="53b0f-121">*f \_ pbCRL* \[\]</span><span class="sxs-lookup"><span data-stu-id="53b0f-121">*f\_pbCRL* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53b0f-122">Buffer che riceve l'elenco di revoche.</span><span class="sxs-lookup"><span data-stu-id="53b0f-122">Buffer that receives the revocation list.</span></span> <span data-ttu-id="53b0f-123">Impostare su **null** per ottenere la dimensione del buffer richiesta.</span><span class="sxs-lookup"><span data-stu-id="53b0f-123">Set to **NULL** to get the required buffer size.</span></span>

</dd> <dt>

<span data-ttu-id="53b0f-124">*f \_ pcbCRL* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="53b0f-124">*f\_pcbCRL* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="53b0f-125">Dimensione del buffer in byte.</span><span class="sxs-lookup"><span data-stu-id="53b0f-125">Size of the buffer in bytes.</span></span> <span data-ttu-id="53b0f-126">Se *f \_ PbCRL* è **null**, questo valore viene impostato sulla dimensione del buffer richiesta nell'output.</span><span class="sxs-lookup"><span data-stu-id="53b0f-126">If *f\_pbCRL* is **NULL**, this value is set to the required buffer size on output.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53b0f-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="53b0f-127">Return value</span></span>

<span data-ttu-id="53b0f-128">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="53b0f-128">The method returns an **HRESULT**.</span></span> <span data-ttu-id="53b0f-129">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="53b0f-129">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="53b0f-130">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="53b0f-130">Return code</span></span>                                                                          | <span data-ttu-id="53b0f-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53b0f-131">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="53b0f-132"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="53b0f-132"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="53b0f-133">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="53b0f-133">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="53b0f-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53b0f-134">Requirements</span></span>



| <span data-ttu-id="53b0f-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="53b0f-135">Requirement</span></span> | <span data-ttu-id="53b0f-136">Valore</span><span class="sxs-lookup"><span data-stu-id="53b0f-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53b0f-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="53b0f-137">Header</span></span><br/>  | <dl> <span data-ttu-id="53b0f-138"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="53b0f-138"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="53b0f-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="53b0f-139">Library</span></span><br/> | <dl> <span data-ttu-id="53b0f-140"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53b0f-140"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53b0f-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53b0f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53b0f-142">**Revoca e rinnovo automatici dei componenti**</span><span class="sxs-lookup"><span data-stu-id="53b0f-142">**Automated Component Revocation and Renewal**</span></span>](automated-component-revocation-and-renewal.md)
</dt> <dt>

[<span data-ttu-id="53b0f-143">**GetRevocationDataVersion**</span><span class="sxs-lookup"><span data-stu-id="53b0f-143">**GetRevocationDataVersion**</span></span>](iwmdrmsecurity-getrevocationdataversion.md)
</dt> <dt>

[<span data-ttu-id="53b0f-144">**Interfaccia IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="53b0f-144">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> <dt>

[<span data-ttu-id="53b0f-145">**SetRevocationData**</span><span class="sxs-lookup"><span data-stu-id="53b0f-145">**SetRevocationData**</span></span>](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 






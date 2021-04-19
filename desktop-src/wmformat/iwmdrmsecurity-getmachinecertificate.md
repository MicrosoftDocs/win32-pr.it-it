---
title: Metodo IWMDRMSecurity GetMachineCertificate (wmdrmsdk. h)
description: Il metodo GetMachineCertificate Recupera il certificato del computer del sottosistema DRM nel computer client.
ms.assetid: 38b8e812-e997-4a63-b906-ebd26a5556be
keywords:
- Metodo GetMachineCertificate Windows Media Format
- Metodo GetMachineCertificate Windows Media Format, interfaccia IWMDRMSecurity
- Interfaccia IWMDRMSecurity-formato Windows Media, metodo GetMachineCertificate
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetMachineCertificate
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d6c66c54ab9528a458910def5978ec83b191654
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327457"
---
# <a name="iwmdrmsecuritygetmachinecertificate-method"></a><span data-ttu-id="b91d3-106">Metodo IWMDRMSecurity:: GetMachineCertificate</span><span class="sxs-lookup"><span data-stu-id="b91d3-106">IWMDRMSecurity::GetMachineCertificate method</span></span>

<span data-ttu-id="b91d3-107">Il metodo **GetMachineCertificate** Recupera il certificato del computer del sottosistema DRM nel computer client.</span><span class="sxs-lookup"><span data-stu-id="b91d3-107">The **GetMachineCertificate** method retrieves the machine certificate of the DRM subsystem on the client computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="b91d3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b91d3-108">Syntax</span></span>


```C++
HRESULT GetMachineCertificate(
  [in]      DWORD dwCertificateType,
  [out]     BYTE  rgbVersion[4],
  [out]     BYTE  **ppbCertificate,
  [in, out] DWORD *pcbCertificate
);
```



## <a name="parameters"></a><span data-ttu-id="b91d3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b91d3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b91d3-110">*dwCertificateType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b91d3-110">*dwCertificateType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b91d3-111">Tipo di certificato da recuperare.</span><span class="sxs-lookup"><span data-stu-id="b91d3-111">Type of certificate to retrieve.</span></span> <span data-ttu-id="b91d3-112">Impostare su uno dei valori riportati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="b91d3-112">Set to one of the values in the following table.</span></span>



| <span data-ttu-id="b91d3-113">Valore</span><span class="sxs-lookup"><span data-stu-id="b91d3-113">Value</span></span>                        | <span data-ttu-id="b91d3-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b91d3-114">Description</span></span>                                                                           |
|------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b91d3-115">\_Tipo di certificato WMDRM \_ \_ V1</span><span class="sxs-lookup"><span data-stu-id="b91d3-115">WMDRM\_CERTIFICATE\_TYPE\_V1</span></span> | <span data-ttu-id="b91d3-116">Il certificato verrà recuperato nel formato utilizzato dai componenti legacy.</span><span class="sxs-lookup"><span data-stu-id="b91d3-116">The certificate will be retrieved in the format used by legacy components.</span></span>            |
| <span data-ttu-id="b91d3-117">\_Tipo di certificato WMDRM \_ \_ v2</span><span class="sxs-lookup"><span data-stu-id="b91d3-117">WMDRM\_CERTIFICATE\_TYPE\_V2</span></span> | <span data-ttu-id="b91d3-118">Il certificato verrà recuperato nel formato utilizzato dai componenti di Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b91d3-118">The certificate will be retrieved in the format used by the Windows Vista components.</span></span> |



 

</dd> <dt>

<span data-ttu-id="b91d3-119">*rgbVersion \[ 4 \]* in \[ uscita\]</span><span class="sxs-lookup"><span data-stu-id="b91d3-119">*rgbVersion\[4\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b91d3-120">Matrice di quattro byte che specifica la versione del sottosistema DRM nel computer client.</span><span class="sxs-lookup"><span data-stu-id="b91d3-120">Array of four bytes specifying the version of the DRM subsystem on the client computer.</span></span>

</dd> <dt>

<span data-ttu-id="b91d3-121">*ppbCertificate* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b91d3-121">*ppbCertificate* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b91d3-122">Indirizzo di una variabile che riceve un puntatore ai dati del certificato.</span><span class="sxs-lookup"><span data-stu-id="b91d3-122">Address of a variable that receives a pointer to the certificate data.</span></span> <span data-ttu-id="b91d3-123">Impostare su **null** per fare in modo che il metodo fornisca la dimensione del buffer necessaria per contenere il certificato in *pcbCertificate*.</span><span class="sxs-lookup"><span data-stu-id="b91d3-123">Set to **NULL** to have the method provide the buffer size required to hold the certificate in *pcbCertificate*.</span></span>

</dd> <dt>

<span data-ttu-id="b91d3-124">*pcbCertificate* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="b91d3-124">*pcbCertificate* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b91d3-125">Dimensioni in byte del certificato.</span><span class="sxs-lookup"><span data-stu-id="b91d3-125">Size of the certificate in bytes.</span></span> <span data-ttu-id="b91d3-126">Se *ppbCertificate* è **null**, questo valore verrà impostato sulle dimensioni del certificato.</span><span class="sxs-lookup"><span data-stu-id="b91d3-126">If *ppbCertificate* is **NULL**, this value will be set to the size of the certificate.</span></span> <span data-ttu-id="b91d3-127">Se *ppbCertificate* non è **null**, questo valore deve essere impostato sulla dimensione del buffer.</span><span class="sxs-lookup"><span data-stu-id="b91d3-127">If *ppbCertificate* is not **NULL**, this value must be set to the size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b91d3-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b91d3-128">Return value</span></span>

<span data-ttu-id="b91d3-129">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b91d3-129">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b91d3-130">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="b91d3-130">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b91d3-131">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b91d3-131">Return code</span></span>                                                                          | <span data-ttu-id="b91d3-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b91d3-132">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="b91d3-133"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b91d3-133"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="b91d3-134">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="b91d3-134">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b91d3-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b91d3-135">Requirements</span></span>



| <span data-ttu-id="b91d3-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="b91d3-136">Requirement</span></span> | <span data-ttu-id="b91d3-137">Valore</span><span class="sxs-lookup"><span data-stu-id="b91d3-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b91d3-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b91d3-138">Header</span></span><br/>  | <dl> <span data-ttu-id="b91d3-139"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="b91d3-139"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="b91d3-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="b91d3-140">Library</span></span><br/> | <dl> <span data-ttu-id="b91d3-141"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b91d3-141"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b91d3-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b91d3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b91d3-143">**Interfaccia IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="b91d3-143">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 






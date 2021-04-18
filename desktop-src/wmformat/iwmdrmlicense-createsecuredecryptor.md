---
title: Metodo IWMDRMLicense CreateSecureDecryptor (wmdrmsdk. h)
description: Il metodo CreateSecureDecryptor crea un oggetto di decrittografia protetto. Il decrittografia sicuro è diverso da quello normale in quanto decrittografa il contenuto e quindi lo crittografa nuovamente in base alle impostazioni specificate nei parametri di questo metodo.
ms.assetid: f3fe8d47-ec7b-4ba5-b5ae-6262cb455ffc
keywords:
- Metodo CreateSecureDecryptor Windows Media Format
- Metodo CreateSecureDecryptor Windows Media Format, interfaccia IWMDRMLicense
- Interfaccia IWMDRMLicense-formato Windows Media, metodo CreateSecureDecryptor
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateSecureDecryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ededb4c985e345c1e40563d02c87bfe447b8960f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324283"
---
# <a name="iwmdrmlicensecreatesecuredecryptor-method"></a><span data-ttu-id="20200-107">Metodo IWMDRMLicense:: CreateSecureDecryptor</span><span class="sxs-lookup"><span data-stu-id="20200-107">IWMDRMLicense::CreateSecureDecryptor method</span></span>

<span data-ttu-id="20200-108">Il metodo **CreateSecureDecryptor** crea un oggetto di decrittografia protetto.</span><span class="sxs-lookup"><span data-stu-id="20200-108">The **CreateSecureDecryptor** method creates a secure decryptor object.</span></span> <span data-ttu-id="20200-109">Il decrittografia sicuro è diverso da quello normale in quanto decrittografa il contenuto e quindi lo crittografa nuovamente in base alle impostazioni specificate nei parametri di questo metodo.</span><span class="sxs-lookup"><span data-stu-id="20200-109">The secure decryptor differs from the normal decryptor in that it decrypts the content and then re-encrypts it according to the settings specified in the parameters of this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="20200-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="20200-110">Syntax</span></span>


```C++
HRESULT CreateSecureDecryptor(
  [in]      BYTE          *pbCertificate,
  [in]      DWORD         cbCertificate,
  [in]      DWORD         dwCertificateType,
  [in]      DWORD         dwFlags,
  [out]     BYTE          *pbInitializationVector,
  [in, out] DWORD         *pcbInitializationVector,
  [out]     IWMDRMDecrypt **ppDecryptor
);
```



## <a name="parameters"></a><span data-ttu-id="20200-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="20200-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20200-112">*pbCertificate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20200-112">*pbCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20200-113">Certificato dell'applicazione chiamante.</span><span class="sxs-lookup"><span data-stu-id="20200-113">Certificate of the calling application.</span></span>

</dd> <dt>

<span data-ttu-id="20200-114">*cbCertificate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20200-114">*cbCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20200-115">Dimensioni in byte del certificato.</span><span class="sxs-lookup"><span data-stu-id="20200-115">Size of the certificate in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="20200-116">*dwCertificateType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20200-116">*dwCertificateType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20200-117">Tipo di certificato.</span><span class="sxs-lookup"><span data-stu-id="20200-117">The type of the certificate.</span></span> <span data-ttu-id="20200-118">Impostare sul \_ tipo di certificato WMDRM \_ \_ XML.</span><span class="sxs-lookup"><span data-stu-id="20200-118">Set to WMDRM\_CERTIFICATE\_TYPE\_XML.</span></span>

</dd> <dt>

<span data-ttu-id="20200-119">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20200-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20200-120">Tipo di protezione della sessione da utilizzare per la nuova codifica.</span><span class="sxs-lookup"><span data-stu-id="20200-120">The type of session protection to use for re-encoding.</span></span> <span data-ttu-id="20200-121">Deve essere impostato su una delle costanti della tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="20200-121">Must be set to one of the constants in the following table:</span></span>



| <span data-ttu-id="20200-122">Costante</span><span class="sxs-lookup"><span data-stu-id="20200-122">Constant</span></span>                     | <span data-ttu-id="20200-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20200-123">Description</span></span>                                                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20200-124">\_Tipo di protezione WMDRM \_ \_ RC4</span><span class="sxs-lookup"><span data-stu-id="20200-124">WMDRM\_PROTECTION\_TYPE\_RC4</span></span> | <span data-ttu-id="20200-125">Usa la crittografia RC4 per la crittografia della sessione.</span><span class="sxs-lookup"><span data-stu-id="20200-125">Uses RC4 encryption for session encryption.</span></span> <span data-ttu-id="20200-126">Questa è l'unica protezione della sessione supportata per questa versione.</span><span class="sxs-lookup"><span data-stu-id="20200-126">This is the only supported session protection for this version.</span></span> |



 

</dd> <dt>

<span data-ttu-id="20200-127">*pbInitializationVector* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="20200-127">*pbInitializationVector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20200-128">Riceve il vettore di inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="20200-128">Receives the initialization vector.</span></span> <span data-ttu-id="20200-129">Il vettore di inizializzazione è crittografato con RSA usando lo schema di riempimento OAEP con la chiave pubblica RSA trovata nel certificato.</span><span class="sxs-lookup"><span data-stu-id="20200-129">The initialization vector is RSA encrypted using the OAEP padding scheme with the RSA public key found in the certificate.</span></span> <span data-ttu-id="20200-130">Impostare su **null** per ricevere le dimensioni del buffer richieste in *pcbInitializationVector*.</span><span class="sxs-lookup"><span data-stu-id="20200-130">Set to **NULL** to receive the required buffer size in *pcbInitializationVector*.</span></span>

</dd> <dt>

<span data-ttu-id="20200-131">*pcbInitializationVector* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="20200-131">*pcbInitializationVector* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="20200-132">In input, dimensione del buffer passata come *pbInitializationVector*.</span><span class="sxs-lookup"><span data-stu-id="20200-132">On input, the size of the buffer passed as *pbInitializationVector*.</span></span> <span data-ttu-id="20200-133">Nell'output, dimensioni della parte utilizzata del buffer.</span><span class="sxs-lookup"><span data-stu-id="20200-133">On output, the size of the used portion of the buffer.</span></span> <span data-ttu-id="20200-134">Se si passa **null** per *pbInitializationVector*, questo valore viene impostato sulla dimensione del buffer richiesta nell'output.</span><span class="sxs-lookup"><span data-stu-id="20200-134">If you pass **NULL** for *pbInitializationVector*, this value is set to the required buffer size on output.</span></span>

</dd> <dt>

<span data-ttu-id="20200-135">*ppDecryptor* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="20200-135">*ppDecryptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20200-136">Riceve un puntatore all'interfaccia [**IWMDRMDecrypt**](iwmdrmdecrypt.md) dell'oggetto appena creato.</span><span class="sxs-lookup"><span data-stu-id="20200-136">Receives a pointer to the [**IWMDRMDecrypt**](iwmdrmdecrypt.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20200-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="20200-137">Return value</span></span>

<span data-ttu-id="20200-138">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="20200-138">The method returns an **HRESULT**.</span></span> <span data-ttu-id="20200-139">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="20200-139">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="20200-140">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="20200-140">Return code</span></span>                                                                          | <span data-ttu-id="20200-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20200-141">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="20200-142"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="20200-142"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="20200-143">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="20200-143">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="20200-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="20200-144">Remarks</span></span>

<span data-ttu-id="20200-145">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="20200-145">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="20200-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20200-146">Requirements</span></span>



| <span data-ttu-id="20200-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="20200-147">Requirement</span></span> | <span data-ttu-id="20200-148">Valore</span><span class="sxs-lookup"><span data-stu-id="20200-148">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="20200-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="20200-149">Header</span></span><br/> | <dl> <span data-ttu-id="20200-150"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="20200-150"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20200-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20200-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20200-152">**Interfaccia IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="20200-152">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 






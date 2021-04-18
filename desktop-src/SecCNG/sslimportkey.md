---
description: Importa una chiave nel provider del protocollo SSL (Secure Sockets Layer Protocol).
ms.assetid: 42310799-384e-4396-a9d5-5f226ca25a86
title: Funzione SslImportKey (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslImportKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8bf1b03fd5d51974db3676dcdbccc2a2b0fa4323
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310761"
---
# <a name="sslimportkey-function"></a><span data-ttu-id="c4368-103">SslImportKey (funzione)</span><span class="sxs-lookup"><span data-stu-id="c4368-103">SslImportKey function</span></span>

<span data-ttu-id="c4368-104">La funzione **SslImportKey** importa una chiave nel provider del protocollo SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="c4368-104">The **SslImportKey** function imports a key into the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4368-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4368-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslImportKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phKey,
  _In_  LPCWSTR            pszBlobType,
  _In_  PBYTE              pbKeyBlob,
  _In_  DWORD              cbKeyBlob,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="c4368-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c4368-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4368-107">*hSslProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4368-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4368-108">Handle per l'istanza del provider del protocollo SSL.</span><span class="sxs-lookup"><span data-stu-id="c4368-108">The handle to the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="c4368-109">*phKey* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c4368-109">*phKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4368-110">Puntatore all'handle della [*chiave crittografica*](/windows/desktop/SecGloss/c-gly) per la ricezione della chiave importata.</span><span class="sxs-lookup"><span data-stu-id="c4368-110">A pointer to the handle of the [*cryptographic key*](/windows/desktop/SecGloss/c-gly) to receive the imported key.</span></span>

</dd> <dt>

<span data-ttu-id="c4368-111">*pszBlobType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4368-111">*pszBlobType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4368-112">Stringa Unicode con terminazione null che contiene un identificatore che specifica il tipo di [*BLOB*](/windows/desktop/SecGloss/b-gly) contenuto nel buffer *pbInput* .</span><span class="sxs-lookup"><span data-stu-id="c4368-112">A null-terminated Unicode string that contains an identifier that specifies the type of [*BLOB*](/windows/desktop/SecGloss/b-gly) that is contained in the *pbInput* buffer.</span></span> <span data-ttu-id="c4368-113">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="c4368-113">This can be one of the following values.</span></span>



| <span data-ttu-id="c4368-114">Valore</span><span class="sxs-lookup"><span data-stu-id="c4368-114">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="c4368-115">Significato</span><span class="sxs-lookup"><span data-stu-id="c4368-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_DH_PUBLIC_BLOB"></span><span id="bcrypt_dh_public_blob"></span><dl> <span data-ttu-id="c4368-116"><dt>**\_ \_ BLOB pubblico di BCRYPT DH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c4368-116"><dt>**BCRYPT\_DH\_PUBLIC\_BLOB**</dt></span></span> </dl>    | <span data-ttu-id="c4368-117">Esportare una [*chiave pubblica*](/windows/desktop/SecGloss/p-gly)Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="c4368-117">Export a Diffie-Hellman [*public key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="c4368-118">Il buffer *pbOutput* riceve una [**struttura \_ \_ \_ BLOB di chiavi BCRYPT DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) immediatamente seguita dai dati della chiave.</span><span class="sxs-lookup"><span data-stu-id="c4368-118">The *pbOutput* buffer receives a [**BCRYPT\_DH\_KEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) structure immediately followed by the key data.</span></span><br/>                                                                                                                                                        |
| <span id="BCRYPT_ECCPUBLIC_BLOB"></span><span id="bcrypt_eccpublic_blob"></span><dl> <span data-ttu-id="c4368-119"><dt>**\_BLOB ECCPUBLIC \_ BCRYPT**</dt></span><span class="sxs-lookup"><span data-stu-id="c4368-119"><dt>**BCRYPT\_ECCPUBLIC\_BLOB**</dt></span></span> </dl>     | <span data-ttu-id="c4368-120">Esportare una [*chiave pubblica*](/windows/desktop/SecGloss/p-gly)di [*crittografia a curva ellittica*](/windows/desktop/SecGloss/e-gly) (ecc).</span><span class="sxs-lookup"><span data-stu-id="c4368-120">Export an [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC) [*public key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="c4368-121">Il buffer *pbOutput* riceve una [**struttura \_ \_ BLOB ECCKEY BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) immediatamente seguita dai dati della chiave.</span><span class="sxs-lookup"><span data-stu-id="c4368-121">The *pbOutput* buffer receives a [**BCRYPT\_ECCKEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) structure immediately followed by the key data.</span></span><br/>                             |
| <span id="BCRYPT_OPAQUE_KEY_BLOB"></span><span id="bcrypt_opaque_key_blob"></span><dl> <span data-ttu-id="c4368-122"><dt>**\_BLOB della \_ chiave OPACa BCRYPT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c4368-122"><dt>**BCRYPT\_OPAQUE\_KEY\_BLOB**</dt></span></span> </dl> | <span data-ttu-id="c4368-123">Esportare una [*chiave simmetrica*](/windows/desktop/SecGloss/s-gly) in un formato specifico per un singolo provider del [*servizio di crittografia*](/windows/desktop/SecGloss/c-gly) (CSP).</span><span class="sxs-lookup"><span data-stu-id="c4368-123">Export a [*symmetric key*](/windows/desktop/SecGloss/s-gly) in a format that is specific to a single [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP).</span></span> <span data-ttu-id="c4368-124">I BLOB opachi non sono trasferibili e devono essere importati utilizzando lo stesso CSP che ha generato il BLOB.</span><span class="sxs-lookup"><span data-stu-id="c4368-124">Opaque BLOBs are not transferable and must be imported by using the same CSP that generated the BLOB.</span></span><br/> |
| <span id="BCRYPT_RSAPUBLIC_BLOB"></span><span id="bcrypt_rsapublic_blob"></span><dl> <span data-ttu-id="c4368-125"><dt>**\_BLOB RSAPUBLIC \_ BCRYPT**</dt></span><span class="sxs-lookup"><span data-stu-id="c4368-125"><dt>**BCRYPT\_RSAPUBLIC\_BLOB**</dt></span></span> </dl>     | <span data-ttu-id="c4368-126">Esportare una chiave pubblica [*RSA*](/windows/desktop/SecGloss/r-gly) .</span><span class="sxs-lookup"><span data-stu-id="c4368-126">Export an [*RSA*](/windows/desktop/SecGloss/r-gly) public key.</span></span> <span data-ttu-id="c4368-127">Il buffer *pbOutput* riceve una [**struttura \_ \_ BLOB rsaKey BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) immediatamente seguita dai dati della chiave.</span><span class="sxs-lookup"><span data-stu-id="c4368-127">The *pbOutput* buffer receives a [**BCRYPT\_RSAKEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) structure immediately followed by the key data.</span></span><br/>                                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="c4368-128">*pbKeyBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4368-128">*pbKeyBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4368-129">Puntatore al buffer che contiene il BLOB della [*chiave*](/windows/desktop/SecGloss/k-gly).</span><span class="sxs-lookup"><span data-stu-id="c4368-129">A pointer to the buffer that contains the [*key BLOB*](/windows/desktop/SecGloss/k-gly).</span></span>

</dd> <dt>

<span data-ttu-id="c4368-130">*cbKeyBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4368-130">*cbKeyBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4368-131">Dimensione, in byte, del buffer *pbKeyBlob* .</span><span class="sxs-lookup"><span data-stu-id="c4368-131">The size, in bytes, of the *pbKeyBlob* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c4368-132">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4368-132">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4368-133">Questo parametro è riservato per usi futuri.</span><span class="sxs-lookup"><span data-stu-id="c4368-133">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4368-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c4368-134">Return value</span></span>

<span data-ttu-id="c4368-135">Se la funzione ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="c4368-135">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="c4368-136">Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="c4368-136">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="c4368-137">I codici restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="c4368-137">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="c4368-138">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="c4368-138">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="c4368-139">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4368-139">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c4368-140"><dt>**Nte \_ Nessun \_**</dt> <dt>0x8009000EL</dt> di memoria</span><span class="sxs-lookup"><span data-stu-id="c4368-140"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="c4368-141">La memoria disponibile non è sufficiente per allocare i buffer necessari.</span><span class="sxs-lookup"><span data-stu-id="c4368-141">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="c4368-142"><dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c4368-142"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="c4368-143">Handle *hSslProvider* non valido.</span><span class="sxs-lookup"><span data-stu-id="c4368-143">The *hSslProvider* handle is not valid.</span></span><br/>                       |
| <dl> <span data-ttu-id="c4368-144"><dt>**Nte \_ \_Parametro 0X80090027L non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c4368-144"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="c4368-145">Il parametro *phKey* è **null**.</span><span class="sxs-lookup"><span data-stu-id="c4368-145">The *phKey* parameter is **NULL**.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="c4368-146">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4368-146">Remarks</span></span>

<span data-ttu-id="c4368-147">È possibile utilizzare la funzione **SslImportKey** per importare le chiavi della sessione come parte del processo di trasferimento delle chiavi di sessione da un processo a un altro.</span><span class="sxs-lookup"><span data-stu-id="c4368-147">You can use the **SslImportKey** function to import session keys as a part of the process of transferring session keys from one process to another.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4368-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4368-148">Requirements</span></span>



| <span data-ttu-id="c4368-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4368-149">Requirement</span></span> | <span data-ttu-id="c4368-150">Valore</span><span class="sxs-lookup"><span data-stu-id="c4368-150">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4368-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4368-151">Minimum supported client</span></span><br/> | <span data-ttu-id="c4368-152">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c4368-152">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c4368-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4368-153">Minimum supported server</span></span><br/> | <span data-ttu-id="c4368-154">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c4368-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c4368-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c4368-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4368-156"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4368-156"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="c4368-157">DLL</span><span class="sxs-lookup"><span data-stu-id="c4368-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4368-158"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4368-158"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 


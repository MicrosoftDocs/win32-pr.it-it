---
description: Restituisce una chiave di sessione SSL (Secure Sockets Layer Protocol) o una chiave temporanea pubblica in un BLOB serializzato.
ms.assetid: c978e6ac-a535-4625-8598-4aa16484dcad
title: Funzione SslExportKey (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslExportKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: c5fcbcfa1a8b6c1aa9922b98a7699bdf2bf4b0fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967180"
---
# <a name="sslexportkey-function"></a><span data-ttu-id="4dd93-103">SslExportKey (funzione)</span><span class="sxs-lookup"><span data-stu-id="4dd93-103">SslExportKey function</span></span>

<span data-ttu-id="4dd93-104">La funzione **SslExportKey** restituisce una [*chiave di sessione*](/windows/desktop/SecGloss/s-gly) SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ) o una chiave temporanea pubblica in un [*BLOB*](/windows/desktop/SecGloss/b-gly)serializzato.</span><span class="sxs-lookup"><span data-stu-id="4dd93-104">The **SslExportKey** function returns an [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) [*session key*](/windows/desktop/SecGloss/s-gly) or public ephemeral key into a serialized [*BLOB*](/windows/desktop/SecGloss/b-gly).</span></span>

## <a name="syntax"></a><span data-ttu-id="4dd93-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4dd93-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslExportKey(
  _In_      NCRYPT_PROV_HANDLE hSslProvider,
  _In_      NCRYPT_KEY_HANDLE  hKey,
  _In_      LPCWSTR            pszBlobType,
  _Out_opt_ PBYTE              pbOutput,
  _In_      DWORD              cbOutput,
  _Out_     DWORD              *pcbResult,
  _In_      DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="4dd93-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4dd93-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4dd93-107">*hSslProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4dd93-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4dd93-108">Handle dell'istanza del provider del protocollo SSL.</span><span class="sxs-lookup"><span data-stu-id="4dd93-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="4dd93-109">*HKEY* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4dd93-109">*hKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4dd93-110">Handle della chiave da esportare.</span><span class="sxs-lookup"><span data-stu-id="4dd93-110">The handle of the key to export.</span></span>

<span data-ttu-id="4dd93-111">Quando non si specifica una chiave, impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="4dd93-111">When you are not specifying a key, set this parameter to **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="4dd93-112">Un handle *HKEY* viene ottenuto chiamando la funzione [**SslOpenPrivateKey**](sslopenprivatekey.md) .</span><span class="sxs-lookup"><span data-stu-id="4dd93-112">A *hKey* handle is obtained by calling the [**SslOpenPrivateKey**](sslopenprivatekey.md) function.</span></span> <span data-ttu-id="4dd93-113">Gli handle ottenuti dalla funzione [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="4dd93-113">Handles obtained from the [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) function are not supported.</span></span>

 

</dd> <dt>

<span data-ttu-id="4dd93-114">*pszBlobType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4dd93-114">*pszBlobType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4dd93-115">Stringa Unicode con terminazione null che contiene un identificatore che specifica il tipo di BLOB da esportare.</span><span class="sxs-lookup"><span data-stu-id="4dd93-115">A null-terminated Unicode string that contains an identifier that specifies the type of BLOB to export.</span></span> <span data-ttu-id="4dd93-116">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="4dd93-116">This can be one of the following values.</span></span>



| <span data-ttu-id="4dd93-117">Valore</span><span class="sxs-lookup"><span data-stu-id="4dd93-117">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="4dd93-118">Significato</span><span class="sxs-lookup"><span data-stu-id="4dd93-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BCRYPT_DH_PUBLIC_BLOB"></span><span id="bcrypt_dh_public_blob"></span><dl> <span data-ttu-id="4dd93-119"><dt>**\_ \_ BLOB pubblico di BCRYPT DH \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4dd93-119"><dt>**BCRYPT\_DH\_PUBLIC\_BLOB**</dt></span></span> </dl>    | <span data-ttu-id="4dd93-120">Esportare una [*chiave pubblica*](/windows/desktop/SecGloss/p-gly)Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="4dd93-120">Export a Diffie-Hellman [*public key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="4dd93-121">Il buffer *pbOutput* riceve una [**struttura \_ \_ \_ BLOB di chiavi BCRYPT DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) immediatamente seguita dai dati della chiave.</span><span class="sxs-lookup"><span data-stu-id="4dd93-121">The *pbOutput* buffer receives a [**BCRYPT\_DH\_KEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_key_blob) structure immediately followed by the key data.</span></span><br/>                                                                                                               |
| <span id="BCRYPT_ECCPUBLIC_BLOB"></span><span id="bcrypt_eccpublic_blob"></span><dl> <span data-ttu-id="4dd93-122"><dt>**\_BLOB ECCPUBLIC \_ BCRYPT**</dt></span><span class="sxs-lookup"><span data-stu-id="4dd93-122"><dt>**BCRYPT\_ECCPUBLIC\_BLOB**</dt></span></span> </dl>     | <span data-ttu-id="4dd93-123">Esportare una chiave pubblica di [*crittografia a curva ellittica*](/windows/desktop/SecGloss/e-gly) (ecc).</span><span class="sxs-lookup"><span data-stu-id="4dd93-123">Export an [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC) public key.</span></span> <span data-ttu-id="4dd93-124">Il buffer *pbOutput* riceve una [**struttura \_ \_ BLOB ECCKEY BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) immediatamente seguita dai dati della chiave.</span><span class="sxs-lookup"><span data-stu-id="4dd93-124">The *pbOutput* buffer receives a [**BCRYPT\_ECCKEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_ecckey_blob) structure immediately followed by the key data.</span></span><br/>                                                          |
| <span id="BCRYPT_OPAQUE_KEY_BLOB"></span><span id="bcrypt_opaque_key_blob"></span><dl> <span data-ttu-id="4dd93-125"><dt>**\_BLOB della \_ chiave OPACa BCRYPT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4dd93-125"><dt>**BCRYPT\_OPAQUE\_KEY\_BLOB**</dt></span></span> </dl> | <span data-ttu-id="4dd93-126">Esportare una chiave simmetrica in un formato specifico per un singolo provider del [*servizio di crittografia*](/windows/desktop/SecGloss/c-gly) (CSP).</span><span class="sxs-lookup"><span data-stu-id="4dd93-126">Export a symmetric key in a format that is specific to a single [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP).</span></span> <span data-ttu-id="4dd93-127">I BLOB opachi non sono trasferibili e devono essere importati utilizzando lo stesso *provider del servizio di crittografia* (CSP) che ha generato il BLOB.</span><span class="sxs-lookup"><span data-stu-id="4dd93-127">Opaque BLOBs are not transferable and must be imported by using the same *cryptographic service provider* (CSP) that generated the BLOB.</span></span><br/> |
| <span id="BCRYPT_RSAPUBLIC_BLOB"></span><span id="bcrypt_rsapublic_blob"></span><dl> <span data-ttu-id="4dd93-128"><dt>**\_BLOB RSAPUBLIC \_ BCRYPT**</dt></span><span class="sxs-lookup"><span data-stu-id="4dd93-128"><dt>**BCRYPT\_RSAPUBLIC\_BLOB**</dt></span></span> </dl>     | <span data-ttu-id="4dd93-129">Esportare una chiave pubblica RSA.</span><span class="sxs-lookup"><span data-stu-id="4dd93-129">Export an RSA public key.</span></span> <span data-ttu-id="4dd93-130">Il buffer *pbOutput* riceve una [**struttura \_ \_ BLOB rsaKey BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) immediatamente seguita dai dati della chiave.</span><span class="sxs-lookup"><span data-stu-id="4dd93-130">The *pbOutput* buffer receives a [**BCRYPT\_RSAKEY\_BLOB**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_rsakey_blob) structure immediately followed by the key data.</span></span><br/>                                                                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="4dd93-131">*pbOutput* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="4dd93-131">*pbOutput* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4dd93-132">Indirizzo di un buffer che riceve il [*BLOB della chiave*](/windows/desktop/SecGloss/k-gly).</span><span class="sxs-lookup"><span data-stu-id="4dd93-132">The address of a buffer that receives the [*key BLOB*](/windows/desktop/SecGloss/k-gly).</span></span> <span data-ttu-id="4dd93-133">Il parametro *cbOutput* contiene la dimensione del buffer.</span><span class="sxs-lookup"><span data-stu-id="4dd93-133">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="4dd93-134">Se questo parametro è **null**, questa funzione inserisce la dimensione richiesta, in byte, nel **valore DWORD** a cui fa riferimento il parametro *pcbResult* .</span><span class="sxs-lookup"><span data-stu-id="4dd93-134">If this parameter is **NULL**, this function will place the required size, in bytes, in the **DWORD** pointed to by the *pcbResult* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4dd93-135">*cbOutput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4dd93-135">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4dd93-136">Dimensione, in byte, del buffer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="4dd93-136">The size, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="4dd93-137">*pcbResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4dd93-137">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4dd93-138">Indirizzo di una variabile **DWORD** che riceve il numero di byte copiati nel buffer di *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="4dd93-138">The address of a **DWORD** variable that receives the number of bytes copied to the *pbOutput* buffer.</span></span> <span data-ttu-id="4dd93-139">Se il parametro *pbOutput* è impostato su **null** quando viene chiamata la funzione, la dimensione richiesta per il buffer *pbOutput* , in byte, viene restituita nel **valore DWORD** a cui punta il parametro.</span><span class="sxs-lookup"><span data-stu-id="4dd93-139">If the *pbOutput* parameter is set to **NULL** when the function is called, the required size for the *pbOutput* buffer, in bytes, is returned in the **DWORD** pointed to by this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4dd93-140">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4dd93-140">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4dd93-141">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="4dd93-141">Reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4dd93-142">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4dd93-142">Return value</span></span>

<span data-ttu-id="4dd93-143">Se la funzione ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="4dd93-143">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="4dd93-144">Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="4dd93-144">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="4dd93-145">I codici restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="4dd93-145">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="4dd93-146">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="4dd93-146">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="4dd93-147">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4dd93-147">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="4dd93-148"><dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4dd93-148"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="4dd93-149">Uno degli handle forniti non è valido.</span><span class="sxs-lookup"><span data-stu-id="4dd93-149">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4dd93-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="4dd93-150">Remarks</span></span>

<span data-ttu-id="4dd93-151">La funzione **SslExportKey** facilita il trasporto di chiavi di sessione da un processo a un altro e l'esportazione della parte pubblica di una chiave temporanea.</span><span class="sxs-lookup"><span data-stu-id="4dd93-151">The **SslExportKey** function facilitates transporting session keys from one process to another as well as exporting the public portion an ephemeral key.</span></span>

<span data-ttu-id="4dd93-152">Quando si esportano le chiavi di sessione, il tipo di BLOB è opaco, vale a dire che il formato del BLOB è irrilevante, purché entrambe le funzioni **SslExportKey** e [**SslImportKey**](sslimportkey.md) possano interpretarlo.</span><span class="sxs-lookup"><span data-stu-id="4dd93-152">When exporting session keys, the BLOB type is opaque, meaning that the format of the BLOB is irrelevant as long as both the **SslExportKey** and [**SslImportKey**](sslimportkey.md) functions can interpret it.</span></span>

<span data-ttu-id="4dd93-153">Quando si esporta la parte pubblica di una chiave temporanea, il tipo di BLOB deve essere il tipo appropriato, ad esempio il BLOB **\_ pubblico NCRYPT DH \_ \_** o il **\_ \_ BLOB ECCPUBLIC NCRYPT**.</span><span class="sxs-lookup"><span data-stu-id="4dd93-153">When exporting the public portion of an ephemeral key the BLOB type must be the appropriate type, such as **NCRYPT\_DH\_PUBLIC\_BLOB** or **NCRYPT\_ECCPUBLIC\_BLOB**.</span></span>

## <a name="requirements"></a><span data-ttu-id="4dd93-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4dd93-154">Requirements</span></span>



| <span data-ttu-id="4dd93-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="4dd93-155">Requirement</span></span> | <span data-ttu-id="4dd93-156">Valore</span><span class="sxs-lookup"><span data-stu-id="4dd93-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dd93-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4dd93-157">Minimum supported client</span></span><br/> | <span data-ttu-id="4dd93-158">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4dd93-158">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4dd93-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4dd93-159">Minimum supported server</span></span><br/> | <span data-ttu-id="4dd93-160">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4dd93-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4dd93-161">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4dd93-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="4dd93-162"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="4dd93-162"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="4dd93-163">DLL</span><span class="sxs-lookup"><span data-stu-id="4dd93-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4dd93-164"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4dd93-164"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 


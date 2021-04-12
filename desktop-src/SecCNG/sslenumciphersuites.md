---
description: Enumera i pacchetti di crittografia supportati da un provider del protocollo SSL (Secure Sockets Layer Protocol).
ms.assetid: c12bc422-71c9-44f4-abf7-76902b19d3bd
title: Funzione SslEnumCipherSuites (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEnumCipherSuites
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8991842f38f3d3dc3d721cd30ebfb857ad20308a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345041"
---
# <a name="sslenumciphersuites-function"></a><span data-ttu-id="e9bb2-103">SslEnumCipherSuites (funzione)</span><span class="sxs-lookup"><span data-stu-id="e9bb2-103">SslEnumCipherSuites function</span></span>

<span data-ttu-id="e9bb2-104">La funzione **SslEnumCipherSuites** enumera i pacchetti di crittografia supportati da un provider del protocollo SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="e9bb2-104">The **SslEnumCipherSuites** function enumerates the cipher suites supported by a [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9bb2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9bb2-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslEnumCipherSuites(
  _In_     NCRYPT_PROV_HANDLE      hSslProvider,
  _In_opt_ NCRYPT_KEY_HANDLE       hPrivateKey,
  _Out_    NCRYPT_SSL_CIPHER_SUITE **ppCipherSuite,
  _Inout_  PVOID                   *ppEnumState,
  _In_     DWORD                   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="e9bb2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9bb2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9bb2-107">*hSslProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9bb2-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9bb2-108">Handle dell'istanza del provider del protocollo SSL.</span><span class="sxs-lookup"><span data-stu-id="e9bb2-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="e9bb2-109">*hPrivateKey* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e9bb2-109">*hPrivateKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e9bb2-110">Handle di una [*chiave privata*](/windows/desktop/SecGloss/p-gly).</span><span class="sxs-lookup"><span data-stu-id="e9bb2-110">The handle of a [*private key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="e9bb2-111">Quando si specifica una chiave privata, **SslEnumCipherSuites** enumera i pacchetti di crittografia compatibili con la chiave privata.</span><span class="sxs-lookup"><span data-stu-id="e9bb2-111">When a private key is specified, **SslEnumCipherSuites** enumerates the cipher suites that are compatible with the private key.</span></span> <span data-ttu-id="e9bb2-112">Ad esempio, se la chiave privata è una chiave DSS, vengono restituiti solo i pacchetti di \_ crittografia DSS dhe.</span><span class="sxs-lookup"><span data-stu-id="e9bb2-112">For example, if the private key is a DSS key, then only the DSS\_DHE cipher suites are returned.</span></span> <span data-ttu-id="e9bb2-113">Se la chiave privata è una chiave RSA, ma non supporta le operazioni di decrittografia non elaborate, i pacchetti di crittografia SSL2 non vengono restituiti.</span><span class="sxs-lookup"><span data-stu-id="e9bb2-113">If the private key is an RSA key, but it does not support raw decryption operations, then the SSL2 cipher suites are not returned.</span></span>

<span data-ttu-id="e9bb2-114">Se non si specifica una chiave privata, impostare questo parametro su **null** .</span><span class="sxs-lookup"><span data-stu-id="e9bb2-114">Set this parameter to **NULL** when you are not specifying a private key.</span></span>

> [!Note]  
> <span data-ttu-id="e9bb2-115">Un handle *hPrivateKey* viene ottenuto chiamando la funzione [**SslOpenPrivateKey**](sslopenprivatekey.md) .</span><span class="sxs-lookup"><span data-stu-id="e9bb2-115">A *hPrivateKey* handle is obtained by calling the [**SslOpenPrivateKey**](sslopenprivatekey.md) function.</span></span> <span data-ttu-id="e9bb2-116">Gli handle ottenuti dalla funzione [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="e9bb2-116">Handles obtained from the [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) function are not supported.</span></span>

 

</dd> <dt>

<span data-ttu-id="e9bb2-117">*ppCipherSuite* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e9bb2-117">*ppCipherSuite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9bb2-118">Puntatore a una struttura [**del \_ \_ \_ pacchetto di crittografia SSL NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) per ricevere l'indirizzo del pacchetto di crittografia successivo nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="e9bb2-118">A pointer to a [**NCRYPT\_SSL\_CIPHER\_SUITE**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) structure to receive the address of the next cipher suite in the list.</span></span>

</dd> <dt>

<span data-ttu-id="e9bb2-119">*ppEnumState* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="e9bb2-119">*ppEnumState* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9bb2-120">Puntatore a un buffer che indica la posizione corrente nell'elenco dei pacchetti di crittografia.</span><span class="sxs-lookup"><span data-stu-id="e9bb2-120">A pointer to a buffer that indicates the current position in the list of cipher suites.</span></span>

<span data-ttu-id="e9bb2-121">Impostare il puntatore su **null** nella prima chiamata a **SslEnumCipherSuites**.</span><span class="sxs-lookup"><span data-stu-id="e9bb2-121">Set the pointer to **NULL** on the first call to **SslEnumCipherSuites**.</span></span> <span data-ttu-id="e9bb2-122">Per ogni chiamata successiva, passare il valore non modificato di nuovo a **SslEnumCipherSuites**.</span><span class="sxs-lookup"><span data-stu-id="e9bb2-122">On each subsequent call, pass the unmodified value back to **SslEnumCipherSuites**.</span></span>

<span data-ttu-id="e9bb2-123">Quando non sono disponibili altri pacchetti di crittografia, è necessario liberare *ppEnumState* chiamando la funzione [**SslFreeBuffer**](sslfreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="e9bb2-123">When there are no more cipher suites available, you should free *ppEnumState* by calling the [**SslFreeBuffer**](sslfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="e9bb2-124">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9bb2-124">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9bb2-125">Questo parametro è riservato per usi futuri.</span><span class="sxs-lookup"><span data-stu-id="e9bb2-125">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9bb2-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9bb2-126">Return value</span></span>

<span data-ttu-id="e9bb2-127">Se la funzione ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="e9bb2-127">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="e9bb2-128">Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="e9bb2-128">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="e9bb2-129">I codici restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="e9bb2-129">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="e9bb2-130">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9bb2-130">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="e9bb2-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9bb2-131">Description</span></span>                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e9bb2-132"><dt>**Nte \_ Nessun \_**</dt> <dt>0x8009000EL</dt> di memoria</span><span class="sxs-lookup"><span data-stu-id="e9bb2-132"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>      | <span data-ttu-id="e9bb2-133">La memoria disponibile non è sufficiente per allocare i buffer necessari.</span><span class="sxs-lookup"><span data-stu-id="e9bb2-133">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="e9bb2-134"><dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e9bb2-134"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="e9bb2-135">Uno degli handle forniti non è valido.</span><span class="sxs-lookup"><span data-stu-id="e9bb2-135">One of the provided handles is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="e9bb2-136"><dt>**Nte \_ Nessun \_ altro \_ elemento**</dt> <dt>0x8009002AL</dt></span><span class="sxs-lookup"><span data-stu-id="e9bb2-136"><dt>**NTE\_NO\_MORE\_ITEMS**</dt> <dt>0x8009002AL</dt></span></span> </dl> | <span data-ttu-id="e9bb2-137">Non sono supportati altri pacchetti di crittografia.</span><span class="sxs-lookup"><span data-stu-id="e9bb2-137">No additional cipher suites are supported.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="e9bb2-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9bb2-138">Remarks</span></span>

<span data-ttu-id="e9bb2-139">Per enumerare tutti i pacchetti di crittografia supportati dal provider SSL, chiamare la funzione **SslEnumCipherSuites** in un ciclo fino a quando non viene restituito **\_ nessun \_ altro \_ elemento** .</span><span class="sxs-lookup"><span data-stu-id="e9bb2-139">To enumerate all cipher suites supported by the SSL provider, call the **SslEnumCipherSuites** function in a loop until **NTE\_NO\_MORE\_ITEMS** is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9bb2-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9bb2-140">Requirements</span></span>



| <span data-ttu-id="e9bb2-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9bb2-141">Requirement</span></span> | <span data-ttu-id="e9bb2-142">Valore</span><span class="sxs-lookup"><span data-stu-id="e9bb2-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9bb2-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9bb2-143">Minimum supported client</span></span><br/> | <span data-ttu-id="e9bb2-144">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e9bb2-144">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e9bb2-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9bb2-145">Minimum supported server</span></span><br/> | <span data-ttu-id="e9bb2-146">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e9bb2-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e9bb2-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9bb2-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9bb2-148"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9bb2-148"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="e9bb2-149">Libreria</span><span class="sxs-lookup"><span data-stu-id="e9bb2-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="e9bb2-150"><dt>Ncrypt. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9bb2-150"><dt>Ncrypt.lib</dt></span></span> </dl>    |
| <span data-ttu-id="e9bb2-151">DLL</span><span class="sxs-lookup"><span data-stu-id="e9bb2-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9bb2-152"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9bb2-152"><dt>Ncrypt.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="e9bb2-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9bb2-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9bb2-154">**\_pacchetto di \_ crittografia \_ SSL NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="e9bb2-154">**NCRYPT\_SSL\_CIPHER\_SUITE**</span></span>](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**)
</dt> </dl>

 


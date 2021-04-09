---
description: Calcola l'hash inviato nel messaggio terminato dell'handshake del protocollo di Secure Sockets Layer (SSL).
ms.assetid: 82dfeb1d-c141-40c9-b692-daad78ab6d55
title: Funzione SslComputeFinishedHash (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeFinishedHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 365f3c849b0a499d2bd875c8d234bbda1911eb71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967185"
---
# <a name="sslcomputefinishedhash-function"></a><span data-ttu-id="3b525-103">SslComputeFinishedHash (funzione)</span><span class="sxs-lookup"><span data-stu-id="3b525-103">SslComputeFinishedHash function</span></span>

<span data-ttu-id="3b525-104">La funzione **SslComputeFinishedHash** calcola l' [*hash*](/windows/desktop/SecGloss/h-gly) inviato nel messaggio finito dell'handshake SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="3b525-104">The **SslComputeFinishedHash** function computes the [*hash*](/windows/desktop/SecGloss/h-gly) sent in the finished message of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) handshake.</span></span> <span data-ttu-id="3b525-105">Per ulteriori informazioni sulla sequenza di handshake SSL, vedere [la descrizione dell'handshake Secure Sockets Layer (SSL)](https://support.microsoft.com/kb/257591).</span><span class="sxs-lookup"><span data-stu-id="3b525-105">For more information about the SSL handshake sequence, see [Description of the Secure Sockets Layer (SSL) Handshake](https://support.microsoft.com/kb/257591).</span></span>

## <a name="syntax"></a><span data-ttu-id="3b525-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3b525-106">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslComputeFinishedHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _In_  NCRYPT_HASH_HANDLE hHandshakeHash,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="3b525-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3b525-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b525-108">*hSslProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3b525-108">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b525-109">Handle dell'istanza del provider del protocollo SSL.</span><span class="sxs-lookup"><span data-stu-id="3b525-109">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="3b525-110">*hMasterKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3b525-110">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b525-111">Handle dell'oggetto [*chiave master*](/windows/desktop/SecGloss/m-gly) .</span><span class="sxs-lookup"><span data-stu-id="3b525-111">The handle of the [*master key*](/windows/desktop/SecGloss/m-gly) object.</span></span>

</dd> <dt>

<span data-ttu-id="3b525-112">*hHandshakeHash* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3b525-112">*hHandshakeHash* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b525-113">Handle dell'hash dei messaggi di handshake.</span><span class="sxs-lookup"><span data-stu-id="3b525-113">The handle of the hash of the handshake messages.</span></span>

</dd> <dt>

<span data-ttu-id="3b525-114">*pbOutput* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3b525-114">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b525-115">Puntatore a un buffer che riceve l'hash per il messaggio di fine.</span><span class="sxs-lookup"><span data-stu-id="3b525-115">A pointer to a buffer that receives the hash for the finish message.</span></span>

</dd> <dt>

<span data-ttu-id="3b525-116">*cbOutput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3b525-116">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b525-117">Lunghezza, in byte, del buffer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="3b525-117">The length, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3b525-118">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3b525-118">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b525-119">Una delle seguenti costanti.</span><span class="sxs-lookup"><span data-stu-id="3b525-119">One of the following constants.</span></span>



| <span data-ttu-id="3b525-120">Valore</span><span class="sxs-lookup"><span data-stu-id="3b525-120">Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="3b525-121">Significato</span><span class="sxs-lookup"><span data-stu-id="3b525-121">Meaning</span></span>                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <span data-ttu-id="3b525-122"><dt>**NCRYPT \_ \_ \_ Flag client SSL**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="3b525-122"><dt>**NCRYPT\_SSL\_CLIENT\_FLAG**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="3b525-123">Specifica che si tratta di una chiamata client.</span><span class="sxs-lookup"><span data-stu-id="3b525-123">Specifies that this is a client call.</span></span><br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <span data-ttu-id="3b525-124"><dt>**NCRYPT \_ \_ \_ Flag server SSL**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="3b525-124"><dt>**NCRYPT\_SSL\_SERVER\_FLAG**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="3b525-125">Specifica che si tratta di una chiamata al server.</span><span class="sxs-lookup"><span data-stu-id="3b525-125">Specifies that this is a server call.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b525-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3b525-126">Return value</span></span>

<span data-ttu-id="3b525-127">Se la funzione ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="3b525-127">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="3b525-128">Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="3b525-128">If the function fails, it returns a nonzero error value.</span></span>



| <span data-ttu-id="3b525-129">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="3b525-129">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="3b525-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b525-130">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="3b525-131"><dt>**Nte \_ \_Handle non valido**</dt> <dt>2148073510 (0x80090026)</dt></span><span class="sxs-lookup"><span data-stu-id="3b525-131"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>2148073510 (0x80090026)</dt></span></span> </dl> | <span data-ttu-id="3b525-132">Uno degli handle forniti non è valido.</span><span class="sxs-lookup"><span data-stu-id="3b525-132">One of the supplied handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3b525-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="3b525-133">Remarks</span></span>

<span data-ttu-id="3b525-134">La funzione **SslComputeFinishedHash** è una delle tre funzioni usate per generare un hash da usare durante l'handshake SSL.</span><span class="sxs-lookup"><span data-stu-id="3b525-134">The **SslComputeFinishedHash** function is one of three functions used to generate a hash to use during the SSL handshake.</span></span>

1.  <span data-ttu-id="3b525-135">Viene chiamata la funzione [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) per ottenere un handle hash.</span><span class="sxs-lookup"><span data-stu-id="3b525-135">The [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) function is called to obtain a hash handle.</span></span>
2.  <span data-ttu-id="3b525-136">La funzione [**SslHashHandshake**](sslhashhandshake.md) viene chiamata un numero qualsiasi di volte con l'handle hash per aggiungere dati all'hash.</span><span class="sxs-lookup"><span data-stu-id="3b525-136">The [**SslHashHandshake**](sslhashhandshake.md) function is called any number of times with the hash handle to add data to the hash.</span></span>
3.  <span data-ttu-id="3b525-137">La funzione **SslComputeFinishedHash** viene chiamata con l'handle hash per ottenere il digest dei dati con hash.</span><span class="sxs-lookup"><span data-stu-id="3b525-137">The **SslComputeFinishedHash** function is called with the hash handle to obtain the digest of the hashed data.</span></span>

<span data-ttu-id="3b525-138">Il valore hash viene calcolato eseguendo l'hashing della master secret con un hash di tutti i messaggi di handshake precedenti inviati o ricevuti.</span><span class="sxs-lookup"><span data-stu-id="3b525-138">The hash value is computed by hashing the master secret with a hash of all previous handshake messages sent or received.</span></span>

<span data-ttu-id="3b525-139">Il valore di *cbOutput* determina la lunghezza dei dati hash.</span><span class="sxs-lookup"><span data-stu-id="3b525-139">The value of *cbOutput* determines the length of the hash data.</span></span> <span data-ttu-id="3b525-140">Quando si usa il protocollo TLS ( [*Transport Layer Security Protocol*](/windows/desktop/SecGloss/t-gly) ) 1,0, deve essere sempre 12 (byte).</span><span class="sxs-lookup"><span data-stu-id="3b525-140">When the [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) 1.0 protocol is used, this should always be 12 (bytes).</span></span> <span data-ttu-id="3b525-141">Per ulteriori informazioni, vedere [la versione 1,0 del protocollo TLS](https://www.ietf.org/rfc/rfc2246.txt).</span><span class="sxs-lookup"><span data-stu-id="3b525-141">For more information, see [The TLS Protocol Version 1.0](https://www.ietf.org/rfc/rfc2246.txt).</span></span>

## <a name="requirements"></a><span data-ttu-id="3b525-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b525-142">Requirements</span></span>



| <span data-ttu-id="3b525-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b525-143">Requirement</span></span> | <span data-ttu-id="3b525-144">Valore</span><span class="sxs-lookup"><span data-stu-id="3b525-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b525-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b525-145">Minimum supported client</span></span><br/> | <span data-ttu-id="3b525-146">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3b525-146">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3b525-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b525-147">Minimum supported server</span></span><br/> | <span data-ttu-id="3b525-148">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3b525-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3b525-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3b525-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b525-150"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b525-150"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="3b525-151">DLL</span><span class="sxs-lookup"><span data-stu-id="3b525-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b525-152"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b525-152"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 


---
description: Calcola un hash da utilizzare durante l'autenticazione del certificato.
ms.assetid: f4a12464-8ad6-4bf9-8b6e-49bdf5332b66
title: Funzione SslComputeClientAuthHash (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeClientAuthHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: faea1699657efd92049068e48ff361c48242e9c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227049"
---
# <a name="sslcomputeclientauthhash-function"></a><span data-ttu-id="0b8cb-103">SslComputeClientAuthHash (funzione)</span><span class="sxs-lookup"><span data-stu-id="0b8cb-103">SslComputeClientAuthHash function</span></span>

<span data-ttu-id="0b8cb-104">La funzione **SslComputeClientAuthHash** calcola un [*hash*](/windows/desktop/SecGloss/h-gly) da usare durante l'autenticazione del [*certificato*](/windows/desktop/SecGloss/c-gly) .</span><span class="sxs-lookup"><span data-stu-id="0b8cb-104">The **SslComputeClientAuthHash** function computes a [*hash*](/windows/desktop/SecGloss/h-gly) to use during [*certificate*](/windows/desktop/SecGloss/c-gly) authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b8cb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b8cb-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslComputeClientAuthHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _In_  NCRYPT_HASH_HANDLE hHandshakeHash,
  _In_  LPCWSTR            pszAlgId,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _Out_ DWORD              *pcbResult,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="0b8cb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0b8cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b8cb-107">*hSslProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b8cb-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b8cb-108">Handle dell'istanza del provider di protocollo SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="0b8cb-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="0b8cb-109">*hMasterKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b8cb-109">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b8cb-110">Handle dell'oggetto [*chiave master*](/windows/desktop/SecGloss/m-gly) .</span><span class="sxs-lookup"><span data-stu-id="0b8cb-110">The handle of the [*master key*](/windows/desktop/SecGloss/m-gly) object.</span></span>

</dd> <dt>

<span data-ttu-id="0b8cb-111">*hHandshakeHash* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b8cb-111">*hHandshakeHash* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b8cb-112">Handle dell'hash dell'handshake calcolato fino a questo momento.</span><span class="sxs-lookup"><span data-stu-id="0b8cb-112">The handle of the hash of the handshake computed so far.</span></span>

</dd> <dt>

<span data-ttu-id="0b8cb-113">*pszAlgId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b8cb-113">*pszAlgId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b8cb-114">Puntatore a una stringa Unicode con terminazione null che identifica l' [*algoritmo di crittografia*](/windows/desktop/SecGloss/c-gly)richiesto.</span><span class="sxs-lookup"><span data-stu-id="0b8cb-114">A pointer to a null-terminated Unicode string that identifies the requested [*cryptographic algorithm*](/windows/desktop/SecGloss/c-gly).</span></span> <span data-ttu-id="0b8cb-115">Può trattarsi di uno degli [**identificatori dell'algoritmo CNG**](cng-algorithm-identifiers.md) standard o dell'identificatore di un altro algoritmo registrato.</span><span class="sxs-lookup"><span data-stu-id="0b8cb-115">This can be one of the standard [**CNG Algorithm Identifiers**](cng-algorithm-identifiers.md) or the identifier for another registered algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="0b8cb-116">*pbOutput* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0b8cb-116">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b8cb-117">Indirizzo di un buffer che riceve il [*BLOB della chiave*](/windows/desktop/SecGloss/k-gly).</span><span class="sxs-lookup"><span data-stu-id="0b8cb-117">The address of a buffer that receives the [*key BLOB*](/windows/desktop/SecGloss/k-gly).</span></span> <span data-ttu-id="0b8cb-118">Il parametro *cbOutput* contiene la dimensione del buffer.</span><span class="sxs-lookup"><span data-stu-id="0b8cb-118">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="0b8cb-119">Se questo parametro è **null**, questa funzione inserisce la dimensione richiesta, in byte, nel **valore DWORD** a cui fa riferimento il parametro *pcbResult* .</span><span class="sxs-lookup"><span data-stu-id="0b8cb-119">If this parameter is **NULL**, this function will place the required size, in bytes, in the **DWORD** pointed to by the *pcbResult* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0b8cb-120">*cbOutput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b8cb-120">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b8cb-121">Lunghezza, in byte, del buffer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="0b8cb-121">The length, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0b8cb-122">*pcbResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0b8cb-122">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b8cb-123">Puntatore a un valore **DWORD** che specifica la lunghezza, in byte, dell'hash scritto nel buffer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="0b8cb-123">A pointer to a **DWORD** value that specifies the length, in bytes, of the hash written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0b8cb-124">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b8cb-124">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b8cb-125">Questo parametro è riservato per usi futuri.</span><span class="sxs-lookup"><span data-stu-id="0b8cb-125">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b8cb-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0b8cb-126">Return value</span></span>

<span data-ttu-id="0b8cb-127">Se la funzione ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="0b8cb-127">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="0b8cb-128">Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="0b8cb-128">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="0b8cb-129">I codici restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="0b8cb-129">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="0b8cb-130">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="0b8cb-130">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="0b8cb-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b8cb-131">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="0b8cb-132"><dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="0b8cb-132"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="0b8cb-133">Uno degli handle forniti non è valido.</span><span class="sxs-lookup"><span data-stu-id="0b8cb-133">One of the supplied handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0b8cb-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b8cb-134">Remarks</span></span>

<span data-ttu-id="0b8cb-135">La funzione **SslComputeClientAuthHash** calcola l'hash che viene inviato nel messaggio di verifica del certificato dell'handshake SSL.</span><span class="sxs-lookup"><span data-stu-id="0b8cb-135">The **SslComputeClientAuthHash** function computes the hash that is sent in the certificate verification message of the SSL handshake.</span></span> <span data-ttu-id="0b8cb-136">Il valore hash viene calcolato creando un hash che contiene il master secret con un hash di tutti i messaggi di handshake precedenti inviati o ricevuti.</span><span class="sxs-lookup"><span data-stu-id="0b8cb-136">The hash value is computed by creating a hash that contains the master secret with a hash of all previous handshake messages sent or received.</span></span> <span data-ttu-id="0b8cb-137">Per ulteriori informazioni sulla sequenza di handshake SSL, vedere [la descrizione dell'handshake Secure Sockets Layer (SSL)](https://support.microsoft.com/kb/257591).</span><span class="sxs-lookup"><span data-stu-id="0b8cb-137">For more information about the SSL handshake sequence, see [Description of the Secure Sockets Layer (SSL) Handshake](https://support.microsoft.com/kb/257591).</span></span>

<span data-ttu-id="0b8cb-138">Il modo in cui viene calcolato l'hash dipende dal protocollo e dal pacchetto di crittografia utilizzati.</span><span class="sxs-lookup"><span data-stu-id="0b8cb-138">The manner in which the hash is computed depends on the protocol and cipher suite used.</span></span> <span data-ttu-id="0b8cb-139">Inoltre, l'hash dipende dal tipo di chiave di autenticazione client utilizzata; il parametro *pszAlgId* indica il tipo di chiave utilizzata per l'autenticazione client.</span><span class="sxs-lookup"><span data-stu-id="0b8cb-139">In addition, the hash depends on the type of client authentication key used; the *pszAlgId* parameter indicates the type of key used for client authentication.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b8cb-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b8cb-140">Requirements</span></span>



| <span data-ttu-id="0b8cb-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b8cb-141">Requirement</span></span> | <span data-ttu-id="0b8cb-142">Valore</span><span class="sxs-lookup"><span data-stu-id="0b8cb-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b8cb-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b8cb-143">Minimum supported client</span></span><br/> | <span data-ttu-id="0b8cb-144">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0b8cb-144">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0b8cb-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b8cb-145">Minimum supported server</span></span><br/> | <span data-ttu-id="0b8cb-146">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0b8cb-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0b8cb-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0b8cb-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b8cb-148"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b8cb-148"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="0b8cb-149">DLL</span><span class="sxs-lookup"><span data-stu-id="0b8cb-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b8cb-150"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b8cb-150"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 


---
description: Firma un hash usando la chiave privata specificata.
ms.assetid: 25e8ebc5-278d-4d1f-977a-c2fab07b790a
title: Funzione SslSignHash (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslSignHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 339d0a27cb987557ff90cbd0f489813edb357b77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484628"
---
# <a name="sslsignhash-function"></a><span data-ttu-id="5b60f-103">SslSignHash (funzione)</span><span class="sxs-lookup"><span data-stu-id="5b60f-103">SslSignHash function</span></span>

<span data-ttu-id="5b60f-104">La funzione **SslSignHash** firma un [*hash*](/windows/desktop/SecGloss/h-gly) usando la [*chiave privata*](/windows/desktop/SecGloss/p-gly)specificata.</span><span class="sxs-lookup"><span data-stu-id="5b60f-104">The **SslSignHash** function signs a [*hash*](/windows/desktop/SecGloss/h-gly) by using the specified [*private key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="5b60f-105">Il processo di firma viene eseguito sul server.</span><span class="sxs-lookup"><span data-stu-id="5b60f-105">The signing process is performed on the server.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b60f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5b60f-106">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslSignHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _In_  PBYTE              pbHashValue,
  _In_  DWORD              cbHashValue,
  _Out_ PBYTE              pbSignature,
  _In_  DWORD              cbSignature,
  _Out_ DWORD              *pcbResult,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="5b60f-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5b60f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b60f-108">*hSslProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b60f-108">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b60f-109">Handle per l'istanza del provider di protocollo SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="5b60f-109">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="5b60f-110">*hPrivateKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b60f-110">*hPrivateKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b60f-111">Handle per la chiave privata da utilizzare per firmare l'hash.</span><span class="sxs-lookup"><span data-stu-id="5b60f-111">The handle to the private key to use to sign the hash.</span></span>

</dd> <dt>

<span data-ttu-id="5b60f-112">*pbHashValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b60f-112">*pbHashValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b60f-113">Puntatore a un buffer contenente l'hash da firmare.</span><span class="sxs-lookup"><span data-stu-id="5b60f-113">A pointer to a buffer that contains the hash to sign.</span></span>

</dd> <dt>

<span data-ttu-id="5b60f-114">*cbHashValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b60f-114">*cbHashValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b60f-115">Dimensione, in byte, del buffer *pbHashValue* .</span><span class="sxs-lookup"><span data-stu-id="5b60f-115">The size, in bytes, of the *pbHashValue* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5b60f-116">*pbSignature* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5b60f-116">*pbSignature* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b60f-117">Indirizzo di un buffer che riceve la firma dell'hash.</span><span class="sxs-lookup"><span data-stu-id="5b60f-117">The address of a buffer that receives the signature of the hash.</span></span> <span data-ttu-id="5b60f-118">Il parametro *cbSignature* contiene la dimensione del buffer.</span><span class="sxs-lookup"><span data-stu-id="5b60f-118">The *cbSignature* parameter contains the size of this buffer.</span></span> <span data-ttu-id="5b60f-119">Per determinare le dimensioni di dimensioni richieste del buffer, impostare il parametro *pbSignature* su **null**.</span><span class="sxs-lookup"><span data-stu-id="5b60f-119">To determine the required sized size of the buffer, set the *pbSignature* parameter to **NULL**.</span></span> <span data-ttu-id="5b60f-120">La dimensione richiesta del buffer verrà restituita nel parametro *pcbResult* .</span><span class="sxs-lookup"><span data-stu-id="5b60f-120">The required size of the buffer will be returned in the *pcbResult* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5b60f-121">*cbSignature* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b60f-121">*cbSignature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b60f-122">Dimensione, in byte, del buffer *pbSignature* .</span><span class="sxs-lookup"><span data-stu-id="5b60f-122">The size, in bytes, of the *pbSignature* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5b60f-123">*pcbResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5b60f-123">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b60f-124">Puntatore a un valore che, al termine, contiene il numero effettivo di byte scritti nel buffer *pbSignature* .</span><span class="sxs-lookup"><span data-stu-id="5b60f-124">A pointer to a value that, upon completion, contains the actual number of bytes written to the *pbSignature* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5b60f-125">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b60f-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b60f-126">Questo parametro è riservato per usi futuri.</span><span class="sxs-lookup"><span data-stu-id="5b60f-126">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b60f-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5b60f-127">Return value</span></span>

<span data-ttu-id="5b60f-128">Se la funzione ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="5b60f-128">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="5b60f-129">Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="5b60f-129">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="5b60f-130">I codici restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="5b60f-130">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="5b60f-131">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="5b60f-131">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="5b60f-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b60f-132">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="5b60f-133"><dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="5b60f-133"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="5b60f-134">Uno degli handle forniti non è valido.</span><span class="sxs-lookup"><span data-stu-id="5b60f-134">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5b60f-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b60f-135">Requirements</span></span>



| <span data-ttu-id="5b60f-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b60f-136">Requirement</span></span> | <span data-ttu-id="5b60f-137">Valore</span><span class="sxs-lookup"><span data-stu-id="5b60f-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b60f-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b60f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="5b60f-139">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5b60f-139">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5b60f-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b60f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="5b60f-141">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5b60f-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5b60f-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5b60f-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b60f-143"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b60f-143"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="5b60f-144">DLL</span><span class="sxs-lookup"><span data-stu-id="5b60f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b60f-145"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b60f-145"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 


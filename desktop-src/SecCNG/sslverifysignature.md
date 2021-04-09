---
description: Verifica la firma specificata usando l'hash fornito e la chiave pubblica.
ms.assetid: fa274851-15f2-4be0-9e2f-4cdced36daff
title: Funzione SslVerifySignature (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslVerifySignature
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: cb2a50a7f16062f271a89b6061e3f2fa2dd16685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878966"
---
# <a name="sslverifysignature-function"></a><span data-ttu-id="3a5de-103">SslVerifySignature (funzione)</span><span class="sxs-lookup"><span data-stu-id="3a5de-103">SslVerifySignature function</span></span>

<span data-ttu-id="3a5de-104">La funzione **SslVerifySignature** verifica la firma specificata usando l' [*hash*](/windows/desktop/SecGloss/h-gly) fornito e la [*chiave pubblica*](/windows/desktop/SecGloss/p-gly).</span><span class="sxs-lookup"><span data-stu-id="3a5de-104">The **SslVerifySignature** function verifies the specified signature by using the supplied [*hash*](/windows/desktop/SecGloss/h-gly) and the [*public key*](/windows/desktop/SecGloss/p-gly).</span></span>

## <a name="syntax"></a><span data-ttu-id="3a5de-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3a5de-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslVerifySignature(
  _In_ NCRYPT_PROV_HANDLE hSslProvider,
  _In_ NCRYPT_KEY_HANDLE  hPublicKey,
  _In_ PBYTE              pbHashValue,
  _In_ DWORD              cbHashValue,
  _In_ PBYTE              pbSignature,
  _In_ DWORD              cbSignature,
  _In_ DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="3a5de-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3a5de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a5de-107">*hSslProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a5de-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a5de-108">Handle per l'istanza del provider di protocollo SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="3a5de-108">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="3a5de-109">*hPublicKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a5de-109">*hPublicKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a5de-110">Handle per la chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="3a5de-110">The handle to the public key.</span></span>

</dd> <dt>

<span data-ttu-id="3a5de-111">*pbHashValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a5de-111">*pbHashValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a5de-112">Puntatore a un buffer contenente l'hash da usare per verificare la firma.</span><span class="sxs-lookup"><span data-stu-id="3a5de-112">A pointer to a buffer that contains the hash to use to verify the signature.</span></span>

</dd> <dt>

<span data-ttu-id="3a5de-113">*cbHashValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a5de-113">*cbHashValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a5de-114">Dimensione, in byte, del buffer *pbHashValue* .</span><span class="sxs-lookup"><span data-stu-id="3a5de-114">The size, in bytes, of the *pbHashValue* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3a5de-115">*pbSignature* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a5de-115">*pbSignature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a5de-116">Puntatore a un buffer contenente la firma da verificare.</span><span class="sxs-lookup"><span data-stu-id="3a5de-116">A pointer to a buffer that contains the signature to verify.</span></span>

</dd> <dt>

<span data-ttu-id="3a5de-117">*cbSignature* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a5de-117">*cbSignature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a5de-118">Dimensione, in byte, del buffer *pbSignature* .</span><span class="sxs-lookup"><span data-stu-id="3a5de-118">The size, in bytes, of the *pbSignature* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3a5de-119">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3a5de-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a5de-120">Questo parametro è riservato per usi futuri.</span><span class="sxs-lookup"><span data-stu-id="3a5de-120">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a5de-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3a5de-121">Return value</span></span>

<span data-ttu-id="3a5de-122">Se la funzione ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="3a5de-122">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="3a5de-123">Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="3a5de-123">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="3a5de-124">I codici restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="3a5de-124">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="3a5de-125">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="3a5de-125">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="3a5de-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3a5de-126">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="3a5de-127"><dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3a5de-127"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="3a5de-128">Uno degli handle forniti non è valido.</span><span class="sxs-lookup"><span data-stu-id="3a5de-128">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3a5de-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="3a5de-129">Remarks</span></span>

<span data-ttu-id="3a5de-130">La funzione **SslVerifySignature** non è attualmente chiamata da Windows.</span><span class="sxs-lookup"><span data-stu-id="3a5de-130">The **SslVerifySignature** function is not currently called by Windows.</span></span> <span data-ttu-id="3a5de-131">Questa funzione è una parte obbligatoria dell'interfaccia del provider SSL e deve essere implementata completamente per garantire la compatibilità con le edizioni.</span><span class="sxs-lookup"><span data-stu-id="3a5de-131">This function is a required part of the SSL Provider interface and should be fully implemented to ensure forward compatibility.</span></span>

<span data-ttu-id="3a5de-132">Le implementazioni correnti del lato server della connessione TLS ( [*Transport Layer Security Protocol*](/windows/desktop/SecGloss/t-gly) ) chiamano la funzione [**NCryptVerifySignature**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) durante l'autenticazione del client per elaborare il messaggio di verifica del certificato.</span><span class="sxs-lookup"><span data-stu-id="3a5de-132">Current implementations of the server side of the [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) connection call the [**NCryptVerifySignature**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) function during the client authentication to process the certificate verify message.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a5de-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3a5de-133">Requirements</span></span>



| <span data-ttu-id="3a5de-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a5de-134">Requirement</span></span> | <span data-ttu-id="3a5de-135">Valore</span><span class="sxs-lookup"><span data-stu-id="3a5de-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a5de-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a5de-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3a5de-137">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3a5de-137">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3a5de-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3a5de-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3a5de-139">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3a5de-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3a5de-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3a5de-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a5de-141"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a5de-141"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="3a5de-142">DLL</span><span class="sxs-lookup"><span data-stu-id="3a5de-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a5de-143"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a5de-143"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 


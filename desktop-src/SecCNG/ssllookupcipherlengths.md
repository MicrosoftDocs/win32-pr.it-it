---
description: Restituisce una \_ \_ \_ struttura di lunghezze di crittografia SSL NCRYPT che contiene le lunghezze dell'intestazione e del trailer del protocollo di input, del pacchetto di crittografia e del tipo di chiave.
ms.assetid: 44d0d803-16d7-4bdf-9638-afbdaf9e1802
title: Funzione SslLookupCipherLengths (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslLookupCipherLengths
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e756fb84d47ed877ffe4afcd54ce93c53a768e69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967133"
---
# <a name="ssllookupcipherlengths-function"></a><span data-ttu-id="c8040-103">SslLookupCipherLengths (funzione)</span><span class="sxs-lookup"><span data-stu-id="c8040-103">SslLookupCipherLengths function</span></span>

<span data-ttu-id="c8040-104">La funzione **SslLookupCipherLengths** restituisce una struttura di [**\_ \_ \_ lunghezza di crittografia SSL NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) che contiene le lunghezze dell'intestazione e del trailer del protocollo di input, del pacchetto di crittografia e del tipo di chiave.</span><span class="sxs-lookup"><span data-stu-id="c8040-104">The **SslLookupCipherLengths** function returns an [**NCRYPT\_SSL\_CIPHER\_LENGTHS**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) structure that contains the header and trailer lengths of the input protocol, cipher suite, and key type.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8040-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c8040-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslLookupCipherLengths(
  _In_  NCRYPT_PROV_HANDLE        hSslProvider,
  _In_  DWORD                     dwProtocol,
  _In_  DWORD                     dwCipherSuite,
  _In_  DWORD                     dwKeyType,
  _Out_ NCRYPT_SSL_CIPHER_LENGTHS *pCipherLengths,
  _In_  DWORD                     cbCipherLengths,
  _In_  DWORD                     dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="c8040-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c8040-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8040-107">*hSslProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8040-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8040-108">Handle dell'istanza del provider di protocollo SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="c8040-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="c8040-109">*dwProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8040-109">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8040-110">Uno dei valori dell' [**identificatore del protocollo del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="c8040-110">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="c8040-111">*dwCipherSuite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8040-111">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8040-112">Uno dei valori dell' [**identificatore del pacchetto di crittografia del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="c8040-112">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="c8040-113">*dwKeyType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8040-113">*dwKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8040-114">Uno dei valori dell' [**identificatore del tipo di chiave del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="c8040-114">One of the [**CNG SSL Provider Key Type Identifier**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) values.</span></span> <span data-ttu-id="c8040-115">Per i tipi di chiave che non sono la [*crittografia a curva ellittica*](/windows/desktop/SecGloss/e-gly) (ecc), impostare questo parametro su zero.</span><span class="sxs-lookup"><span data-stu-id="c8040-115">For key types that are not [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC), set this parameter to zero.</span></span>

</dd> <dt>

<span data-ttu-id="c8040-116">*pCipherLengths* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c8040-116">*pCipherLengths* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8040-117">Puntatore a un buffer per ricevere la struttura [**delle \_ \_ \_ lunghezze di crittografia SSL NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) .</span><span class="sxs-lookup"><span data-stu-id="c8040-117">A pointer to a buffer to receive the [**NCRYPT\_SSL\_CIPHER\_LENGTHS**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) structure.</span></span>

</dd> <dt>

<span data-ttu-id="c8040-118">*cbCipherLengths* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8040-118">*cbCipherLengths* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8040-119">Lunghezza, in byte, del buffer a cui punta il parametro *pCipherLengths* .</span><span class="sxs-lookup"><span data-stu-id="c8040-119">The length, in bytes, of the buffer pointed to by the *pCipherLengths* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c8040-120">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8040-120">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8040-121">Questo parametro è riservato per utilizzi futuri e deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="c8040-121">This parameter is reserved for future use and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8040-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c8040-122">Return value</span></span>

<span data-ttu-id="c8040-123">Se la funzione ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="c8040-123">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="c8040-124">Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="c8040-124">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="c8040-125">I codici restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="c8040-125">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="c8040-126">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="c8040-126">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="c8040-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8040-127">Description</span></span>                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c8040-128"><dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c8040-128"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="c8040-129">Il parametro *hSslProvider* contiene un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="c8040-129">The *hSslProvider* parameter contains a pointer that is not valid.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="c8040-130"><dt>**Nte \_ \_Parametro 0X80090027L non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c8040-130"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="c8040-131">Il parametro *pCipherLengths* è impostato su **null** o la lunghezza del buffer specificata da *cbCipherLengths* è troppo corta.</span><span class="sxs-lookup"><span data-stu-id="c8040-131">The *pCipherLengths* parameter is set to **NULL** or the buffer length specified by the *cbCipherLengths* is too short.</span></span><br/> |
| <dl> <span data-ttu-id="c8040-132"><dt>**Nte \_ \_Flag non validi**</dt> <dt>0x80090009L</dt></span><span class="sxs-lookup"><span data-stu-id="c8040-132"><dt>**NTE\_BAD\_FLAGS**</dt> <dt>0x80090009L</dt></span></span> </dl>         | <span data-ttu-id="c8040-133">Il parametro *dwFlags* deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="c8040-133">The *dwFlags* parameter must be set to zero.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="c8040-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="c8040-134">Remarks</span></span>

<span data-ttu-id="c8040-135">La funzione **SslLookupCipherLengths** viene chiamata per le conversazioni [*Transport Layer Security Protocol*](/windows/desktop/SecGloss/t-gly) (TLS) 1,1 o versioni successive per eseguire una query sulle lunghezze dell'intestazione e del trailer per il protocollo richiesto, il pacchetto di crittografia e il tipo di chiave.</span><span class="sxs-lookup"><span data-stu-id="c8040-135">The **SslLookupCipherLengths** function is called for [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) 1.1 or later conversations to query the header and trailer lengths for the requested protocol, cipher suite, and key type.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8040-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8040-136">Requirements</span></span>



| <span data-ttu-id="c8040-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8040-137">Requirement</span></span> | <span data-ttu-id="c8040-138">Valore</span><span class="sxs-lookup"><span data-stu-id="c8040-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8040-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8040-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c8040-140">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c8040-140">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c8040-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8040-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c8040-142">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c8040-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c8040-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c8040-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8040-144"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8040-144"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="c8040-145">DLL</span><span class="sxs-lookup"><span data-stu-id="c8040-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8040-146"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8040-146"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 


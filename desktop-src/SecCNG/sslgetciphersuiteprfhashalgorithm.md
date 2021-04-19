---
description: "Restituisce l'identificatore dell'algoritmo CNG (Cryptography API: Next Generation) dell'algoritmo hash utilizzato per Transport Layer Security la funzione pseudo-casuale (PRF) del protocollo di crittografia per il protocollo di input, il pacchetto di crittografia e il tipo di chiave."
ms.assetid: 8d20b2da-390e-458e-b122-f5ef3722ad87
title: Funzione SslGetCipherSuitePRFHashAlgorithm (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetCipherSuitePRFHashAlgorithm
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 452cb7b36b20697a95b2c2abae7d8cd3b4180050
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319911"
---
# <a name="sslgetciphersuiteprfhashalgorithm-function"></a><span data-ttu-id="fbf35-103">SslGetCipherSuitePRFHashAlgorithm (funzione)</span><span class="sxs-lookup"><span data-stu-id="fbf35-103">SslGetCipherSuitePRFHashAlgorithm function</span></span>

<span data-ttu-id="fbf35-104">La funzione **SslGetCipherSuitePRFHashAlgorithm** restituisce l'identificatore dell'algoritmo CNG (Cryptography API: Next Generation) dell' [*algoritmo di hash*](/windows/desktop/SecGloss/h-gly) utilizzato per Transport Layer Security la [*funzione pseudo-casuale*](/windows/desktop/SecGloss/p-gly) (PRF) del [*protocollo*](/windows/desktop/SecGloss/t-gly) di input (PRF) per il protocollo di input, il pacchetto di crittografia e il tipo di chiave.</span><span class="sxs-lookup"><span data-stu-id="fbf35-104">The **SslGetCipherSuitePRFHashAlgorithm** function returns the Cryptography API: Next Generation (CNG) Algorithm Identifier of the [*hashing algorithm*](/windows/desktop/SecGloss/h-gly) that is used for the [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) [*pseudo-random function*](/windows/desktop/SecGloss/p-gly) (PRF) for the input protocol, cipher suite, and key type.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbf35-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fbf35-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGetCipherSuitePRFHashAlgorithm(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwKeyType,
  _Out_ WCHAR              szPRFHash[NCRYPT_SSL_MAX_NAME_SIZE],
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="fbf35-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fbf35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbf35-107">*hSslProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fbf35-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbf35-108">Handle dell'istanza del provider di protocollo SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="fbf35-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="fbf35-109">*dwProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fbf35-109">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbf35-110">Uno dei valori dell' [**identificatore del protocollo del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="fbf35-110">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="fbf35-111">*dwCipherSuite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fbf35-111">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbf35-112">Uno dei valori dell' [**identificatore del pacchetto di crittografia del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="fbf35-112">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="fbf35-113">*dwKeyType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fbf35-113">*dwKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbf35-114">Uno dei valori dell' [**identificatore del tipo di chiave del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="fbf35-114">One of the [**CNG SSL Provider Key Type Identifier**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) values.</span></span> <span data-ttu-id="fbf35-115">Per i tipi di chiave che non sono la [*crittografia a curva ellittica*](/windows/desktop/SecGloss/e-gly) (ecc), impostare questo parametro su zero.</span><span class="sxs-lookup"><span data-stu-id="fbf35-115">For key types that are not [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC), set this parameter to zero.</span></span>

</dd> <dt>

<span data-ttu-id="fbf35-116">*szPRFHash* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fbf35-116">*szPRFHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fbf35-117">Uno degli [**identificatori dell'algoritmo CNG**](cng-algorithm-identifiers.md) per l'hash che verrà usato per la PRF TLS.</span><span class="sxs-lookup"><span data-stu-id="fbf35-117">One of the [**CNG Algorithm Identifiers**](cng-algorithm-identifiers.md) for the hash that will be used for the TLS PRF.</span></span>

</dd> <dt>

<span data-ttu-id="fbf35-118">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fbf35-118">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbf35-119">Questo parametro è riservato per utilizzi futuri e deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="fbf35-119">This parameter is reserved for future use and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbf35-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fbf35-120">Return value</span></span>

<span data-ttu-id="fbf35-121">Se la funzione ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="fbf35-121">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="fbf35-122">Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="fbf35-122">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="fbf35-123">I codici restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="fbf35-123">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="fbf35-124">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="fbf35-124">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="fbf35-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fbf35-125">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fbf35-126"><dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fbf35-126"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="fbf35-127">Il parametro *hSslProvider* contiene un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="fbf35-127">The *hSslProvider* parameter contains a pointer that is not valid.</span></span><br/>                |
| <dl> <span data-ttu-id="fbf35-128"><dt>**Nte \_ \_Parametro 0X80090027L non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fbf35-128"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="fbf35-129">Il parametro *szPRFHash* è impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="fbf35-129">The *szPRFHash* parameter is set to **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="fbf35-130"><dt>**Nte \_ 0x80090029L non \_ supportato**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fbf35-130"><dt>**NTE\_NOT\_SUPPORTED**</dt> <dt>0x80090029L</dt></span></span> </dl>     | <span data-ttu-id="fbf35-131">La funzione selezionata non è supportata nella versione specificata dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="fbf35-131">The selected function is not supported in the specified version of the interface.</span></span><br/> |
| <dl> <span data-ttu-id="fbf35-132"><dt>**Nte \_ \_Flag non validi**</dt> <dt>0x80090009L</dt></span><span class="sxs-lookup"><span data-stu-id="fbf35-132"><dt>**NTE\_BAD\_FLAGS**</dt> <dt>0x80090009L</dt></span></span> </dl>         | <span data-ttu-id="fbf35-133">Il parametro *dwFlags* deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="fbf35-133">The *dwFlags* parameter must be set to zero.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="fbf35-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="fbf35-134">Remarks</span></span>

<span data-ttu-id="fbf35-135">Questa funzione **SslGetCipherSuitePRFHashAlgorithm** viene chiamata per le conversazioni TLS 1,2 o successive per eseguire una query sull'algoritmo di hash che verrà usato in TLS PRF.</span><span class="sxs-lookup"><span data-stu-id="fbf35-135">This **SslGetCipherSuitePRFHashAlgorithm** function is called for TLS 1.2 or later conversations to query the hashing algorithm that will be used in the TLS PRF.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbf35-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fbf35-136">Requirements</span></span>



| <span data-ttu-id="fbf35-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbf35-137">Requirement</span></span> | <span data-ttu-id="fbf35-138">Valore</span><span class="sxs-lookup"><span data-stu-id="fbf35-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbf35-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fbf35-139">Minimum supported client</span></span><br/> | <span data-ttu-id="fbf35-140">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="fbf35-140">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="fbf35-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fbf35-141">Minimum supported server</span></span><br/> | <span data-ttu-id="fbf35-142">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="fbf35-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fbf35-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fbf35-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="fbf35-144"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbf35-144"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="fbf35-145">DLL</span><span class="sxs-lookup"><span data-stu-id="fbf35-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbf35-146"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbf35-146"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 


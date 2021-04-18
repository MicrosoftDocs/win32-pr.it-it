---
description: Recupera un handle per l'hash di handshake utilizzato per l'autenticazione client.
ms.assetid: 55007ce0-4bf1-4605-9b34-2931935762aa
title: Funzione SslCreateClientAuthHash (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateClientAuthHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 4ac83d6d8aeea8429812d80b7bf66de7c87062a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310766"
---
# <a name="sslcreateclientauthhash-function"></a><span data-ttu-id="610a7-103">SslCreateClientAuthHash (funzione)</span><span class="sxs-lookup"><span data-stu-id="610a7-103">SslCreateClientAuthHash function</span></span>

<span data-ttu-id="610a7-104">La funzione **SslCreateClientAuthHash** recupera un handle per l' [*hash*](/windows/desktop/SecGloss/h-gly) di handshake usato per l'autenticazione client.</span><span class="sxs-lookup"><span data-stu-id="610a7-104">The **SslCreateClientAuthHash** function retrieves a handle to the handshake [*hash*](/windows/desktop/SecGloss/h-gly) that is used for client authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="610a7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="610a7-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslCreateClientAuthHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_HASH_HANDLE *phHandshakeHash,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  LPCWSTR            pszHashAlgId,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="610a7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="610a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="610a7-107">*hSslProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="610a7-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="610a7-108">Handle dell'istanza del provider di protocollo SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="610a7-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="610a7-109">*phHandshakeHash* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="610a7-109">*phHandshakeHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="610a7-110">Puntatore a una variabile **dell' \_ \_ handle di hash NCRYPT** per la ricezione dell'handle hash.</span><span class="sxs-lookup"><span data-stu-id="610a7-110">A pointer to an **NCRYPT\_HASH\_HANDLE** variable to receive the hash handle.</span></span>

</dd> <dt>

<span data-ttu-id="610a7-111">*dwProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="610a7-111">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="610a7-112">Uno dei valori dell' [**identificatore del protocollo del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="610a7-112">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="610a7-113">*dwCipherSuite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="610a7-113">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="610a7-114">Uno dei valori dell' [**identificatore del pacchetto di crittografia del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="610a7-114">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="610a7-115">*pszHashAlgId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="610a7-115">*pszHashAlgId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="610a7-116">Uno dei valori degli [**identificatori dell'algoritmo CNG**](cng-algorithm-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="610a7-116">One of the [**CNG Algorithm Identifiers**](cng-algorithm-identifiers.md) values.</span></span>

</dd> <dt>

<span data-ttu-id="610a7-117">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="610a7-117">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="610a7-118">Questo parametro è riservato per utilizzi futuri e deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="610a7-118">This parameter is reserved for future use and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="610a7-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="610a7-119">Return value</span></span>

<span data-ttu-id="610a7-120">Se la funzione ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="610a7-120">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="610a7-121">Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="610a7-121">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="610a7-122">I codici restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="610a7-122">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="610a7-123">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="610a7-123">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="610a7-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="610a7-124">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="610a7-125"><dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="610a7-125"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="610a7-126">Il parametro *hSslProvider* contiene un puntatore non valido.</span><span class="sxs-lookup"><span data-stu-id="610a7-126">The *hSslProvider* parameter contains a pointer that is not valid.</span></span><br/>                |
| <dl> <span data-ttu-id="610a7-127"><dt>**Nte \_ \_Parametro 0X80090027L non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="610a7-127"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="610a7-128">Il parametro *phHandshakeHash* è impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="610a7-128">The *phHandshakeHash* parameter is set to **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="610a7-129"><dt>**Nte \_ 0x80090029L non \_ supportato**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="610a7-129"><dt>**NTE\_NOT\_SUPPORTED**</dt> <dt>0x80090029L</dt></span></span> </dl>     | <span data-ttu-id="610a7-130">La funzione selezionata non è supportata nella versione specificata dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="610a7-130">The selected function is not supported in the specified version of the interface.</span></span><br/> |
| <dl> <span data-ttu-id="610a7-131"><dt>**Nte \_ Nessun \_**</dt> <dt>0x8009000EL</dt> di memoria</span><span class="sxs-lookup"><span data-stu-id="610a7-131"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="610a7-132">Memoria insufficiente per allocare i buffer.</span><span class="sxs-lookup"><span data-stu-id="610a7-132">Insufficient memory to allocate buffers.</span></span><br/>                                          |
| <dl> <span data-ttu-id="610a7-133"><dt>**Nte \_ \_Flag non validi**</dt> <dt>0x80090009L</dt></span><span class="sxs-lookup"><span data-stu-id="610a7-133"><dt>**NTE\_BAD\_FLAGS**</dt> <dt>0x80090009L</dt></span></span> </dl>         | <span data-ttu-id="610a7-134">Il parametro *dwFlags* deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="610a7-134">The *dwFlags* parameter must be set to zero.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="610a7-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="610a7-135">Remarks</span></span>

<span data-ttu-id="610a7-136">La funzione **SslCreateClientAuthHash** viene chiamata per le conversazioni [*Transport Layer Security Protocol*](/windows/desktop/SecGloss/t-gly) (TLS) 1,2 o versioni successive per creare oggetti hash utilizzati per i messaggi di handshake hash.</span><span class="sxs-lookup"><span data-stu-id="610a7-136">The **SslCreateClientAuthHash** function is called for [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) 1.2 or later conversations to create hash objects that are used to hash handshake messages.</span></span> <span data-ttu-id="610a7-137">Viene chiamato una volta per ogni possibile [*algoritmo di hashing*](/windows/desktop/SecGloss/h-gly) che può essere usato nella firma di autenticazione client.</span><span class="sxs-lookup"><span data-stu-id="610a7-137">It is called once for each possible [*hashing algorithm*](/windows/desktop/SecGloss/h-gly) that can be used in the client authentication signature.</span></span>

## <a name="requirements"></a><span data-ttu-id="610a7-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="610a7-138">Requirements</span></span>



| <span data-ttu-id="610a7-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="610a7-139">Requirement</span></span> | <span data-ttu-id="610a7-140">Valore</span><span class="sxs-lookup"><span data-stu-id="610a7-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="610a7-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="610a7-141">Minimum supported client</span></span><br/> | <span data-ttu-id="610a7-142">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="610a7-142">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="610a7-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="610a7-143">Minimum supported server</span></span><br/> | <span data-ttu-id="610a7-144">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="610a7-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="610a7-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="610a7-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="610a7-146"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="610a7-146"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="610a7-147">DLL</span><span class="sxs-lookup"><span data-stu-id="610a7-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="610a7-148"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="610a7-148"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 


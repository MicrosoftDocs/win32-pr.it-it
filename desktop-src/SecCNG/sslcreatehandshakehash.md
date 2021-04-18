---
description: Ottiene un handle hash utilizzato per l'hashing dei messaggi di handshake.
ms.assetid: 31390584-9d23-41d1-8604-b84a5e52ecde
title: Funzione SslCreateHandshakeHash (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateHandshakeHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8affda999278ce2d4a740293a7532643a6c564ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310764"
---
# <a name="sslcreatehandshakehash-function"></a><span data-ttu-id="00f41-103">SslCreateHandshakeHash (funzione)</span><span class="sxs-lookup"><span data-stu-id="00f41-103">SslCreateHandshakeHash function</span></span>

<span data-ttu-id="00f41-104">La funzione **SslCreateHandshakeHash** ottiene un handle hash utilizzato per l'hashing dei messaggi di handshake.</span><span class="sxs-lookup"><span data-stu-id="00f41-104">The **SslCreateHandshakeHash** function obtains a hash handle that is used to hash handshake messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="00f41-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00f41-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslCreateHandshakeHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_HASH_HANDLE *phHandshakeHash,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="00f41-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="00f41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00f41-107">*hSslProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00f41-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00f41-108">Handle dell'istanza del provider di protocollo SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="00f41-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="00f41-109">*phHandshakeHash* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="00f41-109">*phHandshakeHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00f41-110">Handle hash che può essere passato ad altre funzioni del provider SSL.</span><span class="sxs-lookup"><span data-stu-id="00f41-110">A hash handle that can be passed to other SSL provider functions.</span></span>

</dd> <dt>

<span data-ttu-id="00f41-111">*dwProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00f41-111">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00f41-112">Uno dei valori dell' [**identificatore del protocollo del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="00f41-112">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

> [!Note]  
> <span data-ttu-id="00f41-113">Questa funzione non viene utilizzata con il protocollo SSL 2,0.</span><span class="sxs-lookup"><span data-stu-id="00f41-113">This function is not used with the SSL 2.0 protocol.</span></span>

 

</dd> <dt>

<span data-ttu-id="00f41-114">*dwCipherSuite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00f41-114">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00f41-115">Uno dei valori dell' [**identificatore del pacchetto di crittografia del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="00f41-115">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="00f41-116">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00f41-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00f41-117">Questo parametro è riservato per usi futuri.</span><span class="sxs-lookup"><span data-stu-id="00f41-117">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00f41-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="00f41-118">Return value</span></span>

<span data-ttu-id="00f41-119">Se la funzione ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="00f41-119">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="00f41-120">Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="00f41-120">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="00f41-121">I codici restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="00f41-121">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="00f41-122">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="00f41-122">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="00f41-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00f41-123">Description</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="00f41-124"><dt>**Nte \_ Nessun \_**</dt> <dt>0x8009000EL</dt> di memoria</span><span class="sxs-lookup"><span data-stu-id="00f41-124"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="00f41-125">Memoria insufficiente per l'allocazione del buffer hash.</span><span class="sxs-lookup"><span data-stu-id="00f41-125">There is insufficient memory to allocate the hash buffer.</span></span><br/> |
| <dl> <span data-ttu-id="00f41-126"><dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="00f41-126"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="00f41-127">Handle *hSslProvider* non valido.</span><span class="sxs-lookup"><span data-stu-id="00f41-127">The *hSslProvider* handle is not valid.</span></span><br/>                   |
| <dl> <span data-ttu-id="00f41-128"><dt>**Nte \_ \_Parametro 0X80090027L non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="00f41-128"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="00f41-129">*PhHandshakeHash* è null.</span><span class="sxs-lookup"><span data-stu-id="00f41-129">The *phHandshakeHash* is null.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="00f41-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="00f41-130">Remarks</span></span>

<span data-ttu-id="00f41-131">La funzione **SslCreateHandshakeHash** è una delle tre funzioni usate per generare un hash da usare durante l'handshake SSL.</span><span class="sxs-lookup"><span data-stu-id="00f41-131">The **SslCreateHandshakeHash** function is one of three functions used to generate a hash to use during the SSL handshake.</span></span>

1.  <span data-ttu-id="00f41-132">Viene chiamata la funzione **SslCreateHandshakeHash** per ottenere un handle hash.</span><span class="sxs-lookup"><span data-stu-id="00f41-132">The **SslCreateHandshakeHash** function is called to obtain a hash handle.</span></span>
2.  <span data-ttu-id="00f41-133">La funzione [**SslHashHandshake**](sslhashhandshake.md) viene chiamata un numero qualsiasi di volte con l'handle hash per aggiungere dati all'hash.</span><span class="sxs-lookup"><span data-stu-id="00f41-133">The [**SslHashHandshake**](sslhashhandshake.md) function is called any number of times with the hash handle to add data to the hash.</span></span>
3.  <span data-ttu-id="00f41-134">La funzione [**SslComputeFinishedHash**](sslcomputefinishedhash.md) viene chiamata con l'handle hash per ottenere il digest dei dati con hash.</span><span class="sxs-lookup"><span data-stu-id="00f41-134">The [**SslComputeFinishedHash**](sslcomputefinishedhash.md) function is called with the hash handle to obtain the digest of the hashed data.</span></span>

## <a name="requirements"></a><span data-ttu-id="00f41-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00f41-135">Requirements</span></span>



| <span data-ttu-id="00f41-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="00f41-136">Requirement</span></span> | <span data-ttu-id="00f41-137">Valore</span><span class="sxs-lookup"><span data-stu-id="00f41-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="00f41-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00f41-138">Minimum supported client</span></span><br/> | <span data-ttu-id="00f41-139">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="00f41-139">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="00f41-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00f41-140">Minimum supported server</span></span><br/> | <span data-ttu-id="00f41-141">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="00f41-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="00f41-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="00f41-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="00f41-143"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="00f41-143"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="00f41-144">DLL</span><span class="sxs-lookup"><span data-stu-id="00f41-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00f41-145"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00f41-145"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 


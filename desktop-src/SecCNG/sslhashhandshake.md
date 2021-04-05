---
description: Restituisce un handle per l'hash di handshake.
ms.assetid: c0f20084-c863-42cf-afdf-298c5a96eed9
title: Funzione SslHashHandshake (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslHashHandshake
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 1dbfdbceb4242d389669a3eebf14260a3bb396fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968221"
---
# <a name="sslhashhandshake-function"></a><span data-ttu-id="5bd6f-103">SslHashHandshake (funzione)</span><span class="sxs-lookup"><span data-stu-id="5bd6f-103">SslHashHandshake function</span></span>

<span data-ttu-id="5bd6f-104">La funzione **SslHashHandshake** restituisce un handle per l'hash di handshake.</span><span class="sxs-lookup"><span data-stu-id="5bd6f-104">The **SslHashHandshake** function returns a handle to the handshake hash.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bd6f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5bd6f-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslHashHandshake(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_HASH_HANDLE hHandshakeHash,
  _Out_   PBYTE              pbInput,
  _In_    DWORD              cbInput,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="5bd6f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5bd6f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bd6f-107">*hSslProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5bd6f-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd6f-108">Handle per l'istanza del provider di protocollo SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="5bd6f-108">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="5bd6f-109">*hHandshakeHash* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="5bd6f-109">*hHandshakeHash* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd6f-110">Handle per l'oggetto hash.</span><span class="sxs-lookup"><span data-stu-id="5bd6f-110">The handle to the hash object.</span></span>

</dd> <dt>

<span data-ttu-id="5bd6f-111">*pbInput* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5bd6f-111">*pbInput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd6f-112">Indirizzo di un buffer che contiene i dati di cui eseguire l'hashing.</span><span class="sxs-lookup"><span data-stu-id="5bd6f-112">The address of a buffer that contains the data to be hashed.</span></span>

</dd> <dt>

<span data-ttu-id="5bd6f-113">*cbInput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5bd6f-113">*cbInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd6f-114">Dimensione, in byte, del buffer *pbInput* .</span><span class="sxs-lookup"><span data-stu-id="5bd6f-114">The size, in bytes, of the *pbInput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5bd6f-115">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5bd6f-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5bd6f-116">Questo parametro è riservato per usi futuri.</span><span class="sxs-lookup"><span data-stu-id="5bd6f-116">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bd6f-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5bd6f-117">Return value</span></span>

<span data-ttu-id="5bd6f-118">Se la funzione ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="5bd6f-118">If the function succeeds, it returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bd6f-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="5bd6f-119">Remarks</span></span>

<span data-ttu-id="5bd6f-120">La funzione **SslHashHandshake** è una delle tre funzioni usate per generare un hash da usare durante l'handshake SSL.</span><span class="sxs-lookup"><span data-stu-id="5bd6f-120">The **SslHashHandshake** function is one of three functions used to generate a hash to use during the SSL handshake.</span></span>

1.  <span data-ttu-id="5bd6f-121">Viene chiamata la funzione [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) per ottenere un handle hash.</span><span class="sxs-lookup"><span data-stu-id="5bd6f-121">The [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) function is called to obtain a hash handle.</span></span>
2.  <span data-ttu-id="5bd6f-122">La funzione **SslHashHandshake** viene chiamata un numero qualsiasi di volte con l'handle hash per aggiungere dati all'hash.</span><span class="sxs-lookup"><span data-stu-id="5bd6f-122">The **SslHashHandshake** function is called any number of times with the hash handle to add data to the hash.</span></span>
3.  <span data-ttu-id="5bd6f-123">La funzione [**SslComputeFinishedHash**](sslcomputefinishedhash.md) viene chiamata con l'handle hash per ottenere il digest dei dati con hash.</span><span class="sxs-lookup"><span data-stu-id="5bd6f-123">The [**SslComputeFinishedHash**](sslcomputefinishedhash.md) function is called with the hash handle to obtain the digest of the hashed data.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bd6f-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5bd6f-124">Requirements</span></span>



| <span data-ttu-id="5bd6f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bd6f-125">Requirement</span></span> | <span data-ttu-id="5bd6f-126">Valore</span><span class="sxs-lookup"><span data-stu-id="5bd6f-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bd6f-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5bd6f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5bd6f-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5bd6f-128">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5bd6f-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5bd6f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5bd6f-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5bd6f-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5bd6f-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5bd6f-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bd6f-132"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bd6f-132"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="5bd6f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5bd6f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5bd6f-134"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5bd6f-134"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 


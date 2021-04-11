---
description: Apre un handle per una chiave privata.
ms.assetid: 2406be2c-121c-4475-b193-d370a88641da
title: Funzione SslOpenPrivateKey (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslOpenPrivateKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 6fd5c10ce6385e377c72d21f4557d27d2345737d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128803"
---
# <a name="sslopenprivatekey-function"></a><span data-ttu-id="de3fb-103">SslOpenPrivateKey (funzione)</span><span class="sxs-lookup"><span data-stu-id="de3fb-103">SslOpenPrivateKey function</span></span>

<span data-ttu-id="de3fb-104">La funzione **SslOpenPrivateKey** apre un handle per una [*chiave privata*](/windows/desktop/SecGloss/p-gly).</span><span class="sxs-lookup"><span data-stu-id="de3fb-104">The **SslOpenPrivateKey** function opens a handle to a [*private key*](/windows/desktop/SecGloss/p-gly).</span></span>

## <a name="syntax"></a><span data-ttu-id="de3fb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="de3fb-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslOpenPrivateKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phPrivateKey,
  _In_  PCCERT_CONTEXT     pCertContext,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="de3fb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="de3fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de3fb-107">*hSslProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de3fb-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de3fb-108">Handle per l'istanza del provider di protocollo SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="de3fb-108">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="de3fb-109">*phPrivateKey* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="de3fb-109">*phPrivateKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de3fb-110">Indirizzo di un buffer in cui scrivere l'handle per la chiave privata.</span><span class="sxs-lookup"><span data-stu-id="de3fb-110">The address of a buffer in which to write the handle to the private key.</span></span>

<span data-ttu-id="de3fb-111">Al termine dell'uso della chiave, è necessario liberare *phPrivateKey* chiamando la funzione [**SslFreeObject**](sslfreeobject.md) .</span><span class="sxs-lookup"><span data-stu-id="de3fb-111">When you have finished using the key, you should free *phPrivateKey* by calling the [**SslFreeObject**](sslfreeobject.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="de3fb-112">*pCertContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de3fb-112">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de3fb-113">Indirizzo del certificato da cui ottenere la chiave privata.</span><span class="sxs-lookup"><span data-stu-id="de3fb-113">The address of the certificate from which to obtain the private key.</span></span>

</dd> <dt>

<span data-ttu-id="de3fb-114">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de3fb-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de3fb-115">Questo parametro è riservato per usi futuri.</span><span class="sxs-lookup"><span data-stu-id="de3fb-115">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de3fb-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="de3fb-116">Return value</span></span>

<span data-ttu-id="de3fb-117">Se la funzione ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="de3fb-117">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="de3fb-118">Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="de3fb-118">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="de3fb-119">I codici restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="de3fb-119">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="de3fb-120">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="de3fb-120">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="de3fb-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de3fb-121">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="de3fb-122"><dt>**Nte \_ Nessun \_**</dt> <dt>0x8009000EL</dt> di memoria</span><span class="sxs-lookup"><span data-stu-id="de3fb-122"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="de3fb-123">La memoria disponibile non è sufficiente per allocare i buffer necessari.</span><span class="sxs-lookup"><span data-stu-id="de3fb-123">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="de3fb-124"><dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="de3fb-124"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="de3fb-125">Handle *hSslProvider* non valido.</span><span class="sxs-lookup"><span data-stu-id="de3fb-125">The *hSslProvider* handle is not valid.</span></span><br/>                       |
| <dl> <span data-ttu-id="de3fb-126"><dt>**Nte \_ \_Parametro 0X80090027L non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="de3fb-126"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="de3fb-127">Il parametro *phPrivateKey* o *pCertContext* è **null**.</span><span class="sxs-lookup"><span data-stu-id="de3fb-127">The *phPrivateKey* or *pCertContext* parameter is **NULL**.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="de3fb-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="de3fb-128">Remarks</span></span>

<span data-ttu-id="de3fb-129">La chiave privata ottenuta è parte di una [*coppia di chiavi pubblica/privata*](/windows/desktop/SecGloss/p-gly) all'interno di un [*certificato*](/windows/desktop/SecGloss/c-gly).</span><span class="sxs-lookup"><span data-stu-id="de3fb-129">The private key obtained is part of a [*public/private key pair*](/windows/desktop/SecGloss/p-gly) within a [*certificate*](/windows/desktop/SecGloss/c-gly).</span></span> <span data-ttu-id="de3fb-130">Questa funzione estrae semplicemente la chiave privata dal certificato specificato dal parametro *pCertContext* .</span><span class="sxs-lookup"><span data-stu-id="de3fb-130">This function merely extracts the private key from the certificate specified by the *pCertContext* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="de3fb-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de3fb-131">Requirements</span></span>



| <span data-ttu-id="de3fb-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="de3fb-132">Requirement</span></span> | <span data-ttu-id="de3fb-133">Valore</span><span class="sxs-lookup"><span data-stu-id="de3fb-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="de3fb-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de3fb-134">Minimum supported client</span></span><br/> | <span data-ttu-id="de3fb-135">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="de3fb-135">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="de3fb-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de3fb-136">Minimum supported server</span></span><br/> | <span data-ttu-id="de3fb-137">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="de3fb-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="de3fb-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="de3fb-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="de3fb-139"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="de3fb-139"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="de3fb-140">DLL</span><span class="sxs-lookup"><span data-stu-id="de3fb-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de3fb-141"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de3fb-141"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 


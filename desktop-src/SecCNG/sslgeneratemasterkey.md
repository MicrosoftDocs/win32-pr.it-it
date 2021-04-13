---
description: Calcola la chiave di master secret SSL (Secure Sockets Layer Protocol).
ms.assetid: c9408eb3-711d-42c3-a4ba-e388689da34e
title: Funzione SslGenerateMasterKey (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGenerateMasterKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: ae8b357743cabf652721d3666c177990568718e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401802"
---
# <a name="sslgeneratemasterkey-function"></a><span data-ttu-id="8001a-103">SslGenerateMasterKey (funzione)</span><span class="sxs-lookup"><span data-stu-id="8001a-103">SslGenerateMasterKey function</span></span>

<span data-ttu-id="8001a-104">La funzione **SslGenerateMasterKey** calcola la chiave di master secret SSL ( [*Secure Sockets Layer Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="8001a-104">The **SslGenerateMasterKey** function computes the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) master secret key.</span></span>

## <a name="syntax"></a><span data-ttu-id="8001a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8001a-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGenerateMasterKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _In_  NCRYPT_KEY_HANDLE  hPublicKey,
  _Out_ NCRYPT_KEY_HANDLE  *phMasterKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  PNCryptBufferDesc  pParameterList,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _Out_ DWORD              *pcbResult,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="8001a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8001a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8001a-107">*hSslProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8001a-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8001a-108">Handle per l'istanza del provider del protocollo SSL.</span><span class="sxs-lookup"><span data-stu-id="8001a-108">The handle to the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="8001a-109">*hPrivateKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8001a-109">*hPrivateKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8001a-110">Handle per la [*chiave privata*](/windows/desktop/SecGloss/p-gly) utilizzata in Exchange.</span><span class="sxs-lookup"><span data-stu-id="8001a-110">The handle to the [*private key*](/windows/desktop/SecGloss/p-gly) used in the exchange.</span></span>

</dd> <dt>

<span data-ttu-id="8001a-111">*hPublicKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8001a-111">*hPublicKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8001a-112">Handle per la [*chiave pubblica*](/windows/desktop/SecGloss/p-gly) utilizzata in Exchange.</span><span class="sxs-lookup"><span data-stu-id="8001a-112">The handle to the [*public key*](/windows/desktop/SecGloss/p-gly) used in the exchange.</span></span>

</dd> <dt>

<span data-ttu-id="8001a-113">*phMasterKey* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8001a-113">*phMasterKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8001a-114">Puntatore all'handle per la [*chiave master*](/windows/desktop/SecGloss/m-gly)generata.</span><span class="sxs-lookup"><span data-stu-id="8001a-114">A pointer to the handle to the generated [*master key*](/windows/desktop/SecGloss/m-gly).</span></span>

</dd> <dt>

<span data-ttu-id="8001a-115">*dwProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8001a-115">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8001a-116">Uno dei valori dell' [**identificatore del protocollo del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="8001a-116">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="8001a-117">*dwCipherSuite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8001a-117">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8001a-118">Uno dei valori dell' [**identificatore del pacchetto di crittografia del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="8001a-118">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="8001a-119">*pParameterList* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8001a-119">*pParameterList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8001a-120">Puntatore a una matrice di buffer [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) che contengono informazioni utilizzate come parte dell'operazione di scambio delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="8001a-120">A pointer to an array of [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) buffers that contain information used as part of the key exchange operation.</span></span> <span data-ttu-id="8001a-121">Il set preciso di buffer dipende dal protocollo e dal pacchetto di crittografia utilizzati.</span><span class="sxs-lookup"><span data-stu-id="8001a-121">The precise set of buffers is dependent on the protocol and cipher suite that is used.</span></span> <span data-ttu-id="8001a-122">Come minimo, l'elenco conterrà i buffer contenenti i valori casuali specificati dal client e dal server.</span><span class="sxs-lookup"><span data-stu-id="8001a-122">At the minimum, the list will contain buffers that contain the client and server supplied random values.</span></span>

</dd> <dt>

<span data-ttu-id="8001a-123">*pbOutput* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8001a-123">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8001a-124">Indirizzo di un buffer che riceve il segreto premaster crittografato con la chiave pubblica del server.</span><span class="sxs-lookup"><span data-stu-id="8001a-124">The address of a buffer that receives the premaster secret encrypted with the public key of the server.</span></span> <span data-ttu-id="8001a-125">Il parametro *cbOutput* contiene la dimensione del buffer.</span><span class="sxs-lookup"><span data-stu-id="8001a-125">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="8001a-126">Se questo parametro è **null**, questa funzione restituisce la dimensione richiesta, in byte, nel **valore DWORD** a cui punta il parametro *pcbResult* .</span><span class="sxs-lookup"><span data-stu-id="8001a-126">If this parameter is **NULL**, this function returns the required size, in bytes, in the **DWORD** pointed to by the *pcbResult* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="8001a-127">Questo buffer viene usato quando si esegue uno scambio di chiavi RSA.</span><span class="sxs-lookup"><span data-stu-id="8001a-127">This buffer is used when performing a RSA key exchange.</span></span>

 

</dd> <dt>

<span data-ttu-id="8001a-128">*cbOutput* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8001a-128">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8001a-129">Dimensione, in byte, del buffer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="8001a-129">The size, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="8001a-130">*pcbResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8001a-130">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8001a-131">Puntatore a un valore **DWORD** in cui inserire il numero di byte scritti nel buffer *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="8001a-131">A pointer to a **DWORD** value in which to place number of bytes written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="8001a-132">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8001a-132">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8001a-133">Specifica se questa funzione viene utilizzata per lo scambio di chiavi sul lato client o sul lato server.</span><span class="sxs-lookup"><span data-stu-id="8001a-133">Specifies whether this function is being used for client-side or server-side key exchange.</span></span>



| <span data-ttu-id="8001a-134">Valore</span><span class="sxs-lookup"><span data-stu-id="8001a-134">Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="8001a-135">Significato</span><span class="sxs-lookup"><span data-stu-id="8001a-135">Meaning</span></span>                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <span data-ttu-id="8001a-136"><dt>**NCRYPT \_ \_ \_ Flag client SSL**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="8001a-136"><dt>**NCRYPT\_SSL\_CLIENT\_FLAG**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="8001a-137">Specifica uno scambio di chiavi sul lato client.</span><span class="sxs-lookup"><span data-stu-id="8001a-137">Specifies a client-side key exchange.</span></span><br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <span data-ttu-id="8001a-138"><dt>**NCRYPT \_ \_ \_ Flag server SSL**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="8001a-138"><dt>**NCRYPT\_SSL\_SERVER\_FLAG**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="8001a-139">Specifica uno scambio di chiavi sul lato server.</span><span class="sxs-lookup"><span data-stu-id="8001a-139">Specifies a server-side key exchange.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8001a-140">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8001a-140">Return value</span></span>

<span data-ttu-id="8001a-141">Se la funzione ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="8001a-141">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="8001a-142">Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="8001a-142">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="8001a-143">I codici restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="8001a-143">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="8001a-144">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="8001a-144">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="8001a-145">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8001a-145">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8001a-146"><dt>**Nte \_ Nessun \_**</dt> <dt>0x8009000EL</dt> di memoria</span><span class="sxs-lookup"><span data-stu-id="8001a-146"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="8001a-147">La memoria disponibile non è sufficiente per allocare i buffer necessari.</span><span class="sxs-lookup"><span data-stu-id="8001a-147">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="8001a-148"><dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8001a-148"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="8001a-149">Uno degli handle forniti non è valido.</span><span class="sxs-lookup"><span data-stu-id="8001a-149">One of the provided handles is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="8001a-150"><dt>**Nte \_ \_Parametro 0X80090027L non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8001a-150"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="8001a-151">Il parametro *phMasterKey* o *hPublicKey* non è valido.</span><span class="sxs-lookup"><span data-stu-id="8001a-151">The *phMasterKey* or *hPublicKey* parameter is not valid.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="8001a-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8001a-152">Requirements</span></span>



| <span data-ttu-id="8001a-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="8001a-153">Requirement</span></span> | <span data-ttu-id="8001a-154">Valore</span><span class="sxs-lookup"><span data-stu-id="8001a-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8001a-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8001a-155">Minimum supported client</span></span><br/> | <span data-ttu-id="8001a-156">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8001a-156">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8001a-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8001a-157">Minimum supported server</span></span><br/> | <span data-ttu-id="8001a-158">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8001a-158">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8001a-159">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8001a-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="8001a-160"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="8001a-160"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="8001a-161">DLL</span><span class="sxs-lookup"><span data-stu-id="8001a-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8001a-162"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8001a-162"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 


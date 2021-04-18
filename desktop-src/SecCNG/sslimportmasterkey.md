---
description: Esegue un'operazione di scambio di chiave del protocollo SSL (Secure Sockets Layer) sul lato server.
ms.assetid: 052e38ee-658c-47dc-8098-c9a1fd359e1c
title: Funzione SslImportMasterKey (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslImportMasterKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e21c4cd0f6e51662124e02881b82c905dba68c9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311937"
---
# <a name="sslimportmasterkey-function"></a><span data-ttu-id="aac07-103">SslImportMasterKey (funzione)</span><span class="sxs-lookup"><span data-stu-id="aac07-103">SslImportMasterKey function</span></span>

<span data-ttu-id="aac07-104">La funzione **SslImportMasterKey** esegue un'operazione di scambio di chiave del protocollo SSL ( [*Secure Sockets Layer*](/windows/desktop/SecGloss/s-gly) ) sul lato server.</span><span class="sxs-lookup"><span data-stu-id="aac07-104">The **SslImportMasterKey** function performs a server-side [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) key exchange operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="aac07-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aac07-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslImportMasterKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _Out_ NCRYPT_KEY_HANDLE  *phMasterKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  PNCryptBufferDesc  pParameterList,
  _In_  PBYTE              pbEncryptedKey,
  _In_  DWORD              cbEncryptedKey,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="aac07-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="aac07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aac07-107">*hSslProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aac07-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aac07-108">Handle per l'istanza del provider del protocollo SSL.</span><span class="sxs-lookup"><span data-stu-id="aac07-108">The handle to the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="aac07-109">*hPrivateKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aac07-109">*hPrivateKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aac07-110">Handle per la [*chiave privata*](/windows/desktop/SecGloss/p-gly) utilizzata in Exchange.</span><span class="sxs-lookup"><span data-stu-id="aac07-110">The handle to the [*private key*](/windows/desktop/SecGloss/p-gly) used in the exchange.</span></span>

</dd> <dt>

<span data-ttu-id="aac07-111">*phMasterKey* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="aac07-111">*phMasterKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aac07-112">Puntatore all'handle per la ricezione della [*chiave master*](/windows/desktop/SecGloss/m-gly).</span><span class="sxs-lookup"><span data-stu-id="aac07-112">A pointer to the handle to receive the [*master key*](/windows/desktop/SecGloss/m-gly).</span></span>

</dd> <dt>

<span data-ttu-id="aac07-113">*dwProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aac07-113">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aac07-114">Uno dei valori dell' [**identificatore del protocollo del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="aac07-114">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="aac07-115">*dwCipherSuite* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aac07-115">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aac07-116">Uno dei valori degli [**identificatori del pacchetto di crittografia del provider SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="aac07-116">One of the [**CNG SSL Provider Cipher Suite Identifiers**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="aac07-117">*pParameterList* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aac07-117">*pParameterList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aac07-118">Puntatore a una matrice di buffer [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) che contengono informazioni utilizzate come parte dell'operazione di scambio delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="aac07-118">A pointer to an array of [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) buffers that contain information used as part of the key exchange operation.</span></span> <span data-ttu-id="aac07-119">Il set preciso di buffer dipende dal protocollo e dal pacchetto di crittografia utilizzati.</span><span class="sxs-lookup"><span data-stu-id="aac07-119">The precise set of buffers is dependent on the protocol and cipher suite that is used.</span></span> <span data-ttu-id="aac07-120">Come minimo, l'elenco conterrà i buffer contenenti i valori casuali specificati dal client e dal server.</span><span class="sxs-lookup"><span data-stu-id="aac07-120">At the minimum, the list will contain buffers that contain the client and server supplied random values.</span></span>

</dd> <dt>

<span data-ttu-id="aac07-121">*pbEncryptedKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aac07-121">*pbEncryptedKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aac07-122">Puntatore a un buffer contenente la chiave privata premaster crittografata crittografata con la [*chiave pubblica*](/windows/desktop/SecGloss/p-gly) del server.</span><span class="sxs-lookup"><span data-stu-id="aac07-122">A pointer to a buffer that contains the encrypted premaster secret key encrypted with the [*public key*](/windows/desktop/SecGloss/p-gly) of the server.</span></span>

</dd> <dt>

<span data-ttu-id="aac07-123">*cbEncryptedKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aac07-123">*cbEncryptedKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aac07-124">Dimensione, in byte, del buffer *pbEncryptedKey* .</span><span class="sxs-lookup"><span data-stu-id="aac07-124">The size, in bytes, of the *pbEncryptedKey* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="aac07-125">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aac07-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aac07-126">Impostare questo parametro su **NCRYPT \_ SSL \_ server \_ flag** per indicare che si tratta di una chiamata al server.</span><span class="sxs-lookup"><span data-stu-id="aac07-126">Set this parameter to **NCRYPT\_SSL\_SERVER\_FLAG** to indicate that this is a server call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aac07-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aac07-127">Return value</span></span>

<span data-ttu-id="aac07-128">Se la funzione ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="aac07-128">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="aac07-129">Se la funzione ha esito negativo, restituisce un valore di errore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="aac07-129">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="aac07-130">I codici restituiti possibili includono, ma non sono limitati a, quanto segue.</span><span class="sxs-lookup"><span data-stu-id="aac07-130">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="aac07-131">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="aac07-131">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="aac07-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aac07-132">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aac07-133"><dt>**Nte \_ Nessun \_**</dt> <dt>0x8009000EL</dt> di memoria</span><span class="sxs-lookup"><span data-stu-id="aac07-133"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="aac07-134">La memoria disponibile non è sufficiente per allocare i buffer necessari.</span><span class="sxs-lookup"><span data-stu-id="aac07-134">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="aac07-135"><dt>**Nte \_ 0x80090026L \_ handle non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="aac07-135"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="aac07-136">Uno degli handle forniti non è valido.</span><span class="sxs-lookup"><span data-stu-id="aac07-136">One of the provided handles is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="aac07-137"><dt>**Nte \_ \_Parametro 0X80090027L non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="aac07-137"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="aac07-138">Il parametro *phMasterKey* è **null**.</span><span class="sxs-lookup"><span data-stu-id="aac07-138">The *phMasterKey* parameter is **NULL**.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="aac07-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="aac07-139">Remarks</span></span>

<span data-ttu-id="aac07-140">Questa funzione decrittografa il segreto premaster, calcola il master secret SSL e restituisce al chiamante un handle per questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="aac07-140">This function decrypts the premaster secret, computes the SSL master secret, and returns a handle to this object to the caller.</span></span> <span data-ttu-id="aac07-141">Questa chiave master può quindi essere usata per derivare la chiave di sessione SSL e completare l'handshake SSL.</span><span class="sxs-lookup"><span data-stu-id="aac07-141">This master key can then be used to derive the SSL session key and finish the SSL handshake.</span></span>

> [!Note]  
> <span data-ttu-id="aac07-142">Questa funzione viene usata quando si usa l'algoritmo di scambio delle chiavi [*RSA*](/windows/desktop/SecGloss/r-gly) .</span><span class="sxs-lookup"><span data-stu-id="aac07-142">This function is used when the [*RSA*](/windows/desktop/SecGloss/r-gly) key exchange algorithm is being used.</span></span> <span data-ttu-id="aac07-143">Quando si usa [*DH*](/windows/desktop/SecGloss/d-gly) , il codice server chiama invece [**SslGenerateMasterKey**](sslgeneratemasterkey.md) .</span><span class="sxs-lookup"><span data-stu-id="aac07-143">When [*DH*](/windows/desktop/SecGloss/d-gly) is used, then the server code calls [**SslGenerateMasterKey**](sslgeneratemasterkey.md) instead.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="aac07-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aac07-144">Requirements</span></span>



| <span data-ttu-id="aac07-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="aac07-145">Requirement</span></span> | <span data-ttu-id="aac07-146">Valore</span><span class="sxs-lookup"><span data-stu-id="aac07-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="aac07-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aac07-147">Minimum supported client</span></span><br/> | <span data-ttu-id="aac07-148">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aac07-148">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="aac07-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aac07-149">Minimum supported server</span></span><br/> | <span data-ttu-id="aac07-150">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="aac07-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="aac07-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aac07-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="aac07-152"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="aac07-152"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="aac07-153">DLL</span><span class="sxs-lookup"><span data-stu-id="aac07-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aac07-154"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aac07-154"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 


---
description: Fornisce proprietà e metodi per crittografare e decrittografare i dati usando una chiave di sessione derivata da un segreto.
ms.assetid: 3b9bd0a2-6e15-4d58-a682-588a93895799
title: EncryptedData (oggetto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 123e0973343e4990dd2d49cfb321d739085358f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324896"
---
# <a name="encrypteddata-object"></a><span data-ttu-id="1adf3-103">EncryptedData (oggetto)</span><span class="sxs-lookup"><span data-stu-id="1adf3-103">EncryptedData object</span></span>

<span data-ttu-id="1adf3-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1adf3-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="1adf3-105">Usare invece i servizi PInvoke (Platform Invocation Services) per chiamare le funzioni API Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) e [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) per crittografare e decrittografare i messaggi.</span><span class="sxs-lookup"><span data-stu-id="1adf3-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="1adf3-106">Per informazioni su PInvoke, vedere l' [esercitazione Platform Invoke](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="1adf3-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="1adf3-107">Può essere utile anche [.NET e CryptoAPI tramite p/invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) e [.NET e CryptoAPI tramite p/invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) sottosezioni di [estensione della crittografia .NET con CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="1adf3-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="1adf3-108">L'oggetto **EncryptedData** fornisce proprietà e metodi per crittografare e decrittografare i dati usando una [*chiave di sessione*](../secgloss/s-gly.md) derivata da un segreto.</span><span class="sxs-lookup"><span data-stu-id="1adf3-108">The **EncryptedData** object provides properties and methods to encrypt and decrypt data using a [*session key*](../secgloss/s-gly.md) derived from a secret.</span></span>

> [!Note]  
> <span data-ttu-id="1adf3-109">CAPICOM non supporta il \# tipo di contenuto EncryptedData di PKCS 7, ma usa una struttura ASN non standard per **EncryptedData**.</span><span class="sxs-lookup"><span data-stu-id="1adf3-109">CAPICOM does not support the PKCS \#7 EncryptedData content type but uses a nonstandard ASN structure for **EncryptedData**.</span></span> <span data-ttu-id="1adf3-110">Pertanto, solo CAPICOM è in grado di decrittografare un oggetto capicot **EncryptedData** .</span><span class="sxs-lookup"><span data-stu-id="1adf3-110">Therefore, only CAPICOM can decrypt a CAPICOM **EncryptedData** object.</span></span>

 

## <a name="members"></a><span data-ttu-id="1adf3-111">Membri</span><span class="sxs-lookup"><span data-stu-id="1adf3-111">Members</span></span>

<span data-ttu-id="1adf3-112">L'oggetto **EncryptedData** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1adf3-112">The **EncryptedData** object has these types of members:</span></span>

-   [<span data-ttu-id="1adf3-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="1adf3-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="1adf3-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1adf3-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1adf3-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="1adf3-115">Methods</span></span>

<span data-ttu-id="1adf3-116">L'oggetto **EncryptedData** ha questi metodi.</span><span class="sxs-lookup"><span data-stu-id="1adf3-116">The **EncryptedData** object has these methods.</span></span>



| <span data-ttu-id="1adf3-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="1adf3-117">Method</span></span>                                       | <span data-ttu-id="1adf3-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1adf3-118">Description</span></span>                                                                             |
|:---------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="1adf3-119">**Decrypt**</span><span class="sxs-lookup"><span data-stu-id="1adf3-119">**Decrypt**</span></span>](encrypteddata-decrypt.md)     | <span data-ttu-id="1adf3-120">Decrittografa il contenuto crittografato usando il segreto.</span><span class="sxs-lookup"><span data-stu-id="1adf3-120">Decrypts encrypted content using the secret.</span></span><br/>                                 |
| [<span data-ttu-id="1adf3-121">**Crittografare**</span><span class="sxs-lookup"><span data-stu-id="1adf3-121">**Encrypt**</span></span>](encrypteddata-encrypt.md)     | <span data-ttu-id="1adf3-122">Crittografa il contenuto utilizzando l'algoritmo di crittografia e il segreto corrente.</span><span class="sxs-lookup"><span data-stu-id="1adf3-122">Encrypts the content using the current secret and encryption algorithm.</span></span><br/>      |
| [<span data-ttu-id="1adf3-123">**Sesecret**</span><span class="sxs-lookup"><span data-stu-id="1adf3-123">**SetSecret**</span></span>](encrypteddata-setsecret.md) | <span data-ttu-id="1adf3-124">Imposta il segreto da cui viene derivata la chiave della sessione di crittografia/decrittografia.</span><span class="sxs-lookup"><span data-stu-id="1adf3-124">Sets the secret from which the encryption/decryption session key is derived.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1adf3-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1adf3-125">Properties</span></span>

<span data-ttu-id="1adf3-126">L'oggetto **EncryptedData** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1adf3-126">The **EncryptedData** object has these properties.</span></span>



| <span data-ttu-id="1adf3-127">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1adf3-127">Property</span></span>                                                | <span data-ttu-id="1adf3-128">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="1adf3-128">Access type</span></span>           | <span data-ttu-id="1adf3-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1adf3-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:--------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1adf3-130">**Algoritmo**</span><span class="sxs-lookup"><span data-stu-id="1adf3-130">**Algorithm**</span></span>](encrypteddata-algorithm.md)<br/> | <span data-ttu-id="1adf3-131">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="1adf3-131">Read-only</span></span><br/>  | <span data-ttu-id="1adf3-132">Algoritmo utilizzato per la crittografia/decrittografia.</span><span class="sxs-lookup"><span data-stu-id="1adf3-132">Algorithm used for encryption/decryption.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="1adf3-133">**Contenuto**</span><span class="sxs-lookup"><span data-stu-id="1adf3-133">**Content**</span></span>](encrypteddata-content.md)<br/>     | <span data-ttu-id="1adf3-134">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="1adf3-134">Read/write</span></span><br/> | <span data-ttu-id="1adf3-135">Contenuto da crittografare o decrittografare.</span><span class="sxs-lookup"><span data-stu-id="1adf3-135">The content to be encrypted or decrypted.</span></span> <span data-ttu-id="1adf3-136">L'impostazione di questa proprietà deve essere eseguita prima che venga chiamato il metodo [**Encrypt**](encrypteddata-encrypt.md) .</span><span class="sxs-lookup"><span data-stu-id="1adf3-136">Setting this property must be done before the [**Encrypt**](encrypteddata-encrypt.md) method is called.</span></span> <br/> <span data-ttu-id="1adf3-137">Quando il valore di questa proprietà viene reimpostato, direttamente o indirettamente, viene reimpostato l'intero [*stato*](../secgloss/s-gly.md) dell'oggetto e qualsiasi contenuto crittografato nell'oggetto viene perso.</span><span class="sxs-lookup"><span data-stu-id="1adf3-137">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any encrypted content in the object is lost.</span></span><br/> <span data-ttu-id="1adf3-138">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="1adf3-138">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1adf3-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="1adf3-139">Remarks</span></span>

<span data-ttu-id="1adf3-140">È possibile creare l'oggetto **EncryptedData** ed è sicuro per lo scripting.</span><span class="sxs-lookup"><span data-stu-id="1adf3-140">The **EncryptedData** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="1adf3-141">Il ProgID per l'oggetto **EncryptedData** è capicom. EncryptedData. 1.</span><span class="sxs-lookup"><span data-stu-id="1adf3-141">The ProgID for the **EncryptedData** object is CAPICOM.EncryptedData.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="1adf3-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1adf3-142">Requirements</span></span>



| <span data-ttu-id="1adf3-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="1adf3-143">Requirement</span></span> | <span data-ttu-id="1adf3-144">Valore</span><span class="sxs-lookup"><span data-stu-id="1adf3-144">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1adf3-145">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="1adf3-145">End of client support</span></span><br/> | <span data-ttu-id="1adf3-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1adf3-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1adf3-147">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="1adf3-147">End of server support</span></span><br/> | <span data-ttu-id="1adf3-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1adf3-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1adf3-149">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="1adf3-149">Redistributable</span></span><br/>       | <span data-ttu-id="1adf3-150">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="1adf3-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1adf3-151">DLL</span><span class="sxs-lookup"><span data-stu-id="1adf3-151">DLL</span></span><br/>                   | <dl> <span data-ttu-id="1adf3-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1adf3-152"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1adf3-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1adf3-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1adf3-154">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="1adf3-154">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 

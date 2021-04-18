---
description: L'oggetto EnvelopedData fornisce proprietà e metodi per l'inviluppo dei dati per la privacy mediante crittografia.
ms.assetid: 7c5f3e3d-6a70-455d-8921-20495eec4b3e
title: Oggetto EnvelopedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e5309061c6ab315a089a1e1d8b9488556cae9f31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327092"
---
# <a name="envelopeddata-object"></a><span data-ttu-id="2c109-103">Oggetto EnvelopedData</span><span class="sxs-lookup"><span data-stu-id="2c109-103">EnvelopedData object</span></span>

<span data-ttu-id="2c109-104">\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2c109-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="2c109-105">Usare invece la [**classe EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="2c109-105">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="2c109-106">L'oggetto **EnvelopedData** fornisce proprietà e metodi per l'inviluppo dei dati per la privacy mediante crittografia.</span><span class="sxs-lookup"><span data-stu-id="2c109-106">The **EnvelopedData** object provides properties and methods to envelop data for privacy by encryption.</span></span> <span data-ttu-id="2c109-107">Per la busta dei dati, viene generata una chiave crittografica della sessione.</span><span class="sxs-lookup"><span data-stu-id="2c109-107">To envelop data, a session cryptographic key is generated.</span></span> <span data-ttu-id="2c109-108">Tale [*chiave di sessione*](../secgloss/s-gly.md) viene quindi crittografata per ogni destinatario desiderato utilizzando la [*chiave pubblica*](../secgloss/p-gly.md) di quel destinatario previsto dal certificato del destinatario.</span><span class="sxs-lookup"><span data-stu-id="2c109-108">That [*session key*](../secgloss/s-gly.md) is then encrypted for each intended recipient using the [*public key*](../secgloss/p-gly.md) of that intended recipient from the recipient's certificate.</span></span> <span data-ttu-id="2c109-109">I dati crittografati e il set di chiavi di sessione crittografati possono essere inviati a tutti i destinatari desiderati.</span><span class="sxs-lookup"><span data-stu-id="2c109-109">The encrypted data and the set of encrypted session keys can be sent to all intended recipients.</span></span> <span data-ttu-id="2c109-110">Il messaggio generato è in \# formato PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="2c109-110">The message generated is in PKCS \#7 format.</span></span>

## <a name="members"></a><span data-ttu-id="2c109-111">Membri</span><span class="sxs-lookup"><span data-stu-id="2c109-111">Members</span></span>

<span data-ttu-id="2c109-112">L'oggetto **EnvelopedData** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2c109-112">The **EnvelopedData** object has these types of members:</span></span>

-   [<span data-ttu-id="2c109-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="2c109-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="2c109-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2c109-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2c109-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="2c109-115">Methods</span></span>

<span data-ttu-id="2c109-116">L'oggetto **EnvelopedData** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="2c109-116">The **EnvelopedData** object has these methods.</span></span>



| <span data-ttu-id="2c109-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="2c109-117">Method</span></span>                                   | <span data-ttu-id="2c109-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c109-118">Description</span></span>                                                                                                 |
|:-----------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c109-119">**Decrypt**</span><span class="sxs-lookup"><span data-stu-id="2c109-119">**Decrypt**</span></span>](envelopeddata-decrypt.md) | <span data-ttu-id="2c109-120">Decrittografa il contenuto in busta.</span><span class="sxs-lookup"><span data-stu-id="2c109-120">Decrypts enveloped content.</span></span><br/>                                                                      |
| [<span data-ttu-id="2c109-121">**Crittografare**</span><span class="sxs-lookup"><span data-stu-id="2c109-121">**Encrypt**</span></span>](envelopeddata-encrypt.md) | <span data-ttu-id="2c109-122">Crittografa il contenuto, crittografa una chiave di sessione per ogni destinatario e restituisce il BLOB crittografato.</span><span class="sxs-lookup"><span data-stu-id="2c109-122">Encrypts the content, encrypts a session key for each recipient, and returns the encrypted BLOB.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2c109-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2c109-123">Properties</span></span>

<span data-ttu-id="2c109-124">L'oggetto **EnvelopedData** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2c109-124">The **EnvelopedData** object has these properties.</span></span>



| <span data-ttu-id="2c109-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2c109-125">Property</span></span>                                                  | <span data-ttu-id="2c109-126">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="2c109-126">Access type</span></span>           | <span data-ttu-id="2c109-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c109-127">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:----------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c109-128">**Algoritmo**</span><span class="sxs-lookup"><span data-stu-id="2c109-128">**Algorithm**</span></span>](envelopeddata-algorithm.md)<br/>   | <span data-ttu-id="2c109-129">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="2c109-129">Read/write</span></span><br/> | <span data-ttu-id="2c109-130">Algoritmo di crittografia e [*lunghezza della chiave*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2c109-130">Encryption algorithm and [*key length*](../secgloss/k-gly.md).</span></span><br/>                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="2c109-131">**Contenuto**</span><span class="sxs-lookup"><span data-stu-id="2c109-131">**Content**</span></span>](envelopeddata-content.md)<br/>       | <span data-ttu-id="2c109-132">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="2c109-132">Read/write</span></span><br/> | <span data-ttu-id="2c109-133">Contenuto di testo non crittografato di un messaggio da racchiudere.</span><span class="sxs-lookup"><span data-stu-id="2c109-133">The plaintext content of a message to be enveloped.</span></span> <span data-ttu-id="2c109-134">L'impostazione di questa proprietà deve essere eseguita prima che venga chiamato il metodo [**Encrypt**](envelopeddata-encrypt.md) .</span><span class="sxs-lookup"><span data-stu-id="2c109-134">Setting this property must be done before the [**Encrypt**](envelopeddata-encrypt.md) method is called.</span></span><br/> <span data-ttu-id="2c109-135">Quando il valore di questa proprietà viene reimpostato, direttamente o indirettamente, viene reimpostato l'intero [*stato*](../secgloss/s-gly.md) dell'oggetto e qualsiasi contenuto crittografato nell'oggetto viene perso.</span><span class="sxs-lookup"><span data-stu-id="2c109-135">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any encrypted content in the object is lost.</span></span><br/> <span data-ttu-id="2c109-136">Si tratta della proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="2c109-136">This is the default property.</span></span><br/> |
| [<span data-ttu-id="2c109-137">**Destinatari**</span><span class="sxs-lookup"><span data-stu-id="2c109-137">**Recipients**</span></span>](envelopeddata-recipients.md)<br/> | <span data-ttu-id="2c109-138">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="2c109-138">Read-only</span></span><br/>  | <span data-ttu-id="2c109-139">Raccolta di oggetti [**certificato**](certificate.md) per ricevere il messaggio in busta digitale.</span><span class="sxs-lookup"><span data-stu-id="2c109-139">Collection of [**Certificate**](certificate.md) objects to receive the enveloped message.</span></span><br/>                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="2c109-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="2c109-140">Remarks</span></span>

<span data-ttu-id="2c109-141">È possibile creare l'oggetto **EnvelopedData** ed è sicuro per lo scripting.</span><span class="sxs-lookup"><span data-stu-id="2c109-141">The **EnvelopedData** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="2c109-142">Il ProgID per l'oggetto **EnvelopedData** è capicom. EnvelopedData. 1.</span><span class="sxs-lookup"><span data-stu-id="2c109-142">The ProgID for the **EnvelopedData** object is CAPICOM.EnvelopedData.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c109-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c109-143">Requirements</span></span>



| <span data-ttu-id="2c109-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c109-144">Requirement</span></span> | <span data-ttu-id="2c109-145">Valore</span><span class="sxs-lookup"><span data-stu-id="2c109-145">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c109-146">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="2c109-146">End of client support</span></span><br/> | <span data-ttu-id="2c109-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c109-147">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2c109-148">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="2c109-148">End of server support</span></span><br/> | <span data-ttu-id="2c109-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c109-149">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2c109-150">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="2c109-150">Redistributable</span></span><br/>       | <span data-ttu-id="2c109-151">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="2c109-151">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2c109-152">DLL</span><span class="sxs-lookup"><span data-stu-id="2c109-152">DLL</span></span><br/>                   | <dl> <span data-ttu-id="2c109-153"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c109-153"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c109-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c109-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c109-155">**Oggetti Cryptography**</span><span class="sxs-lookup"><span data-stu-id="2c109-155">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 

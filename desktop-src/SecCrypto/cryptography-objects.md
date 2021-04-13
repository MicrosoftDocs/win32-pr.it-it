---
description: Elenca gli oggetti forniti da CryptoAPI.
ms.assetid: 4ab16355-1341-4c7a-b570-bd33f11dde00
title: Oggetti Cryptography
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ea3476e7edad1d32fe1e11635bd65622d2a8375
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401651"
---
# <a name="cryptography-objects"></a><span data-ttu-id="269e1-103">Oggetti Cryptography</span><span class="sxs-lookup"><span data-stu-id="269e1-103">Cryptography Objects</span></span>

<span data-ttu-id="269e1-104">Gli oggetti di crittografia sono suddivisi in categorie in base all'utilizzo come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="269e1-104">Cryptography objects are categorized according to usage as follows:</span></span>

-   [<span data-ttu-id="269e1-105">Oggetti archivio certificati</span><span class="sxs-lookup"><span data-stu-id="269e1-105">Certificate Store Objects</span></span>](#certificate-store-objects)
-   [<span data-ttu-id="269e1-106">Oggetti firma digitale</span><span class="sxs-lookup"><span data-stu-id="269e1-106">Digital Signature Objects</span></span>](#digital-signature-objects)
-   [<span data-ttu-id="269e1-107">Oggetti dati in busta</span><span class="sxs-lookup"><span data-stu-id="269e1-107">Enveloped Data Objects</span></span>](#enveloped-data-objects)
-   [<span data-ttu-id="269e1-108">Oggetti di crittografia dei dati</span><span class="sxs-lookup"><span data-stu-id="269e1-108">Data Encryption Objects</span></span>](#data-encryption-objects)
-   [<span data-ttu-id="269e1-109">Oggetti ausiliari</span><span class="sxs-lookup"><span data-stu-id="269e1-109">Auxiliary Objects</span></span>](#auxiliary-objects)
-   [<span data-ttu-id="269e1-110">Oggetti di registrazione del certificato</span><span class="sxs-lookup"><span data-stu-id="269e1-110">Certificate Enrollment Objects</span></span>](#certificate-enrollment-objects)

## <a name="certificate-store-objects"></a><span data-ttu-id="269e1-111">Oggetti archivio certificati</span><span class="sxs-lookup"><span data-stu-id="269e1-111">Certificate Store Objects</span></span>

<span data-ttu-id="269e1-112">Gli oggetti seguenti funzionano con gli [*archivi certificati*](../secgloss/c-gly.md) e i certificati in tali archivi.</span><span class="sxs-lookup"><span data-stu-id="269e1-112">The following objects work with [*certificate stores*](../secgloss/c-gly.md) and the certificates in those stores.</span></span> <span data-ttu-id="269e1-113">CAPICOM supporta l'uso degli archivi certificati utente corrente, computer locale, memoria e Active Directory.</span><span class="sxs-lookup"><span data-stu-id="269e1-113">CAPICOM supports the use of Current User, Local Machine, memory, and Active Directory certificate stores.</span></span>



| <span data-ttu-id="269e1-114">Oggetto</span><span class="sxs-lookup"><span data-stu-id="269e1-114">Object</span></span>                                             | <span data-ttu-id="269e1-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="269e1-115">Description</span></span>                                                                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="269e1-116">**Certificato**</span><span class="sxs-lookup"><span data-stu-id="269e1-116">**Certificate**</span></span>](certificate.md)                 | <span data-ttu-id="269e1-117">Un singolo certificato digitale.</span><span class="sxs-lookup"><span data-stu-id="269e1-117">A single digital certificate.</span></span>                                                                                           |
| [<span data-ttu-id="269e1-118">**CertificatePolicies**</span><span class="sxs-lookup"><span data-stu-id="269e1-118">**CertificatePolicies**</span></span>](certificatepolicies.md) | <span data-ttu-id="269e1-119">Raccolta di oggetti [**PolicyInformation**](policyinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="269e1-119">A collection of [**PolicyInformation**](policyinformation.md) objects.</span></span>                                                 |
| [<span data-ttu-id="269e1-120">**Certificati**</span><span class="sxs-lookup"><span data-stu-id="269e1-120">**Certificates**</span></span>](certificates.md)               | <span data-ttu-id="269e1-121">Raccolta di oggetti [**Certificate**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="269e1-121">Collection of [**Certificate**](certificate.md) objects.</span></span>                                                               |
| [<span data-ttu-id="269e1-122">**CertificateStatus**</span><span class="sxs-lookup"><span data-stu-id="269e1-122">**CertificateStatus**</span></span>](certificatestatus.md)     | <span data-ttu-id="269e1-123">Fornisce informazioni sullo stato di un certificato.</span><span class="sxs-lookup"><span data-stu-id="269e1-123">Provides status information on a certificate.</span></span>                                                                           |
| [<span data-ttu-id="269e1-124">**Catena**</span><span class="sxs-lookup"><span data-stu-id="269e1-124">**Chain**</span></span>](chain.md)                             | <span data-ttu-id="269e1-125">Crea e verifica una catena di convalida del certificato basata su un certificato digitale.</span><span class="sxs-lookup"><span data-stu-id="269e1-125">Creates and checks a certificate validation chain based on a digital certificate.</span></span>                                       |
| [<span data-ttu-id="269e1-126">**ExtendedProperties**</span><span class="sxs-lookup"><span data-stu-id="269e1-126">**ExtendedProperties**</span></span>](extendedproperties.md)   | <span data-ttu-id="269e1-127">Rappresenta una raccolta di oggetti [**ExtendedProperty**](extendedproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="269e1-127">Represents a collection of [**ExtendedProperty**](extendedproperty.md) objects.</span></span>                                        |
| [<span data-ttu-id="269e1-128">**ExtendedProperty**</span><span class="sxs-lookup"><span data-stu-id="269e1-128">**ExtendedProperty**</span></span>](extendedproperties.md)     | <span data-ttu-id="269e1-129">Rappresenta una proprietà estesa a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="269e1-129">Represents a Microsoft-extended property.</span></span>                                                                               |
| [<span data-ttu-id="269e1-130">**Estensione**</span><span class="sxs-lookup"><span data-stu-id="269e1-130">**Extension**</span></span>](extension.md)                     | <span data-ttu-id="269e1-131">Rappresenta una singola estensione del certificato.</span><span class="sxs-lookup"><span data-stu-id="269e1-131">Represents a single certificate extension.</span></span>                                                                              |
| [<span data-ttu-id="269e1-132">**Estensioni**</span><span class="sxs-lookup"><span data-stu-id="269e1-132">**Extensions**</span></span>](extensions.md)                   | <span data-ttu-id="269e1-133">Rappresenta una raccolta di oggetti di [**estensione**](extension.md) .</span><span class="sxs-lookup"><span data-stu-id="269e1-133">Represents a collection of [**Extension**](extension.md) objects.</span></span>                                                      |
| [<span data-ttu-id="269e1-134">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="269e1-134">**PrivateKey**</span></span>](privatekey.md)                   | <span data-ttu-id="269e1-135">Rappresenta una chiave privata.</span><span class="sxs-lookup"><span data-stu-id="269e1-135">Represents a private key.</span></span>                                                                                               |
| [<span data-ttu-id="269e1-136">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="269e1-136">**PublicKey**</span></span>](publickey.md)                     | <span data-ttu-id="269e1-137">Rappresenta una chiave pubblica in un oggetto [**certificato**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="269e1-137">Represents a public key in a [**Certificate**](certificate.md) object.</span></span>                                                 |
| [<span data-ttu-id="269e1-138">**Store**</span><span class="sxs-lookup"><span data-stu-id="269e1-138">**Store**</span></span>](store.md)                             | <span data-ttu-id="269e1-139">Fornisce le proprietà e i metodi per scegliere, gestire e usare gli archivi certificati e i certificati in tali archivi.</span><span class="sxs-lookup"><span data-stu-id="269e1-139">Provides the properties and methods to choose, manage, and use certificate stores and the certificates in those stores.</span></span> |
| [<span data-ttu-id="269e1-140">**Modello**</span><span class="sxs-lookup"><span data-stu-id="269e1-140">**Template**</span></span>](template.md)                       | <span data-ttu-id="269e1-141">Rappresenta il modello di estensione del certificato del certificato.</span><span class="sxs-lookup"><span data-stu-id="269e1-141">Represents the certificate extension template of the certificate.</span></span>                                                       |



 

## <a name="digital-signature-objects"></a><span data-ttu-id="269e1-142">Oggetti firma digitale</span><span class="sxs-lookup"><span data-stu-id="269e1-142">Digital Signature Objects</span></span>

<span data-ttu-id="269e1-143">Gli oggetti seguenti vengono esportati per la firma digitale dei dati e per la verifica delle firme digitali.</span><span class="sxs-lookup"><span data-stu-id="269e1-143">The following objects are exported to digitally sign data and to verify digital signatures.</span></span>



| <span data-ttu-id="269e1-144">Oggetto</span><span class="sxs-lookup"><span data-stu-id="269e1-144">Object</span></span>                           | <span data-ttu-id="269e1-145">Descrizione</span><span class="sxs-lookup"><span data-stu-id="269e1-145">Description</span></span>                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="269e1-146">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="269e1-146">**SignedCode**</span></span>](signedcode.md) | <span data-ttu-id="269e1-147">Oggetto utilizzato per firmare il codice con una firma digitale Authenticode e per verificare la firma sul codice firmato.</span><span class="sxs-lookup"><span data-stu-id="269e1-147">Object used to sign code with an Authenticode digital signature and to verify the signature on signed code.</span></span> |
| [<span data-ttu-id="269e1-148">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="269e1-148">**SignedData**</span></span>](signeddata.md) | <span data-ttu-id="269e1-149">Oggetto utilizzato per firmare i dati e verificare la firma sui dati firmati.</span><span class="sxs-lookup"><span data-stu-id="269e1-149">Object used to sign data and to verify the signature on signed data.</span></span>                                        |
| [<span data-ttu-id="269e1-150">**Firmatario**</span><span class="sxs-lookup"><span data-stu-id="269e1-150">**Signer**</span></span>](signer.md)         | <span data-ttu-id="269e1-151">Informazioni su un singolo firmatario di dati, incluso il certificato del firmatario.</span><span class="sxs-lookup"><span data-stu-id="269e1-151">Information on a single data signer, including the signer's certificate.</span></span>                                    |
| [<span data-ttu-id="269e1-152">**Firmatari**</span><span class="sxs-lookup"><span data-stu-id="269e1-152">**Signers**</span></span>](signers.md)       | <span data-ttu-id="269e1-153">Raccolta di oggetti [**firmatari**](signer.md) .</span><span class="sxs-lookup"><span data-stu-id="269e1-153">Collection of [**Signer**](signer.md) objects.</span></span>                                                             |



 

## <a name="enveloped-data-objects"></a><span data-ttu-id="269e1-154">Oggetti dati in busta</span><span class="sxs-lookup"><span data-stu-id="269e1-154">Enveloped Data Objects</span></span>

<span data-ttu-id="269e1-155">Gli oggetti seguenti vengono esportati per creare messaggi di dati in busta per la privacy e per decrittografare i dati nei messaggi in busta digitale.</span><span class="sxs-lookup"><span data-stu-id="269e1-155">The following objects are exported to create enveloped data messages for privacy and to decrypt data in enveloped messages.</span></span>



| <span data-ttu-id="269e1-156">Oggetto</span><span class="sxs-lookup"><span data-stu-id="269e1-156">Object</span></span>                                 | <span data-ttu-id="269e1-157">Descrizione</span><span class="sxs-lookup"><span data-stu-id="269e1-157">Description</span></span>                                                                                                                                |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="269e1-158">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="269e1-158">**EnvelopedData**</span></span>](envelopeddata.md) | <span data-ttu-id="269e1-159">Oggetti utilizzati per creare, inviare e ricevere dati in busta.</span><span class="sxs-lookup"><span data-stu-id="269e1-159">Objects used to create, send, and receive enveloped data.</span></span> <span data-ttu-id="269e1-160">I dati in busta digitale vengono crittografati in modo che solo i destinatari desiderati possano decrittografarli.</span><span class="sxs-lookup"><span data-stu-id="269e1-160">Enveloped data is encrypted so that only the intended recipients can decrypt it.</span></span> |
| [<span data-ttu-id="269e1-161">**Destinatari**</span><span class="sxs-lookup"><span data-stu-id="269e1-161">**Recipients**</span></span>](recipients.md)       | <span data-ttu-id="269e1-162">Raccolta degli oggetti [**certificato**](certificate.md) dei destinatari desiderati di un messaggio in busta digitale.</span><span class="sxs-lookup"><span data-stu-id="269e1-162">Collection of the [**Certificate**](certificate.md) objects of the intended recipients of an enveloped message.</span></span>                           |



 

## <a name="data-encryption-objects"></a><span data-ttu-id="269e1-163">Oggetti di crittografia dei dati</span><span class="sxs-lookup"><span data-stu-id="269e1-163">Data Encryption Objects</span></span>

<span data-ttu-id="269e1-164">L'oggetto seguente viene esportato per crittografare i dati arbitrari per la privacy e per decrittografare i dati crittografati.</span><span class="sxs-lookup"><span data-stu-id="269e1-164">The following object is exported to encrypt arbitrary data for privacy and to decrypt encrypted data.</span></span>



| <span data-ttu-id="269e1-165">Oggetto</span><span class="sxs-lookup"><span data-stu-id="269e1-165">Object</span></span>                                 | <span data-ttu-id="269e1-166">Descrizione</span><span class="sxs-lookup"><span data-stu-id="269e1-166">Description</span></span>                                                                                                        |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="269e1-167">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="269e1-167">**EncryptedData**</span></span>](encrypteddata.md) | <span data-ttu-id="269e1-168">Oggetti utilizzati per crittografare i dati.</span><span class="sxs-lookup"><span data-stu-id="269e1-168">Objects used to encrypt data.</span></span> <span data-ttu-id="269e1-169">I dati crittografati in un oggetto [**EncryptedData**](encrypteddata.md) possono essere decrittografati.</span><span class="sxs-lookup"><span data-stu-id="269e1-169">Encrypted data in an [**EncryptedData**](encrypteddata.md) object can be decrypted.</span></span> |



 

## <a name="auxiliary-objects"></a><span data-ttu-id="269e1-170">Oggetti ausiliari</span><span class="sxs-lookup"><span data-stu-id="269e1-170">Auxiliary Objects</span></span>

<span data-ttu-id="269e1-171">Gli oggetti seguenti vengono esportati per modificare i comportamenti predefiniti di altri oggetti e per gestire certificati, archivi certificati e messaggi.</span><span class="sxs-lookup"><span data-stu-id="269e1-171">The following objects are exported to change default behaviors of other objects and to manage certificates, certificate stores, and messages.</span></span>



| <span data-ttu-id="269e1-172">Oggetto</span><span class="sxs-lookup"><span data-stu-id="269e1-172">Object</span></span>                                         | <span data-ttu-id="269e1-173">Descrizione</span><span class="sxs-lookup"><span data-stu-id="269e1-173">Description</span></span>                                                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="269e1-174">**Algoritmo**</span><span class="sxs-lookup"><span data-stu-id="269e1-174">**Algorithm**</span></span>](algorithm.md)                 | <span data-ttu-id="269e1-175">Imposta l'algoritmo e la [*lunghezza della chiave*](../secgloss/k-gly.md) da utilizzare nelle operazioni di crittografia.</span><span class="sxs-lookup"><span data-stu-id="269e1-175">Sets the algorithm and [*key length*](../secgloss/k-gly.md) to be used in cryptographic operations.</span></span> |
| [<span data-ttu-id="269e1-176">**Attributo**</span><span class="sxs-lookup"><span data-stu-id="269e1-176">**Attribute**</span></span>](attribute.md)                 | <span data-ttu-id="269e1-177">Fornisce una singola parte di informazioni aggiuntive su una firma, ad esempio l'ora di firma.</span><span class="sxs-lookup"><span data-stu-id="269e1-177">Provides a single piece of added information about a signature, such as the time of signing.</span></span>                                                    |
| [<span data-ttu-id="269e1-178">**Attributi**</span><span class="sxs-lookup"><span data-stu-id="269e1-178">**Attributes**</span></span>](attributes.md)               | <span data-ttu-id="269e1-179">Raccolta di oggetti [**attributo**](attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="269e1-179">Collection of [**Attribute**](attribute.md) objects.</span></span>                                                                                           |
| [<span data-ttu-id="269e1-180">**BasicConstraints**</span><span class="sxs-lookup"><span data-stu-id="269e1-180">**BasicConstraints**</span></span>](basicconstraints.md)   | <span data-ttu-id="269e1-181">Fornisce accesso in sola lettura ai vincoli di base sull'utilizzo di un certificato.</span><span class="sxs-lookup"><span data-stu-id="269e1-181">Provides read-only access to basic constraints on the uses of a certificate.</span></span>                                                                    |
| [<span data-ttu-id="269e1-182">**EKU**</span><span class="sxs-lookup"><span data-stu-id="269e1-182">**EKU**</span></span>](eku.md)                             | <span data-ttu-id="269e1-183">Fornisce l'accesso alle proprietà EKU dei certificati.</span><span class="sxs-lookup"><span data-stu-id="269e1-183">Provides access to EKU properties of certificates.</span></span>                                                                                              |
| [<span data-ttu-id="269e1-184">**EKU**</span><span class="sxs-lookup"><span data-stu-id="269e1-184">**EKUs**</span></span>](ekus.md)                           | <span data-ttu-id="269e1-185">Raccolta di oggetti [**EKU**](eku.md) .</span><span class="sxs-lookup"><span data-stu-id="269e1-185">Collection of [**EKU**](eku.md) objects.</span></span>                                                                                                       |
| [<span data-ttu-id="269e1-186">**EncodedData**</span><span class="sxs-lookup"><span data-stu-id="269e1-186">**EncodedData**</span></span>](encodeddata.md)             | <span data-ttu-id="269e1-187">Rappresenta un blocco di dati codificati.</span><span class="sxs-lookup"><span data-stu-id="269e1-187">Represents a block of encoded data.</span></span>                                                                                                             |
| [<span data-ttu-id="269e1-188">**ExtendedKeyUsage**</span><span class="sxs-lookup"><span data-stu-id="269e1-188">**ExtendedKeyUsage**</span></span>](extendedkeyusage.md)   | <span data-ttu-id="269e1-189">Fornisce accesso in sola lettura alle proprietà di utilizzo chiavi estese dei certificati.</span><span class="sxs-lookup"><span data-stu-id="269e1-189">Provides read-only access to the extended key usage properties of certificates.</span></span>                                                                 |
| [<span data-ttu-id="269e1-190">**HashedData**</span><span class="sxs-lookup"><span data-stu-id="269e1-190">**HashedData**</span></span>](hasheddata.md)               | <span data-ttu-id="269e1-191">Fornisce la funzionalità per l'applicazione di un algoritmo hash a una stringa.</span><span class="sxs-lookup"><span data-stu-id="269e1-191">Provides functionality for applying a hash algorithm to a string.</span></span>                                                                               |
| [<span data-ttu-id="269e1-192">**KeyUsage**</span><span class="sxs-lookup"><span data-stu-id="269e1-192">**KeyUsage**</span></span>](keyusage.md)                   | <span data-ttu-id="269e1-193">Fornisce accesso in sola lettura alle proprietà di utilizzo chiave dei certificati.</span><span class="sxs-lookup"><span data-stu-id="269e1-193">Provides read-only access to key usage properties of certificates.</span></span>                                                                              |
| [<span data-ttu-id="269e1-194">**NoticeNumbers**</span><span class="sxs-lookup"><span data-stu-id="269e1-194">**NoticeNumbers**</span></span>](noticenumbers.md)         | <span data-ttu-id="269e1-195">Rappresenta una raccolta di oggetti di [**estensione**](extension.md) .</span><span class="sxs-lookup"><span data-stu-id="269e1-195">Represents a collection of [**Extension**](extension.md) objects.</span></span>                                                                              |
| [<span data-ttu-id="269e1-196">**OID**</span><span class="sxs-lookup"><span data-stu-id="269e1-196">**OID**</span></span>](oid.md)                             | <span data-ttu-id="269e1-197">Rappresenta un identificatore di oggetto utilizzato da diverse proprietà di CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="269e1-197">Represents an object identifier that is used by several CAPICOM properties.</span></span>                                                                     |
| [<span data-ttu-id="269e1-198">**OID**</span><span class="sxs-lookup"><span data-stu-id="269e1-198">**OIDs**</span></span>](oids.md)                           | <span data-ttu-id="269e1-199">Rappresenta una raccolta di oggetti [**OID**](oid.md) .</span><span class="sxs-lookup"><span data-stu-id="269e1-199">Represents a collection of [**OID**](oid.md) objects.</span></span>                                                                                          |
| [<span data-ttu-id="269e1-200">**PolicyInformation**</span><span class="sxs-lookup"><span data-stu-id="269e1-200">**PolicyInformation**</span></span>](policyinformation.md) | <span data-ttu-id="269e1-201">Consente di accedere ai criteri OID di un'estensione.</span><span class="sxs-lookup"><span data-stu-id="269e1-201">Provides access to the policy OIDs of an extension.</span></span>                                                                                             |
| [<span data-ttu-id="269e1-202">**Qualifier**</span><span class="sxs-lookup"><span data-stu-id="269e1-202">**Qualifier**</span></span>](qualifier.md)                 | <span data-ttu-id="269e1-203">Rappresenta un puntatore CPS (Certification Practice Statement) o un qualificatore di avviso utente.</span><span class="sxs-lookup"><span data-stu-id="269e1-203">Represents a Certification Practice Statement (CPS) pointer or user notice qualifier.</span></span>                                                           |
| [<span data-ttu-id="269e1-204">**Qualificatori**</span><span class="sxs-lookup"><span data-stu-id="269e1-204">**Qualifiers**</span></span>](qualifiers.md)               | <span data-ttu-id="269e1-205">Rappresenta una raccolta di qualificatori.</span><span class="sxs-lookup"><span data-stu-id="269e1-205">Represents a collection of qualifiers.</span></span>                                                                                                          |
| [<span data-ttu-id="269e1-206">**Impostazioni**</span><span class="sxs-lookup"><span data-stu-id="269e1-206">**Settings**</span></span>](settings.md)                   | <span data-ttu-id="269e1-207">Abilita o Disabilita le finestre di dialogo per richiedere l'identità del firmatario o del mittente se tale identità non è specificata.</span><span class="sxs-lookup"><span data-stu-id="269e1-207">Enables or disables dialog boxes to prompt for signer or sender identity if that identity is not specified.</span></span>                                     |
| [<span data-ttu-id="269e1-208">**Utilità**</span><span class="sxs-lookup"><span data-stu-id="269e1-208">**Utilities**</span></span>](utilities.md)                 | <span data-ttu-id="269e1-209">Fornisce funzionalità per le attività comuni.</span><span class="sxs-lookup"><span data-stu-id="269e1-209">Provides functionality for common tasks.</span></span>                                                                                                        |



 

## <a name="certificate-enrollment-objects"></a><span data-ttu-id="269e1-210">Oggetti di registrazione del certificato</span><span class="sxs-lookup"><span data-stu-id="269e1-210">Certificate Enrollment Objects</span></span>

<span data-ttu-id="269e1-211">L'oggetto seguente viene usato per la registrazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="269e1-211">The following object is used for certificate enrollment.</span></span>



| <span data-ttu-id="269e1-212">Oggetto</span><span class="sxs-lookup"><span data-stu-id="269e1-212">Object</span></span>                     | <span data-ttu-id="269e1-213">Descrizione</span><span class="sxs-lookup"><span data-stu-id="269e1-213">Description</span></span>                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="269e1-214">[**CEnroll**](/previous-versions/windows/desktop/legacy/aa376007(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="269e1-214">[**CEnroll**](/previous-versions/windows/desktop/legacy/aa376007(v=vs.85))</span></span> | <span data-ttu-id="269e1-215">Oggetto che rappresenta il controllo di registrazione del certificato.</span><span class="sxs-lookup"><span data-stu-id="269e1-215">Object that represents the Certificate Enrollment Control.</span></span> <span data-ttu-id="269e1-216">Viene utilizzato principalmente per la programmazione in Visual Basic o in un altro linguaggio di automazione.</span><span class="sxs-lookup"><span data-stu-id="269e1-216">It is primarily used when programming in Visual Basic or another Automation language.</span></span> |



 

 

 

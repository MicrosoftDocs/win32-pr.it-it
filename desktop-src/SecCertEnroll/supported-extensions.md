---
description: È possibile usare l'interfaccia IX509Extension per definire un'estensione arbitraria.
ms.assetid: 025447f4-98d0-4cb8-b546-4797b7e60722
title: Estensioni supportate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd55886b03cdea5783f918182c84382910510918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752162"
---
# <a name="supported-extensions"></a><span data-ttu-id="a870b-103">Estensioni supportate</span><span class="sxs-lookup"><span data-stu-id="a870b-103">Supported Extensions</span></span>

<span data-ttu-id="a870b-104">È possibile usare l'interfaccia [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) per definire un'estensione arbitraria.</span><span class="sxs-lookup"><span data-stu-id="a870b-104">You can use the [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) interface to define an arbitrary extension.</span></span> <span data-ttu-id="a870b-105">L'API di registrazione certificati fornisce anche le interfacce derivate da **IX509Extension** per consentire di creare facilmente le estensioni più comuni.</span><span class="sxs-lookup"><span data-stu-id="a870b-105">The Certificate Enrollment API also provides interfaces derived from **IX509Extension** to enable you to easily create any of the most common extensions.</span></span> <span data-ttu-id="a870b-106">Nell'elenco seguente vengono identificate le estensioni comuni supportate dalle autorità di certificazione Microsoft e gli identificatori e le interfacce di oggetto che è possibile utilizzare per crearli.</span><span class="sxs-lookup"><span data-stu-id="a870b-106">The following list identifies the common extensions supported by Microsoft certification authorities, and the object identifiers and interfaces that you can use to create them.</span></span>

## <a name="alternativenames"></a><span data-ttu-id="a870b-107">AlternativeNames</span><span class="sxs-lookup"><span data-stu-id="a870b-107">AlternativeNames</span></span>

<span data-ttu-id="a870b-108">L'estensione dei nomi alternativi può essere usata per definire uno o più moduli nome alternativi per l'oggetto della richiesta di certificato.</span><span class="sxs-lookup"><span data-stu-id="a870b-108">The alternative names extension can be used to define one or more alternative name forms for the subject of the certificate request.</span></span> <span data-ttu-id="a870b-109">Esempi di forme alternative includono indirizzi email, nomi DNS; indirizzi IP e URI.</span><span class="sxs-lookup"><span data-stu-id="a870b-109">Example alternative forms include email addresses, DNS names, IP addresses, and URIs.</span></span>

<span data-ttu-id="a870b-110">**Interfaccia:** [ **IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)</span><span class="sxs-lookup"><span data-stu-id="a870b-110">**Interface:** [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)</span></span>

<span data-ttu-id="a870b-111">**OID:** \_Oggetto Oid \_ XCN \_ ALT \_ name2 (2.5.29.17)</span><span class="sxs-lookup"><span data-stu-id="a870b-111">**OID:** XCN\_OID\_SUBJECT\_ALT\_NAME2 (2.5.29.17)</span></span>

## <a name="authorityinformationaccess"></a><span data-ttu-id="a870b-112">AuthorityInformationAccess</span><span class="sxs-lookup"><span data-stu-id="a870b-112">AuthorityInformationAccess</span></span>

<span data-ttu-id="a870b-113">L'estensione di accesso alle informazioni sull'autorità identifica come accedere alle informazioni e ai servizi della CA.</span><span class="sxs-lookup"><span data-stu-id="a870b-113">The authority information access extension identifies how to access CA information and services.</span></span> <span data-ttu-id="a870b-114">Il valore dell'estensione contiene una sequenza di URI.</span><span class="sxs-lookup"><span data-stu-id="a870b-114">The extension value contains a sequence of URIs.</span></span>

<span data-ttu-id="a870b-115">**Interfaccia:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="a870b-115">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="a870b-116">**OID:** XCN \_ OID \_ Authority \_ info \_ Access (1.3.6.1.5.5.7.1.1)</span><span class="sxs-lookup"><span data-stu-id="a870b-116">**OID:** XCN\_OID\_AUTHORITY\_INFO\_ACCESS (1.3.6.1.5.5.7.1.1)</span></span>

## <a name="authoritykeyidentifier"></a><span data-ttu-id="a870b-117">AuthorityKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="a870b-117">AuthorityKeyIdentifier</span></span>

<span data-ttu-id="a870b-118">L'estensione dell'identificatore di chiave dell'autorità consente l'identificazione della chiave pubblica dell'autorità di certificazione che corrisponde alla chiave privata della CA che ha firmato un certificato emesso.</span><span class="sxs-lookup"><span data-stu-id="a870b-118">The authority key identifier extension enables identification of the CA public key that corresponds to the CA private key that signed an issued certificate.</span></span> <span data-ttu-id="a870b-119">Viene usato dal percorso del certificato per la creazione di software in un server Windows per trovare il certificato della CA.</span><span class="sxs-lookup"><span data-stu-id="a870b-119">It is used by certificate path building software on a Windows server to find the CA certificate.</span></span> <span data-ttu-id="a870b-120">Quando un'autorità di certificazione emette un certificato, il valore dell'estensione viene impostato in modo uguale all'estensione **SubjectKeyIdentifier** nel certificato di firma della CA.</span><span class="sxs-lookup"><span data-stu-id="a870b-120">When a CA issues a certificate, the extension value is set equal to the **SubjectKeyIdentifier** extension in the CA signing certificate.</span></span> <span data-ttu-id="a870b-121">Il valore è in genere un hash SHA-1 della chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="a870b-121">The value is typically a SHA-1 hash of the public key.</span></span>

<span data-ttu-id="a870b-122">**Interfaccia:** [ **IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier)</span><span class="sxs-lookup"><span data-stu-id="a870b-122">**Interface:** [**IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier)</span></span>

<span data-ttu-id="a870b-123">**OID:** \_Chiave dell' \_ autorità OID XCN \_ \_ IDENTIFIER2 (2.5.29.35)</span><span class="sxs-lookup"><span data-stu-id="a870b-123">**OID:** XCN\_OID\_AUTHORITY\_KEY\_IDENTIFIER2 (2.5.29.35)</span></span>

## <a name="basicconstraints"></a><span data-ttu-id="a870b-124">BasicConstraints</span><span class="sxs-lookup"><span data-stu-id="a870b-124">BasicConstraints</span></span>

<span data-ttu-id="a870b-125">L'estensione dei vincoli di base può essere usata per determinare se l'entità può essere usata come autorità di certificazione (CA) e, in caso affermativo, il numero di CA subordinate che possono esistere al di sotto di esso nella catena di certificati.</span><span class="sxs-lookup"><span data-stu-id="a870b-125">The basic constraints extension can be used to identify whether the entity can be used as a certification authority (CA) and, if so, the number of subordinate CAs that can exist beneath it in the certificate chain.</span></span>

<span data-ttu-id="a870b-126">**Interfaccia:** [ **IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)</span><span class="sxs-lookup"><span data-stu-id="a870b-126">**Interface:** [**IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)</span></span>

<span data-ttu-id="a870b-127">**OID:** XCN \_ OID \_ Basic \_ CONSTRAINTS2 (2.5.29.19)</span><span class="sxs-lookup"><span data-stu-id="a870b-127">**OID:** XCN\_OID\_BASIC\_CONSTRAINTS2 (2.5.29.19)</span></span>

## <a name="certificatepolicies"></a><span data-ttu-id="a870b-128">CertificatePolicies</span><span class="sxs-lookup"><span data-stu-id="a870b-128">CertificatePolicies</span></span>

<span data-ttu-id="a870b-129">È possibile utilizzare l'estensione criteri certificati per identificare i criteri con cui il certificato è stato emesso ed è possibile utilizzarne gli scopi.</span><span class="sxs-lookup"><span data-stu-id="a870b-129">The certificate policies extension can be used to identify the policies under which the certificate has been issued and the purposes for it can be used.</span></span> <span data-ttu-id="a870b-130">Sono identificati da una raccolta di identificatori di oggetto (OID).</span><span class="sxs-lookup"><span data-stu-id="a870b-130">These are identified by a collection of object identifiers (OIDs).</span></span> <span data-ttu-id="a870b-131">I criteri vengono personalizzati per i requisiti di un'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="a870b-131">Policies are customized for the requirements of an organization.</span></span>

<span data-ttu-id="a870b-132">**Interfaccia:** [ **IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)</span><span class="sxs-lookup"><span data-stu-id="a870b-132">**Interface:** [**IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)</span></span>

<span data-ttu-id="a870b-133">**OID:** \_ \_ Criteri certificato OID XCN \_ (2.5.29.32)</span><span class="sxs-lookup"><span data-stu-id="a870b-133">**OID:** XCN\_OID\_CERT\_POLICIES (2.5.29.32)</span></span>

## <a name="crldistributionpoints"></a><span data-ttu-id="a870b-134">CrlDistributionPoints</span><span class="sxs-lookup"><span data-stu-id="a870b-134">CrlDistributionPoints</span></span>

<span data-ttu-id="a870b-135">L'estensione dei punti di distribuzione dell'elenco di revoche di certificati (CRL) contiene l'URI dell'elenco di revoche di certificati (CRL) di base.</span><span class="sxs-lookup"><span data-stu-id="a870b-135">The certificate revocation list (CRL) distribution points extension contains the URI of the base certificate revocation list (CRL).</span></span>

<span data-ttu-id="a870b-136">**Interfaccia:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="a870b-136">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="a870b-137">**OID:** XCN \_ OID \_ CRL \_ punti di dist \_ (2.5.29.31)</span><span class="sxs-lookup"><span data-stu-id="a870b-137">**OID:** XCN\_OID\_CRL\_DIST\_POINTS (2.5.29.31)</span></span>

## <a name="enhancedkeyusage"></a><span data-ttu-id="a870b-138">Campo EnhancedKeyUsage</span><span class="sxs-lookup"><span data-stu-id="a870b-138">EnhancedKeyUsage</span></span>

<span data-ttu-id="a870b-139">L'estensione utilizzo chiavi avanzato può essere usata per definire uno o più usi della chiave pubblica contenuta nel certificato.</span><span class="sxs-lookup"><span data-stu-id="a870b-139">The enhanced key usage extension can be used to define one or more uses of the public key contained in the certificate.</span></span>

<span data-ttu-id="a870b-140">**Interfaccia:** [ **IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)</span><span class="sxs-lookup"><span data-stu-id="a870b-140">**Interface:** [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)</span></span>

<span data-ttu-id="a870b-141">**OID:** \_ \_ Utilizzo chiavi avanzato OID XCN \_ \_ (2.5.29.37)</span><span class="sxs-lookup"><span data-stu-id="a870b-141">**OID:** XCN\_OID\_ENHANCED\_KEY\_USAGE (2.5.29.37)</span></span>

## <a name="freshestcrl"></a><span data-ttu-id="a870b-142">FreshestCRL</span><span class="sxs-lookup"><span data-stu-id="a870b-142">FreshestCRL</span></span>

<span data-ttu-id="a870b-143">L'estensione CRL più aggiornata contiene l'URI del Delta CRL.</span><span class="sxs-lookup"><span data-stu-id="a870b-143">The freshest CRL extension contains the URI of the delta CRL.</span></span> <span data-ttu-id="a870b-144">Per questa estensione e l'estensione **CrlDistributionPoints** viene utilizzata la stessa sintassi ASN. 1.</span><span class="sxs-lookup"><span data-stu-id="a870b-144">The same ASN.1 syntax is used for this extension and the **CrlDistributionPoints** extension.</span></span>

<span data-ttu-id="a870b-145">**Interfaccia:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="a870b-145">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="a870b-146">**OID:** XCN \_ OID più \_ recente \_ CRL (2.5.29.46)</span><span class="sxs-lookup"><span data-stu-id="a870b-146">**OID:** XCN\_OID\_FRESHEST\_CRL (2.5.29.46)</span></span>

## <a name="keyusage"></a><span data-ttu-id="a870b-147">KeyUsage</span><span class="sxs-lookup"><span data-stu-id="a870b-147">KeyUsage</span></span>

<span data-ttu-id="a870b-148">L'estensione utilizzo chiave può essere utilizzata per definire restrizioni sulle operazioni che possono essere eseguite dalla chiave pubblica contenuta nel certificato.</span><span class="sxs-lookup"><span data-stu-id="a870b-148">The key usage extension can be used to define restrictions on the operations that can be performed by the public key contained in the certificate.</span></span> <span data-ttu-id="a870b-149">Ad esempio, è possibile specificare che la chiave pubblica deve essere utilizzata solo per creare una firma digitale, firmare un elenco di revoche di certificati (CRL) o crittografare un'altra chiave.</span><span class="sxs-lookup"><span data-stu-id="a870b-149">For example, you can specify that the public key be used only to create a digital signature, sign a certificate revocation list (CRL), or encrypt another key.</span></span>

<span data-ttu-id="a870b-150">**Interfaccia:** [ **IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)</span><span class="sxs-lookup"><span data-stu-id="a870b-150">**Interface:** [**IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)</span></span>

<span data-ttu-id="a870b-151">**OID:** \_ \_ Utilizzo chiave OID XCN \_ (2.5.29.15)</span><span class="sxs-lookup"><span data-stu-id="a870b-151">**OID:** XCN\_OID\_KEY\_USAGE (2.5.29.15)</span></span>

## <a name="msapplicationpolicies"></a><span data-ttu-id="a870b-152">MSApplicationPolicies</span><span class="sxs-lookup"><span data-stu-id="a870b-152">MSApplicationPolicies</span></span>

<span data-ttu-id="a870b-153">L'estensione criteri per le applicazioni Microsoft può essere utilizzata da un'applicazione per filtrare i certificati sulla base dell'utilizzo consentito.</span><span class="sxs-lookup"><span data-stu-id="a870b-153">The Microsoft application policies extension can be used by an application to filter certificates on the basis of permitted use.</span></span> <span data-ttu-id="a870b-154">Gli utilizzi consentiti sono identificati da OID.</span><span class="sxs-lookup"><span data-stu-id="a870b-154">Permitted uses are identified by OIDs.</span></span> <span data-ttu-id="a870b-155">Questa estensione è simile all'estensione **campo EnhancedKeyUsage** ma con una semantica più restrittiva applicata alla CA padre.</span><span class="sxs-lookup"><span data-stu-id="a870b-155">This extension is similar to the **EnhancedKeyUsage** extension but with stricter semantics applied to the parent CA.</span></span> <span data-ttu-id="a870b-156">L'estensione è specifica di Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a870b-156">The extension is Microsoft specific.</span></span>

<span data-ttu-id="a870b-157">**Interfaccia:** [ **IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)</span><span class="sxs-lookup"><span data-stu-id="a870b-157">**Interface:** [**IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)</span></span>

<span data-ttu-id="a870b-158">**OID:** \_Criteri del \_ certificato dell'applicazione OID XCN \_ \_ (1.3.6.1.4.1.311.21.10)</span><span class="sxs-lookup"><span data-stu-id="a870b-158">**OID:** XCN\_OID\_APPLICATION\_CERT\_POLICIES (1.3.6.1.4.1.311.21.10)</span></span>

## <a name="nameconstraints"></a><span data-ttu-id="a870b-159">NameConstraints</span><span class="sxs-lookup"><span data-stu-id="a870b-159">NameConstraints</span></span>

<span data-ttu-id="a870b-160">L'estensione vincoli di nome viene utilizzata per identificare lo spazio dei nomi nel quale devono essere individuati tutti i nomi soggetto dei certificati in una gerarchia di certificati.</span><span class="sxs-lookup"><span data-stu-id="a870b-160">The name constraints extension is used to identify the namespace within which all subject names of certificates in a certificate hierarchy must be located.</span></span> <span data-ttu-id="a870b-161">L'estensione è usata solo in un certificato di autorità di certificazione.</span><span class="sxs-lookup"><span data-stu-id="a870b-161">The extension is used only in a CA certificate.</span></span>

<span data-ttu-id="a870b-162">**Interfaccia:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="a870b-162">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="a870b-163">**OID:** \_Vincoli di \_ nome OID XCN \_ (2.5.29.30)</span><span class="sxs-lookup"><span data-stu-id="a870b-163">**OID:** XCN\_OID\_NAME\_CONSTRAINTS (2.5.29.30)</span></span>

## <a name="policyconstraints"></a><span data-ttu-id="a870b-164">PolicyConstraints</span><span class="sxs-lookup"><span data-stu-id="a870b-164">PolicyConstraints</span></span>

<span data-ttu-id="a870b-165">L'estensione dei vincoli di criteri viene aggiunta ai certificati della CA per limitare la convalida del percorso proibindo il mapping dei criteri o richiedendo che ogni certificato nella gerarchia contenga un identificatore di criterio accettabile.</span><span class="sxs-lookup"><span data-stu-id="a870b-165">The policy constraints extension is added to CA certificates to constrain path validation by prohibiting policy mapping or by requiring that each certificate in the hierarchy contain an acceptable policy identifier.</span></span>

<span data-ttu-id="a870b-166">**Interfaccia:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="a870b-166">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="a870b-167">**OID:** \_Vincoli dei \_ criteri OID XCN \_ (2.5.29.36)</span><span class="sxs-lookup"><span data-stu-id="a870b-167">**OID:** XCN\_OID\_POLICY\_CONSTRAINTS (2.5.29.36)</span></span>

## <a name="policymappings"></a><span data-ttu-id="a870b-168">PolicyMappings</span><span class="sxs-lookup"><span data-stu-id="a870b-168">PolicyMappings</span></span>

<span data-ttu-id="a870b-169">L'estensione mapping dei criteri viene usata per identificare i criteri in una CA subordinata che corrispondono ai criteri nella CA emittente.</span><span class="sxs-lookup"><span data-stu-id="a870b-169">The policy mappings extension is used to identify the policies in a subordinate CA that correspond to policies in the issuing CA.</span></span> <span data-ttu-id="a870b-170">Il valore dell'estensione contiene una sequenza di autorità di certificazione emittente e mapping dei criteri della CA subordinata rappresentati dagli identificatori di oggetto.</span><span class="sxs-lookup"><span data-stu-id="a870b-170">The extension value contains a sequence of issuing CA and subordinate CA policy mappings represented by object identifiers.</span></span>

<span data-ttu-id="a870b-171">**Interfaccia:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="a870b-171">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="a870b-172">**OID:** \_Mapping dei \_ criteri OID XCN \_ (2.5.29.33)</span><span class="sxs-lookup"><span data-stu-id="a870b-172">**OID:** XCN\_OID\_POLICY\_MAPPINGS (2.5.29.33)</span></span>

## <a name="privatekeyusageperiod"></a><span data-ttu-id="a870b-173">PrivateKeyUsagePeriod</span><span class="sxs-lookup"><span data-stu-id="a870b-173">PrivateKeyUsagePeriod</span></span>

<span data-ttu-id="a870b-174">L'estensione del periodo di utilizzo della chiave privata viene usata per specificare un periodo di validità diverso per la chiave privata rispetto al certificato a cui è associata la chiave.</span><span class="sxs-lookup"><span data-stu-id="a870b-174">The private key usage period extension is used to specify a different validity period for the private key than for the certificate with which the key is associated.</span></span>

<span data-ttu-id="a870b-175">**Interfaccia:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="a870b-175">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="a870b-176">**OID:** XCN \_ OID \_ PRIVATEKEY \_ periodo di utilizzo \_ (2.5.29.16)</span><span class="sxs-lookup"><span data-stu-id="a870b-176">**OID:** XCN\_OID\_PRIVATEKEY\_USAGE\_PERIOD (2.5.29.16)</span></span>

## <a name="smimecapabilities"></a><span data-ttu-id="a870b-177">SmimeCapabilities</span><span class="sxs-lookup"><span data-stu-id="a870b-177">SmimeCapabilities</span></span>

<span data-ttu-id="a870b-178">L'estensione delle funzionalità Secure/Multipurpose Internet Mail Extensions (S/MIME) può essere usata per segnalare le funzionalità di decrittografia di un destinatario di posta elettronica al mittente del messaggio di posta elettronica, in modo che il mittente possa scegliere l'algoritmo di crittografia più sicuro supportato da entrambe le parti.</span><span class="sxs-lookup"><span data-stu-id="a870b-178">The Secure/Multipurpose Internet Mail Extensions (S/MIME) capabilities extension can be used to report an email recipient's decryption capabilities to the sender of the email message so that the sender can choose the most secure encryption algorithm supported by both parties.</span></span> <span data-ttu-id="a870b-179">Il valore dell'estensione contiene una raccolta di algoritmi di crittografia simmetrica OID e un livello di crittografia facoltativo per ciascuno di essi.</span><span class="sxs-lookup"><span data-stu-id="a870b-179">The extension value contains a collection of symmetric encryption algorithm OIDs and an optional encryption strength for each.</span></span>

<span data-ttu-id="a870b-180">**Interfaccia:** [ **IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)</span><span class="sxs-lookup"><span data-stu-id="a870b-180">**Interface:** [**IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)</span></span>

<span data-ttu-id="a870b-181">**OID:** \_OID XCN \_ RSA \_ SMIMECapabilities (1.2.840.113549.1.9.15)</span><span class="sxs-lookup"><span data-stu-id="a870b-181">**OID:** XCN\_OID\_RSA\_SMIMECapabilities (1.2.840.113549.1.9.15)</span></span>

## <a name="subjectdirectoryattributes"></a><span data-ttu-id="a870b-182">SubjectDirectoryAttributes</span><span class="sxs-lookup"><span data-stu-id="a870b-182">SubjectDirectoryAttributes</span></span>

<span data-ttu-id="a870b-183">L'estensione degli attributi della directory oggetto può essere utilizzata per fornire attributi di identificazione, ad esempio la cittadinanza del soggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="a870b-183">The subject directory attributes extension can be used to convey identification attributes such as the nationality of the certificate subject.</span></span> <span data-ttu-id="a870b-184">Il valore dell'estensione è una sequenza di coppie di valori OID.</span><span class="sxs-lookup"><span data-stu-id="a870b-184">The extension value is a sequence of OID-value pairs.</span></span>

<span data-ttu-id="a870b-185">**Interfaccia:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="a870b-185">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="a870b-186">**OID:** XCN \_ \_ oggetto Oid \_ \_ attrs (2.5.29.9)</span><span class="sxs-lookup"><span data-stu-id="a870b-186">**OID:** XCN\_OID\_SUBJECT\_DIR\_ATTRS (2.5.29.9)</span></span>

## <a name="subjectkeyidentifier"></a><span data-ttu-id="a870b-187">SubjectKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="a870b-187">SubjectKeyIdentifier</span></span>

<span data-ttu-id="a870b-188">L'estensione dell'identificatore di chiave del soggetto può essere usata per distinguere tra più chiavi pubbliche utilizzate dal soggetto del certificato.</span><span class="sxs-lookup"><span data-stu-id="a870b-188">The subject key identifier extension can be used to differentiate between multiple public keys held by the certificate subject.</span></span> <span data-ttu-id="a870b-189">Il valore dell'estensione è in genere un hash SHA-1 della chiave.</span><span class="sxs-lookup"><span data-stu-id="a870b-189">The extension value is typically a SHA-1 hash of the key.</span></span>

<span data-ttu-id="a870b-190">**Interfaccia:** [ **IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)</span><span class="sxs-lookup"><span data-stu-id="a870b-190">**Interface:** [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)</span></span>

<span data-ttu-id="a870b-191">**OID:** \_Identificatore di chiave del soggetto XCN OID \_ \_ \_ (2.5.29.14)</span><span class="sxs-lookup"><span data-stu-id="a870b-191">**OID:** XCN\_OID\_SUBJECT\_KEY\_IDENTIFIER (2.5.29.14)</span></span>

## <a name="template"></a><span data-ttu-id="a870b-192">Modello</span><span class="sxs-lookup"><span data-stu-id="a870b-192">Template</span></span>

<span data-ttu-id="a870b-193">L'estensione del modello può essere usata per identificare il modello della versione 2 da usare quando si emette o si rinnova un certificato.</span><span class="sxs-lookup"><span data-stu-id="a870b-193">The template extension can be used to identify the version 2 template to use when issuing or renewing a certificate.</span></span> <span data-ttu-id="a870b-194">Il valore dell'estensione contiene l'OID del modello e le informazioni facoltative sulla versione.</span><span class="sxs-lookup"><span data-stu-id="a870b-194">The extension value contains the template OID and optional version information.</span></span> <span data-ttu-id="a870b-195">L'estensione è specifica di Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a870b-195">The extension is Microsoft specific.</span></span>

<span data-ttu-id="a870b-196">**Interfaccia:** [ **IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)</span><span class="sxs-lookup"><span data-stu-id="a870b-196">**Interface:** [**IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)</span></span>

<span data-ttu-id="a870b-197">**OID:** \_Modello di \_ certificato OID XCN \_ (1.3.6.1.4.1.311.21.7)</span><span class="sxs-lookup"><span data-stu-id="a870b-197">**OID:** XCN\_OID\_CERTIFICATE\_TEMPLATE (1.3.6.1.4.1.311.21.7)</span></span>

## <a name="templatename"></a><span data-ttu-id="a870b-198">TemplateName</span><span class="sxs-lookup"><span data-stu-id="a870b-198">TemplateName</span></span>

<span data-ttu-id="a870b-199">L'estensione del nome del modello può essere usata per identificare il modello della versione 1 da usare quando si emette o si rinnova un certificato.</span><span class="sxs-lookup"><span data-stu-id="a870b-199">The template name extension can be used to identify the version 1 template to use when issuing or renewing a certificate.</span></span> <span data-ttu-id="a870b-200">Il valore dell'estensione contiene il nome del modello.</span><span class="sxs-lookup"><span data-stu-id="a870b-200">The extension value contains the name of the template.</span></span> <span data-ttu-id="a870b-201">L'estensione è specifica di Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a870b-201">The extension is Microsoft specific.</span></span>

<span data-ttu-id="a870b-202">**Interfaccia:** [ **IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)</span><span class="sxs-lookup"><span data-stu-id="a870b-202">**Interface:** [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)</span></span>

<span data-ttu-id="a870b-203">**OID:** XCN \_ OID \_ registrazione \_ \_ estensione tipo certificato (1.3.6.1.4.1.311.20.2)</span><span class="sxs-lookup"><span data-stu-id="a870b-203">**OID:** XCN\_OID\_ENROLL\_CERTTYPE\_EXTENSION (1.3.6.1.4.1.311.20.2)</span></span>

## <a name="related-topics"></a><span data-ttu-id="a870b-204">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a870b-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a870b-205">Estensioni</span><span class="sxs-lookup"><span data-stu-id="a870b-205">Extensions</span></span>](extensions.md)
</dt> </dl>

 

 




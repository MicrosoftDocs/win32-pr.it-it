---
title: Proprietà del metodo EAP (Eaptypes. h)
description: Usato dai supplicant e dagli autenticatori per determinare i metodi EAP da usare con un supplicant o un autenticatore specifico. Le proprietà del metodo specificano inoltre la configurazione di un metodo.
ms.assetid: 10407b85-5d2c-4c75-9b65-a0d65d4cc7ab
topic_type:
- apiref
api_name:
- eapPropCipherSuiteNegotiation
- eapPropMutualAuth
- eapPropIntegrity
- eapPropReplayProtection
- eapPropConfidentiality
- eapPropKeyDerivation
- eapPropKeyStrength64
- eapPropKeyStrength128
- eapPropKeyStrength256
- eapPropKeyStrength512
- eapPropKeyStrength1024
- eapPropDictionaryAttackResistance
- eapPropFastReconnect
- eapPropCryptoBinding
- eapPropSessionIndependence
- eapPropFragmentation
- eapPropChannelBinding
- eapPropNap
- eapPropStandalone
- eapPropMppeEncryption
- eapPropTunnelMethod
- eapPropSupportsConfig
- eapPropCertifiedMethod
- eapPropmachineAuth
- eapPropUserAuth
- eapPropIdentityPrivacy
- eapPropMethodChaining
- eapPropSharedStateEquivalence
- eapPropReserved
api_location:
- eaptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 844f897456ee21dfa93dfaa5b16b4f218ba5efb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741847"
---
# <a name="eap-method-properties"></a><span data-ttu-id="40d87-104">Proprietà del metodo EAP</span><span class="sxs-lookup"><span data-stu-id="40d87-104">EAP Method Properties</span></span>

<span data-ttu-id="40d87-105">Usato dai supplicant e dagli autenticatori per determinare i metodi EAP da usare con un supplicant o un autenticatore specifico.</span><span class="sxs-lookup"><span data-stu-id="40d87-105">Used by supplicants and authenticators to determine the EAP methods to be used with a given supplicant or authenticator.</span></span> <span data-ttu-id="40d87-106">Le proprietà del metodo specificano inoltre la configurazione di un metodo.</span><span class="sxs-lookup"><span data-stu-id="40d87-106">Method properties also specify the configuration of a method.</span></span>

<span data-ttu-id="40d87-107">Ad esempio, il richiedente [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) può richiedere metodi per avere determinate proprietà da usare con il supplicant [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="40d87-107">For example, the [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) supplicant may require methods to have certain properties for use with the [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) supplicant.</span></span> <span data-ttu-id="40d87-108">Il materiale delle chiavi, ad esempio, è un requisito.</span><span class="sxs-lookup"><span data-stu-id="40d87-108">Keying material, for example, is a requirement.</span></span>

<span data-ttu-id="40d87-109">Sono elencate le proprietà supportate dai metodi EAP.</span><span class="sxs-lookup"><span data-stu-id="40d87-109">The properties supported by EAP methods are listed.</span></span> <span data-ttu-id="40d87-110">Le proprietà vengono archiviate come valori della chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="40d87-110">Properties are stored as registry key values.</span></span> <span data-ttu-id="40d87-111">Per ulteriori informazioni, vedere la sezione relativa alla chiave del registro di sistema della DLL del metodo peer EAP nell'argomento [configurazione del registro di sistema per i metodi EAP.](registry-keys-for-eap-methods.md)</span><span class="sxs-lookup"><span data-stu-id="40d87-111">For more information, see the EAP Peer Method DLL Registry Key section of the topic [Registry Configuration for EAP Methods.](registry-keys-for-eap-methods.md)</span></span>

<dl> <dt>

<span data-ttu-id="40d87-112"><span id="eapPropCipherSuiteNegotiation"></span><span id="eappropciphersuitenegotiation"></span><span id="EAPPROPCIPHERSUITENEGOTIATION"></span>**eapPropCipherSuiteNegotiation**</span><span class="sxs-lookup"><span data-stu-id="40d87-112"><span id="eapPropCipherSuiteNegotiation"></span><span id="eappropciphersuitenegotiation"></span><span id="EAPPROPCIPHERSUITENEGOTIATION"></span>**eapPropCipherSuiteNegotiation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d87-113">0x00000001</span><span class="sxs-lookup"><span data-stu-id="40d87-113">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="40d87-114">Il metodo consente la negoziazione del pacchetto di crittografia ai fini della crittografia dei dati.</span><span class="sxs-lookup"><span data-stu-id="40d87-114">The method allows the cipher suite to be negotiated for the purpose of data encryption.</span></span> <span data-ttu-id="40d87-115">Windows Server 2008 supporta i pacchetti di [crittografia](/windows/desktop/SecAuthN/tls-cipher-suites)3DES seguenti:</span><span class="sxs-lookup"><span data-stu-id="40d87-115">Windows Server 2008 supports the following 3DES [cipher suites](/windows/desktop/SecAuthN/tls-cipher-suites):</span></span>

-   <span data-ttu-id="40d87-116">\_Sha RSA \_ con \_ 3DES \_ Ede \_ \_ (TLS & SSL 3)</span><span class="sxs-lookup"><span data-stu-id="40d87-116">TLS\_RSA\_WITH\_3DES\_EDE\_CBC\_SHA (TLS & SSL 3)</span></span>
-   <span data-ttu-id="40d87-117">TLS \_ dhe \_ DSS \_ with \_ 3DES \_ EDE \_ CBC \_ SHA (TLS & SSL 3)</span><span class="sxs-lookup"><span data-stu-id="40d87-117">TLS\_DHE\_DSS\_WITH\_3DES\_EDE\_CBC\_SHA (TLS & SSL 3)</span></span>
-   <span data-ttu-id="40d87-118">SSL \_ CK \_ des \_ 192 \_ EDE3 \_ CBC \_ con \_ MD5 (SSL 2 se abilitato)</span><span class="sxs-lookup"><span data-stu-id="40d87-118">SSL\_CK\_DES\_192\_EDE3\_CBC\_WITH\_MD5 (SSL 2 if enabled)</span></span>

<span data-ttu-id="40d87-119">Per ulteriori informazioni sul protocollo di sicurezza TLS 1,0, vedere [RFC 2246](https://go.microsoft.com/fwlink/p/?linkid=84035).</span><span class="sxs-lookup"><span data-stu-id="40d87-119">For more information about the TLS 1.0 security protocol, see [RFC 2246](https://go.microsoft.com/fwlink/p/?linkid=84035).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40d87-120"><span id="eapPropMutualAuth"></span><span id="eappropmutualauth"></span><span id="EAPPROPMUTUALAUTH"></span>**eapPropMutualAuth**</span><span class="sxs-lookup"><span data-stu-id="40d87-120"><span id="eapPropMutualAuth"></span><span id="eappropmutualauth"></span><span id="EAPPROPMUTUALAUTH"></span>**eapPropMutualAuth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d87-121">0x00000002</span><span class="sxs-lookup"><span data-stu-id="40d87-121">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="40d87-122">Il metodo fornisce uno scambio, in cui l'autenticatore autentica il peer e viceversa.</span><span class="sxs-lookup"><span data-stu-id="40d87-122">The method provides an exchange, in which the authenticator authenticates the peer and vice versa.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40d87-123"><span id="eapPropIntegrity"></span><span id="eappropintegrity"></span><span id="EAPPROPINTEGRITY"></span>**eapPropIntegrity**</span><span class="sxs-lookup"><span data-stu-id="40d87-123"><span id="eapPropIntegrity"></span><span id="eappropintegrity"></span><span id="EAPPROPINTEGRITY"></span>**eapPropIntegrity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d87-124">0x00000004</span><span class="sxs-lookup"><span data-stu-id="40d87-124">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="40d87-125">Il metodo fornisce l'autenticazione e la protezione dell'origine dati contro la modifica non autorizzata delle informazioni per i pacchetti EAP, incluse le richieste e le risposte EAP.</span><span class="sxs-lookup"><span data-stu-id="40d87-125">The method provides data origin authentication and protection against unauthorized modification of information for EAP packets, including EAP requests and responses.</span></span> <span data-ttu-id="40d87-126">Quando si esegue questa attestazione, una specifica del metodo deve specificare i pacchetti EAP protetti e i campi protetti all'interno dei pacchetti EAP.</span><span class="sxs-lookup"><span data-stu-id="40d87-126">When making this claim, a method specification must specify the protected EAP packets and protected fields within EAP packets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40d87-127"><span id="eapPropReplayProtection"></span><span id="eappropreplayprotection"></span><span id="EAPPROPREPLAYPROTECTION"></span>**eapPropReplayProtection**</span><span class="sxs-lookup"><span data-stu-id="40d87-127"><span id="eapPropReplayProtection"></span><span id="eappropreplayprotection"></span><span id="EAPPROPREPLAYPROTECTION"></span>**eapPropReplayProtection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d87-128">0x00000008</span><span class="sxs-lookup"><span data-stu-id="40d87-128">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="40d87-129">Il metodo può proteggersi dalla riproduzione di un metodo EAP o dei relativi messaggi.</span><span class="sxs-lookup"><span data-stu-id="40d87-129">The method can protect against replay of an EAP method or its messages.</span></span> <span data-ttu-id="40d87-130">Impossibile riprodurre le indicazioni relative al risultato dell'esito positivo e negativo.</span><span class="sxs-lookup"><span data-stu-id="40d87-130">Success and failure result indications cannot be replayed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40d87-131"><span id="eapPropConfidentiality"></span><span id="eappropconfidentiality"></span><span id="EAPPROPCONFIDENTIALITY"></span>**eapPropConfidentiality**</span><span class="sxs-lookup"><span data-stu-id="40d87-131"><span id="eapPropConfidentiality"></span><span id="eappropconfidentiality"></span><span id="EAPPROPCONFIDENTIALITY"></span>**eapPropConfidentiality**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d87-132">0x00000010</span><span class="sxs-lookup"><span data-stu-id="40d87-132">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="40d87-133">Il metodo può crittografare i messaggi EAP.</span><span class="sxs-lookup"><span data-stu-id="40d87-133">The method can encrypt EAP messages.</span></span> <span data-ttu-id="40d87-134">Le richieste EAP, le risposte EAP, le indicazioni relative al risultato dell'esito positivo e l'errore vengono crittografate.</span><span class="sxs-lookup"><span data-stu-id="40d87-134">EAP requests, EAP responses, success result indications, and failure result indications are encrypted.</span></span> <span data-ttu-id="40d87-135">Un metodo che rende questa attestazione deve supportare Identity Protection.</span><span class="sxs-lookup"><span data-stu-id="40d87-135">A method making this claim must support identity protection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40d87-136"><span id="eapPropKeyDerivation"></span><span id="eappropkeyderivation"></span><span id="EAPPROPKEYDERIVATION"></span>**eapPropKeyDerivation**</span><span class="sxs-lookup"><span data-stu-id="40d87-136"><span id="eapPropKeyDerivation"></span><span id="eappropkeyderivation"></span><span id="EAPPROPKEYDERIVATION"></span>**eapPropKeyDerivation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d87-137">0x00000020</span><span class="sxs-lookup"><span data-stu-id="40d87-137">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="40d87-138">Il metodo può derivare il materiale delle chiavi esportabili, ad esempio la chiave della sessione master (MSK) e la chiave della sessione master estesa (EMSK).</span><span class="sxs-lookup"><span data-stu-id="40d87-138">The method can derive exportable keying material, such as the Master Session Key (MSK) and the Extended Master Session Key (EMSK).</span></span> <span data-ttu-id="40d87-139">Il MSK viene utilizzato solo per ulteriori derivazioni delle chiavi, non direttamente per la protezione della conversazione EAP o dei dati successivi.</span><span class="sxs-lookup"><span data-stu-id="40d87-139">The MSK is used only for further key derivation, not directly for protection of the EAP conversation or subsequent data.</span></span> <span data-ttu-id="40d87-140">L'uso di EMSK è riservato.</span><span class="sxs-lookup"><span data-stu-id="40d87-140">Use of the EMSK is reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40d87-141"><span id="eapPropKeyStrength64"></span><span id="eappropkeystrength64"></span><span id="EAPPROPKEYSTRENGTH64"></span>**eapPropKeyStrength64**</span><span class="sxs-lookup"><span data-stu-id="40d87-141"><span id="eapPropKeyStrength64"></span><span id="eappropkeystrength64"></span><span id="EAPPROPKEYSTRENGTH64"></span>**eapPropKeyStrength64**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d87-142">0x00000040</span><span class="sxs-lookup"><span data-stu-id="40d87-142">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="40d87-143">La lunghezza minima della chiave supportata dal metodo EAP è 64 bit.</span><span class="sxs-lookup"><span data-stu-id="40d87-143">The minimum key length supported by the EAP method is 64 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40d87-144"><span id="eapPropKeyStrength128"></span><span id="eappropkeystrength128"></span><span id="EAPPROPKEYSTRENGTH128"></span>**eapPropKeyStrength128**</span><span class="sxs-lookup"><span data-stu-id="40d87-144"><span id="eapPropKeyStrength128"></span><span id="eappropkeystrength128"></span><span id="EAPPROPKEYSTRENGTH128"></span>**eapPropKeyStrength128**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d87-145">0x00000080</span><span class="sxs-lookup"><span data-stu-id="40d87-145">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="40d87-146">La lunghezza minima della chiave supportata dal metodo EAP è 128 bit.</span><span class="sxs-lookup"><span data-stu-id="40d87-146">The minimum key length supported by the EAP method is 128 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40d87-147"><span id="eapPropKeyStrength256"></span><span id="eappropkeystrength256"></span><span id="EAPPROPKEYSTRENGTH256"></span>**eapPropKeyStrength256**</span><span class="sxs-lookup"><span data-stu-id="40d87-147"><span id="eapPropKeyStrength256"></span><span id="eappropkeystrength256"></span><span id="EAPPROPKEYSTRENGTH256"></span>**eapPropKeyStrength256**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d87-148">0x00000100</span><span class="sxs-lookup"><span data-stu-id="40d87-148">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="40d87-149">La lunghezza minima della chiave supportata dal metodo EAP è 256 bit.</span><span class="sxs-lookup"><span data-stu-id="40d87-149">The minimum key length supported by the EAP method is 256 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40d87-150"><span id="eapPropKeyStrength512"></span><span id="eappropkeystrength512"></span><span id="EAPPROPKEYSTRENGTH512"></span>**eapPropKeyStrength512**</span><span class="sxs-lookup"><span data-stu-id="40d87-150"><span id="eapPropKeyStrength512"></span><span id="eappropkeystrength512"></span><span id="EAPPROPKEYSTRENGTH512"></span>**eapPropKeyStrength512**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d87-151">0x00000200</span><span class="sxs-lookup"><span data-stu-id="40d87-151">0x00000200</span></span>
</dt> <dt>



<span data-ttu-id="40d87-152">La lunghezza minima della chiave supportata dal metodo EAP è 512 bit.</span><span class="sxs-lookup"><span data-stu-id="40d87-152">The minimum key length supported by the EAP method is 512 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40d87-153"><span id="eapPropKeyStrength1024"></span><span id="eappropkeystrength1024"></span><span id="EAPPROPKEYSTRENGTH1024"></span>**eapPropKeyStrength1024**</span><span class="sxs-lookup"><span data-stu-id="40d87-153"><span id="eapPropKeyStrength1024"></span><span id="eappropkeystrength1024"></span><span id="EAPPROPKEYSTRENGTH1024"></span>**eapPropKeyStrength1024**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d87-154">0x00000400</span><span class="sxs-lookup"><span data-stu-id="40d87-154">0x00000400</span></span>
</dt> <dt>



<span data-ttu-id="40d87-155">La lunghezza minima della chiave supportata dal metodo EAP è 1024 bit.</span><span class="sxs-lookup"><span data-stu-id="40d87-155">The minimum key length supported by the EAP method is 1024 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40d87-156"><span id="eapPropDictionaryAttackResistance"></span><span id="eappropdictionaryattackresistance"></span><span id="EAPPROPDICTIONARYATTACKRESISTANCE"></span>**eapPropDictionaryAttackResistance**</span><span class="sxs-lookup"><span data-stu-id="40d87-156"><span id="eapPropDictionaryAttackResistance"></span><span id="eappropdictionaryattackresistance"></span><span id="EAPPROPDICTIONARYATTACKRESISTANCE"></span>**eapPropDictionaryAttackResistance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d87-157">0x00000800</span><span class="sxs-lookup"><span data-stu-id="40d87-157">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="40d87-158">Il metodo non consente un attacco offline che ha un fattore di lavoro basato sul numero di password nel dizionario di un utente malintenzionato.</span><span class="sxs-lookup"><span data-stu-id="40d87-158">The method does not allow an offline attack that has a work factor based on the number of passwords in an attacker's dictionary.</span></span> <span data-ttu-id="40d87-159">Quando si usa l'autenticazione della password, le password vengono generalmente selezionate da un set di piccole dimensioni (rispetto a un set di chiavi a N bit), che genera un problema per gli attacchi con dizionario.</span><span class="sxs-lookup"><span data-stu-id="40d87-159">Where password authentication is used, passwords are commonly selected from a small set (as compared to a set of N-bit keys), which raises a concern about dictionary attacks.</span></span> <span data-ttu-id="40d87-160">È possibile che un metodo fornisca la protezione contro gli attacchi del dizionario se, quando usa una password come segreto, il metodo non consente un attacco offline che ha un fattore di lavoro basato sul numero di password nel dizionario di un utente malintenzionato.</span><span class="sxs-lookup"><span data-stu-id="40d87-160">A method may be said to provide protection against dictionary attacks if, when it uses a password as a secret, the method does not allow an offline attack that has a work factor based on the number of passwords in an attacker's dictionary.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40d87-161"><span id="eapPropFastReconnect"></span><span id="eappropfastreconnect"></span><span id="EAPPROPFASTRECONNECT"></span>**eapPropFastReconnect**</span><span class="sxs-lookup"><span data-stu-id="40d87-161"><span id="eapPropFastReconnect"></span><span id="eappropfastreconnect"></span><span id="EAPPROPFASTRECONNECT"></span>**eapPropFastReconnect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d87-162">0x00001000</span><span class="sxs-lookup"><span data-stu-id="40d87-162">0x00001000</span></span>
</dt> <dt>



<span data-ttu-id="40d87-163">Il metodo ha la possibilità, nel caso in cui sia stata stabilita un'associazione di sicurezza in precedenza, per creare un'associazione di sicurezza nuova o aggiornata in modo più efficiente o con un numero minore di round trip.</span><span class="sxs-lookup"><span data-stu-id="40d87-163">The method has the ability, in the case where a security association has been previously established, to create a new or refreshed security association more efficiently or in a smaller number of round-trips.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40d87-164"><span id="eapPropCryptoBinding"></span><span id="eappropcryptobinding"></span><span id="EAPPROPCRYPTOBINDING"></span>**eapPropCryptoBinding**</span><span class="sxs-lookup"><span data-stu-id="40d87-164"><span id="eapPropCryptoBinding"></span><span id="eappropcryptobinding"></span><span id="EAPPROPCRYPTOBINDING"></span>**eapPropCryptoBinding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d87-165">0x00002000</span><span class="sxs-lookup"><span data-stu-id="40d87-165">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="40d87-166">Il metodo dimostra al server EAP che una singola entità ha agito come peer EAP per tutti i metodi eseguiti in un metodo di tunneling.</span><span class="sxs-lookup"><span data-stu-id="40d87-166">The method demonstrates to the EAP server that a single entity has acted as the EAP peer for all methods executed within a tunnel method.</span></span> <span data-ttu-id="40d87-167">Il binding può inoltre implicare che il server EAP dimostri al peer che una singola entità ha agito come server EAP per tutti i metodi eseguiti in un metodo di tunneling.</span><span class="sxs-lookup"><span data-stu-id="40d87-167">Binding may also imply that the EAP server demonstrates to the peer that a single entity has acted as the EAP server for all methods executed within a tunnel method.</span></span> <span data-ttu-id="40d87-168">Se eseguita correttamente, l'associazione serve a mitigare le vulnerabilità man-in-the-Middle.</span><span class="sxs-lookup"><span data-stu-id="40d87-168">If executed correctly, binding serves to mitigate man-in-the-middle vulnerabilities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40d87-169"><span id="eapPropSessionIndependence"></span><span id="eappropsessionindependence"></span><span id="EAPPROPSESSIONINDEPENDENCE"></span>**eapPropSessionIndependence**</span><span class="sxs-lookup"><span data-stu-id="40d87-169"><span id="eapPropSessionIndependence"></span><span id="eappropsessionindependence"></span><span id="EAPPROPSESSIONINDEPENDENCE"></span>**eapPropSessionIndependence**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d87-170">0x00004000</span><span class="sxs-lookup"><span data-stu-id="40d87-170">0x00004000</span></span>
</dt> <dt>



<span data-ttu-id="40d87-171">Il metodo dimostra che gli attacchi passivi, ad esempio l'acquisizione della conversazione EAP, o gli attacchi attivi (inclusa la compromissione di MSK o EMSK) non compromettono i MSKs o EMSKs successivi o precedenti.</span><span class="sxs-lookup"><span data-stu-id="40d87-171">The method demonstrates that passive attacks (such as capture of the EAP conversation) or active attacks (including compromise of the MSK or EMSK) do not compromise subsequent or prior MSKs or EMSKs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40d87-172"><span id="eapPropFragmentation"></span><span id="eappropfragmentation"></span><span id="EAPPROPFRAGMENTATION"></span>**eapPropFragmentation**</span><span class="sxs-lookup"><span data-stu-id="40d87-172"><span id="eapPropFragmentation"></span><span id="eappropfragmentation"></span><span id="EAPPROPFRAGMENTATION"></span>**eapPropFragmentation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d87-173">0x00008000</span><span class="sxs-lookup"><span data-stu-id="40d87-173">0x00008000</span></span>
</dt> <dt>



<span data-ttu-id="40d87-174">Il metodo può supportare la frammentazione e il riassemblaggio se i pacchetti EAP superano la MTU minima (unità di trasmissione massima) di 1020 ottetti.</span><span class="sxs-lookup"><span data-stu-id="40d87-174">The method can support fragmentation and reassembly if EAP packets exceed the minimum MTU (maximum transmission unit) of 1020 octets.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40d87-175"><span id="eapPropChannelBinding"></span><span id="eappropchannelbinding"></span><span id="EAPPROPCHANNELBINDING"></span>**eapPropChannelBinding**</span><span class="sxs-lookup"><span data-stu-id="40d87-175"><span id="eapPropChannelBinding"></span><span id="eappropchannelbinding"></span><span id="EAPPROPCHANNELBINDING"></span>**eapPropChannelBinding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d87-176">0x00010000</span><span class="sxs-lookup"><span data-stu-id="40d87-176">0x00010000</span></span>
</dt> <dt>



<span data-ttu-id="40d87-177">Il metodo può comunicare proprietà del canale protette dall'integrità, ad esempio identificatori di endpoint, che possono essere confrontati con i valori comunicati usando meccanismi fuori banda, ad esempio [autenticazione, autorizzazione e accounting](https://go.microsoft.com/fwlink/p/?linkid=84063) (AAA) o il protocollo di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="40d87-177">The method can communicate integrity-protected channel properties, such as endpoint identifiers, which can be compared to values communicated using out of band mechanisms - such as an [Authentication, Authorization, and Accounting](https://go.microsoft.com/fwlink/p/?linkid=84063) (AAA) or the lower layer protocol.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40d87-178"><span id="eapPropNap"></span><span id="eappropnap"></span><span id="EAPPROPNAP"></span>**eapPropNap**</span><span class="sxs-lookup"><span data-stu-id="40d87-178"><span id="eapPropNap"></span><span id="eappropnap"></span><span id="EAPPROPNAP"></span>**eapPropNap**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="40d87-179">0x00020000</span><span class="sxs-lookup"><span data-stu-id="40d87-179">0x00020000</span></span>
</dt> <dt>



<span data-ttu-id="40d87-180">Il metodo supporta protezione accesso alla rete (NAP).</span><span class="sxs-lookup"><span data-stu-id="40d87-180">The method supports Network Access Protection (NAP).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40d87-181"><span id="eapPropStandalone"></span><span id="eappropstandalone"></span><span id="EAPPROPSTANDALONE"></span>**eapPropStandalone**</span><span class="sxs-lookup"><span data-stu-id="40d87-181"><span id="eapPropStandalone"></span><span id="eappropstandalone"></span><span id="EAPPROPSTANDALONE"></span>**eapPropStandalone**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d87-182">0x00040000</span><span class="sxs-lookup"><span data-stu-id="40d87-182">0x00040000</span></span>
</dt> <dt>



<span data-ttu-id="40d87-183">Il metodo può essere usato in un computer autonomo.</span><span class="sxs-lookup"><span data-stu-id="40d87-183">The method can be used on a standalone machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40d87-184"><span id="eapPropMppeEncryption"></span><span id="eappropmppeencryption"></span><span id="EAPPROPMPPEENCRYPTION"></span>**eapPropMppeEncryption**</span><span class="sxs-lookup"><span data-stu-id="40d87-184"><span id="eapPropMppeEncryption"></span><span id="eappropmppeencryption"></span><span id="EAPPROPMPPEENCRYPTION"></span>**eapPropMppeEncryption**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="40d87-185">0x00080000</span><span class="sxs-lookup"><span data-stu-id="40d87-185">0x00080000</span></span>
</dt> <dt>



<span data-ttu-id="40d87-186">Il metodo supporta la crittografia del [protocollo Microsoft Point-to-Point Encryption (MPPE)](https://go.microsoft.com/fwlink/p/?linkid=83915) .</span><span class="sxs-lookup"><span data-stu-id="40d87-186">The method supports [Microsoft Point-to-Point Encryption (MPPE) protocol](https://go.microsoft.com/fwlink/p/?linkid=83915) encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40d87-187"><span id="eapPropTunnelMethod"></span><span id="eapproptunnelmethod"></span><span id="EAPPROPTUNNELMETHOD"></span>**eapPropTunnelMethod**</span><span class="sxs-lookup"><span data-stu-id="40d87-187"><span id="eapPropTunnelMethod"></span><span id="eapproptunnelmethod"></span><span id="EAPPROPTUNNELMETHOD"></span>**eapPropTunnelMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d87-188">0x00100000</span><span class="sxs-lookup"><span data-stu-id="40d87-188">0x00100000</span></span>
</dt> <dt>



<span data-ttu-id="40d87-189">Il metodo supporta il tunneling di altri metodi EAP.</span><span class="sxs-lookup"><span data-stu-id="40d87-189">The method supports tunneling of other EAP methods.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40d87-190"><span id="eapPropSupportsConfig"></span><span id="eappropsupportsconfig"></span><span id="EAPPROPSUPPORTSCONFIG"></span>**eapPropSupportsConfig**</span><span class="sxs-lookup"><span data-stu-id="40d87-190"><span id="eapPropSupportsConfig"></span><span id="eappropsupportsconfig"></span><span id="EAPPROPSUPPORTSCONFIG"></span>**eapPropSupportsConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d87-191">0x00200000</span><span class="sxs-lookup"><span data-stu-id="40d87-191">0x00200000</span></span>
</dt> <dt>



<span data-ttu-id="40d87-192">Il metodo supporta le proprietà configurabili e dispone di un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="40d87-192">The method supports configurable properties, and has a user interface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40d87-193"><span id="eapPropCertifiedMethod"></span><span id="eappropcertifiedmethod"></span><span id="EAPPROPCERTIFIEDMETHOD"></span>**eapPropCertifiedMethod**</span><span class="sxs-lookup"><span data-stu-id="40d87-193"><span id="eapPropCertifiedMethod"></span><span id="eappropcertifiedmethod"></span><span id="EAPPROPCERTIFIEDMETHOD"></span>**eapPropCertifiedMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d87-194">0x00400000</span><span class="sxs-lookup"><span data-stu-id="40d87-194">0x00400000</span></span>
</dt> <dt>



<span data-ttu-id="40d87-195">Il metodo è stato certificato dal programma di certificazione EAP.</span><span class="sxs-lookup"><span data-stu-id="40d87-195">The method was certified by the EAP Certification Program.</span></span> <span data-ttu-id="40d87-196">Questo bit deve essere inviato solo dai metodi EAP che hanno superato la certificazione.</span><span class="sxs-lookup"><span data-stu-id="40d87-196">This bit should only be sent by EAP methods that have passed certification.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40d87-197"><span id="eapPropmachineAuth"></span><span id="eappropmachineauth"></span><span id="EAPPROPMACHINEAUTH"></span>**eapPropmachineAuth**</span><span class="sxs-lookup"><span data-stu-id="40d87-197"><span id="eapPropmachineAuth"></span><span id="eappropmachineauth"></span><span id="EAPPROPMACHINEAUTH"></span>**eapPropmachineAuth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d87-198">0x01000000</span><span class="sxs-lookup"><span data-stu-id="40d87-198">0x01000000</span></span>
</dt> <dt>



<span data-ttu-id="40d87-199">Windows 7 o versioni successive: il metodo può essere usato per autenticare un computer in una rete usando le credenziali dei computer.</span><span class="sxs-lookup"><span data-stu-id="40d87-199">Windows 7 or later: The method can be used to authenticate a machine on to a network using the machines credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40d87-200"><span id="eapPropUserAuth"></span><span id="eappropuserauth"></span><span id="EAPPROPUSERAUTH"></span>**eapPropUserAuth**</span><span class="sxs-lookup"><span data-stu-id="40d87-200"><span id="eapPropUserAuth"></span><span id="eappropuserauth"></span><span id="EAPPROPUSERAUTH"></span>**eapPropUserAuth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d87-201">0x02000000</span><span class="sxs-lookup"><span data-stu-id="40d87-201">0x02000000</span></span>
</dt> <dt>



<span data-ttu-id="40d87-202">Windows 7 o versioni successive: il metodo può essere usato per autenticare un utente in una rete usando le credenziali degli utenti.</span><span class="sxs-lookup"><span data-stu-id="40d87-202">Windows 7 or later: The method can be used to authenticate a user on to a network using the users credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40d87-203"><span id="eapPropIdentityPrivacy"></span><span id="eappropidentityprivacy"></span><span id="EAPPROPIDENTITYPRIVACY"></span>**eapPropIdentityPrivacy**</span><span class="sxs-lookup"><span data-stu-id="40d87-203"><span id="eapPropIdentityPrivacy"></span><span id="eappropidentityprivacy"></span><span id="EAPPROPIDENTITYPRIVACY"></span>**eapPropIdentityPrivacy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d87-204">0x04000000</span><span class="sxs-lookup"><span data-stu-id="40d87-204">0x04000000</span></span>
</dt> <dt>



<span data-ttu-id="40d87-205">Windows 7 o versioni successive: il metodo supporta l'invio dell'identità utente in un canale protetto.</span><span class="sxs-lookup"><span data-stu-id="40d87-205">Windows 7 or later: The method supports sending the user identity in a protected channel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40d87-206"><span id="eapPropMethodChaining"></span><span id="eappropmethodchaining"></span><span id="EAPPROPMETHODCHAINING"></span>**eapPropMethodChaining**</span><span class="sxs-lookup"><span data-stu-id="40d87-206"><span id="eapPropMethodChaining"></span><span id="eappropmethodchaining"></span><span id="EAPPROPMETHODCHAINING"></span>**eapPropMethodChaining**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d87-207">0x08000000</span><span class="sxs-lookup"><span data-stu-id="40d87-207">0x08000000</span></span>
</dt> <dt>



<span data-ttu-id="40d87-208">Windows 7 o versioni successive: il metodo è un metodo con tunneling e supporta il concatenamento di metodi EAP all'interno del tunnel.</span><span class="sxs-lookup"><span data-stu-id="40d87-208">Windows 7 or later: The method is a tunnelled method and supports EAP method chaining within the tunnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40d87-209"><span id="eapPropSharedStateEquivalence"></span><span id="eappropsharedstateequivalence"></span><span id="EAPPROPSHAREDSTATEEQUIVALENCE"></span>**eapPropSharedStateEquivalence**</span><span class="sxs-lookup"><span data-stu-id="40d87-209"><span id="eapPropSharedStateEquivalence"></span><span id="eappropsharedstateequivalence"></span><span id="EAPPROPSHAREDSTATEEQUIVALENCE"></span>**eapPropSharedStateEquivalence**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d87-210">0x10000000</span><span class="sxs-lookup"><span data-stu-id="40d87-210">0x10000000</span></span>
</dt> <dt>



<span data-ttu-id="40d87-211">Windows 7 o versioni successive: il metodo supporta l'equivalenza dello stato condiviso come definito nella [specifica RFC 4017](https://go.microsoft.com/fwlink/p/?linkid=90455).</span><span class="sxs-lookup"><span data-stu-id="40d87-211">Windows 7 or later: The method supports shared state equivalence as defined in [RFC 4017](https://go.microsoft.com/fwlink/p/?linkid=90455).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="40d87-212"><span id="eapPropReserved"></span><span id="eappropreserved"></span><span id="EAPPROPRESERVED"></span>**eapPropReserved**</span><span class="sxs-lookup"><span data-stu-id="40d87-212"><span id="eapPropReserved"></span><span id="eappropreserved"></span><span id="EAPPROPRESERVED"></span>**eapPropReserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40d87-213">0x80000000</span><span class="sxs-lookup"><span data-stu-id="40d87-213">0x80000000</span></span>
</dt> <dt>



<span data-ttu-id="40d87-214">Riservato.</span><span class="sxs-lookup"><span data-stu-id="40d87-214">Reserved.</span></span> <span data-ttu-id="40d87-215">Non usato.</span><span class="sxs-lookup"><span data-stu-id="40d87-215">Not used.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="40d87-216">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40d87-216">Requirements</span></span>



| <span data-ttu-id="40d87-217">Requisito</span><span class="sxs-lookup"><span data-stu-id="40d87-217">Requirement</span></span> | <span data-ttu-id="40d87-218">Valore</span><span class="sxs-lookup"><span data-stu-id="40d87-218">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="40d87-219">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40d87-219">Minimum supported client</span></span><br/> | <span data-ttu-id="40d87-220">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="40d87-220">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="40d87-221">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40d87-221">Minimum supported server</span></span><br/> | <span data-ttu-id="40d87-222">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="40d87-222">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="40d87-223">Intestazione</span><span class="sxs-lookup"><span data-stu-id="40d87-223">Header</span></span><br/>                   | <dl> <span data-ttu-id="40d87-224"><dt>Eaptypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="40d87-224"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40d87-225">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40d87-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40d87-226">Chiavi del registro di sistema per i metodi EAP</span><span class="sxs-lookup"><span data-stu-id="40d87-226">Registry Keys for EAP Methods</span></span>](registry-keys-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="40d87-227">Costanti EAPHost comuni</span><span class="sxs-lookup"><span data-stu-id="40d87-227">Common EAPHost Constants</span></span>](common-eap-host-error-constants.md)
</dt> </dl>


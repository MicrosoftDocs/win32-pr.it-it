---
title: Domande frequenti generali
description: Leggi le risposte alle domande frequenti sulle API EAPHost, ad esempio "Qual è la durata di un'autenticazione?".
ms.assetid: 4025e8da-8cb1-477b-86bb-7756d9636224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eb0dd9b3b997d8682c3cab1ba91afc3ee2db7ba
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/18/2020
ms.locfileid: "106300718"
---
# <a name="general-frequently-asked-questions"></a><span data-ttu-id="b36c4-103">Domande frequenti generali</span><span class="sxs-lookup"><span data-stu-id="b36c4-103">General Frequently Asked Questions</span></span>

<span data-ttu-id="b36c4-104">Nell'argomento seguente vengono fornite le risposte alle domande frequenti sulle API EAPHost.</span><span class="sxs-lookup"><span data-stu-id="b36c4-104">The following topic provides answers to commonly-asked questions about the EAPHost APIs.</span></span>

### <a name="general-frequently-asked-questions"></a><span data-ttu-id="b36c4-105">Domande frequenti generali</span><span class="sxs-lookup"><span data-stu-id="b36c4-105">General Frequently Asked Questions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b36c4-106">Domanda</span><span class="sxs-lookup"><span data-stu-id="b36c4-106">Question</span></span></th>
<th><span data-ttu-id="b36c4-107">Risposta</span><span class="sxs-lookup"><span data-stu-id="b36c4-107">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b36c4-108">Che cos'è un supplicant?</span><span class="sxs-lookup"><span data-stu-id="b36c4-108">What is a supplicant?</span></span></td>
<td><span data-ttu-id="b36c4-109">Il supplicant è l'entità da autenticare usando EAPHost.</span><span class="sxs-lookup"><span data-stu-id="b36c4-109">The supplicant is the entity to be authenticated using EAPHost.</span></span> <span data-ttu-id="b36c4-110">I supplicant tipici sono client [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) , client 802,3 e servizio Routing e accesso remoto (RRAS), client Point-to-Point (PPP).</span><span class="sxs-lookup"><span data-stu-id="b36c4-110">Typical supplicants are [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) clients, 802.3 clients, and Routing and Remote Access Service (RRAS), Point-to-Point (PPP) clients.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b36c4-111">Che cos'è un peer?</span><span class="sxs-lookup"><span data-stu-id="b36c4-111">What is a peer?</span></span></td>
<td><span data-ttu-id="b36c4-112">Il peer è il lato client di un'autenticazione EAP.</span><span class="sxs-lookup"><span data-stu-id="b36c4-112">The peer is the client side of an EAP authentication.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b36c4-113">In che modo un peer è diverso da un supplicant?</span><span class="sxs-lookup"><span data-stu-id="b36c4-113">How does a peer differ from a supplicant?</span></span></td>
<td><span data-ttu-id="b36c4-114">Il richiedente trasporta pacchetti, mentre un peer non lo è.</span><span class="sxs-lookup"><span data-stu-id="b36c4-114">The supplicant transports packets, whereas a peer does not.</span></span> <span data-ttu-id="b36c4-115">Tuttavia, i termini peer, supplicant e client sono in gran parte sinonimi.</span><span class="sxs-lookup"><span data-stu-id="b36c4-115">Nonetheless, the terms peer, supplicant and client are largely synonymous.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b36c4-116">Che cos'è un autenticatore?</span><span class="sxs-lookup"><span data-stu-id="b36c4-116">What is an authenticator?</span></span></td>
<td><span data-ttu-id="b36c4-117">L'autenticatore è il punto di accesso wireless, il server di accesso alla rete (NAS) o il dispositivo di accesso alla rete (NAD) che autentica il supplicante.</span><span class="sxs-lookup"><span data-stu-id="b36c4-117">The authenticator is the wireless access point, network access server (NAS), or network access device (NAD) that authenticates the supplicant.</span></span> <span data-ttu-id="b36c4-118">L'autenticatore è noto anche come server EAP.</span><span class="sxs-lookup"><span data-stu-id="b36c4-118">The authenticator is also known as the EAP server.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b36c4-119">Qual è la durata di un'autenticazione?</span><span class="sxs-lookup"><span data-stu-id="b36c4-119">What is the lifetime of an authentication?</span></span></td>
<td><span data-ttu-id="b36c4-120">Il ciclo di vita di una singola sessione di autenticazione sul lato client è tutto ciò che si verifica tra le funzioni [<strong>EapHostPeerBeginSession</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession) e [<strong>EapHostPeerEndSession</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerendsession) chiamate.</span><span class="sxs-lookup"><span data-stu-id="b36c4-120">The lifetime of a single authentication session on the client side is everything that occurs between the [<strong>EapHostPeerBeginSession</strong>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) and [<strong>EapHostPeerEndSession</strong>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) functions being called.</span></span> <span data-ttu-id="b36c4-121">La durata sul lato Authenticator è tutto ciò che si verifica tra le funzioni [<strong>EapPeerBeginSession</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeerbeginsession) e [<strong>EapPeerEndSession</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeerendsession).</span><span class="sxs-lookup"><span data-stu-id="b36c4-121">The lifetime on the authenticator side is everything that occurs between the [<strong>EapPeerBeginSession</strong>](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) and [<strong>EapPeerEndSession</strong>](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession) functions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b36c4-122">Che cos'è un BLOB?</span><span class="sxs-lookup"><span data-stu-id="b36c4-122">What is a BLOB?</span></span> <span data-ttu-id="b36c4-123">Perché convertire un BLOB di configurazione (binario) in XML?</span><span class="sxs-lookup"><span data-stu-id="b36c4-123">Why would I convert a configuration (binary) BLOB to XML?</span></span></td>
<td><span data-ttu-id="b36c4-124">Un BLOB è un oggetto binario di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="b36c4-124">A BLOB is a binary large object.</span></span> <span data-ttu-id="b36c4-125">XML presenta diversi vantaggi rispetto a un BLOB di configurazione binaria.</span><span class="sxs-lookup"><span data-stu-id="b36c4-125">XML has several advantages over a binary configuration BLOB.</span></span> <span data-ttu-id="b36c4-126">I dati di configurazione archiviati in XML sono leggibili, modificabili in formato umano e multipiattaforma.</span><span class="sxs-lookup"><span data-stu-id="b36c4-126">Configuration data that is stored in XML is human-readable, human-editable, and cross-platform.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b36c4-127">Quando si converte un BLOB XML archiviato in un BLOB binario?</span><span class="sxs-lookup"><span data-stu-id="b36c4-127">When do I convert a stored XML BLOB back to a binary BLOB?</span></span></td>
<td><span data-ttu-id="b36c4-128">È possibile archiviare un BLOB binario o XML, ma è sempre necessario convertire di nuovo il BLOB XML in un BLOB binario prima di usarlo con le API di Runtime. le API di runtime non accettano una directory XML.</span><span class="sxs-lookup"><span data-stu-id="b36c4-128">It's possible to store a binary BLOB or XML BLOB, but you must always convert the XML BLOB back to a binary BLOB before use with run-time APIs; the run-time APIs cannot accept an XML directory.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b36c4-129">Che cosa sono i metodi nativi?</span><span class="sxs-lookup"><span data-stu-id="b36c4-129">What are native methods?</span></span></td>
<td><span data-ttu-id="b36c4-130">I metodi EAP nativi usano la nuova API EAPHost.</span><span class="sxs-lookup"><span data-stu-id="b36c4-130">Native EAP methods use the new EAPHost API.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b36c4-131">Che cosa sono i metodi legacy?</span><span class="sxs-lookup"><span data-stu-id="b36c4-131">What are legacy methods?</span></span></td>
<td><span data-ttu-id="b36c4-132">I metodi EAP legacy sono definiti nella Guida di [riferimento al protocollo Extensible Authentication](/previous-versions/windows/desktop/eap/extensible-authentication-protocol-reference).</span><span class="sxs-lookup"><span data-stu-id="b36c4-132">Legacy EAP methods are defined in the [Extensible Authentication Protocol Reference](/previous-versions/windows/desktop/eap/extensible-authentication-protocol-reference).</span></span> <span data-ttu-id="b36c4-133">I metodi EAP legacy sono disponibili per l'utilizzo in Windows Vista e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="b36c4-133">The legacy EAP methods are available for use in Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="b36c4-134">Questi metodi potrebbero non essere disponibili per l'utilizzo nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b36c4-134">These methods may not be available for use in subsequent versions of the operating system.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b36c4-135">Qual è la differenza tra i metodi legacy e native?</span><span class="sxs-lookup"><span data-stu-id="b36c4-135">What's the difference between legacy and native methods?</span></span></td>
<td><span data-ttu-id="b36c4-136">Le API native sono più semplici e presentano meno funzionalità.</span><span class="sxs-lookup"><span data-stu-id="b36c4-136">The native APIs are simpler and have fewer features.</span></span> <span data-ttu-id="b36c4-137">Tutti i nuovi metodi EAP devono essere scritti usando l'API EAPHost.</span><span class="sxs-lookup"><span data-stu-id="b36c4-137">All new EAP methods should be written using the EAPHost API.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b36c4-138">Che cosa sono i &quot; criteri di gruppo &quot; ?</span><span class="sxs-lookup"><span data-stu-id="b36c4-138">What is &quot;group policy&quot;?</span></span></td>
<td><span data-ttu-id="b36c4-139">Per una descrizione dei criteri di gruppo, vedere [criteri di gruppo Collection](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="b36c4-139">For a description of group policy, see [Group Policy Collection](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b36c4-140">Le funzioni EAPHost possono eseguire l'override dei criteri di configurazione specificati da criteri di gruppo?</span><span class="sxs-lookup"><span data-stu-id="b36c4-140">Can EAPHost functions override configuration policy specified by group policy?</span></span></td>
<td><span data-ttu-id="b36c4-141">No, mai.</span><span class="sxs-lookup"><span data-stu-id="b36c4-141">No, never.</span></span> <span data-ttu-id="b36c4-142">Se criteri di gruppo è in uso, le impostazioni di criteri di gruppo eseguiranno sempre l'override delle impostazioni di configurazione EAPHost.</span><span class="sxs-lookup"><span data-stu-id="b36c4-142">If group policy is in use, group policy settings will always override EAPHost configuration settings.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b36c4-143">Che cos'è Single Sign-on (SSO)?</span><span class="sxs-lookup"><span data-stu-id="b36c4-143">What is Single-Sign-On (SSO)?</span></span></td>
<td><span data-ttu-id="b36c4-144">[802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) è un meccanismo di autenticazione di livello 2.</span><span class="sxs-lookup"><span data-stu-id="b36c4-144">[802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) is a layer 2 authentication mechanism.</span></span> <span data-ttu-id="b36c4-145">A seconda della configurazione SSO, SSO consente agli utenti di eseguire l'autenticazione alla rete utilizzando l'autenticazione [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) prima o immediatamente dopo l'accesso a Windows.</span><span class="sxs-lookup"><span data-stu-id="b36c4-145">Depending on the SSO configuration, SSO enables users to authenticate to the network using [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) authentication before or immediately after logging on to Windows.</span></span> <span data-ttu-id="b36c4-146">SSO può essere configurato in modo da utilizzare le credenziali di Windows per l'autenticazione di rete (in tal caso, gli utenti immettono le credenziali una sola volta) o utilizzano credenziali diverse per Windows e l'autenticazione di rete.</span><span class="sxs-lookup"><span data-stu-id="b36c4-146">SSO can be configured to use Windows credentials for network authentication (in which case users enter their credentials only once) or use different credentials for Windows and network authentication.</span></span> <span data-ttu-id="b36c4-147">Per ulteriori informazioni, vedere [SSO e PLAP](understanding-sso-and-plap.md).</span><span class="sxs-lookup"><span data-stu-id="b36c4-147">For more information, see [SSO and PLAP](understanding-sso-and-plap.md).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b36c4-148">Informazioni sul provider di accesso con pre-accesso (PLAP)</span><span class="sxs-lookup"><span data-stu-id="b36c4-148">What is Pre-Logon Access Provider (PLAP)</span></span></td>
<td><span data-ttu-id="b36c4-149">Per ulteriori informazioni, vedere [SSO e PLAP](understanding-sso-and-plap.md).</span><span class="sxs-lookup"><span data-stu-id="b36c4-149">For more information, see [SSO and PLAP](understanding-sso-and-plap.md).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b36c4-150">Che cos'è PEAP (Protected Extensible Authentication Protocol)?</span><span class="sxs-lookup"><span data-stu-id="b36c4-150">What is Protected Extensible Authentication Protocol (PEAP)?</span></span></td>
<td><span data-ttu-id="b36c4-151">Per ulteriori informazioni, vedere [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)) e [informazioni sul protocollo di autenticazione estendibile](/previous-versions/windows/desktop/eap/about-extensible-authentication-protocol).</span><span class="sxs-lookup"><span data-stu-id="b36c4-151">For more information, see [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)) and [About Extensible Authentication Protocol](/previous-versions/windows/desktop/eap/about-extensible-authentication-protocol).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b36c4-152">In che modo PEAP affronta la ripresa della sessione e la nuova autenticazione?</span><span class="sxs-lookup"><span data-stu-id="b36c4-152">How does PEAP deal with session resumption and re-authentication?</span></span></td>
<td><span data-ttu-id="b36c4-153">Il ripristino e la riautenticazione della sessione si verificano in genere durante il roaming su una rete wireless.</span><span class="sxs-lookup"><span data-stu-id="b36c4-153">Session resumption and re-authentication typically occurs while roaming on a wireless network.</span></span> <span data-ttu-id="b36c4-154">Windows Data Protection API (DPAPI) fornisce un modo per proteggere e associare dati a un utente e, facoltativamente, alla sessione di accesso.</span><span class="sxs-lookup"><span data-stu-id="b36c4-154">Windows Data Protection API (DPAPI) provides a way to protect and bind data to a user and optionally the logon session.</span></span> <span data-ttu-id="b36c4-155">Il chiamante assegna a [<strong>CryptProtectMemory</strong>] (/Windows/Desktop/API/DPAPI/NF-DPAPI-cryptprotectmemory) un buffer non crittografato e DPAPI crittografa la memoria sul posto.</span><span class="sxs-lookup"><span data-stu-id="b36c4-155">The caller gives [<strong>CryptProtectMemory</strong>](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory) an unencrypted buffer and DPAPI will encrypt the memory in place.</span></span> <span data-ttu-id="b36c4-156">In un secondo momento, il chiamante può passare il buffer crittografato a [<strong>CryptUnprotectMemory</strong>] (/Windows/Desktop/API/DPAPI/NF-DPAPI-cryptunprotectmemory) e DPAPI decrittografare la memoria, ancora una volta sul posto.</span><span class="sxs-lookup"><span data-stu-id="b36c4-156">Later, the caller can pass in the encrypted buffer to [<strong>CryptUnprotectMemory</strong>](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectmemory) and DPAPI will decrypt the memory, once again in place.</span></span> <span data-ttu-id="b36c4-157">Per ulteriori informazioni, vedere [estensione dell'applicazione TLS interna (TSL/IA)](https://go.microsoft.com/fwlink/p/?linkid=84011) e [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="b36c4-157">For more information, see [TLS Inner Application Extension (TSL/IA)](https://go.microsoft.com/fwlink/p/?linkid=84011) and [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b36c4-158">Che cos'è la sicurezza a livello di EAP-Transport (EAP-TLS)?</span><span class="sxs-lookup"><span data-stu-id="b36c4-158">What is EAP-Transport Level Security (EAP-TLS)?</span></span></td>
<td><span data-ttu-id="b36c4-159">EAP-TLS è un protocollo client-server in cui i profili certificato distinti vengono in genere usati per il client e il server. Per ulteriori informazioni, vedere [IETF RTC 2716](/previous-versions/windows/embedded/ms885336(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="b36c4-159">EAP-TLS is a client-server protocol in which distinct certificate profiles are typically used for the client and server.For more information, see [IETF RTC 2716](/previous-versions/windows/embedded/ms885336(v=msdn.10)).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b36c4-160">Ricerca per categorie implementare una modifica della password con l'API dell'autorità di protezione locale (LSA)?</span><span class="sxs-lookup"><span data-stu-id="b36c4-160">How do I implement a password change using the Local Security Authority (LSA) API?</span></span></td>
<td><span data-ttu-id="b36c4-161">Usare la funzione [<strong>LsaCallAuthenticationPackage</strong>] (/Windows/Desktop/API/ntsecapi/NF-ntsecapi-LsaCallAuthenticationPackage) per implementare una modifica della password.</span><span class="sxs-lookup"><span data-stu-id="b36c4-161">Use the [<strong>LsaCallAuthenticationPackage</strong>](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) function to implement a password change.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b36c4-162">Perché si vuole abilitare la traccia in EAPHost?</span><span class="sxs-lookup"><span data-stu-id="b36c4-162">Why would I want to enable tracing in EAPHost?</span></span></td>
<td><span data-ttu-id="b36c4-163">I log di traccia contengono informazioni di debug (disponibili solo in inglese) che possono aiutare gli sviluppatori e i partner Microsoft a trovare le cause principali di eventuali problemi riscontrati durante il processo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="b36c4-163">The trace logs contain debugging information (available in English only) that may assist Microsoft developers and partners in finding the root causes of any issues being experienced with the authentication process.</span></span> <span data-ttu-id="b36c4-164">Per ulteriori informazioni, vedere [Abilitazione della traccia](enabling-tracing.md).</span><span class="sxs-lookup"><span data-stu-id="b36c4-164">For more information, see [Enabling Tracing](enabling-tracing.md).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b36c4-165">Perché si verifica il codice di errore NTE_BAD_KEY_STATE (0x8009000BL) quando si usa l'API di [crittografia](/windows/desktop/SecCrypto/cryptography-portal) per accedere allo scambio EAP-TLS?</span><span class="sxs-lookup"><span data-stu-id="b36c4-165">Why do I encounter the error code, NTE_BAD_KEY_STATE (0x8009000BL) when I use the [Cryptography](/windows/desktop/SecCrypto/cryptography-portal) API to sign into the EAP-TLS exchange?</span></span></td>
<td><span data-ttu-id="b36c4-166">In Winerror. h NTE_BAD_KEY_STATE (0x8009000BL) è definito come &quot; chiave non valida per l'utilizzo nello stato specificato &quot; .</span><span class="sxs-lookup"><span data-stu-id="b36c4-166">In Winerror.h NTE_BAD_KEY_STATE (0x8009000BL) is defined as a &quot;key not valid for use in specified state&quot;.</span></span> <span data-ttu-id="b36c4-167">Questo errore viene in genere restituito negli scenari seguenti.</span><span class="sxs-lookup"><span data-stu-id="b36c4-167">This error is typically returned in the following scenarios.</span></span>
<ul>
<li><span data-ttu-id="b36c4-168">Quando si tenta di esportare un BLOB di chiave privata non esportabile</span><span class="sxs-lookup"><span data-stu-id="b36c4-168">When attempting to export a non-exportable private key BLOB</span></span></li>
<li><span data-ttu-id="b36c4-169">Quando si tenta di generare un handle di hash PRF (pseudo-random Function) utilizzando [<strong>CryptCreateHash</strong>] (/Windows/Desktop/API/Wincrypt/NF-Wincrypt-CryptCreateHash).</span><span class="sxs-lookup"><span data-stu-id="b36c4-169">When unsuccessfully attempting to generate a pseudo-random function (PRF) hash handle using [<strong>CryptCreateHash</strong>](/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash)</span></span></li>
</ul>
<span data-ttu-id="b36c4-170">Per ulteriori informazioni, vedere la pagina relativa alla [fine dei messaggi nel protocollo TLS 1,0](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).</span><span class="sxs-lookup"><span data-stu-id="b36c4-170">For more information, see [Finish Messages in the TLS 1.0 Protocol](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b36c4-171">Che cos'è una funzione pseudo-casuale (PRF)?</span><span class="sxs-lookup"><span data-stu-id="b36c4-171">What is a pseudo-random function (PRF)?</span></span></td>
<td><span data-ttu-id="b36c4-172">Funzione che accetta una chiave, un'etichetta e un valore di inizializzazione come input, quindi produce un output di lunghezza arbitraria.</span><span class="sxs-lookup"><span data-stu-id="b36c4-172">A function that takes a key, label, and seed as input, then produces an output of arbitrary length.</span></span> <span data-ttu-id="b36c4-173">Per ulteriori informazioni, vedere la pagina relativa alla [fine dei messaggi nel protocollo TLS 1,0](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).</span><span class="sxs-lookup"><span data-stu-id="b36c4-173">For more information, see [Finish Messages in the TLS 1.0 Protocol](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b36c4-174">Come è possibile associare EAPHost alle schede di rete?</span><span class="sxs-lookup"><span data-stu-id="b36c4-174">How does EAPHost bind to network adapters?</span></span></td>
<td><span data-ttu-id="b36c4-175">EAPHost consente il funzionamento simultaneo di più supplicant e ogni supplicant può essere associato a più schede di rete.</span><span class="sxs-lookup"><span data-stu-id="b36c4-175">EAPHost allows multiple supplicants to operate simultaneously, and each supplicant can bind to multiple network adapters.</span></span> <span data-ttu-id="b36c4-176">I supplicant EAPHost forniscono il binding ai livelli di rete e guidano il processo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="b36c4-176">EAPHost supplicants provide binding to the network layers and drive the authentication process.</span></span> <span data-ttu-id="b36c4-177">I supplicant contengono la configurazione dell'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="b36c4-177">Supplicants contain authentication configuration.</span></span> <span data-ttu-id="b36c4-178">I supplicant salvano inoltre lo stato e forniscono la successiva sicurezza della connessione.</span><span class="sxs-lookup"><span data-stu-id="b36c4-178">Supplicants also save the state and provide subsequent connection security.</span></span> <span data-ttu-id="b36c4-179">Poiché EAPHost non è associato direttamente ad alcun meccanismo di rete, l'estendibilità dei supplicant è possibile.</span><span class="sxs-lookup"><span data-stu-id="b36c4-179">Because EAPHost doesn't directly bind to any network mechanism, supplicant extensibility is possible.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="b36c4-180">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b36c4-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b36c4-181">Domande frequenti sul supplicant EAPHost</span><span class="sxs-lookup"><span data-stu-id="b36c4-181">EAPHost Supplicant FAQs</span></span>](eaphost-supplicant-frequently-asked-questions.md)
</dt> <dt>

[<span data-ttu-id="b36c4-182">Domande frequenti sul metodo EAPHost</span><span class="sxs-lookup"><span data-stu-id="b36c4-182">EAPHost Method FAQs</span></span>](eap-method-frequently-asked-questions.md)
</dt> <dt>

[<span data-ttu-id="b36c4-183">Domande frequenti sullo sviluppo di EAPHost</span><span class="sxs-lookup"><span data-stu-id="b36c4-183">EAPHost Development FAQs</span></span>](eaphost-development-frequently-asked-questions.md)
</dt> </dl>


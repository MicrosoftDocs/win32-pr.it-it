---
title: Costanti di autenticazione (WSManDisp. h)
description: Specificare il metodo di autenticazione e la modalità di gestione dei server di certificati per il trasporto HTTPS delle richieste.
ms.assetid: adfefbc9-c386-48db-a0c2-145aa4f91bfa
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagCredUsernamePassword
- WSManFlagSkipCACheck
- WSManFlagSkipCNCheck
- WSManFlagUseNoAuthentication
- WSManFlagUseDigest
- WSManFlagUseNegotiate
- WSManFlagUseBasic
- WSManFlagUseKerberos
- WSManFlagNoEncryption
- WSManFlagUseClientCertificate
- WSManFlagUseCredSsp
- WSManFlagSkipRevocationCheck
- WSManFlagAllowNegotiateImplicitCredentials
- WSManFlagUseSsl
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce45d1474cf6c925149c05ae348231333c3356e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518772"
---
# <a name="authentication-constants"></a><span data-ttu-id="9bfa7-103">Costanti di autenticazione</span><span class="sxs-lookup"><span data-stu-id="9bfa7-103">Authentication Constants</span></span>

<span data-ttu-id="9bfa7-104">Le costanti di autenticazione sono costanti nell'enumerazione **\_ \_ WSManSessionFlags** che specificano il metodo di autenticazione e come gestire i server dei certificati per il trasporto HTTPS delle richieste.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-104">Authentication constants are constants in the **\_\_WSManSessionFlags** enumeration that specify the authentication method and how to handle certificate servers for HTTPS transport of requests.</span></span>

<span data-ttu-id="9bfa7-105">Una o più costanti elencate nell'elenco seguente sono obbligatorie nel parametro *Flags* nelle chiamate a [**WSMan. CreateSession**](wsman-createsession.md) o in [**IWSMan:: CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) chiamate che si connettono a un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-105">One or more of the constants listed in the following list are required in the *flags* parameter in calls to [**WSMan.CreateSession**](wsman-createsession.md) or in [**IWSMan::CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) calls that connect to a remote computer.</span></span>

<dl> <dt>

<span data-ttu-id="9bfa7-106"><span id="WSManFlagCredUsernamePassword"></span><span id="wsmanflagcredusernamepassword"></span><span id="WSMANFLAGCREDUSERNAMEPASSWORD"></span>**WSManFlagCredUsernamePassword**</span><span class="sxs-lookup"><span data-stu-id="9bfa7-106"><span id="WSManFlagCredUsernamePassword"></span><span id="wsmanflagcredusernamepassword"></span><span id="WSMANFLAGCREDUSERNAMEPASSWORD"></span>**WSManFlagCredUsernamePassword**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bfa7-107">4096 (0x1000)</span><span class="sxs-lookup"><span data-stu-id="9bfa7-107">4096 (0x1000)</span></span>
</dt> <dt>



<span data-ttu-id="9bfa7-108">Usare il nome utente e la password come credenziali.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-108">Use the user name and password as the credentials.</span></span> <span data-ttu-id="9bfa7-109">Impostare questo flag quando si crea un oggetto [**ConnectionOptions**](connectionoptions.md) e si forniscono [**nome utente**](connectionoptions-username.md) e [**password**](connectionoptions-password.md).</span><span class="sxs-lookup"><span data-stu-id="9bfa7-109">Set this flag when you create a [**ConnectionOptions**](connectionoptions.md) object and supply [**Username**](connectionoptions-username.md) and [**Password**](connectionoptions-password.md).</span></span> <span data-ttu-id="9bfa7-110">Le credenziali possono essere un account di dominio o un account nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-110">The credentials can be a domain account or an account on the local computer.</span></span> <span data-ttu-id="9bfa7-111">Per impostazione predefinita, l'account deve essere un membro del gruppo Administrators locale nel computer locale o remoto.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-111">By default, the account must be a member of the local Administrators group on the local or remote computer.</span></span> <span data-ttu-id="9bfa7-112">Il servizio gestione remota Windows può tuttavia essere configurato in modo da consentire altri utenti.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-112">However, the WinRM service can be configured to allow other users.</span></span> <span data-ttu-id="9bfa7-113">Per ulteriori informazioni, vedere [installazione e configurazione per gestione remota Windows](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="9bfa7-113">For more information, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span> <span data-ttu-id="9bfa7-114">È possibile impostare questo flag quando si specificano le credenziali per l'autenticazione Negotiate (nota anche come [*autenticazione integrata di Windows*](windows-remote-management-glossary.md)) o per [*l'autenticazione di base*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="9bfa7-114">You can set this flag when you specify credentials for Negotiate authentication (also known as [*Windows Integrated Authentication*](windows-remote-management-glossary.md)) or for [*Basic authentication*](windows-remote-management-glossary.md).</span></span>

<span data-ttu-id="9bfa7-115">Il metodo di scripting associato è [**WSMan. SessionFlagCredUsernamePassword**](wsman-sessionflagcredusernamepassword.md)e il metodo C++ è [**IWSManEx. SessionFlagCredUsernamePassword**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagcredusernamepassword).</span><span class="sxs-lookup"><span data-stu-id="9bfa7-115">The associated scripting method is [**WSMan.SessionFlagCredUsernamePassword**](wsman-sessionflagcredusernamepassword.md), and the C++ method is [**IWSManEx.SessionFlagCredUsernamePassword**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagcredusernamepassword).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bfa7-116"><span id="WSManFlagSkipCACheck"></span><span id="wsmanflagskipcacheck"></span><span id="WSMANFLAGSKIPCACHECK"></span>**WSManFlagSkipCACheck**</span><span class="sxs-lookup"><span data-stu-id="9bfa7-116"><span id="WSManFlagSkipCACheck"></span><span id="wsmanflagskipcacheck"></span><span id="WSMANFLAGSKIPCACHECK"></span>**WSManFlagSkipCACheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bfa7-117">8192 (0x2000)</span><span class="sxs-lookup"><span data-stu-id="9bfa7-117">8192 (0x2000)</span></span>
</dt> <dt>



<span data-ttu-id="9bfa7-118">Quando si esegue la connessione tramite HTTPS, il client non convalida che il certificato del server sia firmato da un'autorità di certificazione (CA) attendibile.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-118">When connecting over HTTPS, the client does not validate that the server certificate is signed by a trusted certification authority (CA).</span></span> <span data-ttu-id="9bfa7-119">Usare questo valore solo quando il computer remoto è considerato attendibile da altri mezzi, ad esempio se il computer remoto fa parte di una rete fisicamente sicura e isolata oppure il computer remoto è elencato come host attendibile nella configurazione di WinRM.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-119">Use this value only when the remote computer is trusted by other means, for example, if the remote computer is part of a network that is physically secure and isolated or the remote computer is listed as a trusted host in the WinRM configuration.</span></span>

<span data-ttu-id="9bfa7-120">Il metodo di scripting associato è [**WSMan. SessionFlagSkipCACheck**](wsman-sessionflagskipcacheck.md)e il metodo C++ è [**IWSManEx. SessionFlagSkipCACheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcacheck).</span><span class="sxs-lookup"><span data-stu-id="9bfa7-120">The associated scripting method is [**WSMan.SessionFlagSkipCACheck**](wsman-sessionflagskipcacheck.md), and the C++ method is [**IWSManEx.SessionFlagSkipCACheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcacheck).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bfa7-121"><span id="WSManFlagSkipCNCheck"></span><span id="wsmanflagskipcncheck"></span><span id="WSMANFLAGSKIPCNCHECK"></span>**WSManFlagSkipCNCheck**</span><span class="sxs-lookup"><span data-stu-id="9bfa7-121"><span id="WSManFlagSkipCNCheck"></span><span id="wsmanflagskipcncheck"></span><span id="WSMANFLAGSKIPCNCHECK"></span>**WSManFlagSkipCNCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bfa7-122">16384 (0x4000)</span><span class="sxs-lookup"><span data-stu-id="9bfa7-122">16384 (0x4000)</span></span>
</dt> <dt>



<span data-ttu-id="9bfa7-123">Quando si esegue la connessione tramite HTTPS, il client non convalida che il nome comune (CN) nel certificato del server corrisponda al nome del computer nella stringa di connessione.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-123">When connecting over HTTPS, the client will not validate that the common name (CN) in the server certificate matches the computer name in the connection string.</span></span> <span data-ttu-id="9bfa7-124">Usare solo quando il computer remoto è considerato attendibile da altri mezzi, ad esempio se il computer remoto fa parte di una rete fisicamente sicura e isolata oppure il computer remoto è elencato come host attendibile nella configurazione di WinRM.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-124">Use only when the remote computer is trusted by other means, for example, if the remote computer is part of a network that is physically secure and isolated or the remote computer is listed as a trusted host in the WinRM configuration.</span></span>

<span data-ttu-id="9bfa7-125">Il metodo di scripting associato è [**WSMan. SessionFlagSkipCNCheck**](wsman-sessionflagskipcncheck.md)e il metodo C++ è [**IWSManEx. SessionFlagSkipCNCheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcncheck).</span><span class="sxs-lookup"><span data-stu-id="9bfa7-125">The associated scripting method is [**WSMan.SessionFlagSkipCNCheck**](wsman-sessionflagskipcncheck.md), and the C++ method is [**IWSManEx.SessionFlagSkipCNCheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcncheck).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bfa7-126"><span id="WSManFlagUseNoAuthentication"></span><span id="wsmanflagusenoauthentication"></span><span id="WSMANFLAGUSENOAUTHENTICATION"></span>**WSManFlagUseNoAuthentication**</span><span class="sxs-lookup"><span data-stu-id="9bfa7-126"><span id="WSManFlagUseNoAuthentication"></span><span id="wsmanflagusenoauthentication"></span><span id="WSMANFLAGUSENOAUTHENTICATION"></span>**WSManFlagUseNoAuthentication**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bfa7-127">32768 (0x8000)</span><span class="sxs-lookup"><span data-stu-id="9bfa7-127">32768 (0x8000)</span></span>
</dt> <dt>



<span data-ttu-id="9bfa7-128">Non usare alcuna autenticazione.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-128">Use no authentication.</span></span> <span data-ttu-id="9bfa7-129">Specificare questa costante durante il test di una connessione a un computer remoto per determinare se un servizio che implementa il protocollo WS-Management è configurato per l'ascolto delle richieste di dati.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-129">Specify this constant when testing a connection to a remote computer to determine if a service that implements the WS-Management protocol is configured to listen for data requests.</span></span> <span data-ttu-id="9bfa7-130">Non è possibile combinare **WSManFlagUseNoAuthentication** con altre costanti di [**sessione**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="9bfa7-130">**WSManFlagUseNoAuthentication** cannot be combined with any other [**Session**](session.md) constant.</span></span> <span data-ttu-id="9bfa7-131">Il metodo di scripting associato è [**WSMan. SessionFlagUseNoAuthentication**](wsman-sessionflagusenoauthentication.md)e il metodo C++ è [**WSManEx. SessionFlagUseNoAuthentication**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenoauthentication).</span><span class="sxs-lookup"><span data-stu-id="9bfa7-131">The associated scripting method is [**WSMan.SessionFlagUseNoAuthentication**](wsman-sessionflagusenoauthentication.md), and the C++ method is [**WSManEx.SessionFlagUseNoAuthentication**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenoauthentication).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bfa7-132"><span id="WSManFlagUseDigest"></span><span id="wsmanflagusedigest"></span><span id="WSMANFLAGUSEDIGEST"></span>**WSManFlagUseDigest**</span><span class="sxs-lookup"><span data-stu-id="9bfa7-132"><span id="WSManFlagUseDigest"></span><span id="wsmanflagusedigest"></span><span id="WSMANFLAGUSEDIGEST"></span>**WSManFlagUseDigest**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bfa7-133">65536 (0x10000)</span><span class="sxs-lookup"><span data-stu-id="9bfa7-133">65536 (0x10000)</span></span>
</dt> <dt>



<span data-ttu-id="9bfa7-134">Usare l'autenticazione del digest.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-134">Use Digest authentication.</span></span> <span data-ttu-id="9bfa7-135">Solo il computer client può avviare una richiesta di autenticazione del digest.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-135">Only the client computer can initiate a Digest authentication request.</span></span> <span data-ttu-id="9bfa7-136">Il client invia una richiesta al server per l'autenticazione e la ricezione di una stringa di token dal server.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-136">The client sends a request to the server to authenticate and receives a token string from the server.</span></span> <span data-ttu-id="9bfa7-137">Il client invia quindi la richiesta di risorse, inclusi il nome utente e un hash crittografico della password combinata con la stringa del token.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-137">The client then sends the resource request, including the user name and a cryptographic hash of the password combined with the token string.</span></span> <span data-ttu-id="9bfa7-138">L'autenticazione del digest è supportata per HTTP e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-138">Digest authentication is supported for HTTP and HTTPS.</span></span> <span data-ttu-id="9bfa7-139">Gli script client WinRM e le applicazioni possono specificare l'autenticazione del digest, ma non il servizio.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-139">WinRM client scripts and applications can specify Digest authentication, but not the service.</span></span>

<span data-ttu-id="9bfa7-140">Il metodo di scripting associato è [**WSMan. SessionFlagUseDigest**](wsman-sessionflagusedigest.md)e il metodo C++ è [**IWSManEx. SessionFlagUseDigest**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusedigest).</span><span class="sxs-lookup"><span data-stu-id="9bfa7-140">The associated scripting method is [**WSMan.SessionFlagUseDigest**](wsman-sessionflagusedigest.md), and the C++ method is [**IWSManEx.SessionFlagUseDigest**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusedigest).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bfa7-141"><span id="WSManFlagUseNegotiate"></span><span id="wsmanflagusenegotiate"></span><span id="WSMANFLAGUSENEGOTIATE"></span>**WSManFlagUseNegotiate**</span><span class="sxs-lookup"><span data-stu-id="9bfa7-141"><span id="WSManFlagUseNegotiate"></span><span id="wsmanflagusenegotiate"></span><span id="WSMANFLAGUSENEGOTIATE"></span>**WSManFlagUseNegotiate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bfa7-142">131072 (0x20000)</span><span class="sxs-lookup"><span data-stu-id="9bfa7-142">131072 (0x20000)</span></span>
</dt> <dt>



<span data-ttu-id="9bfa7-143">Usare l'autenticazione Negotiate.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-143">Use Negotiate authentication.</span></span> <span data-ttu-id="9bfa7-144">Il client invia una richiesta al server per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-144">The client sends a request to the server to authenticate.</span></span> <span data-ttu-id="9bfa7-145">Il server determina se utilizzare Kerberos o NTLM.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-145">The server determines whether to use Kerberos or NTLM.</span></span> <span data-ttu-id="9bfa7-146">Kerberos è selezionato per autenticare un account di dominio ed è selezionato NTLM per gli account computer locali.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-146">Kerberos is selected to authenticate a domain account and NTLM is selected for local computer accounts.</span></span> <span data-ttu-id="9bfa7-147">Il nome utente deve essere specificato nel formato dominio \\ nomeutente per un utente di dominio o nome utente nomeserver \\ per un utente locale in un computer server.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-147">The user name should be specified in the form domain\\username for a domain user or servername\\username for a local user on a server computer.</span></span>

<span data-ttu-id="9bfa7-148">Il [controllo dell'account utente (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) influiscono sull'accesso al servizio WinRM.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-148">[User Account Control (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) affects access to the WinRM service.</span></span> <span data-ttu-id="9bfa7-149">Quando si usa l'autenticazione Negotiate in un gruppo di lavoro o in un dominio, solo l'account Administrator predefinito può accedere al servizio.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-149">When Negotiate authentication is used in a workgroup or domain, only the built-in Administrator account can access the service.</span></span> <span data-ttu-id="9bfa7-150">Per consentire a tutti gli account del gruppo Administrators di accedere al servizio, impostare la seguente chiave del registro di sistema su 1: **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Policies \\ System \\ LocalAccountTokenFilterPolicy**.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-150">To allow all accounts in the Administrators group to access the service, set the following registry key to 1: **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Policies\\system\\LocalAccountTokenFilterPolicy**.</span></span>

<span data-ttu-id="9bfa7-151">Il metodo di scripting associato è [**WSMan. SessionFlagUseNegotiate**](wsman-sessionflagusenegotiate.md)e il metodo C++ è [**IWSManEx. SessionFlagUseNegotiate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenegotiate).</span><span class="sxs-lookup"><span data-stu-id="9bfa7-151">The associated scripting method is [**WSMan.SessionFlagUseNegotiate**](wsman-sessionflagusenegotiate.md), and the C++ method is [**IWSManEx.SessionFlagUseNegotiate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenegotiate).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bfa7-152"><span id="WSManFlagUseBasic"></span><span id="wsmanflagusebasic"></span><span id="WSMANFLAGUSEBASIC"></span>**WSManFlagUseBasic**</span><span class="sxs-lookup"><span data-stu-id="9bfa7-152"><span id="WSManFlagUseBasic"></span><span id="wsmanflagusebasic"></span><span id="WSMANFLAGUSEBASIC"></span>**WSManFlagUseBasic**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bfa7-153">262144 (0x40000)</span><span class="sxs-lookup"><span data-stu-id="9bfa7-153">262144 (0x40000)</span></span>
</dt> <dt>



<span data-ttu-id="9bfa7-154">Usa l'autenticazione di base.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-154">Use Basic authentication.</span></span> <span data-ttu-id="9bfa7-155">Il client presenta le credenziali sotto forma di nome utente e password, trasmesse direttamente nel messaggio di richiesta.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-155">The client presents credentials in the form of a user name and password, directly transmitted in the request message.</span></span> <span data-ttu-id="9bfa7-156">È possibile specificare solo le credenziali che identificano un account amministratore locale nel computer remoto.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-156">You can specify only credentials that identify a local administrator account on the remote computer.</span></span>

<span data-ttu-id="9bfa7-157">Il metodo di scripting associato è [**WSMan. SessionFlagUseBasic**](wsman-sessionflagusebasic.md)e il metodo C++ è [**IWSManEx. SessionFlagUseBasic**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusebasic).</span><span class="sxs-lookup"><span data-stu-id="9bfa7-157">The associated scripting method is [**WSMan.SessionFlagUseBasic**](wsman-sessionflagusebasic.md), and the C++ method is [**IWSManEx.SessionFlagUseBasic**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusebasic).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bfa7-158"><span id="WSManFlagUseKerberos"></span><span id="wsmanflagusekerberos"></span><span id="WSMANFLAGUSEKERBEROS"></span>**WSManFlagUseKerberos**</span><span class="sxs-lookup"><span data-stu-id="9bfa7-158"><span id="WSManFlagUseKerberos"></span><span id="wsmanflagusekerberos"></span><span id="WSMANFLAGUSEKERBEROS"></span>**WSManFlagUseKerberos**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bfa7-159">524288 (0x80000)</span><span class="sxs-lookup"><span data-stu-id="9bfa7-159">524288 (0x80000)</span></span>
</dt> <dt>



<span data-ttu-id="9bfa7-160">Utilizzo dell'autenticazione Kerberos.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-160">Use Kerberos authentication.</span></span> <span data-ttu-id="9bfa7-161">Il client e il server eseguono l'autenticazione reciproca usando i ticket Kerberos.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-161">The client and server mutually authenticate using Kerberos tickets.</span></span>

<span data-ttu-id="9bfa7-162">Il metodo di scripting associato è [**WSMan. SessionFlagUseKerberos**](wsman-sessionflagusekerberos.md)e il metodo C++ è [**IWSManEx. WSMan. SessionFlagUseKerberos**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusekerberos).</span><span class="sxs-lookup"><span data-stu-id="9bfa7-162">The associated scripting method is [**WSMan.SessionFlagUseKerberos**](wsman-sessionflagusekerberos.md), and the C++ method is [**IWSManEx.WSMan.SessionFlagUseKerberos**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusekerberos).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bfa7-163"><span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**</span><span class="sxs-lookup"><span data-stu-id="9bfa7-163"><span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bfa7-164">1048576 (0x100000)</span><span class="sxs-lookup"><span data-stu-id="9bfa7-164">1048576 (0x100000)</span></span>
</dt> <dt>



<span data-ttu-id="9bfa7-165">Usare nessuna crittografia.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-165">Use no encryption.</span></span> <span data-ttu-id="9bfa7-166">Il traffico non crittografato non è consentito per impostazione predefinita e deve essere abilitato sia nel client che nel server.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-166">Unencrypted traffic is not allowed by default and must be enabled on both the client and server.</span></span>

<span data-ttu-id="9bfa7-167">Il metodo di scripting associato è [**WSMan. SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md)e il metodo C++ è [**IWSManEx. SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).</span><span class="sxs-lookup"><span data-stu-id="9bfa7-167">The associated scripting method is [**WSMan.SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md), and the C++ method is [**IWSManEx.SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bfa7-168"><span id="WSManFlagUseClientCertificate"></span><span id="wsmanflaguseclientcertificate"></span><span id="WSMANFLAGUSECLIENTCERTIFICATE"></span>**WSManFlagUseClientCertificate**</span><span class="sxs-lookup"><span data-stu-id="9bfa7-168"><span id="WSManFlagUseClientCertificate"></span><span id="wsmanflaguseclientcertificate"></span><span id="WSMANFLAGUSECLIENTCERTIFICATE"></span>**WSManFlagUseClientCertificate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bfa7-169">2097152 (0x200000)</span><span class="sxs-lookup"><span data-stu-id="9bfa7-169">2097152 (0x200000)</span></span>
</dt> <dt>



<span data-ttu-id="9bfa7-170">Usare l'autenticazione basata sui certificati client.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-170">Use client certificate-based authentication.</span></span>

<span data-ttu-id="9bfa7-171">Il metodo di scripting associato è [**WSMan. SessionFlagUseClientCertificate**](wsman-sessionflaguseclientcert.md)e il metodo C++ è [**IWSManEx2. SessionFlagUseClientCertificate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex2-sessionflaguseclientcertificate).</span><span class="sxs-lookup"><span data-stu-id="9bfa7-171">The associated scripting method is [**WSMan.SessionFlagUseClientCertificate**](wsman-sessionflaguseclientcert.md), and the C++ method is [**IWSManEx2.SessionFlagUseClientCertificate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex2-sessionflaguseclientcertificate).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bfa7-172"><span id="WSManFlagUseCredSsp"></span><span id="wsmanflagusecredssp"></span><span id="WSMANFLAGUSECREDSSP"></span>**WSManFlagUseCredSsp**</span><span class="sxs-lookup"><span data-stu-id="9bfa7-172"><span id="WSManFlagUseCredSsp"></span><span id="wsmanflagusecredssp"></span><span id="WSMANFLAGUSECREDSSP"></span>**WSManFlagUseCredSsp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bfa7-173">16777216 (0x1000000)</span><span class="sxs-lookup"><span data-stu-id="9bfa7-173">16777216 (0x1000000)</span></span>
</dt> <dt>



<span data-ttu-id="9bfa7-174">Usare l'autenticazione Credential Security Support Provider (CredSSP).</span><span class="sxs-lookup"><span data-stu-id="9bfa7-174">Use Credential Security Support Provider (CredSSP) authentication.</span></span>

<span data-ttu-id="9bfa7-175">Il metodo di scripting associato è [**WSMan. SessionFlagUseCredSsp**](wsman-sessionflagusecredssp.md)e il metodo C++ è [**IWSManEx3. SessionFlagUseCredSsp**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex3-sessionflagusecredssp).</span><span class="sxs-lookup"><span data-stu-id="9bfa7-175">The associated scripting method is [**WSMan.SessionFlagUseCredSsp**](wsman-sessionflagusecredssp.md), and the C++ method is [**IWSManEx3.SessionFlagUseCredSsp**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex3-sessionflagusecredssp).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bfa7-176"><span id="WSManFlagSkipRevocationCheck"></span><span id="wsmanflagskiprevocationcheck"></span><span id="WSMANFLAGSKIPREVOCATIONCHECK"></span>**WSManFlagSkipRevocationCheck**</span><span class="sxs-lookup"><span data-stu-id="9bfa7-176"><span id="WSManFlagSkipRevocationCheck"></span><span id="wsmanflagskiprevocationcheck"></span><span id="WSMANFLAGSKIPREVOCATIONCHECK"></span>**WSManFlagSkipRevocationCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bfa7-177">0x2000000</span><span class="sxs-lookup"><span data-stu-id="9bfa7-177">0x2000000</span></span>
</dt> <dt>



<span data-ttu-id="9bfa7-178">Non controllare la revoca dei certificati durante l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-178">Do not check for certificate revocation during authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bfa7-179"><span id="WSManFlagAllowNegotiateImplicitCredentials"></span><span id="wsmanflagallownegotiateimplicitcredentials"></span><span id="WSMANFLAGALLOWNEGOTIATEIMPLICITCREDENTIALS"></span>**WSManFlagAllowNegotiateImplicitCredentials**</span><span class="sxs-lookup"><span data-stu-id="9bfa7-179"><span id="WSManFlagAllowNegotiateImplicitCredentials"></span><span id="wsmanflagallownegotiateimplicitcredentials"></span><span id="WSMANFLAGALLOWNEGOTIATEIMPLICITCREDENTIALS"></span>**WSManFlagAllowNegotiateImplicitCredentials**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bfa7-180">0x4000000</span><span class="sxs-lookup"><span data-stu-id="9bfa7-180">0x4000000</span></span>
</dt> <dt>



<span data-ttu-id="9bfa7-181">Consenti le credenziali implicite.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-181">Allow implicit credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9bfa7-182"><span id="WSManFlagUseSsl"></span><span id="wsmanflagusessl"></span><span id="WSMANFLAGUSESSL"></span>**WSManFlagUseSsl**</span><span class="sxs-lookup"><span data-stu-id="9bfa7-182"><span id="WSManFlagUseSsl"></span><span id="wsmanflagusessl"></span><span id="WSMANFLAGUSESSL"></span>**WSManFlagUseSsl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9bfa7-183">0x8000000</span><span class="sxs-lookup"><span data-stu-id="9bfa7-183">0x8000000</span></span>
</dt> <dt>



<span data-ttu-id="9bfa7-184">USA Secure Socket Layer, Abilita HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9bfa7-184">Use Secure Socket Layer, enables HTTPS.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9bfa7-185">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9bfa7-185">Requirements</span></span>



| <span data-ttu-id="9bfa7-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bfa7-186">Requirement</span></span> | <span data-ttu-id="9bfa7-187">Valore</span><span class="sxs-lookup"><span data-stu-id="9bfa7-187">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bfa7-188">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9bfa7-188">Minimum supported client</span></span><br/> | <span data-ttu-id="9bfa7-189">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9bfa7-189">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="9bfa7-190">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9bfa7-190">Minimum supported server</span></span><br/> | <span data-ttu-id="9bfa7-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9bfa7-191">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="9bfa7-192">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9bfa7-192">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bfa7-193"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9bfa7-193"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9bfa7-194">IDL</span><span class="sxs-lookup"><span data-stu-id="9bfa7-194">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9bfa7-195"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9bfa7-195"><dt>WSManDisp.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bfa7-196">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9bfa7-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bfa7-197">Costanti di sessione</span><span class="sxs-lookup"><span data-stu-id="9bfa7-197">Session Constants</span></span>](session-constants.md)
</dt> </dl>

 

 






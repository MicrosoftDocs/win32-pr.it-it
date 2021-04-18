---
title: Esempi di livelli di canale di sicurezza
description: Negli esempi seguenti viene illustrata la sicurezza nel livello del canale.
ms.assetid: ac4f0275-4783-411d-98da-2c5a1a169dcc
keywords:
- esempi di sicurezza
- esempi di sicurezza, installazione
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b1283339b1a4af624e118e3f6c76a07449f9274
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298517"
---
# <a name="security-channel-layer-examples"></a><span data-ttu-id="85450-107">Esempi di livelli di canale di sicurezza</span><span class="sxs-lookup"><span data-stu-id="85450-107">Security Channel Layer Examples</span></span>

<span data-ttu-id="85450-108">Negli esempi seguenti viene illustrata la sicurezza nel [livello del canale](channel-layer-overview.md)</span><span class="sxs-lookup"><span data-stu-id="85450-108">The following examples illustrate security in the [Channel Layer](channel-layer-overview.md)</span></span>

<span data-ttu-id="85450-109">Sicurezza del trasporto Windows su TCP: client: [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md), server: [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md).</span><span class="sxs-lookup"><span data-stu-id="85450-109">Windows transport security over TCP: Client: [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md), Server: [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md).</span></span>

<span data-ttu-id="85450-110">Sicurezza del trasporto Windows su Named Pipes: client: [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md), server: [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md).</span><span class="sxs-lookup"><span data-stu-id="85450-110">Windows transport security over named pipes: Client: [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md), Server: [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md).</span></span>

<span data-ttu-id="85450-111">Sicurezza del trasporto SSL: client: [HttpClientWithSslExample](httpclientwithsslexample.md), server: [HttpServerWithSslExample](httpserverwithsslexample.md).</span><span class="sxs-lookup"><span data-stu-id="85450-111">SSL transport security: Client: [HttpClientWithSslExample](httpclientwithsslexample.md), Server: [HttpServerWithSslExample](httpserverwithsslexample.md).</span></span>

<span data-ttu-id="85450-112">Nome utente sulla sicurezza in modalità mista SSL: client: [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md), server: [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md).</span><span class="sxs-lookup"><span data-stu-id="85450-112">Username over SSL mixed-mode security: Client: [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md), Server: [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md).</span></span>

<span data-ttu-id="85450-113">Nome utente sulla sicurezza in modalità mista SSL: client: [HttpClientWithKerberosOverSslExample](httpclientwithkerberosoversslexample.md), server: [HttpServerWithKerberosOverSslExample](httpserverwithkerberosoversslexample.md).</span><span class="sxs-lookup"><span data-stu-id="85450-113">Username over SSL mixed-mode security: Client: [HttpClientWithKerberosOverSslExample](httpclientwithkerberosoversslexample.md), Server: [HttpServerWithKerberosOverSslExample](httpserverwithkerberosoversslexample.md).</span></span>

<span data-ttu-id="85450-114">Nome utente sulla sicurezza in modalità mista SSL: [MetadataImportWithUsernameOverSslExample](metadataimportwithusernameoversslexample.md).</span><span class="sxs-lookup"><span data-stu-id="85450-114">Username over SSL mixed-mode security: [MetadataImportWithUsernameOverSslExample](metadataimportwithusernameoversslexample.md).</span></span> <span data-ttu-id="85450-115">Token emesso sulla sicurezza in modalità mista SSL: [MetadataImportWithIssuedTokenOverSslExample](metadataimportwithissuedtokenoversslexample.md).</span><span class="sxs-lookup"><span data-stu-id="85450-115">Issued token over SSL mixed-mode security: [MetadataImportWithIssuedTokenOverSslExample](metadataimportwithissuedtokenoversslexample.md).</span></span> <span data-ttu-id="85450-116">Certificato X509 sulla sicurezza in modalità mista SSL: [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md).</span><span class="sxs-lookup"><span data-stu-id="85450-116">X509 certificate over SSL mixed-mode security: [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md).</span></span>

## <a name="one-time-setup-for-security-samples"></a><span data-ttu-id="85450-117">One-Time installazione per gli esempi di sicurezza</span><span class="sxs-lookup"><span data-stu-id="85450-117">One-Time Setup for Security Samples</span></span>

<span data-ttu-id="85450-118">Per eseguire gli esempi di sicurezza di WWSAPI, è necessario configurare i certificati client e server per SSL, oltre a un account utente locale per l'autenticazione dell'intestazione HTTP.</span><span class="sxs-lookup"><span data-stu-id="85450-118">To run WWSAPI security examples, you need to set up the client and server certificates for SSL, as well as a local user account for HTTP header authentication.</span></span> <span data-ttu-id="85450-119">Prima di iniziare, sono necessari gli strumenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="85450-119">Before you start, you need the following tools:</span></span>

-   <span data-ttu-id="85450-120">MakeCert.exe (disponibile in Windows 7 SDK).</span><span class="sxs-lookup"><span data-stu-id="85450-120">MakeCert.exe (Available in the Windows 7 SDK.)</span></span>
-   <span data-ttu-id="85450-121">CertUtil.exe o CertMgr.exe (CertUtil.exe è disponibile negli SDK di Windows a partire da Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="85450-121">CertUtil.exe or CertMgr.exe (CertUtil.exe is available in the Windows SDKs starting with Windows Server 2003.</span></span> <span data-ttu-id="85450-122">CertMgr.exe è disponibile in Windows 7 SDK.</span><span class="sxs-lookup"><span data-stu-id="85450-122">CertMgr.exe is available in the Windows 7 SDK.</span></span> <span data-ttu-id="85450-123">È necessario solo uno di questi strumenti.</span><span class="sxs-lookup"><span data-stu-id="85450-123">You only need one of these tools.)</span></span>
-   <span data-ttu-id="85450-124">HttpCfg.exe: questa operazione è necessaria solo se si utilizza Windows 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="85450-124">HttpCfg.exe: (You need this only if you are using Windows 2003 or Windows XP.</span></span> <span data-ttu-id="85450-125">Questo strumento è disponibile negli strumenti di supporto di Windows XP SP2 e viene fornito anche con il CD di Windows Server 2003 Resource Kit Tools.</span><span class="sxs-lookup"><span data-stu-id="85450-125">This tool is available in Windows XP SP2 Support Tools and also comes with the Windows Server 2003 Resource Kit Tools CD.)</span></span>

<span data-ttu-id="85450-126">Se si ottengono gli esempi di WWSAPI installando Windows 7 SDK, è possibile trovare il MakeCert.exe e CertMgr.exe in% ProgramFiles% \\ Microsoft SDK \\ Windows \\ v 7.0 \\ bin.</span><span class="sxs-lookup"><span data-stu-id="85450-126">If you get the WWSAPI examples by installing the Windows 7 SDK, you can find the MakeCert.exe and CertMgr.exe under %ProgramFiles%\\Microsoft SDKs\\Windows\\v7.0\\bin.</span></span>

<span data-ttu-id="85450-127">Eseguire l'installazione in cinque passaggi seguente dal prompt dei comandi (con privilegi elevati se si utilizza Windows Vista e versioni successive):</span><span class="sxs-lookup"><span data-stu-id="85450-127">Perform the following five-step setup from the command prompt (elevated if you are using Windows Vista and above):</span></span>

1.  <span data-ttu-id="85450-128">Generare un certificato autofirmato in modo che sia l'autorità di certificazione (CA) o l'emittente: **MakeCert.exe-SS root-SR LocalMachine-n "CN = fake-test-CA"-CY Authority-r-SK "CAKeyContainer"**</span><span class="sxs-lookup"><span data-stu-id="85450-128">Generate a self-signed certificate to be the certificate authority (CA) or issuer: **MakeCert.exe -ss Root -sr LocalMachine -n "CN=Fake-Test-CA" -cy authority -r -sk "CAKeyContainer"**</span></span>
2.  <span data-ttu-id="85450-129">Generare un certificato server usando il certificato precedente come emittente: **MakeCert.exe-SS My-SR LocalMachine-n "CN = localhost"-Sky Exchange-is root-IR LocalMachine-in fake-test-CA-SK "ServerKeyContainer"**</span><span class="sxs-lookup"><span data-stu-id="85450-129">Generate a server certificate using the previous certificate as the issuer: **MakeCert.exe -ss My -sr LocalMachine -n "CN=localhost" -sky exchange -is Root -ir LocalMachine -in Fake-Test-CA -sk "ServerKeyContainer"**</span></span>
3.  <span data-ttu-id="85450-130">Trovare l'identificazione personale (hash SHA-1 a 40 caratteri) del certificato server eseguendo uno dei comandi seguenti e cercare il certificato denominato localhost con Issuer fake-test-CA:</span><span class="sxs-lookup"><span data-stu-id="85450-130">Find the thumbprint (a 40-character SHA-1 hash) of the server certificate by running either of the following commands and search for the certificate named localhost with issuer Fake-Test-CA:</span></span>
    -   <span data-ttu-id="85450-131">**CertUtil.exe-archivia localhost**</span><span class="sxs-lookup"><span data-stu-id="85450-131">**CertUtil.exe -store My localhost**</span></span>
    -   <span data-ttu-id="85450-132">**CertMgr.exe-s-r LocalMachine My**</span><span class="sxs-lookup"><span data-stu-id="85450-132">**CertMgr.exe -s -r LocalMachine My**</span></span>
4.  <span data-ttu-id="85450-133">Registrare l'identificazione personale del certificato del server senza spazi con HTTP.SYS:</span><span class="sxs-lookup"><span data-stu-id="85450-133">Register the server certificate?s thumbprint with no spaces with HTTP.SYS:</span></span>
    -   <span data-ttu-id="85450-134">In Windows Vista e versioni successive (l'opzione "AppID" è un GUID arbitrario): **Netsh.exe http add sslcert ipport = 0.0.0.0:8443 appid = {00112233-4455-6677-8899-AABBCCDDEEFF}** certhash =<40CharacterThumbprint></span><span class="sxs-lookup"><span data-stu-id="85450-134">On Windows Vista and above (the "appid" option is an arbitrary GUID): **Netsh.exe http add sslcert ipport=0.0.0.0:8443 appid={00112233-4455-6677-8899-AABBCCDDEEFF}** certhash=<40CharacterThumbprint></span></span>
    -   <span data-ttu-id="85450-135">In Windows XP o 2003: **HttpCfg.exe impostare SSL-i 0.0.0.0:8443-h <40CharacterThumbprint>**</span><span class="sxs-lookup"><span data-stu-id="85450-135">On Windows XP or 2003: **HttpCfg.exe set ssl -i 0.0.0.0:8443 -h <40CharacterThumbprint>**</span></span>
5.  <span data-ttu-id="85450-136">Creare un utente locale: **net user "TestUserForBasicAuth" "TstPWD@ \* 4Bsic"/Add**</span><span class="sxs-lookup"><span data-stu-id="85450-136">Create a local user: **Net user "TestUserForBasicAuth" "TstPWD@\*4Bsic" /add**</span></span>

<span data-ttu-id="85450-137">Per pulire i certificati, l'associazione di certificati SSL e l'account utente creato nei passaggi precedenti, eseguire i comandi seguenti.</span><span class="sxs-lookup"><span data-stu-id="85450-137">To clean up the certificates, SSL certificate binding and the user account created in the previous steps, run the following commands.</span></span> <span data-ttu-id="85450-138">Nota Se sono presenti più certificati con lo stesso nome, CertMgr.exe necessario l'input prima di eliminarli.</span><span class="sxs-lookup"><span data-stu-id="85450-138">Note if there are multiple certificates of the same name, CertMgr.exe will need your input before deleting them.</span></span>

-   <span data-ttu-id="85450-139">**CertMgr.exe-del-c-n Fake-test-CA-s-r LocalMachine radice**</span><span class="sxs-lookup"><span data-stu-id="85450-139">**CertMgr.exe -del -c -n Fake-Test-CA -s -r LocalMachine Root**</span></span>
-   <span data-ttu-id="85450-140">**CertMgr.exe-del-c-n localhost-s-r LocalMachine My**</span><span class="sxs-lookup"><span data-stu-id="85450-140">**CertMgr.exe -del -c -n localhost -s -r LocalMachine My**</span></span>
-   <span data-ttu-id="85450-141">**Netsh.exe http delete sslcert ipport = 0.0.0.0:8443 (o HttpCfg.exe Delete SSL-i 0.0.0.0:8443)**</span><span class="sxs-lookup"><span data-stu-id="85450-141">**Netsh.exe http delete sslcert ipport=0.0.0.0:8443 (or HttpCfg.exe delete ssl -i 0.0.0.0:8443)**</span></span>
-   <span data-ttu-id="85450-142">**NET User "TestUserForBasicAuth"/Delete**</span><span class="sxs-lookup"><span data-stu-id="85450-142">**Net user "TestUserForBasicAuth" /delete**</span></span>

<span data-ttu-id="85450-143">Verificare che sia presente un solo certificato radice denominato fake-test-CA.</span><span class="sxs-lookup"><span data-stu-id="85450-143">Make sure there is only one root certificate named Fake-Test-CA.</span></span> <span data-ttu-id="85450-144">Se non si è certi, è sempre sicuro provare a pulire questi certificati usando i comandi di pulitura precedenti (e ignorare gli errori) prima di avviare l'installazione in cinque passaggi.</span><span class="sxs-lookup"><span data-stu-id="85450-144">If you are unsure, it?s always safe to try to clean up these certificates using the cleanup commands above (and ignore errors) before starting the five-step setup.</span></span>

 

 





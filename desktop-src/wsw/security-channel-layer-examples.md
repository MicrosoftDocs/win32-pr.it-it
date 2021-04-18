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
# <a name="security-channel-layer-examples"></a>Esempi di livelli di canale di sicurezza

Negli esempi seguenti viene illustrata la sicurezza nel [livello del canale](channel-layer-overview.md)

Sicurezza del trasporto Windows su TCP: client: [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md), server: [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md).

Sicurezza del trasporto Windows su Named Pipes: client: [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md), server: [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md).

Sicurezza del trasporto SSL: client: [HttpClientWithSslExample](httpclientwithsslexample.md), server: [HttpServerWithSslExample](httpserverwithsslexample.md).

Nome utente sulla sicurezza in modalità mista SSL: client: [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md), server: [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md).

Nome utente sulla sicurezza in modalità mista SSL: client: [HttpClientWithKerberosOverSslExample](httpclientwithkerberosoversslexample.md), server: [HttpServerWithKerberosOverSslExample](httpserverwithkerberosoversslexample.md).

Nome utente sulla sicurezza in modalità mista SSL: [MetadataImportWithUsernameOverSslExample](metadataimportwithusernameoversslexample.md). Token emesso sulla sicurezza in modalità mista SSL: [MetadataImportWithIssuedTokenOverSslExample](metadataimportwithissuedtokenoversslexample.md). Certificato X509 sulla sicurezza in modalità mista SSL: [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md).

## <a name="one-time-setup-for-security-samples"></a>One-Time installazione per gli esempi di sicurezza

Per eseguire gli esempi di sicurezza di WWSAPI, è necessario configurare i certificati client e server per SSL, oltre a un account utente locale per l'autenticazione dell'intestazione HTTP. Prima di iniziare, sono necessari gli strumenti seguenti:

-   MakeCert.exe (disponibile in Windows 7 SDK).
-   CertUtil.exe o CertMgr.exe (CertUtil.exe è disponibile negli SDK di Windows a partire da Windows Server 2003. CertMgr.exe è disponibile in Windows 7 SDK. È necessario solo uno di questi strumenti.
-   HttpCfg.exe: questa operazione è necessaria solo se si utilizza Windows 2003 o Windows XP. Questo strumento è disponibile negli strumenti di supporto di Windows XP SP2 e viene fornito anche con il CD di Windows Server 2003 Resource Kit Tools.

Se si ottengono gli esempi di WWSAPI installando Windows 7 SDK, è possibile trovare il MakeCert.exe e CertMgr.exe in% ProgramFiles% \\ Microsoft SDK \\ Windows \\ v 7.0 \\ bin.

Eseguire l'installazione in cinque passaggi seguente dal prompt dei comandi (con privilegi elevati se si utilizza Windows Vista e versioni successive):

1.  Generare un certificato autofirmato in modo che sia l'autorità di certificazione (CA) o l'emittente: **MakeCert.exe-SS root-SR LocalMachine-n "CN = fake-test-CA"-CY Authority-r-SK "CAKeyContainer"**
2.  Generare un certificato server usando il certificato precedente come emittente: **MakeCert.exe-SS My-SR LocalMachine-n "CN = localhost"-Sky Exchange-is root-IR LocalMachine-in fake-test-CA-SK "ServerKeyContainer"**
3.  Trovare l'identificazione personale (hash SHA-1 a 40 caratteri) del certificato server eseguendo uno dei comandi seguenti e cercare il certificato denominato localhost con Issuer fake-test-CA:
    -   **CertUtil.exe-archivia localhost**
    -   **CertMgr.exe-s-r LocalMachine My**
4.  Registrare l'identificazione personale del certificato del server senza spazi con HTTP.SYS:
    -   In Windows Vista e versioni successive (l'opzione "AppID" è un GUID arbitrario): **Netsh.exe http add sslcert ipport = 0.0.0.0:8443 appid = {00112233-4455-6677-8899-AABBCCDDEEFF}** certhash =<40CharacterThumbprint>
    -   In Windows XP o 2003: **HttpCfg.exe impostare SSL-i 0.0.0.0:8443-h <40CharacterThumbprint>**
5.  Creare un utente locale: **net user "TestUserForBasicAuth" "TstPWD@ \* 4Bsic"/Add**

Per pulire i certificati, l'associazione di certificati SSL e l'account utente creato nei passaggi precedenti, eseguire i comandi seguenti. Nota Se sono presenti più certificati con lo stesso nome, CertMgr.exe necessario l'input prima di eliminarli.

-   **CertMgr.exe-del-c-n Fake-test-CA-s-r LocalMachine radice**
-   **CertMgr.exe-del-c-n localhost-s-r LocalMachine My**
-   **Netsh.exe http delete sslcert ipport = 0.0.0.0:8443 (o HttpCfg.exe Delete SSL-i 0.0.0.0:8443)**
-   **NET User "TestUserForBasicAuth"/Delete**

Verificare che sia presente un solo certificato radice denominato fake-test-CA. Se non si è certi, è sempre sicuro provare a pulire questi certificati usando i comandi di pulitura precedenti (e ignorare gli errori) prima di avviare l'installazione in cinque passaggi.

 

 





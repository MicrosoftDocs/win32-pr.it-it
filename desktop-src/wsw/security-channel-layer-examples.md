---
title: Esempi di livello del canale di sicurezza
description: Gli esempi seguenti illustrano la sicurezza nel livello canale.
ms.assetid: ac4f0275-4783-411d-98da-2c5a1a169dcc
keywords:
- esempi di sicurezza
- esempi di sicurezza, configurazione
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d130bc7e0e4250107c6e331a43f7d5a13786929c37bd998177ee587c2f29049
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118192772"
---
# <a name="security-channel-layer-examples"></a>Esempi di livello del canale di sicurezza

Gli esempi seguenti illustrano la sicurezza nel [livello canale](channel-layer-overview.md)

Windows sicurezza del trasporto su TCP: Client: [RequestReplyTcpClientWithWindowsTransportSecurityExample](requestreplytcpclientwithwindowstransportsecurityexample.md), Server: [RequestReplyTcpServerWithWindowsTransportSecurityExample](requestreplytcpserverwithwindowstransportsecurityexample.md).

Windows sicurezza del trasporto su named pipe: Client: [RequestReplyNamedPipesClientWithWindowsTransportSecurityExample](requestreplynamedpipesclientwithwindowstransportsecurityexample.md), Server: [RequestReplyNamedPipesServerWithWindowsTransportSecurityExample](requestreplynamedpipesserverwithwindowstransportsecurityexample.md).

Sicurezza del trasporto SSL: Client: [HttpClientWithSslExample](httpclientwithsslexample.md), Server: [HttpServerWithSslExample](httpserverwithsslexample.md).

Nome utente su sicurezza in modalità mista SSL: Client: [HttpClientWithUsernameOverSslExample](httpclientwithusernameoversslexample.md), Server: [HttpServerWithUsernameOverSslExample](httpserverwithusernameoversslexample.md).

Nome utente su sicurezza in modalità mista SSL: Client: [HttpClientWithKerberosOverSslExample](httpclientwithkerberosoversslexample.md), Server: [HttpServerWithKerberosOverSslExample](httpserverwithkerberosoversslexample.md).

Nome utente su sicurezza in modalità mista SSL: [MetadataImportWithUsernameOverSslExample](metadataimportwithusernameoversslexample.md). Token rilasciato sulla sicurezza in modalità mista SSL: [MetadataImportWithIssuedTokenOverSslExample](metadataimportwithissuedtokenoversslexample.md). Certificato X509 su sicurezza in modalità mista SSL: [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md).

## <a name="one-time-setup-for-security-samples"></a>One-Time programma di installazione per gli esempi di sicurezza

Per eseguire esempi di sicurezza WWSAPI, è necessario configurare i certificati client e server per SSL, nonché un account utente locale per l'autenticazione dell'intestazione HTTP. Prima di iniziare, sono necessari gli strumenti seguenti:

-   MakeCert.exe (disponibile nell'SDK Windows 7).
-   CertUtil.exe o CertMgr.exe (CertUtil.exe è disponibile negli SDK Windows a partire da Windows Server 2003. CertMgr.exe è disponibile nell'SDK Windows 7. È necessario solo uno di questi strumenti.
-   HttpCfg.exe: questa operazione è necessaria solo se si usa Windows 2003 o Windows XP. Questo strumento è disponibile in Windows strumenti di supporto di XP SP2 e viene fornito anche con il CD degli strumenti di Windows Server 2003 Resource Kit).

Se si ottengono gli esempi WWSAPI installando Windows 7 SDK, è possibile trovare MakeCert.exe e CertMgr.exe in %ProgramFiles% \\ Microsoft SDKs \\ Windows \\ v7.0 \\ bin.

Eseguire la configurazione in cinque passaggi seguente dal prompt dei comandi (con privilegi elevati se si usa Windows Vista e versioni successive):

1.  Generare un certificato autofirmato come autorità di certificazione (CA) o autorità di certificazione: **MakeCert.exe -ss Root -sr LocalMachine -n "CN=Fake-Test-CA" -cy authority -r -sk "CAKeyContainer"**
2.  Generare un certificato server usando il certificato precedente come autorità di certificazione: **MakeCert.exe -ss My -sr LocalMachine -n "CN=localhost" -sky exchange -is Root -ir LocalMachine -in Fake-Test-CA -sk "ServerKeyContainer"**
3.  Trovare l'identificazione personale (un hash SHA-1 di 40 caratteri) del certificato server eseguendo uno dei comandi seguenti e cercare il certificato denominato localhost con autorità di certificazione Fake-Test-CA:
    -   **CertUtil.exe -store My localhost**
    -   **CertMgr.exe -s -r LocalMachine My**
4.  Registrare l'identificazione personale del certificato server senza spazi HTTP.SYS:
    -   In Windows Vista e versioni successive (l'opzione "appid" è un GUID arbitrario): **Netsh.exe http add sslcert ipport=0.0.0.0:8443 appid={001 12233-4455-6677-8899-AABBCCDDEEFF}** certhash=<40CharacterThumbprint>
    -   In Windows XP o 2003: **HttpCfg.exe set ssl -i 0.0.0.0:8443 -h <40CharacterThumbprint>**
5.  Creare un utente locale: **Net user "TestUserForBasicAuth" "TstPWD@ \* 4Bsic" /add**

Per pulire i certificati, l'associazione di certificati SSL e l'account utente creato nei passaggi precedenti, eseguire i comandi seguenti. Si noti che se sono presenti più certificati con lo stesso nome, CertMgr.exe sarà necessario l'input prima di eliminarli.

-   **CertMgr.exe -del -c -n Fake-Test-CA -s -r LocalMachine Root**
-   **CertMgr.exe -del -c -n localhost -s -r LocalMachine My**
-   **Netsh.exe http delete sslcert ipport=0.0.0.0:8443 (o HttpCfg.exe delete ssl -i 0.0.0.0:8443)**
-   **Utente di rete "TestUserForBasicAuth" /delete**

Assicurarsi che sia presente un solo certificato radice denominato Fake-Test-CA. In caso di dubbi, è sempre possibile provare a pulire questi certificati usando i comandi di pulizia precedenti (e ignorare gli errori) prima di avviare la configurazione in cinque passaggi.

 

 





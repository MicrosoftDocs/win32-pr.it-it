---
description: Esempi avanzati di Winsock con le estensioni secure socket
ms.assetid: 9c429363-f9bb-4394-89be-f87507f5cbdd
title: Esempi avanzati di Winsock con le estensioni secure socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ead38a7e62be527e91474ac921803327647ca6cefd1ec68778d03e1c68c1bf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412171"
---
# <a name="advanced-winsock-samples-using-secure-socket-extensions"></a>Esempi avanzati di Winsock con le estensioni secure socket

## <a name="secure-tcp-client-and-server-sample"></a>Esempio di client e server TCP sicuri

In Microsoft Windows Software Development Kit (SDK) è incluso un esempio Winsock più avanzato che illustra l'uso delle estensioni del socket sicuro. L'esempio include un client TCP e un server che si connettono in modo sicuro usando Winsock e le estensioni del socket sicuro.

Per impostazione predefinita, il codice sorgente di esempio Winsock viene installato nella directory seguente:

*C: \\ Programmi Microsoft SDK Windows \\ \\ \\ v6.0 \\ Samples \\ NetDs \\ winsock*

Un esempio si trova nella cartella seguente:

*securesocket*

Il codice di esempio è suddiviso in directory separate, come descritto di seguito:

-   stcpclient: cartella che contiene il codice client TCP sicuro.
-   stcpcommon: cartella che contiene il codice della libreria comune condiviso tra il client TCP sicuro e il server.
-   stcpserver: cartella che contiene il codice del server TCP sicuro.

Si noti che gli esempi devono essere eseguiti in due computer diversi che eseguono Windows Vista o versioni successive. È inoltre necessario effettuare il provisioning delle credenziali IPsec in entrambi i computer perché la connessione riesca, perché l'esempio usa IPsec per proteggere il traffico. Per altre informazioni sulla configurazione delle credenziali [IPsec,](/windows/desktop/FWP/ipsec-configuration) vedere la documentazione di Configurazione IPsec.

La compilazione dell'esempio genererà due file eseguibili:

*stcpclient.exe* e *stcpserver.exe*.

Copiare *stcpclient.exe* computer A e *copiare* stcpserver.exenel computer B. Nel computer B avviare il server TCP eseguendo quanto segue in un prompt dei comandi:

**stcpserver.exe**

Eseguire il comando seguente per altre opzioni di utilizzo per il server:

**stcpserver.exe /?**

Nel computer A avviare quindi il client TCP eseguendo quanto segue in un prompt dei comandi:

**stcpclient.exe <-qualified-DNS-name-for-machine-B>**

A questo punto la connessione deve essere stabilita in modo sicuro.

Eseguire il comando seguente per altre opzioni di utilizzo per il client:

**stcpclient.exe /?**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni Windows filtering platform](/windows/desktop/FWP/about-windows-filtering-platform)
</dt> <dt>

[Applicazione a livello di applicazione (ALE)](/windows/desktop/FWP/application-layer-enforcement--ale-)
</dt> <dt>

[Configurazione IPsec](/windows/desktop/FWP/ipsec-configuration)
</dt> <dt>

[Funzioni IPsec](/windows/desktop/FWP/fwp-ipsec-functions)
</dt> <dt>

[Uso delle estensioni secure socket](using-secure-socket-extensions.md)
</dt> <dt>

[Security Support Provider Interface (SSPI)](/windows/desktop/Rpc/security-support-provider-interface-sspi-)
</dt> <dt>

[Piattaforma filtro Windows](/windows/desktop/FWP/windows-filtering-platform-start-page)
</dt> <dt>

[Windows Funzioni api della piattaforma di filtro](/windows/desktop/FWP/fwp-functions)
</dt> <dt>

[Winsock Secure Socket Extensions](winsock-secure-socket-extensions.md)
</dt> </dl>

 

 

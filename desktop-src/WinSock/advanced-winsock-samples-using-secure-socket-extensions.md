---
description: Esempi avanzati di Winsock con estensioni Secure Socket
ms.assetid: 9c429363-f9bb-4394-89be-f87507f5cbdd
title: Esempi avanzati di Winsock con estensioni Secure Socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6701809ad97c7d39acf1f0eae646e7555e5c967f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966683"
---
# <a name="advanced-winsock-samples-using-secure-socket-extensions"></a>Esempi avanzati di Winsock con estensioni Secure Socket

## <a name="secure-tcp-client-and-server-sample"></a>Esempio di client e server TCP sicuro

Con il Software Development Kit (SDK) di Microsoft Windows è incluso un esempio Winsock più avanzato che illustra l'uso delle estensioni Secure Socket. L'esempio include un client e un server TCP che si connettono in modo sicuro tramite Winsock e le estensioni Secure Socket.

Per impostazione predefinita, il codice sorgente di esempio Winsock viene installato nella directory seguente:

*C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 6.0 \\ esempi \\ NetDs \\ Winsock*

Un esempio si trova nella cartella seguente:

*securesocket*

Il codice di esempio viene suddiviso in directory separate, come descritto di seguito:

-   stcpclient: cartella che contiene il codice client TCP protetto.
-   stcpcommon: cartella che contiene il codice di libreria comune condiviso tra il client e il server TCP protetti.
-   stcpserver: cartella che contiene il codice del server TCP protetto.

Si noti che gli esempi devono essere eseguiti in due computer diversi che eseguono Windows Vista o versioni successive. Inoltre, è necessario eseguire il provisioning delle credenziali IPsec in entrambi i computer per la connessione perché l'esempio utilizza IPsec per la protezione del traffico. Per ulteriori informazioni sull'impostazione delle credenziali IPsec, consultare la documentazione sulla [configurazione IPSec](/windows/desktop/FWP/ipsec-configuration) .

La compilazione dell'esempio genererà due file eseguibili:

*stcpclient.exe* e *stcpserver.exe*.

Copiare *stcpclient.exe* nel computer a e copiare *stcpserver.exe* nel computer B. Nel computer B avviare il server TCP eseguendo il comando seguente in un prompt dei comandi:

**stcpserver.exe**

Per altre opzioni di utilizzo per il server, eseguire il comando seguente:

**stcpserver.exe/?**

Quindi, nel computer A, avviare il client TCP eseguendo il comando seguente in un prompt dei comandi:

**stcpclient.exe <completo-DNS-Name-for-Machine-B>**

A questo punto la connessione deve essere stabilita in modo sicuro.

Eseguire il comando seguente per altre opzioni di utilizzo per il client:

**stcpclient.exe/?**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulla piattaforma filtro Windows](/windows/desktop/FWP/about-windows-filtering-platform)
</dt> <dt>

[Application Layer Enforcement (ALE)](/windows/desktop/FWP/application-layer-enforcement--ale-)
</dt> <dt>

[Configurazione IPsec](/windows/desktop/FWP/ipsec-configuration)
</dt> <dt>

[Funzioni IPsec](/windows/desktop/FWP/fwp-ipsec-functions)
</dt> <dt>

[Uso delle estensioni Secure Socket](using-secure-socket-extensions.md)
</dt> <dt>

[Security Support Provider Interface (SSPI)](/windows/desktop/Rpc/security-support-provider-interface-sspi-)
</dt> <dt>

[Piattaforma filtro Windows](/windows/desktop/FWP/windows-filtering-platform-start-page)
</dt> <dt>

[Funzioni API della piattaforma filtro Windows](/windows/desktop/FWP/fwp-functions)
</dt> <dt>

[Estensioni Secure socket Winsock](winsock-secure-socket-extensions.md)
</dt> </dl>

 

 

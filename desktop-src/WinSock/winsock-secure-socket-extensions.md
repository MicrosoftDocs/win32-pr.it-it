---
description: Le estensioni Secure Socket per Winsock consentono a un'applicazione socket di controllare la sicurezza del traffico in una rete.
ms.assetid: 023a9f96-814f-40c3-a186-ae0a0c9baef2
title: Estensioni Secure socket Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b62ee593b3abbb3bb0f8dbf27b79d6868f04fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049476"
---
# <a name="winsock-secure-socket-extensions"></a>Estensioni Secure socket Winsock

Le estensioni Secure Socket per Winsock consentono a un'applicazione socket di controllare la sicurezza del traffico in una rete. Queste estensioni consentono a un'applicazione di fornire i criteri di sicurezza e i requisiti per il traffico di rete e di eseguire query sulle impostazioni di sicurezza applicate. Ad esempio, un'applicazione può usare queste estensioni per eseguire una query sul token di sicurezza peer che può essere usato per eseguire controlli di accesso a livello di applicazione.

Le estensioni Secure Socket sono progettate per integrare i servizi forniti da IPsec e altri protocolli di sicurezza con il Framework Winsock. Prima di Windows Vista, in Windows Server 2003 e Windows XP, IPsec è stato configurato da un amministratore tramite criteri locali e di dominio. In Windows Vista, le estensioni Secure Socket consentono invece alle applicazioni di configurare completamente o parzialmente e controllare la sicurezza del traffico di rete a livello di socket.

Le applicazioni possono già proteggere il traffico di rete usando le API pubbliche, ad esempio la gestione IPsec, Windows Filtering Platform e Security Support Provider Interface (SSPI). Tuttavia, l'uso di queste API può rendere più difficile lo sviluppo dell'applicazione e potrebbe renderla più difficile da configurare e distribuire. Le estensioni di socket protette Winsock sono state progettate per semplificare lo sviluppo di applicazioni di rete che richiedono il traffico di rete sicuro, consentendo a Winsock di gestire la maggior parte della complessità.

Queste estensioni socket protette sono disponibili in Windows Vista e versioni successive.

## <a name="secure-socket-functions"></a>Funzioni socket protette

Le funzioni di estensione Secure Socket sono le seguenti:

-   [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname)
-   [**WSAImpersonateSocketPeer**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer)
-   [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity)
-   [**WSARevertImpersonation**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation)
-   [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)
-   [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity)

> [!Note]  
> Le funzioni socket protette supportano attualmente solo il protocollo IPsec e sono disponibili in Windows Vista e versioni successive.

 

Le strutture e le enumerazioni utilizzate dalle funzioni socket protette sono le seguenti:

-   [**\_ \_ Nome destinazione peer del socket \_**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_peer_target_name)
-   [**\_protocollo di sicurezza socket \_**](/windows/desktop/api/Mstcpip/ne-mstcpip-socket_security_protocol)
-   [**\_informazioni sulle \_ query di sicurezza socket \_**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_query_info)
-   [**\_modello di \_ query di sicurezza socket \_**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_query_template)
-   [**\_impostazioni di sicurezza socket \_**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_settings)
-   [**\_impostazioni di sicurezza socket \_ \_ IPSec**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_settings_ipsec)

Le funzioni socket protette sono semplici da usare per le applicazioni normali e sono sufficientemente flessibili per le applicazioni che richiedono un elevato livello di controllo sulla sicurezza. Queste funzioni consentono di evitare che il meccanismo di sicurezza sottostante sia nascosto dall'applicazione. Un'applicazione può specificare requisiti di sicurezza generici e consentire all'amministratore di controllare il protocollo di sicurezza utilizzato per supportare i requisiti. Sebbene sia possibile estendere queste funzioni per aggiungere altri protocolli di sicurezza, attualmente solo IPsec si integra con le funzioni socket protette.

La funzione [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) consente a un'applicazione di abilitare la sicurezza e di applicare le impostazioni di sicurezza prima che venga stabilita una connessione.

La funzione [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) consente a un'applicazione di specificare il nome di destinazione corrispondente a un'entità peer. Il protocollo di sicurezza selezionato utilizzerà queste informazioni per l'autenticazione del peer. Questa funzionalità risolve i problemi relativi agli attacchi man-in-the-Middle attendibili.

La funzione [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname) viene usata per eliminare un nome peer specificato in precedenza per un socket.

Una volta stabilita una connessione, la funzione [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) consente a un'applicazione di eseguire query sulle proprietà di sicurezza della connessione, che può includere l'accesso peer o il token di accesso del computer.

Una volta stabilita una connessione, la funzione [**WSAImpersonateSocketPeer**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer) consente a un'applicazione di rappresentare l'entità di sicurezza corrispondente a un peer del socket per eseguire l'autorizzazione a livello di applicazione.

[**WSARevertImpersonation**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation) consente a un'applicazione di terminare la rappresentazione di un peer di socket.

## <a name="secure-socket-architecture"></a>Architettura Secure Socket

![architettura di base delle estensioni del socket sicuro Winsock](images/ss-arch.png)

-   Un'applicazione chiama le funzioni socket sicure per impostare o eseguire query sulle impostazioni di sicurezza per un socket.
-   Le funzioni socket protette sono un set di funzioni di estensione indipendenti dai tipi che eseguono il wrapping delle chiamate alla funzione [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) utilizzando valori appena definiti per il parametro *DwIoControlCode* disponibile in Windows Vista e versioni successive. Questi IOCTL vengono gestiti dallo stack di rete.
-   Lo stack di rete indirizza la chiamata a [Application Layer Enforcement (ale)](../fwp/application-layer-enforcement--ale-.md) insieme all'handle dell'endpoint. Per le funzioni [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname), [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)e [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) , ale configurerà le impostazioni dell'applicazione nell'endpoint locale. Per la funzione [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) , ale leggerà le informazioni richieste dagli endpoint locali e remoti applicabili.
-   In base agli eventi socket, Application Layer Enforcement (ALE) applica i criteri per l'architettura Secure Socket usando la piattaforma filtro Windows. Per ulteriori informazioni, vedere [About Windows Filtering Platform](../fwp/about-windows-filtering-platform.md) and [Application Layer Enforcement (ale)](../fwp/application-layer-enforcement--ale-.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulla piattaforma filtro Windows](../fwp/about-windows-filtering-platform.md)
</dt> <dt>

[Esempi avanzati di Winsock con estensioni Secure Socket](advanced-winsock-samples-using-secure-socket-extensions.md)
</dt> <dt>

[Application Layer Enforcement (ALE)](../fwp/application-layer-enforcement--ale-.md)
</dt> <dt>

[Configurazione IPsec](../fwp/ipsec-configuration.md)
</dt> <dt>

[Funzioni IPsec](../fwp/fwp-ipsec-functions.md)
</dt> <dt>

[Programmazione Winsock sicura](secure-winsock-programming.md)
</dt> <dt>

[Security Support Provider Interface (SSPI)](../rpc/security-support-provider-interface-sspi-.md)
</dt> <dt>

[Uso delle estensioni Secure Socket](using-secure-socket-extensions.md)
</dt> <dt>

[Piattaforma filtro Windows](../fwp/windows-filtering-platform-start-page.md)
</dt> <dt>

[Funzioni API della piattaforma filtro Windows](../fwp/fwp-functions.md)
</dt> </dl>

 

 

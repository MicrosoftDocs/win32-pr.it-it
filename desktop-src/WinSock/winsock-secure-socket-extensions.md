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
# <a name="winsock-secure-socket-extensions"></a><span data-ttu-id="b894a-103">Estensioni Secure socket Winsock</span><span class="sxs-lookup"><span data-stu-id="b894a-103">Winsock Secure Socket Extensions</span></span>

<span data-ttu-id="b894a-104">Le estensioni Secure Socket per Winsock consentono a un'applicazione socket di controllare la sicurezza del traffico in una rete.</span><span class="sxs-lookup"><span data-stu-id="b894a-104">The secure socket extensions to Winsock allow a socket application to control the security of their traffic over a network.</span></span> <span data-ttu-id="b894a-105">Queste estensioni consentono a un'applicazione di fornire i criteri di sicurezza e i requisiti per il traffico di rete e di eseguire query sulle impostazioni di sicurezza applicate.</span><span class="sxs-lookup"><span data-stu-id="b894a-105">These extensions allow an application to provide security policy and requirements for their network traffic, and query the security settings applied.</span></span> <span data-ttu-id="b894a-106">Ad esempio, un'applicazione può usare queste estensioni per eseguire una query sul token di sicurezza peer che può essere usato per eseguire controlli di accesso a livello di applicazione.</span><span class="sxs-lookup"><span data-stu-id="b894a-106">For example, an application can use these extensions to query the peer security token that can be used to perform application level access checks.</span></span>

<span data-ttu-id="b894a-107">Le estensioni Secure Socket sono progettate per integrare i servizi forniti da IPsec e altri protocolli di sicurezza con il Framework Winsock.</span><span class="sxs-lookup"><span data-stu-id="b894a-107">The secure socket extensions are intended to integrate the services provided by IPsec and other security protocols with the Winsock framework.</span></span> <span data-ttu-id="b894a-108">Prima di Windows Vista, in Windows Server 2003 e Windows XP, IPsec è stato configurato da un amministratore tramite criteri locali e di dominio.</span><span class="sxs-lookup"><span data-stu-id="b894a-108">Prior to Windows Vista, on Windows Server 2003 and Windows XP, IPsec has been configured by an administrator via local and domain policies.</span></span> <span data-ttu-id="b894a-109">In Windows Vista, le estensioni Secure Socket consentono invece alle applicazioni di configurare completamente o parzialmente e controllare la sicurezza del traffico di rete a livello di socket.</span><span class="sxs-lookup"><span data-stu-id="b894a-109">On Windows Vista, the secure socket extensions instead allow applications to entirely or partially configure and control the security of their network traffic at the socket level.</span></span>

<span data-ttu-id="b894a-110">Le applicazioni possono già proteggere il traffico di rete usando le API pubbliche, ad esempio la gestione IPsec, Windows Filtering Platform e Security Support Provider Interface (SSPI).</span><span class="sxs-lookup"><span data-stu-id="b894a-110">Applications can already secure network traffic by using public APIs, such as IPsec management, Windows Filtering Platform and Security Support Provider Interface (SSPI).</span></span> <span data-ttu-id="b894a-111">Tuttavia, l'uso di queste API può rendere più difficile lo sviluppo dell'applicazione e potrebbe renderla più difficile da configurare e distribuire.</span><span class="sxs-lookup"><span data-stu-id="b894a-111">However, using these APIs may make the application more difficult to develop, and may make it more difficult to configure and deploy.</span></span> <span data-ttu-id="b894a-112">Le estensioni di socket protette Winsock sono state progettate per semplificare lo sviluppo di applicazioni di rete che richiedono il traffico di rete sicuro, consentendo a Winsock di gestire la maggior parte della complessità.</span><span class="sxs-lookup"><span data-stu-id="b894a-112">The Winsock secure socket extensions have been designed to simplify the development of network applications that require secure network traffic by letting Winsock handle most of the complexity.</span></span>

<span data-ttu-id="b894a-113">Queste estensioni socket protette sono disponibili in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b894a-113">These secure socket extensions are available on Windows Vista and later.</span></span>

## <a name="secure-socket-functions"></a><span data-ttu-id="b894a-114">Funzioni socket protette</span><span class="sxs-lookup"><span data-stu-id="b894a-114">Secure Socket Functions</span></span>

<span data-ttu-id="b894a-115">Le funzioni di estensione Secure Socket sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="b894a-115">The secure socket extension functions are as follows:</span></span>

-   [<span data-ttu-id="b894a-116">**WSADeleteSocketPeerTargetName**</span><span class="sxs-lookup"><span data-stu-id="b894a-116">**WSADeleteSocketPeerTargetName**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname)
-   [<span data-ttu-id="b894a-117">**WSAImpersonateSocketPeer**</span><span class="sxs-lookup"><span data-stu-id="b894a-117">**WSAImpersonateSocketPeer**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer)
-   [<span data-ttu-id="b894a-118">**WSAQuerySocketSecurity**</span><span class="sxs-lookup"><span data-stu-id="b894a-118">**WSAQuerySocketSecurity**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity)
-   [<span data-ttu-id="b894a-119">**WSARevertImpersonation**</span><span class="sxs-lookup"><span data-stu-id="b894a-119">**WSARevertImpersonation**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation)
-   [<span data-ttu-id="b894a-120">**WSASetSocketPeerTargetName**</span><span class="sxs-lookup"><span data-stu-id="b894a-120">**WSASetSocketPeerTargetName**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)
-   [<span data-ttu-id="b894a-121">**WSASetSocketSecurity**</span><span class="sxs-lookup"><span data-stu-id="b894a-121">**WSASetSocketSecurity**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity)

> [!Note]  
> <span data-ttu-id="b894a-122">Le funzioni socket protette supportano attualmente solo il protocollo IPsec e sono disponibili in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b894a-122">The secure socket functions currently support only the IPsec protocol and are available on Windows Vista and later.</span></span>

 

<span data-ttu-id="b894a-123">Le strutture e le enumerazioni utilizzate dalle funzioni socket protette sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="b894a-123">The structures and enumerations used by the secure socket functions are as follows:</span></span>

-   [<span data-ttu-id="b894a-124">**\_ \_ Nome destinazione peer del socket \_**</span><span class="sxs-lookup"><span data-stu-id="b894a-124">**SOCKET\_PEER\_TARGET\_NAME**</span></span>](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_peer_target_name)
-   [<span data-ttu-id="b894a-125">**\_protocollo di sicurezza socket \_**</span><span class="sxs-lookup"><span data-stu-id="b894a-125">**SOCKET\_SECURITY\_PROTOCOL**</span></span>](/windows/desktop/api/Mstcpip/ne-mstcpip-socket_security_protocol)
-   [<span data-ttu-id="b894a-126">**\_informazioni sulle \_ query di sicurezza socket \_**</span><span class="sxs-lookup"><span data-stu-id="b894a-126">**SOCKET\_SECURITY\_QUERY\_INFO**</span></span>](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_query_info)
-   [<span data-ttu-id="b894a-127">**\_modello di \_ query di sicurezza socket \_**</span><span class="sxs-lookup"><span data-stu-id="b894a-127">**SOCKET\_SECURITY\_QUERY\_TEMPLATE**</span></span>](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_query_template)
-   [<span data-ttu-id="b894a-128">**\_impostazioni di sicurezza socket \_**</span><span class="sxs-lookup"><span data-stu-id="b894a-128">**SOCKET\_SECURITY\_SETTINGS**</span></span>](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_settings)
-   [<span data-ttu-id="b894a-129">**\_impostazioni di sicurezza socket \_ \_ IPSec**</span><span class="sxs-lookup"><span data-stu-id="b894a-129">**SOCKET\_SECURITY\_SETTINGS\_IPSEC**</span></span>](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_settings_ipsec)

<span data-ttu-id="b894a-130">Le funzioni socket protette sono semplici da usare per le applicazioni normali e sono sufficientemente flessibili per le applicazioni che richiedono un elevato livello di controllo sulla sicurezza.</span><span class="sxs-lookup"><span data-stu-id="b894a-130">The secure socket functions are simple to use for normal applications and are flexible enough for applications that need a high degree of control over their security.</span></span> <span data-ttu-id="b894a-131">Queste funzioni consentono di evitare che il meccanismo di sicurezza sottostante sia nascosto dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b894a-131">These functions make it possible to keep the underlying security mechanism hidden from the application.</span></span> <span data-ttu-id="b894a-132">Un'applicazione può specificare requisiti di sicurezza generici e consentire all'amministratore di controllare il protocollo di sicurezza utilizzato per supportare i requisiti.</span><span class="sxs-lookup"><span data-stu-id="b894a-132">An application can specify generic security requirements and let the administrator control the security protocol that is used to support the requirements.</span></span> <span data-ttu-id="b894a-133">Sebbene sia possibile estendere queste funzioni per aggiungere altri protocolli di sicurezza, attualmente solo IPsec si integra con le funzioni socket protette.</span><span class="sxs-lookup"><span data-stu-id="b894a-133">While it is possible to extend these functions to add other security protocols, currently only IPsec integrates with the secure socket functions.</span></span>

<span data-ttu-id="b894a-134">La funzione [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) consente a un'applicazione di abilitare la sicurezza e di applicare le impostazioni di sicurezza prima che venga stabilita una connessione.</span><span class="sxs-lookup"><span data-stu-id="b894a-134">The [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) function allows an application to enable security and apply security settings before a connection is established.</span></span>

<span data-ttu-id="b894a-135">La funzione [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) consente a un'applicazione di specificare il nome di destinazione corrispondente a un'entità peer.</span><span class="sxs-lookup"><span data-stu-id="b894a-135">The [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) function allows an application to specify the target name corresponding to a peer entity.</span></span> <span data-ttu-id="b894a-136">Il protocollo di sicurezza selezionato utilizzerà queste informazioni per l'autenticazione del peer.</span><span class="sxs-lookup"><span data-stu-id="b894a-136">The selected security protocol will use this information when authenticating the peer.</span></span> <span data-ttu-id="b894a-137">Questa funzionalità risolve i problemi relativi agli attacchi man-in-the-Middle attendibili.</span><span class="sxs-lookup"><span data-stu-id="b894a-137">This feature addresses concerns about trusted man-in-the-middle attacks.</span></span>

<span data-ttu-id="b894a-138">La funzione [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname) viene usata per eliminare un nome peer specificato in precedenza per un socket.</span><span class="sxs-lookup"><span data-stu-id="b894a-138">The [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname) function is used to delete a previously specified peer name for a socket.</span></span>

<span data-ttu-id="b894a-139">Una volta stabilita una connessione, la funzione [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) consente a un'applicazione di eseguire query sulle proprietà di sicurezza della connessione, che può includere l'accesso peer o il token di accesso del computer.</span><span class="sxs-lookup"><span data-stu-id="b894a-139">After a connection is established, the [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) function allows an application to query the security properties of the connection, which can include the peer access or computer access token.</span></span>

<span data-ttu-id="b894a-140">Una volta stabilita una connessione, la funzione [**WSAImpersonateSocketPeer**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer) consente a un'applicazione di rappresentare l'entità di sicurezza corrispondente a un peer del socket per eseguire l'autorizzazione a livello di applicazione.</span><span class="sxs-lookup"><span data-stu-id="b894a-140">After a connection is established, the [**WSAImpersonateSocketPeer**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer) function allows an application to impersonate the security principal corresponding to a socket peer in order to perform application-level authorization.</span></span>

<span data-ttu-id="b894a-141">[**WSARevertImpersonation**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation) consente a un'applicazione di terminare la rappresentazione di un peer di socket.</span><span class="sxs-lookup"><span data-stu-id="b894a-141">The [**WSARevertImpersonation**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation) allows an application to terminate the impersonation of a socket peer.</span></span>

## <a name="secure-socket-architecture"></a><span data-ttu-id="b894a-142">Architettura Secure Socket</span><span class="sxs-lookup"><span data-stu-id="b894a-142">Secure Socket Architecture</span></span>

![architettura di base delle estensioni del socket sicuro Winsock](images/ss-arch.png)

-   <span data-ttu-id="b894a-144">Un'applicazione chiama le funzioni socket sicure per impostare o eseguire query sulle impostazioni di sicurezza per un socket.</span><span class="sxs-lookup"><span data-stu-id="b894a-144">An application calls the secure socket functions to set or query security settings for a socket.</span></span>
-   <span data-ttu-id="b894a-145">Le funzioni socket protette sono un set di funzioni di estensione indipendenti dai tipi che eseguono il wrapping delle chiamate alla funzione [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) utilizzando valori appena definiti per il parametro *DwIoControlCode* disponibile in Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b894a-145">The secure socket functions are a set of type-safe extension functions that wrap calls to the [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) function using newly-defined values for the *dwIoControlCode* parameter available on Windows Vista and later.</span></span> <span data-ttu-id="b894a-146">Questi IOCTL vengono gestiti dallo stack di rete.</span><span class="sxs-lookup"><span data-stu-id="b894a-146">These IOCTLs are handled by the network stack.</span></span>
-   <span data-ttu-id="b894a-147">Lo stack di rete indirizza la chiamata a [Application Layer Enforcement (ale)](../fwp/application-layer-enforcement--ale-.md) insieme all'handle dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="b894a-147">The network stack will direct the call to [Application Layer Enforcement (ALE)](../fwp/application-layer-enforcement--ale-.md) along with the endpoint handle.</span></span> <span data-ttu-id="b894a-148">Per le funzioni [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname), [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)e [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) , ale configurerà le impostazioni dell'applicazione nell'endpoint locale.</span><span class="sxs-lookup"><span data-stu-id="b894a-148">For the [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname), [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname), and [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) functions, ALE will configure the application's settings on the local endpoint.</span></span> <span data-ttu-id="b894a-149">Per la funzione [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) , ale leggerà le informazioni richieste dagli endpoint locali e remoti applicabili.</span><span class="sxs-lookup"><span data-stu-id="b894a-149">For the [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) function, ALE will read the requested information from applicable local and remote endpoints.</span></span>
-   <span data-ttu-id="b894a-150">In base agli eventi socket, Application Layer Enforcement (ALE) applica i criteri per l'architettura Secure Socket usando la piattaforma filtro Windows.</span><span class="sxs-lookup"><span data-stu-id="b894a-150">Based on socket events, Application Layer Enforcement (ALE) enforces policies for the secure socket architecture using the Windows Filtering Platform.</span></span> <span data-ttu-id="b894a-151">Per ulteriori informazioni, vedere [About Windows Filtering Platform](../fwp/about-windows-filtering-platform.md) and [Application Layer Enforcement (ale)](../fwp/application-layer-enforcement--ale-.md).</span><span class="sxs-lookup"><span data-stu-id="b894a-151">For more information, see [About Windows Filtering Platform](../fwp/about-windows-filtering-platform.md) and [Application Layer Enforcement (ALE)](../fwp/application-layer-enforcement--ale-.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b894a-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b894a-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b894a-153">Informazioni sulla piattaforma filtro Windows</span><span class="sxs-lookup"><span data-stu-id="b894a-153">About Windows Filtering Platform</span></span>](../fwp/about-windows-filtering-platform.md)
</dt> <dt>

[<span data-ttu-id="b894a-154">Esempi avanzati di Winsock con estensioni Secure Socket</span><span class="sxs-lookup"><span data-stu-id="b894a-154">Advanced Winsock Samples Using Secure Socket Extensions</span></span>](advanced-winsock-samples-using-secure-socket-extensions.md)
</dt> <dt>

[<span data-ttu-id="b894a-155">Application Layer Enforcement (ALE)</span><span class="sxs-lookup"><span data-stu-id="b894a-155">Application Layer Enforcement (ALE)</span></span>](../fwp/application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="b894a-156">Configurazione IPsec</span><span class="sxs-lookup"><span data-stu-id="b894a-156">IPsec Configuration</span></span>](../fwp/ipsec-configuration.md)
</dt> <dt>

[<span data-ttu-id="b894a-157">Funzioni IPsec</span><span class="sxs-lookup"><span data-stu-id="b894a-157">IPsec Functions</span></span>](../fwp/fwp-ipsec-functions.md)
</dt> <dt>

[<span data-ttu-id="b894a-158">Programmazione Winsock sicura</span><span class="sxs-lookup"><span data-stu-id="b894a-158">Secure Winsock Programming</span></span>](secure-winsock-programming.md)
</dt> <dt>

[<span data-ttu-id="b894a-159">Security Support Provider Interface (SSPI)</span><span class="sxs-lookup"><span data-stu-id="b894a-159">Security Support Provider Interface (SSPI)</span></span>](../rpc/security-support-provider-interface-sspi-.md)
</dt> <dt>

[<span data-ttu-id="b894a-160">Uso delle estensioni Secure Socket</span><span class="sxs-lookup"><span data-stu-id="b894a-160">Using Secure Socket Extensions</span></span>](using-secure-socket-extensions.md)
</dt> <dt>

[<span data-ttu-id="b894a-161">Piattaforma filtro Windows</span><span class="sxs-lookup"><span data-stu-id="b894a-161">Windows Filtering Platform</span></span>](../fwp/windows-filtering-platform-start-page.md)
</dt> <dt>

[<span data-ttu-id="b894a-162">Funzioni API della piattaforma filtro Windows</span><span class="sxs-lookup"><span data-stu-id="b894a-162">Windows Filtering Platform API Functions</span></span>](../fwp/fwp-functions.md)
</dt> </dl>

 

 

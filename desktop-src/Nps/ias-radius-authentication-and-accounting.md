---
title: Autenticazione, autorizzazione e accounting RADIUS
description: NPS supporta completamente il protocollo Remote Authentication Dial-In User Service (RADIUS). Il protocollo RADIUS è lo standard de facto per l'autenticazione utente remota ed è documentato in RFC 2865 e RFC 2866.
ms.assetid: 3e00d555-355c-4a4c-a389-ab44e9ed9ca9
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cce45bbc6e4802ed5137849a5b22520c8a4badbb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399401"
---
# <a name="radius-authentication-authorization-and-accounting"></a><span data-ttu-id="1af32-104">Autenticazione, autorizzazione e accounting RADIUS</span><span class="sxs-lookup"><span data-stu-id="1af32-104">RADIUS Authentication, Authorization, and Accounting</span></span>

> [!Note]  
> <span data-ttu-id="1af32-105">Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="1af32-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="1af32-106">Il contenuto di questo argomento si applica sia a IAS che a NPS.</span><span class="sxs-lookup"><span data-stu-id="1af32-106">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="1af32-107">In tutto il testo, NPS viene utilizzato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.</span><span class="sxs-lookup"><span data-stu-id="1af32-107">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="1af32-108">NPS supporta completamente il protocollo Remote Authentication Dial-In User Service (RADIUS).</span><span class="sxs-lookup"><span data-stu-id="1af32-108">NPS fully supports the Remote Authentication Dial-In User Service (RADIUS) protocol.</span></span> <span data-ttu-id="1af32-109">Il protocollo RADIUS è lo standard de facto per l'autenticazione utente remota ed è documentato in [rfc 2865](https://www.ietf.org/rfc/rfc2865.txt) e [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span><span class="sxs-lookup"><span data-stu-id="1af32-109">The RADIUS protocol is the de facto standard for remote user authentication and it is documented in [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt) and [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span></span>

## <a name="radius-authentication-and-authorization"></a><span data-ttu-id="1af32-110">Autenticazione e autorizzazione RADIUS</span><span class="sxs-lookup"><span data-stu-id="1af32-110">RADIUS Authentication and Authorization</span></span>

<span data-ttu-id="1af32-111">Il diagramma seguente mostra un client di autenticazione ("utente") che si connette a un server di accesso alla rete (NAS) tramite una connessione remota, usando il Point-to-Point Protocol (PPP).</span><span class="sxs-lookup"><span data-stu-id="1af32-111">The following diagram shows an authenticating client ("User") connecting to a Network Access Server (NAS) over a dial-up connection, using the Point-to-Point Protocol (PPP).</span></span> <span data-ttu-id="1af32-112">Per autenticare l'utente, il NAS Contatta un server remoto che esegue NPS.</span><span class="sxs-lookup"><span data-stu-id="1af32-112">In order to authenticate the User, the NAS contacts a remote server running NPS.</span></span> <span data-ttu-id="1af32-113">Il NAS e il server NPS comunicano tramite il protocollo RADIUS.</span><span class="sxs-lookup"><span data-stu-id="1af32-113">The NAS and the NPS server communicate using the RADIUS protocol.</span></span>

![autenticazione utente remoto](images/ias01.png)

<span data-ttu-id="1af32-115">Un NAS funziona come un client di un server o di server che supportano il protocollo RADIUS.</span><span class="sxs-lookup"><span data-stu-id="1af32-115">A NAS operates as a client of a server or servers that support the RADIUS protocol.</span></span> <span data-ttu-id="1af32-116">I server che supportano il protocollo RADIUS vengono in genere definiti server RADIUS.</span><span class="sxs-lookup"><span data-stu-id="1af32-116">Servers that support the RADIUS protocol are generally referred to as the RADIUS servers.</span></span> <span data-ttu-id="1af32-117">Il client RADIUS, ovvero il NAS, passa le informazioni relative all'utente ai server RADIUS designati, quindi agisce sulla risposta restituita dai server.</span><span class="sxs-lookup"><span data-stu-id="1af32-117">The RADIUS client, that is, the NAS, passes information about the User to designated RADIUS servers, and then acts on the response that the servers return.</span></span> <span data-ttu-id="1af32-118">La richiesta inviata dal NAS al server RADIUS per autenticare l'utente è in genere denominata "richiesta di autenticazione".</span><span class="sxs-lookup"><span data-stu-id="1af32-118">The request sent by the NAS to the RADIUS server in order to authenticate the User is generally called an "authentication request."</span></span>

<span data-ttu-id="1af32-119">Se un server RADIUS autentica l'utente correttamente, il server RADIUS restituisce al NAS le informazioni di configurazione in modo da poter fornire al servizio di rete l'utente.</span><span class="sxs-lookup"><span data-stu-id="1af32-119">If a RADIUS server authenticates the User successfully, the RADIUS server returns configuration information to the NAS so that it can provide network service to the user.</span></span> <span data-ttu-id="1af32-120">Queste informazioni di configurazione sono costituite da "autorizzazioni" e contengono, tra le altre, il tipo di servizio che può fornire all'utente (ad esempio, PPP o Telnet).</span><span class="sxs-lookup"><span data-stu-id="1af32-120">This configuration information is composed of "authorizations" and contains, among others, the type of service NAS may provide to the User (for example, PPP, or telnet).</span></span>

<span data-ttu-id="1af32-121">Mentre il server RADIUS sta elaborando la richiesta di autenticazione, può eseguire funzioni di autorizzazione, ad esempio verificare il numero di telefono dell'utente e verificare se l'utente ha già una sessione in corso.</span><span class="sxs-lookup"><span data-stu-id="1af32-121">While the RADIUS server is processing the authentication request, it can perform authorization functions such as verifying the user's telephone number and checking whether the user already has a session in progress.</span></span> <span data-ttu-id="1af32-122">Il server RADIUS può determinare se l'utente dispone già di una sessione in corso contattando un server di stato.</span><span class="sxs-lookup"><span data-stu-id="1af32-122">The RADIUS server can determine whether the user already has a session in progress by contacting a state server.</span></span>

<span data-ttu-id="1af32-123">Per ulteriori informazioni sull'autenticazione e l'autorizzazione RADIUS, vedere [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt).</span><span class="sxs-lookup"><span data-stu-id="1af32-123">For more information on RADIUS authentication and authorization, see [RFC 2865](https://www.ietf.org/rfc/rfc2865.txt).</span></span>

## <a name="radius-accounting"></a><span data-ttu-id="1af32-124">Accounting RADIUS</span><span class="sxs-lookup"><span data-stu-id="1af32-124">RADIUS Accounting</span></span>

<span data-ttu-id="1af32-125">Il server RADIUS raccoglie anche un'ampia gamma di informazioni inviate dal NAS che possono essere usate per l'accounting e per la creazione di report sull'attività di rete.</span><span class="sxs-lookup"><span data-stu-id="1af32-125">The RADIUS server also collects a variety of information sent by the NAS that can be used for accounting and for reporting on network activity.</span></span> <span data-ttu-id="1af32-126">Il client RADIUS invia le informazioni ai server RADIUS designati quando l'utente si connette e si disconnette.</span><span class="sxs-lookup"><span data-stu-id="1af32-126">The RADIUS client sends information to designated RADIUS servers when the User logs on and logs off.</span></span> <span data-ttu-id="1af32-127">Il client RADIUS può inviare informazioni aggiuntive sull'utilizzo a intervalli regolari mentre è in corso la sessione.</span><span class="sxs-lookup"><span data-stu-id="1af32-127">The RADIUS client may send additional usage information on a periodic basis while the session is in progress.</span></span> <span data-ttu-id="1af32-128">Le richieste inviate dal client al server per registrare le informazioni di accesso/disconnessione e di utilizzo vengono in genere denominate "richieste di contabilità".</span><span class="sxs-lookup"><span data-stu-id="1af32-128">The requests sent by the client to the server to record logon/logoff and usage information are generally called "accounting requests."</span></span>

<span data-ttu-id="1af32-129">Per ulteriori informazioni sull'accounting RADIUS, vedere [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span><span class="sxs-lookup"><span data-stu-id="1af32-129">For more information on RADIUS accounting, see [RFC 2866](https://www.ietf.org/rfc/rfc2866.txt).</span></span>

## <a name="radius-proxy"></a><span data-ttu-id="1af32-130">Proxy RADIUS</span><span class="sxs-lookup"><span data-stu-id="1af32-130">RADIUS Proxy</span></span>

<span data-ttu-id="1af32-131">Un server RADIUS può fungere da client proxy per altri server RADIUS.</span><span class="sxs-lookup"><span data-stu-id="1af32-131">A RADIUS server can act as a proxy client to other RADIUS servers.</span></span> <span data-ttu-id="1af32-132">In questi casi, il server RADIUS contattato dal NAS passa la richiesta di autenticazione o di accounting a un altro server RADIUS che esegue effettivamente l'autenticazione o l'attività di contabilità.</span><span class="sxs-lookup"><span data-stu-id="1af32-132">In these cases, the RADIUS server contacted by the NAS passes the authentication or accounting request to another RADIUS server that actually performs the authentication or the accounting task.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1af32-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1af32-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1af32-134">Servizio di autenticazione Internet e server dei criteri di rete</span><span class="sxs-lookup"><span data-stu-id="1af32-134">Internet Authentication Service and Network Policy Server</span></span>](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[<span data-ttu-id="1af32-135">Pacchetti accounting RADIUS</span><span class="sxs-lookup"><span data-stu-id="1af32-135">RADIUS Accounting Packets</span></span>](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[<span data-ttu-id="1af32-136">Utilizzo di un server di stato</span><span class="sxs-lookup"><span data-stu-id="1af32-136">Working with a State Server</span></span>](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

 
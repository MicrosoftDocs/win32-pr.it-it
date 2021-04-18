---
title: Autenticazione reciproca tramite Kerberos
description: L'autenticazione reciproca è una funzionalità di sicurezza in cui un processo client deve dimostrare la propria identità a un servizio e il servizio deve dimostrare la propria identità al client, prima che il traffico dell'applicazione venga trasmesso attraverso la connessione client/servizio.
ms.assetid: 775dd350-5c70-4d97-aa2f-d21e9aecc778
ms.tgt_platform: multiple
keywords:
- Active Directory, uso dell'autenticazione reciproca
- Active Directory, utilizzo, sicurezza, autenticazione reciproca
- ANNUNCIO sulla sicurezza
- Active Directory di sicurezza, autenticazione reciproca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cf2e68c1983dde9221cc3fa89866b5358ee6eb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "106299566"
---
# <a name="mutual-authentication-using-kerberos"></a><span data-ttu-id="77b03-107">Autenticazione reciproca tramite Kerberos</span><span class="sxs-lookup"><span data-stu-id="77b03-107">Mutual Authentication Using Kerberos</span></span>

<span data-ttu-id="77b03-108">L'autenticazione reciproca è una funzionalità di sicurezza in cui un processo client deve dimostrare la propria identità a un servizio e il servizio deve dimostrare la propria identità al client, prima che il traffico dell'applicazione venga trasmesso attraverso la connessione client/servizio.</span><span class="sxs-lookup"><span data-stu-id="77b03-108">Mutual authentication is a security feature in which a client process must prove its identity to a service, and the service must prove its identity to the client, before any application traffic is transmitted over the client/service connection.</span></span>

<span data-ttu-id="77b03-109">Active Directory Domain Services e Windows forniscono supporto per i nomi dell'entità servizio (SPN), che costituiscono un componente chiave del meccanismo Kerberos mediante il quale un client autentica un servizio.</span><span class="sxs-lookup"><span data-stu-id="77b03-109">Active Directory Domain Services and Windows provide support for service principal names (SPN), which are a key component in the Kerberos mechanism by which a client authenticates a service.</span></span> <span data-ttu-id="77b03-110">Un SPN è un nome univoco che identifica un'istanza di un servizio ed è associato all'account di accesso con cui viene eseguita l'istanza del servizio.</span><span class="sxs-lookup"><span data-stu-id="77b03-110">An SPN is a unique name that identifies an instance of a service and is associated with the logon account under which the service instance runs.</span></span> <span data-ttu-id="77b03-111">I componenti di un nome SPN sono tali che un client può comporre un nome SPN per un servizio senza l'account di accesso del servizio.</span><span class="sxs-lookup"><span data-stu-id="77b03-111">The components of an SPN are such that a client can compose an SPN for a service without the service logon account.</span></span> <span data-ttu-id="77b03-112">Ciò consente al client di richiedere al servizio di autenticare l'account anche se il client non ha il nome dell'account.</span><span class="sxs-lookup"><span data-stu-id="77b03-112">This enables the client to request the service to authenticate its account even though the client does not have the account name.</span></span>

<span data-ttu-id="77b03-113">Questa sezione include una panoramica di:</span><span class="sxs-lookup"><span data-stu-id="77b03-113">This section includes an overview of:</span></span>

-   <span data-ttu-id="77b03-114">Autenticazione reciproca tramite Kerberos.</span><span class="sxs-lookup"><span data-stu-id="77b03-114">Mutual authentication using Kerberos.</span></span>
-   <span data-ttu-id="77b03-115">Composizione di un nome SPN univoco.</span><span class="sxs-lookup"><span data-stu-id="77b03-115">Composing a unique SPN.</span></span>
-   <span data-ttu-id="77b03-116">Come un programma di installazione del servizio registra i nomi SPN nell'oggetto account associato a un'istanza del servizio.</span><span class="sxs-lookup"><span data-stu-id="77b03-116">How a service installer registers SPNs on the account object associated with a service instance.</span></span>
-   <span data-ttu-id="77b03-117">Il modo in cui un'applicazione client utilizza l'oggetto punto di connessione del servizio (SCP) di un'istanza di servizio in Active Directory Domain Services per recuperare i dati da cui comporre un nome SPN per il servizio.</span><span class="sxs-lookup"><span data-stu-id="77b03-117">How a client application uses a service instance's service connection point (SCP) object in Active Directory Domain Services to retrieve data from which to compose an SPN for the service.</span></span>
-   <span data-ttu-id="77b03-118">In che modo un'applicazione client utilizza un SPN del servizio in combinazione con Security Support Provider Interface (SSPI) per autenticare il servizio.</span><span class="sxs-lookup"><span data-stu-id="77b03-118">How a client application uses a service SPN in conjunction with the Security Support Provider Interface (SSPI) to authenticate the service.</span></span>
-   <span data-ttu-id="77b03-119">Esempio di codice per un'applicazione client/servizio Windows Sockets che utilizza SCP e SSPI per eseguire l'autenticazione reciproca.</span><span class="sxs-lookup"><span data-stu-id="77b03-119">A code example for a Windows Sockets client/service application that uses an SCP and SSPI to perform mutual authentication.</span></span>
-   <span data-ttu-id="77b03-120">Un esempio di codice per un client/servizio RPC che esegue l'autenticazione reciproca usando il servizio nome RPC e l'autenticazione RPC.</span><span class="sxs-lookup"><span data-stu-id="77b03-120">A code example for an RPC client/service that performs mutual authentication using the RPC name service and RPC authentication.</span></span>
-   <span data-ttu-id="77b03-121">Il modo in cui un servizio di registrazione e risoluzione (RnR) di Windows Socket usa nomi SPN per eseguire l'autenticazione reciproca.</span><span class="sxs-lookup"><span data-stu-id="77b03-121">How a Windows Sockets Registration and Resolution (RnR) service uses SPNs to perform mutual authentication.</span></span>

<span data-ttu-id="77b03-122">Questa sezione illustra l'uso di Dominio di Active Directory servizio per l'autenticazione reciproca, in particolare lo scopo dei punti di connessione del servizio e i nomi dell'entità servizio nell'autenticazione reciproca.</span><span class="sxs-lookup"><span data-stu-id="77b03-122">This section discusses using Active Directory Domain Service for mutual authentication, in particular, the purpose of service connection points and service principal names in mutual authentication.</span></span> <span data-ttu-id="77b03-123">Non è una spiegazione completa di come utilizzare SSPI per l'autenticazione reciproca o il supporto per l'autenticazione e la sicurezza disponibili per le applicazioni RPC e Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="77b03-123">It is not a complete discussion of how to use SSPI for mutual authentication or the authentication and security support available for RPC and Windows Sockets applications.</span></span>

<span data-ttu-id="77b03-124">Per altre informazioni, vedere:</span><span class="sxs-lookup"><span data-stu-id="77b03-124">For more information, see:</span></span>

-   [<span data-ttu-id="77b03-125">Pubblicazione con i punti di connessione del servizio</span><span class="sxs-lookup"><span data-stu-id="77b03-125">Publishing with service connection points</span></span>](publishing-with-service-connection-points.md)
-   [<span data-ttu-id="77b03-126">SSPI</span><span class="sxs-lookup"><span data-stu-id="77b03-126">SSPI</span></span>](/windows/desktop/SecAuthN/sspi)
-   [<span data-ttu-id="77b03-127">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="77b03-127">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
-   [<span data-ttu-id="77b03-128">RPC</span><span class="sxs-lookup"><span data-stu-id="77b03-128">RPC</span></span>](/windows/desktop/Rpc/rpc-start-page)

 

 
---
title: Nomi dell'entità servizio
description: Un nome dell'entità servizio (SPN) è un identificatore univoco di un'istanza del servizio.
ms.assetid: 54b02853-4097-4e37-b7a2-6b5cfd168ece
ms.tgt_platform: multiple
keywords:
- Nomi dell'entità servizio
- Nome SPN vedere nomi dell'entità servizio
- Active Directory nome entità servizio
- Active Directory nome entità servizio, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa34b7d90803a324faced7d67b56c0b6a1f13af
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103872250"
---
# <a name="service-principal-names"></a><span data-ttu-id="9b073-107">Nomi dell'entità servizio</span><span class="sxs-lookup"><span data-stu-id="9b073-107">Service Principal Names</span></span>

<span data-ttu-id="9b073-108">Un nome dell'entità servizio (SPN) è un identificatore univoco di un'istanza del servizio.</span><span class="sxs-lookup"><span data-stu-id="9b073-108">A service principal name (SPN) is a unique identifier of a service instance.</span></span> <span data-ttu-id="9b073-109">Gli SPN vengono utilizzati dall' [autenticazione Kerberos](mutual-authentication-using-kerberos.md) per associare un'istanza del servizio a un account di accesso al servizio.</span><span class="sxs-lookup"><span data-stu-id="9b073-109">SPNs are used by [Kerberos authentication](mutual-authentication-using-kerberos.md) to associate a service instance with a service logon account.</span></span> <span data-ttu-id="9b073-110">Questo consente a un'applicazione client di richiedere che il servizio esegua l'autenticazione di un account anche se il client non ha il nome dell'account.</span><span class="sxs-lookup"><span data-stu-id="9b073-110">This allows a client application to request that the service authenticate an account even if the client does not have the account name.</span></span>

<span data-ttu-id="9b073-111">Se si installano più istanze di un servizio in computer distribuiti in una foresta, a ogni istanza deve essere associato un nome SPN distinto.</span><span class="sxs-lookup"><span data-stu-id="9b073-111">If you install multiple instances of a service on computers throughout a forest, each instance must have its own SPN.</span></span> <span data-ttu-id="9b073-112">Se i client possono usare più nomi per l'autenticazione, una determinata istanza di servizio può presentare più SPN.</span><span class="sxs-lookup"><span data-stu-id="9b073-112">A given service instance can have multiple SPNs if there are multiple names that clients might use for authentication.</span></span> <span data-ttu-id="9b073-113">Un SPN, ad esempio, include sempre il nome del computer host in cui è in esecuzione l'istanza del servizio, pertanto un'istanza del servizio potrebbe registrare un nome SPN per ogni nome o alias del relativo host.</span><span class="sxs-lookup"><span data-stu-id="9b073-113">For example, an SPN always includes the name of the host computer on which the service instance is running, so a service instance might register an SPN for each name or alias of its host.</span></span> <span data-ttu-id="9b073-114">Per ulteriori informazioni sul formato SPN e sulla composizione di un nome SPN univoco, vedere [formati dei nomi per nomi SPN univoci](name-formats-for-unique-spns.md).</span><span class="sxs-lookup"><span data-stu-id="9b073-114">For more information about SPN format and composing a unique SPN, see [Name Formats for Unique SPNs](name-formats-for-unique-spns.md).</span></span>

<span data-ttu-id="9b073-115">Prima che il servizio di autenticazione Kerberos possa utilizzare un nome SPN per autenticare un servizio, è necessario che il nome SPN sia registrato nell'oggetto account utilizzato dall'istanza del servizio per l'accesso.</span><span class="sxs-lookup"><span data-stu-id="9b073-115">Before the Kerberos authentication service can use an SPN to authenticate a service, the SPN must be registered on the account object that the service instance uses to log on.</span></span> <span data-ttu-id="9b073-116">Un determinato nome SPN può essere registrato in un solo account.</span><span class="sxs-lookup"><span data-stu-id="9b073-116">A given SPN can be registered on only one account.</span></span> <span data-ttu-id="9b073-117">Per i servizi Win32, un programma di installazione del servizio specifica l'account di accesso quando viene installata un'istanza del servizio.</span><span class="sxs-lookup"><span data-stu-id="9b073-117">For Win32 services, a service installer specifies the logon account when an instance of the service is installed.</span></span> <span data-ttu-id="9b073-118">Il programma di installazione compone quindi i nomi SPN e li scrive come proprietà dell'oggetto account in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="9b073-118">The installer then composes the SPNs and writes them as a property of the account object in Active Directory Domain Services.</span></span> <span data-ttu-id="9b073-119">Se l'account di accesso di un'istanza del servizio viene modificato, è necessario registrare nuovamente i nomi SPN con il nuovo account.</span><span class="sxs-lookup"><span data-stu-id="9b073-119">If the logon account of a service instance changes, the SPNs must be re-registered under the new account.</span></span> <span data-ttu-id="9b073-120">Per ulteriori informazioni, vedere [come un servizio registra i relativi nomi SPN](how-a-service-registers-its-spns.md).</span><span class="sxs-lookup"><span data-stu-id="9b073-120">For more information, see [How a Service Registers its SPNs](how-a-service-registers-its-spns.md).</span></span>

<span data-ttu-id="9b073-121">Per connettersi a un servizio, un client individua un'istanza del servizio, compone un nome SPN per l'istanza, esegue la connessione al servizio e presenta il nome SPN al servizio per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="9b073-121">When a client wants to connect to a service, it locates an instance of the service, composes an SPN for that instance, connects to the service, and presents the SPN for the service to authenticate.</span></span> <span data-ttu-id="9b073-122">Per ulteriori informazioni, vedere [modalità di composizione del nome SPN di un servizio](how-clients-compose-a-serviceampaposs-spn.md)da parte dei client.</span><span class="sxs-lookup"><span data-stu-id="9b073-122">For more information, see [How Clients Compose a Service's SPN](how-clients-compose-a-serviceampaposs-spn.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9b073-123">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="9b073-123">In this Section</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9b073-124">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="9b073-124">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="9b073-125">Formati dei nomi per nomi SPN univoci</span><span class="sxs-lookup"><span data-stu-id="9b073-125">Name Formats for Unique SPNs</span></span>](name-formats-for-unique-spns.md)
</dt> <dt>

[<span data-ttu-id="9b073-126">Come un servizio compone i relativi nomi SPN</span><span class="sxs-lookup"><span data-stu-id="9b073-126">How a Service Composes its SPNs</span></span>](how-a-service-composes-its-spns.md)
</dt> <dt>

[<span data-ttu-id="9b073-127">Modalità di registrazione dei nomi SPN da un servizio</span><span class="sxs-lookup"><span data-stu-id="9b073-127">How a Service Registers its SPNs</span></span>](how-a-service-registers-its-spns.md)
</dt> <dt>

[<span data-ttu-id="9b073-128">Composizione del nome SPN di un servizio da parte dei client</span><span class="sxs-lookup"><span data-stu-id="9b073-128">How Clients Compose a Service's SPN</span></span>](how-clients-compose-a-serviceampaposs-spn.md)
</dt> </dl>

## <a name="related-topics"></a><span data-ttu-id="9b073-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9b073-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b073-130">Che cos'è un nome SPN e perché prestare attenzione?</span><span class="sxs-lookup"><span data-stu-id="9b073-130">What is an SPN and why should you care?</span></span>](/archive/blogs/autz_auth_stuff/what-is-a-spn-and-why-should-you-care)
</dt> <dt>

[<span data-ttu-id="9b073-131">Autenticazione reciproca tramite Kerberos</span><span class="sxs-lookup"><span data-stu-id="9b073-131">Mutual Authentication Using Kerberos</span></span>](mutual-authentication-using-kerberos.md)
</dt> </dl>

 

 
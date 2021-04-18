---
description: In questo argomento vengono illustrati alcuni scenari di blocco di compilazione, in cui vengono illustrati i criteri descritti in decidere dove applicare la protezione.
ms.assetid: e9820e53-8891-4bff-a333-00ad2dbb03a4
title: Scenari di base per la protezione dei dati nelle applicazioni multilivello
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7929bcfeba96b43b7ec91513b42ffb7f46266613
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305021"
---
# <a name="basic-scenarios-for-securing-data-in-multi-tier-applications"></a><span data-ttu-id="765b5-103">Scenari di base per la protezione dei dati nelle applicazioni multilivello</span><span class="sxs-lookup"><span data-stu-id="765b5-103">Basic Scenarios for Securing Data in Multi-Tier Applications</span></span>

<span data-ttu-id="765b5-104">In questo argomento vengono illustrati alcuni scenari di blocco di compilazione, in cui vengono illustrati i criteri descritti in [decidere dove applicare la protezione](deciding-where-to-enforce-security.md).</span><span class="sxs-lookup"><span data-stu-id="765b5-104">This topic presents a few building-block scenarios, illustrating the criteria discussed in [Deciding Where to Enforce Security](deciding-where-to-enforce-security.md).</span></span>

## <a name="trusted-server-scenario"></a><span data-ttu-id="765b5-105">Scenario server attendibile</span><span class="sxs-lookup"><span data-stu-id="765b5-105">Trusted Server Scenario</span></span>

-   <span data-ttu-id="765b5-106">Il database considera completamente attendibile l'applicazione COM+ per autenticare e autorizzare gli utenti finali ad accedere ai dati nel database.</span><span class="sxs-lookup"><span data-stu-id="765b5-106">The database fully trusts the COM+ application to authenticate and authorize end users to access data in the database.</span></span>
-   <span data-ttu-id="765b5-107">Preferibilmente, il database è protetto da qualsiasi accesso, tranne che tramite l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="765b5-107">Preferably, the database is secured against any access except through the application.</span></span>
-   <span data-ttu-id="765b5-108">L'applicazione COM+ utilizza la protezione basata sui ruoli per autorizzare gli utenti.</span><span class="sxs-lookup"><span data-stu-id="765b5-108">The COM+ application uses role-based security to authorize users.</span></span>
-   <span data-ttu-id="765b5-109">Le connessioni vengono aperte sotto l'identità dell'applicazione COM+ e sono completamente pool.</span><span class="sxs-lookup"><span data-stu-id="765b5-109">Connections are opened under the COM+ application's identity and are fully poolable.</span></span>
-   <span data-ttu-id="765b5-110">Il controllo e la registrazione possono essere eseguiti dall'applicazione COM+ oppure è possibile passare queste informazioni nel database dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="765b5-110">Auditing and logging can be done by the COM+ application, or this information can be passed into the database by the application.</span></span>

<span data-ttu-id="765b5-111">Questo scenario è ottimale per i dati a cui è possibile accedere da categorie stimabili di utenti che possono essere incapsulati in ruoli.</span><span class="sxs-lookup"><span data-stu-id="765b5-111">This scenario works best for data that can be accessed by predictable categories of users that can be encapsulated in roles.</span></span> <span data-ttu-id="765b5-112">Ad esempio, solo "managers", "Tellers" e "Accountants" hanno l'autorizzazione per accedere agli account.</span><span class="sxs-lookup"><span data-stu-id="765b5-112">For example, only "Managers," "Tellers," and "Accountants" have permission to access accounts.</span></span> <span data-ttu-id="765b5-113">La logica di business di tutti gli elementi abilitati per l'esecuzione viene applicata al livello intermedio.</span><span class="sxs-lookup"><span data-stu-id="765b5-113">The business logic of what precisely each is enabled to do is enforced in the middle tier.</span></span>

## <a name="impersonation-scenario"></a><span data-ttu-id="765b5-114">Scenario di rappresentazione</span><span class="sxs-lookup"><span data-stu-id="765b5-114">Impersonation Scenario</span></span>

-   <span data-ttu-id="765b5-115">Il database esegue l'autenticazione e l'autorizzazione degli utenti finali per limitare l'accesso ai dati nel database.</span><span class="sxs-lookup"><span data-stu-id="765b5-115">The database does its own authentication and authorization of end users to help limit access to data in the database.</span></span>
-   <span data-ttu-id="765b5-116">L'applicazione COM+ rappresenta i client ogni volta che accedono al database.</span><span class="sxs-lookup"><span data-stu-id="765b5-116">The COM+ application impersonates clients whenever it is accessing the database.</span></span>
-   <span data-ttu-id="765b5-117">Le connessioni vengono effettuate per ogni singola chiamata e non possono essere riutilizzate.</span><span class="sxs-lookup"><span data-stu-id="765b5-117">Connections are made on a per-call basis and can't be reused.</span></span>

<span data-ttu-id="765b5-118">Questo scenario funziona in modo ottimale per i dati strettamente associati a classi di utenti di dimensioni molto ridotte.</span><span class="sxs-lookup"><span data-stu-id="765b5-118">This scenario works best for data that is closely bound to very small classes of users.</span></span> <span data-ttu-id="765b5-119">Ogni dipendente può ad esempio accedere solo al proprio file personale e ogni responsabile può accedere solo ai file personali dei report.</span><span class="sxs-lookup"><span data-stu-id="765b5-119">For example, each employee can access only his own personnel file, and each manager can access only the personnel files of her reports.</span></span>

## <a name="hybrid-scenario"></a><span data-ttu-id="765b5-120"> Scenario ibrido</span><span class="sxs-lookup"><span data-stu-id="765b5-120">Hybrid Scenario</span></span>

<span data-ttu-id="765b5-121">Combinazione dei due scenari precedenti, in cui la rappresentazione viene utilizzata solo quando è necessario.</span><span class="sxs-lookup"><span data-stu-id="765b5-121">A combination of the preceding two scenarios, where impersonation is used only when it is needed.</span></span>

<span data-ttu-id="765b5-122">Questo scenario è ottimale nelle situazioni in cui si hanno relazioni ibride tra dati utente.</span><span class="sxs-lookup"><span data-stu-id="765b5-122">This scenario works best in situations where you have hybrid user-data relationships.</span></span> <span data-ttu-id="765b5-123">Ad esempio, si hanno "Manager", "cassieri", "ragionieri" e migliaia di singoli client Web che possono accedere solo ai propri account.</span><span class="sxs-lookup"><span data-stu-id="765b5-123">For example, you have "Managers," "Tellers," "Accountants," and thousands of individual Web clients who can access just their own accounts.</span></span> <span data-ttu-id="765b5-124">È possibile separare i percorsi logici attraverso l'applicazione, potenzialmente con componenti distinti, per gestire la seconda classe di utenti, in particolare laddove i presupposti delle prestazioni per tali utenti sono diversi.</span><span class="sxs-lookup"><span data-stu-id="765b5-124">You can separate logic paths through the application, potentially with separate components, to handle the latter class of users, particularly where performance assumptions for those users are different.</span></span>

## <a name="trusted-scenario-using-microsoft-sql-server-roles"></a><span data-ttu-id="765b5-125">Scenario attendibile mediante ruoli di Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="765b5-125">Trusted Scenario Using Microsoft SQL Server Roles</span></span>

-   <span data-ttu-id="765b5-126">Microsoft SQL Server 7,0 e versioni successive possono autorizzare l'accesso a righe specifiche utilizzando i ruoli, ma considera attendibile l'applicazione COM+ per autenticare e autorizzare gli utenti e per eseguirne il mapping ai ruoli corretti nel database.</span><span class="sxs-lookup"><span data-stu-id="765b5-126">Microsoft SQL Server 7.0 and later can authorize access to specific rows using roles but trusts the COM+ application to authenticate and authorize users and to map them to the correct roles in the database.</span></span>
-   <span data-ttu-id="765b5-127">L'applicazione COM+ autorizza gli utenti a utilizzare la protezione basata sui ruoli e i ruoli dell'applicazione corrispondono perfettamente ai ruoli del database.</span><span class="sxs-lookup"><span data-stu-id="765b5-127">The COM+ application authorizes users using role-based security, and the application roles correspond well to database roles.</span></span>
-   <span data-ttu-id="765b5-128">È possibile aprire le connessioni specifiche di un particolare ruolo del database.</span><span class="sxs-lookup"><span data-stu-id="765b5-128">Connections can be opened that are specific to a particular database role.</span></span> <span data-ttu-id="765b5-129">Queste connessioni possono essere riutilizzate se vengono mantenute da oggetti in pool nelle applicazioni COM+.</span><span class="sxs-lookup"><span data-stu-id="765b5-129">These connections can be reused if they are held by pooled objects in the COM+ applications.</span></span> <span data-ttu-id="765b5-130">Per informazioni dettagliate su come eseguire questa operazione, vedere la pagina relativa al [pool di oggetti com+](com--object-pooling.md).</span><span class="sxs-lookup"><span data-stu-id="765b5-130">For details on how to do this, see [COM+ Object Pooling](com--object-pooling.md).</span></span>
-   <span data-ttu-id="765b5-131">Il controllo e la registrazione possono essere eseguiti dall'applicazione COM+ oppure tali informazioni possono essere passate al database dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="765b5-131">Auditing and logging can be done by the COM+ application, or this information can be passed in to the database by the application.</span></span>

<span data-ttu-id="765b5-132">Questo scenario funziona meglio per gli stessi tipi di utenti e dati del primo scenario server attendibile, perché l'applicazione COM+ è ancora in gran parte attendibile per gestire correttamente l'autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="765b5-132">This scenario works best for generally the same kinds of users and data as in the first trusted server scenario because the COM+ application is still being largely trusted to handle authorization correctly.</span></span> <span data-ttu-id="765b5-133">Tuttavia, contribuisce a proteggere il database da accessi non autorizzati, consentendo potenzialmente l'accesso da più origini all'esterno dell'applicazione COM+, senza incorrere in problemi di scalabilità e prestazioni presenti nello scenario di rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="765b5-133">However, it does help protect the database against unauthorized access while allowing access potentially from multiple sources outside the COM+ application, without incurring the scaling and performance penalties present with the impersonation scenario.</span></span>

## <a name="related-topics"></a><span data-ttu-id="765b5-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="765b5-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="765b5-135">Decidere dove applicare la protezione</span><span class="sxs-lookup"><span data-stu-id="765b5-135">Deciding Where to Enforce Security</span></span>](deciding-where-to-enforce-security.md)
</dt> <dt>

[<span data-ttu-id="765b5-136">Sicurezza delle applicazioni a più livelli</span><span class="sxs-lookup"><span data-stu-id="765b5-136">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> </dl>

 

 




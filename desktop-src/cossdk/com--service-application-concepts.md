---
description: Concetti relativi all'applicazione del servizio COM+
ms.assetid: d6b1cf4a-ca39-4d50-a33d-aa639937ef9e
title: Concetti relativi all'applicazione del servizio COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b24db7a031ed0520f30891d98688af67e853ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483068"
---
# <a name="com-service-application-concepts"></a><span data-ttu-id="2778b-103">Concetti relativi all'applicazione del servizio COM+</span><span class="sxs-lookup"><span data-stu-id="2778b-103">COM+ Service Application Concepts</span></span>

<span data-ttu-id="2778b-104">È possibile utilizzare lo strumento di amministrazione Servizi componenti per configurare un'applicazione server COM+ come applicazione di servizio.</span><span class="sxs-lookup"><span data-stu-id="2778b-104">You can use the Component Services administrative tool to configure a COM+ server application as a service application.</span></span> <span data-ttu-id="2778b-105">L'esecuzione di un'applicazione server COM+ come servizio offre i vantaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="2778b-105">Running a COM+ server application as a service offers the following advantages:</span></span>

-   <span data-ttu-id="2778b-106">Se è sempre necessario che l'applicazione sia in esecuzione, Servizi componenti può facoltativamente avviare automaticamente il server e riavviare il server in caso di timeout. Se, ad esempio, un computer che esegue componenti del listener dei componenti in coda viene riavviato, i listener di componenti in coda possono essere avviati automaticamente se sono configurati come servizio.</span><span class="sxs-lookup"><span data-stu-id="2778b-106">If your application always needs to be running, Component Services can optionally have the server started automatically and can also restart the server if it times out. For example, if a computer running Queued Components listener components is rebooted, the Queued Components listeners can be started automatically if they are configured as a service.</span></span>
-   <span data-ttu-id="2778b-107">Se l'applicazione deve eseguire operazioni con privilegi, l'applicazione può essere eseguita come account di sistema locale.</span><span class="sxs-lookup"><span data-stu-id="2778b-107">If your application needs to perform privileged operations, the application can run as the local system account.</span></span> <span data-ttu-id="2778b-108">Con questo livello di sicurezza è consentita l'esecuzione solo dei servizi NT.</span><span class="sxs-lookup"><span data-stu-id="2778b-108">Only NT services are allowed to run with this level of security.</span></span> <span data-ttu-id="2778b-109">L'applicazione sarà compatibile con la Servizio cluster di Windows che gestisce i servizi durante il failover del sistema.</span><span class="sxs-lookup"><span data-stu-id="2778b-109">The application will be compatible with the Windows Cluster service, which manages services during system failover.</span></span>
-   <span data-ttu-id="2778b-110">Se gli altri servizi devono essere contrassegnati come dipendenti, Servizi componenti fornisce tale opzione.</span><span class="sxs-lookup"><span data-stu-id="2778b-110">If other services need to be marked as dependent, Component Services provides that option.</span></span> <span data-ttu-id="2778b-111">Se, ad esempio, l'applicazione usa la funzionalità fornita da un altro servizio, il servizio contrassegnato come dipendente verrà avviato prima dell'avvio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2778b-111">For example, if your application makes use of functionality provided by another service, the service marked as dependent will be started before your application starts.</span></span>

## <a name="starting-an-application-automatically"></a><span data-ttu-id="2778b-112">Avvio automatico di un'applicazione</span><span class="sxs-lookup"><span data-stu-id="2778b-112">Starting an Application Automatically</span></span>

<span data-ttu-id="2778b-113">Quando l'applicazione server COM+ viene avviata automaticamente, funge da servizio, richiedendo allo sviluppatore la gestione del server tramite lo strumento di amministrazione servizi.</span><span class="sxs-lookup"><span data-stu-id="2778b-113">When the COM+ server application is started automatically, it acts like a service, requiring the developer to manage the server using the Services administrative tool.</span></span>

> [!Note]  
> <span data-ttu-id="2778b-114">Per accedere allo strumento di amministrazione servizi, è possibile avviare lo strumento di amministrazione Servizi componenti, quindi fare clic su **Servizi (locale)**.</span><span class="sxs-lookup"><span data-stu-id="2778b-114">The Services administrative tool can be accessed by launching the Component Services administrative tool and then clicking **Services (Local)**.</span></span>

 

## <a name="starting-an-application-manually"></a><span data-ttu-id="2778b-115">Avvio manuale di un'applicazione</span><span class="sxs-lookup"><span data-stu-id="2778b-115">Starting an Application Manually</span></span>

<span data-ttu-id="2778b-116">Quando l'applicazione server COM+ viene avviata manualmente, funge da host DLL con le impostazioni di sicurezza di un servizio.</span><span class="sxs-lookup"><span data-stu-id="2778b-116">When the COM+ server application is started manually, it acts like a DLL host with the security settings of a service.</span></span> <span data-ttu-id="2778b-117">Il servizio verrà avviato manualmente quando viene attivato e arrestato automaticamente quando si verifica il timeout.</span><span class="sxs-lookup"><span data-stu-id="2778b-117">The service will be started up manually when activated and shut down automatically when it times out.</span></span>

## <a name="service-configurations"></a><span data-ttu-id="2778b-118">Configurazioni del servizio</span><span class="sxs-lookup"><span data-stu-id="2778b-118">Service Configurations</span></span>

<span data-ttu-id="2778b-119">Indipendentemente dal tipo di avvio, l'applicazione può essere configurata in modo da essere eseguita come account di sistema locale o assegnata a un account utente.</span><span class="sxs-lookup"><span data-stu-id="2778b-119">Regardless of the startup type, the application can be configured to run as a local system account or assigned to a user account.</span></span> <span data-ttu-id="2778b-120">Il sistema locale e l'account utente possono essere configurati al momento della creazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="2778b-120">The local system and user account can be configured at the time of creating the service.</span></span> <span data-ttu-id="2778b-121">Per configurare le impostazioni di sicurezza, sarà necessario utilizzare lo strumento di amministrazione servizi.</span><span class="sxs-lookup"><span data-stu-id="2778b-121">To configure the security settings, the Services administrative tool will have to be used.</span></span> <span data-ttu-id="2778b-122">Le dipendenze possono essere impostate anche per il servizio.</span><span class="sxs-lookup"><span data-stu-id="2778b-122">Dependencies can also be set for the service.</span></span>

<span data-ttu-id="2778b-123">L'applicazione può anche essere avviata in un ordine particolare selezionando le dipendenze da un elenco di altri servizi di sistema.</span><span class="sxs-lookup"><span data-stu-id="2778b-123">The application can also be started in any particular order by selecting dependencies from a list of other system services.</span></span> <span data-ttu-id="2778b-124">I servizi di sistema, ad esempio, possono essere contrassegnati come dipendenti e non avvieranno l'applicazione fino a quando i servizi di sistema non saranno stati avviati nell'ordine specificato.</span><span class="sxs-lookup"><span data-stu-id="2778b-124">For example, the system services can be marked as dependent and will not start the application until the system services have been started in the specified order.</span></span> <span data-ttu-id="2778b-125">L'applicazione di servizio verrà inizializzata correttamente prima di essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2778b-125">This will properly initialize the service application before it is used.</span></span>

<span data-ttu-id="2778b-126">Per istruzioni dettagliate su come configurare un'applicazione COM+ per l'esecuzione come servizio, vedere [configurazione di un'applicazione server com+ come applicazione di servizio](configuring-a-com--server-application-as-a-service-application.md).</span><span class="sxs-lookup"><span data-stu-id="2778b-126">For a step-by-step instruction on how to configure a COM+ application to run as a service, see [Configuring a COM+ Server Application as a Service Application](configuring-a-com--server-application-as-a-service-application.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2778b-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2778b-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2778b-128">Attività delle applicazioni del servizio COM+</span><span class="sxs-lookup"><span data-stu-id="2778b-128">COM+ Service Application Tasks</span></span>](com--service-application-tasks.md)
</dt> </dl>

 

 




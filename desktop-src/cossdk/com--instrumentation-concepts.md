---
description: Il servizio di strumentazione COM+ consente di creare programmi di registrazione e gestione degli eventi COM+ personalizzati quando si desidera visualizzare diverse metriche delle prestazioni per i componenti COM+.
ms.assetid: 07f68734-a382-4fe5-86af-90805f61c68d
title: Concetti relativi alla strumentazione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d86b5dbb7bb3f6db14d82220d88c58dbc0a8255
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304736"
---
# <a name="com-instrumentation-concepts"></a><span data-ttu-id="75b53-103">Concetti relativi alla strumentazione COM+</span><span class="sxs-lookup"><span data-stu-id="75b53-103">COM+ Instrumentation Concepts</span></span>

<span data-ttu-id="75b53-104">Il servizio di strumentazione COM+ consente di creare programmi di registrazione e gestione degli eventi COM+ personalizzati quando si desidera visualizzare diverse metriche delle prestazioni per i componenti COM+.</span><span class="sxs-lookup"><span data-stu-id="75b53-104">The COM+ instrumentation service enables you to build your own COM+ event management and logging programs when you want to display various performance metrics for your COM+ components.</span></span> <span data-ttu-id="75b53-105">La strumentazione COM+ può essere utilizzata anche per configurare gli eventi definiti dall'utente e per convertire gli eventi COM+ nel formato Visual Studio Analyzer (VSA) quando si esegue l'aggiornamento di pacchetti MTS che ricevono eventi MTS.</span><span class="sxs-lookup"><span data-stu-id="75b53-105">COM+ instrumentation can also be used to configure user-defined events and to convert COM+ events to Visual Studio Analyzer (VSA) format when you are upgrading MTS packages that are receiving MTS events.</span></span>

> [!Note]  
> <span data-ttu-id="75b53-106">A partire da Windows Server 2003, solo gli amministratori dispongono di privilegi di accesso in lettura ai registri di traccia per gli eventi di sistema.</span><span class="sxs-lookup"><span data-stu-id="75b53-106">As of Windows Server 2003, only administrators have read access privileges to the trace logs for system events.</span></span>

 

<span data-ttu-id="75b53-107">Sottoscrivendo gli eventi pubblicati dal server di pubblicazione degli eventi di sistema, i client possono implementare le [interfacce di strumentazione com+](com--instrumentation-interfaces.md) per ricevere notifiche per un'ampia gamma di metriche delle prestazioni com+, ad esempio informazioni su oggetti COM+ specifici, applicazioni com+ e servizi com+.</span><span class="sxs-lookup"><span data-stu-id="75b53-107">By subscribing to the events published by the system events publisher, clients can implement the [COM+ instrumentation interfaces](com--instrumentation-interfaces.md) to receive notifications for a variety of COM+ performance metrics, such as information about specific COM+ objects, COM+ applications, and COM+ services.</span></span> <span data-ttu-id="75b53-108">Le metriche vengono pubblicate nel client usando il [servizio eventi com+](com--events.md), un sistema di eventi a regime di controllo libero (LCE) che archivia le informazioni sugli eventi da autori diversi in un archivio eventi nel catalogo com+.</span><span class="sxs-lookup"><span data-stu-id="75b53-108">The metrics are published to the client by using the [COM+ events service](com--events.md), a loosely coupled events (LCE) system that stores event information from different publishers in an event store in the COM+ catalog.</span></span>

> [!Note]  
> <span data-ttu-id="75b53-109">La strumentazione COM+ non garantisce il recapito di un evento.</span><span class="sxs-lookup"><span data-stu-id="75b53-109">COM+ instrumentation does not guarantee the delivery of an event.</span></span>

 

<span data-ttu-id="75b53-110">Ogni metrica ha un timestamp che indica l'ora in cui è stata generata la metrica, non l'ora in cui è stato inviato o ricevuto.</span><span class="sxs-lookup"><span data-stu-id="75b53-110">Every metric has a timestamp that indicates the time when the metric was generated, not the time that it was dispatched or received.</span></span> <span data-ttu-id="75b53-111">Il client può correlare il timestamp e individuare il costo di esecuzione di un'applicazione COM+, il costo di una transazione eseguita all'interno di un'applicazione COM+ o il costo di una chiamata al metodo all'interno di un'applicazione COM+.</span><span class="sxs-lookup"><span data-stu-id="75b53-111">The client can correlate the timestamp and find out the cost of running a COM+ application, the cost of a transaction executed inside a COM+ application, or the cost of a method call inside of a COM+ application.</span></span>

<span data-ttu-id="75b53-112">È inoltre possibile utilizzare il servizio di strumentazione COM+ per filtrare le specifiche informazioni sulle metriche delle prestazioni che si desidera visualizzare.</span><span class="sxs-lookup"><span data-stu-id="75b53-112">You can also use the COM+ Instrumentation service to filter for the specific performance metrics information that you want to see.</span></span> <span data-ttu-id="75b53-113">Ad esempio, quando si sottoscrive un'interfaccia o un metodo di strumentazione COM+, è possibile specificare le proprietà per la sottoscrizione nella struttura [**COMSVCSEVENTINFO**](/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo) , ad esempio l'ID applicazione (membro **guidApp** ) o l'ID processo (membro **dwPid** ).</span><span class="sxs-lookup"><span data-stu-id="75b53-113">For example, when you subscribe to a COM+ instrumentation interface or method, you can specify properties for the subscription in the [**COMSVCSEVENTINFO**](/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo) structure, such as the application ID (**guidApp** member) or the process ID (**dwPid** member).</span></span>

<span data-ttu-id="75b53-114">Quando si specifica l'ID applicazione, si ricevono solo le metriche dell'applicazione specificata.</span><span class="sxs-lookup"><span data-stu-id="75b53-114">When the application ID is specified, you receive only the metrics from the specified application.</span></span> <span data-ttu-id="75b53-115">Quando viene specificato l'ID processo, vengono ricevute le metriche dell'applicazione server e delle applicazioni di libreria specificate caricate in tale processo.</span><span class="sxs-lookup"><span data-stu-id="75b53-115">When the process ID is specified, you receive metrics from the specified server application and library applications that are loaded in that process.</span></span> <span data-ttu-id="75b53-116">L'utente può specificare l'ID dell'applicazione e l'ID del processo, ma l'ID applicazione deve essere quello dell'applicazione server in esecuzione nel processo con l'ID di processo specificato.</span><span class="sxs-lookup"><span data-stu-id="75b53-116">The user can specify both the application ID and the process ID, but the application ID has to be that of the server application running in the process with the specified process ID.</span></span> <span data-ttu-id="75b53-117">Se non si specifica nessuno, l'utente riceve le metriche da tutte le applicazioni server e di libreria.</span><span class="sxs-lookup"><span data-stu-id="75b53-117">If neither is specified, the user receives metrics from all the server and library applications.</span></span>

<span data-ttu-id="75b53-118">Le metriche di strumentazione COM+ forniscono informazioni sufficienti per consentire all'applicazione di monitoraggio di metterle in correlazione con le metriche del sistema operativo per l'analisi delle prestazioni, la pianificazione della capacità e la modellazione e la stima.</span><span class="sxs-lookup"><span data-stu-id="75b53-118">The COM+ instrumentation metrics provide enough information for the monitoring application to correlate them with the operating system metrics for performance analysis, capacity planning, and for modeling and prediction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75b53-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="75b53-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75b53-120">Interfacce di strumentazione COM+</span><span class="sxs-lookup"><span data-stu-id="75b53-120">COM+ Instrumentation Interfaces</span></span>](com--instrumentation-interfaces.md)
</dt> </dl>

 

 




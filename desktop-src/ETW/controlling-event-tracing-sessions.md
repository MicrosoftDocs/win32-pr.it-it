---
description: Le sessioni di traccia eventi registrano gli eventi da uno o più provider.
ms.assetid: 43841d2f-5a4c-493d-9531-21941311ffbc
title: Controllo delle sessioni di traccia eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03f1917354679e7a68f9dbd001fc3aa10f09db0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977719"
---
# <a name="controlling-event-tracing-sessions"></a><span data-ttu-id="77097-103">Controllo delle sessioni di traccia eventi</span><span class="sxs-lookup"><span data-stu-id="77097-103">Controlling Event Tracing Sessions</span></span>

<span data-ttu-id="77097-104">Le sessioni di traccia eventi registrano gli eventi da uno o più [provider](providing-events.md).</span><span class="sxs-lookup"><span data-stu-id="77097-104">Event tracing sessions record events from one or more [providers](providing-events.md).</span></span> <span data-ttu-id="77097-105">Il controller definisce la sessione e Abilita i provider.</span><span class="sxs-lookup"><span data-stu-id="77097-105">The controller defines the session and enables the providers.</span></span> <span data-ttu-id="77097-106">La definizione della sessione include in genere la specifica del nome del file di log e della sessione, il tipo di file di log da usare e la risoluzione del timestamp usato per registrare gli eventi.</span><span class="sxs-lookup"><span data-stu-id="77097-106">Defining the session typically includes specifying the session and log file name, type of log file to use, and the resolution of the time stamp used to record the events.</span></span> <span data-ttu-id="77097-107">I controller possono inoltre aggiornare ed eseguire query sulle sessioni di traccia eventi.</span><span class="sxs-lookup"><span data-stu-id="77097-107">Controllers can also update and query event tracing sessions.</span></span>

<span data-ttu-id="77097-108">Negli argomenti seguenti viene illustrato come definire e aggiornare una sessione e abilitare i provider di traccia eventi:</span><span class="sxs-lookup"><span data-stu-id="77097-108">The following topics demonstrate how to define and update a session, and enable event trace providers:</span></span>

-   [<span data-ttu-id="77097-109">Configurazione e avvio di una sessione di traccia eventi</span><span class="sxs-lookup"><span data-stu-id="77097-109">Configuring and Starting an Event Tracing Session</span></span>](configuring-and-starting-an-event-tracing-session.md)
-   [<span data-ttu-id="77097-110">Configurazione e avvio di una sessione SystemTraceProvider</span><span class="sxs-lookup"><span data-stu-id="77097-110">Configuring and Starting a SystemTraceProvider Session</span></span>](configuring-and-starting-a-systemtraceprovider-session.md)
-   [<span data-ttu-id="77097-111">Configurazione e avvio di una sessione di autologger</span><span class="sxs-lookup"><span data-stu-id="77097-111">Configuring and Starting an AutoLogger Session</span></span>](configuring-and-starting-an-autologger-session.md)
-   [<span data-ttu-id="77097-112">Configurazione e avvio di una sessione di logger privata</span><span class="sxs-lookup"><span data-stu-id="77097-112">Configuring and Starting a Private Logger Session</span></span>](configuring-and-starting-a-private-logger-session.md)
-   [<span data-ttu-id="77097-113">Aggiornamento di una sessione di traccia eventi</span><span class="sxs-lookup"><span data-stu-id="77097-113">Updating an Event Tracing Session</span></span>](updating-an-event-tracing-session.md)
-   [<span data-ttu-id="77097-114">Recupero di dati di traccia eventi aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="77097-114">Retrieving Additional Event Tracing Data</span></span>](retrieving-additional-event-tracing-data.md)

<span data-ttu-id="77097-115">Per informazioni sullo scaricamento e l'esecuzione di query sulle sessioni, vedere rispettivamente [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) e [**QueryAllTraces**](/windows/win32/api/evntrace/nf-evntrace-queryalltracesa).</span><span class="sxs-lookup"><span data-stu-id="77097-115">For information on flushing and querying sessions, see [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) and [**QueryAllTraces**](/windows/win32/api/evntrace/nf-evntrace-queryalltracesa), respectively.</span></span>

<span data-ttu-id="77097-116">Solo gli utenti che eseguono con privilegi amministrativi elevati, gli utenti nel gruppo Performance Log Users e le applicazioni in esecuzione come LocalSystem, LocalService o NetworkService possono controllare le sessioni di traccia eventi.</span><span class="sxs-lookup"><span data-stu-id="77097-116">Only users running with elevated administrative privileges, users in the Performance Log Users group, and applications running as LocalSystem, LocalService or NetworkService can control event tracing sessions.</span></span> <span data-ttu-id="77097-117">Per concedere a un utente con restrizioni la possibilità di controllare le sessioni di traccia, aggiungerle al gruppo Performance Log Users.</span><span class="sxs-lookup"><span data-stu-id="77097-117">To grant a restricted user the ability to control trace sessions, add them to the Performance Log Users group.</span></span>

<span data-ttu-id="77097-118">**Windows XP e windows 2000:** Chiunque può controllare una sessione di traccia.</span><span class="sxs-lookup"><span data-stu-id="77097-118">**Windows XP and Windows 2000:** Anyone can control a trace session.</span></span>

 

 

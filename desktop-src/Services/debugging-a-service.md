---
description: Per eseguire il debug del servizio, è possibile utilizzare uno dei metodi seguenti.
ms.assetid: 6f4ae117-2120-4c1e-b69f-641ce2e633fa
title: Debug di un servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ebd99acfc6ad0e436b7f726c96af9e5d1c58442
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750799"
---
# <a name="debugging-a-service"></a><span data-ttu-id="fa54a-103">Debug di un servizio</span><span class="sxs-lookup"><span data-stu-id="fa54a-103">Debugging a Service</span></span>

<span data-ttu-id="fa54a-104">Per eseguire il debug del servizio, è possibile utilizzare uno dei metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="fa54a-104">You can use any one of the following methods to debug your service.</span></span>

-   <span data-ttu-id="fa54a-105">Usare il debugger per eseguire il debug del servizio mentre è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="fa54a-105">Use your debugger to debug the service while it is running.</span></span> <span data-ttu-id="fa54a-106">Ottenere innanzitutto l'identificatore di processo (PID) del processo del servizio.</span><span class="sxs-lookup"><span data-stu-id="fa54a-106">First, obtain the process identifier (PID) of the service process.</span></span> <span data-ttu-id="fa54a-107">Una volta ottenuto il PID, connettersi al processo in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="fa54a-107">After you have obtained the PID, attach to the running process.</span></span> <span data-ttu-id="fa54a-108">Per informazioni sulla sintassi, vedere la documentazione inclusa nel debugger.</span><span class="sxs-lookup"><span data-stu-id="fa54a-108">For syntax information, see the documentation included with your debugger.</span></span>
-   <span data-ttu-id="fa54a-109">Chiamare la funzione [**DebugBreak**](/windows/desktop/api/debugapi/nf-debugapi-debugbreak) per richiamare il debugger per il debug JIT.</span><span class="sxs-lookup"><span data-stu-id="fa54a-109">Call the [**DebugBreak**](/windows/desktop/api/debugapi/nf-debugapi-debugbreak) function to invoke the debugger for just-in-time debugging.</span></span>
-   <span data-ttu-id="fa54a-110">Specificare un debugger da usare all'avvio di un programma.</span><span class="sxs-lookup"><span data-stu-id="fa54a-110">Specify a debugger to use when starting a program.</span></span> <span data-ttu-id="fa54a-111">A tale scopo, creare una chiave denominata **Image File Execution Options** nel seguente percorso del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="fa54a-111">To do so, create a key called **Image File Execution Options** in the following registry location:</span></span>

    <span data-ttu-id="fa54a-112">**HKEY \_ \_ computer locale \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion**</span><span class="sxs-lookup"><span data-stu-id="fa54a-112">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion**</span></span>

    <span data-ttu-id="fa54a-113">Creare una sottochiave con lo stesso nome del servizio, ad esempio MYSERV.EXE.</span><span class="sxs-lookup"><span data-stu-id="fa54a-113">Create a subkey with the same name as your service (for example, MYSERV.EXE).</span></span> <span data-ttu-id="fa54a-114">Per questa sottochiave aggiungere un valore di tipo **reg \_ SZ**, denominato **debugger**.</span><span class="sxs-lookup"><span data-stu-id="fa54a-114">To this subkey, add a value of type **REG\_SZ**, named **Debugger**.</span></span> <span data-ttu-id="fa54a-115">Utilizzare il percorso completo del debugger come valore stringa.</span><span class="sxs-lookup"><span data-stu-id="fa54a-115">Use the full path to the debugger as the string value.</span></span> <span data-ttu-id="fa54a-116">Nell'applet del pannello di controllo dei servizi selezionare il servizio, fare clic su **avvio** e selezionare **Consenti al servizio di interagire con il desktop**.</span><span class="sxs-lookup"><span data-stu-id="fa54a-116">In the Services control panel applet, select your service, click **Startup** and check **Allow Service to Interact with Desktop**.</span></span> <span data-ttu-id="fa54a-117">Il servizio deve essere un servizio interattivo. in caso contrario, il debugger non può essere eseguito sul desktop predefinito.</span><span class="sxs-lookup"><span data-stu-id="fa54a-117">The service must be an interactive service, or else the debugger cannot run on the default desktop.</span></span> <span data-ttu-id="fa54a-118">Si noti che questa tecnica non è più supportata a partire da Windows Vista perché tutti i servizi vengono eseguiti nella sessione riservata esclusivamente ai servizi e non supporta la visualizzazione di un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="fa54a-118">Note that this technique is no longer supported as of Windows Vista because all services are run in session that is reserved exclusively for services and does not support displaying a user interface.</span></span>

-   <span data-ttu-id="fa54a-119">Usare la [traccia eventi](/windows/desktop/ETW/event-tracing-portal) per registrare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="fa54a-119">Use [Event Tracing](/windows/desktop/ETW/event-tracing-portal) to log information.</span></span>

<span data-ttu-id="fa54a-120">Per eseguire il debug del codice di inizializzazione di un servizio di avvio automatico, sarà necessario installare ed eseguire temporaneamente il servizio come servizio di avvio a richiesta.</span><span class="sxs-lookup"><span data-stu-id="fa54a-120">To debug the initialization code of an auto-start service, you will have to temporarily install and run the service as a demand-start service.</span></span>

<span data-ttu-id="fa54a-121">In alcuni casi potrebbe essere necessario eseguire un servizio come applicazione console a scopo di debug.</span><span class="sxs-lookup"><span data-stu-id="fa54a-121">At times, it may be necessary to run a service as a console application for debugging purposes.</span></span> <span data-ttu-id="fa54a-122">In questo scenario, la funzione [**Impossibile eseguire StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) restituirà un **errore di \_ \_ \_ \_ connessione del controller di servizio non riuscito**.</span><span class="sxs-lookup"><span data-stu-id="fa54a-122">In this scenario, the [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) function will return **ERROR\_FAILED\_SERVICE\_CONTROLLER\_CONNECT**.</span></span> <span data-ttu-id="fa54a-123">Pertanto, assicurarsi di strutturare il codice in modo tale che il codice specifico del servizio non venga chiamato quando viene restituito l'errore.</span><span class="sxs-lookup"><span data-stu-id="fa54a-123">Therefore, be sure to structure your code such that service-specific code is not called when this error is returned.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa54a-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fa54a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa54a-125">Debug di un'applicazione di servizio</span><span class="sxs-lookup"><span data-stu-id="fa54a-125">Debugging a Service Application</span></span>](https://msdn.microsoft.com/library/cc267835.aspx)
</dt> <dt>

[<span data-ttu-id="fa54a-126">Strumenti di debug per Windows</span><span class="sxs-lookup"><span data-stu-id="fa54a-126">Debugging Tools for Windows</span></span>](https://msdn.microsoft.com/library/cc267445.aspx)
</dt> </dl>

 

 

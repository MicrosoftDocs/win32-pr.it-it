---
description: Un'applicazione in esecuzione come utente standard comunica con un servizio eseguito come sistema utilizzando RPC (Remote Procedure Call).
ms.assetid: c0bcebe3-f7eb-471f-a21d-5840d2e26729
title: Modello di servizio del sistema operativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ce545c60da8e480247c8fc8b02cfc01e4487340
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967891"
---
# <a name="operating-system-service-model"></a><span data-ttu-id="ba749-103">Modello di servizio del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="ba749-103">Operating System Service Model</span></span>

<span data-ttu-id="ba749-104">Nel modello del servizio del sistema operativo, un'applicazione in esecuzione come utente standard comunica con un servizio eseguito come **sistema** utilizzando RPC ( [Remote Procedure Call](/windows/desktop/Rpc/rpc-start-page) ).</span><span class="sxs-lookup"><span data-stu-id="ba749-104">In the operating system service model, an application running as a standard user communicates with a service running as **SYSTEM** by using [Remote Procedure Call](/windows/desktop/Rpc/rpc-start-page) (RPC).</span></span>

<span data-ttu-id="ba749-105">L'applicazione utente standard è contrassegnata nel manifesto dell'applicazione con un **requestedExecutionLevel** di **asInvoker**.</span><span class="sxs-lookup"><span data-stu-id="ba749-105">The standard user application is marked in the application manifest with a **requestedExecutionLevel** of **asInvoker**.</span></span> <span data-ttu-id="ba749-106">Per eseguire un'operazione che richiede privilegi di amministratore, l'applicazione utente standard effettua una richiesta al servizio.</span><span class="sxs-lookup"><span data-stu-id="ba749-106">To perform an operation that requires administrator privilege, the standard user application makes a request to the service.</span></span>

<span data-ttu-id="ba749-107">Un utilizzo del modello di servizio del sistema operativo è quello di gestire le applicazioni che potrebbero avere un effetto sul sistema, ad esempio antivirus o altro software indesiderato e spyware.</span><span class="sxs-lookup"><span data-stu-id="ba749-107">One use for the operating system service model is to manage applications that could impact the system, such as antivirus or other unwanted software and spyware.</span></span> <span data-ttu-id="ba749-108">L'applicazione utente standard consente all'utente connesso di controllare alcuni aspetti del servizio.</span><span class="sxs-lookup"><span data-stu-id="ba749-108">The standard user application allows the logged on user to control some aspects of the service.</span></span> <span data-ttu-id="ba749-109">Il servizio è responsabile di determinare le operazioni eseguite per un'applicazione utente standard.</span><span class="sxs-lookup"><span data-stu-id="ba749-109">The service is responsible for determining which operations it performs for a standard user application.</span></span> <span data-ttu-id="ba749-110">Ad esempio, un servizio antivirus potrebbe consentire a un utente standard di avviare un'analisi del sistema, ma potrebbe non consentire a un utente standard di disabilitare il controllo dei virus in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="ba749-110">For example, an antivirus service might allow a standard user to start a scan of the system, but it might not allow a standard user to disable real-time virus checking.</span></span>

<span data-ttu-id="ba749-111">Un vantaggio principale dell'utilizzo del modello di servizio del sistema operativo è che non è richiesta alcuna richiesta di elevazione dei privilegi.</span><span class="sxs-lookup"><span data-stu-id="ba749-111">A major benefit of using the operating system service model is that no elevation prompting is required.</span></span>

<span data-ttu-id="ba749-112">Uno svantaggio dell'uso del modello del servizio del sistema operativo è che un servizio in esecuzione nel sistema usa più risorse di un'attività e un servizio non può essere arrestato da un utente standard.</span><span class="sxs-lookup"><span data-stu-id="ba749-112">One drawback of using the operating system service model is that a service running on the system uses more resources than a task, and a service cannot be stopped by a standard user.</span></span> <span data-ttu-id="ba749-113">Se è sufficiente, provare a usare il [modello di attività con privilegi elevati](elevated-task-model.md) .</span><span class="sxs-lookup"><span data-stu-id="ba749-113">Consider using the [Elevated Task Model](elevated-task-model.md) if it suffices.</span></span>

<span data-ttu-id="ba749-114">Per implementare il modello di servizio del sistema operativo, creare un'applicazione client utente standard e un servizio del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ba749-114">To implement the operating system service model, create a standard user client application and an operating system service.</span></span> <span data-ttu-id="ba749-115">Installare il servizio nel sistema operativo durante l'installazione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="ba749-115">Install the service in the operating system during product installation time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba749-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ba749-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba749-117">Sviluppo di applicazioni che richiedono privilegi di amministratore</span><span class="sxs-lookup"><span data-stu-id="ba749-117">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[<span data-ttu-id="ba749-118">Modello di broker amministratore</span><span class="sxs-lookup"><span data-stu-id="ba749-118">Administrator Broker Model</span></span>](administrator-broker-model.md)
</dt> <dt>

[<span data-ttu-id="ba749-119">Modello a oggetti COM dell'amministratore</span><span class="sxs-lookup"><span data-stu-id="ba749-119">Administrator COM Object Model</span></span>](administrator-com-object-model.md)
</dt> <dt>

[<span data-ttu-id="ba749-120">Modello di attività con privilegi elevati</span><span class="sxs-lookup"><span data-stu-id="ba749-120">Elevated Task Model</span></span>](elevated-task-model.md)
</dt> </dl>

 

 

---
description: Il \_ mutex MSIExecute viene impostato solo durante l'elaborazione della tabella InstallExecuteSequence, della tabella AdminExecuteSequence o della tabella AdvtExecuteSequence.
ms.assetid: 2186422d-ccb2-4f7e-8c6d-326c00e0d9a9
title: Mutex _MSIExecute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c22a9ca79e83e8593c2ee99884965acfd414ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881198"
---
# <a name="_msiexecute-mutex"></a><span data-ttu-id="40a55-103">\_Mutex MSIExecute</span><span class="sxs-lookup"><span data-stu-id="40a55-103">\_MSIExecute Mutex</span></span>

<span data-ttu-id="40a55-104">Il \_ mutex MSIExecute viene impostato solo durante l'elaborazione della tabella [InstallExecuteSequence](installexecutesequence-table.md), della [tabella AdminExecuteSequence](adminexecutesequence-table.md)o della [tabella AdvtExecuteSequence](advtexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="40a55-104">The \_MSIExecute Mutex is set only while processing the [InstallExecuteSequence table](installexecutesequence-table.md), [AdminExecuteSequence table](adminexecutesequence-table.md), or [AdvtExecuteSequence table](advtexecutesequence-table.md).</span></span>

<span data-ttu-id="40a55-105">Poiché non è possibile eseguire due installazioni nello stesso processo, un tentativo di chiamare il Application Programming Interface (API) del programma di installazione restituisce l'errore di \_ installazione \_ già in \_ esecuzione (1618) in due casi:</span><span class="sxs-lookup"><span data-stu-id="40a55-105">Because two installations cannot be run in the same process, an attempt to call the installer's application programming interface (API) returns ERROR\_INSTALL\_ALREADY\_RUNNING (1618) in two cases:</span></span>

-   <span data-ttu-id="40a55-106">Mentre \_ è impostato il mutex MSIExecute.</span><span class="sxs-lookup"><span data-stu-id="40a55-106">While the \_MSIExecute Mutex is set.</span></span>
-   <span data-ttu-id="40a55-107">Mentre il processo corrente sta elaborando la tabella [InstallUISequence](installuisequence-table.md) o la [tabella AdminUISequence](adminuisequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="40a55-107">While the current process is processing the [InstallUISequence table](installuisequence-table.md) or [AdminUISequence table](adminuisequence-table.md).</span></span>

<span data-ttu-id="40a55-108">Per informazioni sull'applicazione installata, vedere i messaggi di [registrazione eventi](event-logging.md) .</span><span class="sxs-lookup"><span data-stu-id="40a55-108">See the [Event Logging](event-logging.md) messages for information about what application is being installed.</span></span>

<span data-ttu-id="40a55-109">Nei casi in cui è impraticabile restituire un errore di \_ installazione \_ già \_ in esecuzione, è possibile recuperare lo stato corrente del servizio Windows Installer prima di tentare di avviare l'installazione tramite la funzione [**QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) .</span><span class="sxs-lookup"><span data-stu-id="40a55-109">In cases where it is impractical to return an ERROR\_INSTALL\_ALREADY\_RUNNING error, you can retrieve the current status of the Windows Installer service before attempting to start the installation by using the [**QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) function.</span></span> <span data-ttu-id="40a55-110">Il servizio Windows Installer è attualmente in esecuzione se il valore del membro **dwControlsAccepted** della struttura del [**\_ \_ processo di stato del servizio**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) restituito è **servizio \_ accettazione \_ arresto**.</span><span class="sxs-lookup"><span data-stu-id="40a55-110">The Windows Installer service is currently running if the value of the **dwControlsAccepted** member of the returned [**SERVICE\_STATUS\_PROCESS**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) structure is **SERVICE\_ACCEPT\_SHUTDOWN**.</span></span>

<span data-ttu-id="40a55-111">**Windows Installer 2,0:** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="40a55-111">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="40a55-112">L'uso della funzione [**QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) per recuperare lo stato corrente del servizio Windows Installer richiede Windows Installer versione 3,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="40a55-112">The use of the [**QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) function to retrieve the current status of the Windows Installer service requires Windows Installer version 3.0 or greater.</span></span>

 

 

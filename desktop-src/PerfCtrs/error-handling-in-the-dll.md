---
description: Utilizzare la registrazione eventi per registrare gli errori che si verificano nella DLL delle prestazioni.
ms.assetid: 61bc4fa1-8185-4e07-a3b5-4bd357f0f75a
title: Gestione degli errori nella DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd21f0b9338600012d65aa19801ee57794fac294
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967516"
---
# <a name="error-handling-in-the-dll"></a><span data-ttu-id="91bec-103">Gestione degli errori nella DLL</span><span class="sxs-lookup"><span data-stu-id="91bec-103">Error Handling in the DLL</span></span>

<span data-ttu-id="91bec-104">Utilizzare la registrazione eventi per registrare gli errori che si verificano nella DLL delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="91bec-104">Use event logging to record errors that occur in the performance DLL.</span></span> <span data-ttu-id="91bec-105">La registrazione degli eventi di errore contribuisce alla risoluzione dei problemi relativi alle applicazioni che forniscono dati sulle prestazioni durante lo sviluppo e dopo l'installazione.</span><span class="sxs-lookup"><span data-stu-id="91bec-105">Logging error events aids in troubleshooting applications that provide performance data during development and after installation.</span></span> <span data-ttu-id="91bec-106">È necessario limitare la quantità di registrazione degli errori che si verifica nella funzione [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) perché la raccolta dei dati può essere frequente.</span><span class="sxs-lookup"><span data-stu-id="91bec-106">You should limit the amount of error logging that occurs in the [**CollectPerformanceData**](/windows/win32/api/winperf/nc-winperf-pm_collect_proc) function because data collection can be frequent.</span></span>

<span data-ttu-id="91bec-107">Se si verificano problemi con la funzione [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) , il sistema registra gli errori seguenti nel registro eventi.</span><span class="sxs-lookup"><span data-stu-id="91bec-107">The system logs the following errors to the event log if there are problems with the [**OpenPerformanceData**](/previous-versions/windows/desktop/legacy/aa372200(v=vs.85)) function.</span></span> <span data-ttu-id="91bec-108">Se si verifica uno degli errori seguenti, il sistema non chiama di nuovo la DLL delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="91bec-108">If one of the following errors occurs, the system does not call the performance DLL again.</span></span> <span data-ttu-id="91bec-109">La DLL viene invece scaricata.</span><span class="sxs-lookup"><span data-stu-id="91bec-109">Instead, the DLL is unloaded.</span></span>

-   <span data-ttu-id="91bec-110">**Perflib \_ Impossibile \_ \_ \_ trovare il processo di apertura**: registrato quando il nome della stored procedure definito nel registro di sistema non è stato trovato nella dll come funzione esportata.</span><span class="sxs-lookup"><span data-stu-id="91bec-110">**PERFLIB\_OPEN\_PROC\_NOT\_FOUND**—Logged when the procedure name defined in the registry could not be found in the DLL as an exported function.</span></span> <span data-ttu-id="91bec-111">Questo problema si verifica in genere quando la DLL o il servizio non è installato correttamente o il nome della funzione è stato rinominato senza aggiornare la procedura di installazione.</span><span class="sxs-lookup"><span data-stu-id="91bec-111">This usually occurs when the DLL or the service is not installed correctly or the function name has been renamed without updating the installation procedure.</span></span>
-   <span data-ttu-id="91bec-112">**Perflib \_ Errore di apertura \_ proc \_**: registrato quando la procedura di apertura restituisce uno stato di errore diverso da Error \_ Success.</span><span class="sxs-lookup"><span data-stu-id="91bec-112">**PERFLIB\_OPEN\_PROC\_FAILURE**—Logged when the open procedure returned an error status other than ERROR\_SUCCESS.</span></span> <span data-ttu-id="91bec-113">In tal caso, è necessario che nella DLL sia stata immessa anche una voce del registro eventi che descrive le condizioni che hanno causato l'errore.</span><span class="sxs-lookup"><span data-stu-id="91bec-113">Should this happen, the DLL should have also entered an event log entry describing the conditions that caused the failure.</span></span>
-   <span data-ttu-id="91bec-114">**Perflib \_ Apri \_ \_ eccezione proc**: registrato quando la procedura di apertura rileva un'eccezione non gestita.</span><span class="sxs-lookup"><span data-stu-id="91bec-114">**PERFLIB\_OPEN\_PROC\_EXCEPTION**—Logged when the open procedure encounters an unhandled exception.</span></span> <span data-ttu-id="91bec-115">Questo problema si verifica in genere a causa di una condizione di errore imprevista rilevata dalla procedura di apertura.</span><span class="sxs-lookup"><span data-stu-id="91bec-115">This is usually due to an unexpected error condition encountered by the open procedure.</span></span>

 

 

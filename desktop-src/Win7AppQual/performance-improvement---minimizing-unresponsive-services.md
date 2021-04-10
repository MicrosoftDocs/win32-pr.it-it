---
description: .
ms.assetid: 51df3fb9-416d-46b8-b3a7-0281401fb390
title: Procedure consigliate per ridurre al minimo i servizi che non rispondono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51e1fbad7fe60c4165ebb97847c303482314f68e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885238"
---
# <a name="best-practices-for-minimizing-unresponsive-services"></a><span data-ttu-id="25605-103">Procedure consigliate per ridurre al minimo i servizi che non rispondono</span><span class="sxs-lookup"><span data-stu-id="25605-103">Best Practices for Minimizing Unresponsive Services</span></span>

## <a name="affected-platform"></a><span data-ttu-id="25605-104">Piattaforma interessata</span><span class="sxs-lookup"><span data-stu-id="25605-104">Affected Platform</span></span>

 <span data-ttu-id="25605-105">**Client** – Windows Vista \| Windows 7</span><span class="sxs-lookup"><span data-stu-id="25605-105">**Clients** – Windows Vista \| Windows 7</span></span>  

## <a name="description"></a><span data-ttu-id="25605-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="25605-106">Description</span></span>

<span data-ttu-id="25605-107">I servizi che non rispondono possono causare timeout, sessioni interrotte e persino dati persi.</span><span class="sxs-lookup"><span data-stu-id="25605-107">Unresponsive services can result in timeouts, terminated sessions, and even lost data.</span></span> <span data-ttu-id="25605-108">L'utilizzo delle procedure consigliate può ridurre notevolmente l'occorrenza di servizi che non rispondono.</span><span class="sxs-lookup"><span data-stu-id="25605-108">Employing best practices can greatly reduce the occurrence of unresponsive services.</span></span>

## <a name="best-practices"></a><span data-ttu-id="25605-109">Procedure consigliate</span><span class="sxs-lookup"><span data-stu-id="25605-109">Best Practices</span></span>

<span data-ttu-id="25605-110">Assicurarsi che le applicazioni e tutti i relativi servizi e driver dipendenti rispondano alle notifiche di accensione e spegnimento del sistema.</span><span class="sxs-lookup"><span data-stu-id="25605-110">Make sure your applications and all of their dependent services and drivers respond to system power and shutdown notifications.</span></span>

-   <span data-ttu-id="25605-111">Tutte le applicazioni devono rispondere tempestivamente e in modo appropriato ai messaggi di chiusura, ad esempio WM \_ QUERYENDSESSION e WM \_ ENDSESSION, che indicano che è in corso l'arresto.</span><span class="sxs-lookup"><span data-stu-id="25605-111">All applications should respond promptly and appropriately to shutdown messages such as WM\_QUERYENDSESSION and WM\_ENDSESSION that indicate a shutdown is in progress.</span></span>
-   <span data-ttu-id="25605-112">Tutti i servizi devono rispondere tempestivamente alle notifiche di chiusura di SCM.</span><span class="sxs-lookup"><span data-stu-id="25605-112">All services should promptly respond to SCM shutdown notifications.</span></span> <span data-ttu-id="25605-113">In caso contrario, il computer li considera non risponde e avvia un timeout di 20 secondi e li arresta, aprendo la possibilità di perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="25605-113">If they fail to do so, the machine treats them as unresponsive and initiates a 20-second time-out and stops them, opening up the possibility of lost data.</span></span> <span data-ttu-id="25605-114">Vengono inoltre aggiunti 20 secondi all'ora di arresto dell'arresto di un computer.</span><span class="sxs-lookup"><span data-stu-id="25605-114">This also adds 20 seconds to the shutdown time of a machine shutdown.</span></span>
-   <span data-ttu-id="25605-115">Tutti i servizi che hanno dipendenze del driver di dispositivo kernel devono rispondere tempestivamente e in modo appropriato alla \_ notifica di arresto per l'IRP \_ di MJ nelle routine DispatchShutdown.</span><span class="sxs-lookup"><span data-stu-id="25605-115">All services that have kernel device driver dependencies should respond promptly and appropriately to IRP\_MJ\_SHUTDOWN notification in their DispatchShutdown routines.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="25605-116">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="25605-116">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="25605-117">Windows Performance Toolkit</span><span class="sxs-lookup"><span data-stu-id="25605-117">Windows Performance Toolkit</span></span>](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)  
</dl>

 

 




---
description: Procedure consigliate per ridurre al minimo i servizi che non rispondono
ms.assetid: 51df3fb9-416d-46b8-b3a7-0281401fb390
title: Procedure consigliate per ridurre al minimo i servizi che non rispondono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90416e8256383e16fd78c436dfaa8d6a2186c540
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087999"
---
# <a name="best-practices-for-minimizing-unresponsive-services"></a><span data-ttu-id="f3202-103">Procedure consigliate per ridurre al minimo i servizi che non rispondono</span><span class="sxs-lookup"><span data-stu-id="f3202-103">Best Practices for Minimizing Unresponsive Services</span></span>

## <a name="affected-platform"></a><span data-ttu-id="f3202-104">Piattaforma interessata</span><span class="sxs-lookup"><span data-stu-id="f3202-104">Affected Platform</span></span>

 <span data-ttu-id="f3202-105">**Client** : Windows Vista \| Windows 7</span><span class="sxs-lookup"><span data-stu-id="f3202-105">**Clients** – Windows Vista \| Windows 7</span></span>  

## <a name="description"></a><span data-ttu-id="f3202-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3202-106">Description</span></span>

<span data-ttu-id="f3202-107">I servizi che non rispondono possono comportare timeout, sessioni terminate e persino perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="f3202-107">Unresponsive services can result in timeouts, terminated sessions, and even lost data.</span></span> <span data-ttu-id="f3202-108">L'utilizzo di procedure consigliate può ridurre notevolmente il numero di servizi che non rispondono.</span><span class="sxs-lookup"><span data-stu-id="f3202-108">Employing best practices can greatly reduce the occurrence of unresponsive services.</span></span>

## <a name="best-practices"></a><span data-ttu-id="f3202-109">Procedure consigliate</span><span class="sxs-lookup"><span data-stu-id="f3202-109">Best Practices</span></span>

<span data-ttu-id="f3202-110">Assicurarsi che le applicazioni e tutti i relativi servizi e driver dipendenti rispondano alle notifiche relative all'alimentazione e all'arresto del sistema.</span><span class="sxs-lookup"><span data-stu-id="f3202-110">Make sure your applications and all of their dependent services and drivers respond to system power and shutdown notifications.</span></span>

-   <span data-ttu-id="f3202-111">Tutte le applicazioni devono rispondere tempestivamente e in modo appropriato ai messaggi di arresto, ad esempio WM QUERYENDSESSION e WM ENDSESSION che indicano che è in corso \_ \_ un arresto.</span><span class="sxs-lookup"><span data-stu-id="f3202-111">All applications should respond promptly and appropriately to shutdown messages such as WM\_QUERYENDSESSION and WM\_ENDSESSION that indicate a shutdown is in progress.</span></span>
-   <span data-ttu-id="f3202-112">Tutti i servizi devono rispondere tempestivamente alle notifiche di arresto di Gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="f3202-112">All services should promptly respond to SCM shutdown notifications.</span></span> <span data-ttu-id="f3202-113">In caso contrario, il computer li considera come non risponde e avvia un timeout di 20 secondi e li arresta, aprendo la possibilità di perdere i dati.</span><span class="sxs-lookup"><span data-stu-id="f3202-113">If they fail to do so, the machine treats them as unresponsive and initiates a 20-second time-out and stops them, opening up the possibility of lost data.</span></span> <span data-ttu-id="f3202-114">Ciò aggiunge anche 20 secondi all'ora di arresto di un computer.</span><span class="sxs-lookup"><span data-stu-id="f3202-114">This also adds 20 seconds to the shutdown time of a machine shutdown.</span></span>
-   <span data-ttu-id="f3202-115">Tutti i servizi con dipendenze del driver di dispositivo kernel devono rispondere tempestivamente e in modo appropriato alla notifica \_ IRP MJ SHUTDOWN nelle \_ routine DispatchShutdown.</span><span class="sxs-lookup"><span data-stu-id="f3202-115">All services that have kernel device driver dependencies should respond promptly and appropriately to IRP\_MJ\_SHUTDOWN notification in their DispatchShutdown routines.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="f3202-116">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="f3202-116">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="f3202-117">Windows Performance Toolkit</span><span class="sxs-lookup"><span data-stu-id="f3202-117">Windows Performance Toolkit</span></span>](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)  
</dl>

 

 




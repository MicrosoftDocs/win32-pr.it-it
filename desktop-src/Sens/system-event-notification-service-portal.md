---
description: Monitorare le notifiche degli eventi di sistema dai programmi eseguiti sui computer portatili per determinare la latenza e la larghezza di banda della connessione di rete. Scrivi applicazioni ottimizzate per il mobile computing e le LAN a latenza elevata.
ms.assetid: a27386c5-1ab3-448a-88d9-8c9a18599e59
title: Servizio di notifica eventi di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3238441f82c26a33370c37fe09b3e4007639f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968199"
---
# <a name="system-event-notification-service"></a><span data-ttu-id="8558b-104">Servizio di notifica eventi di sistema</span><span class="sxs-lookup"><span data-stu-id="8558b-104">System Event Notification Service</span></span>

## <a name="purpose"></a><span data-ttu-id="8558b-105">Scopo</span><span class="sxs-lookup"><span data-stu-id="8558b-105">Purpose</span></span>

<span data-ttu-id="8558b-106">Le applicazioni progettate per l'uso da parte degli utenti mobili richiedono un set univoco di notifiche e funzioni di connettività.</span><span class="sxs-lookup"><span data-stu-id="8558b-106">Applications designed for use by mobile users require a unique set of connectivity functions and notifications.</span></span> <span data-ttu-id="8558b-107">In passato queste singole applicazioni erano necessarie per implementare queste funzionalità internamente.</span><span class="sxs-lookup"><span data-stu-id="8558b-107">In the past these individual applications were required to implement these features internally.</span></span> <span data-ttu-id="8558b-108">Il servizio di notifica eventi di sistema (SENS) offre ora queste funzionalità nel sistema operativo, creando una connettività uniforme e un'interfaccia di notifica per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="8558b-108">The System Event Notification Service (SENS) now provides these capabilities in the operating system, creating a uniform connectivity and notification interface for applications.</span></span> <span data-ttu-id="8558b-109">L'uso degli sviluppatori di SENS può determinare la larghezza di banda di connessione e le informazioni sulla latenza all'interno dell'applicazione e ottimizzare l'operazione dell'applicazione in base a tali condizioni.</span><span class="sxs-lookup"><span data-stu-id="8558b-109">Using SENS developers can determine connection bandwidth and latency information from within their application and optimize the application's operation based on those conditions.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="8558b-110">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="8558b-110">Where applicable</span></span>

<span data-ttu-id="8558b-111">Le funzioni di connettività e le notifiche di SENS sono utili per le applicazioni scritte per computer portatili o computer connessi a reti locali a latenza elevata.</span><span class="sxs-lookup"><span data-stu-id="8558b-111">The connectivity functions and notifications of SENS are useful for applications written for mobile computers or computers connected to high latency local area networks.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="8558b-112">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="8558b-112">Developer audience</span></span>

<span data-ttu-id="8558b-113">Questo documento è destinato agli sviluppatori di software che sviluppano applicazioni per il mobile computing e le reti locali a latenza elevata.</span><span class="sxs-lookup"><span data-stu-id="8558b-113">This document is intended for software developers who develop applications for mobile computing and high latency local area networks.</span></span> <span data-ttu-id="8558b-114">Questo documento fornisce un riferimento completo di tutte le parti del servizio di notifica degli eventi di sistema, inclusi l'oggetto SENS e i metodi di supporto.</span><span class="sxs-lookup"><span data-stu-id="8558b-114">This document provides a complete reference of all parts of the System Event Notification Service including the SENS object and supporting methods.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="8558b-115">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="8558b-115">Run-time requirements</span></span>

<span data-ttu-id="8558b-116">Richiede Microsoft Windows XP o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="8558b-116">Requires Microsoft Windows XP or later.</span></span> <span data-ttu-id="8558b-117">Per informazioni sui sistemi operativi necessari per usare un'interfaccia o una funzione specifica, vedere la sezione requisiti della documentazione.</span><span class="sxs-lookup"><span data-stu-id="8558b-117">For information about which operating systems are required to use a particular interface or function, see the Requirements section of the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8558b-118">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="8558b-118">In this section</span></span>



| <span data-ttu-id="8558b-119">Argomento</span><span class="sxs-lookup"><span data-stu-id="8558b-119">Topic</span></span>                                                              | <span data-ttu-id="8558b-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8558b-120">Description</span></span>                                                                           |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="8558b-121">Overview</span><span class="sxs-lookup"><span data-stu-id="8558b-121">Overview</span></span>](about-system-event-notification-service.md)<br/> | <span data-ttu-id="8558b-122">Informazioni generali sul servizio di notifica eventi di sistema.</span><span class="sxs-lookup"><span data-stu-id="8558b-122">General information about System Event Notification Service.</span></span><br/>               |
| [<span data-ttu-id="8558b-123">Riferimento</span><span class="sxs-lookup"><span data-stu-id="8558b-123">Reference</span></span>](sens-reference.md)<br/>                         | <span data-ttu-id="8558b-124">Documentazione relativa a metodi e interfacce del servizio di notifica degli eventi di sistema.</span><span class="sxs-lookup"><span data-stu-id="8558b-124">Documentation of System Event Notification Service methods and interfaces.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="8558b-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8558b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8558b-126">**IEventSubscription**</span><span class="sxs-lookup"><span data-stu-id="8558b-126">**IEventSubscription**</span></span>](/windows/win32/api/eventsys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 

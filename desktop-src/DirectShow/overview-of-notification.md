---
description: Panoramica della notifica degli eventi
ms.assetid: c8b960db-fb8b-4c32-99c3-9d83432574cc
title: Panoramica della notifica degli eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c60c3251a74606f07f25ab6870cfd1f333ecbbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746567"
---
# <a name="overview-of-event-notification"></a><span data-ttu-id="f7b60-103">Panoramica della notifica degli eventi</span><span class="sxs-lookup"><span data-stu-id="f7b60-103">Overview of Event Notification</span></span>

<span data-ttu-id="f7b60-104">Un filtro notifica a Filter Graph Manager informazioni su un evento pubblicando una notifica degli eventi.</span><span class="sxs-lookup"><span data-stu-id="f7b60-104">A filter notifies the Filter Graph Manager about an event by posting an event notification.</span></span> <span data-ttu-id="f7b60-105">Potrebbe trattarsi di un evento previsto, ad esempio la fine di un flusso, oppure potrebbe rappresentare un errore, ad esempio un errore di rendering di un flusso.</span><span class="sxs-lookup"><span data-stu-id="f7b60-105">The event could be something expected, such as the end of a stream, or it could represent an error, such as a failure to render a stream.</span></span> <span data-ttu-id="f7b60-106">Il gestore del grafico del filtro gestisce alcuni eventi di filtro in modo autonomo e ne lascia gli altri per la gestione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f7b60-106">The Filter Graph Manager handles some filter events by itself, and it leaves others for the application to handle.</span></span> <span data-ttu-id="f7b60-107">Se il gestore del grafico del filtro non gestisce un evento di filtro, inserisce la notifica degli eventi in una coda.</span><span class="sxs-lookup"><span data-stu-id="f7b60-107">If the Filter Graph Manager does not handle a filter event, it places the event notification into a queue.</span></span> <span data-ttu-id="f7b60-108">Il grafico del filtro può anche accodare le proprie notifiche degli eventi per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f7b60-108">The filter graph can also queue its own event notifications for the application.</span></span>

<span data-ttu-id="f7b60-109">Un'applicazione recupera gli eventi dalla coda e li risponde in base al tipo di evento.</span><span class="sxs-lookup"><span data-stu-id="f7b60-109">An application retrieves events from the queue and responds to them based on the type of event.</span></span> <span data-ttu-id="f7b60-110">La notifica degli eventi in DirectShow è pertanto simile allo schema di Accodamento messaggi di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f7b60-110">Event notification in DirectShow is therefore similar to the Microsoft Windows message queuing scheme.</span></span> <span data-ttu-id="f7b60-111">Un'applicazione può inoltre annullare il comportamento predefinito di Filter Graph Manager per un determinato tipo di evento.</span><span class="sxs-lookup"><span data-stu-id="f7b60-111">An application can also cancel the Filter Graph Manager's default behavior for a given event type.</span></span> <span data-ttu-id="f7b60-112">Il gestore del grafico dei filtri inserisce quindi tali eventi direttamente nella coda affinché l'applicazione venga gestita.</span><span class="sxs-lookup"><span data-stu-id="f7b60-112">The Filter Graph Manager then puts those events directly into the queue for the application to handle.</span></span>

<span data-ttu-id="f7b60-113">Questo meccanismo Abilita</span><span class="sxs-lookup"><span data-stu-id="f7b60-113">This mechanism enables</span></span>

-   <span data-ttu-id="f7b60-114">Gestore del grafico di filtro per comunicare con l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f7b60-114">The Filter Graph Manager to communicate with the application.</span></span>
-   <span data-ttu-id="f7b60-115">Filtra per comunicare con l'applicazione e con il gestore del grafo dei filtri.</span><span class="sxs-lookup"><span data-stu-id="f7b60-115">Filters to communicate with both the application and the Filter Graph Manager.</span></span>
-   <span data-ttu-id="f7b60-116">Applicazione per determinare il livello di coinvolgimento nella gestione degli eventi.</span><span class="sxs-lookup"><span data-stu-id="f7b60-116">The application to determine its degree of involvement in handling events.</span></span>

 

 




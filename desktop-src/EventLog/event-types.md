---
description: Sono disponibili cinque tipi di eventi che è possibile registrare. Tutti questi contengono dati comuni ben definiti e possono facoltativamente includere dati specifici degli eventi.
ms.assetid: 4ab4a284-a4cd-4cf7-a9d2-e4a75fce01b9
title: Tipi di evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3832f90ccdb8dafc676c139f92665efde732533c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880889"
---
# <a name="event-types"></a><span data-ttu-id="602a0-104">Tipi di evento</span><span class="sxs-lookup"><span data-stu-id="602a0-104">Event Types</span></span>

<span data-ttu-id="602a0-105">Sono disponibili cinque tipi di eventi che è possibile registrare.</span><span class="sxs-lookup"><span data-stu-id="602a0-105">There are five types of events that can be logged.</span></span> <span data-ttu-id="602a0-106">Tutti questi contengono dati comuni ben definiti e possono facoltativamente includere dati specifici degli eventi.</span><span class="sxs-lookup"><span data-stu-id="602a0-106">All of these have well-defined common data and can optionally include event-specific data.</span></span>

<span data-ttu-id="602a0-107">L'applicazione indica il tipo di evento quando segnala un evento.</span><span class="sxs-lookup"><span data-stu-id="602a0-107">The application indicates the event type when it reports an event.</span></span> <span data-ttu-id="602a0-108">Ogni evento deve essere di un solo tipo.</span><span class="sxs-lookup"><span data-stu-id="602a0-108">Each event must be of a single type.</span></span> <span data-ttu-id="602a0-109">Il Visualizzatore eventi Visualizza un'icona diversa per ogni tipo nella visualizzazione elenco del registro eventi.</span><span class="sxs-lookup"><span data-stu-id="602a0-109">The Event Viewer displays a different icon for each type in the list view of the event log.</span></span>

<span data-ttu-id="602a0-110">Nella tabella seguente vengono descritti i cinque tipi di eventi utilizzati nella registrazione degli eventi.</span><span class="sxs-lookup"><span data-stu-id="602a0-110">The following table describes the five event types used in event logging.</span></span>



| <span data-ttu-id="602a0-111">Tipo di evento</span><span class="sxs-lookup"><span data-stu-id="602a0-111">Event type</span></span>        | <span data-ttu-id="602a0-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="602a0-112">Description</span></span>                                                                                                                                                                                                                                                                                              |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="602a0-113">**Error (Errore) (Error (Errore)e)**</span><span class="sxs-lookup"><span data-stu-id="602a0-113">**Error**</span></span>         | <span data-ttu-id="602a0-114">Evento che indica un problema significativo, ad esempio la perdita di dati o la perdita di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="602a0-114">An event that indicates a significant problem such as loss of data or loss of functionality.</span></span> <span data-ttu-id="602a0-115">Se, ad esempio, un servizio non viene caricato durante l'avvio, viene registrato un evento di errore.</span><span class="sxs-lookup"><span data-stu-id="602a0-115">For example, if a service fails to load during startup, an Error event is logged.</span></span>                                                                                                                           |
| <span data-ttu-id="602a0-116">**Avviso**</span><span class="sxs-lookup"><span data-stu-id="602a0-116">**Warning**</span></span>       | <span data-ttu-id="602a0-117">Un evento che non è necessariamente significativo, ma potrebbe indicare un possibile problema futuro.</span><span class="sxs-lookup"><span data-stu-id="602a0-117">An event that is not necessarily significant, but may indicate a possible future problem.</span></span> <span data-ttu-id="602a0-118">Ad esempio, quando lo spazio su disco è insufficiente, viene registrato un evento di avviso.</span><span class="sxs-lookup"><span data-stu-id="602a0-118">For example, when disk space is low, a Warning event is logged.</span></span> <span data-ttu-id="602a0-119">Se un'applicazione può eseguire il ripristino da un evento senza perdita di funzionalità o dati, in genere può classificare l'evento come un evento di avviso.</span><span class="sxs-lookup"><span data-stu-id="602a0-119">If an application can recover from an event without loss of functionality or data, it can generally classify the event as a Warning event.</span></span>     |
| <span data-ttu-id="602a0-120">**Informazioni**</span><span class="sxs-lookup"><span data-stu-id="602a0-120">**Information**</span></span>   | <span data-ttu-id="602a0-121">Evento che descrive il funzionamento corretto di un'applicazione, un driver o un servizio.</span><span class="sxs-lookup"><span data-stu-id="602a0-121">An event that describes the successful operation of an application, driver, or service.</span></span> <span data-ttu-id="602a0-122">Ad esempio, quando un driver di rete viene caricato correttamente, potrebbe essere opportuno registrare un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="602a0-122">For example, when a network driver loads successfully, it may be appropriate to log an Information event.</span></span> <span data-ttu-id="602a0-123">Si noti che in genere non è appropriato che un'applicazione desktop registri un evento ogni volta che viene avviato.</span><span class="sxs-lookup"><span data-stu-id="602a0-123">Note that it is generally inappropriate for a desktop application to log an event each time it starts.</span></span> |
| <span data-ttu-id="602a0-124">**Controllo con esito positivo**</span><span class="sxs-lookup"><span data-stu-id="602a0-124">**Success Audit**</span></span> | <span data-ttu-id="602a0-125">Un evento che registra un tentativo di accesso di sicurezza controllato che ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="602a0-125">An event that records an audited security access attempt that is successful.</span></span> <span data-ttu-id="602a0-126">Ad esempio, un tentativo dell'utente di accedere al sistema viene registrato come evento di controllo con esito positivo.</span><span class="sxs-lookup"><span data-stu-id="602a0-126">For example, a user's successful attempt to log on to the system is logged as a Success Audit event.</span></span>                                                                                                                        |
| <span data-ttu-id="602a0-127">**Controllo con esito negativo**</span><span class="sxs-lookup"><span data-stu-id="602a0-127">**Failure Audit**</span></span> | <span data-ttu-id="602a0-128">Un evento che registra un tentativo di accesso di sicurezza controllato che ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="602a0-128">An event that records an audited security access attempt that fails.</span></span> <span data-ttu-id="602a0-129">Se, ad esempio, un utente tenta di accedere a un'unità di rete e ha esito negativo, il tentativo viene registrato come evento di controllo non riuscito.</span><span class="sxs-lookup"><span data-stu-id="602a0-129">For example, if a user tries to access a network drive and fails, the attempt is logged as a Failure Audit event.</span></span>                                                                                                                   |



 

<span data-ttu-id="602a0-130">Le attività selezionate degli utenti possono essere rilevate tramite il controllo degli eventi di sicurezza e quindi l'inserimento di voci nel registro di sicurezza di un computer.</span><span class="sxs-lookup"><span data-stu-id="602a0-130">Selected activities of users can be tracked by auditing security events and then placing entries in a computer's security log.</span></span>

 

 




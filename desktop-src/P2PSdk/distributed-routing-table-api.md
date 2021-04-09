---
description: L'API DRT (Distributed routing table) consente alle applicazioni di pubblicare e risolvere chiavi numeriche in una rete peer.
ms.assetid: 17422d71-4c6d-458b-87b6-b31fc2b5bda5
title: API Tabella di routing distribuito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f8c2b435e1c0c813fb279c40b9bbfa9afb6b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104050025"
---
# <a name="distributed-routing-table-api"></a><span data-ttu-id="e071e-103">API Tabella di routing distribuito</span><span class="sxs-lookup"><span data-stu-id="e071e-103">Distributed Routing Table API</span></span>

<span data-ttu-id="e071e-104">L'API DRT (Distributed routing table) consente alle applicazioni di pubblicare e risolvere chiavi numeriche in una rete peer.</span><span class="sxs-lookup"><span data-stu-id="e071e-104">The Distributed Routing Table (DRT) API allows applications to publish and resolve numeric keys in a peer network.</span></span>

<span data-ttu-id="e071e-105">Un'applicazione che utilizza DRT può eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="e071e-105">An application utilizing DRT can accomplish the following:</span></span>

-   <span data-ttu-id="e071e-106">Creazione di tabelle di routing distribuite specifiche dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e071e-106">Create application-specific Distributed Routing Tables.</span></span>
-   <span data-ttu-id="e071e-107">Registrare le chiavi e associarle agli indirizzi IP e ai dati dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e071e-107">Register keys, and associate these keys with IP addresses and application data.</span></span>
-   <span data-ttu-id="e071e-108">Cercare le chiavi e recuperare gli indirizzi IP e i dati dell'applicazione associati.</span><span class="sxs-lookup"><span data-stu-id="e071e-108">Search for keys and retrieve the IP addresses and application data associated with them.</span></span> <span data-ttu-id="e071e-109">Questa funzionalità può essere utilizzata per costruire tabelle hash distribuite (DHT), sistemi di risoluzione dei nomi senza server e reti mesh sovrapposte di molte topologie.</span><span class="sxs-lookup"><span data-stu-id="e071e-109">This functionality can be used to construct Distributed Hash Tables (DHTs), serverless name resolution systems, and overlay mesh networks of many topologies.</span></span>

> [!Note]  
> <span data-ttu-id="e071e-110">Gli amministratori e gli utenti di applicazioni abilitate per DRT devono fare in modo che gli utenti finali delle proprie applicazioni riconoscano le informazioni pubblicate.</span><span class="sxs-lookup"><span data-stu-id="e071e-110">The administrators and users of DRT-enabled applications should make the end users of their applications aware of the information being published.</span></span> <span data-ttu-id="e071e-111">I server Microsoft non sono utilizzati da questa tecnologia e le informazioni non vengono inviate a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e071e-111">Microsoft servers are not employed by this technology and information is not sent to Microsoft.</span></span>

 

<span data-ttu-id="e071e-112">La documentazione fornita per questa API è divisa in tre sezioni.</span><span class="sxs-lookup"><span data-stu-id="e071e-112">The provided documentation for this API is divided into three sections.</span></span>



| <span data-ttu-id="e071e-113">Sezione</span><span class="sxs-lookup"><span data-stu-id="e071e-113">Section</span></span>                                                                                | <span data-ttu-id="e071e-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e071e-114">Description</span></span>                                                                                                          |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e071e-115">Informazioni sulle tabelle di routing distribuite</span><span class="sxs-lookup"><span data-stu-id="e071e-115">About Distributed Routing Tables</span></span>](about-distributed-routing-tables.md)               | <span data-ttu-id="e071e-116">Informazioni che descrivono in dettaglio il ciclo di vita e le modifiche di stato dell'API DRT.</span><span class="sxs-lookup"><span data-stu-id="e071e-116">Information detailing the life cycle and state changes of the DRT API.</span></span><br/>                                    |
| [<span data-ttu-id="e071e-117">Uso del API Tabella di routing distribuito</span><span class="sxs-lookup"><span data-stu-id="e071e-117">Using the Distributed Routing Table API</span></span>](using-the-distributed-routing-table-api.md) | <span data-ttu-id="e071e-118">Informazioni che descrivono in dettaglio l'utilizzo generale dell'API DRT.</span><span class="sxs-lookup"><span data-stu-id="e071e-118">Information detailing the general usage of the DRT API.</span></span><br/>                                                   |
| [<span data-ttu-id="e071e-119">Riferimento API Tabella routing distribuito</span><span class="sxs-lookup"><span data-stu-id="e071e-119">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md) | <span data-ttu-id="e071e-120">Informazioni che descrivono in dettaglio le funzioni, le strutture di dati e le costanti enumerate che comprendono l'API DRT.</span><span class="sxs-lookup"><span data-stu-id="e071e-120">Information detailing the functions, data structures, and enumerated constants that comprise the DRT API.</span></span><br/> |



 

 

 





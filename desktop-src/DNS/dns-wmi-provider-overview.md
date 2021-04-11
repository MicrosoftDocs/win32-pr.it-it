---
title: Panoramica del provider WMI DNS
description: Un provider è un elemento architetturale di Strumentazione gestione Windows (WMI).
ms.assetid: e6ada7b5-dd46-4c47-8db8-55f910429e31
keywords:
- Domain Name System, provider WMI, architettura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6aed54d0d9cbac4070483e8e72e9917607e824c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044585"
---
# <a name="dns-wmi-provider-overview"></a><span data-ttu-id="c6dc8-104">Panoramica del provider WMI DNS</span><span class="sxs-lookup"><span data-stu-id="c6dc8-104">DNS WMI Provider Overview</span></span>

<span data-ttu-id="c6dc8-105">Un provider è un elemento architetturale di *Strumentazione gestione Windows (WMI)*.</span><span class="sxs-lookup"><span data-stu-id="c6dc8-105">A provider is an architectural element of *Windows Management Instrumentation (WMI)*.</span></span> <span data-ttu-id="c6dc8-106">WMI definisce un'architettura unificata per la descrizione, l'accesso e la strumentazione degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="c6dc8-106">WMI defines a unified architecture for describing, accessing, and instrumenting objects.</span></span> <span data-ttu-id="c6dc8-107">Parte di questa architettura è un database di grandi dimensioni di classi WMI utilizzate per eseguire attività di gestione remota su oggetti specifici.</span><span class="sxs-lookup"><span data-stu-id="c6dc8-107">Part of this architecture is a large database of WMI classes used to carry out remote management tasks on specific objects.</span></span>

<span data-ttu-id="c6dc8-108">I provider WMI fungono da intermediari tra WMI e uno o più oggetti gestiti.</span><span class="sxs-lookup"><span data-stu-id="c6dc8-108">WMI providers act as intermediaries between WMI and one or more managed objects.</span></span> <span data-ttu-id="c6dc8-109">Quando WMI riceve una richiesta da un'applicazione di gestione per i dati che non sono disponibili dal repository CIM o per le notifiche di eventi non supportati da WMI, inoltra la richiesta a un provider.</span><span class="sxs-lookup"><span data-stu-id="c6dc8-109">When WMI receives a request from a management application for data that is not available from the CIM repository or for notifications of events that WMI does not support, it forwards the request to a provider.</span></span> <span data-ttu-id="c6dc8-110">I provider forniscono dati e notifiche di eventi per gli oggetti gestiti specifici del proprio dominio.</span><span class="sxs-lookup"><span data-stu-id="c6dc8-110">Providers supply data and event notifications for managed objects that are specific to their particular domain.</span></span> <span data-ttu-id="c6dc8-111">Un provider estende lo schema WMI delle classi per consentire l'utilizzo di WMI con nuovi tipi di oggetti.</span><span class="sxs-lookup"><span data-stu-id="c6dc8-111">A provider extends the WMI schema of classes to allow WMI to work with new types of objects.</span></span> <span data-ttu-id="c6dc8-112">Il provider WMI DNS definisce le classi per l'esecuzione di query e la configurazione di un server DNS, insieme alle zone DNS e ai record DNS associati.</span><span class="sxs-lookup"><span data-stu-id="c6dc8-112">The DNS WMI Provider defines classes for querying and configuring a DNS Server, along with its associated DNS zones and DNS records.</span></span>

<span data-ttu-id="c6dc8-113">Il provider WMI DNS espone alcuni oggetti DNS ai client, tra cui server DNS, dominio DNS e oggetti RR DNS.</span><span class="sxs-lookup"><span data-stu-id="c6dc8-113">The DNS WMI provider exposes a number of DNS objects to clients, including DNS Server, DNS domain, and DNS RR objects.</span></span> <span data-ttu-id="c6dc8-114">Attraverso questi oggetti, i client sono in grado di eseguire attività di gestione DNS.</span><span class="sxs-lookup"><span data-stu-id="c6dc8-114">Through those objects, clients are able to perform DNS management activities.</span></span>

<span data-ttu-id="c6dc8-115">Utilizzando il provider WMI DNS, è possibile creare strumenti personalizzati per eseguire la maggior parte delle attività di amministrazione del server DNS.</span><span class="sxs-lookup"><span data-stu-id="c6dc8-115">Using the DNS WMI Provider, you can create your own tools to perform most DNS Server administration tasks.</span></span> <span data-ttu-id="c6dc8-116">Ad esempio, è possibile creare, eliminare e visualizzare le zone e i record; Reimposta le proprietà del server e della zona; ed eseguono operazioni di amministrazione di routine, ad esempio l'aggiornamento della zona, il ricaricamento della zona, l'aggiornamento della zona, la riscrittura della zona in un file o Active Directory, la sospensione e la ripresa della zona, la cancellazione della cache, l'arresto e l'avvio del servizio DNS e la visualizzazione delle statistiche.</span><span class="sxs-lookup"><span data-stu-id="c6dc8-116">For example, you can create, delete, and view zones and records; reset server and zone properties; and perform routine administration operations such as updating the zone, reloading the zone, refreshing the zone, writing the zone back to a file or Active Directory, pausing and resuming the zone, clearing the cache, stopping and starting the DNS service, and viewing statistics.</span></span>

<span data-ttu-id="c6dc8-117">Il provider WMI DNS ha un set di comportamenti univoci non trovato in altri provider.</span><span class="sxs-lookup"><span data-stu-id="c6dc8-117">The DNS WMI Provider has a set of unique behaviors not found in other providers.</span></span> <span data-ttu-id="c6dc8-118">Per informazioni dettagliate sulla classe, vedere la Guida di [riferimento del provider WMI DNS](dns-wmi-provider-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="c6dc8-118">See the [DNS WMI Provider Reference](dns-wmi-provider-reference.md) for class details.</span></span>

 

 





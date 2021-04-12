---
title: Il database del servizio nome RPC
description: Un servizio nome è un servizio che esegue il mapping dei nomi agli oggetti e in genere mantiene le coppie (nome, oggetto) in un database.
ms.assetid: 9ced2307-cf30-45d5-bcd2-c1e4aae8c63b
keywords:
- RPC (Remote Procedure Call), descritto, nome del database del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19ae37473bcf28ddf995ab0a657f300ce13aa83c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471422"
---
# <a name="the-rpc-name-service-database"></a><span data-ttu-id="63111-104">Il database del servizio nome RPC</span><span class="sxs-lookup"><span data-stu-id="63111-104">The RPC Name Service Database</span></span>

<span data-ttu-id="63111-105">Un servizio nome è un servizio che esegue il mapping dei nomi agli oggetti e in genere mantiene le coppie (nome, oggetto) in un database.</span><span class="sxs-lookup"><span data-stu-id="63111-105">A name service is a service that maps names to objects, and usually maintains the (name, object) pairs in a database.</span></span> <span data-ttu-id="63111-106">In genere, il nome è un nome logico che è facile per gli utenti ricordare e usare.</span><span class="sxs-lookup"><span data-stu-id="63111-106">Generally, the name is a logical name that is easy for users to remember and use.</span></span> <span data-ttu-id="63111-107">Ad esempio, un servizio nome consente a un utente di utilizzare il nome logico "condivisione StampanteLaser".</span><span class="sxs-lookup"><span data-stu-id="63111-107">For example, a name service would allow a user to use the logical name "laserprinter."</span></span> <span data-ttu-id="63111-108">Il servizio nome esegue il mapping di questo nome al nome specifico della rete utilizzato dal server di stampa.</span><span class="sxs-lookup"><span data-stu-id="63111-108">The name service maps this name to the network-specific name used by the print server.</span></span>

<span data-ttu-id="63111-109">Per utilizzare una spiegazione semplificata, il servizio nome RPC esegue il mapping di un nome a un handle di associazione e mantiene i mapping (nome, handle di associazione) nel database del servizio del nome RPC.</span><span class="sxs-lookup"><span data-stu-id="63111-109">To use a simplified explanation, the RPC name service maps a name to a binding handle and maintains the (name, binding handle) mappings in the RPC name service database.</span></span> <span data-ttu-id="63111-110">Il servizio nome RPC consente alle applicazioni client di utilizzare un nome logico anziché una sequenza di protocollo e un indirizzo di rete specifici.</span><span class="sxs-lookup"><span data-stu-id="63111-110">The RPC name service allows client applications to use a logical name instead of a specific protocol sequence and network address.</span></span> <span data-ttu-id="63111-111">L'utilizzo del nome logico consente agli amministratori di rete di installare e configurare l'applicazione distribuita in modo più semplice.</span><span class="sxs-lookup"><span data-stu-id="63111-111">The use of the logical name makes it easier for network administrators to install and configure your distributed application.</span></span>

<span data-ttu-id="63111-112">Una voce del database del servizio nome RPC ha uno dei seguenti attributi: **Server**, **gruppo** o **profilo**.</span><span class="sxs-lookup"><span data-stu-id="63111-112">An RPC name service database entry has one of the following attributes: **server**, **group**, or **profile**.</span></span> <span data-ttu-id="63111-113">Nell'implementazione Microsoft, le voci possono avere un solo attributo, pertanto queste voci sono note anche come voci del server, voci di gruppo e voci del profilo.</span><span class="sxs-lookup"><span data-stu-id="63111-113">In the Microsoft implementation, entries can have only one attribute, so these entries are also known as server entries, group entries, and profile entries.</span></span>

<span data-ttu-id="63111-114">La voce server è costituita da UUID di interfaccia, UUID di oggetti (necessario quando il server implementa più punti di ingresso), indirizzo di rete, sequenza di protocollo ed eventuali informazioni sull'endpoint associate a endpoint noti.</span><span class="sxs-lookup"><span data-stu-id="63111-114">The server entry consists of interface UUIDs, object UUIDs (needed when the server implements multiple-entry points), network address, protocol sequence, and any endpoint information associated with well-known endpoints.</span></span> <span data-ttu-id="63111-115">Quando viene utilizzato un endpoint dinamico, le informazioni sull'endpoint vengono mantenute nel database della mappa endpoint anziché nel database del servizio dei nomi e l'endpoint viene risolto in modo analogo a qualsiasi altro endpoint dinamico.</span><span class="sxs-lookup"><span data-stu-id="63111-115">When a dynamic endpoint is used, the endpoint information is kept in the endpoint-map database rather than the name service database, and the endpoint is resolved like any other dynamic endpoint.</span></span> <span data-ttu-id="63111-116">Le voci del server sono gestite da funzioni che iniziano con il prefisso "RpcNsBinding".</span><span class="sxs-lookup"><span data-stu-id="63111-116">Server entries are managed by functions that start with the prefix "RpcNsBinding".</span></span>

<span data-ttu-id="63111-117">La voce di gruppo può contenere voci del server o altre voci di gruppo.</span><span class="sxs-lookup"><span data-stu-id="63111-117">The group entry can contain server entries or other group entries.</span></span> <span data-ttu-id="63111-118">Le voci di gruppo sono gestite da funzioni che iniziano con il prefisso "RpcNsGroup".</span><span class="sxs-lookup"><span data-stu-id="63111-118">Group entries are managed by functions that start with the prefix "RpcNsGroup".</span></span>

<span data-ttu-id="63111-119">La voce del profilo può contenere voci di profilo, gruppo o server.</span><span class="sxs-lookup"><span data-stu-id="63111-119">The profile entry can contain profile, group, or server entries.</span></span> <span data-ttu-id="63111-120">Le voci del profilo sono gestite dalle funzioni che iniziano con il prefisso "RpcNsProfile".</span><span class="sxs-lookup"><span data-stu-id="63111-120">Profile entries are managed by the functions that start with the prefix "RpcNsProfile".</span></span>

<span data-ttu-id="63111-121">In questa sezione viene presentata una panoramica del nome del database del servizio negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="63111-121">This section presents an overview of the name service database in the following topics:</span></span>

-   [<span data-ttu-id="63111-122">Linee guida sull'applicazione di servizio nome</span><span class="sxs-lookup"><span data-stu-id="63111-122">Name Service Application Guidelines</span></span>](name-service-application-guidelines.md)
-   [<span data-ttu-id="63111-123">Panoramica dell'immissione del nome del servizio</span><span class="sxs-lookup"><span data-stu-id="63111-123">An Overview of the Name Service Entry</span></span>](an-overview-of-the-name-service-entry.md)
-   [<span data-ttu-id="63111-124">Criteri per le voci del servizio dei nomi</span><span class="sxs-lookup"><span data-stu-id="63111-124">Criteria for Name Service Entries</span></span>](criteria-for-name-service-entries.md)
-   [<span data-ttu-id="63111-125">Pulizia voce servizio nome</span><span class="sxs-lookup"><span data-stu-id="63111-125">Name Service Entry Cleanup</span></span>](name-service-entry-cleanup.md)
-   [<span data-ttu-id="63111-126">Cosa accade durante una query</span><span class="sxs-lookup"><span data-stu-id="63111-126">What Happens During a Query</span></span>](what-happens-during-a-query.md)
-   [<span data-ttu-id="63111-127">Uso di Microsoft Locator</span><span class="sxs-lookup"><span data-stu-id="63111-127">Using Microsoft Locator</span></span>](using-microsoft-locator.md)
-   [<span data-ttu-id="63111-128">Uso del servizio directory delle celle (CDS)</span><span class="sxs-lookup"><span data-stu-id="63111-128">Using the Cell Directory Service (CDS)</span></span>](using-the-cell-directory-service-cds-.md)
-   [<span data-ttu-id="63111-129">Sintassi del nome</span><span class="sxs-lookup"><span data-stu-id="63111-129">Name Syntax</span></span>](name-syntax.md)

 

 





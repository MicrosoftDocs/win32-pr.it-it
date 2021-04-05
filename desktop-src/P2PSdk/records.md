---
description: I record sono un modo per comunicare tra i nodi di un grafico o i membri di un gruppo.
ms.assetid: f4c0869f-f147-4c2b-9418-3b407e22cb16
title: Record
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9c2d3c5ae3bd80bc0b3c0ca100155fc8efd7c71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968014"
---
# <a name="records"></a><span data-ttu-id="3f5ad-103">Record</span><span class="sxs-lookup"><span data-stu-id="3f5ad-103">Records</span></span>

<span data-ttu-id="3f5ad-104">I record sono un modo per comunicare tra i nodi di un grafico o i membri di un gruppo.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-104">Records are a way to communicate between nodes in a graph or members in a group.</span></span> <span data-ttu-id="3f5ad-105">Un record è costituito dalle due parti seguenti:</span><span class="sxs-lookup"><span data-stu-id="3f5ad-105">A record consists of the following two parts:</span></span>

-   <span data-ttu-id="3f5ad-106">Intestazione record</span><span class="sxs-lookup"><span data-stu-id="3f5ad-106">Record header</span></span>
-   <span data-ttu-id="3f5ad-107">Contenuto dati opaco specifico</span><span class="sxs-lookup"><span data-stu-id="3f5ad-107">Specific opaque data content</span></span>

<span data-ttu-id="3f5ad-108">L'intestazione contiene informazioni sul record, tra cui la versione, l'autore e il tipo di dati da pubblicare.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-108">The header contains information about the record, including the version, creator, and type of data being published.</span></span> <span data-ttu-id="3f5ad-109">L'intestazione contiene anche un campo degli attributi XML che consente alle applicazioni di aggiungere attributi nome-valore che descrivono i dati e di cercare in modo efficiente nel database di record record specifici che sono stati pubblicati in precedenza.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-109">The header also contains an XML attributes field that allows applications to add name-value attributes that describe the data, and to efficiently search the record database for specific records that have previously been published.</span></span> <span data-ttu-id="3f5ad-110">Il contenuto è i dati definiti dall'applicazione ed è opaco per l'infrastruttura peer.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-110">The content is the application-defined data, and is opaque to the Peer Infrastructure.</span></span>

<span data-ttu-id="3f5ad-111">Quando viene pubblicato un record, esso (intestazione e dati) viene sovraccaricato nel grafico o nel gruppo.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-111">When a record is published, it (both header and data) is flooded throughout the graph or group.</span></span> <span data-ttu-id="3f5ad-112">I peer sincronizzati ricevono questi dati e li archiviano in un database locale.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-112">Synchronized peers receive this data and store it in a local database.</span></span> <span data-ttu-id="3f5ad-113">I peer non sincronizzati e offline ricevono i dati la volta successiva che si connettono e si sincronizzano con il grafo o il gruppo peer.</span><span class="sxs-lookup"><span data-stu-id="3f5ad-113">Unsynchronized and offline peers receive the data the next time they connect and synchronize with the peer graph or group.</span></span>

<span data-ttu-id="3f5ad-114">Per informazioni sull'utilizzo dei record, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="3f5ad-114">For information about working with records, see the following topics:</span></span>

-   [<span data-ttu-id="3f5ad-115">Registrare le dipendenze</span><span class="sxs-lookup"><span data-stu-id="3f5ad-115">Record Dependencies</span></span>](record-dependencies.md)
-   [<span data-ttu-id="3f5ad-116">Gestione dei record</span><span class="sxs-lookup"><span data-stu-id="3f5ad-116">Record Management</span></span>](record-management.md)
-   [<span data-ttu-id="3f5ad-117">Schema attributo record</span><span class="sxs-lookup"><span data-stu-id="3f5ad-117">Record Attribute Schema</span></span>](record-attribute-schema.md)
-   [<span data-ttu-id="3f5ad-118">Formato della query di ricerca record</span><span class="sxs-lookup"><span data-stu-id="3f5ad-118">Record Search Query Format</span></span>](record-search-query-format.md)

 

 




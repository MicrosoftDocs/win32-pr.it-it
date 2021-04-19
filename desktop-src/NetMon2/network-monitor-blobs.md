---
description: Il Network Monitor BLOB (Binary Large Object) è una struttura di dati generica che contiene informazioni sulla configurazione e sulla posizione delle schede di interfaccia di rete (NIC).
ms.assetid: 910bf929-aa89-434d-83c3-07c80c627405
title: BLOB Network Monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dce6dd6ca8643eabe8ab49387c0ef39eb49b6f2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319929"
---
# <a name="network-monitor-blobs"></a><span data-ttu-id="2d3f2-103">BLOB Network Monitor</span><span class="sxs-lookup"><span data-stu-id="2d3f2-103">Network Monitor BLOBs</span></span>

<span data-ttu-id="2d3f2-104">Il Network Monitor BLOB (Binary Large Object) è una struttura di dati generica che contiene informazioni sulla configurazione e sulla posizione delle schede di interfaccia di rete (NIC).</span><span class="sxs-lookup"><span data-stu-id="2d3f2-104">The Network Monitor binary large object (BLOB) is a generic data structure that contains configuration and location information of network interface cards (NICs).</span></span> <span data-ttu-id="2d3f2-105">Usare i BLOB per rappresentare le schede di rete e filtrare le voci in un elenco di schede di rete.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-105">Use BLOBs to represent NICs and to filter entries in a list of NICs.</span></span> <span data-ttu-id="2d3f2-106">I BLOB possono inoltre contenere dati specifici dell'applicazione senza influire sugli altri dati che contengono.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-106">BLOBS can also contain application-specific data without affecting the other data that they hold.</span></span> <span data-ttu-id="2d3f2-107">L'implementazione di BLOB è opaca a tutti i livelli che devono accedere ai BLOB con le API BLOB.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-107">BLOB implementation is opaque to all levels that must access BLOBs with BLOB APIs.</span></span>

## <a name="blob-structure"></a><span data-ttu-id="2d3f2-108">Struttura BLOB</span><span class="sxs-lookup"><span data-stu-id="2d3f2-108">BLOB Structure</span></span>

<span data-ttu-id="2d3f2-109">Un BLOB può essere considerato come un albero gerarchico utilizzato per designare le stringhe.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-109">A BLOB can be considered as a hierarchical tree used to designate strings.</span></span> <span data-ttu-id="2d3f2-110">Questo albero è costituito da tre livelli: proprietario, categoria e tag.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-110">This tree has three layers: Owner, Category, and Tag.</span></span> <span data-ttu-id="2d3f2-111">Owner è una stringa che indica, in generale, che legge una voce.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-111">Owner is a string that indicates, in general, who reads an entry.</span></span> <span data-ttu-id="2d3f2-112">La categoria è anche una stringa che designa un raggruppamento funzionale generale di tag sotto il proprietario.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-112">The Category is also a string, which designates a general functional grouping of tags under the owner.</span></span> <span data-ttu-id="2d3f2-113">Il tag è il nome effettivo della voce.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-113">The Tag is the actual name of the entry.</span></span>

<span data-ttu-id="2d3f2-114">Le caratteristiche strutturali dei BLOB includono:</span><span class="sxs-lookup"><span data-stu-id="2d3f2-114">The structural characteristics of BLOBs include:</span></span>

-   <span data-ttu-id="2d3f2-115">Gli helper BLOB all'interno di un processo sono protetti l'uno dall'altro da un mutex incorporato in ogni BLOB.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-115">BLOB helpers within one process are protected from one another by a mutex built into each BLOB.</span></span>
-   <span data-ttu-id="2d3f2-116">Ogni BLOB ha un numero di versione interno, in modo che gli helper possano gestire i form BLOB sia presenti che futuri.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-116">Each BLOB has an internal version number so that the helpers can handle both present and future BLOB forms.</span></span> <span data-ttu-id="2d3f2-117">È possibile che si verifichino conflitti di versione se si invia un BLOB a un altro computer tramite una chiamata di procedura remota.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-117">Version conflicts may occur if you send a BLOB to another computer via a remote procedure call.</span></span>
-   <span data-ttu-id="2d3f2-118">Il BLOB è un puntatore a un void.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-118">The BLOB itself is a pointer to a void.</span></span> <span data-ttu-id="2d3f2-119">Tenere presente che le applicazioni devono allocare BLOB con il modificatore **const** per evitare di modificare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-119">Be aware that applications should allocate BLOBs with the **const** modifier to avoid altering the contents.</span></span>
-   <span data-ttu-id="2d3f2-120">Ogni designatore e i rispettivi valori sono stringhe.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-120">Each of the designators, as well as their values, are strings.</span></span> <span data-ttu-id="2d3f2-121">Tenere presente che le stringhe restituite dalle funzioni **GetString** sono in realtà puntatori al BLOB e non devono essere modificate.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-121">Be aware that the strings returned by **GetString** functions are actually pointers into the BLOB and should not be changed.</span></span> <span data-ttu-id="2d3f2-122">Per questo motivo, è necessario specificare queste stringhe come **const char** _ \_ px \* per evitare che le applicazioni le modifichino accidentalmente.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-122">For this reason, these strings must be specified as **const char** _\_pX\* to keep applications from accidentally changing them.</span></span>

<span data-ttu-id="2d3f2-123">In generale, tutti i parametri con l'indicatore **const** incoraggiano il chiamante ad evitare la modifica dei valori anziché impedire alle funzioni di supporto di modificarle.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-123">In general, all parameters with the **const** designator encourage the caller to refrain from changing the values rather than prohibit the helper functions from changing them.</span></span> <span data-ttu-id="2d3f2-124">Infatti, le funzioni di supporto in genere modificano tali valori.</span><span class="sxs-lookup"><span data-stu-id="2d3f2-124">In fact, the helper functions will usually change those values.</span></span>

 

 




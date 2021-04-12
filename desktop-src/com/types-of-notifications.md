---
title: Tipi di notifiche
description: Tipi di notifiche
ms.assetid: 1e7f44ea-f4ac-457e-96a3-94036508d7b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21216ca99e1a606aaba793371ad6b8619d13f2a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396530"
---
# <a name="types-of-notifications"></a><span data-ttu-id="4dc45-103">Tipi di notifiche</span><span class="sxs-lookup"><span data-stu-id="4dc45-103">Types of Notifications</span></span>

<span data-ttu-id="4dc45-104">Le notifiche rientrano in tre gruppi: documento composto, dati e visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="4dc45-104">Notifications fall into three groups: compound document, data, and view.</span></span> <span data-ttu-id="4dc45-105">Un oggetto invia notifiche di documenti composti in risposta alla ridenominazione, al salvataggio, alla chiusura o, nel caso di un collegamento, con la ridenominazione dell'origine del collegamento.</span><span class="sxs-lookup"><span data-stu-id="4dc45-105">An object sends compound document notifications in response to being renamed, saved, closed or, in the case of a link, having its link source renamed.</span></span> <span data-ttu-id="4dc45-106">Come ci si aspetterebbe, gli oggetti inviano notifiche dati in risposta alle modifiche nei dati e inviano notifiche di visualizzazione in risposta alle modifiche nella presentazione.</span><span class="sxs-lookup"><span data-stu-id="4dc45-106">As you would expect, objects send data notifications in response to changes in their data and send view notifications in response to changes in their presentation.</span></span> <span data-ttu-id="4dc45-107">Le applicazioni contenitore devono essere registrate separatamente per ognuno di questi tipi di notifica, ma tutte possono essere gestite da un singolo sink consultivo.</span><span class="sxs-lookup"><span data-stu-id="4dc45-107">Container applications must register separately for each of these notification types, but all can be handled by a single advisory sink.</span></span>

<span data-ttu-id="4dc45-108">Tutti i contenitori, il gestore dell'oggetto e il registro oggetti collegati per le notifiche dei documenti composti.</span><span class="sxs-lookup"><span data-stu-id="4dc45-108">All containers, the object handler, and the linked object register for compound document notifications.</span></span> <span data-ttu-id="4dc45-109">Il contenitore tipico viene registrato anche per le notifiche di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="4dc45-109">The typical container also registers for view notifications.</span></span> <span data-ttu-id="4dc45-110">Le notifiche dei dati vengono in genere inviate sia all'oggetto collegato che al gestore dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4dc45-110">Data notifications are usually sent to both the linked object and object handler.</span></span> <span data-ttu-id="4dc45-111">Un contenitore per scopi specifici, ad esempio quello che esegue il rendering dei dati, potrebbe trarre vantaggio dalla ricezione di notifiche di dati anziché da notifiche di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="4dc45-111">A special purpose container, such as one that renders the data itself, might benefit from receiving data notifications instead of view notifications.</span></span> <span data-ttu-id="4dc45-112">Ad esempio, un contenitore del grafico incorporato con un collegamento a una tabella può registrarsi per le notifiche dei dati.</span><span class="sxs-lookup"><span data-stu-id="4dc45-112">For example, an embedded chart container with a link to a table can register for data notifications.</span></span> <span data-ttu-id="4dc45-113">Poiché una modifica alla tabella influiscono sul grafico, la ricezione di una notifica dati indicherà al contenitore di ottenere i nuovi dati tabulari.</span><span class="sxs-lookup"><span data-stu-id="4dc45-113">Because a change to the table affects the chart, the receipt of a data notification would direct the container to get the new tabular data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4dc45-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4dc45-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4dc45-115">Notifications</span><span class="sxs-lookup"><span data-stu-id="4dc45-115">Notifications</span></span>](notifications.md)
</dt> </dl>

 

 





---
title: Stati degli oggetti
description: Stati degli oggetti
ms.assetid: 8ebef6d6-7a2f-4b95-91ca-999646cde82d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 268b9bc9c69009850a5172259ab7a13c760d2c72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297874"
---
# <a name="object-states"></a><span data-ttu-id="d2e0d-103">Stati degli oggetti</span><span class="sxs-lookup"><span data-stu-id="d2e0d-103">Object States</span></span>

<span data-ttu-id="d2e0d-104">Un oggetto composto esiste in uno dei tre stati seguenti: passivo, caricato o in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d2e0d-104">A compound object exists in one of three states: passive, loaded, or running.</span></span> <span data-ttu-id="d2e0d-105">Lo stato di un oggetto documento composto descrive la relazione tra l'oggetto nel contenitore e l'applicazione responsabile della sua creazione.</span><span class="sxs-lookup"><span data-stu-id="d2e0d-105">A compound-document object's state describes the relationship between the object in its container and the application responsible for its creation.</span></span> <span data-ttu-id="d2e0d-106">Nella tabella seguente vengono riepilogati questi Stati.</span><span class="sxs-lookup"><span data-stu-id="d2e0d-106">The following table summarizes these states.</span></span>



| <span data-ttu-id="d2e0d-107">Stato oggetto</span><span class="sxs-lookup"><span data-stu-id="d2e0d-107">Object state</span></span>       | <span data-ttu-id="d2e0d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2e0d-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2e0d-109">Passivo</span><span class="sxs-lookup"><span data-stu-id="d2e0d-109">Passive</span></span><br/> | <span data-ttu-id="d2e0d-110">L'oggetto documento composto esiste solo nello spazio di archiviazione, su disco o in un database.</span><span class="sxs-lookup"><span data-stu-id="d2e0d-110">The compound-document object exists only in storage, either on disk or in a database.</span></span> <span data-ttu-id="d2e0d-111">In questo stato, l'oggetto non è disponibile per la visualizzazione o la modifica.</span><span class="sxs-lookup"><span data-stu-id="d2e0d-111">In this state, the object is unavailable for viewing or editing.</span></span><br/>                                                                                                                                                                                                                                   |
| <span data-ttu-id="d2e0d-112">Loaded</span><span class="sxs-lookup"><span data-stu-id="d2e0d-112">Loaded</span></span><br/>  | <span data-ttu-id="d2e0d-113">Le strutture di dati dell'oggetto create dal gestore dell'oggetto si trovano nella memoria del contenitore.</span><span class="sxs-lookup"><span data-stu-id="d2e0d-113">The object's data structures created by the object handler are in the container's memory.</span></span> <span data-ttu-id="d2e0d-114">Il contenitore ha stabilito la comunicazione con il gestore oggetti e sono disponibili dati di presentazione memorizzati nella cache per il rendering dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d2e0d-114">The container has established communication with the object handler and there is cached presentation data available for rendering the object.</span></span> <span data-ttu-id="d2e0d-115">Le chiamate vengono elaborate dal gestore dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d2e0d-115">Calls are processed by the object handler.</span></span> <span data-ttu-id="d2e0d-116">Questo stato, a causa del sovraccarico ridotto, viene usato quando un utente sta semplicemente visualizzando o stampando un oggetto.</span><span class="sxs-lookup"><span data-stu-id="d2e0d-116">This state, because of its low overhead, is used when a user is simply viewing or printing an object.</span></span><br/> |
| <span data-ttu-id="d2e0d-117">In esecuzione</span><span class="sxs-lookup"><span data-stu-id="d2e0d-117">Running</span></span><br/> | <span data-ttu-id="d2e0d-118">Gli oggetti che controllano la comunicazione remota sono stati creati e l'applicazione server OLE è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d2e0d-118">The objects that control remoting have been created and the OLE server application is running.</span></span> <span data-ttu-id="d2e0d-119">Le interfacce dell'oggetto sono accessibili e il contenitore può ricevere una notifica delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="d2e0d-119">The object's interfaces are accessible, and the container can receive notification of changes.</span></span> <span data-ttu-id="d2e0d-120">In questo stato, un utente finale può modificare o modificare l'oggetto in altro modo.</span><span class="sxs-lookup"><span data-stu-id="d2e0d-120">In this state, an end user can edit or otherwise manipulate the object.</span></span><br/>                                                                                                                    |



 

<span data-ttu-id="d2e0d-121">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="d2e0d-121">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="d2e0d-122">Immissione dello stato caricato</span><span class="sxs-lookup"><span data-stu-id="d2e0d-122">Entering the Loaded State</span></span>](entering-the-loaded-state.md)
-   [<span data-ttu-id="d2e0d-123">Immissione dello stato in esecuzione</span><span class="sxs-lookup"><span data-stu-id="d2e0d-123">Entering the Running State</span></span>](entering-the-running-state.md)
-   [<span data-ttu-id="d2e0d-124">Immissione dello stato passivo</span><span class="sxs-lookup"><span data-stu-id="d2e0d-124">Entering the Passive State</span></span>](entering-the-passive-state.md)

## <a name="related-topics"></a><span data-ttu-id="d2e0d-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d2e0d-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2e0d-126">Documenti composti</span><span class="sxs-lookup"><span data-stu-id="d2e0d-126">Compound Documents</span></span>](compound-documents.md)
</dt> </dl>

 

 






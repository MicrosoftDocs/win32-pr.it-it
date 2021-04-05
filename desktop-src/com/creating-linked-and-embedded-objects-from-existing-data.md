---
title: Creazione di oggetti collegati e incorporati da dati esistenti
description: Creazione di oggetti collegati e incorporati da dati esistenti
ms.assetid: 76848b7e-6068-4bac-9793-304f813096f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f60064516a4312a9de3ce511e00e49ce7276f0b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714266"
---
# <a name="creating-linked-and-embedded-objects-from-existing-data"></a><span data-ttu-id="b9af2-103">Creazione di oggetti collegati e incorporati da dati esistenti</span><span class="sxs-lookup"><span data-stu-id="b9af2-103">Creating Linked and Embedded Objects from Existing Data</span></span>

<span data-ttu-id="b9af2-104">Un utente in genere assembla un documento composto usando gli Appunti o il trascinamento della selezione per copiare un oggetto dati dalla relativa applicazione server all'applicazione contenitore dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b9af2-104">A user typically assembles a compound document by using either the clipboard or drag and drop to copy a data object from its server application to the user's container application.</span></span> <span data-ttu-id="b9af2-105">Con le applicazioni che supportano OLE, l'utente può avviare il trasferimento dal server o dal contenitore.</span><span class="sxs-lookup"><span data-stu-id="b9af2-105">With applications that support OLE, the user can initiate the transfer from either the server or the container.</span></span> <span data-ttu-id="b9af2-106">Il server può, ad esempio, copiare i dati negli Appunti nell'applicazione server, quindi passare all'applicazione contenitore e scegliere Incolla oggetto speciale/incorporato o un comando di menu equivalente per creare un nuovo oggetto incorporato dai dati selezionati.</span><span class="sxs-lookup"><span data-stu-id="b9af2-106">For example, the server can copy data to the clipboard in the server application, then switch to the container application and choose Paste Special/Embedded Object or an equivalent menu command to create a new embedded object from the selected data.</span></span> <span data-ttu-id="b9af2-107">In alternativa, l'utente può trascinare i dati da un'applicazione all'altra.</span><span class="sxs-lookup"><span data-stu-id="b9af2-107">Or, the user can drag the data from one application to the other.</span></span> <span data-ttu-id="b9af2-108">Il processo è simile per la creazione di un oggetto collegato.</span><span class="sxs-lookup"><span data-stu-id="b9af2-108">The process is similar for creating a linked object.</span></span>

> [!Note]  
> <span data-ttu-id="b9af2-109">Un'applicazione che funge sia da server OLE che da contenitore può utilizzare una selezione dei propri dati per creare un oggetto incorporato o collegato in una nuova posizione all'interno dello stesso documento.</span><span class="sxs-lookup"><span data-stu-id="b9af2-109">An application that functions as both OLE server and container can use a selection of its own data to create an embedded or linked object at a new location within the same document.</span></span>

 

<span data-ttu-id="b9af2-110">Il trasferimento dei dati tra il server OLE e le applicazioni contenitore è basato sul trasferimento dati uniforme, come descritto in [trasferimento dati](data-transfer.md).</span><span class="sxs-lookup"><span data-stu-id="b9af2-110">Data transfer between OLE server and container applications is built on uniform data transfer, as described in [Data Transfer](data-transfer.md).</span></span> <span data-ttu-id="b9af2-111">I server OLE e i gestori di oggetti implementano [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) per rendere i dati disponibili per i trasferimenti usando gli Appunti o il trascinamento della selezione.</span><span class="sxs-lookup"><span data-stu-id="b9af2-111">OLE servers and object handlers implement [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) in order to make their data available for transfers using either the clipboard or drag and drop.</span></span> <span data-ttu-id="b9af2-112">Gli oggetti OLE supportano tutti i formati degli Appunti usuali.</span><span class="sxs-lookup"><span data-stu-id="b9af2-112">OLE objects support all the usual clipboard formats.</span></span> <span data-ttu-id="b9af2-113">Sono inoltre supportati sei formati degli appunti che supportano la creazione di oggetti collegati e incorporati da un oggetto dati selezionato.</span><span class="sxs-lookup"><span data-stu-id="b9af2-113">In addition, they support six clipboard formats that support the creation of linked and embedded objects from a selected data object.</span></span>

<span data-ttu-id="b9af2-114">I formati degli Appunti OLE descrivono gli oggetti dati che, dopo essere stati eliminati o incollati nei contenitori OLE, devono diventare oggetti di documenti compositi incorporati o collegati.</span><span class="sxs-lookup"><span data-stu-id="b9af2-114">OLE clipboard formats describe data objects that, upon being dropped or pasted in OLE containers, are to become embedded or linked compound-document objects.</span></span> <span data-ttu-id="b9af2-115">L'oggetto dati presenta questi formati alle applicazioni contenitore in ordine di fedeltà come descrizione dei dati.</span><span class="sxs-lookup"><span data-stu-id="b9af2-115">The data object presents these formats to container applications in order of their fidelity as descriptions of the data.</span></span> <span data-ttu-id="b9af2-116">In altre parole, l'oggetto presenta innanzitutto il formato che meglio lo rappresenta, seguito dal formato migliore successivo e così via.</span><span class="sxs-lookup"><span data-stu-id="b9af2-116">In other words, the object presents first the format that best represents it, followed by the next best format, and so on.</span></span> <span data-ttu-id="b9af2-117">Questo ordinamento intenzionale invita un'applicazione contenitore a usare il formato migliore possibile.</span><span class="sxs-lookup"><span data-stu-id="b9af2-117">This intentional ordering encourages a container application to use the best possible format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9af2-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b9af2-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9af2-119">Documenti composti</span><span class="sxs-lookup"><span data-stu-id="b9af2-119">Compound Documents</span></span>](compound-documents.md)
</dt> <dt>

[<span data-ttu-id="b9af2-120">Trasferimento dati</span><span class="sxs-lookup"><span data-stu-id="b9af2-120">Data Transfer</span></span>](data-transfer.md)
</dt> </dl>

 

 





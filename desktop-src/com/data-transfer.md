---
title: Trasferimento dati
description: Trasferimento dati
ms.assetid: 26b16438-f940-4086-869e-74021ed00b1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37dee268b99f205e0093288f6980c8425220a45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516066"
---
# <a name="data-transfer"></a><span data-ttu-id="f1728-103">Trasferimento dati</span><span class="sxs-lookup"><span data-stu-id="f1728-103">Data Transfer</span></span>

<span data-ttu-id="f1728-104">Il Component Object Model (COM) fornisce un meccanismo standard per il trasferimento dei dati tra le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f1728-104">The Component Object Model (COM) provides a standard mechanism for transferring data between applications.</span></span> <span data-ttu-id="f1728-105">Questo meccanismo è l' *oggetto dati*, che è semplicemente un oggetto com che implementa l'interfaccia [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) .</span><span class="sxs-lookup"><span data-stu-id="f1728-105">This mechanism is the *data object*, which is simply any COM object that implements the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) interface.</span></span> <span data-ttu-id="f1728-106">Alcuni oggetti dati, ad esempio una porzione di testo copiata negli Appunti, hanno **IDataObject** come unica interfaccia.</span><span class="sxs-lookup"><span data-stu-id="f1728-106">Some data objects, such as a piece of text copied to the clipboard, have **IDataObject** as their sole interface.</span></span> <span data-ttu-id="f1728-107">Altri, ad esempio oggetti documento composito, espongono diverse interfacce, di cui **IDataObject** è semplicemente uno.</span><span class="sxs-lookup"><span data-stu-id="f1728-107">Others, such as compound document objects, expose several interfaces, of which **IDataObject** is simply one.</span></span> <span data-ttu-id="f1728-108">Gli oggetti dati sono fondamentali per l'utilizzo di documenti composti, sebbene abbiano anche un'applicazione diffusa al di fuori della tecnologia OLE.</span><span class="sxs-lookup"><span data-stu-id="f1728-108">Data objects are fundamental to the working of compound documents, although they also have widespread application outside that OLE technology.</span></span>

<span data-ttu-id="f1728-109">Scambiando i puntatori a un oggetto dati, i provider e i consumer di dati possono gestire i trasferimenti di dati in modo uniforme, indipendentemente dal formato dei dati, dal tipo di supporto usato per trasferire i dati o dal dispositivo di destinazione in cui deve essere eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="f1728-109">By exchanging pointers to a data object, providers and consumers of data can manage data transfers in a uniform manner, regardless of the format of the data, the type of medium used to transfer the data, or the target device on which it is to be rendered.</span></span> <span data-ttu-id="f1728-110">È possibile includere il supporto nell'applicazione per i trasferimenti di base degli Appunti, i trasferimenti con trascinamento della selezione e i trasferimenti di documenti compositi OLE con una singola implementazione di [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject).</span><span class="sxs-lookup"><span data-stu-id="f1728-110">You can include support in your application for basic clipboard transfers, drag and drop transfers, and OLE compound document transfers with a single implementation of [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject).</span></span> <span data-ttu-id="f1728-111">Una volta eseguita questa operazione, la quantità di codice necessaria per gestire la semantica speciale di ogni protocollo è minima.</span><span class="sxs-lookup"><span data-stu-id="f1728-111">Having done that, the amount of code required to accommodate the special semantics of each protocol is minimal.</span></span>

<span data-ttu-id="f1728-112">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="f1728-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="f1728-113">Interfacce di Trasferimento dati</span><span class="sxs-lookup"><span data-stu-id="f1728-113">Data Transfer Interfaces</span></span>](data-transfer-interfaces.md)
-   [<span data-ttu-id="f1728-114">Formati di dati e supporti di trasferimento</span><span class="sxs-lookup"><span data-stu-id="f1728-114">Data Formats and Transfer Media</span></span>](data-formats-and-transfer-media.md)
-   [<span data-ttu-id="f1728-115">Trascinamento della selezione</span><span class="sxs-lookup"><span data-stu-id="f1728-115">Drag and Drop</span></span>](drag-and-drop.md)

## <a name="related-topics"></a><span data-ttu-id="f1728-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f1728-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1728-117">Documenti composti</span><span class="sxs-lookup"><span data-stu-id="f1728-117">Compound Documents</span></span>](compound-documents.md)
</dt> </dl>

 

 





---
description: L'API del documento XPS implementa il modello a oggetti XPS e consente agli sviluppatori di creare un modello a oggetti XPS, modificare il contenuto del documento XPS nei programmi Windows nativi \\ \\ e salvare i dati XPS om in un file o in un flusso come documento XPS.
ms.assetid: dbb48dae-1ee6-4a8b-9184-8b796755087e
title: Informazioni sull'API documento XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e24a93061b7f09697a987aa83be121dac42703c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316428"
---
# <a name="about-xps-document-api"></a><span data-ttu-id="f60bc-103">Informazioni sull'API documento XPS</span><span class="sxs-lookup"><span data-stu-id="f60bc-103">About XPS Document API</span></span>

<span data-ttu-id="f60bc-104">L' [API del documento XPS](documents-xps.md) implementa il modello a oggetti XPS e consente agli sviluppatori di creare un modello a oggetti XPS, modificare il contenuto del documento XPS nei programmi Windows nativi \\ \\ e salvare i dati XPS om in un file o in un flusso come documento XPS.</span><span class="sxs-lookup"><span data-stu-id="f60bc-104">The [XPS Document API](documents-xps.md) implements the XPS object model and enables developers to create an XPS OM, manipulate XPS document content in native Windows \\\\ programs, and save the XPS OM to a file or stream as an XPS document.</span></span> <span data-ttu-id="f60bc-105">Gli sviluppatori dei moduli della pipeline filtro XPSDrv possono inoltre utilizzare l'API documento XPS per modificare il contenuto del documento XPS in un filtro di driver della stampante XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="f60bc-105">Developers of XPSDrv filter pipeline modules can also use the XPS Document API to manipulate XPS document content in an XPSDrv printer driver filter.</span></span>

## <a name="xps-document-api-overview"></a><span data-ttu-id="f60bc-106">Panoramica dell'API documento XPS</span><span class="sxs-lookup"><span data-stu-id="f60bc-106">XPS Document API Overview</span></span>

<span data-ttu-id="f60bc-107">Il modello a oggetti XPS è il modello informativo di un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="f60bc-107">The XPS object model is the information model of an XPS document.</span></span> <span data-ttu-id="f60bc-108">Il modello informativo del documento XPS è separato dal modello di markup utilizzato nelle parti del documento.</span><span class="sxs-lookup"><span data-stu-id="f60bc-108">The information model of the XPS document is separate from the markup model that is used inside the document parts.</span></span> <span data-ttu-id="f60bc-109">Nel modello a oggetti XPS viene descritta l'organizzazione dei componenti interni che costituiscono un documento XPS e nel modello di markup viene descritto il contenuto di tali componenti.</span><span class="sxs-lookup"><span data-stu-id="f60bc-109">The XPS object model describes the organization of the internal components that make up an XPS document, and the markup model describes the contents of those components.</span></span>

<span data-ttu-id="f60bc-110">In un programma, viene creata un'istanza del modello a oggetti XPS come OM XPS.</span><span class="sxs-lookup"><span data-stu-id="f60bc-110">In a program, the XPS object model is instantiated as an XPS OM.</span></span> <span data-ttu-id="f60bc-111">XPS OM è essenzialmente una versione in memoria del contenuto di un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="f60bc-111">The XPS OM is essentially an in-memory version of an XPS document's contents.</span></span> <span data-ttu-id="f60bc-112">Analogamente, in un'organizzazione logica a un documento XPS, un OM XPS non viene considerato un documento XPS fino a quando non viene serializzato in un file o in un flusso.</span><span class="sxs-lookup"><span data-stu-id="f60bc-112">While similar in logical organization to an XPS document, an XPS OM is not considered an XPS document until it has been serialized to a file or a stream.</span></span>

<span data-ttu-id="f60bc-113">La struttura esatta del markup non è disponibile per XPS OM quando un documento XPS viene deserializzato dal markup a un OM XPS.</span><span class="sxs-lookup"><span data-stu-id="f60bc-113">The exact structure of the markup is not available to the XPS OM when an XPS document is deserialized from markup to an XPS OM.</span></span> <span data-ttu-id="f60bc-114">Ad esempio, se la proprietà è stata rappresentata come elemento o attributo nel markup, il valore della proprietà di un oggetto documento viene presentato da XPS OM esattamente allo stesso modo.</span><span class="sxs-lookup"><span data-stu-id="f60bc-114">For example, whether the property was represented as an element or an attribute in the markup, the property value of a document object is presented by the XPS OM in exactly the same way.</span></span>

<span data-ttu-id="f60bc-115">L' [API documento XPS](documents-xps.md) può essere divisa nelle categorie seguenti:</span><span class="sxs-lookup"><span data-stu-id="f60bc-115">The [XPS Document API](documents-xps.md) can be divided into the following categories:</span></span>

-   [<span data-ttu-id="f60bc-116">Interfacce trunk XPS OM</span><span class="sxs-lookup"><span data-stu-id="f60bc-116">XPS OM Trunk Interfaces</span></span>](xps-om-trunk-interfaces.md)

    <span data-ttu-id="f60bc-117">Le interfacce trunk consentono di accedere ai componenti di primo livello della struttura del documento XPS.</span><span class="sxs-lookup"><span data-stu-id="f60bc-117">The trunk interfaces provide access to the top-level components of the XPS document structure.</span></span> <span data-ttu-id="f60bc-118">Queste interfacce forniscono inoltre i mezzi per serializzare un oggetto XPS OM e deserializzare un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="f60bc-118">These interfaces also provide the means to serialize an XPS OM and deserialize an XPS document.</span></span>

-   [<span data-ttu-id="f60bc-119">Interfacce di pagine XPS OM</span><span class="sxs-lookup"><span data-stu-id="f60bc-119">XPS OM Page Interfaces</span></span>](xps-object-model-page-interfaces.md)

    <span data-ttu-id="f60bc-120">Le interfacce di pagina consentono di accedere al contenuto di una pagina in un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="f60bc-120">The page interfaces provide access to the contents of a page in an XPS document.</span></span> <span data-ttu-id="f60bc-121">Le interfacce che descrivono il contenuto della pagina sono incluse anche con le interfacce di pagina.</span><span class="sxs-lookup"><span data-stu-id="f60bc-121">The interfaces that describe the content of the page are also included with the page interfaces.</span></span>

-   [<span data-ttu-id="f60bc-122">Firme digitali XPS OM</span><span class="sxs-lookup"><span data-stu-id="f60bc-122">XPS OM Digital Signatures</span></span>](using-the-xps-digital-signatures.md)

    <span data-ttu-id="f60bc-123">XPS OM supporta le firme digitali.</span><span class="sxs-lookup"><span data-stu-id="f60bc-123">The XPS OM supports digital signatures.</span></span> <span data-ttu-id="f60bc-124">Tuttavia, è possibile accedere direttamente alle firme digitali in un documento XPS senza creare un OM XPS.</span><span class="sxs-lookup"><span data-stu-id="f60bc-124">However, you can access digital signatures in an XPS document directly without creating an XPS OM.</span></span> <span data-ttu-id="f60bc-125">Per ulteriori informazioni su come accedere alle firme digitali XPS senza XPS OM, vedere [XPS Digital Signature API](xps-digital-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="f60bc-125">For more information about how to access XPS digital signatures without an XPS OM, see [XPS Digital Signature API](xps-digital-signatures.md).</span></span>

-   [<span data-ttu-id="f60bc-126">Interfacce del ticket di stampa XPS OM</span><span class="sxs-lookup"><span data-stu-id="f60bc-126">XPS OM Print Ticket Interfaces</span></span>](xps-object-model-print-ticket-interfaces.md)

    <span data-ttu-id="f60bc-127">I documenti XPS supportano i ticket di stampa a livello di pacchetto (processo), documento e pagina.</span><span class="sxs-lookup"><span data-stu-id="f60bc-127">XPS documents support print tickets at the package (job), document, and page level.</span></span> <span data-ttu-id="f60bc-128">I ticket di stampa contengono informazioni su come formattare il contenuto del documento per la stampa o la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="f60bc-128">Print tickets contain information about how to format document content for printing or viewing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f60bc-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f60bc-129">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f60bc-130">**Argomenti della sezione**</span><span class="sxs-lookup"><span data-stu-id="f60bc-130">**In This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="f60bc-131">Interfacce trunk XPS OM</span><span class="sxs-lookup"><span data-stu-id="f60bc-131">XPS OM Trunk Interfaces</span></span>](xps-om-trunk-interfaces.md)
</dt> <dt>

[<span data-ttu-id="f60bc-132">Interfacce di pagine XPS OM</span><span class="sxs-lookup"><span data-stu-id="f60bc-132">XPS OM Page Interfaces</span></span>](xps-object-model-page-interfaces.md)
</dt> <dt>

[<span data-ttu-id="f60bc-133">Firme digitali XPS OM</span><span class="sxs-lookup"><span data-stu-id="f60bc-133">XPS OM Digital Signatures</span></span>](using-the-xps-digital-signatures.md)
</dt> <dt>

[<span data-ttu-id="f60bc-134">Interfacce del ticket di stampa XPS OM</span><span class="sxs-lookup"><span data-stu-id="f60bc-134">XPS OM Print Ticket Interfaces</span></span>](xps-object-model-print-ticket-interfaces.md)
</dt> <dt>

<span data-ttu-id="f60bc-135">**Altri argomenti correlati**</span><span class="sxs-lookup"><span data-stu-id="f60bc-135">**Other Related Topics**</span></span>
</dt> <dt>

[<span data-ttu-id="f60bc-136">Inizializzare un OM XPS</span><span class="sxs-lookup"><span data-stu-id="f60bc-136">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="f60bc-137">Firme digitali XPS OM</span><span class="sxs-lookup"><span data-stu-id="f60bc-137">XPS OM Digital Signatures</span></span>](using-the-xps-digital-signatures.md)
</dt> <dt>

[<span data-ttu-id="f60bc-138">Informazioni di riferimento sulle API documento XPS</span><span class="sxs-lookup"><span data-stu-id="f60bc-138">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="f60bc-139">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="f60bc-139">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 




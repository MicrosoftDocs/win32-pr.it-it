---
description: In questo argomento viene descritta una nuova visualizzazione in Esplora risorse, denominata visualizzazione contenuto, che Visualizza il contenuto più rilevante per ogni elemento.
title: Visualizzazione contenuto per tipo di file o tipo
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E01A6726-14C4-4c00-81D4-AE1008088678
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 81982d2242a7ea466c10e7d0ee37d899eea3e687
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757361"
---
# <a name="content-view-by-file-type-or-kind"></a><span data-ttu-id="1ab81-103">Visualizzazione contenuto per tipo di file o tipo</span><span class="sxs-lookup"><span data-stu-id="1ab81-103">Content View By File Type or Kind</span></span>

<span data-ttu-id="1ab81-104">In questo argomento viene descritta una nuova visualizzazione in Esplora risorse, denominata visualizzazione contenuto, che Visualizza il contenuto più rilevante per ogni elemento.</span><span class="sxs-lookup"><span data-stu-id="1ab81-104">This topic describes a new view in Windows Explorer, called the Content view, that displays the most relevant content for each item.</span></span> <span data-ttu-id="1ab81-105">Utilizzando un set di chiavi del registro di sistema, gli elementi possono definire un elenco di proprietà e un layout utilizzati dalla Shell per la visualizzazione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="1ab81-105">Using a set of registry keys, items can define a property list and a layout that the Shell uses for Content view.</span></span> <span data-ttu-id="1ab81-106">La shell recupera le chiavi del registro di sistema usando la [matrice di associazioni](fa-perceivedtypes.md)dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="1ab81-106">The Shell retrieves the registry keys by using the item's [association array](fa-perceivedtypes.md).</span></span>

## <a name="how-does-the-content-view-work"></a><span data-ttu-id="1ab81-107">Come funziona la visualizzazione del contenuto?</span><span class="sxs-lookup"><span data-stu-id="1ab81-107">How Does the Content View Work?</span></span>

<span data-ttu-id="1ab81-108">In Windows 7 e versioni successive, la visualizzazione contenuto usa una logica di ridimensionamento che rilascia le proprietà quando la dimensione della finestra diminuisce, per garantire che le proprietà più importanti abbiano ancora spazio per essere leggibili in modo chiaro.</span><span class="sxs-lookup"><span data-stu-id="1ab81-108">In Windows 7 and later, the Content view uses a resizing logic that drops properties when the window size decreases, to ensure that the most critical properties still have room to be clearly readable.</span></span> <span data-ttu-id="1ab81-109">Lo screenshot seguente illustra la visualizzazione contenuto dei risultati della ricerca che contengono musica, immagini e documenti.</span><span class="sxs-lookup"><span data-stu-id="1ab81-109">The following screen shot illustrates the Content view of search results containing music, pictures, and documents.</span></span>

![Visualizzazione contenuto dei risultati della ricerca che contengono musica, immagini e documenti](images/content-view/contentviewsearchresults.png)

<span data-ttu-id="1ab81-111">Alcune origini dati della Shell utilizzano la visualizzazione contenuto per impostazione predefinita, ma gli utenti possono selezionare la visualizzazione contenuto facendo clic sul pulsante **Visualizza controllo** in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="1ab81-111">Some Shell data sources use Content view by default, but users can select the Content view by clicking the **View Control** button in Windows Explorer.</span></span> <span data-ttu-id="1ab81-112">Un'origine dati della shell estende lo spazio dei nomi della shell ed espone gli elementi in un archivio dati.</span><span class="sxs-lookup"><span data-stu-id="1ab81-112">A Shell data source extends the Shell namespace and exposes items in a data store.</span></span> <span data-ttu-id="1ab81-113">Gli elementi in un archivio dati possono essere indicizzati dal sistema di ricerca Windows utilizzando un gestore di protocollo.</span><span class="sxs-lookup"><span data-stu-id="1ab81-113">The items in a data store can be indexed by the Windows Search system using a protocol handler.</span></span>

## <a name="how-to-implement-the-content-view"></a><span data-ttu-id="1ab81-114">Come implementare la visualizzazione contenuto</span><span class="sxs-lookup"><span data-stu-id="1ab81-114">How to Implement the Content View</span></span>

<span data-ttu-id="1ab81-115">Quando si registra un nuovo [tipo di file](fa-file-types.md) o [gestore di protocollo](../search/-search-3x-wds-extidx-prot-implementing.md), è possibile sfruttare la visualizzazione contenuto utilizzando uno di due approcci diversi.</span><span class="sxs-lookup"><span data-stu-id="1ab81-115">When registering a new [file type](fa-file-types.md) or [protocol handler](../search/-search-3x-wds-extidx-prot-implementing.md), you can take advantage of the Content view by using either of two different approaches.</span></span> <span data-ttu-id="1ab81-116">È possibile usare un set di proprietà e un modello di layout esistente oppure è possibile creare una combinazione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="1ab81-116">You can use an existing set of properties and layout pattern, or you can create your own combination.</span></span>

<span data-ttu-id="1ab81-117">È possibile utilizzare una voce del registro di sistema per associare il tipo di file o l'elemento a un [tipo](../properties/building-property-handlers-user-friendly-kind-names.md)predefinito, ovvero una proprietà che è possibile considerare come una categoria di contenuto.</span><span class="sxs-lookup"><span data-stu-id="1ab81-117">You can use a registry entry to associate your file type or item with a predefined [Kind](../properties/building-property-handlers-user-friendly-kind-names.md), which is a property that you can think of as a content category.</span></span> <span data-ttu-id="1ab81-118">Associando il tipo di file o l'elemento con determinati tipi, si ereditano automaticamente i modelli di layout di visualizzazione del contenuto e gli elenchi di proprietà di tale tipo.</span><span class="sxs-lookup"><span data-stu-id="1ab81-118">By associating your file type or item with certain of these Kinds, you automatically inherit that Kind's Content view layout patterns and property lists.</span></span> <span data-ttu-id="1ab81-119">Windows definisce i modelli di layout di visualizzazione del contenuto e gli elenchi di proprietà per i tipi seguenti: Documents, email, Folder, Music, Picture e Generic.</span><span class="sxs-lookup"><span data-stu-id="1ab81-119">Windows defines Content view layout patterns and property lists for the following Kinds: documents, email, folder, music, picture, and generic.</span></span> <span data-ttu-id="1ab81-120">Questo tipo di associazione è consigliato.</span><span class="sxs-lookup"><span data-stu-id="1ab81-120">This type of association is encouraged.</span></span> <span data-ttu-id="1ab81-121">Consente di fornire l'esperienza coerente che un utente aspetta per gli elementi simili.</span><span class="sxs-lookup"><span data-stu-id="1ab81-121">It lets you provide the consistent experience that a user expects for similar items.</span></span>

<span data-ttu-id="1ab81-122">Per altre informazioni, vedere [tipi di file](fa-file-types.md) e [nomi](../properties/building-property-handlers-user-friendly-kind-names.md) di tipi e [come registrare un set di visualizzazioni di contenuto univoco di proprietà e pattern di layout per il tipo di file o l'elemento](register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item.md).</span><span class="sxs-lookup"><span data-stu-id="1ab81-122">For more information, see [File Types](fa-file-types.md) and [Kind Names](../properties/building-property-handlers-user-friendly-kind-names.md) and [How To Register a Unique Content View Set of Properties and Layout Pattern for the File Type or Item](register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1ab81-123">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="1ab81-123">Additional Resources</span></span>

-   <span data-ttu-id="1ab81-124">Per la documentazione di riferimento della proprietà, vedere [System. Kind](../properties/props-system-kind.md)e [System. KindText](../properties/props-system-kindtext.md).</span><span class="sxs-lookup"><span data-stu-id="1ab81-124">For property reference documentation, see [System.Kind](../properties/props-system-kind.md), and [System.KindText](../properties/props-system-kindtext.md).</span></span>
-   <span data-ttu-id="1ab81-125">Per la documentazione di riferimento di proprietà, vedere [System. propt. ContentViewModeForBrowse](../properties/props-system-proplist-contentviewmodeforbrowse.md)e [System. propt. ContentViewModeForSearch](../properties/props-system-proplist-contentviewmodeforsearch.md).</span><span class="sxs-lookup"><span data-stu-id="1ab81-125">For PropList reference documentation, see [System.PropList.ContentViewModeForBrowse](../properties/props-system-proplist-contentviewmodeforbrowse.md), and [System.PropList.ContentViewModeForSearch](../properties/props-system-proplist-contentviewmodeforsearch.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ab81-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1ab81-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ab81-127">Registrazione dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="1ab81-127">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="1ab81-128">Tipi di file</span><span class="sxs-lookup"><span data-stu-id="1ab81-128">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="1ab81-129">Funzionamento delle associazioni di file</span><span class="sxs-lookup"><span data-stu-id="1ab81-129">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="1ab81-130">Tipo di file Verifier</span><span class="sxs-lookup"><span data-stu-id="1ab81-130">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="1ab81-131">Gestori di tipi di file</span><span class="sxs-lookup"><span data-stu-id="1ab81-131">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="1ab81-132">Identificatori a livello di codice</span><span class="sxs-lookup"><span data-stu-id="1ab81-132">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="1ab81-133">Tipi percepiti</span><span class="sxs-lookup"><span data-stu-id="1ab81-133">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="1ab81-134">Matrici di associazione</span><span class="sxs-lookup"><span data-stu-id="1ab81-134">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 

---
title: Trascinamento e rilascio
description: Il trascinamento della selezione si riferisce ai trasferimenti di dati in cui un mouse o un altro dispositivo di puntamento viene usato per specificare sia l'origine dati che la relativa destinazione.
ms.assetid: bba0ddf8-fcf9-4827-bf85-7ac597d33b4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dc4b425637432024d097acb8afdc5e169467c6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298347"
---
# <a name="drag-and-drop"></a><span data-ttu-id="06062-103">Trascinamento e rilascio</span><span class="sxs-lookup"><span data-stu-id="06062-103">Drag and Drop</span></span>

<span data-ttu-id="06062-104">Il *trascinamento della selezione* si riferisce ai trasferimenti di dati in cui un mouse o un altro dispositivo di puntamento viene usato per specificare sia l'origine dati che la relativa destinazione.</span><span class="sxs-lookup"><span data-stu-id="06062-104">*Drag and drop* refers to data transfers in which a mouse or other pointing device is used to specify both the data source and its destination.</span></span> <span data-ttu-id="06062-105">In una tipica operazione di trascinamento della selezione, un utente seleziona l'oggetto da trasferire spostando il puntatore del mouse su di esso e tenendo premuto il pulsante sinistro o un altro pulsante designato a questo scopo.</span><span class="sxs-lookup"><span data-stu-id="06062-105">In a typical drag and drop operation, a user selects the object to be transferred by moving the mouse pointer to it and holding down either the left button or some other button designated for this purpose.</span></span> <span data-ttu-id="06062-106">Continuando a tenere premuto il pulsante, l'utente avvia il trasferimento trascinando l'oggetto nella relativa destinazione, che può essere qualsiasi contenitore OLE.</span><span class="sxs-lookup"><span data-stu-id="06062-106">While continuing to hold down the button, the user initiates the transfer by dragging the object to its destination, which can be any OLE container.</span></span> <span data-ttu-id="06062-107">Il trascinamento della selezione fornisce esattamente la stessa funzionalità degli Appunti OLE copia e incolla, ma aggiunge commenti e suggerimenti visivi ed elimina la necessità di menu.</span><span class="sxs-lookup"><span data-stu-id="06062-107">Drag and drop provides exactly the same functionality as the OLE clipboard copy and paste but adds visual feedback and eliminates the need for menus.</span></span> <span data-ttu-id="06062-108">Infatti, se un'applicazione supporta la copia e incolla degli Appunti, per supportare il trascinamento della selezione è necessario molto altro.</span><span class="sxs-lookup"><span data-stu-id="06062-108">In fact, if an application supports clipboard copy and paste, little extra is needed to support drag and drop.</span></span>

<span data-ttu-id="06062-109">Durante un'operazione di trascinamento e rilascio OLE vengono usate le tre parti separate di codice seguenti.</span><span class="sxs-lookup"><span data-stu-id="06062-109">During an OLE drag and drop operation, the following three separate pieces of code are used.</span></span>



| <span data-ttu-id="06062-110">Origine codice di trascinamento della selezione</span><span class="sxs-lookup"><span data-stu-id="06062-110">Drag-and-drop code source</span></span>                               | <span data-ttu-id="06062-111">Implementazione e utilizzo</span><span class="sxs-lookup"><span data-stu-id="06062-111">Implementation and use</span></span>                                                                                                                                                                      |
|---------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06062-112">Interfaccia [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)</span><span class="sxs-lookup"><span data-stu-id="06062-112">[**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) interface</span></span><br/> | <span data-ttu-id="06062-113">Implementata dall'oggetto che contiene i dati trascinati, a cui viene fatto riferimento come *origine del trascinamento*.</span><span class="sxs-lookup"><span data-stu-id="06062-113">Implemented by the object containing the dragged data, referred to as the *drag source*.</span></span><br/>                                                                                         |
| <span data-ttu-id="06062-114">[**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="06062-114">[**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) interface</span></span><br/> | <span data-ttu-id="06062-115">Implementata dall'oggetto che ha lo scopo di accettare l'eliminazione, denominata destinazione di *rilascio*.</span><span class="sxs-lookup"><span data-stu-id="06062-115">Implemented by the object that is intended to accept the drop, referred to as the *drop target*.</span></span><br/>                                                                                 |
| <span data-ttu-id="06062-116">[**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) (funzione)</span><span class="sxs-lookup"><span data-stu-id="06062-116">[**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) function</span></span><br/>    | <span data-ttu-id="06062-117">Implementato da OLE e utilizzato per avviare un'operazione di trascinamento della selezione.</span><span class="sxs-lookup"><span data-stu-id="06062-117">Implemented by OLE and used to initiate a drag and drop operation.</span></span> <span data-ttu-id="06062-118">Dopo che l'operazione è in corso, facilita la comunicazione tra l'origine di trascinamento e l'obiettivo di rilascio.</span><span class="sxs-lookup"><span data-stu-id="06062-118">After the operation is in progress, it facilitates communication between the drag source and the drop target.</span></span><br/> |



 

<span data-ttu-id="06062-119">Le interfacce [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) e [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) possono essere implementate in un contenitore o in un'applicazione a oggetti.</span><span class="sxs-lookup"><span data-stu-id="06062-119">The [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) and [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) interfaces can be implemented in either a container or in an object application.</span></span> <span data-ttu-id="06062-120">Il ruolo di origine di trascinamento o destinazione di rilascio non è limitato a un tipo di applicazione OLE.</span><span class="sxs-lookup"><span data-stu-id="06062-120">The role of drag source or drop target is not limited to any one type of OLE application.</span></span>

<span data-ttu-id="06062-121">La funzione OLE [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) implementa un ciclo che tiene traccia del movimento del mouse e della tastiera fino al momento in cui viene annullato o si verifica un trascinamento.</span><span class="sxs-lookup"><span data-stu-id="06062-121">The OLE function [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) implements a loop that tracks mouse and keyboard movement until such time as the drag is canceled or a drop occurs.</span></span> <span data-ttu-id="06062-122">**DoDragDrop** è la funzione chiave nel processo di trascinamento della selezione, che facilita la comunicazione tra l'origine di trascinamento e l'obiettivo di rilascio.</span><span class="sxs-lookup"><span data-stu-id="06062-122">**DoDragDrop** is the key function in the drag and drop process, facilitating communication between the drag source and drop target.</span></span>

<span data-ttu-id="06062-123">Durante un'operazione di trascinamento della selezione, è possibile visualizzare tre tipi di commenti e suggerimenti all'utente.</span><span class="sxs-lookup"><span data-stu-id="06062-123">During a drag and drop operation, three types of feedback can be displayed to the user.</span></span>



| <span data-ttu-id="06062-124">Tipo di feedback</span><span class="sxs-lookup"><span data-stu-id="06062-124">Type of feedback</span></span>            | <span data-ttu-id="06062-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06062-125">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06062-126">Feedback sull'origine</span><span class="sxs-lookup"><span data-stu-id="06062-126">Source feedback</span></span><br/>  | <span data-ttu-id="06062-127">Fornito dall'origine di trascinamento, il feedback sull'origine indica che i dati vengono trascinati e non cambiano nel corso del trascinamento.</span><span class="sxs-lookup"><span data-stu-id="06062-127">Provided by the drag source, the source feedback indicates the data is being dragged and does not change during the course of the drag.</span></span> <span data-ttu-id="06062-128">In genere, i dati vengono evidenziati per segnalare che è stata selezionata.</span><span class="sxs-lookup"><span data-stu-id="06062-128">Typically, the data is highlighted to signal it has been selected.</span></span><br/>                                                                                                                                            |
| <span data-ttu-id="06062-129">Feedback del puntatore</span><span class="sxs-lookup"><span data-stu-id="06062-129">Pointer feedback</span></span><br/> | <span data-ttu-id="06062-130">Fornito dall'origine di trascinamento, il feedback del puntatore indica cosa accade se il mouse viene rilasciato in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="06062-130">Provided by the drag source, the pointer feedback indicates what happens if the mouse is released at any given moment.</span></span> <span data-ttu-id="06062-131">Il feedback del puntatore cambia continuamente quando l'utente sposta il mouse e/o preme un tasto di modifica.</span><span class="sxs-lookup"><span data-stu-id="06062-131">Pointer feedback changes continually as the user moves the mouse and/or presses a modifier key.</span></span> <span data-ttu-id="06062-132">Se, ad esempio, il puntatore viene spostato in una finestra che non può accettare un rilascio, il puntatore viene modificato nel simbolo "non consentito".</span><span class="sxs-lookup"><span data-stu-id="06062-132">For example, if the pointer is moved into a window that cannot accept a drop, the pointer changes to the "not allowed" symbol.</span></span><br/> |
| <span data-ttu-id="06062-133">Feedback di destinazione</span><span class="sxs-lookup"><span data-stu-id="06062-133">Target feedback</span></span><br/>  | <span data-ttu-id="06062-134">Fornito dalla destinazione di rilascio, il feedback di destinazione indica dove deve essere eseguito il rilascio.</span><span class="sxs-lookup"><span data-stu-id="06062-134">Provided by the drop target, target feedback indicates where the drop is to occur.</span></span><br/>                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="06062-135">Per altre informazioni, vedere [trascinare le responsabilità dell'origine](drag-source-responsibilities.md).</span><span class="sxs-lookup"><span data-stu-id="06062-135">For more information, see [Drag Source Responsibilities](drag-source-responsibilities.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="06062-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="06062-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06062-137">Trasferimento dati</span><span class="sxs-lookup"><span data-stu-id="06062-137">Data Transfer</span></span>](data-transfer.md)
</dt> </dl>

 

 






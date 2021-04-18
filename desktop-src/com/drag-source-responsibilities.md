---
title: Trascinare le responsabilità dell'origine
description: Trascinare le responsabilità dell'origine
ms.assetid: bafef0c1-f78e-424a-9ed0-07764a60b22d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45ce91a795815148f442c19530a552cf7c843332
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300506"
---
# <a name="drag-source-responsibilities"></a><span data-ttu-id="d5369-103">Trascinare le responsabilità dell'origine</span><span class="sxs-lookup"><span data-stu-id="d5369-103">Drag Source Responsibilities</span></span>

<span data-ttu-id="d5369-104">L'origine di trascinamento è responsabile delle attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="d5369-104">The drag source is responsible for the following tasks:</span></span>

-   <span data-ttu-id="d5369-105">Fornire un oggetto di trasferimento dei dati per l'obiettivo di rilascio che espone le interfacce [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) e [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) .</span><span class="sxs-lookup"><span data-stu-id="d5369-105">Providing a data-transfer object for the drop target that exposes the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) and [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) interfaces.</span></span>
-   <span data-ttu-id="d5369-106">Generazione del puntatore e feedback sull'origine.</span><span class="sxs-lookup"><span data-stu-id="d5369-106">Generating pointer and source feedback.</span></span>
-   <span data-ttu-id="d5369-107">Determinare quando l'operazione di trascinamento è stata annullata o si è verificata un'operazione di rilascio.</span><span class="sxs-lookup"><span data-stu-id="d5369-107">Determining when the drag operation has been canceled or a drop operation has occurred.</span></span>
-   <span data-ttu-id="d5369-108">Esecuzione di qualsiasi azione sui dati originali causati dall'operazione DROP, ad esempio l'eliminazione dei dati o la creazione di un collegamento.</span><span class="sxs-lookup"><span data-stu-id="d5369-108">Performing any action on the original data caused by the drop operation, such as deleting the data or creating a link to it.</span></span>

<span data-ttu-id="d5369-109">L'attività principale consiste nella creazione di un oggetto di trasferimento dei dati che espone le interfacce [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) e [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) .</span><span class="sxs-lookup"><span data-stu-id="d5369-109">The main task is creating a data-transfer object that exposes the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) and [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) interfaces.</span></span> <span data-ttu-id="d5369-110">È possibile che l'origine di trascinamento non includa una copia dei dati selezionati.</span><span class="sxs-lookup"><span data-stu-id="d5369-110">The drag source might or might not include a copy of the selected data.</span></span> <span data-ttu-id="d5369-111">Questa operazione non è obbligatoria, ma consente di proteggersi da modifiche accidentali e consente al codice operativo degli Appunti di essere identico al codice di trascinamento della selezione.</span><span class="sxs-lookup"><span data-stu-id="d5369-111">Including it is not mandatory, but doing so helps protect against inadvertent changes and allows the Clipboard operations code to be identical to the drag and drop code.</span></span>

<span data-ttu-id="d5369-112">Mentre è in corso un'operazione di trascinamento, l'origine di trascinamento è responsabile dell'impostazione del puntatore del mouse e, se necessario, per fornire commenti e suggerimenti sull'origine aggiuntivi all'utente.</span><span class="sxs-lookup"><span data-stu-id="d5369-112">While a drag operation is in progress, the drag source is responsible for setting the mouse pointer and, if appropriate, for providing additional source feedback to the user.</span></span> <span data-ttu-id="d5369-113">L'origine di trascinamento non può fornire commenti e suggerimenti per tenere traccia della posizione del mouse, ad eccezione del fatto che imposta effettivamente il puntatore reale (vedere la funzione [**secursor**](/windows/win32/api/winuser/nf-winuser-setcursor) ).</span><span class="sxs-lookup"><span data-stu-id="d5369-113">The drag source cannot provide any feedback that tracks the mouse position other than by actually setting the real pointer (see the [**SetCursor**](/windows/win32/api/winuser/nf-winuser-setcursor) function).</span></span> <span data-ttu-id="d5369-114">Questa regola deve essere applicata per evitare conflitti con il feedback fornito dall'obiettivo di rilascio.</span><span class="sxs-lookup"><span data-stu-id="d5369-114">This rule must be enforced to avoid conflicts with the feedback provided by the drop target.</span></span> <span data-ttu-id="d5369-115">Un'origine di trascinamento può anche essere un obiettivo di rilascio.</span><span class="sxs-lookup"><span data-stu-id="d5369-115">(A drag source can also be a drop target.</span></span> <span data-ttu-id="d5369-116">Quando si rilasciano i dati, l'origine/destinazione può, ovviamente, fornire il feedback di destinazione per tenere traccia della posizione del mouse.</span><span class="sxs-lookup"><span data-stu-id="d5369-116">When dropping on itself, the source/target can, of course, provide target feedback to track the mouse position.</span></span> <span data-ttu-id="d5369-117">In questo caso, tuttavia, si tratta dell'obiettivo di rilascio che tiene traccia del mouse, non dell'origine. In base ai commenti e suggerimenti offerti dall'obiettivo di rilascio, l'origine imposta un puntatore appropriato.</span><span class="sxs-lookup"><span data-stu-id="d5369-117">In this case, however, it is the drop target tracking the mouse, not the source.) Based on the feedback offered by the drop target, the source sets an appropriate pointer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5369-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d5369-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5369-119">Trascinamento della selezione</span><span class="sxs-lookup"><span data-stu-id="d5369-119">Drag and Drop</span></span>](drag-and-drop.md)
</dt> </dl>

 

 
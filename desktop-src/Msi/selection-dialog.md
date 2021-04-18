---
description: Questa finestra di dialogo modale consente agli utenti di selezionare determinati elementi.
ms.assetid: 76e0f369-839e-4dc0-bb42-c48dbf1511f3
title: Finestra di dialogo di selezione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d5a6b8700bbbdefe2bd1b2270797b34b0cebfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319433"
---
# <a name="selection-dialog"></a><span data-ttu-id="8572d-103">Finestra di dialogo di selezione</span><span class="sxs-lookup"><span data-stu-id="8572d-103">Selection Dialog</span></span>

<span data-ttu-id="8572d-104">Questa finestra di dialogo modale consente agli utenti di selezionare determinati elementi.</span><span class="sxs-lookup"><span data-stu-id="8572d-104">This modal dialog box enables users to select particular items.</span></span>

<span data-ttu-id="8572d-105">Una finestra di dialogo di selezione contiene un [controllo SelectionTree](selectiontree-control.md) che pubblica più ControlEvents.</span><span class="sxs-lookup"><span data-stu-id="8572d-105">A Selection Dialog box contains a [SelectionTree control](selectiontree-control.md) that publishes several ControlEvents.</span></span> <span data-ttu-id="8572d-106">Comunemente questi ControlEvents sono sottoscritti da controlli di [testo](text-control.md), [icona](icon-control.md)o [bitmap](bitmap-control.md) che visualizzano una descrizione, le dimensioni, il percorso e l'icona dell'elemento evidenziato.</span><span class="sxs-lookup"><span data-stu-id="8572d-106">Commonly these ControlEvents are subscribed to by [Text](text-control.md), [Icon](icon-control.md), or [Bitmap](bitmap-control.md) controls that display a description, the size, the path, and the icon of the highlighted item.</span></span>

<span data-ttu-id="8572d-107">Nella finestra di dialogo è presente un [controllo pulsante](pushbutton-control.md) che pubblica il [ControlEvent SelectionBrowse](selectionbrowse-controlevent.md) e genera una finestra di [dialogo di esplorazione](browse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="8572d-107">There is a [PushButton control](pushbutton-control.md) on the dialog box that publishes the [SelectionBrowse ControlEvent](selectionbrowse-controlevent.md) and spawns a [Browse Dialog](browse-dialog.md).</span></span> <span data-ttu-id="8572d-108">Il controllo Browse consente all'utente di selezionare una directory.</span><span class="sxs-lookup"><span data-stu-id="8572d-108">The Browse control enables the user to select a directory.</span></span>

<span data-ttu-id="8572d-109">L'albero di selezione viene popolato solo dopo la chiamata dell' [azione CostInitialize](costinitialize-action.md) e dell' [azione CostFinalize secondo](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="8572d-109">The selection tree is populated only after the [CostInitialize action](costinitialize-action.md) and [CostFinalize action](costfinalize-action.md) are called.</span></span>

<span data-ttu-id="8572d-110">Una finestra di dialogo di selezione viene comunemente usata per selezionare le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="8572d-110">A Selection dialog box is commonly used to select features.</span></span> <span data-ttu-id="8572d-111">Le funzionalità sono elencate come elementi in un controllo SelectionTree ed etichettate con la breve stringa di testo visualizzata nella colonna title della [tabella Feature](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="8572d-111">The features are listed as items in a SelectionTree control and labeled with the short string of text appearing in the Title column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="8572d-112">La stringa di testo nella colonna Descrizione della tabella delle funzionalità viene pubblicata come [SelectionDescription ControlEvent](selectiondescription-controlevent.md) e visualizzata da un [controllo di testo](text-control.md) nella finestra di dialogo di selezione.</span><span class="sxs-lookup"><span data-stu-id="8572d-112">The text string in the Description column of the Feature table is published as a [SelectionDescription ControlEvent](selectiondescription-controlevent.md) and displayed by a [Text control](text-control.md) in the Selection Dialog box.</span></span> <span data-ttu-id="8572d-113">Il controllo albero di selezione pubblica anche l'handle per l'icona dell'elemento evidenziato.</span><span class="sxs-lookup"><span data-stu-id="8572d-113">The Selection tree control also publishes the handle to the icon of the highlighted item.</span></span>

 

 




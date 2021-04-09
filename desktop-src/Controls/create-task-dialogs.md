---
title: Come creare finestre di dialogo attività
description: Una finestra di dialogo attività viene creata e visualizzata utilizzando la funzione TaskDialog o la funzione TaskDialogIndirect.
ms.assetid: CCEFF52F-D501-4145-9799-0A9C529017E1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ea8e3097454505acccf60c7cba3ef56c637af0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044288"
---
# <a name="how-to-create-task-dialogs"></a><span data-ttu-id="e1dcd-103">Come creare finestre di dialogo attività</span><span class="sxs-lookup"><span data-stu-id="e1dcd-103">How to Create Task Dialogs</span></span>

<span data-ttu-id="e1dcd-104">Una finestra di dialogo attività viene creata e visualizzata utilizzando la funzione [**taskDialog**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog) o la funzione [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="e1dcd-104">A task dialog is created and shown by using either the [**TaskDialog**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialog) function or the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) function.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="e1dcd-105">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="e1dcd-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="e1dcd-106">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="e1dcd-106">Technologies</span></span>

-   [<span data-ttu-id="e1dcd-107">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="e1dcd-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="e1dcd-108">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="e1dcd-108">Prerequisites</span></span>

-   <span data-ttu-id="e1dcd-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="e1dcd-109">C/C++</span></span>
-   <span data-ttu-id="e1dcd-110">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="e1dcd-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="e1dcd-111">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="e1dcd-111">Instructions</span></span>

### <a name="taskdialog"></a><span data-ttu-id="e1dcd-112">TaskDialog</span><span class="sxs-lookup"><span data-stu-id="e1dcd-112">TaskDialog</span></span>

<span data-ttu-id="e1dcd-113">La funzione **taskDialog** è adatta per le finestre di dialogo semplici che presentano informazioni testuali e richiedono una scelta standard.</span><span class="sxs-lookup"><span data-stu-id="e1dcd-113">The **TaskDialog** function is suitable for simple dialog boxes that present textual information and ask for a standard choice.</span></span> <span data-ttu-id="e1dcd-114">Questa funzione di creazione non supporta barre di stato, caselle di controllo, piè di pagina, pulsanti di espansione/compressione, pulsanti personalizzati o pulsanti di opzione.</span><span class="sxs-lookup"><span data-stu-id="e1dcd-114">This creation function does not support progress bars, check boxes, footers, expand/collapse buttons, custom buttons, or radio buttons.</span></span>

### <a name="taskdialogindirect"></a><span data-ttu-id="e1dcd-115">TaskDialogIndirect</span><span class="sxs-lookup"><span data-stu-id="e1dcd-115">TaskDialogIndirect</span></span>

<span data-ttu-id="e1dcd-116">La funzione **TaskDialogIndirect** è più potente, supporta tutti gli elementi dell'interfaccia disponibili e consente di acquisire gli eventi in una procedura di callback in modo che l'applicazione possa aggiornare un indicatore di stato o rispondere a un clic su un collegamento ipertestuale o un pulsante.</span><span class="sxs-lookup"><span data-stu-id="e1dcd-116">The **TaskDialogIndirect** function is more powerful, supporting all available interface elements and also enabling you to capture events in a callback procedure so that your application can update a progress bar or respond to a click of a hyperlink or button.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1dcd-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e1dcd-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1dcd-118">Utilizzo delle finestre di dialogo delle attività</span><span class="sxs-lookup"><span data-stu-id="e1dcd-118">Using Task Dialogs</span></span>](using-task-dialogs.md)
</dt> </dl>

 

 





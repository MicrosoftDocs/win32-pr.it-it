---
title: Come ottenere l'input dell'utente da una finestra di dialogo attività
description: Per completare un'attività, gli utenti inviano i dettagli dell'attività all'applicazione configurando i controlli all'interno della finestra di dialogo attività e quindi facendo clic su un pulsante di comando (in genere OK).
ms.assetid: 73CD8FBF-95C9-43C8-B9D8-3823840C23A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd53c8051747187123821211ac7e17c9915b5fd
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963511"
---
# <a name="how-to-get-user-input-from-a-task-dialog"></a><span data-ttu-id="69cf6-103">Come ottenere l'input dell'utente da una finestra di dialogo attività</span><span class="sxs-lookup"><span data-stu-id="69cf6-103">How to Get User Input from a Task Dialog</span></span>

<span data-ttu-id="69cf6-104">Per completare un'attività, gli utenti inviano i dettagli dell'attività all'applicazione configurando i controlli all'interno della finestra di dialogo attività e quindi facendo clic su un pulsante di comando (in genere **OK**).</span><span class="sxs-lookup"><span data-stu-id="69cf6-104">To complete a task, users submit the task details to the application by configuring the controls within the task dialog, and then clicking a command button (usually **OK**).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="69cf6-105">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="69cf6-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="69cf6-106">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="69cf6-106">Technologies</span></span>

-   [<span data-ttu-id="69cf6-107">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="69cf6-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="69cf6-108">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="69cf6-108">Prerequisites</span></span>

-   <span data-ttu-id="69cf6-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="69cf6-109">C/C++</span></span>
-   <span data-ttu-id="69cf6-110">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="69cf6-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="69cf6-111">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="69cf6-111">Instructions</span></span>

### <a name="getting-user-input-from-a-task-dialog"></a><span data-ttu-id="69cf6-112">Recupero dell'input utente da una finestra di dialogo attività</span><span class="sxs-lookup"><span data-stu-id="69cf6-112">Getting User Input from a Task Dialog</span></span>

<span data-ttu-id="69cf6-113">È possibile identificare il pulsante su cui è stato fatto clic esaminando il parametro *pnButton* della funzione chiamante.</span><span class="sxs-lookup"><span data-stu-id="69cf6-113">You can identify the button that was clicked by examining the *pnButton* parameter of the calling function.</span></span> <span data-ttu-id="69cf6-114">È anche possibile identificare il pulsante di opzione selezionato dal parametro *pnRadioButton* di [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)e lo stato della casella di controllo della verifica dal parametro *pfVerificationFlagChecked* .</span><span class="sxs-lookup"><span data-stu-id="69cf6-114">You can also identify the selected radio button from the *pnRadioButton* parameter of [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect), and the state of the verification check box from the *pfVerificationFlagChecked* parameter.</span></span>

<span data-ttu-id="69cf6-115">I clic sui pulsanti e i collegamenti ipertestuali vengono ricevuti dalla funzione [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) sotto forma di [ \_ pulsante TDN \_ selezionato](tdn-button-clicked.md) e [ \_ collegamento ipertestuale TDN \_ fatto clic](tdn-hyperlink-clicked.md) su notifiche.</span><span class="sxs-lookup"><span data-stu-id="69cf6-115">Clicks on buttons and hyperlinks are received by the [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) function in the form of [TDN\_BUTTON\_CLICKED](tdn-button-clicked.md) and [TDN\_HYPERLINK\_CLICKED](tdn-hyperlink-clicked.md) notifications.</span></span> <span data-ttu-id="69cf6-116">Se la funzione di callback restituisce \_ OK dopo aver gestito una notifica di un pulsante, la finestra di dialogo attività viene chiusa e l'identificatore di comando del pulsante viene restituito in *pnButton*.</span><span class="sxs-lookup"><span data-stu-id="69cf6-116">If your callback function returns S\_OK after handling a button notification, the task dialog closes and the command identifier of the button is returned in *pnButton*.</span></span> <span data-ttu-id="69cf6-117">Se si restituisce \_ false oppure non si dispone di una funzione di callback, la finestra di dialogo attività rimane aperta.</span><span class="sxs-lookup"><span data-stu-id="69cf6-117">If you return S\_FALSE, or do not have a callback function, the task dialog remains open.</span></span>

## <a name="related-topics"></a><span data-ttu-id="69cf6-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="69cf6-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69cf6-119">Utilizzo delle finestre di dialogo delle attività</span><span class="sxs-lookup"><span data-stu-id="69cf6-119">Using Task Dialogs</span></span>](using-task-dialogs.md)
</dt> </dl>

 

 
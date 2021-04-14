---
description: Una finestra di dialogo di errore è una finestra di dialogo modale in cui viene visualizzato un messaggio di errore. In ogni installazione può essere presente più di una finestra di dialogo di errore.
ms.assetid: 11d4fe8b-ec5f-4576-95e5-c86344f0195c
title: Finestra di dialogo di errore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a153f5e6ee38235f830937d794a9ca9b81314583
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527252"
---
# <a name="error-dialog"></a><span data-ttu-id="aa0a5-104">Finestra di dialogo di errore</span><span class="sxs-lookup"><span data-stu-id="aa0a5-104">Error Dialog</span></span>

<span data-ttu-id="aa0a5-105">Una finestra di dialogo di errore è una finestra di dialogo modale in cui viene visualizzato un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-105">An Error dialog box is a modal dialog box box that displays an error message.</span></span> <span data-ttu-id="aa0a5-106">In ogni installazione può essere presente più di una finestra di dialogo di errore.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-106">More than one Error dialog box can exist in each installation.</span></span>

<span data-ttu-id="aa0a5-107">È necessario impostare una proprietà ErrorDialog che specifichi la finestra di dialogo da usare.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-107">An ErrorDialog property needs to be set that specifies which dialog box is to be used.</span></span> <span data-ttu-id="aa0a5-108">Se questa proprietà non è impostata o non punta a una finestra di dialogo di errore valida, i messaggi di errore non verranno visualizzati.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-108">If this property is not set or does not point to a valid Error dialog box, then the error messages will not be displayed.</span></span> <span data-ttu-id="aa0a5-109">In questo caso, l'errore viene registrato solo con un avviso sulla finestra di dialogo mancante.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-109">In this case, the error is only logged with a warning about the missing dialog box.</span></span>

<span data-ttu-id="aa0a5-110">Per una finestra di dialogo di errore è necessario impostare il [bit di stile della finestra di dialogo di errore](error-dialog-style-bit.md) .</span><span class="sxs-lookup"><span data-stu-id="aa0a5-110">An Error dialog box must have the [Error Dialog style bit](error-dialog-style-bit.md) set.</span></span> <span data-ttu-id="aa0a5-111">La finestra di dialogo deve avere un [controllo di testo](text-control.md) denominato ErrorText.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-111">The dialog box must have a [Text control](text-control.md) named ErrorText.</span></span> <span data-ttu-id="aa0a5-112">Il record per la finestra di dialogo di errore nella [tabella della finestra di dialogo](dialog-table.md) deve avere il controllo ErrorText immesso nel \_ primo campo del controllo.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-112">The record for the Error dialog box in the [Dialog table](dialog-table.md) must have the ErrorText control entered into the Control\_First field.</span></span>

<span data-ttu-id="aa0a5-113">La finestra di dialogo deve contenere sette [pulsanti](pushbutton-control.md).</span><span class="sxs-lookup"><span data-stu-id="aa0a5-113">The dialog box must contain seven [PushButtons](pushbutton-control.md).</span></span> <span data-ttu-id="aa0a5-114">Tutti questi pulsanti specificano il ControlEvent [EndDialog](enddialog-controlevent.md) nella [tabella ControlEvent](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="aa0a5-114">All of these buttons specify the [EndDialog](enddialog-controlevent.md) ControlEvent in the [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="aa0a5-115">Ogni pulsante specifica uno dei seguenti attributi: **ErrorAbort**, **ErrorCancel**, **ErrorIgnore**, **errorno**, **ErrorOk**, **ErrorRetry**, **ErrorYes**.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-115">Each button specifies one of the following attributes: **ErrorAbort**, **ErrorCancel**, **ErrorIgnore**, **ErrorNo**, **ErrorOk**, **ErrorRetry**, **ErrorYes**.</span></span>

> [!Note]  
> <span data-ttu-id="aa0a5-116">Lo stato attivo di questi controlli non deve essere collegato tramite l'utilizzo della colonna del controllo \_ successiva nella [tabella del controllo](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="aa0a5-116">The focus of these controls should not be linked through the use of the Control\_Next column in the [Control table](control-table.md).</span></span>

 

<span data-ttu-id="aa0a5-117">Questi pulsanti devono essere posizionati approssimativamente nella stessa posizione della finestra di dialogo perché, al momento della creazione, viene creato solo un subset di questi sette pulsanti, a seconda del messaggio.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-117">These buttons should be placed in approximately the same position in the dialog box because when it is created, only a subset of these seven buttons is created, depending on the message.</span></span> <span data-ttu-id="aa0a5-118">La coordinata X dei pulsanti viene modificata in modo che i pulsanti visualizzati siano spaziati in modo uniforme.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-118">The X coordinate of the buttons is modified so the buttons that are displayed are evenly spaced.</span></span> <span data-ttu-id="aa0a5-119">Le coordinate Y, l'altezza e la larghezza dei pulsanti sono invariate.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-119">The Y coordinate, height, and width of the buttons are unchanged.</span></span> <span data-ttu-id="aa0a5-120">Poiché i pulsanti sono disposti orizzontalmente, nessun altro controllo può essere posizionato nella stessa area orizzontale della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-120">Because the buttons are arranged horizontally, no other control can be placed in the same horizontal region of the dialog box.</span></span>

<span data-ttu-id="aa0a5-121">Per una finestra di dialogo di errore, i \_ campi controllo predefinito e \_ Annulla controllo nella tabella della finestra di [dialogo](dialog-table.md) vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-121">For an Error dialog box, the Control\_Default and Control\_Cancel fields in the [Dialog table](dialog-table.md) are ignored.</span></span> <span data-ttu-id="aa0a5-122">Il \_ primo campo controllo per una finestra di dialogo di errore deve specificare il controllo ErrorText.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-122">The Control\_First field for an Error dialog box must specify the ErrorText control.</span></span>

<span data-ttu-id="aa0a5-123">Se in questa finestra di dialogo è incluso un [controllo icona](icon-control.md) denominato ErrorIcon, vengono visualizzate le icone di Windows standard seguenti:</span><span class="sxs-lookup"><span data-stu-id="aa0a5-123">If an [Icon control](icon-control.md) named ErrorIcon is included on this dialog, the following standard Windows icons are displayed:</span></span>

-   <span data-ttu-id="aa0a5-124">\_Errore IDI in risposta ai messaggi imtFatalExit.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-124">IDI\_ERROR in response to imtFatalExit messages.</span></span>
-   <span data-ttu-id="aa0a5-125">Avviso di IDI \_ in risposta ai messaggi imterror e imtWarning.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-125">IDI\_WARNING in response to imtError and imtWarning messages.</span></span>
-   <span data-ttu-id="aa0a5-126">\_Informazioni di Idi in risposta ai messaggi imtOutOfDiskSpace.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-126">IDI\_INFORMATION in response to imtOutOfDiskSpace messages.</span></span>

<span data-ttu-id="aa0a5-127">Il controllo ErrorIcon deve essere creato con l' [attributo del controllo FixedSize](fixedsize-control-attribute.md) impostato in modo da evitare il ridimensionamento non corretto delle icone standard di Windows.</span><span class="sxs-lookup"><span data-stu-id="aa0a5-127">The ErrorIcon control should be created with the [FixedSize control attribute](fixedsize-control-attribute.md) set to avoid improper sizing of the standard Windows icons.</span></span>

 

 




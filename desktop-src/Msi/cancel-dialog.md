---
description: Una finestra di dialogo Annulla conferma che l'utente desidera terminare l'installazione. Si tratta di una finestra di dialogo modale.
ms.assetid: 5dab4315-721e-417d-91e0-b38653a65c23
title: Annulla finestra di dialogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1022a7613f3f5341d8c833b7cbe2645ce871aeb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311000"
---
# <a name="cancel-dialog"></a><span data-ttu-id="5c421-104">Annulla finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="5c421-104">Cancel Dialog</span></span>

<span data-ttu-id="5c421-105">Una finestra di dialogo **Annulla** conferma che l'utente desidera terminare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="5c421-105">A **Cancel** dialog box confirms that the user wants to terminate the installation.</span></span> <span data-ttu-id="5c421-106">Si tratta di una finestra di dialogo modale.</span><span class="sxs-lookup"><span data-stu-id="5c421-106">This is a modal dialog box.</span></span>

<span data-ttu-id="5c421-107">Questo tipo di finestra di dialogo contiene in genere un [controllo di testo](text-control.md) e due [pulsanti](pushbutton-control.md).</span><span class="sxs-lookup"><span data-stu-id="5c421-107">This type of dialog box commonly contains a [Text control](text-control.md) and two [PushButtons](pushbutton-control.md).</span></span> <span data-ttu-id="5c421-108">I due pulsanti consentono all'utente di scegliere di tornare all'ultima finestra di dialogo o di confermare la chiusura dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="5c421-108">The two buttons give the user the choice of either returning to the last dialog box or confirming the termination of the installation.</span></span>

<span data-ttu-id="5c421-109">Il ControlEvent [EndDialog](enddialog-controlevent.md) è collegato a questi due pulsanti nella [tabella ControlEvent](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="5c421-109">The [EndDialog](enddialog-controlevent.md) ControlEvent is linked to these two buttons in the [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="5c421-110">Il parametro *return* del ControlEvent EndDialog è collegato a uno dei pulsanti e causa la terminazione della finestra di dialogo **Cancel** e lo stato attivo per tornare alla finestra di dialogo precedente.</span><span class="sxs-lookup"><span data-stu-id="5c421-110">The *Return* parameter of the EndDialog ControlEvent is linked to one of the buttons and causes the **Cancel** dialog box to be terminated and the focus to return to the previous dialog box.</span></span> <span data-ttu-id="5c421-111">Il parametro *Exit* è collegato al pulsante Other e fa in modo che l'interfaccia utente restituisca il controllo al programma di installazione con il codice appropriato che indica che l'utente desidera uscire.</span><span class="sxs-lookup"><span data-stu-id="5c421-111">The *Exit* parameter is linked to the other button and causes the user interface to return control to the installer with the appropriate code indicating that the user wants to exit.</span></span> <span data-ttu-id="5c421-112">Il programma di installazione viene quindi arrestato e viene visualizzata la [finestra di dialogo UserExit](userexit-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="5c421-112">The installer then shuts down and displays the [UserExit Dialog](userexit-dialog.md).</span></span>

 

 




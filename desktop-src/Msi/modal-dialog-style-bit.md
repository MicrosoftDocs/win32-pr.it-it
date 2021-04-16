---
description: Se questo bit è impostato, la finestra di dialogo è modale, altre finestre di dialogo della stessa applicazione non possono essere posizionate sopra di esso e la finestra di dialogo mantiene il controllo mentre è in esecuzione.
ms.assetid: 14871dc7-c928-4381-a043-6beb06d25214
title: Bit stile finestra di dialogo modale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd0004cc7b31557f9a606050a1f8569fa2a493d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529749"
---
# <a name="modal-dialog-style-bit"></a><span data-ttu-id="8da06-103">Bit stile finestra di dialogo modale</span><span class="sxs-lookup"><span data-stu-id="8da06-103">Modal Dialog Style Bit</span></span>

<span data-ttu-id="8da06-104">Se questo bit è impostato, la finestra di dialogo è modale, altre finestre di dialogo della stessa applicazione non possono essere posizionate sopra di esso e la finestra di dialogo mantiene il controllo mentre è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8da06-104">If this bit is set, the dialog box is modal, other dialogs of the same application cannot be put on top of it, and the dialog keeps the control while it is running.</span></span> <span data-ttu-id="8da06-105">Se questo bit non è impostato, la finestra di dialogo non è modale, altre finestre di dialogo della stessa applicazione possono essere spostate sopra di esso.</span><span class="sxs-lookup"><span data-stu-id="8da06-105">If this bit is not set, the dialog is modeless, other dialogs of the same application may be moved on top of it.</span></span> <span data-ttu-id="8da06-106">Dopo la creazione e la visualizzazione di una finestra di dialogo non modale, l'interfaccia utente restituisce il controllo al programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="8da06-106">After a modeless dialog is created and displayed, the user interface returns control to the installer.</span></span> <span data-ttu-id="8da06-107">Il programma di installazione chiama quindi l'interfaccia utente periodicamente per aggiornare la finestra di dialogo e fornire la possibilità di elaborare i messaggi.</span><span class="sxs-lookup"><span data-stu-id="8da06-107">The installer then calls the user interface periodically to update the dialog and to give it a chance to process the messages.</span></span> <span data-ttu-id="8da06-108">Non appena viene eseguita questa operazione, il controllo viene restituito al programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="8da06-108">As soon as this is done, the control is returned to the installer.</span></span>

> [!Note]  
> <span data-ttu-id="8da06-109">Non devono essere presenti finestre di dialogo non modali in una sequenza della procedura guidata, poiché questo restituisce il controllo al programma di installazione, terminando la sequenza della procedura guidata in modo anomalo.</span><span class="sxs-lookup"><span data-stu-id="8da06-109">There should be no modeless dialogs in a wizard sequence, since this would return control to the installer, ending the wizard sequence prematurely.</span></span>

 

## <a name="value"></a><span data-ttu-id="8da06-110">Valore</span><span class="sxs-lookup"><span data-stu-id="8da06-110">Value</span></span>



| <span data-ttu-id="8da06-111">Decimal</span><span class="sxs-lookup"><span data-stu-id="8da06-111">Decimal</span></span> | <span data-ttu-id="8da06-112">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="8da06-112">Hexadecimal</span></span> | <span data-ttu-id="8da06-113">Costante</span><span class="sxs-lookup"><span data-stu-id="8da06-113">Constant</span></span>                          |
|---------|-------------|-----------------------------------|
| <span data-ttu-id="8da06-114">2</span><span class="sxs-lookup"><span data-stu-id="8da06-114">2</span></span>       | <span data-ttu-id="8da06-115">0x00000002</span><span class="sxs-lookup"><span data-stu-id="8da06-115">0x00000002</span></span>  | <span data-ttu-id="8da06-116">**msidbDialogAttributesSysModal**</span><span class="sxs-lookup"><span data-stu-id="8da06-116">**msidbDialogAttributesSysModal**</span></span> |



 

 

 




---
description: Se questo bit è impostato, la finestra di dialogo è una finestra di dialogo di errore.
ms.assetid: a8a95f6a-6465-433b-98a4-95281cddedd3
title: Bit di stile della finestra di dialogo di errore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ff3e4868cf1941f80be4f7b2d70068ec949a4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308330"
---
# <a name="error-dialog-style-bit"></a><span data-ttu-id="763e0-103">Bit di stile della finestra di dialogo di errore</span><span class="sxs-lookup"><span data-stu-id="763e0-103">Error Dialog Style Bit</span></span>

<span data-ttu-id="763e0-104">Se questo bit è impostato, la finestra di dialogo è una finestra di dialogo di errore.</span><span class="sxs-lookup"><span data-stu-id="763e0-104">If this bit is set, the dialog box is an error dialog.</span></span>

<span data-ttu-id="763e0-105">Con questo stile può essere presente più di una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="763e0-105">There can be more than one dialog with this style.</span></span> <span data-ttu-id="763e0-106">La proprietà **ErrorDialog** determina quale finestra di dialogo viene utilizzata come finestra di dialogo di errore.</span><span class="sxs-lookup"><span data-stu-id="763e0-106">The **ErrorDialog** property determines which dialog is used as an error dialog.</span></span> <span data-ttu-id="763e0-107">La finestra di dialogo selezionata può essere solo una di quelle per cui è impostato questo bit di stile.</span><span class="sxs-lookup"><span data-stu-id="763e0-107">The selected dialog can be only one of those that have this style bit set.</span></span> <span data-ttu-id="763e0-108">La finestra di dialogo di errore deve avere un controllo testo statico denominato ErrorText.</span><span class="sxs-lookup"><span data-stu-id="763e0-108">The error dialog must have a static text control named ErrorText.</span></span> <span data-ttu-id="763e0-109">Questo controllo riceve il testo del messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="763e0-109">This control receives the text of the error message.</span></span> <span data-ttu-id="763e0-110">Nella finestra di dialogo devono essere presenti anche i sette pulsanti di push corrispondenti ai valori restituiti possibili.</span><span class="sxs-lookup"><span data-stu-id="763e0-110">The dialog should also have the seven push buttons corresponding to the possible return values.</span></span> <span data-ttu-id="763e0-111">Il messaggio di errore determina quale di questi pulsanti è effettivamente visualizzato.</span><span class="sxs-lookup"><span data-stu-id="763e0-111">The error message determines which of these buttons are actually displayed.</span></span> <span data-ttu-id="763e0-112">I pulsanti visualizzati vengono ridisposti in modo che siano distribuiti uniformemente nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="763e0-112">The displayed buttons are rearranged so they are evenly distributed on the dialog.</span></span> <span data-ttu-id="763e0-113">Questa ridisposizione modifica la coordinata X dei pulsanti, ma non le altre tre coordinate.</span><span class="sxs-lookup"><span data-stu-id="763e0-113">This rearrangement changes the X coordinate of the buttons, but not the other three coordinates.</span></span> <span data-ttu-id="763e0-114">È pertanto consigliabile che non venga creato alcun altro controllo nella stessa area orizzontale della finestra di dialogo dei pulsanti.</span><span class="sxs-lookup"><span data-stu-id="763e0-114">Therefore it is advisable that no other control should be authored in the same horizontal region of the dialog as the buttons.</span></span> <span data-ttu-id="763e0-115">Se il messaggio di errore non specifica alcun pulsante, viene visualizzato il pulsante **OK** .</span><span class="sxs-lookup"><span data-stu-id="763e0-115">If the error message specifies no button, the **OK** button is displayed.</span></span> <span data-ttu-id="763e0-116">Il pulsante **predefinito** , i valori primo controllo attivo e pulsante **Annulla** vengono ignorati per una finestra di dialogo di errore.</span><span class="sxs-lookup"><span data-stu-id="763e0-116">The **Default** button, First active control and **Cancel** button values are ignored for an error dialog.</span></span> <span data-ttu-id="763e0-117">Il pulsante **predefinito** definito nel messaggio di errore verrà assegnato a tutti e tre i valori.</span><span class="sxs-lookup"><span data-stu-id="763e0-117">The **Default** button defined in the error message will be assigned to all three values.</span></span> <span data-ttu-id="763e0-118">L'effetto del push di questi pulsanti deve essere definito nella [tabella ControlEvent](controlevent-table.md) esattamente come per tutti gli altri pulsanti.</span><span class="sxs-lookup"><span data-stu-id="763e0-118">The effect of pushing these buttons have to be defined in the [ControlEvent table](controlevent-table.md) just like for all other buttons.</span></span> <span data-ttu-id="763e0-119">Il titolo della finestra di dialogo viene creato in modo analogo ad altre finestre di dialogo.</span><span class="sxs-lookup"><span data-stu-id="763e0-119">The title of the dialog is authored in a way similar to other dialogs.</span></span> <span data-ttu-id="763e0-120">Può essere sovrascritto dal messaggio di errore se specifica un testo dell'intestazione dopo l'elenco dei pulsanti.</span><span class="sxs-lookup"><span data-stu-id="763e0-120">It can get overwritten by the error message if it specifies a header text after the button list.</span></span>

## <a name="value"></a><span data-ttu-id="763e0-121">Valore</span><span class="sxs-lookup"><span data-stu-id="763e0-121">Value</span></span>



| <span data-ttu-id="763e0-122">Decimal</span><span class="sxs-lookup"><span data-stu-id="763e0-122">Decimal</span></span> | <span data-ttu-id="763e0-123">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="763e0-123">Hexadecimal</span></span> | <span data-ttu-id="763e0-124">Costante</span><span class="sxs-lookup"><span data-stu-id="763e0-124">Constant</span></span>                       |
|---------|-------------|--------------------------------|
| <span data-ttu-id="763e0-125">65536</span><span class="sxs-lookup"><span data-stu-id="763e0-125">65536</span></span>   | <span data-ttu-id="763e0-126">0x00010000</span><span class="sxs-lookup"><span data-stu-id="763e0-126">0x00010000</span></span>  | <span data-ttu-id="763e0-127">**msidbDialogAttributesError**</span><span class="sxs-lookup"><span data-stu-id="763e0-127">**msidbDialogAttributesError**</span></span> |



 

 

 




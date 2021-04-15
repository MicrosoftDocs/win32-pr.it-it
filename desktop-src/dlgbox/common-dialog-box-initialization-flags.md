---
title: Flag di inizializzazione comuni della finestra di dialogo
description: I flag vengono utilizzati per modificare il comportamento e l'aspetto di una finestra di dialogo comune.
ms.assetid: 072cdcab-00d1-4a09-97fb-a6de2d51392e
keywords:
- Libreria finestra di dialogo comune, inizializzazione
- finestre di dialogo comuni, inizializzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b0c994e743178e3b6a17129275affed099d3004
ms.sourcegitcommit: 56f8e4d5119e5018363fa2dc3472cdff203c6913
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/19/2020
ms.locfileid: "104474729"
---
# <a name="common-dialog-box-initialization-flags"></a><span data-ttu-id="c3f5b-105">Flag di inizializzazione comuni della finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="c3f5b-105">Common Dialog Box Initialization Flags</span></span>

<span data-ttu-id="c3f5b-106">I flag vengono utilizzati per modificare il comportamento e l'aspetto di una finestra di dialogo comune.</span><span class="sxs-lookup"><span data-stu-id="c3f5b-106">Flags are used to modify the behavior and appearance of a common dialog box.</span></span> <span data-ttu-id="c3f5b-107">I flag di inizializzazione sono i valori impostati nel membro **Flags** della struttura utilizzata per creare la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="c3f5b-107">Initialization flags are the values that you set in the **Flags** member of the structure that is used to create the dialog box.</span></span> <span data-ttu-id="c3f5b-108">Usare i flag per specificare i controlli in una finestra di dialogo che ricevono i valori iniziali, per disabilitare i controlli selezionati e per modificare l'intervallo di valori che l'utente può impostare con i controlli.</span><span class="sxs-lookup"><span data-stu-id="c3f5b-108">You use the flags to specify which controls in a dialog box receive initial values, to disable selected controls, and to modify the range of values that the user can set with the controls.</span></span> <span data-ttu-id="c3f5b-109">È inoltre possibile utilizzare i flag per abilitare le procedure Hook e i modelli personalizzati per le finestre di dialogo.</span><span class="sxs-lookup"><span data-stu-id="c3f5b-109">You also use the flags to enable hook procedures and custom templates for the dialog boxes.</span></span>

<span data-ttu-id="c3f5b-110">Ad esempio, è possibile impostare il valore degli **\_ effetti CF** nel membro **flag** della struttura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) per indicare alla finestra di dialogo **tipo di carattere** di visualizzare i controlli effetti.</span><span class="sxs-lookup"><span data-stu-id="c3f5b-110">For example, you can set the **CF\_EFFECTS** value in the **Flags** member of the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure to direct the **Font** dialog box to display the effects controls.</span></span> <span data-ttu-id="c3f5b-111">Questi controlli consentono all'utente di scegliere un colore del carattere, nonché gli effetti barrato e sottolineato.</span><span class="sxs-lookup"><span data-stu-id="c3f5b-111">These controls let the user choose a font color as well as strikethrough and underline effects.</span></span>

<span data-ttu-id="c3f5b-112">I valori del flag di inizializzazione sono univoci per ogni finestra di dialogo comune e sono descritti in dettaglio dai membri dei **flag** delle seguenti strutture corrispondenti:</span><span class="sxs-lookup"><span data-stu-id="c3f5b-112">The initialization flag values are unique to each common dialog box and are described in detail by the **Flags** members of the following structures that correspond to them:</span></span>

-   [<span data-ttu-id="c3f5b-113">**LE CHOOSECOLOR.**</span><span class="sxs-lookup"><span data-stu-id="c3f5b-113">**CHOOSECOLOR**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
-   [<span data-ttu-id="c3f5b-114">**CHOOSEFONT**</span><span class="sxs-lookup"><span data-stu-id="c3f5b-114">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
-   [<span data-ttu-id="c3f5b-115">**FINDREPLACE**</span><span class="sxs-lookup"><span data-stu-id="c3f5b-115">**FINDREPLACE**</span></span>](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
-   [<span data-ttu-id="c3f5b-116">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="c3f5b-116">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
-   [<span data-ttu-id="c3f5b-117">**PAGESETUPDLG**</span><span class="sxs-lookup"><span data-stu-id="c3f5b-117">**PAGESETUPDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
-   [<span data-ttu-id="c3f5b-118">**PRINTDLG**</span><span class="sxs-lookup"><span data-stu-id="c3f5b-118">**PRINTDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-printdlga)
-   [<span data-ttu-id="c3f5b-119">**PRINTDLGEX**</span><span class="sxs-lookup"><span data-stu-id="c3f5b-119">**PRINTDLGEX**</span></span>](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)

 

 





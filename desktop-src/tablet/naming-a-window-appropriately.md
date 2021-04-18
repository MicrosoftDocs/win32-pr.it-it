---
description: Cenni preliminari sulla denominazione di una finestra in modo appropriato e sull'impostazione della didascalia della finestra per Tablet PC.
ms.assetid: 9d064188-53a1-4cb5-b516-99610d7b8134
title: Assegnazione di un nome a una finestra in modo appropriato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaee320f621acf834d7c0ec5978a9e42f0811e31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315562"
---
# <a name="naming-a-window-appropriately"></a><span data-ttu-id="edef8-103">Assegnazione di un nome a una finestra in modo appropriato</span><span class="sxs-lookup"><span data-stu-id="edef8-103">Naming a Window Appropriately</span></span>

<span data-ttu-id="edef8-104">Assegnare a ogni finestra una didascalia intuitiva, anche se la finestra o la relativa didascalia è invisibile.</span><span class="sxs-lookup"><span data-stu-id="edef8-104">Assign every window a user-friendly caption, even if the window or its caption is invisible.</span></span> <span data-ttu-id="edef8-105">Questo consente la funzionalità di riconoscimento vocale per identificare la finestra e la gerarchia della finestra.</span><span class="sxs-lookup"><span data-stu-id="edef8-105">This allows the speech functionality to identify the window and the window hierarchy.</span></span> <span data-ttu-id="edef8-106">Questa raccomandazione si applica a tutte le finestre: finestre di primo livello con frame visibili; finestre figlio, ad esempio tavolozze mobili; controlli personalizzati; barre degli strumenti e riquadri in una finestra, quando vengono implementati come finestre figlio.</span><span class="sxs-lookup"><span data-stu-id="edef8-106">This recommendation applies to all windows: top-level windows with visible frames; child windows, such as floating palettes; custom controls; toolbars; and panes within a window, when implemented as child windows.</span></span>

<span data-ttu-id="edef8-107">È possibile impostare la didascalia della finestra in tre modi:</span><span class="sxs-lookup"><span data-stu-id="edef8-107">There are three ways to set the window caption:</span></span>

-   <span data-ttu-id="edef8-108">Impostare la stringa nello script della risorsa durante la chiamata di [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o delle funzioni correlate.</span><span class="sxs-lookup"><span data-stu-id="edef8-108">Set the string in your resource script when calling [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or related functions.</span></span>
-   <span data-ttu-id="edef8-109">Chiamare la funzione [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) .</span><span class="sxs-lookup"><span data-stu-id="edef8-109">Call the [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) function.</span></span>
-   <span data-ttu-id="edef8-110">Definire il nome dei controlli nelle finestre di dialogo utilizzando le tecniche descritte in [denominare i controlli nelle finestre di dialogo](naming-controls-in-dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="edef8-110">Define the name of controls in dialog boxes by using the techniques described in [Naming Controls in Dialog Boxes](naming-controls-in-dialog-boxes.md).</span></span> <span data-ttu-id="edef8-111">Questo è l'unico metodo per etichettare un controllo di modifica, perché l'impostazione dell'etichetta intrinseca Controls modifica il contenuto dei controlli.</span><span class="sxs-lookup"><span data-stu-id="edef8-111">This is the only method for labeling an edit control, because setting the controls intrinsic label changes the controls contents.</span></span>

<span data-ttu-id="edef8-112">È possibile eseguire una query sulla didascalia usando Microsoft Active Accessibility o il \_ messaggio WM gettext.</span><span class="sxs-lookup"><span data-stu-id="edef8-112">You can query the caption by using either Microsoft Active Accessibility or the WM\_GETTEXT message.</span></span>

<span data-ttu-id="edef8-113">Per ulteriori informazioni sull'esecuzione di query sulla didascalia utilizzando Active Accessibility, vedere la sezione relativa all' [accessibilità](/windows/desktop/accessibility) .</span><span class="sxs-lookup"><span data-stu-id="edef8-113">For more information about querying the caption by using Active Accessibility, see the [Accessibility](/windows/desktop/accessibility) section.</span></span>

 

 

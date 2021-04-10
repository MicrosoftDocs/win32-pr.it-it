---
title: Supporto della localizzazione per i controlli comuni
description: In questo argomento viene descritto il supporto per le lingue nazionali integrate nei controlli comuni.
ms.assetid: c5720198-9071-4213-8dad-50b4c015c5f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70ccc307defa687c8640425dd781660641fe78a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955263"
---
# <a name="localization-support-for-common-controls"></a><span data-ttu-id="b31c1-103">Supporto della localizzazione per i controlli comuni</span><span class="sxs-lookup"><span data-stu-id="b31c1-103">Localization Support for Common Controls</span></span>

<span data-ttu-id="b31c1-104">In questo argomento viene descritto il supporto per le lingue nazionali integrate nei controlli comuni.</span><span class="sxs-lookup"><span data-stu-id="b31c1-104">This topic describes the support for national languages that is built into the common controls.</span></span> <span data-ttu-id="b31c1-105">Il supporto del linguaggio nazionale integrato semplifica l'implementazione delle applicazioni localizzate.</span><span class="sxs-lookup"><span data-stu-id="b31c1-105">The built-in national language support simplifies the implementation of localized applications.</span></span>

<span data-ttu-id="b31c1-106">In questo argomento sono incluse le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="b31c1-106">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="b31c1-107">Specifica di una lingua per i controlli comuni</span><span class="sxs-lookup"><span data-stu-id="b31c1-107">Specifying a Language for the Common Controls</span></span>](#specifying-a-language-for-the-common-controls)
-   [<span data-ttu-id="b31c1-108">Specifica di una lingua per i controlli in una finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="b31c1-108">Specifying a Language for Controls in a Dialog Box</span></span>](#specifying-a-language-for-controls-in-a-dialog-box)
-   [<span data-ttu-id="b31c1-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b31c1-109">Related topics</span></span>](#related-topics)

## <a name="specifying-a-language-for-the-common-controls"></a><span data-ttu-id="b31c1-110">Specifica di una lingua per i controlli comuni</span><span class="sxs-lookup"><span data-stu-id="b31c1-110">Specifying a Language for the Common Controls</span></span>

<span data-ttu-id="b31c1-111">Se si desidera specificare una lingua per i controlli comuni diversi dalla lingua di sistema, chiamare [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage).</span><span class="sxs-lookup"><span data-stu-id="b31c1-111">If you want to specify a language for the common controls that is different than the system language, call [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage).</span></span> <span data-ttu-id="b31c1-112">La lingua specificata da questa funzione si applica solo al processo da cui viene chiamata la funzione.</span><span class="sxs-lookup"><span data-stu-id="b31c1-112">The language specified by this function applies only to the process from which the function is called.</span></span>

<span data-ttu-id="b31c1-113">Per determinare la lingua attualmente utilizzata dai controlli comuni, chiamare [**GetMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-getmuilanguage).</span><span class="sxs-lookup"><span data-stu-id="b31c1-113">To determine the language currently being used by the common controls, call [**GetMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-getmuilanguage).</span></span> <span data-ttu-id="b31c1-114">Restituisce il valore impostato da una chiamata precedente a [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage).</span><span class="sxs-lookup"><span data-stu-id="b31c1-114">It returns the value that was set by a previous call to [**InitMUILanguage**](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage).</span></span> <span data-ttu-id="b31c1-115">Il linguaggio restituito è quello specificato per il processo da cui viene chiamato.</span><span class="sxs-lookup"><span data-stu-id="b31c1-115">The language returned is the one that was specified for the process it is called from.</span></span> <span data-ttu-id="b31c1-116">Se **InitMUILanguage** non è stato chiamato o è stato chiamato da un altro processo, **GetMUILanguage** restituirà un valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="b31c1-116">If **InitMUILanguage** has not been called, or was called from another process, **GetMUILanguage** will return a default value.</span></span>

## <a name="specifying-a-language-for-controls-in-a-dialog-box"></a><span data-ttu-id="b31c1-117">Specifica di una lingua per i controlli in una finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="b31c1-117">Specifying a Language for Controls in a Dialog Box</span></span>

<span data-ttu-id="b31c1-118">A differenza dei controlli comuni, i controlli predefiniti, quali pulsanti o caselle di modifica, non usano la lingua di sistema corrente per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="b31c1-118">Unlike common controls, predefined controls such as buttons or edit boxes do not use the current system language by default.</span></span> <span data-ttu-id="b31c1-119">Il controllo del tipo di carattere nativo è un controllo invisibile che funziona in background per consentire ai controlli predefiniti di una finestra di dialogo di visualizzare la lingua del sistema corrente.</span><span class="sxs-lookup"><span data-stu-id="b31c1-119">The native font control is an invisible control that works in the background to allow a dialog box's predefined controls to display the current system language.</span></span>

<span data-ttu-id="b31c1-120">Per usare il controllo del tipo di carattere nativo, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="b31c1-120">To use the native font control, follow this procedure.</span></span>

1.  <span data-ttu-id="b31c1-121">Inizializzare il controllo del tipo di carattere nativo chiamando [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex).</span><span class="sxs-lookup"><span data-stu-id="b31c1-121">Initialize the native font control by calling [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex).</span></span> <span data-ttu-id="b31c1-122">Impostare il membro **dwICC** della struttura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) a cui punta *lpInitCtrls* alla classe ICC \_ NATIVEFNTCTL \_ .</span><span class="sxs-lookup"><span data-stu-id="b31c1-122">Set the **dwICC** member of the [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure pointed to by *lpInitCtrls* to ICC\_NATIVEFNTCTL\_CLASS.</span></span>
2.  <span data-ttu-id="b31c1-123">Aggiungere il controllo allo script di risorsa per la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b31c1-123">Add the control to the resource script for the dialog box.</span></span> <span data-ttu-id="b31c1-124">Impostare uno o più dei flag di stile seguenti per specificare quali controlli saranno interessati.</span><span class="sxs-lookup"><span data-stu-id="b31c1-124">Set one or more of the following style flags to specify which controls will be affected.</span></span> 

    | <span data-ttu-id="b31c1-125">Contrassegno</span><span class="sxs-lookup"><span data-stu-id="b31c1-125">Flag</span></span>              | <span data-ttu-id="b31c1-126">Si applica a</span><span class="sxs-lookup"><span data-stu-id="b31c1-126">Applies to</span></span>                                                                                                                                                                                                                                                       |
    |-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="b31c1-127">\_modifica NFS</span><span class="sxs-lookup"><span data-stu-id="b31c1-127">NFS\_EDIT</span></span>         | <span data-ttu-id="b31c1-128">Controlli di modifica</span><span class="sxs-lookup"><span data-stu-id="b31c1-128">Edit controls</span></span>                                                                                                                                                                                                                                                    |
    | <span data-ttu-id="b31c1-129">NFS \_ statico</span><span class="sxs-lookup"><span data-stu-id="b31c1-129">NFS\_STATIC</span></span>       | <span data-ttu-id="b31c1-130">Controlli statici</span><span class="sxs-lookup"><span data-stu-id="b31c1-130">Static controls</span></span>                                                                                                                                                                                                                                                  |
    | <span data-ttu-id="b31c1-131">\_LISTCOMBO NFS</span><span class="sxs-lookup"><span data-stu-id="b31c1-131">NFS\_LISTCOMBO</span></span>    | <span data-ttu-id="b31c1-132">Controlli List, ComboBox, List-View e ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="b31c1-132">List, ComboBox, List-View, and ComboBoxEx controls</span></span>                                                                                                                                                                                                               |
    | <span data-ttu-id="b31c1-133">\_pulsante NFS</span><span class="sxs-lookup"><span data-stu-id="b31c1-133">NFS\_BUTTON</span></span>       | <span data-ttu-id="b31c1-134">Controlli pulsante</span><span class="sxs-lookup"><span data-stu-id="b31c1-134">Button controls</span></span>                                                                                                                                                                                                                                                  |
    | <span data-ttu-id="b31c1-135">NFS \_ tutto</span><span class="sxs-lookup"><span data-stu-id="b31c1-135">NFS\_ALL</span></span>          | <span data-ttu-id="b31c1-136">Tutti i controlli</span><span class="sxs-lookup"><span data-stu-id="b31c1-136">All controls</span></span>                                                                                                                                                                                                                                                     |
    | <span data-ttu-id="b31c1-137">\_USEFONTASSOC NFS</span><span class="sxs-lookup"><span data-stu-id="b31c1-137">NFS\_USEFONTASSOC</span></span> | <span data-ttu-id="b31c1-138">Piattaforma Asia orientale.</span><span class="sxs-lookup"><span data-stu-id="b31c1-138">East Asian platform.</span></span> <span data-ttu-id="b31c1-139">Il controllo Usa la funzionalità di associazione dei tipi di carattere anziché passare al tipo di carattere nativo.</span><span class="sxs-lookup"><span data-stu-id="b31c1-139">The control uses the font association feature instead of switching to the native font.</span></span> <span data-ttu-id="b31c1-140">Tutte le altre piattaforme lo ignorano.</span><span class="sxs-lookup"><span data-stu-id="b31c1-140">All other platforms ignore it.</span></span> <span data-ttu-id="b31c1-141">Questa funzionalità è deprecata per Windows Vista e non è supportata in COMCTL V6.</span><span class="sxs-lookup"><span data-stu-id="b31c1-141">This is deprecated for Windows Vista, and is not supported in comctl v6.</span></span> <span data-ttu-id="b31c1-142">Questo esiste in COMCTL V5 per motivi di compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="b31c1-142">This exists in comctl v5 for legacy reasons.</span></span> |

    

     

<span data-ttu-id="b31c1-143">Nell'esempio seguente viene illustrato come aggiungere un controllo del tipo di carattere nativo a uno script di risorsa.</span><span class="sxs-lookup"><span data-stu-id="b31c1-143">The following example illustrates how to add a native font control to a resource script.</span></span> <span data-ttu-id="b31c1-144">La finestra di dialogo modifica, elenco e casella combinata consente di visualizzare il testo utilizzando la lingua del sistema corrente.</span><span class="sxs-lookup"><span data-stu-id="b31c1-144">It causes the dialog box's edit, list, and combo box controls to display text using the current system language.</span></span>


```
CONTROL    "",-1,"NativeFontCtl",NFS_EDIT|NFS_LISTCOMBO,0,0,0,0
```



## <a name="related-topics"></a><span data-ttu-id="b31c1-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b31c1-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b31c1-146">Informazioni sui controlli comuni</span><span class="sxs-lookup"><span data-stu-id="b31c1-146">About Common Controls</span></span>](common-controls-intro.md)
</dt> </dl>

 

 





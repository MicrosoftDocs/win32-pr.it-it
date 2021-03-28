---
description: IContextMenu è l'interfaccia più potente ma anche più complessa da implementare.
ms.assetid: F0C1D60E-7A5A-4609-9136-F4E535E9F6F1
title: Come implementare l'interfaccia IContextMenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f251b9a64c3f401239eeb7c88286c016f399cc39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967443"
---
# <a name="how-to-implement-the-icontextmenu-interface"></a><span data-ttu-id="f48e4-103">Come implementare l'interfaccia IContextMenu</span><span class="sxs-lookup"><span data-stu-id="f48e4-103">How to Implement the IContextMenu Interface</span></span>

<span data-ttu-id="f48e4-104">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) è l'interfaccia più potente ma anche più complessa da implementare.</span><span class="sxs-lookup"><span data-stu-id="f48e4-104">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) is the most powerful but also the most complicated interface to implement.</span></span> <span data-ttu-id="f48e4-105">Si consiglia di implementare un verbo utilizzando uno dei metodi del verbo statico.</span><span class="sxs-lookup"><span data-stu-id="f48e4-105">We strongly recommend that you implement a verb by using one of the static verb methods.</span></span> <span data-ttu-id="f48e4-106">Per ulteriori informazioni, vedere [scelta di un metodo di menu di scelta rapida statico o dinamico](shortcut-choose-method.md).</span><span class="sxs-lookup"><span data-stu-id="f48e4-106">For more information, see [Choosing a Static or Dynamic Shortcut Menu Method](shortcut-choose-method.md).</span></span> <span data-ttu-id="f48e4-107">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) dispone di tre metodi, [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring), [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)e [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), descritti in dettaglio.</span><span class="sxs-lookup"><span data-stu-id="f48e4-107">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) has three methods, [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring), [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand), and [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), which are discussed here in detail.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="f48e4-108">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="f48e4-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="f48e4-109">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="f48e4-109">Technologies</span></span>

-   <span data-ttu-id="f48e4-110">C++</span><span class="sxs-lookup"><span data-stu-id="f48e4-110">C++</span></span>

### <a name="prerequisites"></a><span data-ttu-id="f48e4-111">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="f48e4-111">Prerequisites</span></span>

-   <span data-ttu-id="f48e4-112">Verbo statico</span><span class="sxs-lookup"><span data-stu-id="f48e4-112">Static Verb</span></span>
-   <span data-ttu-id="f48e4-113">Menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="f48e4-113">Shortcut Menu</span></span>

## <a name="instructions"></a><span data-ttu-id="f48e4-114">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="f48e4-114">Instructions</span></span>

### <a name="icontextmenugetcommandstring-method"></a><span data-ttu-id="f48e4-115">Metodo IContextMenu:: GetCommandString</span><span class="sxs-lookup"><span data-stu-id="f48e4-115">IContextMenu::GetCommandString Method</span></span>

<span data-ttu-id="f48e4-116">Il metodo [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) del gestore viene usato per restituire il nome canonico per un verbo.</span><span class="sxs-lookup"><span data-stu-id="f48e4-116">The handler's [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) method is used to return the canonical name for a verb.</span></span> <span data-ttu-id="f48e4-117">È facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f48e4-117">This method is optional.</span></span> <span data-ttu-id="f48e4-118">In Windows XP e nelle versioni precedenti di Windows, quando Esplora risorse dispone di una barra di stato, questo metodo viene utilizzato per recuperare il testo della Guida visualizzato nella barra di stato per una voce di menu.</span><span class="sxs-lookup"><span data-stu-id="f48e4-118">In Windows XP and earlier versions of Windows, when Windows Explorer has a Status bar, this method is used to retrieve the help text that is displayed in the Status bar for a menu item.</span></span>

<span data-ttu-id="f48e4-119">Il parametro *idCmd* include l'offset dell'identificatore del comando definito al momento della chiamata a [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) .</span><span class="sxs-lookup"><span data-stu-id="f48e4-119">The *idCmd* parameter holds the identifier offset of the command that was defined when [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) was called.</span></span> <span data-ttu-id="f48e4-120">Se viene richiesta una stringa della guida, *uFlags* verrà impostato su **cataloghi globali \_ HELPTEXTW**.</span><span class="sxs-lookup"><span data-stu-id="f48e4-120">If a help string is requested, *uFlags* will be set to **GCS\_HELPTEXTW**.</span></span> <span data-ttu-id="f48e4-121">Copiare la stringa della guida nel buffer *pszName* , eseguendone il cast in un **PWSTR**.</span><span class="sxs-lookup"><span data-stu-id="f48e4-121">Copy the help string to the *pszName* buffer, casting it to a **PWSTR**.</span></span> <span data-ttu-id="f48e4-122">La stringa del verbo viene richiesta impostando *uFlags* su **cataloghi globali \_ VERBW**.</span><span class="sxs-lookup"><span data-stu-id="f48e4-122">The verb string is requested by setting *uFlags* to **GCS\_VERBW**.</span></span> <span data-ttu-id="f48e4-123">Copiare la stringa appropriata in *pszName*, proprio come con la stringa della guida.</span><span class="sxs-lookup"><span data-stu-id="f48e4-123">Copy the appropriate string to *pszName*, just as with the help string.</span></span> <span data-ttu-id="f48e4-124">I flag **GC \_ validatea** e **GC \_ VALIDATEW** non vengono utilizzati dai gestori dei menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="f48e4-124">The **GCS\_VALIDATEA** and **GCS\_VALIDATEW** flags are not used by shortcut menu handlers.</span></span>

<span data-ttu-id="f48e4-125">Nell'esempio seguente viene illustrata un'implementazione semplice di [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) che corrisponde all'esempio di [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) fornito nella sezione relativa al [metodo IContextMenu:: QueryContextMenu](shortcut-menu-using-dynamic-verbs.md) di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="f48e4-125">The following example shows a simple implementation of [**GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) that corresponds to the [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) example given in the [IContextMenu::QueryContextMenu Method](shortcut-menu-using-dynamic-verbs.md) section of this topic.</span></span> <span data-ttu-id="f48e4-126">Poiché il gestore aggiunge solo una voce di menu, è possibile restituire un solo set di stringhe.</span><span class="sxs-lookup"><span data-stu-id="f48e4-126">Because the handler adds only one menu item, there is only one set of strings that can be returned.</span></span> <span data-ttu-id="f48e4-127">Il metodo verifica se *idCmd* è valido e, in caso contrario, restituisce la stringa richiesta.</span><span class="sxs-lookup"><span data-stu-id="f48e4-127">The method tests whether *idCmd* is valid and, if it is, returns the requested string.</span></span>

<span data-ttu-id="f48e4-128">La funzione [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) viene usata per copiare la stringa richiesta in *pszName* per assicurarsi che la stringa copiata non superi le dimensioni del buffer specificato da *cchName*.</span><span class="sxs-lookup"><span data-stu-id="f48e4-128">The [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) function is used to copy the requested string to *pszName* to ensure that the copied string does not exceed the size of the buffer specified by *cchName*.</span></span> <span data-ttu-id="f48e4-129">Questo esempio implementa il supporto solo per i valori Unicode di *uFlags*, in quanto solo quelli sono stati usati in Esplora risorse da Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="f48e4-129">This example implements support only for the Unicode values of *uFlags*, because only those have been used in Windows Explorer since Windows 2000.</span></span>


```
IFACEMETHODIMP CMenuExtension::GetCommandString(UINT idCommand, 
                                                UINT uFlags, 
                                                UINT *pReserved, 
                                                PSTR pszName, 
                                                UINT cchName)
{
    HRESULT hr = E_INVALIDARG;

    if (idCommand == IDM_DISPLAY)
    {
        switch (uFlags)
        {
            case GCS_HELPTEXTW:
                // Only useful for pre-Vista versions of Windows that 
                // have a Status bar.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"Display File Name");
                break; 

            case GCS_VERBW:
                // GCS_VERBW is an optional feature that enables a caller
                // to discover the canonical name for the verb that is passed in
                // through idCommand.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"DisplayFileName");
                break; 
        }
    }
    return hr;
}
```



### <a name="icontextmenuinvokecommand-method"></a><span data-ttu-id="f48e4-130">Metodo IContextMenu:: InvokeCommand</span><span class="sxs-lookup"><span data-stu-id="f48e4-130">IContextMenu::InvokeCommand Method</span></span>

<span data-ttu-id="f48e4-131">Questo metodo viene chiamato quando un utente fa clic su una voce di menu per indicare al gestore di eseguire il comando associato.</span><span class="sxs-lookup"><span data-stu-id="f48e4-131">This method is called when a user clicks a menu item to tell the handler to run the associated command.</span></span> <span data-ttu-id="f48e4-132">Il parametro *pici* punta a una struttura che contiene le informazioni necessarie per eseguire il comando.</span><span class="sxs-lookup"><span data-stu-id="f48e4-132">The *pici* parameter points to a structure that contains the information required to run the command.</span></span>

<span data-ttu-id="f48e4-133">Sebbene *pici* sia dichiarato in Shlobj. h come struttura [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) , in pratica spesso punta a una struttura [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) .</span><span class="sxs-lookup"><span data-stu-id="f48e4-133">Although *pici* is declared in Shlobj.h as a [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) structure, in practice it often points to a [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) structure.</span></span> <span data-ttu-id="f48e4-134">Questa struttura è una versione estesa di **CMINVOKECOMMANDINFO** e include diversi membri aggiuntivi che rendono possibile il passaggio di stringhe Unicode.</span><span class="sxs-lookup"><span data-stu-id="f48e4-134">This structure is an extended version of **CMINVOKECOMMANDINFO** and has several additional members that make it possible to pass Unicode strings.</span></span>

<span data-ttu-id="f48e4-135">Verificare il membro **cbSize** di *pici* per determinare la struttura passata.</span><span class="sxs-lookup"><span data-stu-id="f48e4-135">Check the **cbSize** member of *pici* to determine which structure was passed in.</span></span> <span data-ttu-id="f48e4-136">Se si tratta di una struttura [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) e per il membro **fmask** è impostato il flag **\_ \_ Unicode CMIC mask** , eseguire il cast di *pici* a **CMINVOKECOMMANDINFOEX**.</span><span class="sxs-lookup"><span data-stu-id="f48e4-136">If it is a [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) structure and the **fMask** member has the **CMIC\_MASK\_UNICODE** flag set, cast *pici* to **CMINVOKECOMMANDINFOEX**.</span></span> <span data-ttu-id="f48e4-137">Ciò consente all'applicazione di utilizzare le informazioni Unicode contenute negli ultimi cinque membri della struttura.</span><span class="sxs-lookup"><span data-stu-id="f48e4-137">This enables your application to use the Unicode information that is contained in the last five members of the structure.</span></span>

<span data-ttu-id="f48e4-138">Il membro **lpVerb** o **lpVerbW** della struttura viene usato per identificare il comando da eseguire.</span><span class="sxs-lookup"><span data-stu-id="f48e4-138">The structure's **lpVerb** or **lpVerbW** member is used to identify the command to be executed.</span></span> <span data-ttu-id="f48e4-139">I comandi sono identificati in uno dei due modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="f48e4-139">Commands are identified in one of the following two ways:</span></span>

-   <span data-ttu-id="f48e4-140">Dalla stringa del verbo del comando</span><span class="sxs-lookup"><span data-stu-id="f48e4-140">By the command's verb string</span></span>
-   <span data-ttu-id="f48e4-141">In base all'offset dell'identificatore del comando</span><span class="sxs-lookup"><span data-stu-id="f48e4-141">By the command's identifier offset</span></span>

<span data-ttu-id="f48e4-142">Per distinguere tra questi due casi, controllare la parola più ordinata di **lpVerb** per il caso ANSI o **lpVerbW** per il caso Unicode.</span><span class="sxs-lookup"><span data-stu-id="f48e4-142">To distinguish between these two cases, check the high-order word of **lpVerb** for the ANSI case or **lpVerbW** for the Unicode case.</span></span> <span data-ttu-id="f48e4-143">Se la parola più ordinata è diversa da zero, **lpVerb** o **lpVerbW** include una stringa verbo.</span><span class="sxs-lookup"><span data-stu-id="f48e4-143">If the high-order word is nonzero, **lpVerb** or **lpVerbW** holds a verb string.</span></span> <span data-ttu-id="f48e4-144">Se la parola più ordinata è pari a zero, l'offset del comando è nella parola più bassa dell'ordine di **lpVerb**.</span><span class="sxs-lookup"><span data-stu-id="f48e4-144">If the high-order word is zero, the command offset is in the low-order word of **lpVerb**.</span></span>

<span data-ttu-id="f48e4-145">Nell'esempio seguente viene illustrata un'implementazione semplice di [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) che corrisponde agli esempi [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) e [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) forniti prima e dopo questa sezione.</span><span class="sxs-lookup"><span data-stu-id="f48e4-145">The following example shows a simple implementation of [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) that corresponds to the [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) and [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) examples given before and after this section.</span></span> <span data-ttu-id="f48e4-146">Il metodo determina prima di tutto la struttura che viene passata.</span><span class="sxs-lookup"><span data-stu-id="f48e4-146">The method first determines which structure is being passed in.</span></span> <span data-ttu-id="f48e4-147">Quindi determina se il comando viene identificato in base al relativo offset o al relativo verbo.</span><span class="sxs-lookup"><span data-stu-id="f48e4-147">It then determines whether the command is identified by its offset or its verb.</span></span> <span data-ttu-id="f48e4-148">Se **lpVerb** o **lpVerbW** contiene un verbo o un offset valido, il metodo Visualizza una finestra di messaggio.</span><span class="sxs-lookup"><span data-stu-id="f48e4-148">If **lpVerb** or **lpVerbW** holds a valid verb or offset, the method displays a message box.</span></span>


```
STDMETHODIMP CShellExtension::InvokeCommand(LPCMINVOKECOMMANDINFO lpcmi)
{
    BOOL fEx = FALSE;
    BOOL fUnicode = FALSE;

    if(lpcmi->cbSize == sizeof(CMINVOKECOMMANDINFOEX))
    {
        fEx = TRUE;
        if((lpcmi->fMask & CMIC_MASK_UNICODE))
        {
            fUnicode = TRUE;
        }
    }

    if( !fUnicode && HIWORD(lpcmi->lpVerb))
    {
        if(StrCmpIA(lpcmi->lpVerb, m_pszVerb))
        {
            return E_FAIL;
        }
    }

    else if( fUnicode && HIWORD(((CMINVOKECOMMANDINFOEX *) lpcmi)->lpVerbW))
    {
        if(StrCmpIW(((CMINVOKECOMMANDINFOEX *)lpcmi)->lpVerbW, m_pwszVerb))
        {
            return E_FAIL;
        }
    }

    else if(LOWORD(lpcmi->lpVerb) != IDM_DISPLAY)
    {
        return E_FAIL;
    }

    else
    {
        MessageBox(lpcmi->hwnd,
                   "The File Name",
                   "File Name",
                   MB_OK|MB_ICONINFORMATION);
    }

    return S_OK;
}
```



### <a name="icontextmenuquerycontextmenu-method"></a><span data-ttu-id="f48e4-149">Metodo IContextMenu:: QueryContextMenu</span><span class="sxs-lookup"><span data-stu-id="f48e4-149">IContextMenu::QueryContextMenu Method</span></span>

<span data-ttu-id="f48e4-150">La shell chiama [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) per abilitare il gestore del menu di scelta rapida per aggiungere le voci di menu al menu.</span><span class="sxs-lookup"><span data-stu-id="f48e4-150">The Shell calls [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) to enable the shortcut menu handler to add its menu items to the menu.</span></span> <span data-ttu-id="f48e4-151">Passa l'handle **HMENU** nel parametro *HMENU* .</span><span class="sxs-lookup"><span data-stu-id="f48e4-151">It passes in the **HMENU** handle in the *hmenu* parameter.</span></span> <span data-ttu-id="f48e4-152">Il parametro *indexMenu* è impostato sull'indice da utilizzare per la prima voce di menu da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="f48e4-152">The *indexMenu* parameter is set to the index to be used for the first menu item that is to be added.</span></span>

<span data-ttu-id="f48e4-153">Tutte le voci di menu aggiunte dal gestore devono contenere identificatori che rientrano tra i valori nei parametri *idCmdFirst* e *idCmdLast* .</span><span class="sxs-lookup"><span data-stu-id="f48e4-153">Any menu items that are added by the handler must have identifiers that fall between the values in the *idCmdFirst* and *idCmdLast* parameters.</span></span> <span data-ttu-id="f48e4-154">In genere, il primo identificatore del comando è impostato su *idCmdFirst*, che viene incrementato di uno (1) per ogni comando aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="f48e4-154">Typically, the first command identifier is set to *idCmdFirst*, which is incremented by one (1) for each additional command.</span></span> <span data-ttu-id="f48e4-155">Questa procedura consente di evitare il superamento di *idCmdLast* e massimizza il numero di identificatori disponibili nel caso in cui la shell chiami più di un gestore.</span><span class="sxs-lookup"><span data-stu-id="f48e4-155">This practice helps you to avoid exceeding *idCmdLast* and maximizes the number of available identifiers in case the Shell calls more than one handler.</span></span>

<span data-ttu-id="f48e4-156">L' *offset del comando* di un identificatore di elemento è la differenza tra l'identificatore e il valore in *idCmdFirst*.</span><span class="sxs-lookup"><span data-stu-id="f48e4-156">An item identifier's *command offset* is the difference between the identifier and the value in *idCmdFirst*.</span></span> <span data-ttu-id="f48e4-157">Archiviare l'offset di ogni elemento aggiunto dal gestore al menu di scelta rapida, perché la shell potrebbe utilizzare l'offset per identificare l'elemento se successivamente chiama [**IContextMenu:: GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) o [**IContextMenu:: InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span><span class="sxs-lookup"><span data-stu-id="f48e4-157">Store the offset of each item that your handler adds to the shortcut menu, because the Shell might use the offset to identify the item if it subsequently calls [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) or [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span></span>

<span data-ttu-id="f48e4-158">È inoltre consigliabile assegnare un [verbo](launch.md) a ogni comando aggiunto.</span><span class="sxs-lookup"><span data-stu-id="f48e4-158">You should also assign a [verb](launch.md) to each command that you add.</span></span> <span data-ttu-id="f48e4-159">Un verbo è una stringa che può essere utilizzata al posto dell'offset per identificare il comando quando viene chiamato [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) .</span><span class="sxs-lookup"><span data-stu-id="f48e4-159">A verb is a string that can be used instead of the offset to identify the command when [**InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) is called.</span></span> <span data-ttu-id="f48e4-160">Viene anche usato da funzioni come [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) per eseguire i comandi del menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="f48e4-160">It is also used by functions such as [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to execute shortcut menu commands.</span></span>

<span data-ttu-id="f48e4-161">Sono disponibili tre flag che possono essere passati tramite il parametro *uFlags* rilevanti per i gestori dei menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="f48e4-161">There are three flags that can be passed in through the *uFlags* parameter that are relevant to shortcut menu handlers.</span></span> <span data-ttu-id="f48e4-162">descritti nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f48e4-162">They are described in the following table.</span></span>



| <span data-ttu-id="f48e4-163">Flag</span><span class="sxs-lookup"><span data-stu-id="f48e4-163">Flag</span></span>             | <span data-ttu-id="f48e4-164">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f48e4-164">Description</span></span>                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f48e4-165">DEFAULTONLY di CMF \_</span><span class="sxs-lookup"><span data-stu-id="f48e4-165">CMF\_DEFAULTONLY</span></span> | <span data-ttu-id="f48e4-166">L'utente ha selezionato il comando predefinito, in genere facendo doppio clic sull'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f48e4-166">The user has selected the default command, usually by double-clicking the object.</span></span> <span data-ttu-id="f48e4-167">[**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) deve restituire il controllo alla shell senza modificare il menu.</span><span class="sxs-lookup"><span data-stu-id="f48e4-167">[**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) should return control to the Shell without modifying the menu.</span></span> |
| <span data-ttu-id="f48e4-168">CMF \_ NOdefault</span><span class="sxs-lookup"><span data-stu-id="f48e4-168">CMF\_NODEFAULT</span></span>   | <span data-ttu-id="f48e4-169">Nessun elemento nel menu deve essere l'elemento predefinito.</span><span class="sxs-lookup"><span data-stu-id="f48e4-169">No item in the menu should be the default item.</span></span> <span data-ttu-id="f48e4-170">Il metodo deve aggiungere i comandi al menu.</span><span class="sxs-lookup"><span data-stu-id="f48e4-170">The method should add its commands to the menu.</span></span>                                                                                                                          |
| <span data-ttu-id="f48e4-171">\_normale CMF</span><span class="sxs-lookup"><span data-stu-id="f48e4-171">CMF\_NORMAL</span></span>      | <span data-ttu-id="f48e4-172">Il menu di scelta rapida verrà visualizzato normalmente.</span><span class="sxs-lookup"><span data-stu-id="f48e4-172">The shortcut menu will be displayed normally.</span></span> <span data-ttu-id="f48e4-173">Il metodo deve aggiungere i comandi al menu.</span><span class="sxs-lookup"><span data-stu-id="f48e4-173">The method should add its commands to the menu.</span></span>                                                                                                                            |



 

<span data-ttu-id="f48e4-174">Usare [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) o [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) per aggiungere voci di menu all'elenco.</span><span class="sxs-lookup"><span data-stu-id="f48e4-174">Use either [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) or [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) to add menu items to the list.</span></span> <span data-ttu-id="f48e4-175">Restituire quindi un valore **HRESULT** con gravità impostato su gravità \_ riuscita.</span><span class="sxs-lookup"><span data-stu-id="f48e4-175">Then return an **HRESULT** value with the severity set to SEVERITY\_SUCCESS.</span></span> <span data-ttu-id="f48e4-176">Impostare il valore del codice sull'offset dell'identificatore di comando più grande assegnato, più uno (1).</span><span class="sxs-lookup"><span data-stu-id="f48e4-176">Set the code value to the offset of the largest command identifier that was assigned, plus one (1).</span></span> <span data-ttu-id="f48e4-177">Si supponga, ad esempio, che *idCmdFirst* sia impostato su 5 e che vengano aggiunti tre elementi al menu con gli identificatori dei comandi 5, 7 e 8.</span><span class="sxs-lookup"><span data-stu-id="f48e4-177">For example, assume that *idCmdFirst* is set to 5 and you add three items to the menu with command identifiers of 5, 7, and 8.</span></span> <span data-ttu-id="f48e4-178">Il valore restituito deve essere \_ HRESULT (gravità \_ riuscita, 0, 8 + 1).</span><span class="sxs-lookup"><span data-stu-id="f48e4-178">The return value should be MAKE\_HRESULT(SEVERITY\_SUCCESS, 0, 8 + 1).</span></span>

<span data-ttu-id="f48e4-179">Nell'esempio seguente viene illustrata un'implementazione semplice di [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) che inserisce un singolo comando.</span><span class="sxs-lookup"><span data-stu-id="f48e4-179">The following example shows a simple implementation of [**QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) that inserts a single command.</span></span> <span data-ttu-id="f48e4-180">L'offset dell'identificatore per il comando è IDM \_ display, che è impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="f48e4-180">The identifier offset for the command is IDM\_DISPLAY, which is set to zero.</span></span> <span data-ttu-id="f48e4-181">Le variabili **m \_ pszVerb** e **m \_ pwszVerb** sono variabili private utilizzate per archiviare la stringa del verbo indipendente dal linguaggio associata nei formati ANSI e Unicode.</span><span class="sxs-lookup"><span data-stu-id="f48e4-181">The **m\_pszVerb** and **m\_pwszVerb** variables are private variables that are used to store the associated language-independent verb string in both ANSI and Unicode formats.</span></span>


```
#define IDM_DISPLAY 0

STDMETHODIMP CMenuExtension::QueryContextMenu(HMENU hMenu,
                                              UINT indexMenu,
                                              UINT idCmdFirst,
                                              UINT idCmdLast,
                                              UINT uFlags)
{
    HRESULT hr;
    
    if(!(CMF_DEFAULTONLY & uFlags))
    {
        InsertMenu(hMenu, 
                   indexMenu, 
                   MF_STRING | MF_BYPOSITION, 
                   idCmdFirst + IDM_DISPLAY, 
                   "&Display File Name");

    
        
        hr = StringCbCopyA(m_pszVerb, sizeof(m_pszVerb), "display");
        hr = StringCbCopyW(m_pwszVerb, sizeof(m_pwszVerb), L"display");

        return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(IDM_DISPLAY + 1));
    }

    return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(0));}
```



## <a name="remarks"></a><span data-ttu-id="f48e4-182">Commenti</span><span class="sxs-lookup"><span data-stu-id="f48e4-182">Remarks</span></span>

<span data-ttu-id="f48e4-183">Per altre attività di implementazione di verbi, vedere [creazione di gestori di menu di scelta rapida](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="f48e4-183">For other verb implementation tasks, see [Creating Shortcut Menu Handlers](context-menu-handlers.md).</span></span>

 

 

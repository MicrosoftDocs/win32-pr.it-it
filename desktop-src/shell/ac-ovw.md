---
description: Il completamento automatico espande le stringhe che sono state immesse parzialmente in un controllo di modifica in stringhe complete.
title: Utilizzo di completamento automatico
ms.topic: article
ms.date: 05/31/2018
ms.assetid: b990395b-fc10-48f9-a718-7cc006e37eb7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: fbbf0c53fc1b26002d1b46a9a6a6f67cd15e3ead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977423"
---
# <a name="using-autocomplete"></a><span data-ttu-id="91ced-103">Utilizzo di completamento automatico</span><span class="sxs-lookup"><span data-stu-id="91ced-103">Using Autocomplete</span></span>

<span data-ttu-id="91ced-104">Il completamento automatico espande le stringhe che sono state immesse parzialmente in un [controllo di modifica](/windows/desktop/Controls/edit-controls) in stringhe complete.</span><span class="sxs-lookup"><span data-stu-id="91ced-104">Autocompletion expands strings that have been partially entered in an [edit control](/windows/desktop/Controls/edit-controls) into complete strings.</span></span> <span data-ttu-id="91ced-105">Ad esempio, quando un utente inizia a immettere un URL nel controllo di modifica degli indirizzi incorporato nella barra degli strumenti di Windows Internet Explorer, il completamento automatico espande la stringa in una o più opzioni URL complete coerenti con la stringa parziale esistente.</span><span class="sxs-lookup"><span data-stu-id="91ced-105">For example, when a user starts to enter a URL in the Address edit control that is embedded in the Windows Internet Explorer toolbar, autocompletion expands the string into one or more complete URL options that are consistent with the existing partial string.</span></span> <span data-ttu-id="91ced-106">Una stringa URL parziale, ad esempio "MIC", può essere espansa in " https://www.microsoft.com " o " https://www.microsoft.com/windows ".</span><span class="sxs-lookup"><span data-stu-id="91ced-106">A partial URL string such as "mic" might be expanded to "https://www.microsoft.com" or "https://www.microsoft.com/windows".</span></span> <span data-ttu-id="91ced-107">Il completamento automatico viene in genere usato con i controlli di modifica o con controlli che dispongono di un controllo di modifica incorporato, ad esempio il controllo [ComboBoxEx](/windows/desktop/Controls/comboboxex-control-reference) .</span><span class="sxs-lookup"><span data-stu-id="91ced-107">Autocompletion is typically used with edit controls or with controls that have an embedded edit control, such as the [ComboBoxEx](/windows/desktop/Controls/comboboxex-control-reference) control.</span></span>

## <a name="adding-autocomplete-functionality-to-your-application"></a><span data-ttu-id="91ced-108">Aggiunta della funzionalità di completamento automatico all'applicazione</span><span class="sxs-lookup"><span data-stu-id="91ced-108">Adding Autocomplete Functionality to Your Application</span></span>

<span data-ttu-id="91ced-109">Un'applicazione può aggiungere la funzionalità di completamento automatico a un controllo di modifica in due modi:</span><span class="sxs-lookup"><span data-stu-id="91ced-109">An application can add autocomplete functionality to an edit control in two ways:</span></span>

-   <span data-ttu-id="91ced-110">[**SHAutoComplete**](/windows/desktop/api/shlwapi/nf-shlwapi-shautocomplete) è una funzione semplice che consente di completare in modo automatico un percorso o un URL di file.</span><span class="sxs-lookup"><span data-stu-id="91ced-110">[**SHAutoComplete**](/windows/desktop/api/shlwapi/nf-shlwapi-shautocomplete) is a simple function that can autocomplete a file path or URL.</span></span>
-   <span data-ttu-id="91ced-111">L'interfaccia [**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete) viene esposta dall'oggetto di completamento automatico (CLSID AutoComplete \_ ).</span><span class="sxs-lookup"><span data-stu-id="91ced-111">[**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete) interface is exposed by the autocomplete object (CLSID\_AutoComplete).</span></span> <span data-ttu-id="91ced-112">Consente alle applicazioni di inizializzare, abilitare e disabilitare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="91ced-112">It allows applications to initialize, enable, and disable the object.</span></span> <span data-ttu-id="91ced-113">**IAutoComplete** consente un maggiore controllo sulle origini di completamento automatico, inclusa la possibilità di aggiungere un'origine personalizzata.</span><span class="sxs-lookup"><span data-stu-id="91ced-113">**IAutoComplete** allows more control over autocomplete sources, including the ability to add a custom source.</span></span> <span data-ttu-id="91ced-114">Nella parte restante di questo argomento viene illustrato l'uso di **IAutoComplete**.</span><span class="sxs-lookup"><span data-stu-id="91ced-114">The remainder of this topic discusses the use of **IAutoComplete**.</span></span> <span data-ttu-id="91ced-115">Vedere [come abilitare il completamento automatico manualmente](how-to-enable-autocomplete-manually.md) per esempi di utilizzo specifici.</span><span class="sxs-lookup"><span data-stu-id="91ced-115">See [How To Enable Autocomplete Manually](how-to-enable-autocomplete-manually.md) for specific usage examples.</span></span>

## <a name="autocomplete-modes"></a><span data-ttu-id="91ced-116">Modalità di completamento automatico</span><span class="sxs-lookup"><span data-stu-id="91ced-116">Autocomplete Modes</span></span>

<span data-ttu-id="91ced-117">Quando si usa [**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete), il completamento automatico consente di visualizzare la stringa completata in due modalità: AutoAppend e suggerimenti automatici.</span><span class="sxs-lookup"><span data-stu-id="91ced-117">When using [**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete), autocompletion can display the completed string in two modes: autoappend and autosuggest.</span></span> <span data-ttu-id="91ced-118">Le modalità sono indipendenti. è possibile abilitare uno o entrambi.</span><span class="sxs-lookup"><span data-stu-id="91ced-118">The modes are independent; you can enable either or both.</span></span> <span data-ttu-id="91ced-119">Per specificare la modalità, chiamare [**IAutoComplete2:: SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions).</span><span class="sxs-lookup"><span data-stu-id="91ced-119">To specify the mode, call [**IAutoComplete2::SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions).</span></span>

<dl> <dt>

<span data-ttu-id="91ced-120"><span id="Autoappend"></span><span id="autoappend"></span><span id="AUTOAPPEND"></span>Accodamento automatica</span><span class="sxs-lookup"><span data-stu-id="91ced-120"><span id="Autoappend"></span><span id="autoappend"></span><span id="AUTOAPPEND"></span>Autoappend</span></span>
</dt> <dd>

<span data-ttu-id="91ced-121">In modalità autoappenda, il completamento automatico aggiunge il resto della stringa candidata più probabile ai caratteri esistenti, evidenziando i caratteri accodati.</span><span class="sxs-lookup"><span data-stu-id="91ced-121">In autoappend mode, autocompletion appends the remainder of the most likely candidate string to the existing characters, highlighting the appended characters.</span></span> <span data-ttu-id="91ced-122">Se l'utente continua a immettere caratteri, viene aggiunto alla stringa parziale esistente.</span><span class="sxs-lookup"><span data-stu-id="91ced-122">If the user continues to enter characters, they are added to the existing partial string.</span></span> <span data-ttu-id="91ced-123">Se l'utente aggiunge un carattere identico al carattere evidenziato successivo, l'evidenziazione per tale carattere viene disattivata.</span><span class="sxs-lookup"><span data-stu-id="91ced-123">If the user adds a character that is identical to the next highlighted character, the highlighting for that character is turned off.</span></span> <span data-ttu-id="91ced-124">I caratteri rimanenti verranno comunque evidenziati.</span><span class="sxs-lookup"><span data-stu-id="91ced-124">The remaining characters will still be highlighted.</span></span> <span data-ttu-id="91ced-125">Se l'utente aggiunge un carattere che non corrisponde al carattere evidenziato successivo, il completamento automatico tenta di generare una nuova stringa candidata basata sulla stringa parziale più grande e aggiunge il resto della nuova stringa candidata alla stringa parziale corrente.</span><span class="sxs-lookup"><span data-stu-id="91ced-125">If the user adds a character that does not match the next highlighted character, autocompletion attempts to generate a new candidate string based on the larger partial string and appends the remainder of the new candidate string to the current partial string.</span></span> <span data-ttu-id="91ced-126">Se non è possibile trovare una stringa candidata, vengono visualizzati solo i caratteri tipizzati e la casella di modifica si comporta come se fosse senza completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="91ced-126">If no candidate string can be found, only the typed characters appear and the edit box behaves as it would without autocompletion.</span></span> <span data-ttu-id="91ced-127">Questo processo continua fino a quando l'utente non accetta una stringa.</span><span class="sxs-lookup"><span data-stu-id="91ced-127">This process continues until the user accepts a string.</span></span>

</dd> <dt>

<span data-ttu-id="91ced-128"><span id="Autosuggest"></span><span id="autosuggest"></span><span id="AUTOSUGGEST"></span>Suggerimenti automatici</span><span class="sxs-lookup"><span data-stu-id="91ced-128"><span id="Autosuggest"></span><span id="autosuggest"></span><span id="AUTOSUGGEST"></span>Autosuggest</span></span>
</dt> <dd>

<span data-ttu-id="91ced-129">In modalità di suggerimento automatico, completamento automatico Visualizza un elenco a discesa con una o più stringhe complete suggerite sotto il controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="91ced-129">In autosuggest mode, autocompletion displays a drop-down list, with one or more suggested complete strings, beneath the edit control.</span></span> <span data-ttu-id="91ced-130">L'utente può selezionare una delle stringhe suggerite o continuare a digitare.</span><span class="sxs-lookup"><span data-stu-id="91ced-130">The user can select one of the suggested strings or continue typing.</span></span> <span data-ttu-id="91ced-131">Con l'avanzamento della digitazione, l'elenco a discesa potrebbe essere modificato in base alla stringa parziale corrente.</span><span class="sxs-lookup"><span data-stu-id="91ced-131">As typing progresses, the drop-down list might be modified based on the current partial string.</span></span> <span data-ttu-id="91ced-132">Se si imposta il \_ flag di ricerca ACO in [**IAutoComplete2:: SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions), AutoComplete fornisce un'opzione nella parte inferiore dell'elenco a discesa per cercare la stringa parziale corrente.</span><span class="sxs-lookup"><span data-stu-id="91ced-132">If you set the ACO\_SEARCH flag in [**IAutoComplete2::SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions), autocomplete provides an option, at the bottom of the drop-down list, to search for the current partial string.</span></span> <span data-ttu-id="91ced-133">Questa opzione viene visualizzata anche se non sono presenti stringhe suggerite.</span><span class="sxs-lookup"><span data-stu-id="91ced-133">This option is displayed even if there are no suggested strings.</span></span> <span data-ttu-id="91ced-134">Se l'utente seleziona l'opzione di ricerca, l'applicazione deve avviare un motore di ricerca per assistere l'utente.</span><span class="sxs-lookup"><span data-stu-id="91ced-134">If the user selects the search option, your application should launch a search engine to assist the user.</span></span>

</dd> </dl>

## <a name="using-predefined-autocomplete-sources"></a><span data-ttu-id="91ced-135">Utilizzo di origini di completamento automatico predefinite</span><span class="sxs-lookup"><span data-stu-id="91ced-135">Using Predefined Autocomplete Sources</span></span>

<span data-ttu-id="91ced-136">Il completamento automatico dipende dalla presenza di un'origine che le fornisce stringhe per la corrispondenza con la stringa parziale dell'utente.</span><span class="sxs-lookup"><span data-stu-id="91ced-136">Autocompletion depends on having a source that provides it with strings to match against the user's partial string.</span></span> <span data-ttu-id="91ced-137">È possibile scegliere di fornire un'origine di completamento automatico personalizzata, ma molte delle origini più comuni sono fornite dal sistema.</span><span class="sxs-lookup"><span data-stu-id="91ced-137">You have the option of providing a custom autocomplete source, but several of the most common sources are provided by the system.</span></span>

<dl> <dt>

<span data-ttu-id="91ced-138"><span id="CLSID_ACLHistory"></span><span id="clsid_aclhistory"></span><span id="CLSID_ACLHISTORY"></span>\_ACLHISTORY CLSID</span><span class="sxs-lookup"><span data-stu-id="91ced-138"><span id="CLSID_ACLHistory"></span><span id="clsid_aclhistory"></span><span id="CLSID_ACLHISTORY"></span>CLSID\_ACLHistory</span></span>
</dt> <dd>

<span data-ttu-id="91ced-139">Origine di completamento automatico che corrisponde all'elenco di URL nell'elenco della cronologia dell'utente.</span><span class="sxs-lookup"><span data-stu-id="91ced-139">An autocomplete source that matches against the URL list in the user's History list.</span></span>

</dd> <dt>

<span data-ttu-id="91ced-140"><span id="CLSID_ACLMRU"></span><span id="clsid_aclmru"></span>\_ACLMRU CLSID</span><span class="sxs-lookup"><span data-stu-id="91ced-140"><span id="CLSID_ACLMRU"></span><span id="clsid_aclmru"></span>CLSID\_ACLMRU</span></span>
</dt> <dd>

<span data-ttu-id="91ced-141">Origine di completamento automatico che corrisponde all'elenco di URL nell'elenco degli ultimi dati utilizzati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="91ced-141">An autocomplete source that matches against the URL list in the user's Recently Used list.</span></span>

</dd> <dt>

<span data-ttu-id="91ced-142"><span id="CLSID_ACListISF"></span><span id="clsid_aclistisf"></span><span id="CLSID_ACLISTISF"></span>\_ACLISTISF CLSID</span><span class="sxs-lookup"><span data-stu-id="91ced-142"><span id="CLSID_ACListISF"></span><span id="clsid_aclistisf"></span><span id="CLSID_ACLISTISF"></span>CLSID\_ACListISF</span></span>
</dt> <dd>

<span data-ttu-id="91ced-143">Un'origine di completamento automatico che corrisponde agli elementi nello spazio dei nomi della shell, ovvero i file nel computer dell'utente e gli elementi nelle cartelle virtuali, ad esempio il pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="91ced-143">An autocomplete source that matches against items in the Shell namespace: files on the user's computer as well as items in virtual folders such as Control Panel.</span></span>

</dd> </dl>

<span data-ttu-id="91ced-144">In alcuni casi, anziché immediatamente liberare le risorse, potrebbe essere necessario mantenere i puntatori di interfaccia ai vari oggetti interessati dal completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="91ced-144">There are occasions when, rather than immediately freeing the resources, you might want to retain the interface pointers to the various objects involved in autocomplete.</span></span> <span data-ttu-id="91ced-145">In particolare, questa operazione viene eseguita quando si desidera modificare dinamicamente il comportamento di completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="91ced-145">In particular, this is done when you want to adjust the autocomplete behavior dynamically.</span></span> <span data-ttu-id="91ced-146">L'istanza più comune di questo problema si verifica quando si usa l' \_ oggetto CLSID ACListISF, che esegue il completamento automatico dallo spazio dei nomi della shell e ha l'opzione ([**ACLO \_ CURRENTDIR**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2)) dell'enumerazione dalla directory corrente.</span><span class="sxs-lookup"><span data-stu-id="91ced-146">The most common instance of this occurs when using the CLSID\_ACListISF object, which autocompletes from the Shell namespace and has the option ([**ACLO\_CURRENTDIR**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2)) of enumerating from the current directory as well.</span></span> <span data-ttu-id="91ced-147">Ad esempio, quando si passa a una nuova cartella, Internet Explorer modifica la directory corrente della barra degli indirizzi e pertanto le impostazioni devono essere modificate in modo dinamico.</span><span class="sxs-lookup"><span data-stu-id="91ced-147">For example, when you navigate to a new folder, Internet Explorer changes the Address bar's current directory and therefore the settings need to be changed dynamically.</span></span> <span data-ttu-id="91ced-148">Esistono due modi per specificare la directory che l' \_ oggetto ACLISTISF CLSID deve considerare come la directory corrente:</span><span class="sxs-lookup"><span data-stu-id="91ced-148">There are two ways to specify the directory that the CLSID\_ACListISF object should treat as the current directory:</span></span>

-   <span data-ttu-id="91ced-149">[**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) specifica la directory tramite un oggetto [**ItemId**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist).</span><span class="sxs-lookup"><span data-stu-id="91ced-149">[**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) specifies the directory through an [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist).</span></span>
-   <span data-ttu-id="91ced-150">[**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) specifica la directory tramite una stringa di percorso.</span><span class="sxs-lookup"><span data-stu-id="91ced-150">[**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) specifies the directory through a path string.</span></span>

<span data-ttu-id="91ced-151">Nell'esempio seguente si supponga che **PAL** sia un puntatore all'interfaccia [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) di un \_ oggetto ACListISF CLSID:</span><span class="sxs-lookup"><span data-stu-id="91ced-151">In the following, assume that **pal** is a pointer to the [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) interface of a CLSID\_ACListISF object:</span></span>

-   <span data-ttu-id="91ced-152">Uso di [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder):</span><span class="sxs-lookup"><span data-stu-id="91ced-152">Using [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder):</span></span>

    <span data-ttu-id="91ced-153">Per indicare all' \_ oggetto CLSID ACListISF che un elemento [**ItemId**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) specifico deve essere considerato come la directory corrente, è possibile usare l'interfaccia [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="91ced-153">To tell the CLSID\_ACListISF object that a particular [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) should be treated as the current directory, you can use the object's [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) interface.</span></span> <span data-ttu-id="91ced-154">Poiché un oggetto **ItemId** può fare riferimento a una cartella virtuale, questo metodo è più flessibile rispetto all'uso di [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory).</span><span class="sxs-lookup"><span data-stu-id="91ced-154">Since an **ITEMIDLIST** can refer to a virtual folder, this method is more flexible than using [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory).</span></span>

    <span data-ttu-id="91ced-155">Si noti che negli esempi seguenti viene usato creato un modello QueryInterface, che consente un elenco di parametri semplificato.</span><span class="sxs-lookup"><span data-stu-id="91ced-155">Note that the following examples use the templatized QueryInterface, which allows for a simplified parameter list.</span></span>

    ```C++
    IPersistFolder *ppf;

    hr = pal2->QueryInterface(IID_PPV_ARGS(&ppf));   
    if (SUCCEEDED(hr))
    {
        hr = ppf->Initialize(pidlCurrentDirectory);
        ppf->Release();
    }
    ```

    

-   <span data-ttu-id="91ced-156">Uso di [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory):</span><span class="sxs-lookup"><span data-stu-id="91ced-156">Using [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory):</span></span>

    <span data-ttu-id="91ced-157">Per assegnare all' \_ oggetto CLSID ACListISF un percorso come directory corrente, è possibile usare l'interfaccia [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="91ced-157">To give the CLSID\_ACListISF object a path as the current directory, you can use the object's [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) interface.</span></span>

    ```C++
    WCHAR pwszDirectory[MAX_PATH] = L"C:\\Program Files";
    ICurrentWorkingDirectory *pcwd;

    hr = pal2->QueryInterface(IID_PPV_ARGS(&pcwd));    
    if (SUCCEEDED(hr))
    {
        hr = pcwd->SetDirectory(pwszDirectory);
        pcwd->Release();
    }
    ```

    

 

 

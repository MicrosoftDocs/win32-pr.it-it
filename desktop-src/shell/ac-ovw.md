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
# <a name="using-autocomplete"></a>Utilizzo di completamento automatico

Il completamento automatico espande le stringhe che sono state immesse parzialmente in un [controllo di modifica](/windows/desktop/Controls/edit-controls) in stringhe complete. Ad esempio, quando un utente inizia a immettere un URL nel controllo di modifica degli indirizzi incorporato nella barra degli strumenti di Windows Internet Explorer, il completamento automatico espande la stringa in una o più opzioni URL complete coerenti con la stringa parziale esistente. Una stringa URL parziale, ad esempio "MIC", può essere espansa in " https://www.microsoft.com " o " https://www.microsoft.com/windows ". Il completamento automatico viene in genere usato con i controlli di modifica o con controlli che dispongono di un controllo di modifica incorporato, ad esempio il controllo [ComboBoxEx](/windows/desktop/Controls/comboboxex-control-reference) .

## <a name="adding-autocomplete-functionality-to-your-application"></a>Aggiunta della funzionalità di completamento automatico all'applicazione

Un'applicazione può aggiungere la funzionalità di completamento automatico a un controllo di modifica in due modi:

-   [**SHAutoComplete**](/windows/desktop/api/shlwapi/nf-shlwapi-shautocomplete) è una funzione semplice che consente di completare in modo automatico un percorso o un URL di file.
-   L'interfaccia [**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete) viene esposta dall'oggetto di completamento automatico (CLSID AutoComplete \_ ). Consente alle applicazioni di inizializzare, abilitare e disabilitare l'oggetto. **IAutoComplete** consente un maggiore controllo sulle origini di completamento automatico, inclusa la possibilità di aggiungere un'origine personalizzata. Nella parte restante di questo argomento viene illustrato l'uso di **IAutoComplete**. Vedere [come abilitare il completamento automatico manualmente](how-to-enable-autocomplete-manually.md) per esempi di utilizzo specifici.

## <a name="autocomplete-modes"></a>Modalità di completamento automatico

Quando si usa [**IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete), il completamento automatico consente di visualizzare la stringa completata in due modalità: AutoAppend e suggerimenti automatici. Le modalità sono indipendenti. è possibile abilitare uno o entrambi. Per specificare la modalità, chiamare [**IAutoComplete2:: SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions).

<dl> <dt>

<span id="Autoappend"></span><span id="autoappend"></span><span id="AUTOAPPEND"></span>Accodamento automatica
</dt> <dd>

In modalità autoappenda, il completamento automatico aggiunge il resto della stringa candidata più probabile ai caratteri esistenti, evidenziando i caratteri accodati. Se l'utente continua a immettere caratteri, viene aggiunto alla stringa parziale esistente. Se l'utente aggiunge un carattere identico al carattere evidenziato successivo, l'evidenziazione per tale carattere viene disattivata. I caratteri rimanenti verranno comunque evidenziati. Se l'utente aggiunge un carattere che non corrisponde al carattere evidenziato successivo, il completamento automatico tenta di generare una nuova stringa candidata basata sulla stringa parziale più grande e aggiunge il resto della nuova stringa candidata alla stringa parziale corrente. Se non è possibile trovare una stringa candidata, vengono visualizzati solo i caratteri tipizzati e la casella di modifica si comporta come se fosse senza completamento automatico. Questo processo continua fino a quando l'utente non accetta una stringa.

</dd> <dt>

<span id="Autosuggest"></span><span id="autosuggest"></span><span id="AUTOSUGGEST"></span>Suggerimenti automatici
</dt> <dd>

In modalità di suggerimento automatico, completamento automatico Visualizza un elenco a discesa con una o più stringhe complete suggerite sotto il controllo di modifica. L'utente può selezionare una delle stringhe suggerite o continuare a digitare. Con l'avanzamento della digitazione, l'elenco a discesa potrebbe essere modificato in base alla stringa parziale corrente. Se si imposta il \_ flag di ricerca ACO in [**IAutoComplete2:: SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions), AutoComplete fornisce un'opzione nella parte inferiore dell'elenco a discesa per cercare la stringa parziale corrente. Questa opzione viene visualizzata anche se non sono presenti stringhe suggerite. Se l'utente seleziona l'opzione di ricerca, l'applicazione deve avviare un motore di ricerca per assistere l'utente.

</dd> </dl>

## <a name="using-predefined-autocomplete-sources"></a>Utilizzo di origini di completamento automatico predefinite

Il completamento automatico dipende dalla presenza di un'origine che le fornisce stringhe per la corrispondenza con la stringa parziale dell'utente. È possibile scegliere di fornire un'origine di completamento automatico personalizzata, ma molte delle origini più comuni sono fornite dal sistema.

<dl> <dt>

<span id="CLSID_ACLHistory"></span><span id="clsid_aclhistory"></span><span id="CLSID_ACLHISTORY"></span>\_ACLHISTORY CLSID
</dt> <dd>

Origine di completamento automatico che corrisponde all'elenco di URL nell'elenco della cronologia dell'utente.

</dd> <dt>

<span id="CLSID_ACLMRU"></span><span id="clsid_aclmru"></span>\_ACLMRU CLSID
</dt> <dd>

Origine di completamento automatico che corrisponde all'elenco di URL nell'elenco degli ultimi dati utilizzati dall'utente.

</dd> <dt>

<span id="CLSID_ACListISF"></span><span id="clsid_aclistisf"></span><span id="CLSID_ACLISTISF"></span>\_ACLISTISF CLSID
</dt> <dd>

Un'origine di completamento automatico che corrisponde agli elementi nello spazio dei nomi della shell, ovvero i file nel computer dell'utente e gli elementi nelle cartelle virtuali, ad esempio il pannello di controllo.

</dd> </dl>

In alcuni casi, anziché immediatamente liberare le risorse, potrebbe essere necessario mantenere i puntatori di interfaccia ai vari oggetti interessati dal completamento automatico. In particolare, questa operazione viene eseguita quando si desidera modificare dinamicamente il comportamento di completamento automatico. L'istanza più comune di questo problema si verifica quando si usa l' \_ oggetto CLSID ACListISF, che esegue il completamento automatico dallo spazio dei nomi della shell e ha l'opzione ([**ACLO \_ CURRENTDIR**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2)) dell'enumerazione dalla directory corrente. Ad esempio, quando si passa a una nuova cartella, Internet Explorer modifica la directory corrente della barra degli indirizzi e pertanto le impostazioni devono essere modificate in modo dinamico. Esistono due modi per specificare la directory che l' \_ oggetto ACLISTISF CLSID deve considerare come la directory corrente:

-   [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) specifica la directory tramite un oggetto [**ItemId**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist).
-   [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) specifica la directory tramite una stringa di percorso.

Nell'esempio seguente si supponga che **PAL** sia un puntatore all'interfaccia [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) di un \_ oggetto ACListISF CLSID:

-   Uso di [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder):

    Per indicare all' \_ oggetto CLSID ACListISF che un elemento [**ItemId**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) specifico deve essere considerato come la directory corrente, è possibile usare l'interfaccia [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) dell'oggetto. Poiché un oggetto **ItemId** può fare riferimento a una cartella virtuale, questo metodo è più flessibile rispetto all'uso di [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory).

    Si noti che negli esempi seguenti viene usato creato un modello QueryInterface, che consente un elenco di parametri semplificato.

    ```C++
    IPersistFolder *ppf;

    hr = pal2->QueryInterface(IID_PPV_ARGS(&ppf));   
    if (SUCCEEDED(hr))
    {
        hr = ppf->Initialize(pidlCurrentDirectory);
        ppf->Release();
    }
    ```

    

-   Uso di [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory):

    Per assegnare all' \_ oggetto CLSID ACListISF un percorso come directory corrente, è possibile usare l'interfaccia [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) dell'oggetto.

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

    

 

 

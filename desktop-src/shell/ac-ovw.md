---
description: Il completamento automatico espande le stringhe immesse parzialmente in un controllo di modifica in stringhe complete.
title: Uso del completamento automatico
ms.topic: article
ms.date: 05/31/2018
ms.assetid: b990395b-fc10-48f9-a718-7cc006e37eb7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 822f2554f51adfb99b1b4b2ad9d61fe064f802def3c8804371639ec20563b54b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119223711"
---
# <a name="using-autocomplete"></a>Uso del completamento automatico

Il completamento automatico espande le stringhe immesse parzialmente in un controllo [di modifica](/windows/desktop/Controls/edit-controls) in stringhe complete. Ad esempio, quando un utente inizia a immettere un URL nel controllo di modifica Indirizzo incorporato nella barra degli strumenti di Windows Internet Explorer, il completamento automatico espande la stringa in una o più opzioni URL complete coerenti con la stringa parziale esistente. Una stringa URL parziale, ad esempio "mic", potrebbe essere espansa in " https://www.microsoft.com " o " https://www.microsoft.com/windows ". Il completamento automatico viene in genere usato con i controlli di modifica o con controlli con un controllo di modifica incorporato, ad esempio [il controllo ComboBoxEx.](/windows/desktop/Controls/comboboxex-control-reference)

## <a name="adding-autocomplete-functionality-to-your-application"></a>Aggiunta di funzionalità di completamento automatico all'applicazione

Un'applicazione può aggiungere funzionalità di completamento automatico a un controllo di modifica in due modi:

-   [**SHAutoComplete è**](/windows/desktop/api/shlwapi/nf-shlwapi-shautocomplete) una funzione semplice che può completare automaticamente un percorso di file o un URL.
-   [**L'interfaccia IAutoComplete**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete) viene esposta dall'oggetto di completamento automatico (completamento \_ automatico CLSID). Consente alle applicazioni di inizializzare, abilitare e disabilitare l'oggetto. **IAutoComplete consente** un maggiore controllo sulle origini di completamento automatico, inclusa la possibilità di aggiungere un'origine personalizzata. Nella parte restante di questo argomento viene illustrato l'uso di **IAutoComplete.** Vedere [How To Enable Autocomplete Manually (Come](how-to-enable-autocomplete-manually.md) abilitare il completamento automatico manualmente) per esempi di utilizzo specifici.

## <a name="autocomplete-modes"></a>Modalità di completamento automatico

Quando si [**usa IAutoComplete,**](/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete)il completamento automatico può visualizzare la stringa completata in due modalità: autoappend e autosuggest. Le modalità sono indipendenti. È possibile abilitare uno o entrambi. Per specificare la modalità, chiamare [**IAutoComplete2::SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions).

<dl> <dt>

<span id="Autoappend"></span><span id="autoappend"></span><span id="AUTOAPPEND"></span>Append automatica
</dt> <dd>

In modalità di applicazione automatica, il completamento automatico aggiunge il resto della stringa candidata più probabile ai caratteri esistenti, evidenziando i caratteri aggiunti. Se l'utente continua a immettere caratteri, vengono aggiunti alla stringa parziale esistente. Se l'utente aggiunge un carattere identico al carattere evidenziato successivo, l'evidenziazione per tale carattere viene disattivata. I caratteri rimanenti verranno comunque evidenziati. Se l'utente aggiunge un carattere che non corrisponde al carattere evidenziato successivo, il completamento automatico tenta di generare una nuova stringa candidata basata sulla stringa parziale più grande e aggiunge il resto della nuova stringa candidata alla stringa parziale corrente. Se non viene trovata alcuna stringa candidata, vengono visualizzati solo i caratteri digitati e la casella di modifica si comporta come senza completamento automatico. Questo processo continua fino a quando l'utente non accetta una stringa.

</dd> <dt>

<span id="Autosuggest"></span><span id="autosuggest"></span><span id="AUTOSUGGEST"></span>Autosuggest
</dt> <dd>

In modalità suggerimenti automatici, il completamento automatico visualizza un elenco a discesa, con una o più stringhe complete suggerite, sotto il controllo di modifica. L'utente può selezionare una delle stringhe suggerite o continuare a digitare. Con l'avanzamento della digitazione, l'elenco a discesa potrebbe essere modificato in base alla stringa parziale corrente. Se si imposta il flag ACO \_ SEARCH in [**IAutoComplete2::SetOptions**](/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions), il completamento automatico offre un'opzione, nella parte inferiore dell'elenco a discesa, per cercare la stringa parziale corrente. Questa opzione viene visualizzata anche se non sono presenti stringhe suggerite. Se l'utente seleziona l'opzione di ricerca, l'applicazione deve avviare un motore di ricerca per assistere l'utente.

</dd> </dl>

## <a name="using-predefined-autocomplete-sources"></a>Uso di origini predefinite di completamento automatico

Il completamento automatico dipende dalla presenza di un'origine che le fornisce stringhe per la corrispondenza con la stringa parziale dell'utente. È possibile fornire un'origine di completamento automatico personalizzata, ma molte delle origini più comuni vengono fornite dal sistema.

<dl> <dt>

<span id="CLSID_ACLHistory"></span><span id="clsid_aclhistory"></span><span id="CLSID_ACLHISTORY"></span>CLSID \_ ACLHistory
</dt> <dd>

Origine di completamento automatico corrispondente all'elenco di URL nell'elenco Cronologia dell'utente.

</dd> <dt>

<span id="CLSID_ACLMRU"></span><span id="clsid_aclmru"></span>CLSID \_ ACLMRU
</dt> <dd>

Origine di completamento automatico corrispondente all'elenco di URL nell'elenco Recently Used (Usati di recente) dell'utente.

</dd> <dt>

<span id="CLSID_ACListISF"></span><span id="clsid_aclistisf"></span><span id="CLSID_ACLISTISF"></span>CLSID \_ ACListISF
</dt> <dd>

Un'origine di completamento automatico che corrisponde agli elementi nello spazio dei nomi shell: file nel computer dell'utente, nonché elementi in cartelle virtuali, ad esempio Pannello di controllo.

</dd> </dl>

In alcuni casi, invece di liberare immediatamente le risorse, è possibile mantenere i puntatori di interfaccia ai vari oggetti coinvolti nel completamento automatico. In particolare, questa operazione viene eseguita quando si vuole modificare dinamicamente il comportamento di completamento automatico. L'istanza più comune di questo si verifica quando si usa l'oggetto CLSID ACListISF, che viene completato automaticamente dallo spazio dei nomi shell e ha l'opzione \_ ([**ACLO \_ CURRENTDIR**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist2)) di enumerazione anche dalla directory corrente. Ad esempio, quando si passa a una nuova cartella, Internet Explorer modifica la directory corrente della barra degli indirizzi e pertanto le impostazioni devono essere modificate in modo dinamico. Esistono due modi per specificare la directory che l'oggetto \_ CLSID ACListISF deve considerare come directory corrente:

-   [**IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) specifica la directory tramite [**itemIDLIST.**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist)
-   [**ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) specifica la directory tramite una stringa di percorso.

Nell'esempio seguente si supponga che **pal** sia un puntatore all'interfaccia [**IACList**](/windows/win32/api/shlobj_core/nn-shlobj_core-iaclist) di un oggetto CLSID \_ ACListISF:

-   Uso [**di IPersistFolder:**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)

    Per indicare all'oggetto CLSID ACListISF che un particolare ITEMIDLIST deve essere considerato come la directory corrente, è possibile usare \_ [**l'interfaccia IPersistFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) dell'oggetto. [](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) Poiché **itemIDLIST può** fare riferimento a una cartella virtuale, questo metodo è più flessibile rispetto [**all'uso di ICurrentWorkingDirectory.**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory)

    Si noti che negli esempi seguenti viene utilizzata l'interfaccia QueryInterface con modello, che consente un elenco di parametri semplificato.

    ```C++
    IPersistFolder *ppf;

    hr = pal2->QueryInterface(IID_PPV_ARGS(&ppf));   
    if (SUCCEEDED(hr))
    {
        hr = ppf->Initialize(pidlCurrentDirectory);
        ppf->Release();
    }
    ```

    

-   Uso [**di ICurrentWorkingDirectory:**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory)

    Per assegnare all'oggetto CLSID ACListISF un percorso come directory corrente, è possibile usare \_ [**l'interfaccia ICurrentWorkingDirectory**](/windows/win32/api/shlobj/nn-shlobj-icurrentworkingdirectory) dell'oggetto.

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

    

 

 

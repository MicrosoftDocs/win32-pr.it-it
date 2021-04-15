---
description: Per assicurarsi che i dati vengano indicizzati e presentati correttamente all'utente durante le ricerche, è necessario implementare gli archivi dati della shell (noti anche come estensioni dello spazio dei nomi della Shell) e i gestori di tipi di file (noti anche come estensioni della shell, gestori di estensioni o gestori di estensioni della Shell).
ms.assetid: 38cebb3c-51bf-439c-8d4e-445344f6cb66
title: Aggiunta di icone, anteprime e menu di scelta rapida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 501006227f6192b7d81a2a88ba915c368a9cc398
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525531"
---
# <a name="adding-icons-previews-and-shortcut-menus"></a>Aggiunta di icone, anteprime e menu di scelta rapida

Per assicurarsi che i dati vengano indicizzati e presentati correttamente all'utente durante le ricerche, è necessario implementare gli archivi dati della shell (noti anche come [estensioni dello spazio dei nomi della shell](../shell/nse-works.md)) e i gestori di tipi di file (noti anche come estensioni della shell, [gestori](../shell/handlers.md)di estensioni o gestori di estensioni della Shell).

In questo argomento vengono descritte le interfacce seguenti:

-   [Implementazione di gestori di tipi di file](#implementing-file-type-handlers)
    -   [IPersist](#ipersist)
    -   [IPersistFolder](#ipersistfolder)
    -   [IShellFolder](#ishellfolder)
    -   [IContextMenu](#icontextmenu)
    -   [IExtractIcon](#iextracticon)
    -   [IPreviewHandler](#ipreviewhandler)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="implementing-file-type-handlers"></a>Implementazione di gestori di tipi di file

Queste estensioni della shell o gestori di tipi di file forniscono agli utenti le seguenti esperienze della shell:

-   La visualizzazione dei risultati Visualizza un'icona specifica per il tipo di elemento.
-   La visualizzazione risultati Visualizza un'anteprima dell'elemento quando l'utente seleziona l'elemento.
-   Gli utenti possono fare doppio clic sugli elementi per avviare eventi quali l'apertura del file.
-   Gli utenti possono fare clic con il pulsante destro del mouse sugli elementi per accedere a un menu di scelta rapida.
-   Gli utenti possono trascinare gli elementi.

Come tutti gli oggetti Component Object Model (COM), i gestori di tipi di file devono implementare un'interfaccia [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) e una class factory.

In Windows XP o versioni precedenti, i gestori devono implementare anche:

-   [Interfaccia IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile)
-   O [interfaccia IShellExtInit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit)

In Windows Vista, l'interfaccia [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) e l' [interfaccia IShellExtInit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) sono state sostituite dalle tre interfacce seguenti per la Shell per inizializzare il gestore:

-   [Interfaccia IInitializeWithStream](/windows/win32/api/propsys/nn-propsys-iinitializewithstream)
-   [Interfaccia IInitializeWithItem](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [Interfaccia IInitializeWithFile](/windows/win32/api/propsys/nn-propsys-iinitializewithfile)

Per offrire un'esperienza utente ragionevole, è necessario fornire un archivio dati della shell con il gestore di protocollo. Tale archivio dati funge quindi da "Factory" per i gestori di icone, i gestori di menu di scelta rapida, i gestori di anteprime e così via. Le implementazioni minime dell'interfaccia [IPersist](/windows/desktop/api/objidl/nn-objidl-ipersist) e dell'interfaccia [IPersistFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder) sono richieste dall' [interfaccia IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)ed è necessaria un'implementazione minima dell'interfaccia IShellFolder per [IContextMenu](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) e [IExtractIcon](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona).

> [!Note]  
> È necessario implementare lo stesso identificatore di classe (CLSID) per **IPersist**, **IPersistFolder** e **IShellFolder**.

 

Per ulteriori informazioni sulla creazione di un archivio dati della Shell per supportare un gestore di protocollo, vedere [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

### <a name="ipersist"></a>IPersist

L'interfaccia **IPersist** definisce il singolo metodo **GetClassID**, progettato per fornire il CLSID di un oggetto che può essere archiviato in modo permanente nel sistema.



| Metodo     | Descrizione                                      |
|------------|--------------------------------------------------|
| GetClassID | Restituisce il CLSID dell'oggetto archivio dati della shell |



 

### <a name="ipersistfolder"></a>IPersistFolder

L'interfaccia **IPersistFolder** viene utilizzata per inizializzare gli oggetti cartella della shell. L'implementazione di questa interfaccia, derivata da **IPersist**, è il modo in cui viene indicato alla cartella dove si trova nello spazio dei nomi della shell. Questa interfaccia non viene usata direttamente. Viene usato dall'implementazione file system del [metodo IShellFolder:: BindToObject](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) Quando Inizializza un oggetto cartella della shell.



| Metodo     | Descrizione                                                                                            |
|------------|--------------------------------------------------------------------------------------------------------|
| Inizializzare | Indica a un oggetto cartella della shell di inizializzarsi in base alle informazioni passate e restituisce \_ OK |



 

### <a name="ishellfolder"></a>IShellFolder

L'interfaccia [IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) viene utilizzata per gestire le cartelle ed è necessaria un'implementazione parziale in modo che l'icona e le interfacce di contesto implementate per un gestore di protocollo si comportino correttamente nell'interfaccia utente dei risultati di Windows Search. La maggior parte delle funzionalità richieste viene esposta tramite il metodo **GetUIObjectOf** . Questo metodo consente a un componente aggiuntivo di eseguire una query per le interfacce **IExtractIcon** e **IContextMenu** .

L'interfaccia [IShellFolder interfaccia](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) USA PIDL anziché URL. Diversamente dai requisiti di un archivio dati Shell completo, i componenti aggiuntivi possono utilizzare una semplice struttura IDL che contiene solo l'URL.

È necessario implementare i metodi seguenti dell' [interfaccia IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . Cinque di questi metodi richiedono un'implementazione minima.



| Metodo           | Descrizione                                                                                                                                                                                                                                                                   |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BindToObject     | Restituisce E \_ NOTIMPL                                                                                                                                                                                                                                                            |
| BindToStorage    | Restituisce E \_ NOTIMPL                                                                                                                                                                                                                                                            |
| CreateViewObject | Restituisce E \_ NOTIMPL                                                                                                                                                                                                                                                            |
| SetNameOf        | Restituisce E \_ NOTIMPL                                                                                                                                                                                                                                                            |
| ParseDisplayName | Converte un URL nella struttura PIDL                                                                                                                                                                                                                                          |
| CompareIDs       | Confronta due valori PIDL                                                                                                                                                                                                                                                      |
| GetDisplayNameOf | Restituisce l'URL per un PIDL                                                                                                                                                                                                                                                    |
| GetUIObjectOf    | Questo metodo è simile al [metodo IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). Se viene richiesta un'icona, il chiamante richiede l'IID \_ IExtractIcon; se viene richiesto un menu di scelta rapida, il chiamante richiede l'IID \_ IContextMenu |



 

**IShellFolder** non viene utilizzato per enumerare le cartelle. Ciò significa che il nome visualizzato di una cartella sarà l'URL fisico. Questo potrebbe cambiare in futuro.

### <a name="icontextmenu"></a>IContextMenu

Quando Windows Search Visualizza i risultati per l'utente, l'utente può fare clic con il pulsante destro del mouse su un elemento e visualizzare un menu di scelta rapida definito dall'interfaccia **IContextMenu** . I menu di scelta rapida sono noti anche come menu di scelta rapida.

L'azione predefinita nel menu di scelta rapida è identica a quella eseguita quando si fa doppio clic sull'elemento. Senza le interfacce **IShellFolder** o **IContextMenu** corrispondenti per l'elemento, il comportamento predefinito per un evento di doppio clic consiste nel passare l'URL come argomento alla funzione della [funzione ShellExecute](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) .

Per ulteriori informazioni sulla creazione di gestori di menu di scelta rapida e per le [estensioni shell per i gestori di protocollo](-search-3x-wds-ph-ui-samplecode.md) per il codice di esempio, vedere [creazione di gestori di menu](../shell/context-menu-handlers.md) di scelta rapida.

### <a name="iextracticon"></a>IExtractIcon

**IExtractIcon** recupera un'icona per l'interfaccia utente di Windows Search basata sull'URL nel PIDL fornito dal gestore del protocollo.

Per ulteriori informazioni sulla creazione di gestori di icone ed [esempi: estensioni della Shell per i gestori di protocollo](-search-3x-wds-ph-ui-samplecode.md) per il codice di esempio, vedere [creazione di gestori di icone](../shell/how-to-create-icon-handlers.md) .

### <a name="ipreviewhandler"></a>IPreviewHandler

[IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) esegue il rendering di un'anteprima dettagliata di un elemento selezionato in Esplora risorse. Le anteprime sono disponibili in Windows Search 4,0 o in Windows Vista con Windows Desktop Search 3. x.

Per creare un gestore di anteprime personalizzato:

1.  Implementare un [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) che accetta un [IStream](/windows/win32/api/objidl/nn-objidl-istream), seguendo le linee guida fornite nei [gestori di anteprime](../shell/preview-handlers.md).
2.  Registrare il gestore di anteprime:

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>
    ```

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>\ShellEx
    ```

    ```
    HKEY_CLASSES_ROOT\<Your_Object_Type>\ShellEx\{8895b1c6-b41f-4c1c-a562-0d564250836f}
       @ = {<Your_PreviewHandler_GUID>}
    ```

3.  Completare i due passaggi seguenti per implementare una cartella della Shell per l'URL:
    1.  Nel [metodo IShellFolder:: GetUIObjectOf](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof)gestire [IQueryAssociations](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) e restituire l'associazione per gli elementi della shell, come illustrato nell'esempio di codice seguente.

        ```
        CComPtr<IQueryAssociations> spqa;
        AssocCreate(CLSID_QueryAssociations, __uuidof(IQueryAssociations), &spqa);
        spqa->Init(0, L"Your_Object_Type", NULL, NULL);
        spqa->QueryInterface(riid, ppvReturn);
        ```

        

    2.  Dopo che la shell ha eseguito una query sulla cartella della Shell per il flusso di dati per inizializzare il gestore di anteprime, passare al metodo [IShellFolder:: BindToObject Method](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) , gestire IID \_ IStream e restituire un [IStream](/windows/win32/api/objidl/nn-objidl-istream) all'URL.

Per riutilizzare un gestore di anteprime esistente per il tipo di file, effettuare i due passaggi seguenti:

1.  Registrare il gestore di anteprime per il tipo di file usando il CLSID del gestore di anteprime esistente al posto di <\_ \_ GUID PreviewHandler>.
2.  Implementare una cartella della shell.

Per ulteriori informazioni sulla creazione di gestori di anteprime, vedere [IPreviewHandler](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler) e [gestori di anteprime](../shell/preview-handlers.md).

## <a name="additional-resources"></a>Risorse aggiuntive

-   Per una panoramica del processo di indicizzazione, vedere [il processo di indicizzazione](-search-indexing-process-overview.md).
-   Per informazioni sulla creazione di gestori, vedere [registrazione di estensioni della shell](../shell/reg-shell-exts.md), [creazione di gestori](../shell/handlers.md)di estensioni della shell, [menu di scelta rapida](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85)), [estensioni dello spazio dei nomi shell](../shell/nse-works.md) e [gestori di anteprime](../shell/preview-handlers.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Sviluppo di gestori di protocollo](-search-3x-wds-phaddins.md)
</dt> <dt>

[Informazioni sui gestori di protocollo](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[Notifica dell'indice delle modifiche](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[Esempio di codice: estensioni della Shell per i gestori di protocollo](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Installazione e registrazione di gestori di protocollo](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Creazione di un connettore di ricerca per un gestore di protocollo](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[Debug di gestori di protocollo](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 

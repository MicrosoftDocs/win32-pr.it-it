---
title: Collegamenti Internet
description: L'oggetto collegamento Internet viene usato per creare collegamenti sul desktop a siti Internet.
ms.assetid: 367c003f-2362-408c-81e1-fda1ffc7e15b
keywords:
- Oggetti collegamento a Internet
- Controlli WebBrowser
- IPropertySetStorage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aba53c320ed740fe7d91a2425b4d47d66e28d78aa35e4ce893efeed12380c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749409"
---
# <a name="internet-shortcuts"></a>Collegamenti Internet

L'oggetto collegamento Internet viene usato per creare collegamenti sul desktop a siti Internet. Analogamente ai collegamenti agli elementi nel file system, i collegamenti Internet hanno la forma di un'icona sul desktop. Quando l'utente fa clic sull'icona, viene avviato il browser e viene visualizzato il sito associato al collegamento.

Vengono illustrati gli argomenti seguenti.

-   [Creazione di collegamenti Internet](#creating-internet-shortcuts)
    -   [Creazione di un collegamento a Internet da un controllo WebBrowser](#creating-an-internet-shortcut-from-a-webbrowser-control)
    -   [Creazione di un collegamento a Internet da un URL](#creating-an-internet-shortcut-from-a-url)
-   [Accesso alle proprietà Archiviazione](#accessing-property-storage)
-   [Interfacce](#interfaces)
    -   [OLE (interfacce)](#ole-interfaces)
    -   [Interfacce della shell](#shell-interfaces)
-   [Funzioni](#functions)
    -   [Funzioni di utilità collegamento Internet](#internet-shortcut-utility-functions)

## <a name="creating-internet-shortcuts"></a>Creazione di collegamenti Internet

È possibile creare un collegamento a Internet usando un controllo WebBrowser o con l'URL della pagina.

### <a name="creating-an-internet-shortcut-from-a-webbrowser-control"></a>Creazione di un collegamento a Internet da un controllo WebBrowser

Se l'applicazione ospita un controllo WebBrowser, è possibile usare l'oggetto collegamento Internet per creare collegamenti nel modo seguente.

1.  Creare un'istanza dell'oggetto collegamento Internet con [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)usando un identificatore di classe (CLSID) di CLSID \_ InternetShortcut.
2.  Passare il puntatore all'interfaccia [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) di WebBrowser all'oggetto collegamento Internet [con IObjectWithSite::SetSite.](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite)
3.  Chiamare il metodo [IPersistFile::Save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) dell'oggetto collegamento Internet quando si vuole creare un collegamento alla pagina visualizzata dal controllo WebBrowser.

Verrà creato un collegamento nel percorso specificato in [IPersistFile::Save.](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) Questo percorso consente al controllo WebBrowser di ripristinare il proprio stato, che include l'attività di caricamento dei documenti corretti nei set di frame.

### <a name="creating-an-internet-shortcut-from-a-url"></a>Creazione di un collegamento a Internet da un URL

È anche possibile creare un collegamento a Internet se si dispone dell'URL della pagina a cui si vuole eseguire il collegamento.

1.  Creare un'istanza dell'oggetto collegamento Internet [con CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)usando un CLSID di CLSID \_ InternetShortcut.
2.  Usare il [metodo IUniformResourceLocator::SetURL](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/dd565676(v=vs.85)) per impostare l'URL nel collegamento.
3.  Usare il [metodo IPersistFile::Save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) per salvare il file di collegamento nel percorso desiderato.

## <a name="accessing-property-storage"></a>Accesso alle proprietà Archiviazione

L'oggetto collegamento Internet contiene diverse proprietà a cui è possibile accedere tramite [l'interfaccia IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) dell'oggetto con la procedura seguente.

1.  Ottenere [l'interfaccia IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) chiamando [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) con IID \_ IPropertySetStorage.
2.  Accedere al set di archiviazione delle proprietà collegamento Internet chiamando [IPropertySetStorage::Open](/windows/win32/api/propidl/nf-propidl-ipropertysetstorage-open) con FMTID Intshcut o FMTID InternetSite per ottenere \_ \_ [l'interfaccia IPropertyStorage.](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage)
3.  Leggere le informazioni sull'archiviazione delle proprietà [con IPropertyStorage::ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) passando l'ID proprietà appropriato.

Con [la versione 4.70](/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)) o successiva di Shell32.dll, è anche possibile recuperare l'interfaccia [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) chiamando [**IShellFolder::BindToStorage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtostorage) con il parametro *pidl* impostato su . File URL e parametro *riid* impostato su IID \_ IPropertySetStorage.

Gli ID proprietà seguenti possono essere richiesti per FMTID \_ Intshcut.



| PROPID               | Tipo variant | Descrizione                                 |
|----------------------|--------------|---------------------------------------------|
| PID \_ IS \_ URL         | VT \_ LPWSTR   | URL a cui il collegamento guida             |
| PID \_ IS \_ NAME        | VT \_ LPWSTR   | Nome del collegamento Internet               |
| PID \_ IS \_ WORKINGDIR  | VT \_ LPWSTR   | Directory di lavoro per il collegamento          |
| PID \_ IS \_ HOTKEY      | Interfaccia utente \_ VT2      | Tasto di scelta rapida per il collegamento                     |
| PID \_ È \_ SHOWCMD     | VT \_ I4       | Comando Mostra per il collegamento                   |
| PID \_ IS \_ ICONINDEX   | VT \_ I4       | Indice dell'icona                           |
| PID \_ IS \_ ICONFILE    | VT \_ LPWSTR   | File che contiene l'icona                 |
| PID \_ IS \_ WHATSNEW    | VT \_ LPWSTR   | Testo delle novità                             |
| PID \_ IS \_ AUTHOR      | VT \_ LPWSTR   | Autore                                      |
| PID \_ IS \_ DESCRIPTION | VT \_ LPWSTR   | Testo della descrizione del sito                    |
| PID \_ IS \_ COMMENT     | VT \_ LPWSTR   | Commento annotato dall'utente                      |
| ROAMING \_ DEL PID \_      | VT \_ BOOL     | True quando il collegamento viene in roaming per la prima volta |



 

Gli ID proprietà seguenti possono essere richiesti per FMTID \_ InternetSite.



| PROPID                     | Tipo variant | Descrizione                                       |
|----------------------------|--------------|---------------------------------------------------|
| PID \_ INTSITE \_ WHATSNEW     | VT \_ LPWSTR   | Testo delle novità                                   |
| PID \_ INTSITE \_ AUTHOR       | VT \_ LPWSTR   | Autore                                            |
| PID \_ INTSITE \_ LASTVISIT    | VT \_ FILETIME | Ora dell'ultima visita del sito                        |
| PID \_ INTSITE \_ LASTMOD      | VT \_ FILETIME | Ora dell'ultima modifica del sito                       |
| PID \_ INTSITE \_ VISITCOUNT   | VT \_ UI4      | Numero di volte in cui l'utente ha visitato                  |
| PID \_ INTSITE \_ DESCRIPTION  | VT \_ LPWSTR   | Testo della descrizione del sito                          |
| PID \_ INTSITE \_ COMMENT      | VT \_ LPWSTR   | Commento annotato dall'utente                            |
| FLAG \_ INTSITE PID \_        | VT \_ UI4      | Indica l'uso dei flag PIDISF \_ (vedere di seguito)       |
| PID \_ INTSITE \_ CONTENTLEN   | N/A          | Attualmente non supportato                           |
| PID \_ INTSITE \_ CONTENTCODE  | N/A          | Attualmente non supportato                           |
| PID \_ INTSITE \_ RECURSE      | N/A          | Attualmente non supportato                           |
| PID \_ INTSITE \_ WATCH        | N/A          | Attualmente non supportato                           |
| PID \_ INTSITE \_ SUBSCRIPTION | Interfaccia utente \_ VT8      | Valore SUBSCRIPTIONCOOKIE per il gestore delle sottoscrizioni |
| PID \_ INTSITE \_ URL          | VT \_ LPWSTR   | URL a cui il collegamento guida                   |
| PID \_ INTSITE \_ TITLE        | VT \_ LPWSTR   | Titolo                                             |
| PID \_ INTSITE \_ CODEPAGE     | VT \_ UI4      | Tabella codici del documento                          |
| PID \_ INTSITE \_ TRACKING     | N/A          | Attualmente non supportato                           |
| PID \_ INTSITE \_ ICONINDEX    | VT \_ I4       | Indice dell'icona                                 |
| PID \_ INTSITE \_ ICONFILE     | VT \_ LPWSTR   | File che contiene l'icona                       |
| ROAMING \_ DI PID INTSITE \_       | VT \_ UI4      | La voce è stata aggiunta a causa del roaming                |



 

Di seguito sono riportati i flag del sito Internet.



| Flag                    | Descrizione                                |
|-------------------------|--------------------------------------------|
| PIDISF \_ MODIFICATO DI RECENTE | Indica che un sito è stato modificato di recente |
| PIDISF \_ CACHEDSTICKY    | Attualmente non supportato                    |
| PIDISF \_ CACHEIMAGES     | Attualmente non supportato                    |
| PIDISF \_ FOLLOWALLLINKS  | Attualmente non supportato                    |



 

I valori seguenti vengono usati per la cronologia del roaming internet.



| Valore di PID \_ INTSITE \_ ROAMED         | Descrizione                                                                                                                                                              |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valore non impostato o PIDISR \_ UP \_ TO \_ DATE | Questa voce della cache non è stata modificata dal roaming.                                                                                                                       |
| PIDISR \_ RICHIEDE \_ L'AGGIUNTA                    | Questa voce della cache è stata aggiunta alla cache tramite roaming. Impostare PIDISR \_ UP TO DATE al termine \_ \_ dell'elaborazione della voce.                                                   |
| PIDISR \_ RICHIEDE \_ L'AGGIORNAMENTO                 | Questa voce della cache esisteva già nel computer locale, ma è stata aggiornata tramite roaming. Impostare PIDISR \_ UP TO DATE al termine \_ \_ dell'elaborazione della voce.                 |
| PIDISR \_ RICHIEDE \_ L'ELIMINAZIONE                 | Roaming ha rilevato che questa voce della cache deve essere eliminata. Ad esempio, l'utente potrebbe aver cancellato la cronologia del browser. Eliminare la voce usando DeleteUrlCacheEntry. |



 

## <a name="interfaces"></a>Interfacce

L'oggetto collegamento Internet espone una serie di interfacce.

### <a name="ole-interfaces"></a>OLE (interfacce)

-   [Idataobject](/windows/win32/api/objidl/nn-objidl-idataobject)
-   [Ipersistfile](/windows/win32/api/objidl/nn-objidl-ipersistfile)
-   [Ipersiststream](/windows/win32/api/objidl/nn-objidl-ipersiststream)
-   [Iolecommandtarget](/windows/win32/api/docobj/nn-docobj-iolecommandtarget)
-   [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage)
-   [IObjectWithSite](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)

### <a name="shell-interfaces"></a>Interfacce della shell

-   [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2)
-   [**IExtractIcon**](/windows/desktop/api/shlobj_core/nn-shlobj_core-iextracticona)
-   [**INewShortcutHook**](/windows/desktop/api/shlobj/nn-shlobj-inewshortcuthooka)
-   [**IShellExtInit**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellextinit)
-   [**IShellLink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka)
-   [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)
-   [**IQueryInfo**](/windows/desktop/api/shlobj_core/nn-shlobj_core-iqueryinfo)

## <a name="functions"></a>Funzioni

Esistono diverse funzioni di utilità che possono essere usate con l'oggetto collegamento Internet.

### <a name="internet-shortcut-utility-functions"></a>Funzioni di utilità collegamento Internet

-   [**InetIsOffline**](/windows/desktop/api/intshcut/nf-intshcut-inetisoffline)
-   [**MimeAssociationDialog**](/windows/desktop/api/intshcut/nf-intshcut-mimeassociationdialoga)
-   [**TranslateURL**](/windows/desktop/api/intshcut/nf-intshcut-translateurla)
-   [**Finestra di dialogo URLAssociationDialog**](/windows/desktop/api/intshcut/nf-intshcut-urlassociationdialoga)

 

 
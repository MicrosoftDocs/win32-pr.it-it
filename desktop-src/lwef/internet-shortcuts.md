---
title: Collegamenti Internet
description: L'oggetto collegamento Internet viene usato per creare collegamenti desktop ai siti Internet.
ms.assetid: 367c003f-2362-408c-81e1-fda1ffc7e15b
keywords:
- Oggetti collegamento Internet
- Controlli WebBrowser
- IPropertySetStorage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f14bc2ed58f75522e59b9008ded7b0f1416a21fe
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046709"
---
# <a name="internet-shortcuts"></a>Collegamenti Internet

L'oggetto collegamento Internet viene usato per creare collegamenti desktop ai siti Internet. Analogamente ai tasti di scelta rapida per gli elementi del file system, i collegamenti Internet hanno il formato di un'icona sul desktop. Quando l'utente fa clic sull'icona, viene avviato il browser e viene visualizzato il sito associato al collegamento.

Vengono illustrati gli argomenti seguenti.

-   [Creazione di collegamenti a Internet](#creating-internet-shortcuts)
    -   [Creazione di un collegamento Internet da un controllo WebBrowser](#creating-an-internet-shortcut-from-a-webbrowser-control)
    -   [Creazione di un collegamento Internet da un URL](#creating-an-internet-shortcut-from-a-url)
-   [Accesso all'archiviazione delle proprietà](#accessing-property-storage)
-   [Interfacce](#interfaces)
    -   [OLE (interfacce)](#ole-interfaces)
    -   [Interfacce della shell](#shell-interfaces)
-   [Funzioni](#functions)
    -   [Funzioni di utilità di collegamento Internet](#internet-shortcut-utility-functions)

## <a name="creating-internet-shortcuts"></a>Creazione di collegamenti a Internet

È possibile creare un collegamento Internet utilizzando un controllo WebBrowser o con l'URL della pagina.

### <a name="creating-an-internet-shortcut-from-a-webbrowser-control"></a>Creazione di un collegamento Internet da un controllo WebBrowser

Se l'applicazione ospita un controllo WebBrowser, è possibile utilizzare l'oggetto collegamento Internet per creare i collegamenti nel modo seguente.

1.  Creare un'istanza dell'oggetto collegamento Internet con [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), usando un identificatore di classe (CLSID) di CLSID \_ InternetShortcut.
2.  Passare il puntatore all'interfaccia [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) di WebBrowser all'oggetto collegamento Internet con [IObjectWithSite:: SESITE](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite).
3.  Chiamare il metodo [IPersistFile:: Save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) dell'oggetto Shortcut Internet quando si desidera creare un collegamento alla pagina visualizzata dal controllo WebBrowser.

Verrà creato un collegamento nel percorso specificato in [IPersistFile:: Save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). Questo percorso consente al controllo WebBrowser di ripristinare il proprio stato, che include l'attività di caricamento dei documenti corretti in frame.

### <a name="creating-an-internet-shortcut-from-a-url"></a>Creazione di un collegamento Internet da un URL

È anche possibile creare un collegamento a Internet se si dispone dell'URL della pagina a cui si desidera collegarsi.

1.  Creare un'istanza dell'oggetto collegamento Internet con [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), usando un CLSID di CLSID \_ InternetShortcut.
2.  Usare il metodo [IUniformResourceLocator:: SetUrl](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/dd565676(v=vs.85)) per impostare l'URL nel collegamento.
3.  Usare il metodo [IPersistFile:: Save](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) per salvare il file di collegamento nel percorso desiderato.

## <a name="accessing-property-storage"></a>Accesso all'archiviazione delle proprietà

L'oggetto collegamento Internet contiene diverse proprietà a cui è possibile accedere tramite l'interfaccia [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) dell'oggetto con la procedura riportata di seguito.

1.  Ottenere l'interfaccia [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) chiamando [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) con IID \_ IPropertySetStorage.
2.  Accedere al set di archiviazione delle proprietà dei collegamenti Internet chiamando [IPropertySetStorage:: Open](/windows/win32/api/propidl/nf-propidl-ipropertysetstorage-open) con fmtid \_ Intshcut o fmtid \_ InternetSite per ottenere l'interfaccia [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) .
3.  Leggere le informazioni sull'archiviazione delle proprietà con [IPropertyStorage:: ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) passando l'ID di proprietà appropriato.

Con la [versione 4,70 o successiva](/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)) di Shell32.dll, è anche possibile recuperare l'interfaccia [IPropertySetStorage](/windows/win32/api/propidl/nn-propidl-ipropertysetstorage) chiamando [**IShellFolder:: BindToStorage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtostorage) con il parametro *PIDL* impostato su. Il file URL e il parametro *riid* sono impostati su IID \_ IPropertySetStorage.

È possibile richiedere gli ID di proprietà seguenti per FMTID \_ Intshcut.



| PROPID               | Tipo Variant | Descrizione                                 |
|----------------------|--------------|---------------------------------------------|
| PID \_ è un \_ URL         | \_LPWSTR VT   | URL a cui i lead di collegamento             |
| PID \_ è il \_ nome        | \_LPWSTR VT   | Nome del collegamento Internet               |
| PID \_ è \_ WORKINGDIR  | \_LPWSTR VT   | Directory di lavoro per il collegamento          |
| PID \_ è un \_ tasto di scelta rapida      | \_UI2 VT      | Tasto di scelta rapida per il collegamento                     |
| PID \_ è \_ SHOWCMD     | VT \_ I4       | Mostra comando per collegamento                   |
| PID \_ è \_ ICONINDEX   | VT \_ I4       | Indice dell'icona                           |
| PID \_ è \_ IconFile    | \_LPWSTR VT   | File che contiene l'icona                 |
| PID \_ è \_ novità    | \_LPWSTR VT   | Testo novità                             |
| PID \_ è \_ autore      | \_LPWSTR VT   | Autore                                      |
| \_Descrizione PID \_ | \_LPWSTR VT   | Testo della descrizione del sito                    |
| PID \_ è un \_ Commento     | \_LPWSTR VT   | Commento annotato dall'utente                      |
| PID \_ in \_ roaming      | \_bool VT     | True se il collegamento è in roaming per la prima volta |



 

È possibile richiedere gli ID di proprietà seguenti per FMTID \_ InternetSite.



| PROPID                     | Tipo Variant | Descrizione                                       |
|----------------------------|--------------|---------------------------------------------------|
| \_novità INTSITE \_ PID     | \_LPWSTR VT   | Testo novità                                   |
| \_autore INTSITE \_ PID       | \_LPWSTR VT   | Autore                                            |
| \_LASTVISIT INTSITE \_ PID    | FILETIME VT \_ | Data e ora dell'ultima visita del sito                        |
| \_LASTMOD INTSITE \_ PID      | FILETIME VT \_ | Data dell'Ultima modifica del sito                       |
| \_VISITCOUNT INTSITE \_ PID   | \_UI4 VT      | Numero di volte che l'utente ha visitato                  |
| \_Descrizione INTSITE \_ PID  | \_LPWSTR VT   | Testo della descrizione del sito                          |
| \_Commento INTSITE \_ PID      | \_LPWSTR VT   | Commento annotato dall'utente                            |
| \_flag INTSITE \_ PID        | \_UI4 VT      | Indica l'uso dei \_ flag PIDISF (vedere di seguito)       |
| \_CONTENTLEN INTSITE \_ PID   | N/D          | Attualmente non supportato                           |
| \_CONTENTCODE INTSITE \_ PID  | N/D          | Attualmente non supportato                           |
| \_recurse INTSITE PID \_      | N/D          | Attualmente non supportato                           |
| \_orologio PID INTSITE \_        | N/D          | Attualmente non supportato                           |
| \_sottoscrizione PID INTSITE \_ | \_UI8 VT      | Valore SUBSCRIPTIONCOOKIE per Gestione sottoscrizioni |
| \_URL INTSITE \_ PID          | \_LPWSTR VT   | URL a cui i lead di collegamento                   |
| \_titolo INTSITE \_ PID        | \_LPWSTR VT   | Titolo                                             |
| tabella \_ codici PID INTSITE \_     | \_UI4 VT      | Tabella codici del documento                          |
| \_rilevamento INTSITE \_ PID     | N/D          | Attualmente non supportato                           |
| \_ICONINDEX INTSITE \_ PID    | VT \_ I4       | Indice dell'icona                                 |
| \_IconFile INTSITE \_ PID     | \_LPWSTR VT   | File che contiene l'icona                       |
| PID \_ INTSITE in \_ roaming       | \_UI4 VT      | La voce è stata aggiunta a causa del roaming                |



 

Di seguito sono riportati i flag del sito Internet.



| Flag                    | Descrizione                                |
|-------------------------|--------------------------------------------|
| \_RECENTLYCHANGED PIDISF | Indica che un sito è stato modificato di recente |
| \_CACHEDSTICKY PIDISF    | Attualmente non supportato                    |
| \_CACHEIMAGES PIDISF     | Attualmente non supportato                    |
| \_FOLLOWALLLINKS PIDISF  | Attualmente non supportato                    |



 

Per la cronologia roaming Internet vengono usati i valori seguenti.



| Valore di INTSITE PID in \_ \_ roaming         | Descrizione                                                                                                                                                              |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valore non impostato \_ o PIDISR aggiornato \_ \_ | Questa voce della cache non è stata modificata dal roaming.                                                                                                                       |
| PIDISR \_ deve essere \_ aggiunto                    | Questa voce della cache è stata aggiunta alla cache mediante roaming. Impostare PIDISR \_ aggiornato \_ al \_ termine dell'elaborazione della voce.                                                   |
| PIDISR \_ deve essere \_ aggiornato                 | Questa voce della cache esisteva già nel computer locale, ma è stata aggiornata dal roaming. Impostare PIDISR \_ aggiornato \_ al \_ termine dell'elaborazione della voce.                 |
| PIDISR \_ deve essere \_ eliminato                 | Roaming ha rilevato che questa voce della cache deve essere eliminata. Ad esempio, è possibile che l'utente abbia cancellato la cronologia del browser. Eliminare la voce usando DeleteUrlCacheEntry. |



 

## <a name="interfaces"></a>Interfacce

L'oggetto collegamento Internet espone una serie di interfacce.

### <a name="ole-interfaces"></a>OLE (interfacce)

-   [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject)
-   [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile)
-   [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream)
-   [IOleCommandTarget](/windows/win32/api/docobj/nn-docobj-iolecommandtarget)
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

Con l'oggetto collegamento Internet è possibile utilizzare diverse funzioni di utilità.

### <a name="internet-shortcut-utility-functions"></a>Funzioni di utilità di collegamento Internet

-   [**InetIsOffline**](/windows/desktop/api/intshcut/nf-intshcut-inetisoffline)
-   [**MIMEAssociationDialog**](/windows/desktop/api/intshcut/nf-intshcut-mimeassociationdialoga)
-   [**TranslateURL**](/windows/desktop/api/intshcut/nf-intshcut-translateurla)
-   [**URLAssociationDialog**](/windows/desktop/api/intshcut/nf-intshcut-urlassociationdialoga)

 

 
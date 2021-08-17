---
description: In questa sezione vengono descritte le Windows shell.
title: Strutture della shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 814ae153-39b3-49ee-9da1-efe7e649c73e
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: fa046223ba3aa6a6e98d6e74f623aeaad9e85d3a10148bb688eb385c0e7c22fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117675804"
---
# <a name="shell-structures"></a>Strutture della shell

In questa sezione vengono descritte le Windows shell.

## <a name="in-this-section"></a>Contenuto della sezione



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Argomento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj/ns-shlobj-aashellmenufilename"><strong>AASHELLMENUFILENAME</strong></a><br/></td>
<td>Struttura di dimensioni variabili che contiene informazioni sul nome di un file di menu.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj/ns-shlobj-aashellmenuitem"><strong>AASHELLMENUITEM</strong></a><br/></td>
<td>Contiene informazioni su una voce di menu.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-appbardata"><strong>APPBARDATA</strong></a><br/></td>
<td>Contiene informazioni su un messaggio della barra delle app di sistema.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfo"><strong>APPCATEGORYINFO</strong></a><br/></td>
<td>Fornisce informazioni sulla categoria dell'applicazione a Installazione applicazioni in Pannello di controllo. La <a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfolist"><strong>struttura APPCATEGORYINFOLIST</strong></a> viene usata per creare un elenco completo di categorie per un editore di applicazioni.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfolist"><strong>APPCATEGORYINFOLIST</strong></a><br/></td>
<td>Fornisce un elenco delle categorie di applicazioni supportate da un editore di applicazioni a Installazione applicazioni in Pannello di controllo. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shappmgr/ns-shappmgr-appinfodata"><strong>APPINFODATA</strong></a><br/></td>
<td>Fornisce informazioni su un'applicazione pubblicata all'utilità Installazione applicazioni Pannello di controllo pubblicata.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-associationelement"><strong>ASSOCIATIONELEMENT</strong></a><br/></td>
<td>Definisce le informazioni usate da <a href="/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses"><strong>AssocCreateForClasses per</strong></a> recuperare <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>un'interfaccia IQueryAssociations</strong></a> per una determinata associazione di file.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-bandinfosfb"><strong>BANDINFOSFB</strong></a><br/></td>
<td>Contiene informazioni su una banda di cartelle. Questa struttura viene usata con i metodi <a href="/windows/desktop/api/shlobj/nf-shlobj-ishellfolderband-getbandinfosfb"><strong>IShellFolderBand::GetBandInfoSFB</strong></a> e <a href="/windows/desktop/api/shlobj/nf-shlobj-ishellfolderband-setbandinfosfb"><strong>IShellFolderBand::SetBandInfoSFB.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-bandsiteinfo"><strong>BANDSITEINFO</strong></a><br/></td>
<td>Contiene informazioni su un sito a banda. Questa struttura viene usata con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-getbandsiteinfo"><strong>i metodi IBandSite::GetBandSiteInfo</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-setbandsiteinfo"><strong>IBandSite::SetBandSiteInfo.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shdeprecated/ns-shdeprecated-basebrowserdatalh"><strong>BASEBROWSERDATA</strong></a><br/></td>
<td>Contiene i membri protetti della classe di base. <a href="/windows/desktop/api/Shdeprecated/ns-shdeprecated-basebrowserdatalh"><strong>BASEBROWSERDATA</strong></a> definisce lo stato del browser e viene usato con <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-getbasebrowserdata"><strong>IBrowserService2::GetBaseBrowserData</strong></a> e <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-putbasebrowserdata"><strong>IBrowserService2::P utBaseBrowserData</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/cc136564(v=vs.85)"><strong>BORDERWIDTHS</strong></a><br/></td>
<td>Definisce le coordinate degli angoli superiore sinistro e inferiore destro di un rettangolo del bordo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa"><strong>BROWSEINFO</strong></a><br/></td>
<td>Contiene i parametri per <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera"><strong>la funzione SHBrowseForFolder</strong></a> e riceve informazioni sulla cartella selezionata dall'utente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-category_info"><strong>CATEGORY_INFO</strong></a><br/></td>
<td>Contiene informazioni sulla categoria. Una categoria di componenti è un gruppo di classi COM (Logically Related Component Object Model) che condividono un CATID (Common Category Identifier).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-cida"><strong>Cida</strong></a><br/></td>
<td>Usato con il formato <a href="clipboard.md">CFSTR_SHELLIDLIST</a> appunti per trasferire il puntatore a un elenco di identificatori di elemento (PIDL) di uno o più oggetti spazio dei nomi shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo"><strong>CM_COLUMNINFO</strong></a><br/></td>
<td>Definisce le informazioni sulla colonna. Usato dai membri <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>dell'interfaccia IColumnManager.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>CMINVOKECOMMANDINFO</strong></a><br/></td>
<td>Contiene le informazioni necessarie a <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand"><strong>IContextMenu::InvokeCommand</strong></a> per richiamare un comando di menu di scelta rapida.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex"><strong>CMINVOKECOMMANDINFOEX</strong></a><br/></td>
<td>Contiene informazioni estese su un comando di menu di scelta rapida. Questa struttura è una versione estesa di <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>CMINVOKECOMMANDINFO</strong></a> che consente l'uso di valori Unicode.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec"><strong>COMDLG_FILTERSPEC</strong></a><br/></td>
<td>Usato in modo generico per filtrare gli elementi.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-component"><strong>Componente</strong></a><br/></td>
<td>Usato da Windows 2000 per contenere informazioni su un componente. Questa struttura sostituisce la <a href="/windows/win32/api/shlobj_core/ns-shlobj_core-ie4component"><strong>struttura IE4COMPONENT.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-componentsopt"><strong>COMPONENTSOPT</strong></a><br/></td>
<td>Contiene le opzioni dell'elemento del desktop.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-comppos"><strong>COMPPOS</strong></a><br/></td>
<td>Contiene informazioni sulla posizione e sulle dimensioni di un componente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-compstateinfo"><strong>COMPSTATEINFO</strong></a><br/></td>
<td>Usato da Windows 2000 per contenere informazioni sullo stato di un componente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-confirm_conflict_item"><strong>CONFIRM_CONFLICT_ITEM</strong></a><br/></td>
<td>Definisce la struttura degli elementi in conflitto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-confirm_conflict_result_info"><strong>CONFIRM_CONFLICT_RESULT_INFO</strong></a><br/></td>
<td>Definisce la struttura delle informazioni sui risultati dei conflitti.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cpl/ns-cpl-cplinfo"><strong>CPLINFO</strong></a><br/></td>
<td>Contiene informazioni sulle risorse e un valore definito dall'applicazione per una finestra di dialogo supportata da un Pannello di controllo app. La <a href="/windows/desktop/api/cpl/nc-cpl-applet_proc"><strong>funzione CPlApplet</strong></a> dell'applicazione Pannello di controllo restituisce queste informazioni al Pannello di controllo in risposta <a href="cpl-inquire.md"><strong>a</strong></a> un CPL_INQUIRE messaggio.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/ns-credentialprovider-credential_provider_credential_serialization"><strong>CREDENTIAL_PROVIDER_CREDENTIAL_SERIALIZATION</strong></a><br/></td>
<td>Contiene informazioni dettagliate su una credenziale.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/ns-credentialprovider-credential_provider_field_descriptor"><strong>CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR</strong></a><br/></td>
<td>Descrive un singolo campo in una credenziale. Ad esempio, una stringa o un'immagine utente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-csfv"><strong>CSFV</strong></a><br/></td>
<td>Usato con la <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex"><strong>funzione SHCreateShellFolderViewEx.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-datablock_header"><strong>DATABLOCK_HEADER</strong></a><br/></td>
<td>Funge da intestazione per alcune delle strutture di dati aggiuntive usate da <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu"><strong>DEFCONTEXTMENU</strong></a><br/></td>
<td>Contiene informazioni sul menu di scelta <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu"><strong>rapida usate da SHCreateDefaultContextMenu.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-delegateitemid"><strong>DELEGATEITEMID</strong></a><br/></td>
<td>Utilizzato dalle cartelle delegate al posto di una struttura <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a> standard.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo"><strong>DETAILSINFO</strong></a><br/></td>
<td>Contiene informazioni dettagliate per un elemento della cartella Shell. Usato con <a href="sfvm-getdetailsof.md"><strong>la</strong></a> SFVM_GETDETAILSOF notifica.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics"><strong>DFMICS</strong></a><br/></td>
<td>Contiene argomenti aggiuntivi usati da <a href="dfm-invokecommandex.md"><strong>DFM_INVOKECOMMANDEX</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo"><strong>DLLVERSIONINFO</strong></a><br/></td>
<td>Riceve informazioni sulla versione specifiche della DLL. Viene usato con la <a href="/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc"><strong>funzione DllGetVersion.</strong></a> <br/>
<blockquote>
[!Note]<br />
Al posto di questa struttura, è possibile usare la <a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2"><strong>struttura DLLVERSIONINFO2.</strong></a>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2"><strong>DLLVERSIONINFO2</strong></a><br/></td>
<td>Riceve informazioni sulla versione specifiche della DLL. Viene usato con la <a href="/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc"><strong>funzione DllGetVersion.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription"><strong>DROPDESCRIPTION</strong></a><br/></td>
<td>Descrive l'immagine e il testo associato per un oggetto drop.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles"><strong>DROPFILES</strong></a><br/></td>
<td>Definisce il formato <a href="clipboard.md">CF_HDROP</a> Appunti. I dati seguenti sono un elenco di nomi di file con terminazione Null doppio.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_darwin_link"><strong>EXP_DARWIN_LINK</strong></a><br/></td>
<td>Contiene un blocco di dati aggiuntivo usato da <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>. Contiene l'ID del programma di installazione Windows collegamento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_propertystorage"><strong>EXP_PROPERTYSTORAGE</strong></a><br/></td>
<td>Archivia informazioni sullo stato del collegamento shell. Questa struttura viene usata per sezioni di dati aggiuntive contrassegnate con EXP_PROPERTYSTORAGE_SIG.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_special_folder"><strong>EXP_SPECIAL_FOLDER</strong></a><br/></td>
<td>Contiene un blocco di dati aggiuntivo usato da <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>. Contiene informazioni speciali sulla cartella.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_sz_link"><strong>EXP_SZ_LINK</strong></a><br/></td>
<td>Contiene un blocco di dati aggiuntivo usato da <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>. Contiene stringhe di ambiente espandibili per l'icona o la destinazione.<br/></td>
</tr>
<tr class="even">
<td><a href="ext-button.md"><strong>EXT_BUTTON</strong></a><br/></td>
<td>Contiene informazioni su un pulsante aggiunto da una DLL di estensione di File Manager alla barra degli strumenti di File Manager.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-extrasearch"><strong>EXTRASEARCH</strong></a><br/></td>
<td>Utilizzato da un <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumextrasearch"><strong>oggetto enumeratore IEnumExtraSearch</strong></a> per restituire informazioni sugli oggetti di ricerca supportati da un oggetto Shell Folder.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-file_attributes_array"><strong>FILE_ATTRIBUTES_ARRAY</strong></a><br/></td>
<td>Contiene la definizione del formato degli Appunti per CFSTR_FILE_ATTRIBUTES_ARRAY.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-filedescriptora"><strong>FILEDESCRIPTOR</strong></a><br/></td>
<td>Descrive le proprietà di un file copiato tramite gli Appunti durante un'ActiveX di <a href="dragdrop.md">trascinamento della selezione di</a> Microsoft.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-filegroupdescriptora"><strong>FILEGROUPDESCRIPTOR</strong></a><br/></td>
<td>Definisce il formato CF_FILEGROUPDESCRIPTOR appunti.<br/></td>
</tr>
<tr class="odd">
<td><a href="fms-getdriveinfo.md"><strong>FMS_GETDRIVEINFO</strong></a><br/></td>
<td>Contiene informazioni sull'unità selezionata nella finestra attiva di File Manager (la finestra della directory o la finestra Risultati ricerca).<br/></td>
</tr>
<tr class="even">
<td><a href="fms-getfilesel.md"><strong>FMS_GETFILESEL</strong></a><br/></td>
<td>Contiene informazioni su un file selezionato nella finestra attiva di File Manager (la finestra della directory o la finestra Risultati ricerca).<br/></td>
</tr>
<tr class="odd">
<td><a href="fms-helpstring.md"><strong>FMS_HELPSTRING</strong></a><br/></td>
<td>Contiene informazioni utilizzate da Gestione file per aggiungere una stringa della Guida per un menu o una voce di comando della barra degli strumenti.<br/></td>
</tr>
<tr class="even">
<td><a href="fms-load.md"><strong>FMS_LOAD</strong></a><br/></td>
<td>Contiene informazioni utilizzate da Gestione file per aggiungere un menu personalizzato fornito da una DLL di estensione di File Manager. La struttura fornisce anche un valore delta che la DLL di estensione può usare per modificare il menu personalizzato dopo che File Manager ha caricato il menu.<br/></td>
</tr>
<tr class="odd">
<td><a href="fms-toolbarload.md"><strong>FMS_TOOLBARLOAD</strong></a><br/></td>
<td>Contiene informazioni sui pulsanti personalizzati da aggiungere alla barra degli strumenti di File Manager. I pulsanti vengono forniti da una DLL di estensione di File Manager.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings"><strong>FOLDERSETTINGS</strong></a><br/></td>
<td>Contiene informazioni sulla visualizzazione della cartella.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-fvshowinfo"><strong>FVSHOWINFO</strong></a><br/></td>
<td>Contiene informazioni utilizzate dal visualizzatore di file per visualizzare un file.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/winuser/ns-winuser-helpinfo"><strong>HELPINFO</strong></a><br/></td>
<td>Contiene informazioni su un elemento per cui è stata richiesta la Guida sensibile al contesto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/winuser/ns-winuser-helpwininfow"><strong>HELPWININFO</strong></a><br/></td>
<td>Contiene le dimensioni e la posizione di una finestra della Guida primaria o secondaria. Un'applicazione può impostare queste informazioni chiamando la <a href="/windows/desktop/api/Winuser/nf-winuser-winhelpa"><strong>funzione WinHelp</strong></a> con HELP_SETWINPOS valore.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-ie4component"><strong>IE4COMPONENT</strong></a><br/></td>
<td>Usato da Microsoft Internet Explorer 4.0 e Microsoft Internet Explorer 4.01 per contenere informazioni su un componente. Con Windows 2000, viene sostituito dalla <a href="/windows/win32/api/shlobj_core/ns-shlobj_core-component"><strong>struttura COMPONENT.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a><br/></td>
<td>Contiene un elenco di identificatori di elemento.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-itemspacing"><strong>ELEMENTIPACING</strong></a><br/></td>
<td>Archivia le dimensioni delle due possibili dimensioni di spaziatura delle icone disponibili per la visualizzazione: piccola e grande. Usato da <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-getitemspacing"><strong>IShellFolderView::GetItemSpacing</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition"><strong>KNOWNFOLDER_DEFINITION</strong></a><br/></td>
<td>Definisce le specifiche di una cartella nota.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shtypes/ns-shtypes-logfontw"><strong>Logfont</strong></a><br/></td>
<td>Definisce gli attributi di un tipo di carattere.<br/></td>
</tr>
<tr class="odd">
<td><a href="mruinfo.md"><strong>MRUINFO</strong></a><br/></td>
<td>Contiene informazioni che definiscono un nuovo elenco MRU (Most Recently Used). Utilizzato da <a href="createmrulist.md"><strong>CreateMRUListW</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/winuser/ns-winuser-multikeyhelpw"><strong>MULTIKEYHELP</strong></a><br/></td>
<td>Specifica una parola chiave da cercare e la tabella delle parole chiave da cercare Windows Guida.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shellapi/ns-shellapi-nc_address"><strong>NC_ADDRESS</strong></a><br/></td>
<td>Contiene informazioni che descrivono un indirizzo di rete.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/shell/hkey-type"><strong>NET_ADDRESS_INFO</strong></a><br/></td>
<td>Descrive un indirizzo di rete.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cpl/ns-cpl-newcplinfow"><strong>NEWCPLINFO</strong></a><br/></td>
<td>Contiene informazioni sulle risorse e un valore definito dall'applicazione per una finestra di dialogo supportata da un Pannello di controllo app.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa"><strong>NOTIFYICONDATA</strong></a><br/></td>
<td>Contiene informazioni necessarie al sistema per visualizzare le notifiche nell'area di notifica. Usato da <a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona"><strong>Shell_NotifyIcon</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-notifyiconidentifier"><strong>NOTIFYICONIDENTIFIER</strong></a><br/></td>
<td>Contiene le informazioni <a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect"><strong>usate</strong></a> Shell_NotifyIconGetRect per identificare l'icona per cui recuperare il rettangolo di delimitazione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nresarray"><strong>NRESARRAY</strong></a><br/></td>
<td>Definisce il formato CF_NETRESOURCE Appunti.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/ns-shobjidl-nstccustomdraw"><strong>NSTCCUSTOMDRAW</strong></a><br/></td>
<td>Struttura di disegno personalizzata usata <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrolcustomdraw"><strong>dai metodi INameSpaceTreeControlCustomDraw.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nt_console_props"><strong>NT_CONSOLE_PROPS</strong></a><br/></td>
<td>Contiene un blocco di dati aggiuntivo usato da <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>. Contiene le proprietà della console.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nt_fe_console_props"><strong>NT_FE_CONSOLE_PROPS</strong></a><br/></td>
<td>Contiene un blocco di dati aggiuntivo usato da <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>. Contiene la tabella codici della console.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-open_printer_props_infoa"><strong>OPEN_PRINTER_PROPS_INFO</strong></a><br/></td>
<td>Identifica una determinata finestra delle proprietà nelle pagine delle proprietà di una stampante e indica se la finestra delle proprietà deve essere modale. Facoltativamente usato con la <a href="/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda"><strong>funzione SHInvokePrinterCommand.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-openasinfo"><strong>OPENASINFO</strong></a><br/></td>
<td>Archivia le informazioni per <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shopenwithdialog"><strong>la funzione SHOpenWithDialog.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/ns-shobjidl-overlapped"><strong>Sovrapposta</strong></a><br/></td>
<td>Contiene informazioni usate nell'input/output (I/O) asincrono (sovrapposto).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlwapi/ns-shlwapi-parsedurlw"><strong>PARSEDURL</strong></a><br/></td>
<td>Usato dalla <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-parseurla"><strong>funzione ParseURL</strong></a> per restituire l'URL analizzato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-persist_folder_target_info"><strong>PERSIST_FOLDER_TARGET_INFO</strong></a><br/></td>
<td>Specifica la cartella di destinazione di un collegamento alla cartella e i relativi attributi. Questa struttura viene usata da <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-getfoldertargetinfo"><strong>IPersistFolder3::GetFolderTargetInfo</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-initializeex"><strong>IPersistFolder3::InitializeEx</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-previewhandlerframeinfo"><strong>PREVIEWHANDLERFRAMEINFO</strong></a><br/></td>
<td>Struttura della tabella dei tasti di scelta rapida. Usato da <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext"><strong>IPreviewHandlerFrame::GetWindowContext</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Profinfo/ns-profinfo-profileinfoa"><strong>Profileinfo</strong></a><br/></td>
<td>Contiene informazioni utilizzate durante il caricamento o lo scaricamento di un profilo utente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shappmgr/ns-shappmgr-pubappinfo"><strong>PUBAPPINFO</strong></a><br/></td>
<td>Fornisce informazioni su un'applicazione pubblicata da un editore di applicazioni per <strong>Installazione</strong> applicazioni in Pannello di controllo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo"><strong>QCMINFO</strong></a><br/></td>
<td>Contiene informazioni per l'unione di voci di menu Windows menu di Esplora risorse.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-qitab"><strong>Scheda QITAB</strong></a><br/></td>
<td>Usato dalla <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-qisearch"><strong>funzione QISearch</strong></a> per descrivere una singola interfaccia.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/propidl/ns-propidl-serializedpropertyvalue"><strong>SERIALIZEDPROPERTYVALUE</strong></a><br/></td>
<td>Intervallo di memoria di tipo arbitrario che rappresenta una <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>struttura PROPVARIANT serializzata.</strong></a> I programmi non devono controllare il contenuto di <a href="/windows/win32/api/propidl/ns-propidl-serializedpropertyvalue"><strong>serializedPROPERTYVALUE</strong></a>; devono invece modificarlo con le <a href="/windows/desktop/api/propvarutil/nf-propvarutil-stgserializepropvariant"><strong>funzioni StgSerializePropVariant</strong></a> <a href="/windows/desktop/api/propvarutil/nf-propvarutil-stgdeserializepropvariant"><strong>e StgDeserializePropVariant.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfv_create"><strong>SFV_CREATE</strong></a><br/></td>
<td>Questa struttura viene usata con la <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>funzione SHCreateShellFolderView.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-sfv_setitempos"><strong>SFV_SETITEMPOS</strong></a><br/></td>
<td>Archivia le informazioni sulla posizione per un elemento. Utilizzato con il messaggio <a href="sfvm-setitempos.md"><strong>SFVM_SETITEMPOS</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data"><strong>SFVM_HELPTOPIC_DATA</strong></a><br/></td>
<td>Contiene il nome di un file della Guida HTML e di un argomento in tale file. Usato con la <a href="sfvm-gethelptopic.md"><strong>SFVM_GETHELPTOPIC</strong></a> notifica. Questa struttura richiede stringhe Unicode.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data"><strong>SFVM_PROPPAGE_DATA</strong></a><br/></td>
<td>Contiene i dettagli di una pagina da aggiungere alla finestra Proprietà <strong>di un</strong> oggetto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfo"><strong>SHARDAPPIDINFO</strong></a><br/></td>
<td>Contiene i dati <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>usati da SHAddToRecentDocs</strong></a> per identificare sia un elemento, in questo caso <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>come IShellItem,</strong></a>sia il processo a cui è associato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfoidlist"><strong>SHARDAPPIDINFOIDLIST</strong></a><br/></td>
<td>Contiene i dati usati <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>da SHAddToRecentDocs</strong></a> per identificare sia un elemento, in questo caso da un PIDL assoluto, sia il processo a cui è associato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfolink"><strong>SHARDAPPIDINFOLINK</strong></a><br/></td>
<td>Contiene i dati usati <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>da SHAddToRecentDocs</strong></a> per identificare sia un elemento, in questo caso tramite <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>un oggetto IShellLink,</strong></a>sia il processo a cui è associato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shchangenotifyentry"><strong>SHChangeNotifyEntry</strong></a><br/></td>
<td>Contiene e riceve informazioni per le notifiche di modifica. Questa struttura viene usata con la <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister"><strong>funzione SHChangeNotifyRegister</strong></a> e la <a href="sfvm-queryfsnotify.md"><strong>SFVM_QUERYFSNOTIFY</strong></a> notifica.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumndata"><strong>SHCOLUMNDATA</strong></a><br/></td>
<td>Contiene informazioni che identificano un determinato file. Viene usato da <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata"><strong>IColumnProvider::GetItemData</strong></a> quando si richiedono dati per un determinato file.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/shell/objects"><strong>SHCOLUMNID</strong></a><br/></td>
<td>Specifica l'identificatore FMTID/PID di una colonna che verrà visualizzata dalla Windows dettagli di Esplora dati. <br/>
<blockquote>
[!Note]<br />
A Windows Vista, <a href="/windows/desktop/shell/objects"><strong>SHCOLUMNID</strong></a> è considerato un formato legacy e non deve essere usato. Al suo posto, usare la <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>struttura PROPERTYKEY.</strong></a>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumninfo"><strong>SHCOLUMNINFO</strong></a><br/></td>
<td>Contiene informazioni sulle proprietà di una colonna. Viene usato da <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getcolumninfo"><strong>IColumnProvider::GetColumnInfo</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumninit"><strong>SHCOLUMNINIT</strong></a><br/></td>
<td>Passa le informazioni di <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-initialize"><strong>inizializzazione a IColumnProvider::Initialize.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shdescriptionid"><strong>SHDESCRIPTIONID</strong></a><br/></td>
<td>Riceve i dati dell'elemento in risposta a una chiamata a <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdatafromidlista"><strong>SHGetDataFromIDList.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-shdragimage"><strong>SHDRAGIMAGE</strong></a><br/></td>
<td>Contiene le informazioni necessarie per creare un'immagine di trascinamento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-shell_item_resource"><strong>SHELL_ITEM_RESOURCE</strong></a><br/></td>
<td>Definisce la risorsa dell'elemento shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-shelldetails"><strong>DETTAGLI SHELL</strong></a><br/></td>
<td>Segnala informazioni dettagliate su un elemento in una cartella shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa"><strong>SHELLEXECUTEINFO</strong></a><br/></td>
<td>Contiene informazioni usate da <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shellflagstate"><strong>SHELLFLAGSTATE</strong></a><br/></td>
<td>Contiene un set di flag che indicano le impostazioni correnti della shell. Questa struttura viene usata con la <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsettings"><strong>funzione SHGetSettings.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shellstatea"><strong>SHELLSTATE</strong></a><br/></td>
<td>Contiene le impostazioni per lo stato della shell. Questa struttura viene usata con la <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetsettings"><strong>funzione SHGetSetSettings.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shfileinfoa"><strong>SHFILEINFO</strong></a><br/></td>
<td>Contiene informazioni su un oggetto file.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa"><strong>SHFILEOPSTRUCT</strong></a><br/></td>
<td>Contiene informazioni utilizzate dalla <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>funzione SHFileOperation</strong></a> per eseguire operazioni sui file. <br/>
<blockquote>
[!Note]<br />
Al Windows Vista, è consigliabile usare <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>l'interfaccia IFileOperation</strong></a> su questa funzione.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shfoldercustomsettings"><strong>SHFOLDERCUSTOMSETTINGS</strong></a><br/></td>
<td>Contiene le impostazioni della cartella personalizzate. Questa struttura viene usata con la <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetfoldercustomsettings"><strong>funzione SHGetSetFolderCustomSettings.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a><br/></td>
<td>Definisce un identificatore di elemento.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shnamemappinga"><strong>SHNAMEMAPPING</strong></a><br/></td>
<td>Contiene i nomi di percorso nuovo e precedente per ogni file spostato, copiato o rinominato dalla <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>funzione SHFileOperation.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shqueryrbinfo"><strong>SHQUERYRBINFO</strong></a><br/></td>
<td>Contiene le informazioni sulle dimensioni e sul numero di elementi recuperate <a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryrecyclebina"><strong>dalla funzione SHQueryRecycleBin.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shstockiconinfo"><strong>SHSTOCKICONINFO</strong></a><br/></td>
<td>Riceve le informazioni usate per recuperare un'icona shell predefinita. Questa struttura viene usata in una <a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetstockiconinfo"><strong>chiamata a SHGetStockIconInfo</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shappmgr/ns-shappmgr-slowappinfo"><strong>SLOWAPPINFO</strong></a><br/></td>
<td>Fornisce informazioni specifiche sulle applicazioni <strong>per Installazione applicazioni</strong> in Pannello di controllo. Questa struttura non è applicabile alle applicazioni pubblicate.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-smcshchangenotifystruct"><strong>SMCSHCHANGENOTIFYSTRUCT</strong></a><br/></td>
<td>Contiene informazioni sulla notifica delle modifiche. Viene usato da <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm"><strong>IShellMenuCallback::CallbackSM.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata"><strong>SMDATA</strong></a><br/></td>
<td>Contiene informazioni da una banda di menu.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo"><strong>SMINFO</strong></a><br/></td>
<td>Contiene informazioni su una voce di una banda di menu.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/urlmon/ns-urlmon-softdistinfo"><strong>SOFTDISTINFO</strong></a><br/></td>
<td>Contiene informazioni su un aggiornamento software.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-sortcolumn"><strong>Sortcolumn</strong></a><br/></td>
<td>Archivia informazioni su come ordinare una colonna visualizzata nella visualizzazione cartelle.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a><br/></td>
<td>Contiene le stringhe restituite dai <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>metodi dell'interfaccia IShellFolder.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-sv2cvw2_params"><strong>SV2CVW2_PARAMS</strong></a><br/></td>
<td>Contiene i parametri per il <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview2-createviewwindow2"><strong>metodo IShellView2::CreateViewWindow2.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/shell/objects-cpp"><strong>SYNC_HANDLER_ITEM_INFO</strong></a><br/></td>
<td>Definisce un gestore per una sincronizzazione pianificata. Usato con <a href="/previous-versions/windows/desktop/isync-schedule/bb774680(v=vs.85)"><strong>ISyncSchedule::AddItem.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-syncmgr_conflict_id_info"><strong>SYNCMGR_CONFLICT_ID_INFO</strong></a><br/></td>
<td>Descrive la struttura delle informazioni sull'ID conflitto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrhandlerinfo"><strong>SYNCMGRHANDLERINFO</strong></a><br/></td>
<td>Fornisce informazioni sul gestore da usare nel <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-gethandlerinfo"><strong>metodo ISyncMgrSynchronize::GetHandlerInfo.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgritem"><strong>SYNCMGRITEM</strong></a><br/></td>
<td>Fornisce informazioni sugli elementi enumerati <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems"><strong>dall'interfaccia ISyncMgrEnumItems.</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrlogerrorinfo"><strong>SYNCMGRLOGERRORINFO</strong></a><br/></td>
<td>Fornisce informazioni sull'errore da usare <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-logerror"><strong>nel metodo ISyncMgrSynchronizeCallback::LogError.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrprogressitem"><strong>SYNCMGRPROGRESSITEM</strong></a><br/></td>
<td>Fornisce informazioni sullo stato mentre è in corso una sincronizzazione. Questa struttura viene usata con il <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-progress"><strong>metodo ISyncMgrSynchronizeCallback::P rogress</strong></a> e corrisponde a un singolo elemento di sincronizzazione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-tbinfo"><strong>TBINFO</strong></a><br/></td>
<td>Usato con la <a href="sfvm-getbuttoninfo.md"><strong>SFVM_GETBUTTONINFO</strong></a> per specificare il numero di pulsanti da aggiungere alla barra degli strumenti, nonché il modo in cui vengono aggiunti.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton"><strong>CONTROLLO THUMBBUTTON</strong></a><br/></td>
<td>Usato dai metodi <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3"><strong>dell'interfaccia ITaskbarList3</strong></a> per definire i pulsanti usati in una barra degli strumenti incorporata nella rappresentazione di anteprima di una finestra.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-wallpaperopt"><strong>WALLPAPEROPT</strong></a><br/></td>
<td>Contiene le opzioni di visualizzazione dello sfondo. Usato con i membri <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop"><strong>dell'interfaccia IActiveDesktop.</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Tlogstg/ns-tlogstg-windowdata"><strong>WINDOWDATA</strong></a><br/></td>
<td>Archivia i dati della finestra.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Thumbcache/ne-thumbcache-wts_contextflags"><strong>WTS_CONTEXTFLAGS</strong></a><br/></td>
<td>Specifica il contesto di un'estrazione di anteprime. Usato da <a href="/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailsettings-setcontext"><strong>IThumbnailSettings::SetContext</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Thumbcache/ne-thumbcache-wts_flags"><strong>WTS_FLAGS</strong></a><br/></td>
<td>Valori usati da <a href="/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailcache-getthumbnail"><strong>IThumbnailCache::GetThumbnail</strong></a> per specificare le opzioni per l'estrazione e la visualizzazione dell'immagine di anteprima.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Thumbcache/ns-thumbcache-wts_thumbnailid"><strong>WTS_THUMBNAILID</strong></a><br/></td>
<td>Contiene un identificatore univoco per un'anteprima nella cache delle anteprime di sistema.<br/></td>
</tr>
</tbody>
</table>



 

 

 

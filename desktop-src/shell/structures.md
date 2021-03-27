---
description: In questa sezione vengono descritte le strutture della shell di Windows.
title: Strutture della shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 814ae153-39b3-49ee-9da1-efe7e649c73e
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5bbda4cd81c3db2dff664b9d16d2db60aa8f12f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980802"
---
# <a name="shell-structures"></a>Strutture della shell

In questa sezione vengono descritte le strutture della shell di Windows.

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
<td>Struttura a dimensione variabile che contiene informazioni su un nome di file di menu.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj/ns-shlobj-aashellmenuitem"><strong>AASHELLMENUITEM</strong></a><br/></td>
<td>Contiene informazioni su una voce di menu.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-appbardata"><strong>APPBARDATA</strong></a><br/></td>
<td>Contiene informazioni su un messaggio AppBar di sistema.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfo"><strong>APPCATEGORYINFO</strong></a><br/></td>
<td>Fornisce informazioni sulla categoria dell'applicazione per aggiungere/rimuovere programmi nel pannello di controllo. La struttura <a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfolist"><strong>APPCATEGORYINFOLIST</strong></a> viene utilizzata per creare un elenco completo di categorie per un server di pubblicazione dell'applicazione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Appmgmt/ns-appmgmt-appcategoryinfolist"><strong>APPCATEGORYINFOLIST</strong></a><br/></td>
<td>Fornisce un elenco di categorie di applicazioni supportate da un autore dell'applicazione per aggiungere/rimuovere programmi nel pannello di controllo. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shappmgr/ns-shappmgr-appinfodata"><strong>APPINFODATA</strong></a><br/></td>
<td>Fornisce informazioni su un'applicazione pubblicata all'utilità pannello di controllo Installazione applicazioni.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-associationelement"><strong>ASSOCIATIONelement</strong></a><br/></td>
<td>Definisce le informazioni utilizzate da <a href="/windows/desktop/api/Shellapi/nf-shellapi-assoccreateforclasses"><strong>AssocCreateForClasses</strong></a> per recuperare un'interfaccia <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>IQueryAssociations</strong></a> per un'associazione di file specificata.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-bandinfosfb"><strong>BANDINFOSFB</strong></a><br/></td>
<td>Contiene informazioni su una banda di cartelle. Questa struttura viene utilizzata con i metodi <a href="/windows/desktop/api/shlobj/nf-shlobj-ishellfolderband-getbandinfosfb"><strong>IShellFolderBand:: GetBandInfoSFB</strong></a> e <a href="/windows/desktop/api/shlobj/nf-shlobj-ishellfolderband-setbandinfosfb"><strong>IShellFolderBand:: SetBandInfoSFB</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-bandsiteinfo"><strong>BANDSITEINFO</strong></a><br/></td>
<td>Contiene informazioni su un sito della banda. Questa struttura viene utilizzata con i metodi <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-getbandsiteinfo"><strong>IBandSite:: GetBandSiteInfo</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibandsite-setbandsiteinfo"><strong>IBandSite:: SetBandSiteInfo</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shdeprecated/ns-shdeprecated-basebrowserdatalh"><strong>BASEBROWSERDATA</strong></a><br/></td>
<td>Contiene membri protetti della classe di base. <a href="/windows/desktop/api/Shdeprecated/ns-shdeprecated-basebrowserdatalh"><strong>BASEBROWSERDATA</strong></a> definisce lo stato del browser e viene usato con <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-getbasebrowserdata"><strong>IBrowserService2:: GetBaseBrowserData</strong></a> e <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-putbasebrowserdata"><strong>IBrowserService2::P utbasebrowserdata</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/cc136564(v=vs.85)"><strong>BORDERWIDTHS</strong></a><br/></td>
<td>Definisce le coordinate degli angoli superiore sinistro e inferiore destro di un rettangolo del bordo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa"><strong>BROWSEINFO</strong></a><br/></td>
<td>Contiene i parametri per la funzione <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera"><strong>SHBrowseForFolder</strong></a> e riceve informazioni sulla cartella selezionata dall'utente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-category_info"><strong>CATEGORY_INFO</strong></a><br/></td>
<td>Contiene informazioni sulla categoria. Una categoria di componenti è un gruppo di classi COM (Component Object Model) correlate logicamente che condividono un identificatore di categoria comune (CATId).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-cida"><strong>CIDA</strong></a><br/></td>
<td>Utilizzato con il formato degli Appunti <a href="clipboard.md">CFSTR_SHELLIDLIST</a> per trasferire il puntatore a un elenco di identificatori di elemento (PIDL) di uno o più oggetti dello spazio dei nomi della shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo"><strong>CM_COLUMNINFO</strong></a><br/></td>
<td>Definisce le informazioni sulle colonne. Utilizzato dai membri dell'interfaccia <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>icolumnmanager</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>CMINVOKECOMMANDINFO</strong></a><br/></td>
<td>Contiene le informazioni necessarie per <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand"><strong>IContextMenu:: InvokeCommand</strong></a> per richiamare un comando di menu di scelta rapida.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex"><strong>CMINVOKECOMMANDINFOEX</strong></a><br/></td>
<td>Contiene informazioni estese su un comando di menu di scelta rapida. Questa struttura è una versione estesa di <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>CMINVOKECOMMANDINFO</strong></a> che consente l'utilizzo di valori Unicode.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec"><strong>COMDLG_FILTERSPEC</strong></a><br/></td>
<td>Utilizzato in modo generico per filtrare gli elementi.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-component"><strong>COMPONENTE</strong></a><br/></td>
<td>Utilizzato da Windows 2000 per conservare informazioni su un componente. Questa struttura sostituisce la struttura <a href="/windows/win32/api/shlobj_core/ns-shlobj_core-ie4component"><strong>IE4COMPONENT</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-componentsopt"><strong>COMPONENTSOPT</strong></a><br/></td>
<td>Contiene le opzioni per gli elementi del desktop.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-comppos"><strong>COMPPOS</strong></a><br/></td>
<td>Include informazioni sulla posizione e le dimensioni di un componente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-compstateinfo"><strong>COMPSTATEINFO</strong></a><br/></td>
<td>Utilizzato da Windows 2000 per conservare informazioni sullo stato di un componente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-confirm_conflict_item"><strong>CONFIRM_CONFLICT_ITEM</strong></a><br/></td>
<td>Definisce la struttura degli elementi dei conflitti.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-confirm_conflict_result_info"><strong>CONFIRM_CONFLICT_RESULT_INFO</strong></a><br/></td>
<td>Definisce la struttura delle informazioni sui risultati dei conflitti.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/cpl/ns-cpl-cplinfo"><strong>CPLINFO</strong></a><br/></td>
<td>Contiene informazioni sulle risorse e un valore definito dall'applicazione per una finestra di dialogo supportata da un'applicazione del pannello di controllo. La funzione <a href="/windows/desktop/api/cpl/nc-cpl-applet_proc"><strong>CPlApplet</strong></a> dell'applicazione del pannello di controllo restituisce queste informazioni al pannello di controllo in risposta a un messaggio di <a href="cpl-inquire.md"><strong>CPL_INQUIRE</strong></a> .<br/></td>
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
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-csfv"><strong>PESTE suina classica</strong></a><br/></td>
<td>Utilizzato con la funzione <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex"><strong>SHCreateShellFolderViewEx</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-datablock_header"><strong>DATABLOCK_HEADER</strong></a><br/></td>
<td>Funge da intestazione per alcune delle strutture di dati aggiuntive utilizzate da <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu"><strong>DEFCONTEXTMENU</strong></a><br/></td>
<td>Contiene informazioni sul menu di scelta rapida utilizzate da <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu"><strong>SHCreateDefaultContextMenu</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-delegateitemid"><strong>DELEGATEITEMID</strong></a><br/></td>
<td>Utilizzato dalle cartelle delegate al posto di una struttura di <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ID</strong></a> oggetto standard.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo"><strong>DETAILSINFO</strong></a><br/></td>
<td>Contiene informazioni dettagliate per un elemento della cartella della shell. Utilizzato con la notifica <a href="sfvm-getdetailsof.md"><strong>SFVM_GETDETAILSOF</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dfmics"><strong>DFMICS</strong></a><br/></td>
<td>Contiene argomenti aggiuntivi utilizzati da <a href="dfm-invokecommandex.md"><strong>DFM_INVOKECOMMANDEX</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo"><strong>DLLVERSIONINFO</strong></a><br/></td>
<td>Riceve informazioni sulla versione specifiche della DLL. Viene usato con la funzione <a href="/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc"><strong>DllGetVersion</strong></a> . <br/>
<blockquote>
[!Note]<br />
Al posto di questa struttura, è possibile usare la struttura <a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2"><strong>DLLVERSIONINFO2</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2"><strong>DLLVERSIONINFO2</strong></a><br/></td>
<td>Riceve informazioni sulla versione specifiche della DLL. Viene usato con la funzione <a href="/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc"><strong>DllGetVersion</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription"><strong>DROPDESCRIPTION</strong></a><br/></td>
<td>Descrive l'immagine e il testo associato per un oggetto Drop.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dropfiles"><strong>DROPFILES</strong></a><br/></td>
<td>Definisce il formato degli Appunti <a href="clipboard.md">CF_HDROP</a> . I dati seguenti sono un doppio elenco di nomi di file con terminazione null.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_darwin_link"><strong>EXP_DARWIN_LINK</strong></a><br/></td>
<td>Include un blocco di dati aggiuntivo usato da <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>. Che include l'ID Windows Installer del collegamento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_propertystorage"><strong>EXP_PROPERTYSTORAGE</strong></a><br/></td>
<td>Archivia informazioni sullo stato del collegamento della shell. Questa struttura viene utilizzata per sezioni di dati aggiuntive contrassegnate con EXP_PROPERTYSTORAGE_SIG.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_special_folder"><strong>EXP_SPECIAL_FOLDER</strong></a><br/></td>
<td>Include un blocco di dati aggiuntivo usato da <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>. Include informazioni speciali sulla cartella.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-exp_sz_link"><strong>EXP_SZ_LINK</strong></a><br/></td>
<td>Include un blocco di dati aggiuntivo usato da <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>. Include le stringhe di ambiente espandibili per l'icona o la destinazione.<br/></td>
</tr>
<tr class="even">
<td><a href="ext-button.md"><strong>EXT_BUTTON</strong></a><br/></td>
<td>Contiene informazioni su un pulsante aggiunto da una DLL di estensione di file Manager alla barra degli strumenti di gestione file.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-extrasearch"><strong>EXTRASEARCH</strong></a><br/></td>
<td>Usato da un oggetto enumeratore <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumextrasearch"><strong>IEnumExtraSearch</strong></a> per restituire informazioni sugli oggetti di ricerca supportati da un oggetto cartella della shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-file_attributes_array"><strong>FILE_ATTRIBUTES_ARRAY</strong></a><br/></td>
<td>Contiene la definizione di formato degli Appunti per CFSTR_FILE_ATTRIBUTES_ARRAY.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-filedescriptora"><strong>FILEDESCRIPTOR</strong></a><br/></td>
<td>Descrive le proprietà di un file che viene copiato tramite gli appunti durante un'operazione di <a href="dragdrop.md">trascinamento e rilascio</a> di Microsoft ActiveX.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-filegroupdescriptora"><strong>FILEGROUPDESCRIPTOR</strong></a><br/></td>
<td>Definisce il formato degli Appunti CF_FILEGROUPDESCRIPTOR.<br/></td>
</tr>
<tr class="odd">
<td><a href="fms-getdriveinfo.md"><strong>FMS_GETDRIVEINFO</strong></a><br/></td>
<td>Contiene informazioni sull'unità selezionata nella finestra Active File Manager (la finestra Directory o la finestra dei risultati della ricerca).<br/></td>
</tr>
<tr class="even">
<td><a href="fms-getfilesel.md"><strong>FMS_GETFILESEL</strong></a><br/></td>
<td>Contiene informazioni su un file selezionato nella finestra Active File Manager (la finestra Directory o la finestra dei risultati della ricerca).<br/></td>
</tr>
<tr class="odd">
<td><a href="fms-helpstring.md"><strong>FMS_HELPSTRING</strong></a><br/></td>
<td>Contiene informazioni utilizzate da Gestione file per aggiungere una stringa della Guida per un elemento di comando di menu o barre degli strumenti.<br/></td>
</tr>
<tr class="even">
<td><a href="fms-load.md"><strong>FMS_LOAD</strong></a><br/></td>
<td>Contiene informazioni utilizzate da Gestione file per aggiungere un menu personalizzato fornito da una DLL di estensione di file Manager. La struttura fornisce inoltre un valore Delta che può essere utilizzato dalla DLL di estensione per modificare il menu personalizzato dopo che il menu è stato caricato da file Manager.<br/></td>
</tr>
<tr class="odd">
<td><a href="fms-toolbarload.md"><strong>FMS_TOOLBARLOAD</strong></a><br/></td>
<td>Contiene informazioni sui pulsanti personalizzati da aggiungere alla barra degli strumenti di gestione file. I pulsanti sono forniti da una DLL di estensione di file Manager.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings"><strong>FOLDERSETTINGS</strong></a><br/></td>
<td>Contiene informazioni sulla visualizzazione cartelle.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-fvshowinfo"><strong>FVSHOWINFO</strong></a><br/></td>
<td>Contiene informazioni utilizzate dal Visualizzatore file per visualizzare un file.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/winuser/ns-winuser-helpinfo"><strong>HELPINFO</strong></a><br/></td>
<td>Contiene informazioni su un elemento per il quale è stata richiesta la Guida sensibile al contesto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/winuser/ns-winuser-helpwininfow"><strong>HELPWININFO</strong></a><br/></td>
<td>Contiene le dimensioni e la posizione di una finestra della guida primaria o secondaria. Un'applicazione può impostare queste informazioni chiamando la funzione <a href="/windows/desktop/api/Winuser/nf-winuser-winhelpa"><strong>WinHelp</strong></a> con il valore HELP_SETWINPOS.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-ie4component"><strong>IE4COMPONENT</strong></a><br/></td>
<td>Utilizzato da Microsoft Internet Explorer 4,0 e Microsoft Internet Explorer 4,01 per conservare informazioni su un componente. Con Windows 2000, viene sostituito dalla struttura del <a href="/windows/win32/api/shlobj_core/ns-shlobj_core-component"><strong>componente</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ITEMIDLIST</strong></a><br/></td>
<td>Contiene un elenco di identificatori di elemento.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-itemspacing"><strong>ITEMSPACING</strong></a><br/></td>
<td>Archivia le dimensioni delle due possibili dimensioni della spaziatura delle icone disponibili per la visualizzazione: piccola e grande. Usato da <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ishellfolderview-getitemspacing"><strong>IShellFolderView:: GetItemSpacing</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition"><strong>KNOWNFOLDER_DEFINITION</strong></a><br/></td>
<td>Definisce le specifiche di una cartella nota.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shtypes/ns-shtypes-logfontw"><strong>LOGFONT</strong></a><br/></td>
<td>Definisce gli attributi di un tipo di carattere.<br/></td>
</tr>
<tr class="odd">
<td><a href="mruinfo.md"><strong>MRUINFO</strong></a><br/></td>
<td>Contiene informazioni che definiscono un nuovo elenco utilizzato più di recente (MRU). Usato da <a href="createmrulist.md"><strong>CreateMRUListW</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/winuser/ns-winuser-multikeyhelpw"><strong>MULTIKEYHELP</strong></a><br/></td>
<td>Specifica una parola chiave da cercare e la tabella delle parole chiave in cui eseguire la ricerca tramite la Guida di Windows.<br/></td>
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
<td>Contiene informazioni sulle risorse e un valore definito dall'applicazione per una finestra di dialogo supportata da un'applicazione del pannello di controllo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa"><strong>NOTIFYICONDATA</strong></a><br/></td>
<td>Contiene le informazioni necessarie al sistema per visualizzare le notifiche nell'area di notifica. Utilizzato dal <a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona"><strong>Shell_NotifyIcon</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-notifyiconidentifier"><strong>NOTIFYICONIDENTIFIER</strong></a><br/></td>
<td>Contiene informazioni utilizzate da <a href="/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect"><strong>Shell_NotifyIconGetRect</strong></a> per identificare l'icona per la quale recuperare il rettangolo di delimitazione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nresarray"><strong>NRESARRAY</strong></a><br/></td>
<td>Definisce il formato degli Appunti CF_NETRESOURCE.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/ns-shobjidl-nstccustomdraw"><strong>NSTCCUSTOMDRAW</strong></a><br/></td>
<td>Struttura di disegni personalizzata utilizzata dai metodi <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrolcustomdraw"><strong>INameSpaceTreeControlCustomDraw</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nt_console_props"><strong>NT_CONSOLE_PROPS</strong></a><br/></td>
<td>Include un blocco di dati aggiuntivo usato da <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>. Include le proprietà della console.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-nt_fe_console_props"><strong>NT_FE_CONSOLE_PROPS</strong></a><br/></td>
<td>Include un blocco di dati aggiuntivo usato da <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a>. Che include la tabella codici della console.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-open_printer_props_infoa"><strong>OPEN_PRINTER_PROPS_INFO</strong></a><br/></td>
<td>Identifica una particolare finestra delle proprietà nelle pagine delle proprietà di una stampante e indica se la finestra delle proprietà deve essere modale. Utilizzato facoltativamente con la funzione <a href="/windows/desktop/api/Shellapi/nf-shellapi-shinvokeprintercommanda"><strong>SHInvokePrinterCommand</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-openasinfo"><strong>OPENASINFO</strong></a><br/></td>
<td>Archivia le informazioni per la funzione <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shopenwithdialog"><strong>SHOpenWithDialog</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/ns-shobjidl-overlapped"><strong>OVERLAPPED</strong></a><br/></td>
<td>Contiene informazioni utilizzate in input/output (I/O) asincrono (sovrapposto).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlwapi/ns-shlwapi-parsedurlw"><strong>PARSEDURL</strong></a><br/></td>
<td>Usato dalla funzione <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-parseurla"><strong>parseURL</strong></a> per restituire l'URL analizzato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-persist_folder_target_info"><strong>PERSIST_FOLDER_TARGET_INFO</strong></a><br/></td>
<td>Specifica la cartella di destinazione del collegamento alla cartella e i relativi attributi. Questa struttura viene utilizzata da <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-getfoldertargetinfo"><strong>IPersistFolder3:: GetFolderTargetInfo</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-initializeex"><strong>IPersistFolder3:: InitializeEx</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-previewhandlerframeinfo"><strong>PREVIEWHANDLERFRAMEINFO</strong></a><br/></td>
<td>Struttura della tabella dei tasti di scelta rapida. Usato da <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandlerframe-getwindowcontext"><strong>IPreviewHandlerFrame:: GetWindowContext</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Profinfo/ns-profinfo-profileinfoa"><strong>PROFILEINFO</strong></a><br/></td>
<td>Contiene informazioni utilizzate per il caricamento o lo scaricamento di un profilo utente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shappmgr/ns-shappmgr-pubappinfo"><strong>PUBAPPINFO</strong></a><br/></td>
<td>Fornisce informazioni su un'applicazione pubblicata da un autore dell'applicazione per <strong>aggiungere/rimuovere programmi</strong> nel pannello di controllo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo"><strong>QCMINFO</strong></a><br/></td>
<td>Contiene informazioni per unire voci di menu nei menu di Esplora risorse.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ns-shlwapi-qitab"><strong>QITAB</strong></a><br/></td>
<td>Usato dalla funzione <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-qisearch"><strong>QISearch</strong></a> per descrivere una singola interfaccia.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/propidl/ns-propidl-serializedpropertyvalue"><strong>SERIALIZEDPROPERTYVALUE</strong></a><br/></td>
<td>Intervallo di memoria di tipo arbitrario che rappresenta una struttura <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> serializzata. I programmi non devono esaminare il contenuto di un <a href="/windows/win32/api/propidl/ns-propidl-serializedpropertyvalue"><strong>SERIALIZEDPROPERTYVALUE</strong></a>; devono invece manipolarla con le funzioni <a href="/windows/desktop/api/propvarutil/nf-propvarutil-stgserializepropvariant"><strong>StgSerializePropVariant</strong></a> e <a href="/windows/desktop/api/propvarutil/nf-propvarutil-stgdeserializepropvariant"><strong>StgDeserializePropVariant</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfv_create"><strong>SFV_CREATE</strong></a><br/></td>
<td>Questa struttura viene utilizzata con la funzione <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>SHCreateShellFolderView</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-sfv_setitempos"><strong>SFV_SETITEMPOS</strong></a><br/></td>
<td>Archivia le informazioni sulla posizione per un elemento. Utilizzato con <a href="sfvm-setitempos.md"><strong>SFVM_SETITEMPOS</strong></a>del messaggio.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data"><strong>SFVM_HELPTOPIC_DATA</strong></a><br/></td>
<td>Contiene il nome di un file della Guida HTML e un argomento in tale file. Utilizzato con la notifica <a href="sfvm-gethelptopic.md"><strong>SFVM_GETHELPTOPIC</strong></a> . Questa struttura richiede stringhe Unicode.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data"><strong>SFVM_PROPPAGE_DATA</strong></a><br/></td>
<td>Contiene i dettagli di una pagina da aggiungere alla finestra delle <strong>Proprietà</strong> di un oggetto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfo"><strong>SHARDAPPIDINFO</strong></a><br/></td>
<td>Contiene i dati utilizzati da <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>funzione SHAddToRecentDocs</strong></a> per identificare un elemento, in questo caso come <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>, e il processo a cui è associato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfoidlist"><strong>SHARDAPPIDINFOIDLIST</strong></a><br/></td>
<td>Contiene i dati utilizzati da <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>funzione SHAddToRecentDocs</strong></a> per identificare un elemento, in questo caso da un PIDL assoluto, e il processo a cui è associato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shardappidinfolink"><strong>SHARDAPPIDINFOLINK</strong></a><br/></td>
<td>Contiene i dati utilizzati da <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>funzione SHAddToRecentDocs</strong></a> per identificare un elemento, in questo caso tramite un <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a>, e il processo a cui è associato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shchangenotifyentry"><strong>SHChangeNotifyEntry</strong></a><br/></td>
<td>Contiene e riceve informazioni per le notifiche di modifica. Questa struttura viene utilizzata con la funzione <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotifyregister"><strong>SHChangeNotifyRegister</strong></a> e la notifica <a href="sfvm-queryfsnotify.md"><strong>SFVM_QUERYFSNOTIFY</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumndata"><strong>SHCOLUMNDATA</strong></a><br/></td>
<td>Contiene informazioni che identificano un determinato file. Viene usato da <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata"><strong>IColumnProvider:: GetItemData</strong></a> durante la richiesta di dati per un file specifico.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/shell/objects"><strong>SHCOLUMNID</strong></a><br/></td>
<td>Specifica l'identificatore FMTID/PID di una colonna che verrà visualizzata dalla visualizzazione dettagli di Esplora risorse. <br/>
<blockquote>
[!Note]<br />
A partire da Windows Vista, <a href="/windows/desktop/shell/objects"><strong>SHCOLUMNID</strong></a> è considerato un modulo legacy e non deve essere utilizzato. Al suo posto, utilizzare la struttura <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PropertyKey</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumninfo"><strong>SHCOLUMNINFO</strong></a><br/></td>
<td>Contiene informazioni sulle proprietà di una colonna. Viene usato da <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getcolumninfo"><strong>IColumnProvider:: GetColumnInfo</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumninit"><strong>SHCOLUMNINIT</strong></a><br/></td>
<td>Passa le informazioni di inizializzazione a <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-initialize"><strong>IColumnProvider:: Initialize</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shdescriptionid"><strong>SHDESCRIPTIONID</strong></a><br/></td>
<td>Riceve i dati dell'elemento in risposta a una chiamata a <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdatafromidlista"><strong>SHGetDataFromIDList</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-shdragimage"><strong>SHDRAGIMAGE</strong></a><br/></td>
<td>Contiene le informazioni necessarie per creare un'immagine di trascinamento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-shell_item_resource"><strong>SHELL_ITEM_RESOURCE</strong></a><br/></td>
<td>Definisce la risorsa dell'elemento della shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-shelldetails"><strong>SHELLDETAILS</strong></a><br/></td>
<td>Riporta informazioni dettagliate su un elemento in una cartella della shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa"><strong>SHELLEXECUTEINFO</strong></a><br/></td>
<td>Contiene le informazioni utilizzate da <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shellflagstate"><strong>SHELLFLAGSTATE</strong></a><br/></td>
<td>Contiene un set di flag che indicano le impostazioni della shell corrente. Questa struttura viene utilizzata con la funzione <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsettings"><strong>SHGetSettings</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shellstatea"><strong>SHELLSTATE</strong></a><br/></td>
<td>Contiene le impostazioni per lo stato della shell. Questa struttura viene utilizzata con la funzione <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetsettings"><strong>SHGetSetSettings</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shfileinfoa"><strong>SHFILEINFO</strong></a><br/></td>
<td>Contiene informazioni su un oggetto file.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa"><strong>SHFILEOPSTRUCT</strong></a><br/></td>
<td>Contiene informazioni utilizzate dalla funzione <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a> per eseguire operazioni sui file. <br/>
<blockquote>
[!Note]<br />
A partire da Windows Vista, è consigliabile usare l'interfaccia <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>IFileOperation</strong></a> per questa funzione.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shfoldercustomsettings"><strong>SHFOLDERCUSTOMSETTINGS</strong></a><br/></td>
<td>Include le impostazioni della cartella personalizzata. Questa struttura viene utilizzata con la funzione <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetfoldercustomsettings"><strong>SHGetSetFolderCustomSettings</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-shitemid"><strong>SHITEMID</strong></a><br/></td>
<td>Definisce un identificatore di elemento.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shnamemappinga"><strong>SHNAMEMAPPING</strong></a><br/></td>
<td>Contiene i nomi di percorso vecchi e nuovi per ogni file che è stato spostato, copiato o rinominato dalla funzione <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shqueryrbinfo"><strong>SHQUERYRBINFO</strong></a><br/></td>
<td>Contiene le informazioni sulle dimensioni e sul conteggio degli elementi recuperate dalla funzione <a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryrecyclebina"><strong>SHQueryRecycleBin</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ns-shellapi-shstockiconinfo"><strong>SHSTOCKICONINFO</strong></a><br/></td>
<td>Riceve le informazioni utilizzate per recuperare un'icona della shell della borsa. Questa struttura viene utilizzata in una chiamata <a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetstockiconinfo"><strong>SHGetStockIconInfo</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shappmgr/ns-shappmgr-slowappinfo"><strong>SLOWAPPINFO</strong></a><br/></td>
<td>Fornisce informazioni specializzate sull'applicazione per <strong>aggiungere/rimuovere programmi</strong> nel pannello di controllo. Questa struttura non è applicabile alle applicazioni pubblicate.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-smcshchangenotifystruct"><strong>SMCSHCHANGENOTIFYSTRUCT</strong></a><br/></td>
<td>Contiene informazioni sulla notifica delle modifiche. Viene usato da <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm"><strong>IShellMenuCallback:: CallbackSM</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata"><strong>SMDATA</strong></a><br/></td>
<td>Contiene informazioni di una banda di menu.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo"><strong>SMINFO</strong></a><br/></td>
<td>Contiene informazioni su un elemento di una banda di menu.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/urlmon/ns-urlmon-softdistinfo"><strong>SOFTDISTINFO</strong></a><br/></td>
<td>Contiene informazioni su un aggiornamento software.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-sortcolumn"><strong>SORTCOLUMN</strong></a><br/></td>
<td>Archivia le informazioni su come ordinare una colonna visualizzata nella visualizzazione cartelle.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a><br/></td>
<td>Contiene le stringhe restituite dai metodi dell'interfaccia <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-sv2cvw2_params"><strong>SV2CVW2_PARAMS</strong></a><br/></td>
<td>Include i parametri per il metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview2-createviewwindow2"><strong>IShellView2:: CreateViewWindow2</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/shell/objects-cpp"><strong>SYNC_HANDLER_ITEM_INFO</strong></a><br/></td>
<td>Definisce un gestore per una sincronizzazione pianificata. Usato con <a href="/previous-versions/windows/desktop/isync-schedule/bb774680(v=vs.85)"><strong>ISyncSchedule:: AddItem</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ns-syncmgr-syncmgr_conflict_id_info"><strong>SYNCMGR_CONFLICT_ID_INFO</strong></a><br/></td>
<td>Descrive la struttura delle informazioni sull'ID dei conflitti.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrhandlerinfo"><strong>SYNCMGRHANDLERINFO</strong></a><br/></td>
<td>Fornisce informazioni sul gestore da usare nel metodo <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-gethandlerinfo"><strong>ISyncMgrSynchronize:: GetHandlerInfo</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgritem"><strong>SYNCMGRITEM</strong></a><br/></td>
<td>Fornisce informazioni sugli elementi enumerati dall'interfaccia <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems"><strong>ISyncMgrEnumItems</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrlogerrorinfo"><strong>SYNCMGRLOGERRORINFO</strong></a><br/></td>
<td>Fornisce informazioni sull'errore da utilizzare nel metodo <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-logerror"><strong>ISyncMgrSynchronizeCallback:: LogError</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrprogressitem"><strong>SYNCMGRPROGRESSITEM</strong></a><br/></td>
<td>Fornisce informazioni sullo stato mentre è in corso una sincronizzazione. Questa struttura viene utilizzata con il metodo <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-progress"><strong>ISyncMgrSynchronizeCallback::P rogress</strong></a> e corrisponde a un singolo elemento di sincronizzazione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlobj/ns-shlobj-tbinfo"><strong>TBINFO</strong></a><br/></td>
<td>Utilizzato con la notifica di <a href="sfvm-getbuttoninfo.md"><strong>SFVM_GETBUTTONINFO</strong></a> per specificare il numero di pulsanti da aggiungere alla barra degli strumenti e il modo in cui vengono aggiunti.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton"><strong>THUMBBUTTON</strong></a><br/></td>
<td>Utilizzato dai metodi dell'interfaccia <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3"><strong>all'ITaskbarList3</strong></a> per definire i pulsanti utilizzati in una barra degli strumenti incorporata nella rappresentazione di anteprima di una finestra.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-wallpaperopt"><strong>WALLPAPEROPT</strong></a><br/></td>
<td>Contiene le opzioni di visualizzazione dello sfondo. Utilizzato con i membri dell'interfaccia <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop"><strong>IActiveDesktop</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Tlogstg/ns-tlogstg-windowdata"><strong>WINDOWDATA</strong></a><br/></td>
<td>Archivia i dati della finestra.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Thumbcache/ne-thumbcache-wts_contextflags"><strong>WTS_CONTEXTFLAGS</strong></a><br/></td>
<td>Specifica il contesto di un'estrazione di anteprime. Utilizzato da <a href="/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailsettings-setcontext"><strong>IThumbnailSettings:: secontext</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Thumbcache/ne-thumbcache-wts_flags"><strong>WTS_FLAGS</strong></a><br/></td>
<td>Valori usati da <a href="/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailcache-getthumbnail"><strong>IThumbnailCache:: GetThumbnail</strong></a> per specificare le opzioni per l'estrazione e la visualizzazione dell'immagine di anteprima.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Thumbcache/ns-thumbcache-wts_thumbnailid"><strong>WTS_THUMBNAILID</strong></a><br/></td>
<td>Contiene un identificatore univoco per un'anteprima nella cache delle anteprime di sistema.<br/></td>
</tr>
</tbody>
</table>



 

 

 

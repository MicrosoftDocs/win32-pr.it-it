---
description: Set di chiavi stringa usate con il metodo IBindCtx::RegisterObjectParam per specificare un contesto di associazione.
title: Associare chiavi stringa di contesto (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d89a0ee1-9a4b-48a4-8965-0d92f09743a6
api_name:
- STR_AVOID_DRIVE_RESTRICTION_POLICY
- STR_BIND_DELEGATE_CREATE_OBJECT
- STR_BIND_FOLDER_ENUM_MODE
- STR_BIND_FOLDERS_READ_ONLY
- STR_BIND_FORCE_FOLDER_SHORTCUT_RESOLVE
- STR_DONT_PARSE_RELATIVE
- STR_DONT_RESOLVE_LINK
- STR_FILE_SYS_FIND_DATA
- STR_FILE_SYS_BIND_DATA_WIN7_FORMAT
- STR_GET_ASYNC_HANDLER
- STR_GPS_BESTEFFORT
- STR_GPS_DELAYCREATION
- STR_GPS_FASTPROPERTIESONLY
- STR_GPS_HANDLERPROPERTIESONLY
- STR_GPS_NO_OPLOCK
- STR_GPS_OPENSLOWITEM
- STR_IFILTER_FORCE_TEXT_FILTER_FALLBACK
- STR_IFILTER_LOAD_DEFINED_FILTER
- STR_INTERNAL_NAVIGATE
- STR_INTERNETFOLDER_PARSE_ONLY_URLMON_BINDABLE
- STR_ITEM_CACHE_CONTEXT
- STR_NO_VALIDATE_FILENAME_CHARS
- STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS
- STR_PARSE_AND_CREATE_ITEM
- STR_PARSE_DONT_REQUIRE_VALIDATED_URLS
- STR_PARSE_PARTIAL_IDLIST
- STR_PARSE_PREFER_FOLDER_BROWSING
- STR_PARSE_PREFER_WEB_BROWSING
- STR_PARSE_PROPERTYSTORE
- STR_PARSE_SHELL_PROTOCOL_TO_FILE_OBJECTS
- STR_PARSE_SHOW_NET_DIAGNOSTICS_UI
- STR_PARSE_SKIP_NET_CACHE
- STR_PARSE_TRANSLATE_ALIASES
- STR_PARSE_WITH_PROPERTIES
- STR_PROPERTYBAG_PARAM
- STR_SKIP_BINDING_CLSID
- STR_TRACK_CLSID
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 78743f18f9dc10b9c20b7e911224f1cd4e53e3f536f23686936a8f021605bf9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452048"
---
# <a name="bind-context-string-keys"></a>Associare chiavi stringa di contesto

Set di chiavi stringa usate con il [**metodo IBindCtx::RegisterObjectParam**](/windows/win32/api/objidl/nf-objidl-ibindctx-registerobjectparam) per specificare un contesto di associazione.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Costante</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="STR_AVOID_DRIVE_RESTRICTION_POLICY"></span><span id="str_avoid_drive_restriction_policy"></span><dl> <dt><strong>STR_AVOID_DRIVE_RESTRICTION_POLICY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows XP SP2.</strong> Specificare questo contesto di associazione per consentire ai client dell'origine dati di eseguire l'override dei criteri delle lettere di unità nascoste e abilitare l'accesso agli oggetti di visualizzazione per le origini dati nelle unità bloccate.<br/> Usato con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a> o <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem::BindToHandler</strong></a>.<br/> Il sistema supporta criteri controllati dall'amministratore che nascondono lettere di unità specificate per impedire agli utenti di accedere a tali unità tramite Windows Explorer. Quando questo criterio è attivo, il risultato è che gli oggetti di visualizzazione e altri gestori creati con il metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject"><strong>IShellFolder::CreateViewObject</strong></a> avranno esito negativo quando vengono chiamati su unità bloccate dai criteri.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_BIND_DELEGATE_CREATE_OBJECT"></span><span id="str_bind_delegate_create_object"></span><dl> <dt><strong>STR_BIND_DELEGATE_CREATE_OBJECT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows Vista</strong>. Specificare questo contesto di associazione per fare in modo che il metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a> usi l'oggetto specificato dal <em>parametro pbc</em> per creare l'oggetto di destinazione. In questo caso, l'oggetto specificato dal <em>parametro punk</em> nella chiamata <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam"><strong>IBindCtx::RegisterObjectParam</strong></a> deve implementare <a href="/windows/desktop/api/Propsys/nn-propsys-icreateobject"><strong>l'interfaccia ICreateObject.</strong></a> <br/> Usato con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a> o <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem::BindToHandler</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_BIND_FOLDER_ENUM_MODE"></span><span id="str_bind_folder_enum_mode"></span><dl> <dt><strong>STR_BIND_FOLDER_ENUM_MODE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows 7</strong>. Passato a <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a> con <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folder_enum_mode"><strong></strong></a> un valore FOLDER_ENUM_MODE per controllare la modalità di enumerazione dell'elemento analizzato. Il <strong>FOLDER_ENUM_MODE</strong> viene passato nel contesto di associazione tramite un oggetto che implementa <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithfolderenummode"><strong>IObjectWithFolderEnumMode</strong></a>. <br/> Gli elementi con modalità di enumerazione diverse vengono confrontati in modo canonico (SHCIDS_CANONICALONLY) in quanto enumerano set diversi di elementi.<br/> Se un elemento non supporta la modalità di enumerazione (perché non è una cartella o non fornisce la modalità di enumerazione), viene creato nella modalità di enumerazione predefinita.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_BIND_FOLDERS_READ_ONLY"></span><span id="str_bind_folders_read_only"></span><dl> <dt><strong>STR_BIND_FOLDERS_READ_ONLY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows 7</strong>. Passato a <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a> insieme <strong>a STR_FILE_SYS_BIND_DATA</strong>. In questo modo viene forzata l'analisi semplice e viene anche Desktop.ini ricerca di file lungo il percorso da cui ottenere una stringa del nome localizzata. In questo modo si evita il probe delle cartelle lungo il percorso, che, nel caso di una cartella che rappresenta un server o una condivisione, potrebbe richiedere molto tempo e risorse. Desktop.ini file vengono memorizzati nella cache in alcune posizioni, quindi sarà almeno efficiente come il probe per gli attributi delle cartelle e quindi il probe per il Desktop.ini se tale cartella deve trasformare ou tot in sola lettura.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_BIND_FORCE_FOLDER_SHORTCUT_RESOLVE"></span><span id="str_bind_force_folder_shortcut_resolve"></span><dl> <dt><strong>STR_BIND_FORCE_FOLDER_SHORTCUT_RESOLVE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows XP SP2.</strong> Specificare questo contesto di associazione per forzare un collegamento a una cartella per risolvere il collegamento che punta alla destinazione. <br/> Un collegamento a una cartella è un elemento della cartella che punta a un altro elemento della cartella nello stesso spazio dei nomi, usando un collegamento (collegamento) per contenere l'elenco ID della destinazione. Il collegamento viene risolto per tenere traccia della destinazione nel caso in cui sia stata spostata o rinominata. Ad esempio, la cartella Windows XP <strong>My Network Places</strong> e la cartella Windows Vista <strong>Computer</strong> possono contenere i collegamenti alle cartelle creati con la procedura guidata Aggiungi <strong>percorso di</strong> rete. Per migliorare le prestazioni, il <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>metodo IShellFolder::BindToObject</strong></a> non risolve i collegamenti alla cartella di rete per impostazione predefinita.<br/> Usato con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a> o <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem::BindToHandler</strong></a>. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_DONT_PARSE_RELATIVE"></span><span id="str_dont_parse_relative"></span><dl> <dt><strong>STR_DONT_PARSE_RELATIVE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows XP.</strong> Specificare questo contesto di associazione per impedire a una chiamata al metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a> nella cartella <strong>Desktop</strong> di considerare i percorsi relativi come relativi al desktop. In tal caso, l'analisi non riesce quando viene specificato questo contesto di associazione.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_DONT_RESOLVE_LINK"></span><span id="str_dont_resolve_link"></span><dl> <dt><strong>STR_DONT_RESOLVE_LINK</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows Vista</strong>. Specificare questo <strong>contesto</strong> di associazione per indicare a <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> di non risolvere la destinazione del collegamento ottenuta quando si usa il GUID BHID_LinkTargetItem in <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem::BindToHandler</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_FILE_SYS_FIND_DATA"></span><span id="str_file_sys_find_data"></span><dl> <dt><strong>STR_FILE_SYS_FIND_DATA</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows XP.</strong> Specificare questo contesto di associazione per fornire i metadati del file al metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName,</strong></a> che viene usato invece di tentare di recuperare i metadati del file effettivi. L'oggetto associato deve implementare <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata"><strong>IFileSystemBindData</strong></a> e facoltativamente può implementare <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata2"><strong>anche IFileSystemBindData2.</strong></a> Per impostazione predefinita, il metodo <strong>IShellFolder::P arseDisplayName</strong> verifica che il file esista e usa i metadati effettivi del file per popolare l'elenco di ID.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_FILE_SYS_BIND_DATA_WIN7_FORMAT"></span><span id="str_file_sys_bind_data_win7_format"></span><dl> <dt><strong>STR_FILE_SYS_BIND_DATA_WIN7_FORMAT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows 8.1</strong>. Specificare questo contesto di associazione per <strong></strong> indicare che i dati forniti nel contesto di associazione STR_FILE_SYS_FIND_DATA devono essere usati per creare un elenco ItemID nel formato Windows 7.&quot;<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GET_ASYNC_HANDLER"></span><span id="str_get_async_handler"></span><dl> <dt><strong>STR_GET_ASYNC_HANDLER</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows 7</strong>. Specificare questo contesto di associazione quando il gestore viene recuperato nello stesso thread dell'interfaccia utente. È consigliabile evitare qualsiasi attività a elevato utilizzo di memoria, ad esempio quelle che coinvolgono l'accesso al disco o alla rete.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GPS_BESTEFFORT"></span><span id="str_gps_besteffort"></span><dl> <dt><strong>STR_GPS_BESTEFFORT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows Vista</strong>. Specificare questo contesto di associazione quando si richiede un <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>gestore IPropertySetStorage</strong></a> o <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore.</strong></a> Questo valore viene usato con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a>. Per altre <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>informazioni, GPS_BESTEFFORT</strong></a> il flag di configurazione.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GPS_DELAYCREATION"></span><span id="str_gps_delaycreation"></span><dl> <dt><strong>STR_GPS_DELAYCREATION</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows Vista</strong>. Specificare questo contesto di associazione quando si richiede un <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>gestore IPropertySetStorage</strong></a> o <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore.</strong></a> Questo valore viene usato con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a>. Per altre <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>informazioni, GPS_DELAYCREATION</strong></a> il flag di configurazione.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GPS_FASTPROPERTIESONLY"></span><span id="str_gps_fastpropertiesonly"></span><dl> <dt><strong>STR_GPS_FASTPROPERTIESONLY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows Vista</strong>. Specificare questo contesto di associazione quando si richiede un <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>gestore IPropertySetStorage</strong></a> o <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore.</strong></a> Questo valore viene usato con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a>. Per altre <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>informazioni, GPS_FASTPROPERTIESONLY</strong></a> il flag di configurazione.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GPS_HANDLERPROPERTIESONLY"></span><span id="str_gps_handlerpropertiesonly"></span><dl> <dt><strong>STR_GPS_HANDLERPROPERTIESONLY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows Vista</strong>. Specificare questo contesto di associazione quando si richiede un <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>gestore IPropertySetStorage</strong></a> o <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore.</strong></a> Questo valore viene usato con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a>. Per altre <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>informazioni, GPS_HANDLERPROPERTIESONLY</strong></a> il flag di configurazione.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GPS_NO_OPLOCK"></span><span id="str_gps_no_oplock"></span><dl> <dt><strong>STR_GPS_NO_OPLOCK</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows 7</strong>. Specificare questo contesto di associazione quando si richiede un <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>gestore IPropertySetStorage</strong></a> o <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore.</strong></a> Questo valore viene usato con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a>. Per altre <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>informazioni, GPS_NO_OPLOCK</strong></a> il flag di configurazione.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GPS_OPENSLOWITEM"></span><span id="str_gps_openslowitem"></span><dl> <dt><strong>STR_GPS_OPENSLOWITEM</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows Vista</strong>. Specificare questo contesto di associazione quando si richiede un <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>gestore IPropertySetStorage</strong></a> o <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore.</strong></a> Questo valore viene usato con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a>. Per altre <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>informazioni, GPS_OPENSLOWITEM</strong></a> il flag di configurazione.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_IFILTER_FORCE_TEXT_FILTER_FALLBACK"></span><span id="str_ifilter_force_text_filter_fallback"></span><dl> <dt><strong>STR_IFILTER_FORCE_TEXT_FILTER_FALLBACK</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Windows Solo Vista.</strong> Specificare questo contesto di associazione per fare in modo che una chiamata al metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a> che richiede l'interfaccia <a href="/windows/desktop/api/filter/nn-filter-ifilter"><strong>IFilter</strong></a> per un oggetto file system restituirà un filtro di testo se non sono disponibili altri filtri. Questo valore non è definito a Windows 7.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_IFILTER_LOAD_DEFINED_FILTER"></span><span id="str_ifilter_load_defined_filter"></span><dl> <dt><strong>STR_IFILTER_LOAD_DEFINED_FILTER</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Windows Solo Vista.</strong> Specificare questo contesto di associazione per fare in modo che una chiamata al metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a> che richiede all'interfaccia <a href="/windows/desktop/api/filter/nn-filter-ifilter"><strong>IFilter</strong></a> per un oggetto file system di non restituire un filtro di fallback se non è stato trovato alcun filtro registrato.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_INTERNAL_NAVIGATE"></span><span id="str_internal_navigate"></span><dl> <dt><strong>STR_INTERNAL_NAVIGATE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows Vista</strong>. Specificare questo contesto di associazione per abilitare il caricamento della cronologia da un flusso per uno spostamento interno quando viene chiamato il metodo <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768216(v=vs.85)"><strong>IPersistHistory::LoadHistory.</strong></a> Una navigazione interna è una navigazione all'interno della stessa visualizzazione.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_INTERNETFOLDER_PARSE_ONLY_URLMON_BINDABLE"></span><span id="str_internetfolder_parse_only_urlmon_bindable"></span><dl> <dt><strong>STR_INTERNETFOLDER_PARSE_ONLY_URLMON_BINDABLE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows 7</strong>. Specificare questo contesto di associazione con STR_PARSE_PREFER_FOLDER_BROWSING quando il client vuole che i gestori di cartelle della shell Internet generino un IDList per qualsiasi URL valido se non è possibile creare una cartella di tipo DAV per tale URL. L'URL non è verificato. viene controllata solo la sintassi e viene verificato che abbia un gestore di protocollo registrato.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_ITEM_CACHE_CONTEXT"></span><span id="str_item_cache_context"></span><dl> <dt><strong>STR_ITEM_CACHE_CONTEXT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows 7.</strong> Specificare questo contesto di associazione per indicare alle implementazioni di <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-initializeex"><strong>IPersistFolder3::InitializeEx</strong></a> di memorizzare nella cache gli oggetti helper a elevato utilizzo di memoria che possono esistere tra le istanze degli elementi della shell anziché ricreare questi oggetti ogni volta che viene creato un elemento della shell. L'oggetto associato è un altro oggetto contesto di associazione, inizialmente vuoto. Questo dovrebbe comportare un oggetto contesto di associazione separato, a cui si accede tramite <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getobjectparam"><strong>IBindCtx::GetObjectParam</strong></a> o <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam"><strong>IBindCtx::Register.ObjectParam</strong></a>. <br/> Un chiamante deve acconsentire esplicitamente a questo comportamento fornendo questo parametro del contesto di associazione quando chiama <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>SHCreateItemFromParsingName.</strong></a> In questo modo, si ottimizza il comportamento dell'associazione a più nomi di analisi in successione. La durata dell'oggetto contesto di associazione deve estendersi a più istanze degli elementi della shell e ai singoli contesti di associazione.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_NO_VALIDATE_FILENAME_CHARS"></span><span id="str_no_validate_filename_chars"></span><dl> <dt><strong>STR_NO_VALIDATE_FILENAME_CHARS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows Vista.</strong> Specificare questo contesto di associazione per consentire la visualizzazione di caratteri non validi nei nomi di file. Per impostazione predefinita, una chiamata al metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a> rifiuta i caratteri non validi nei nomi file. Questo contesto di associazione è significativo solo in combinazione con il STR_FILE_SYS_FIND_DATA di associazione.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS"></span><span id="str_parse_allow_internet_shell_folders"></span><dl> <dt><strong>STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows Vista.</strong> Specificare questo contesto di associazione per abilitare una chiamata al metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a> nella cartella <strong>Desktop</strong> per analizzare gli URL. Se questo contesto di associazione viene specificato, esegue l'override <strong><strong>STR_PARSE_PREFER_WEB_BROWSING</strong></strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_AND_CREATE_ITEM"></span><span id="str_parse_and_create_item"></span><dl> <dt><strong>STR_PARSE_AND_CREATE_ITEM</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows 7.</strong> Specificare questo contesto di associazione per indicare all'implementazione di un'origine dati di <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a> di ottimizzare il comportamento di <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>SHCreateItemFromParsingName.</strong></a> <br/> In <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>genere, SHCreateItemFromParsingName</strong></a> esegue due operazioni di binding sul nome da analizzare: una fino <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>a IShellFolder::P arseDisplayName</strong></a> e una per creare l'elemento della shell. Quando <strong></strong> il contesto di associazione STR_PARSE_AND_CREATE_ITEM è supportato, la seconda associazione viene evitata creando l'elemento della shell durante l'associazione <strong>IShellFolder::P arseDisplayName</strong> e archiviando l'elemento della shell tramite <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iparseandcreateitem-setitem"><strong>IParseAndCreateItem::SetItem</strong></a>. <strong>SHCreateItemFromParsingName usa</strong> quindi l'elemento della shell archiviato anziché crearne uno.<br/> Questo parametro si applica all'ultimo elemento del nome analizzato. Ad esempio, nel nome &quot;C:\Folder1\File.txt, i dati si applicano a File.txt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_DONT_REQUIRE_VALIDATED_URLS"></span><span id="str_parse_dont_require_validated_urls"></span><dl> <dt><strong>STR_PARSE_DONT_REQUIRE_VALIDATED_URLS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Windows Solo Vista.</strong> Specificare che, durante l'analisi di un URL, questo contesto di associazione non deve richiedere l'esistenza dell'URL prima di generare un IDList. Specificare questo contesto di associazione insieme <strong><strong>STR_PARSE_PREFER_FOLDER_BROWSING</strong></strong> quando il client desidera che i gestori di cartelle della <strong>shell Internet</strong> generino un IDList per l'URL se non è possibile creare una cartella DAV per l'URL specificato.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_PARTIAL_IDLIST"></span><span id="str_parse_partial_idlist"></span><dl> <dt><strong>STR_PARSE_PARTIAL_IDLIST</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows Vista.</strong> Specificare questo contesto di associazione per passare l'elemento originale che viene analizzato di nuovo quando tale elemento viene archiviato come oggetto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> che implementa anche <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparentanditem"><strong>l'interfaccia IParentAndItem.</strong></a> Prima Windows 7 questo valore non era definito in un file di intestazione. Può essere definito dal chiamante o passato come valore stringa <strong>di L &quot; ParseOriginalItem. &quot; </strong> A Windows 7, il valore è definito in Shlobj.h. Si noti che si tratta di un'intestazione diversa rispetto alle altre costanti STR.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_PREFER_FOLDER_BROWSING"></span><span id="str_parse_prefer_folder_browsing"></span><dl> <dt><strong>STR_PARSE_PREFER_FOLDER_BROWSING</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows XP.</strong> Specificare questo contesto di associazione per abilitare una chiamata al metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a> nella cartella <strong>Desktop</strong> per analizzare gli URL come se fossero cartelle. Usare questo contesto di associazione per l'associazione a un server WebDAV.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_PREFER_WEB_BROWSING"></span><span id="str_parse_prefer_web_browsing"></span><dl> <dt><strong>STR_PARSE_PREFER_WEB_BROWSING</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows Vista.</strong> Specificare questo contesto di associazione per impedire una chiamata al metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a> nella cartella <strong>Desktop</strong> per l'analisi degli URL. Questo contesto di associazione può essere sottoposto a override <strong><strong>STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS</strong></strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_PROPERTYSTORE"></span><span id="str_parse_propertystore"></span><dl> <dt><strong>STR_PARSE_PROPERTYSTORE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows Vista.</strong> Specificare questo contesto di associazione per eseguire l'override dell'archivio delle proprietà predefinito usato dal metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a> e usare l'archivio delle proprietà specificato come parametro bind. Si applica alle cartelle delegate.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_SHELL_PROTOCOL_TO_FILE_OBJECTS"></span><span id="str_parse_shell_protocol_to_file_objects"></span><dl> <dt><strong>STR_PARSE_SHELL_PROTOCOL_TO_FILE_OBJECTS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows XP SP2.</strong> Specificare questo contesto di associazione per abilitare una chiamata al metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a> nella cartella <strong>Desktop</strong> per usare la notazione shell: prefix per accedere ai &quot; &quot; file.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_SHOW_NET_DIAGNOSTICS_UI"></span><span id="str_parse_show_net_diagnostics_ui"></span><dl> <dt><strong>STR_PARSE_SHOW_NET_DIAGNOSTICS_UI</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows Vista.</strong> Specificare questo contesto di associazione per fare in modo che una chiamata al metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a> per visualizzare la finestra di dialogo di diagnostica di rete se l'analisi di un percorso di rete non riesce.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_SKIP_NET_CACHE"></span><span id="str_parse_skip_net_cache"></span><dl> <dt><strong>STR_PARSE_SKIP_NET_CACHE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows Vista.</strong> Specificare questo contesto di associazione per fare in modo che una chiamata al metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a> non controlli la cache delle condivisioni di rete e contatti direttamente il server di rete. Le informazioni sulle condivisioni di rete vengono memorizzate nella cache per migliorare le prestazioni <strong>e IShellFolder::P arseDisplayName</strong> controlla questa cache per impostazione predefinita.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_TRANSLATE_ALIASES"></span><span id="str_parse_translate_aliases"></span><dl> <dt><strong>STR_PARSE_TRANSLATE_ALIASES</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows XP.</strong> Specificare questo contesto di associazione per passare le proprietà analizzate al metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a> per uno spazio dei nomi delegato. Lo spazio dei nomi può usare le proprietà passate anziché tentare di analizzare il nome stesso.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_WITH_PROPERTIES"></span><span id="str_parse_with_properties"></span><dl> <dt><strong>STR_PARSE_WITH_PROPERTIES</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Windows Solo Vista.</strong> Contesto di associazione di analisi usato per passare un set di proprietà e il nome dell'elemento quando si chiama <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a>. L'oggetto nel contesto di associazione <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>implementa IPropertyStore</strong></a> e viene recuperato chiamando <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getobjectparam"><strong>IBindCtx::GetObjectParam.</strong></a><br/> DBFolder è un'origine dati shell che rappresenta gli elementi nei risultati della ricerca e nelle viste basate su query. DBFolder recupera questi elementi tramite una query sul Windows di ricerca. Gli elementi nei risultati della ricerca vengono identificati tramite uno schema di protocollo, ad &quot; esempio file: &quot; o &quot; mapi: &quot; . DBFolder fornisce il comportamento per questi elementi delegando alle origini dati della shell create per questi protocolli. Per <a href="/previous-versions/bb233544(v=msdn.10)">altre informazioni, vedere Sviluppo di componenti aggiuntivi</a> per gestori di protocollo.<br/> Quando DBFolder delega l'operazione di analisi alle origini dati della shell che supportano i protocolli di ricerca Windows, questo contesto di associazione fornisce l'accesso ai valori restituiti nel risultato della query per l'elemento. Il comportamento predefinito include quanto segue:<br/>
<ul>
<li><a href="/windows/desktop/properties/props-system-itemtype">System.ItemType</a> (PKEY_ItemType)</li>
<li><a href="/windows/desktop/properties/props-system-parsingpath">System.ParsingPath</a> (PKEY_ParsingPath)</li>
<li><a href="/windows/desktop/properties/props-system-itempathdisplay">System.ItemPathDisplay</a> (PKEY_ItemPathDisplay)</li>
<li><a href="/windows/desktop/properties/props-system-itemnamedisplay">System.ItemNameDisplay</a> (PKEY_ItemNameDisplay)</li>
</ul>
<br/> Questo contesto di associazione può essere usato anche per analizzare un elemento DBFolder se un client dispone di un set di proprietà che definiscono l'elemento. In questo caso è necessario passare un nome vuoto a <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a>.<br/> Prima Windows 7, questo valore non era definito in un file di intestazione. Può essere definito dal chiamante o passato come valore stringa: <code>L&quot;ParseWithProperties&quot;</code> . A Windows 7, il valore è definito in Shlobj.h. Si noti che si tratta di un'intestazione diversa da quella in cui sono definite le altre costanti STR.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PROPERTYBAG_PARAM"></span><span id="str_propertybag_param"></span><dl> <dt><strong>STR_PROPERTYBAG_PARAM</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows 8</strong>. Specificare questo contesto di associazione per indicare che il parametro del contesto di associazione è un contenitore di proprietà (<a href="/windows/win32/api/oaidl/nn-oaidl-ipropertybag"><strong>IPropertyBag</strong></a>) usato per passare i valori VARIANT nel contesto di associazione. Per altri dettagli, vedere la sezione Osservazioni.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_SKIP_BINDING_CLSID"></span><span id="str_skip_binding_clsid"></span><dl> <dt><strong>STR_SKIP_BINDING_CLSID</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotto in Windows XP.</strong> Specificare questo contesto di associazione per fare in modo che le chiamate ai metodi <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arseDisplayName</strong></a> o <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder::BindToObject</strong></a> ignorino una determinata estensione dello spazio dei nomi della shell durante l'analisi o l'associazione. Il CLSID dello spazio dei nomi da ignorare viene fornito dal metodo <a href="/windows/desktop/api/objidl/nf-objidl-ipersist-getclassid"><strong>IPersist::GetClassID</strong></a> del parametro bind. <br/>
<blockquote>
[!Note]<br />
Introdotto in Windows 2000 SP3, questo valore è stato definito in Shlobj.h fino Windows XP, quando è stato spostato in Shobjidl.h.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_TRACK_CLSID"></span><span id="str_track_clsid"></span><dl> <dt><strong>STR_TRACK_CLSID</strong></dt> </dl></td>
<td style="text-align: left;">Non usato.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Commenti

I contesti di associazione vengono usati per passare parametri facoltativi alle funzioni che hanno un parametro \* IBindCtx. Questi parametri sono espressi come oggetti COM e possono implementare interfacce utilizzate per modellare i dati dei parametri. Alcuni contesti di associazione rappresentano un valore booleano, dove **TRUE** indica un oggetto che implementa solo [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e FALSE indica che non è presente alcun oggetto.

[**IShellFolder::P arseDisplayName,**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) [**IShellFolder::BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) e [**IShellItem::BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) accettano un contesto di associazione ed è possibile passarli parametri tramite tale contesto di associazione.

Alcuni contesti di associazione sono specifici per determinate implementazioni di origini dati o tipi di gestore.

I parametri di contesto di associazione vengono definiti per l'uso con una funzione o un metodo specifico.

Quando si richiede un archivio delle proprietà tramite [**IShellFolder,**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)è possibile specificare l'equivalente di [**GPS \_ DEFAULT**](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags) passando un [**parametro IBindCtx**](/windows/win32/api/objidl/nn-objidl-ibindctx) null. È anche possibile specificare l'equivalente di GPS READWRITE passando una modalità \_ STGM \_ READWRITE \| STGM \_ EXCLUSIVE nel contesto di associazione.

L'elenco delle proprietà specificato dall'oggetto contesto di associazione **\_ \_ PARAM PROPERTYBAG STR** contiene valori aggiuntivi a cui è possibile accedere con i metodi [**IPropertyBag::Read**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768197(v=vs.85)) e [**IPropertyBag::Write.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768198(v=vs.85))



| Nome proprietà                                 | Type     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FLAG DEGLI \_ ELEMENTI DI \_ ENUMERAZIONE STR \_                       | VT \_ UI4  | **Introdotto in Windows 8**. Specifica un [**valore SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) da passare a [**IShellFolder::EnumObjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects) quando si chiama [**IShellItem::BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) con **\_ enumItems DISID.**                                                                                                                                                                                                                         |
| STR \_ PARSE \_ EXPLICIT \_ ASSOCIATION \_ SUCCESSFUL | VT \_ BOOL | **Introdotto in Windows 7.** Il metodo [**IShellFolder::P arseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) imposta questa proprietà per indicare al chiamante che l'elenco IDList restituito è stato associato al [ProgID](fa-progids.md) specificato con **STR \_ PARSE WITH EXPLICIT \_ \_ \_ PROGID** o all'applicazione specificata con **STR PARSE WITH EXPLICIT \_ \_ \_ \_ ASSOCAPP.** Quando **STR \_ PARSE EXPLICIT ASSOCIATION \_ \_ \_ SUCCESSFUL** è assente, il ProgID o l'applicazione non è stato associato a IDList. |
| ANALISI STR \_ \_ CON \_ \_ ASSOCAPP ESPLICITO          | VT \_ BSTR | **Introdotto in Windows 7.** Specificare questa proprietà per fare in modo che una chiamata al metodo [**IShellFolder::P arseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) restituirà un idList associato al gestore di associazione del tipo di file per l'applicazione.                                                                                                                                                                                                                                          |
| ANALISI STR \_ \_ CON \_ \_ PROGID ESPLICITO            | VT \_ BSTR | **Introdotto in Windows 7.** Specificare questa proprietà per fare in modo che una chiamata al metodo [**IShellFolder::P arseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) restituirà un idList associato al gestore di associazione file del [ProgID specificato.](fa-progids.md)                                                                                                                                                                                                                          |



 

Vedere [l'esempio di analisi con parametri](samples-parsingwithparameters.md) per un esempio dell'uso di valori di contesto di associazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Shobjidl.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shobjidl.idl</dt> </dl> |



 

 

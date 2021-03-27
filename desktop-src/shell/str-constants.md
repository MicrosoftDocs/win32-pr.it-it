---
description: 'Set di chiavi di stringa utilizzate con il Metodo IBindCtx:: RegisterObjectParam per specificare un contesto di associazione.'
title: Chiavi di stringhe di contesto di binding (ShObjIdl. h)
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
ms.openlocfilehash: b1dcdb3b9199fede88d6f13949cc9276bde17b16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980919"
---
# <a name="bind-context-string-keys"></a>Chiavi della stringa di contesto di binding

Set di chiavi di stringa utilizzate con il metodo [**IBindCtx:: RegisterObjectParam**](/windows/win32/api/objidl/nf-objidl-ibindctx-registerobjectparam) per specificare un contesto di associazione.



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
<td style="text-align: left;"><strong>Introdotta in Windows XP SP2</strong>. Specificare questo contesto di binding per consentire ai client dell'origine dati di eseguire l'override dei criteri lettera di unità nascosta e consentire l'accesso agli oggetti visualizzazione per le origini dati sulle unità bloccate.<br/> Usato con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> o <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem:: BindToHandler</strong></a>.<br/> Il sistema supporta criteri controllati dall'amministratore che nascondono le lettere di unità specificate per impedire agli utenti di accedere a tali unità tramite Esplora risorse. Quando questo criterio è attivo, il risultato è che gli oggetti visualizzazione e altri gestori creati con il metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject"><strong>IShellFolder:: CreateViewObject</strong></a> avranno esito negativo quando vengono chiamati sulle unità bloccate dai criteri.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_BIND_DELEGATE_CREATE_OBJECT"></span><span id="str_bind_delegate_create_object"></span><dl> <dt><strong>STR_BIND_DELEGATE_CREATE_OBJECT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotta in Windows Vista</strong>. Specificare questo contesto di associazione per fare in modo che il metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> usi l'oggetto specificato dal parametro <em>PBC</em> per creare l'oggetto di destinazione. in questo caso, l'oggetto specificato dal parametro <em>punk</em> nella chiamata <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam"><strong>IBindCtx:: RegisterObjectParam</strong></a> deve implementare l'interfaccia <a href="/windows/desktop/api/Propsys/nn-propsys-icreateobject"><strong>ICreateObject</strong></a> . <br/> Usato con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> o <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem:: BindToHandler</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_BIND_FOLDER_ENUM_MODE"></span><span id="str_bind_folder_enum_mode"></span><dl> <dt><strong>STR_BIND_FOLDER_ENUM_MODE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotta in Windows 7</strong>. Passato a <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> con un valore <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folder_enum_mode"><strong>FOLDER_ENUM_MODE</strong></a> per controllare la modalità di enumerazione dell'elemento analizzato. Il valore <strong>FOLDER_ENUM_MODE</strong> viene passato nel contesto di associazione tramite un oggetto che implementa <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithfolderenummode"><strong>IObjectWithFolderEnumMode</strong></a>. <br/> Gli elementi con modalità di enumerazione diverse vengono confrontati in forma canonica (SHCIDS_CANONICALONLY) diversi perché enumerano set di elementi diversi.<br/> Se un elemento non supporta la modalità di enumerazione, perché non è una cartella o non fornisce la modalità di enumerazione, viene creato nella modalità di enumerazione predefinita.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_BIND_FOLDERS_READ_ONLY"></span><span id="str_bind_folders_read_only"></span><dl> <dt><strong>STR_BIND_FOLDERS_READ_ONLY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotta in Windows 7</strong>. Passato a <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> insieme a <strong>STR_FILE_SYS_BIND_DATA</strong>. In questo modo si impone l'analisi semplice durante il sondaggio per i file Desktop.ini lungo il percorso dal quale ottenere una stringa del nome localizzata. In questo modo si evita l'esecuzione di probe per le cartelle lungo il percorso, che, nel caso di una cartella che rappresenta un server o una condivisione, potrebbe richiedere tempo e risorse estese. I file di Desktop.ini vengono memorizzati nella cache in alcune posizioni, pertanto saranno almeno efficienti come il probe per gli attributi delle cartelle e quindi il sondaggio per il Desktop.ini se tale cartella deve trasformare ou tot come di sola lettura.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_BIND_FORCE_FOLDER_SHORTCUT_RESOLVE"></span><span id="str_bind_force_folder_shortcut_resolve"></span><dl> <dt><strong>STR_BIND_FORCE_FOLDER_SHORTCUT_RESOLVE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotta in Windows XP SP2</strong>. Specificare questo contesto di binding per forzare un collegamento alla cartella per risolvere il collegamento che punta alla propria destinazione. <br/> Un collegamento alla cartella è un elemento di cartella che punta a un altro elemento di cartella nello stesso spazio dei nomi, usando un collegamento (collegamento) per mantenere il IDList della destinazione. Il collegamento viene risolto per tenere traccia della destinazione nel caso in cui venga spostato o rinominato. Ad esempio, la cartella dei <strong>punti di rete</strong> di Windows XP e la cartella del <strong>computer</strong> Windows Vista possono contenere i collegamenti alle cartelle creati con l'aggiunta guidata <strong>percorso di rete</strong> . Per migliorare le prestazioni, il metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> non risolve i collegamenti alla cartella di rete per impostazione predefinita.<br/> Usato con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> o <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem:: BindToHandler</strong></a>. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_DONT_PARSE_RELATIVE"></span><span id="str_dont_parse_relative"></span><dl> <dt><strong>STR_DONT_PARSE_RELATIVE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotta in Windows XP</strong>. Specificare questo contesto di associazione per impedire che una chiamata al metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> sulla cartella <strong>Desktop</strong> tratti i percorsi relativi rispetto al desktop; in tal caso, l'analisi ha esito negativo quando viene specificato il contesto di associazione.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_DONT_RESOLVE_LINK"></span><span id="str_dont_resolve_link"></span><dl> <dt><strong>STR_DONT_RESOLVE_LINK</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotta in Windows Vista</strong>. Specificare questo contesto di associazione per indicare a un <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> di non risolvere la destinazione del collegamento ottenuta quando si usa il GUID <strong>BHID_LinkTargetItem</strong> in <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem:: BindToHandler</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_FILE_SYS_FIND_DATA"></span><span id="str_file_sys_find_data"></span><dl> <dt><strong>STR_FILE_SYS_FIND_DATA</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotta in Windows XP</strong>. Specificare questo contesto di associazione per fornire i metadati del file al metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> , che viene usato anziché tentare di recuperare i metadati del file effettivi. L'oggetto associato deve implementare <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata"><strong>IFileSystemBindData</strong></a> e può anche implementare <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata2"><strong>IFileSystemBindData2</strong></a>. Per impostazione predefinita, il metodo <strong>IShellFolder::P arsedisplayname</strong> verifica che il file esista e usa i metadati effettivi del file per popolare l'elenco di ID.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_FILE_SYS_BIND_DATA_WIN7_FORMAT"></span><span id="str_file_sys_bind_data_win7_format"></span><dl> <dt><strong>STR_FILE_SYS_BIND_DATA_WIN7_FORMAT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotta in Windows 8.1</strong>. Specificare questo contesto di associazione per indicare che i dati forniti nel contesto di associazione <strong>STR_FILE_SYS_FIND_DATA</strong> devono essere utilizzati per creare un elenco ItemId nel formato Windows 7.&quot;<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GET_ASYNC_HANDLER"></span><span id="str_get_async_handler"></span><dl> <dt><strong>STR_GET_ASYNC_HANDLER</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotta in Windows 7</strong>. Specificare questo contesto di associazione quando il gestore viene recuperato nello stesso thread dell'interfaccia utente. Tutte le attività che richiedono un utilizzo intensivo della memoria, ad esempio quelle che coinvolgono l'accesso al disco o alla rete, devono essere<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GPS_BESTEFFORT"></span><span id="str_gps_besteffort"></span><dl> <dt><strong>STR_GPS_BESTEFFORT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotta in Windows Vista</strong>. Specificare questo contesto di associazione quando si richiede un gestore <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> o <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> . Questo valore viene usato con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a>. Per ulteriori informazioni, vedere il flag <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_BESTEFFORT</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GPS_DELAYCREATION"></span><span id="str_gps_delaycreation"></span><dl> <dt><strong>STR_GPS_DELAYCREATION</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotta in Windows Vista</strong>. Specificare questo contesto di associazione quando si richiede un gestore <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> o <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> . Questo valore viene usato con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a>. Per ulteriori informazioni, vedere il flag <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_DELAYCREATION</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GPS_FASTPROPERTIESONLY"></span><span id="str_gps_fastpropertiesonly"></span><dl> <dt><strong>STR_GPS_FASTPROPERTIESONLY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotta in Windows Vista</strong>. Specificare questo contesto di associazione quando si richiede un gestore <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> o <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> . Questo valore viene usato con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a>. Per ulteriori informazioni, vedere il flag <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_FASTPROPERTIESONLY</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GPS_HANDLERPROPERTIESONLY"></span><span id="str_gps_handlerpropertiesonly"></span><dl> <dt><strong>STR_GPS_HANDLERPROPERTIESONLY</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotta in Windows Vista</strong>. Specificare questo contesto di associazione quando si richiede un gestore <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> o <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> . Questo valore viene usato con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a>. Per ulteriori informazioni, vedere il flag <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_HANDLERPROPERTIESONLY</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GPS_NO_OPLOCK"></span><span id="str_gps_no_oplock"></span><dl> <dt><strong>STR_GPS_NO_OPLOCK</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotta in Windows 7</strong>. Specificare questo contesto di associazione quando si richiede un gestore <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> o <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> . Questo valore viene usato con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a>. Per ulteriori informazioni, vedere il flag <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_NO_OPLOCK</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GPS_OPENSLOWITEM"></span><span id="str_gps_openslowitem"></span><dl> <dt><strong>STR_GPS_OPENSLOWITEM</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotta in Windows Vista</strong>. Specificare questo contesto di associazione quando si richiede un gestore <a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage"><strong>IPropertySetStorage</strong></a> o <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> . Questo valore viene usato con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a>. Per ulteriori informazioni, vedere il flag <a href="/windows/desktop/api/propsys/ne-propsys-getpropertystoreflags"><strong>GPS_OPENSLOWITEM</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_IFILTER_FORCE_TEXT_FILTER_FALLBACK"></span><span id="str_ifilter_force_text_filter_fallback"></span><dl> <dt><strong>STR_IFILTER_FORCE_TEXT_FILTER_FALLBACK</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Solo Windows Vista.</strong> Specificare questo contesto di associazione per generare una chiamata al metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> che richiede all'interfaccia <a href="/windows/desktop/api/filter/nn-filter-ifilter"><strong>IFilter</strong></a> un oggetto file System per restituire un filtro di testo se non sono disponibili altri filtri. Questo valore non è definito a partire da Windows 7.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_IFILTER_LOAD_DEFINED_FILTER"></span><span id="str_ifilter_load_defined_filter"></span><dl> <dt><strong>STR_IFILTER_LOAD_DEFINED_FILTER</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Solo Windows Vista.</strong> Specificare questo contesto di associazione per generare una chiamata al metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> che richiede all'interfaccia <a href="/windows/desktop/api/filter/nn-filter-ifilter"><strong>IFilter</strong></a> per un oggetto file System di non restituire un filtro di fallback se non è stato trovato alcun filtro registrato.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_INTERNAL_NAVIGATE"></span><span id="str_internal_navigate"></span><dl> <dt><strong>STR_INTERNAL_NAVIGATE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotta in Windows Vista</strong>. Specificare questo contesto di binding per abilitare il caricamento della cronologia da un flusso per una navigazione interna quando viene chiamato il metodo <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768216(v=vs.85)"><strong>IPersistHistory:: loadHistory</strong></a> . Una navigazione interna è una navigazione all'interno della stessa visualizzazione.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_INTERNETFOLDER_PARSE_ONLY_URLMON_BINDABLE"></span><span id="str_internetfolder_parse_only_urlmon_bindable"></span><dl> <dt><strong>STR_INTERNETFOLDER_PARSE_ONLY_URLMON_BINDABLE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotta in Windows 7</strong>. Specificare questo contesto di binding con STR_PARSE_PREFER_FOLDER_BROWSING quando il client desidera che i gestori di cartelle della shell Internet generino un IDList per qualsiasi URL valido se non è possibile creare una cartella di tipo DAV per tale URL. L'URL non è verificato per esistere; solo la relativa sintassi viene controllata e dispone di un gestore di protocollo registrato.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_ITEM_CACHE_CONTEXT"></span><span id="str_item_cache_context"></span><dl> <dt><strong>STR_ITEM_CACHE_CONTEXT</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotta in Windows 7</strong>. Specificare questo contesto di associazione per indicare le implementazioni di <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder3-initializeex"><strong>IPersistFolder3:: InitializeEx</strong></a> per memorizzare nella cache gli oggetti helper con utilizzo intensivo della memoria che possono esistere nelle creazioni di istanze degli elementi della shell anziché ricreare questi oggetti ogni volta che viene creato un elemento della shell. L'oggetto associato è un altro oggetto contesto di binding, inizialmente vuoto. Questo dovrebbe generare un oggetto di contesto di binding separato, a cui si accede tramite <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getobjectparam"><strong>IBindCtx:: GetObjectParam</strong></a> o <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam"><strong>IBindCtx:: Register. ObjectParam</strong></a>. <br/> Un chiamante deve acconsentire esplicitamente a questo comportamento fornendo questo parametro di contesto di binding quando si chiama <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>SHCreateItemFromParsingName</strong></a>. In questo modo, è possibile ottimizzare il comportamento dell'associazione a più nomi di analisi in successione. La durata dell'oggetto contesto di binding deve estendersi a più istanze di elementi della shell e ai rispettivi contesti di binding.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_NO_VALIDATE_FILENAME_CHARS"></span><span id="str_no_validate_filename_chars"></span><dl> <dt><strong>STR_NO_VALIDATE_FILENAME_CHARS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotta in Windows Vista</strong>. Specificare questo contesto di binding per consentire la visualizzazione dei caratteri di nome file non validi nei nomi di file. Per impostazione predefinita, una chiamata al metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> rifiuta i caratteri non validi nei nomi di file. Questo contesto di associazione è significativo solo in combinazione con il contesto di associazione STR_FILE_SYS_FIND_DATA.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS"></span><span id="str_parse_allow_internet_shell_folders"></span><dl> <dt><strong>STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotta in Windows Vista</strong>. Specificare questo contesto di binding per abilitare una chiamata al metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> nella cartella <strong>Desktop</strong> per analizzare gli URL. Se questo contesto di associazione viene specificato, esegue l'override di <strong><strong>STR_PARSE_PREFER_WEB_BROWSING</strong></strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_AND_CREATE_ITEM"></span><span id="str_parse_and_create_item"></span><dl> <dt><strong>STR_PARSE_AND_CREATE_ITEM</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotta in Windows 7</strong>. Specificare questo contesto di associazione per indicare all'implementazione dell'origine dati di <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> di ottimizzare il comportamento di <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>SHCreateItemFromParsingName</strong></a>. <br/> In genere, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromparsingname"><strong>SHCreateItemFromParsingName</strong></a> esegue due operazioni di binding sul nome da analizzare: una alla volta e una a <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> e una per creare l'elemento della shell. Quando il contesto di associazione <strong>STR_PARSE_AND_CREATE_ITEM</strong> è supportato, la seconda associazione viene evitata creando l'elemento della shell durante il <strong>IShellFolder::P arsedisplayname</strong> bind e archiviando l'elemento della shell tramite <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iparseandcreateitem-setitem"><strong>IParseAndCreateItem:: SetItem</strong></a>. <strong>SHCreateItemFromParsingName</strong> usa quindi l'elemento della shell archiviato anziché crearne uno.<br/> Questo parametro si applica all'ultimo elemento del nome analizzato. Nel nomeC:\Folder1\File.txt, ad esempio &quot; , i dati si applicano a File.txt.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_DONT_REQUIRE_VALIDATED_URLS"></span><span id="str_parse_dont_require_validated_urls"></span><dl> <dt><strong>STR_PARSE_DONT_REQUIRE_VALIDATED_URLS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Solo Windows Vista.</strong> Specifica che, durante l'analisi di un URL, questo contesto di associazione non deve richiedere l'URL esistente prima di generare un IDList. Specificare questo contesto di associazione insieme a <strong><strong>STR_PARSE_PREFER_FOLDER_BROWSING</strong></strong> quando il client desidera che i gestori di cartelle della <strong>Shell Internet</strong> generino un IDList per l'URL se non è possibile creare una cartella DAV per l'URL specificato.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_PARTIAL_IDLIST"></span><span id="str_parse_partial_idlist"></span><dl> <dt><strong>STR_PARSE_PARTIAL_IDLIST</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotta in Windows Vista</strong>. Specificare questo contesto di associazione per passare l'elemento originale che viene nuovamente analizzato quando tale elemento viene archiviato come oggetto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> che implementa anche l'interfaccia <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparentanditem"><strong>IParentAndItem</strong></a> . Prima di Windows 7, questo valore non è stato definito in un file di intestazione. Può essere definito dal chiamante o passato come valore stringa di <strong>L &quot; ParseOriginalItem &quot; </strong>. A partire da Windows 7, il valore è definito in Shlobj. h. Si noti che si tratta di un'intestazione diversa rispetto alle altre costanti STR.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_PREFER_FOLDER_BROWSING"></span><span id="str_parse_prefer_folder_browsing"></span><dl> <dt><strong>STR_PARSE_PREFER_FOLDER_BROWSING</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotta in Windows XP</strong>. Specificare questo contesto di binding per abilitare una chiamata al metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> nella cartella <strong>Desktop</strong> per analizzare gli URL come se fossero cartelle. Utilizzare questo contesto di binding per eseguire il binding a un server WebDAV.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_PREFER_WEB_BROWSING"></span><span id="str_parse_prefer_web_browsing"></span><dl> <dt><strong>STR_PARSE_PREFER_WEB_BROWSING</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotta in Windows Vista</strong>. Specificare questo contesto di associazione per impedire una chiamata al metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> sugli URL di analisi del modulo della cartella <strong>Desktop</strong> . Questo contesto di associazione può essere sottoposto a override da <strong><strong>STR_PARSE_ALLOW_INTERNET_SHELL_FOLDERS</strong></strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_PROPERTYSTORE"></span><span id="str_parse_propertystore"></span><dl> <dt><strong>STR_PARSE_PROPERTYSTORE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotta in Windows Vista</strong>. Specificare questo contesto di binding per eseguire l'override dell'archivio delle proprietà predefinito usato dal metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> e usare invece l'archivio di proprietà specificato come parametro bind. Si applica alle cartelle delegate.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_SHELL_PROTOCOL_TO_FILE_OBJECTS"></span><span id="str_parse_shell_protocol_to_file_objects"></span><dl> <dt><strong>STR_PARSE_SHELL_PROTOCOL_TO_FILE_OBJECTS</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotta in Windows XP SP2</strong>. Specificare questo contesto di binding per abilitare una chiamata al metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> nella cartella <strong>Desktop</strong> per usare la &quot; notazione Shell: &quot; prefix per accedere ai file.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_SHOW_NET_DIAGNOSTICS_UI"></span><span id="str_parse_show_net_diagnostics_ui"></span><dl> <dt><strong>STR_PARSE_SHOW_NET_DIAGNOSTICS_UI</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotta in Windows Vista</strong>. Specificare questo contesto di binding per generare una chiamata al metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> per visualizzare la finestra di dialogo Diagnostica di rete se l'analisi di un percorso di rete ha esito negativo.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_SKIP_NET_CACHE"></span><span id="str_parse_skip_net_cache"></span><dl> <dt><strong>STR_PARSE_SKIP_NET_CACHE</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotta in Windows Vista</strong>. Specificare questo contesto di binding per provocare una chiamata al metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> per ignorare il controllo della cache delle condivisioni di rete e contattare direttamente il server di rete. Le informazioni sulle condivisioni di rete vengono memorizzate nella cache per migliorare le prestazioni e <strong>IShellFolder::P arsedisplayname</strong> controlla questa cache per impostazione predefinita.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PARSE_TRANSLATE_ALIASES"></span><span id="str_parse_translate_aliases"></span><dl> <dt><strong>STR_PARSE_TRANSLATE_ALIASES</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotta in Windows XP</strong>. Specificare questo contesto di associazione per passare le proprietà analizzate al metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> per uno spazio dei nomi delegato. Lo spazio dei nomi può utilizzare le proprietà passate anziché tentare di analizzare il nome stesso.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_PARSE_WITH_PROPERTIES"></span><span id="str_parse_with_properties"></span><dl> <dt><strong>STR_PARSE_WITH_PROPERTIES</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Solo Windows Vista.</strong> Contesto di associazione di analisi usato per passare un set di proprietà e il nome dell'elemento quando si chiama <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a>. L'oggetto nel contesto di associazione implementa <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> e viene recuperato chiamando <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-getobjectparam"><strong>IBindCtx:: GetObjectParam</strong></a>.<br/> DBFolder è un'origine dati della shell che rappresenta gli elementi nei risultati della ricerca e nelle viste basate su query. DBFolder recupera questi elementi eseguendo una query sul sistema di ricerca di Windows. Gli elementi nei risultati della ricerca vengono identificati tramite uno schema di protocollo, ad esempio &quot; file: &quot; o &quot; MAPI: &quot; . DBFolder fornisce il comportamento per questi elementi delegando le origini dati della shell create per questi protocolli. Per ulteriori informazioni, vedere sviluppo di componenti aggiuntivi per la <a href="/previous-versions/bb233544(v=msdn.10)">gestione del protocollo</a> .<br/> Quando DBFolder delega l'operazione di analisi alle origini dati della shell che supportano i protocolli di ricerca di Windows, questo contesto di associazione consente di accedere ai valori restituiti nei risultati della query per tale elemento. Il comportamento predefinito include quanto segue:<br/>
<ul>
<li><a href="/windows/desktop/properties/props-system-itemtype">System. ItemType</a> (PKEY_ItemType)</li>
<li><a href="/windows/desktop/properties/props-system-parsingpath">System. ParsingPath</a> (PKEY_ParsingPath)</li>
<li><a href="/windows/desktop/properties/props-system-itempathdisplay">System. ItemPathDisplay</a> (PKEY_ItemPathDisplay)</li>
<li><a href="/windows/desktop/properties/props-system-itemnamedisplay">System. ItemNameDisplay</a> (PKEY_ItemNameDisplay)</li>
</ul>
<br/> Questo contesto di associazione può essere usato anche per analizzare un elemento DBFolder se un client dispone di un set di proprietà che definiscono l'elemento. In questo caso, è necessario passare un nome vuoto a <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a>.<br/> Prima di Windows 7, questo valore non è stato definito in un file di intestazione. Può essere definito dal chiamante o passato come valore stringa: <code>L&quot;ParseWithProperties&quot;</code> . A partire da Windows 7, il valore è definito in Shlobj. h. Si noti che si tratta di un'intestazione diversa da quella in cui sono definite le altre costanti STR.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_PROPERTYBAG_PARAM"></span><span id="str_propertybag_param"></span><dl> <dt><strong>STR_PROPERTYBAG_PARAM</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotta in Windows 8</strong>. Specificare questo contesto di associazione per indicare che il parametro di contesto di binding è un contenitore di proprietà (<a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)"><strong>IPropertyBag</strong></a>) utilizzato per passare valori Variant nel contesto di associazione. Per ulteriori informazioni, vedere la sezione Osservazioni.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_SKIP_BINDING_CLSID"></span><span id="str_skip_binding_clsid"></span><dl> <dt><strong>STR_SKIP_BINDING_CLSID</strong></dt> </dl></td>
<td style="text-align: left;"><strong>Introdotta in Windows XP</strong>. Specificare questo contesto di associazione per fare in modo che le chiamate ai metodi <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a> o <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> ignorino un'estensione dello spazio dei nomi shell specifica durante l'analisi o l'associazione. Il CLSID dello spazio dei nomi da ignorare viene fornito dal metodo <a href="/windows/desktop/api/objidl/nf-objidl-ipersist-getclassid"><strong>IPersist:: GetClassID</strong></a> del parametro bind. <br/>
<blockquote>
[!Note]<br />
Introdotta in Windows 2000 SP3, questo valore è stato definito in Shlobj. h fino a Windows XP, quando è stato spostato in ShObjIdl. h.
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

I contesti di binding vengono usati per passare parametri facoltativi alle funzioni che hanno un \* parametro IBindCtx. Tali parametri sono espressi come oggetti COM e potrebbero implementare interfacce utilizzate per modellare i dati dei parametri. Alcuni contesti di binding rappresentano un valore booleano, dove **true** indica che un oggetto che implementa solo [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e false indica che non è presente alcun oggetto.

[**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname), [**IShellFolder:: BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) e [**IShellItem:: BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) accettano un contesto di associazione ed è possibile passare i parametri tramite il contesto di associazione.

Alcuni contesti di binding sono specifici di determinate implementazioni di origini dati o tipi di gestore.

I parametri del contesto di associazione vengono definiti per l'uso con una funzione o un metodo specifico.

Quando si richiede un archivio di proprietà tramite [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), è possibile specificare l'equivalente [**di \_ default GPS**](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags) passando un parametro [**IBindCtx**](/windows/win32/api/objidl/nn-objidl-ibindctx) null. È anche possibile specificare l'equivalente di \_ ReadWrite GPS passando una modalità STGM \_ ReadWrite \| STGM \_ Exclusive nel contesto di binding.

Il contenitore di proprietà specificato dall'oggetto del contesto di associazione del **\_ \_ param PROPERTYBAG Str** contiene valori aggiuntivi a cui è possibile accedere con i metodi [**IPropertyBag:: Read**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768197(v=vs.85)) e [**IPropertyBag:: Write**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768198(v=vs.85)) .



| Nome proprietà                                 | Type     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ flag elementi Enum \_ Str                       | \_UI4 VT  | **Introdotta in Windows 8**. Specifica un valore [**SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf) da passare a [**IShellFolder:: EnumObjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects) quando si chiama [**IShellItem:: BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) con **BHID \_ EnumItems**.                                                                                                                                                                                                                         |
| STR \_ analisi \_ esplicita \_ associazione \_ riuscita | \_bool VT | **Introdotta in Windows 7**. Il metodo [**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) imposta questa proprietà per indicare al chiamante che il IDList restituito è stato associato al [ProgID](fa-progids.md) specificato con **l' \_ analisi \_ Str \_ con \_ ProgID esplicito** o l'applicazione specificata con l' **\_ analisi Str \_ con \_ \_ ASSOCAPP espliciti**. Quando **Str \_ Parse \_ Explicit \_ Association ha \_ esito positivo** è assente, il ProgID o l'applicazione non è stata associata a IDList. |
| STR \_ Parse \_ con \_ ASSOCAPP esplicito \_          | \_BSTR VT | **Introdotta in Windows 7**. Specificare questa proprietà per generare una chiamata al metodo [**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) per restituire un IDList associato al gestore di associazione del tipo di file per l'applicazione.                                                                                                                                                                                                                                          |
| STR \_ Parse \_ con \_ ProgID esplicito \_            | \_BSTR VT | **Introdotta in Windows 7**. Specificare questa proprietà per generare una chiamata al metodo [**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) per restituire un IDList associato al gestore di associazione file del [ProgID](fa-progids.md)fornito.                                                                                                                                                                                                                          |



 

Vedere l' [esempio di analisi con parametri](samples-parsingwithparameters.md) per un esempio di utilizzo dei valori del contesto di associazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>ShObjIdl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>ShObjIdl. idl</dt> </dl> |



 

 

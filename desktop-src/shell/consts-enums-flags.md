---
description: In questa sezione vengono descritte le costanti, le enumerazioni e i flag della shell di Windows.
title: Costanti, enumerazioni e flag della shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 638beaa7-a065-4ab3-8eb5-286a306a8f24
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 2070ef1acc37262a526186862f46afa002c47343
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104234409"
---
# <a name="shell-constants-enumerations-and-flags"></a>Costanti, enumerazioni e flag della shell

In questa sezione vengono descritte le costanti, le enumerazioni e i flag della shell di Windows.

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
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_svgio"><strong>_SVGIO</strong></a><br/></td>
<td>Usato con i metodi <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-items"><strong>IFolderView:: Items</strong></a>, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-itemcount"><strong>IFolderView:: ItemCount</strong></a>e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-getitemobject"><strong>IShellView:: GetItemObject</strong></a> per limitare o controllare gli elementi nelle raccolte.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_svsif"><strong>_SVSIF</strong></a><br/></td>
<td>Indica i flag utilizzati da <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview"><strong>IFolderView</strong></a>, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview2"><strong>IFolderView2</strong></a>, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview2"><strong>IShellView2</strong></a> per specificare un tipo di selezione da applicare.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shappmgr/ne-shappmgr-appactionflags"><strong>APPACTIONFLAGS</strong></a><br/></td>
<td>Specifica le azioni di gestione delle applicazioni supportate da un server di pubblicazione dell'applicazione. Questi flag sono maschere di maschera passate a <a href="/windows/desktop/api/Shappmgr/nf-shappmgr-ishellapp-getpossibleactions"><strong>IShellApp:: GetPossibleActions</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shappmgr/ne-shappmgr-appinfodataflags"><strong>APPINFODATAFLAGS</strong></a><br/></td>
<td>Specifica le informazioni sull'applicazione che devono essere restituite da <a href="/windows/desktop/api/Shappmgr/nf-shappmgr-ishellapp-getappinfo"><strong>IShellApp:: GetAppInfo</strong></a>. Questi flag sono maschere di maschera utilizzate nel membro <a href="/windows/desktop/api/Shappmgr/ns-shappmgr-appinfodata"><strong>dwMask</strong></a> della struttura <strong>APPINFODATA</strong> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/ne-shobjidl_core-application_view_orientation"><strong>APPLICATION_VIEW_ORIENTATION</strong></a><br/></td>
<td>Definisce il set di modalità di orientamento della visualizzazione per una finestra (visualizzazione app). Usato da <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings2-getapplicationvieworientation"><strong>IApplicationDesignModeSettings2:: GetApplicationViewOrientation</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings2-setapplicationvieworientation"><strong>IApplicationDesignModeSettings2:: SetApplicationViewOrientation</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ne-shobjidl_core-application_view_size_preference"><strong>APPLICATION_VIEW_SIZE_PREFERENCE</strong></a><br/></td>
<td>Definisce il set di possibili preferenze di dimensione della finestra generale (visualizzazione app). Usato da <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ilaunchsourceviewsizepreference-getsourceviewsizepreference"><strong>ILaunchSourceViewSizePreference:: GetSourceViewSizePreference</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ilaunchtargetviewsizepreference-gettargetviewsizepreference"><strong>ILaunchTargetViewSizePreference:: GetTargetViewSizePreference</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-application_view_state"><strong>APPLICATION_VIEW_STATE</strong></a><br/></td>
<td>Indica lo stato di visualizzazione corrente di un'app di Windows Store. Usato da <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-setapplicationviewstate"><strong>IApplicationDesignModeSettings:: SetApplicationViewState</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-isapplicationviewstatesupported"><strong>IApplicationDesignModeSettings:: IsApplicationViewStateSupported</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-assocdata"><strong>ASSOCDATA</strong></a><br/></td>
<td>Usato da <a href="/windows/desktop/api/shlwapi/nf-shlwapi-iqueryassociations-getdata"><strong>IQueryAssociations:: GetData</strong></a> per definire il tipo di dati da restituire.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/shell/assocf_str"><strong>ASSOCF</strong></a><br/></td>
<td>Fornisce informazioni ai metodi dell'interfaccia <a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>IQueryAssociations</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationlevel"><strong>ASSOCIATIONLEVEL</strong></a><br/></td>
<td>Specifica l'origine dell'associazione predefinita per un'estensione del nome di file. Utilizzato dai metodi dell'interfaccia <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration"><strong>IApplicationAssociationRegistration</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationtype"><strong>ASSOCIATIONTYPE</strong></a><br/></td>
<td>Specifica il tipo di associazione per un'applicazione. Utilizzato dai metodi dell'interfaccia <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration"><strong>IApplicationAssociationRegistration</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-assockey"><strong>ASSOCKEY</strong></a><br/></td>
<td>Specifica il tipo di chiave che deve essere restituita da <a href="/windows/desktop/api/shlwapi/nf-shlwapi-iqueryassociations-getkey"><strong>IQueryAssociations:: GetKey</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-assocstr"><strong>ASSOCSTR</strong></a><br/></td>
<td>Usato da <a href="/windows/desktop/api/shlwapi/nf-shlwapi-iqueryassociations-getstring"><strong>IQueryAssociations:: GetString</strong></a> per definire il tipo di stringa da restituire.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-attachment_action"><strong>ATTACHMENT_ACTION</strong></a><br/></td>
<td>Fornisce un set di flag da usare con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-prompt"><strong>IAttachmentExecute::P rompt</strong></a> per indicare l'azione da eseguire alla conferma dell'utente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-attachment_prompt"><strong>ATTACHMENT_PROMPT</strong></a><br/></td>
<td>Fornisce un set di flag da usare con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iattachmentexecute-prompt"><strong>IAttachmentExecute::P rompt</strong></a> per indicare il tipo di interfaccia utente della richiesta di visualizzazione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shlobj_core/ne-shlobj_core-autocompletelistoptions"><strong>AUTOCOMPLETELISTOPTIONS</strong></a><br/></td>
<td>Specifica gli oggetti enumerati per gli elenchi di completamento automatico.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shldisp/ne-shldisp-autocompleteoptions"><strong>AUTOCOMPLETEOPTIONS</strong></a><br/></td>
<td>Specifica i valori usati da <a href="/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-getoptions"><strong>IAutoComplete2:: GetOptions</strong></a> e <a href="/windows/desktop/api/Shldisp/nf-shldisp-iautocomplete2-setoptions"><strong>IAutoComplete2:: SetOption</strong></a> per le opzioni che racchiudono il completamento automatico.<br/></td>
</tr>
<tr class="even">
<td><a href="str-constants.md"><strong>Chiavi della stringa di contesto di binding</strong></a><br/></td>
<td>Set di chiavi di stringa utilizzate con il metodo <a href="/windows/desktop/api/objidl/nf-objidl-ibindctx-registerobjectparam"><strong>IBindCtx:: RegisterObjectParam</strong></a> per specificare un contesto di associazione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shdeprecated/ne-shdeprecated-bnstate"><strong>BNSTATE</strong></a><br/></td>
<td>Deprecato. Usato da <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice-setnavigatestate"><strong>IBrowserService:: SetNavigateState</strong></a> e <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice-getnavigatestate"><strong>IBrowserService:: GetNavigateState</strong></a> per specificare gli Stati di navigazione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/ne-shobjidl_core-_browserframeoptions"><strong>BROWSERFRAMEOPTIONS</strong></a><br/></td>
<td>Utilizzato con il metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibrowserframeoptions-getframeoptions"><strong>IBrowserFrameOptions:: GetFrameOptions</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-categoryinfo_flags"><strong>CATEGORYINFO_FLAGS</strong></a><br/></td>
<td>Fornisce un set di flag da utilizzare con la struttura <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-category_info"><strong>CATEGORY_INFO</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-catsort_flags"><strong>CATSORT_FLAGS</strong></a><br/></td>
<td>Specifica i metodi per l'ordinamento dei dati di categoria.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/bb762483(v=vs.85)"><strong>CDCONTROLSTATE</strong></a><br/></td>
<td>Specifica i valori che indicano se un controllo è visibile e attivato. Utilizzato dai membri dell'interfaccia <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize"><strong>IFileDialogCustomize</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-cm_enum_flags"><strong>CM_ENUM_FLAGS</strong></a><br/></td>
<td>Utilizzato dai membri dell'interfaccia <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>icolumnmanager</strong></a> per specificare il set di colonne richiesto, ovvero tutti o solo quelli attualmente visibili.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-cm_mask"><strong>CM_MASK</strong></a><br/></td>
<td>Indica quali valori della struttura <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo"><strong>CM_COLUMNINFO</strong></a> devono essere impostati durante le chiamate a <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icolumnmanager-setcolumninfo"><strong>icolumnmanager:: SetRowInfo</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-cm_set_width_value"><strong>CM_SET_WIDTH_VALUE</strong></a><br/></td>
<td>Specifica i valori di larghezza in pixel e include supporto speciale per default e AutoSize. Utilizzato dai membri dell'interfaccia <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>icolumnmanager</strong></a> tramite la struttura <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo"><strong>CM_COLUMNINFO</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-cm_state"><strong>CM_STATE</strong></a><br/></td>
<td>Specifica i valori dello stato della colonna. Utilizzato dai membri dell'interfaccia <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>icolumnmanager</strong></a> tramite la struttura <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo"><strong>CM_COLUMNINFO</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/CredentialProvider/ne-credentialprovider-credential_provider_account_options"><strong>CREDENTIAL_PROVIDER_ACCOUNT_OPTIONS</strong></a><br/></td>
<td>Indica il tipo di credenziale che un provider di credenziali deve restituire per associare al &quot; riquadro altro utente &quot; . Utilizzato dal <a href="/windows/desktop/api/CredentialProvider/nf-credentialprovider-icredentialprovideruserarray-getaccountoptions"><strong>ICredentialProviderUserArray_GetAccountOptions</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/CredentialProvider/ne-credentialprovider-credential_provider_credential_field_options"><strong>CREDENTIAL_PROVIDER_CREDENTIAL_FIELD_OPTIONS</strong></a><br/></td>
<td>Fornisce opzioni di personalizzazione per un singolo campo in un'interfaccia utente di accesso o credenziali.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_field_interactive_state"><strong>CREDENTIAL_PROVIDER_FIELD_INTERACTIVE_STATE</strong></a><br/></td>
<td>Descrive lo stato di un campo e il modo in cui un utente può interagire con esso. I campi possono essere visualizzati da un provider di credenziali in un'ampia gamma di stati interattivi diversi.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_field_state"><strong>CREDENTIAL_PROVIDER_FIELD_STATE</strong></a><br/></td>
<td>Specifica lo stato di un singolo campo nell'interfaccia utente delle credenziali.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_field_type"><strong>CREDENTIAL_PROVIDER_FIELD_TYPE</strong></a><br/></td>
<td>Specifica un tipo di campo Credential. Utilizzato dal <a href="/windows/desktop/api/Credentialprovider/ns-credentialprovider-credential_provider_field_descriptor"><strong>CREDENTIAL_PROVIDER_FIELD_DESCRIPTOR</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_get_serialization_response"><strong>CREDENTIAL_PROVIDER_GET_SERIALIZATION_RESPONSE</strong></a><br/></td>
<td>Descrive la risposta quando un provider di credenziali tenta di serializzare le credenziali.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_status_icon"><strong>CREDENTIAL_PROVIDER_STATUS_ICON</strong></a><br/></td>
<td>Indica quale icona di stato deve essere visualizzata.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/ne-credentialprovider-credential_provider_usage_scenario"><strong>CREDENTIAL_PROVIDER_USAGE_SCENARIO</strong></a><br/></td>
<td>Dichiara gli scenari in cui un provider di credenziali è supportato. Uno scenario di utilizzo del provider di credenziali (CPU) consente al provider di credenziali di fornire un comportamento di enumerazione distinto e la configurazione dei campi dell'interfaccia utente tra scenari.<br/></td>
</tr>
<tr class="even">
<td><a href="csidl.md"><strong>CSIDL</strong></a><br/></td>
<td><blockquote>
<p><b>Nota: </b> A partire da Windows Vista, questi valori sono stati sostituiti dai valori <a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a> . Per un elenco delle nuove costanti e dei valori CSIDL corrispondenti, vedere l'argomento. Per praticità, vengono indicati anche i valori <strong>KNOWNFOLDERID</strong> corrispondenti per ogni valore di CSIDL.</p>
<p>Il sistema CSIDL è supportato in Windows Vista per motivi di compatibilità. Tuttavia, il nuovo sviluppo deve usare valori <a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a> anziché valori CSIDL.<br/></p>
</blockquote>
<br/> I valori CSIDL (Constant Special Item ID List) forniscono un modo univoco indipendente dal sistema per identificare le cartelle speciali usate spesso dalle applicazioni, ma che non hanno lo stesso nome o percorso in un determinato sistema. La cartella di sistema, ad esempio, può essere &quot; C:\Windows &quot; in un sistema e &quot; C:\Winnt &quot; in un altro. Queste costanti sono definite in Shlobj. h.<br/></td>
</tr>
<tr class="odd">
<td><a href="ctf.md"><strong>Flag CTF</strong></a><br/></td>
<td>Flag che controllano il comportamento della funzione chiamante. Usato da <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethread"><strong>SHCreateThread</strong></a> e <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shcreatethreadwithhandle"><strong>SHCreateThreadWithHandle</strong></a>. In tali funzioni, questi valori sono definiti come di tipo SHCT_FLAGS.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-dataobj_get_item_flags"><strong>DATAOBJ_GET_ITEM_FLAGS</strong></a><br/></td>
<td>Valori utilizzati dalla funzione <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetitemfromdataobject"><strong>SHGetItemFromDataObject</strong></a> per specificare le opzioni relative all'elaborazione dell'oggetto di origine.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-tagdeskbandcid"><strong>Flag di comando DBID</strong></a><br/></td>
<td>Questi ID comando possono essere inviati al contenitore dell'oggetto band con <a href="/windows/desktop/api/docobj/nf-docobj-iolecommandtarget-exec"><strong>IOleCommandTarget:: Exec</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-def_share_id"><strong>DEF_SHARE_ID</strong></a><br/></td>
<td>Valori che specificano la cartella a cui agiscono i metodi dell'interfaccia <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isharingconfigurationmanager"><strong>ISharingConfigurationManager</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-defaultsavefoldertype"><strong>DEFAULTSAVEFOLDERTYPE</strong></a><br/></td>
<td>Specifica il percorso di salvataggio predefinito.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-default_folder_menu_restrictions"><strong>DEFAULT_FOLDER_MENU_RESTRICTIONS</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-desktop_wallpaper_position"><strong>DESKTOP_WALLPAPER_POSITION</strong></a><br/></td>
<td>Specifica la modalità di visualizzazione dello sfondo del desktop.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shtypes/ne-shtypes-device_scale_factor"><strong>DEVICE_SCALE_FACTOR</strong></a><br/></td>
<td>Indica un fattore di scala del dispositivo falsificato, come percentuale. Usato da <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-setapplicationviewstate"><strong>IApplicationDesignModeSettings:: SetApplicationViewState</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-isapplicationviewstatesupported"><strong>IApplicationDesignModeSettings:: IsApplicationViewStateSupported</strong></a><br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingAPI/ne-shellscalingapi-display_device_type"><strong>DISPLAY_DEVICE_TYPE</strong></a><br/></td>
<td>Indica se il dispositivo è un tipo di visualizzazione principale o immersivo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype"><strong>DROPIMAGETYPE</strong></a><br/></td>
<td>Valori utilizzati con la struttura <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription"><strong>DROPDESCRIPTION</strong></a> per specificare l'immagine di rilascio.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_expcmdstate"><strong>EXPCMDSTATE</strong></a><br/></td>
<td>I valori <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_expcmdstate"><strong>EXPCMDSTATE</strong></a> rappresentano lo stato del comando di un elemento della shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-explorer_browser_fill_flags"><strong>EXPLORER_BROWSER_FILL_FLAGS</strong></a><br/></td>
<td>Questi flag vengono usati con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-fillfromobject"><strong>IExplorerBrowser:: FillFromObject</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-explorer_browser_options"><strong>EXPLORER_BROWSER_OPTIONS</strong></a><br/></td>
<td>Questi flag vengono usati con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-getoptions"><strong>IExplorerBrowser:: GetOptions</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-setoptions"><strong>IExplorerBrowser:: SetOption</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_explorerpanestate"><strong>EXPLORERPANESTATE</strong></a><br/></td>
<td>Indica i flag usati da <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate"><strong>IExplorerPaneVisibility:: GetPaneState</strong></a> per ottenere lo stato corrente del riquadro di Esplora risorse specificato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-fdap"><strong>FDAP</strong></a><br/></td>
<td>Specifica la posizione dell'elenco.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-fde_overwrite_response"><strong>FDE_OVERWRITE_RESPONSE</strong></a><br/></td>
<td>Specifica i valori utilizzati dal metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onoverwrite"><strong>IFileDialogEvents:: OnWrite</strong></a> per indicare la risposta di un'applicazione a una richiesta di sovrascrittura durante un'operazione di salvataggio utilizzando la finestra di dialogo file comune.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-fde_shareviolation_response"><strong>FDE_SHAREVIOLATION_RESPONSE</strong></a><br/></td>
<td>Specifica i valori utilizzati dal metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onshareviolation"><strong>IFileDialogEvents:: OnShareViolation</strong></a> per indicare la risposta di un'applicazione a una violazione di condivisione che si verifica quando un file viene aperto o salvato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-fffp_mode"><strong>FFFP_MODE</strong></a><br/></td>
<td>Descrive i criteri di corrispondenza. Utilizzato dai metodi dell'interfaccia <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager"><strong>IKnownFolderManager</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-file_usage_type"><strong>FILE_USAGE_TYPE</strong></a><br/></td>
<td>Costanti utilizzate da <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileisinuse-getusage"><strong>IFileIsInUse:: getusage</strong></a> per indicare la modalità di utilizzo di un file in uso.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_fileopendialogoptions"><strong>FILEOPENDIALOGOPTIONS</strong></a><br/></td>
<td>Definisce il set di opzioni disponibili per una finestra di dialogo Apri o Salva.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>FILETYPEATTRIBUTEFLAGS</strong></a><br/></td>
<td>Indica le costanti <a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>FILETYPEATTRIBUTEFLAGS</strong></a> utilizzate nel valore flag della chiave del registro di sistema <a href="fa-progids.md">ProgID</a> di un'associazione di file.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folder_enum_mode"><strong>FOLDER_ENUM_MODE</strong></a><br/></td>
<td>Usato dai metodi <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iobjectwithfolderenummode-getmode"><strong>IObjectWithFolderEnumMode:: GetMode</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iobjectwithfolderenummode-setmode"><strong>IObjectWithFolderEnumMode:: semode</strong></a> per ottenere e impostare le modalità di visualizzazione per le cartelle.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderflags"><strong>FOLDERFLAGS</strong></a><br/></td>
<td>Set di flag che specificano le opzioni di visualizzazione cartelle. I flag sono indipendenti l'uno dall'altro e possono essere usati in qualsiasi combinazione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderlogicalviewmode"><strong>FOLDERLOGICALVIEWMODE</strong></a><br/></td>
<td>Usato da <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderviewsettings-getviewmode"><strong>IFolderViewSettings:: GetViewMode</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-setfolderlogicalviewmode"><strong>ISearchFolderItemFactory:: SetFolderLogicalViewMode</strong></a> per descrivere la modalità di visualizzazione.<br/></td>
</tr>
<tr class="odd">
<td><a href="foldertypeid.md"><strong>FOLDERTYPEID</strong></a><br/></td>
<td>I valori <a href="foldertypeid.md"><strong>FOLDERTYPEID</strong></a> rappresentano un modello di vista applicato a una cartella, in genere in base all'utilizzo e al contenuto previsti.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode"><strong>FOLDERVIEWMODE</strong></a><br/></td>
<td>Specifica il tipo di visualizzazione cartella.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/ne-shobjidl-folderviewoptions"><strong>FOLDERVIEWOPTIONS</strong></a><br/></td>
<td>Utilizzato dai metodi dell'interfaccia <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifolderviewoptions"><strong>IFolderViewOptions</strong></a> per attivare le opzioni di Windows Vista non supportate per impostazione predefinita nei sistemi Windows 7 e versioni successive, nonché la disattivazione delle nuove opzioni di Windows 7.<br/></td>
</tr>
<tr class="even">
<td><a href="iactivedesktop-flags.md"><strong>Flag IActiveDesktop</strong></a><br/></td>
<td>In questa sezione vengono descritti i flag utilizzati dai metodi dell'interfaccia <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iactivedesktop"><strong>IActiveDesktop</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shlobj_core/ne-shlobj_core-ieshortcutflags"><strong>IESHORTCUTFLAGS</strong></a><br/></td>
<td>Specifica il modo in cui un tasto di scelta rapida deve essere gestito dal browser.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-kf_category"><strong>KF_CATEGORY</strong></a><br/></td>
<td>Valore che rappresenta una categoria in base alla quale è possibile classificare una cartella registrata con il sistema di cartelle note.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_kf_definition_flags"><strong>KF_DEFINITION_FLAGS</strong></a><br/></td>
<td>Flag che specificano alcuni comportamenti noti della cartella. Utilizzato con la struttura <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition"><strong>KNOWNFOLDER_DEFINITION</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_kf_redirect_flags"><strong>KF_REDIRECT_FLAGS</strong></a><br/></td>
<td>Flag usati da <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-redirect"><strong>IKnownFolderManager:: redirect</strong></a> per specificare i dettagli di un reindirizzamento di cartelle note, ad esempio le autorizzazioni e la proprietà per la cartella reindirizzata.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_kf_redirection_capabilities"><strong>KF_REDIRECTION_CAPABILITIES</strong></a><br/></td>
<td>Flag che specificano le funzionalità di reindirizzamento correnti di una cartella nota. Usato da <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getredirectioncapabilities"><strong>IKnownFolder:: GetRedirectionCapabilities</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag"><strong>KNOWN_FOLDER_FLAG</strong></a><br/></td>
<td>Specificare opzioni di recupero speciali per le cartelle note. Questi valori sostituiscono i valori <a href="csidl.md"><strong>CSIDL</strong></a> , che hanno significati paralleli.<br/></td>
</tr>
<tr class="odd">
<td><a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a><br/></td>
<td>Le costanti <a href="knownfolderid.md"><strong>KNOWNFOLDERID</strong></a> rappresentano i GUID che identificano le cartelle standard registrate con il sistema come <a href="known-folders.md">cartelle note</a>. Queste cartelle vengono installate con Windows Vista e sistemi operativi successivi e un computer avrà solo le cartelle appropriate per l'installazione. Per le descrizioni di queste cartelle, vedere <a href="csidl.md"><strong>CSIDL</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-libraryfolderfilter"><strong>LIBRARYFOLDERFILTER</strong></a><br/></td>
<td>Definisce le opzioni per filtrare gli elementi della cartella. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-librarymanagedialogoptions"><strong>LIBRARYMANAGEDIALOGOPTIONS</strong></a><br/></td>
<td>Usato da <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shshowmanagelibraryui"><strong>SHShowManageLibraryUI</strong></a> per definire le opzioni per la gestione di un conflitto di nomi durante il salvataggio di una libreria.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-libraryoptionflags"><strong>LIBRARYOPTIONFLAGS</strong></a><br/></td>
<td>Specifica le opzioni della libreria.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-librarysaveflags"><strong>LIBRARYSAVEFLAGS</strong></a><br/></td>
<td>Specifica le opzioni per la gestione di un conflitto di nomi durante il salvataggio di una libreria. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Intshcut/ne-intshcut-mimeassociationdialog_in_flags"><strong>MIMEASSOCIATIONDIALOG_IN_FLAGS</strong></a><br/></td>
<td>Utilizzato con la funzione <a href="/windows/desktop/api/Intshcut/nf-intshcut-mimeassociationdialoga"><strong>MIMEAssociationDialog</strong></a> per determinare la modalità di esecuzione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-monitor_app_visibility"><strong>MONITOR_APP_VISIBILITY</strong></a><br/></td>
<td>Specifica se una visualizzazione Mostra le finestre desktop anziché le app di Windows Store.<br/></td>
</tr>
<tr class="even">
<td><a href="mp-popupflags.md"><strong>Costanti MP_POPUPFLAGS</strong></a><br/></td>
<td>Rappresenta le opzioni disponibili quando si visualizza un menu di scelta rapida.<br/></td>
</tr>
<tr class="odd">
<td><a href="net-string.md"><strong>NET_STRING</strong></a><br/></td>
<td>Rappresentano i tipi di indirizzi di rete. Usare uno o più (come combinazione bit per bit) delle costanti seguenti per creare una maschera di indirizzo di rete da usare con la macro <a href="/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype"><strong>NetAddr_SetAllowType</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-nstcfoldercapabilities"><strong>NSTCFOLDERCAPABILITIES</strong></a><br/></td>
<td>Specifica lo stato di un elemento della struttura ad albero. Questi valori vengono usati dai metodi dell'interfaccia <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrolfoldercapabilities"><strong>INameSpaceTreeControlFolderCapabilities</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_nstcitemstate"><strong>NSTCITEMSTATE</strong></a><br/></td>
<td>Specifica lo stato di un elemento della struttura ad albero. Questi valori vengono usati dai metodi dell'interfaccia <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol"><strong>INameSpaceTreeControl</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_nstcstyle"><strong>NSTCSTYLE</strong></a><br/></td>
<td>Descrive le caratteristiche di un determinato controllo struttura ad albero dello spazio dei nomi.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/ne-shobjidl-nstcstyle2"><strong>NSTCSTYLE2</strong></a><br/></td>
<td>Usato dai metodi di <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrol2"><strong>INameSpaceTreeControl2</strong></a> per specificare gli stili di visualizzazione estesi in un TreeView dello spazio dei nomi della shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-nwmf"><strong>NWMF</strong></a><br/></td>
<td>Flag utilizzati da <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-inewwindowmanager-evaluatenewwindow"><strong>INewWindowManager:: EvaluateNewWindow</strong></a>. Questi valori sono fattori nella decisione di visualizzare o meno una finestra popup.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-package_execution_state"><strong>PACKAGE_EXECUTION_STATE</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/win32/api/shtypes/ne-shtypes-perceived"><strong>PERCEPITA</strong></a><br/></td>
<td>Specifica il tipo percepito di un file. Questo set di costanti viene utilizzato nella funzione <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype"><strong>AssocGetPerceivedType</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/shappmgr/ne-shappmgr-pubappinfoflags"><strong>PUBAPPINFOFLAGS</strong></a><br/></td>
<td>Specifica quali membri della struttura <a href="/windows/desktop/api/Shappmgr/ns-shappmgr-pubappinfo"><strong>PUBAPPINFO</strong></a> sono validi. Questi flag sono maschere di maschere impostate nel membro <strong>dwMask</strong> e passati a <a href="/windows/desktop/api/Shappmgr/nf-shappmgr-ipublishedapp-getpublishedappinfo"><strong>IPublishedApp:: GetPublishedAppInfo</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ne-shellapi-query_user_notification_state"><strong>QUERY_USER_NOTIFICATION_STATE</strong></a><br/></td>
<td>Specifica lo stato del computer per l'utente corrente in relazione alla proprietà dell'invio di una notifica. Usato da <a href="/windows/desktop/api/Shellapi/nf-shellapi-shqueryusernotificationstate"><strong>SHQueryUserNotificationState</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="hkey-type.md"><strong>Tipi di dati del registro di sistema</strong></a><br/></td>
<td>Questi tipi di dati possono essere utilizzati per specificare il tipo di un valore del registro di sistema.<br/></td>
</tr>
<tr class="even">
<td><a href="regsam.md"><strong>REGSAM</strong></a><br/></td>
<td>Tipo di dati utilizzato per specificare gli attributi di accesso di sicurezza nel registro di sistema.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions"><strong>RESTRIZIONI</strong></a><br/></td>
<td>Questi flag vengono utilizzati con la funzione <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shrestricted"><strong>SHRestricted</strong></a> . <strong>SHRestricted</strong> viene utilizzato per determinare se i criteri di amministratore specificati sono attivi. In molti casi, le applicazioni devono modificare determinati comportamenti per conformarsi ai criteri applicati dagli amministratori di sistema.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/ShellScalingAPI/ne-shellscalingapi-scale_change_flags"><strong>SCALE_CHANGE_FLAGS</strong></a><br/></td>
<td>Flag utilizzati per indicare la modifica di ridimensionamento che si è verificata.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-scnrt_status"><strong>SCNRT_STATUS</strong></a><br/></td>
<td>Indica se abilitare o disabilitare il registro asincrono e annullare la registrazione per <a href="/windows/desktop/api/Shlobj/nf-shlobj-shchangenotifyregisterthread"><strong>SHChangeNotifyRegisterThread</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-tagsfbs_flags"><strong>SFBS_FLAGS</strong></a><br/></td>
<td>Specifica il modo in cui la funzione <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizeex"><strong>StrFormatByteSizeEx</strong></a> deve gestire l'arrotondamento di cifre non visualizzate.<br/></td>
</tr>
<tr class="odd">
<td><a href="sfgao.md"><strong>SFGAO</strong></a><br/></td>
<td>Attributi che possono essere recuperati su un elemento (file o cartella) o un set di elementi.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-shard"><strong>PARTIZIONE</strong></a><br/></td>
<td>Indica l'interpretazione dei dati passati da <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs"><strong>funzione SHAddToRecentDocs</strong></a> nel parametro <em>PV</em> per identificare l'elemento di cui vengono rilevate le statistiche di utilizzo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-share_role"><strong>SHARE_ROLE</strong></a><br/></td>
<td>Specifica le autorizzazioni di accesso assegnate a <strong>utenti</strong> o cartelle <strong>pubbliche</strong> . Usato in <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isharingconfigurationmanager-createshare"><strong>createshare</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isharingconfigurationmanager-getsharepermissions"><strong>GetSharePermissions</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shtypes/ne-shtypes-shcolstate"><strong>SHCOLSTATE</strong></a><br/></td>
<td>Viene descritta la modalità di trattamento di una proprietà. Questi valori sono definiti in shtypes. h.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_shcontf"><strong>SHCONTF</strong></a><br/></td>
<td>Determina i tipi di elementi inclusi in un'enumerazione. Questi valori vengono usati con il metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects"><strong>IShellFolder:: EnumObjects</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/ne-shlobj_core-shell_link_data_flags"><strong>SHELL_LINK_DATA_FLAGS</strong></a><br/></td>
<td>Specifica le impostazioni delle opzioni. Usato con <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinkdatalist-getflags"><strong>IShellLinkDataList:: GetFlags</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinkdatalist-setflags"><strong>IShellLinkDataList:: Flags</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-shell_ui_component"><strong>SHELL_UI_COMPONENT</strong></a><br/></td>
<td>Identifica il tipo di componente dell'interfaccia utente necessario nella shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shldisp/ne-shldisp-shellfolderviewoptions"><strong>ShellFolderViewOptions</strong></a><br/></td>
<td>Specifica le opzioni di visualizzazione restituite dalla proprietà <a href="shellfolderview-viewoptions.md"><strong>ViewOptions</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants"><strong>ShellSpecialFolderConstants</strong></a><br/></td>
<td>Specifica i valori univoci indipendenti dal sistema che identificano cartelle speciali. Queste cartelle vengono spesso usate dalle applicazioni, ma non hanno lo stesso nome o percorso in un determinato sistema. La cartella di sistema, ad esempio, può essere &quot; C:\Windows &quot; in un sistema e &quot; C:\Winnt &quot; in un altro.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/ExDisp/ne-exdisp-shellwindowfindwindowoptions"><strong>ShellWindowFindWindowOptions</strong></a><br/></td>
<td>Specifica le opzioni per la ricerca della finestra nell'insieme di finestre della shell. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Exdisp/ne-exdisp-shellwindowtypeconstants"><strong>ShellWindowTypeConstants</strong></a><br/></td>
<td>Specifica i tipi di finestre della shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_shgdnf"><strong>SHGDNF</strong></a><br/></td>
<td>Definisce i valori usati con i metodi <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder:: GetDisplayNameOf</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-setnameof"><strong>IShellFolder:: SetNameOf</strong></a> per specificare il tipo di nome di file o di cartella usati da tali metodi. <br/>
<blockquote>
<b>Nota:</b><br />
Prima di Windows 7, questi valori erano inclusi nell'enumerazione SHGNO.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-shglobalcounter"><strong>SHGLOBALCOUNTER</strong></a><br/></td>
<td>Identificatori per vari contatori globali o variabili condivise. È possibile incrementare o decrementare ogni contatore globale usando <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shglobalcounterincrement"><strong>SHGlobalCounterIncrement</strong></a> e <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shglobalcounterdecrement"><strong>SHGlobalCounterDecrement</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-shregdel_flags"><strong>SHREGDEL_FLAGS</strong></a><br/></td>
<td>Fornisce un set di valori che indicano da quale chiave di base verrà eliminato un elemento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-shregenum_flags"><strong>SHREGENUM_FLAGS</strong></a><br/></td>
<td>Fornisce un set di valori che indicano la chiave di base che verrà usata per un'enumerazione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shellapi/ne-shellapi-shstockiconid"><strong>SHSTOCKICONID</strong></a><br/></td>
<td>Usato da <a href="/windows/desktop/api/Shellapi/nf-shellapi-shgetstockiconinfo"><strong>SHGetStockIconInfo</strong></a> per identificare l'icona del sistema azionario da recuperare.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_sichintf"><strong>SICHINTF</strong></a><br/></td>
<td>Utilizzato per determinare come confrontare due elementi della shell. <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-compare"><strong>IShellItem:: compare</strong></a> utilizza questo tipo enumerato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-sigdn"><strong>SIGDN</strong></a><br/></td>
<td>Richiede il form del nome visualizzato di un elemento da recuperare tramite <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname"><strong>IShellItem:: GetDisplayName</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetnamefromidlist"><strong>SHGetNameFromIDList</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-spaction"><strong>SPACTION</strong></a><br/></td>
<td>Descrive un'azione eseguita che richiede lo stato di avanzamento da visualizzare all'utente utilizzando un'interfaccia <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogress"><strong>IActionProgress</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_spbeginf"><strong>SPBEGINF</strong></a><br/></td>
<td>Usato da <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iactionprogress-begin"><strong>IActionProgress:: Begin</strong></a>, queste costanti specificano determinate operazioni dell'interfaccia utente che devono essere abilitate o disabilitate.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-sptext"><strong>SPTEXT</strong></a><br/></td>
<td>Specifica il tipo di testo descrittivo fornito a un'interfaccia <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogress"><strong>IActionProgress</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="srrf.md"><strong>SRRF</strong></a><br/></td>
<td>Flag che limitano l'impostazione o la restituzione dei dati.<br/></td>
</tr>
<tr class="odd">
<td><a href="ssf-constants.md"><strong>Costanti SSF</strong></a><br/></td>
<td>Usato dalla funzione <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetsetsettings"><strong>SHGetSetSettings</strong></a> per specificare i membri della relativa struttura <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-shellstatea"><strong>ShellState</strong></a> da impostare o recuperati.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-stpflag"><strong>STPFLAG</strong></a><br/></td>
<td>Utilizzato dal metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist4-settabproperties"><strong>ITaskbarList4:: SetTabProperties</strong></a> per specificare le proprietà di tabulazione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-svuia_status"><strong>SVUIA_STATUS</strong></a><br/></td>
<td>Utilizzato con il metodo <a href="/windows/desktop/api/Shdeprecated/nf-shdeprecated-ibrowserservice2-_uiactivateview"><strong>IBrowserService2:: _UIActivateView</strong></a> per impostare lo stato di una visualizzazione del browser.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_cancel_request"><strong>SYNCMGR_CANCEL_REQUEST</strong></a><br/></td>
<td>Descrive una richiesta da parte dell'utente di annullare una sincronizzazione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_conflict_item_type"><strong>SYNCMGR_CONFLICT_ITEM_TYPE</strong></a><br/></td>
<td>Descrive il tipo di elemento Conflict.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_control_flags"><strong>SYNCMGR_CONTROL_FLAGS</strong></a><br/></td>
<td>Specifica la modalità di esecuzione di un'operazione richiesta su determinati metodi di <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrcontrol"><strong>ISyncMgrControl</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_event_flags"><strong>SYNCMGR_EVENT_FLAGS</strong></a><br/></td>
<td>Specifica i flag per un evento di sincronizzazione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_event_level"><strong>SYNCMGR_EVENT_LEVEL</strong></a><br/></td>
<td>Specifica il tipo di evento segnalato al centro di sincronizzazione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_handler_capabilities"><strong>SYNCMGR_HANDLER_CAPABILITIES</strong></a><br/></td>
<td>Specifica le funzionalità di un gestore relative alle azioni che possono essere eseguite su di esso.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_handler_policies"><strong>SYNCMGR_HANDLER_POLICIES</strong></a><br/></td>
<td>Enumera i criteri specificati da un gestore di sincronizzazione che devia dal criterio predefinito.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_handler_type"><strong>SYNCMGR_HANDLER_TYPE</strong></a><br/></td>
<td>Specifica il tipo di un gestore. Usato da <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrhandlerinfo-gettype"><strong>ISyncMgrHandlerInfo:: GetType</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_item_capabilities"><strong>SYNCMGR_ITEM_CAPABILITIES</strong></a><br/></td>
<td>Specifica le azioni che possono essere eseguite su un elemento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_item_policies"><strong>SYNCMGR_ITEM_POLICIES</strong></a><br/></td>
<td>Specifica i criteri di un elemento per controllare come possono essere abilitati o disabilitati da criteri di gruppo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_presenter_choice"><strong>SYNCMGR_PRESENTER_CHOICE</strong></a><br/></td>
<td>Descrive la scelta effettuata da un utente sulla risoluzione dei conflitti di gestione sincronizzazione. Usato da <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictpresenter"><strong>ISyncMgrConflictPresenter</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_presenter_next_step"><strong>SYNCMGR_PRESENTER_NEXT_STEP</strong></a><br/></td>
<td>Descrive il passaggio successivo che deve verificarsi nella risoluzione dei conflitti di gestione sincronizzazione. Usato da <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictpresenter"><strong>ISyncMgrConflictPresenter</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_progress_status"><strong>SYNCMGR_PROGRESS_STATUS</strong></a><br/></td>
<td>Specifica lo stato di avanzamento corrente di un processo di sincronizzazione. Usato da <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrsynccallback-reportprogress"><strong>ISyncMgrSyncCallback:: ReportProgress</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_resolution_abilities"><strong>SYNCMGR_RESOLUTION_ABILITIES</strong></a><br/></td>
<td>Indica le funzionalità e l'attività di risoluzione dei conflitti da seguire. Usato con <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrresolutionhandler-queryabilities"><strong>ISyncMgrResolutionHandler:: QueryAbilities</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_resolution_feedback"><strong>SYNCMGR_RESOLUTION_FEEDBACK</strong></a><br/></td>
<td>Descrive Gestione sincronizzazione commenti sulla risoluzione. Usato da <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrresolutionhandler"><strong>ISyncMgrResolutionHandler</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/ne-syncmgr-syncmgr_sync_control_flags"><strong>SYNCMGR_SYNC_CONTROL_FLAGS</strong></a><br/></td>
<td>Indica i flag utilizzati da <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrcontrol-starthandlersync"><strong>ISyncMgrControl:: StartHandlerSync</strong></a> e <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrcontrol-startitemsync"><strong>ISyncMgrControl:: StartItemSync</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrflag"><strong>SYNCMGRFLAG</strong></a><br/></td>
<td>I valori di enumerazione <a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrflag"><strong>SYNCMGRFLAG</strong></a> vengono utilizzati nel metodo <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-initialize"><strong>ISyncMgrSynchronize:: Initialize</strong></a> per indicare la modalità di avvio dell'evento di sincronizzazione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrhandlerflags"><strong>SYNCMGRHANDLERFLAGS</strong></a><br/></td>
<td>Utilizzato nella struttura <a href="/windows/win32/api/mobsync/ns-mobsync-syncmgrhandlerinfo"><strong>SYNCMGRHANDLERINFO</strong></a> come flag applicabili al gestore corrente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrinvokeflags"><strong>SYNCMGRINVOKEFLAGS</strong></a><br/></td>
<td>Il valore di enumerazione <a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrinvokeflags"><strong>SYNCMGRINVOKEFLAGS</strong></a> specifica il modo in cui deve essere richiamato il Gestione sincronizzazione nel metodo <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizeinvoke-updateitems"><strong>ISyncMgrSynchronizeInvoke:: UpdateItems</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgritemflags"><strong>SYNCMGRITEMFLAGS</strong></a><br/></td>
<td>Specifica le informazioni per l'elemento corrente nella struttura <a href="/windows/win32/api/mobsync/ns-mobsync-syncmgritem"><strong>SYNCMGRITEM</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrloglevel"><strong>SYNCMGRLOGLEVEL</strong></a><br/></td>
<td>I valori di enumerazione <a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrloglevel"><strong>SYNCMGRLOGLEVEL</strong></a> specificano un livello di errore da usare nel metodo <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronizecallback-logerror"><strong>ISyncMgrSynchronizeCallback:: LogError</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrregisterflags"><strong>SYNCMGRREGISTERFLAGS</strong></a><br/></td>
<td>I valori di enumerazione <a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrregisterflags"><strong>SYNCMGRREGISTERFLAGS</strong></a> vengono usati nei metodi dell'interfaccia <a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrregister"><strong>ISyncMgrRegister</strong></a> per identificare gli eventi per i quali il gestore è registrato per ricevere una notifica.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/mobsync/ne-mobsync-syncmgrstatus"><strong>SYNCMGRSTATUS</strong></a><br/></td>
<td>Usato nel metodo <a href="/windows/desktop/api/Mobsync/nf-mobsync-isyncmgrsynchronize-setitemstatus"><strong>ISyncMgrSynchronize:: SetItemStatus</strong></a> per specificare lo stato aggiornato per l'elemento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-thumbbuttonflags"><strong>THUMBBUTTONFLAGS</strong></a><br/></td>
<td>Usato da <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton"><strong>ThumbButton</strong></a> per controllare stati e comportamenti specifici del pulsante.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-thumbbuttonmask"><strong>THUMBBUTTONMASK</strong></a><br/></td>
<td>Utilizzato dalla struttura <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton"><strong>ThumbButton</strong></a> per specificare i membri della struttura che contengono dati validi.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/thumbnailstreamcache/ne-thumbnailstreamcache-thumbnailstreamcacheoptions"><strong>ThumbnailStreamCacheOptions</strong></a><br/></td>
<td>Definisce le opzioni della cache utilizzate dall'interfaccia <a href="/windows/desktop/api/thumbnailstreamcache/nn-thumbnailstreamcache-ithumbnailstreamcache"><strong>IThumbnailStreamCache</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-_transfer_source_flags"><strong>TRANSFER_SOURCE_FLAGS</strong></a><br/></td>
<td>Usato dai metodi delle interfacce <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfersource"><strong>ITransferSource</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferdestination"><strong>ITransferDestination</strong></a> per controllare le operazioni sui file.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Intshcut/ne-intshcut-translateurl_in_flags"><strong>TRANSLATEURL_IN_FLAGS</strong></a><br/></td>
<td>I <a href="/windows/desktop/api/Intshcut/ne-intshcut-translateurl_in_flags"><strong>TRANSLATEURL_IN_FLAGS</strong></a> valori enumerati vengono utilizzati con la funzione <a href="/windows/desktop/api/Intshcut/nf-intshcut-translateurla"><strong>TRANSLATEURL</strong></a> per determinare come verrà eseguita.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/ne-shobjidl-undock_reason"><strong>UNDOCK_REASON</strong></a><br/></td>
<td>Valori che indicano il motivo per cui una finestra dell'app di accessibilità ancorata è stata disancorata. Usato da <a href="/windows/desktop/api/shobjidl/nf-shobjidl-iaccessibilitydockingservicecallback-undocked"><strong>IAccessibilityDockingServiceCallback:: Undocked</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/ne-shlwapi-url_scheme"><strong>URL_SCHEME</strong></a><br/></td>
<td>Utilizzato per specificare gli schemi URL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Intshcut/ne-intshcut-urlassociationdialog_in_flags"><strong>URLASSOCIATIONDIALOG_IN_FLAGS</strong></a><br/></td>
<td>I <a href="/windows/desktop/api/Intshcut/ne-intshcut-urlassociationdialog_in_flags"><strong>URLASSOCIATIONDIALOG_IN_FLAGS</strong></a> valori enumerati vengono utilizzati con <a href="/windows/desktop/api/Intshcut/nf-intshcut-urlassociationdialoga"><strong>URLASSOCIATIONDIALOG</strong></a> per determinare la modalità di esecuzione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/ne-shobjidl-vpcolorflags"><strong>VPCOLORFLAGS</strong></a><br/></td>
<td>Specifica l'uso di un colore. Utilizzato dai metodi <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ivisualproperties"><strong>IVisualProperties</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/ne-shobjidl-vpwatermarkflags"><strong>VPWATERMARKFLAGS</strong></a><br/></td>
<td>Specifica i flag di filigrana. Utilizzato da <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-ivisualproperties-setwatermark"><strong>IVisualProperties:: towatermark</strong></a>.<br/></td>
</tr>
</tbody>
</table>



 

 

 

---
description: In questa sezione vengono descritte le interfacce della shell di Windows.
title: 'Interfacce di shell '
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 05223970-14f5-44c2-937b-07826b8aecf9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 23bd87e86ba9e30ce443616920326bf37aba6d2c
ms.sourcegitcommit: 9a614d8ce23dcca88873148683d9ec7d38be57b9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/12/2020
ms.locfileid: "104399991"
---
# <a name="shell-interfaces"></a>Interfacce di shell 

In questa sezione vengono descritte le interfacce della shell di Windows.

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
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iaccessibleobject"><strong>IAccessibleObject</strong></a><br/></td>
<td>Espone un metodo che può essere utilizzato da un'applicazione di accessibilità.<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/hh448546(v=vs.85)"><strong>IAccessibilityDockingService</strong></a><br/></td>
<td>Ancora una singola finestra dell'app di accessibilità nella parte inferiore di una schermata.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/hh448547(v=vs.85)"><strong>IAccessibilityDockingServiceCallback</strong></a><br/></td>
<td>Informa un'app di accessibilità che la finestra è stata disancorata.<br/></td>
</tr>
<tr class="even">
<td><a href="iaclcustommru.md"><strong>IACLCustomMRU</strong></a><br/></td>
<td>Espone i metodi usati per inizializzare un elenco usato più di recente (MRU) per un oggetto di completamento automatico.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iaclist"><strong>IACList</strong></a><br/></td>
<td>Espone un metodo che migliora l'efficienza del <a href="/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete"><strong>completamento automatico</strong></a> quando le stringhe candidate sono organizzate in una gerarchia.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iaclist2"><strong>IACList2</strong></a><br/></td>
<td>Estende l'interfaccia <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iaclist"><strong>IACList</strong></a> per consentire ai client di un oggetto di completamento automatico di recuperare e impostare i flag di opzione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogress"><strong>IActionProgress</strong></a><br/></td>
<td>Rappresenta la classe di base astratta da cui possono ereditare le operazioni basate sullo stato di avanzamento.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iactionprogressdialog"><strong>IActionProgressDialog</strong></a><br/></td>
<td>Espone metodi che inizializzano e arrestano una finestra di dialogo di stato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationactivationmanager"><strong>IApplicationActivationManager</strong></a><br/></td>
<td>Fornisce metodi che attivano le app di Windows Store per le <a href="/previous-versions/windows/apps/hh464906(v=win.10)">estensioni</a>di avvio, file e protocollo. Questa interfaccia viene in genere utilizzata in debugger e strumenti di progettazione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration"><strong>IApplicationAssociationRegistration</strong></a><br/></td>
<td>Espone metodi che eseguono query e impostano applicazioni predefinite per un <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationtype"><strong>tipo di associazione</strong></a>di file specifico e protocolli a un <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-associationlevel"><strong>livello di associazione</strong></a>specifico. <br/>
<blockquote>
[!Note]<br />
A partire da Windows 8, l'unica funzionalità supportata da questa interfaccia è <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault"><strong>QueryCurrentDefault</strong></a>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui"><strong>IApplicationAssociationRegistrationUI</strong></a><br/></td>
<td>Espone un metodo che avvia una finestra di dialogo di associazione avanzata tramite la quale l'utente può personalizzare le associazioni.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdesignmodesettings"><strong>IApplicationDesignModeSettings</strong></a><br/></td>
<td>Consente alle applicazioni dello strumento di sviluppo di eseguire lo spoofing dinamico di Stati di sistema e utente, ad esempio la risoluzione dello schermo nativo, il fattore di scala del dispositivo e lo stato di visualizzazione dell'applicazione, allo scopo di testare le applicazioni Windows Store in esecuzione in modalità progettazione per un'ampia gamma di fattori di forma senza la necessità di hardware effettivo. Consente inoltre di testare le modifiche nello stato normalmente controllato dall'utente per testare le app di Windows Store in diversi scenari.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdesignmodesettings2"><strong>IApplicationDesignModeSettings2</strong></a><br/></td>
<td>Consente alle applicazioni dello strumento di sviluppo di controllare dinamicamente gli Stati del sistema e degli utenti, ad esempio la risoluzione dello schermo nativo, il fattore di scala dei dispositivi e il layout di visualizzazione delle applicazioni, segnalati alle app di Windows Store allo scopo di testare le app di Windows Store in esecuzione in modalità progettazione per un'ampia gamma di fattori di forma senza la necessità di hardware effettivo. Consente inoltre di testare le modifiche nello stato normalmente controllato dall'utente per testare le app di Windows Store in diversi scenari.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations"><strong>IApplicationDestinations</strong></a><br/></td>
<td>Espone metodi che consentono a un'applicazione di rimuovere una o tutte le destinazioni dalle categorie <strong>recenti</strong> o <strong>frequenti</strong> in una Jump List.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists"><strong>IApplicationDocumentLists</strong></a><br/></td>
<td>Espone metodi che consentono a un'applicazione di recuperare il contenuto delle categorie <strong>recenti</strong> o <strong>frequenti</strong> in una Jump List.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-iapppublisher"><strong>IAppPublisher</strong></a><br/></td>
<td>Espone metodi per la pubblicazione di applicazioni tramite <strong>installazione</strong> applicazioni nel pannello di controllo. Si tratta dell'interfaccia principale implementata a questo scopo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iappvisibility"><strong>IAppVisibility</strong></a><br/></td>
<td>Fornisce la funzionalità per determinare se la visualizzazione Mostra le app di Windows Store.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iappvisibilityevents"><strong>IAppVisibilityEvents</strong></a><br/></td>
<td>Consente alle applicazioni di ricevere notifiche delle modifiche di stato in una visualizzazione e di modifiche nella visibilità della schermata iniziale.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandler"><strong>IAssocHandler</strong></a><br/></td>
<td>Espone i metodi per le operazioni con una finestra di dialogo di associazione file o un menu.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandlerinvoker"><strong>IAssocHandlerInvoker</strong></a><br/></td>
<td>Espone metodi che richiamano un gestore dell'applicazione associato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute"><strong>IAttachmentExecute</strong></a><br/></td>
<td>Espone metodi che funzionano con le applicazioni client per presentare un ambiente utente che fornisce il download e lo scambio sicuri di file tramite messaggi di posta elettronica e allegati di messaggistica.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete"><strong>IAutoComplete</strong></a><br/></td>
<td>Esposto dall'oggetto di completamento automatico (CLSID_AutoComplete). Questa interfaccia consente alle applicazioni di inizializzare, abilitare e disabilitare l'oggetto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete2"><strong>IAutoComplete2</strong></a><br/></td>
<td>Estende <a href="/windows/desktop/api/Shldisp/nn-shldisp-iautocomplete"><strong>IAutoComplete</strong></a>. Questa interfaccia consente ai client dell'oggetto di completamento automatico di recuperare e impostare diverse opzioni che controllano il funzionamento del completamento automatico.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iautocompletedropdown"><strong>IAutoCompleteDropDown</strong></a><br/></td>
<td>Espone metodi che consentono ai client di reimpostare o eseguire query sullo stato di visualizzazione dell'elenco a discesa completamento automatico, che contiene i possibili completamenti di una stringa immessa dall'utente in un controllo di modifica.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ibandhost"><strong>IBandHost</strong></a><br/></td>
<td>Espone metodi che creano ed eliminano le bande e specificano la loro disponibilità.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ibandsite"><strong>IBandSite</strong></a><br/></td>
<td>Espone metodi che controllano gli oggetti della banda.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ibrowserframeoptions"><strong>IBrowserFrameOptions</strong></a><br/></td>
<td>Consente a un browser o a un host di richiedere a <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a> il tipo di comportamento di visualizzazione supportato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icategorizer"><strong>ICategorizer</strong></a><br/></td>
<td>Espone i metodi utilizzati per ottenere informazioni sugli elenchi di identificatori di elemento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icategoryprovider"><strong>ICategoryProvider</strong></a><br/></td>
<td>Espone un elenco di classificatori registrati in un <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-icdburn"><strong>ICDBurn</strong></a><br/></td>
<td>Espone metodi che determinano se un sistema dispone di hardware per la scrittura su CD, la lettera di unità di un dispositivo di scrittura CD e avvia a livello di codice una sessione di scrittura CD. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager"><strong>IColumnManager</strong></a><br/></td>
<td>Espone metodi che consentono l'ispezione e la manipolazione delle colonne nella visualizzazione dettagli di Esplora risorse. A ogni colonna viene fatto riferimento da una struttura <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PropertyKey</strong></a> , che assegna un nome a una proprietà.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser"><strong>ICommDlgBrowser</strong></a><br/></td>
<td>Esposto dalle finestre di dialogo file comuni da usare quando ospitano un browser della shell. Se supportato, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser"><strong>ICommDlgBrowser</strong></a> espone metodi che consentono a una visualizzazione shell di gestire diversi casi che richiedono un comportamento diverso in una finestra di dialogo rispetto a una normale visualizzazione Shell. È possibile ottenere un puntatore a interfaccia <strong>ICommDlgBrowser</strong> chiamando <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>QueryInterface</strong></a> sull'oggetto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser"><strong>IShellBrowser</strong></a> . <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2"><strong>ICommDlgBrowser2</strong></a><br/></td>
<td>Estende le funzionalità di <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser"><strong>ICommDlgBrowser</strong></a>. Questa interfaccia viene esposta dalle finestre di dialogo dei file comuni quando ospitano un browser della shell. È possibile ottenere un puntatore a <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2"><strong>ICommDlgBrowser2</strong></a> chiamando <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>QueryInterface</strong></a> sull'oggetto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser"><strong>IShellBrowser</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-icommdlgbrowser3"><strong>ICommDlgBrowser3</strong></a><br/></td>
<td>Estende le funzionalità di <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2"><strong>ICommDlgBrowser2</strong></a>e usate dalle finestre di dialogo dei file comuni quando ospitano un browser della shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl/nn-shobjidl-icomputerinfochangenotify"><strong>IComputerInfoChangeNotify</strong></a><br/></td>
<td>Questa interfaccia potrebbe essere assente nelle versioni successive di Windows.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-iconnectablecredentialprovidercredential"><strong>IConnectableCredentialProviderCredential</strong></a><br/></td>
<td>Espone metodi per la connessione e la disconnessione di oggetti <a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-iconnectablecredentialprovidercredential"><strong>IConnectableCredentialProviderCredential</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-icontactmanagerinterop"><strong>IContactManagerInterop</strong></a><br/></td>
<td>Consente l'accesso ai metodi <a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-icontactmanagerinterop"><strong>ContactManager</strong></a> in un'app che gestisce più finestre.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu"><strong>IContextMenu</strong></a><br/></td>
<td>Espone metodi che creano o uniscono un menu di scelta rapida associato a un oggetto Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2"><strong>IContextMenu2</strong></a><br/></td>
<td>Espone metodi che creano o uniscono un menu di scelta rapida associato a un oggetto Shell. Estende <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu"><strong>IContextMenu</strong></a> aggiungendo un metodo che consente agli oggetti client di gestire i messaggi associati a voci di menu create dal proprietario.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3"><strong>IContextMenu3</strong></a><br/></td>
<td>Espone metodi che creano o uniscono un menu di scelta rapida associato a un oggetto Shell. Consente agli oggetti client di gestire i messaggi associati a voci di menu create dal proprietario ed estende <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2"><strong>IContextMenu2</strong></a> accettando un valore restituito dalla gestione dei messaggi.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb"><strong>IContextMenuCB</strong></a><br/></td>
<td>Espone un metodo che Abilita il callback di un menu di scelta rapida. Ad esempio, per aggiungere un'icona dello scudo a un <strong>MenuItem</strong> che richiede l'elevazione dei privilegi.<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/bb776063(v=vs.85)"><strong>IControlMarkup</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)"><strong>ICopyHook</strong></a><br/></td>
<td>Espone un metodo che crea un <em>gestore di hook di copia</em>. Un gestore di hook di copia è un'estensione della shell che determina se una cartella della shell o un oggetto stampante può essere spostato, copiato, rinominato o eliminato. La shell chiama il metodo <a href="/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)"><strong>ICopyHook:: CopyCallback</strong></a> prima di eseguire una di queste operazioni.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-icreateobject"><strong>ICreateObject</strong></a><br/></td>
<td>Espone un metodo che crea un oggetto di una classe specificata.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreatingprocess"><strong>ICreatingProcess</strong></a><br/></td>
<td>Usato da <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu"><strong>IContextMenu</strong></a> per consentire al chiamante di modificare alcuni parametri del processo da creare.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreateprocessinputs"><strong>ICreateProcessInputs</strong></a><br/></td>
<td>Utilizzato dall'interfaccia <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icreatingprocess"><strong>ICreatingProcess</strong></a> per modificare alcuni parametri del processo che viene creato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovider"><strong>ICredentialProvider</strong></a><br/></td>
<td>Espone i metodi utilizzati per l'installazione e la manipolazione di un provider di credenziali. Tutti i provider di credenziali devono implementare questa interfaccia.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovidercredential"><strong>ICredentialProviderCredential</strong></a><br/></td>
<td>Espone metodi che consentono la gestione di una credenziale.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovidercredential2"><strong>ICredentialProviderCredential2</strong></a><br/></td>
<td>Estende l'interfaccia <a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovidercredential"><strong>ICredentialProviderCredential</strong></a> aggiungendo un metodo che recupera l'ID di sicurezza (SID) di un utente. La credenziale è associata a tale utente e può essere raggruppata sotto il riquadro dell'utente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents"><strong>ICredentialProviderCredentialEvents</strong></a><br/></td>
<td>Fornisce un meccanismo di callback asincrono utilizzato da una credenziale per notificare gli eventi di modifica dello stato o del testo nell'interfaccia utente di accesso o nelle credenziali.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovidercredentialevents2"><strong>ICredentialProviderCredentialEvents2</strong></a><br/></td>
<td>Estende l'interfaccia <a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialprovidercredentialevents"><strong>ICredentialProviderCredentialEvents</strong></a> aggiungendo metodi che consentono l'aggiornamento in batch dei campi nell'interfaccia utente di theLogon o nell'interfaccia utente delle credenziali.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovidercredentialwithfieldoptions"><strong>ICredentialProviderCredentialWithFieldOptions</strong></a><br/></td>
<td>Fornisce un metodo che consente al Framework del provider di credenziali di determinare se è stata apportata una personalizzazione all'opzione di un campo in un'interfaccia utente di accesso o credenziali.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialproviderevents"><strong>ICredentialProviderEvents</strong></a><br/></td>
<td>Fornisce un meccanismo di callback asincrono utilizzato da un provider di credenziali per notificare le modifiche nell'elenco di credenziali o nei rispettivi campi.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-icredentialproviderfilter"><strong>ICredentialProviderFilter</strong></a><br/></td>
<td>Utilizzato per filtrare in modo dinamico i provider di credenziali in base alle informazioni disponibili in fase di esecuzione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovidersetuserarray"><strong>ICredentialProviderSetUserArray</strong></a><br/></td>
<td>Fornisce un metodo che consente a un provider di credenziali di ricevere il set di utenti che verrà visualizzato nell'interfaccia utente di accesso o credenziali.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovideruser"><strong>ICredentialProviderUser</strong></a><br/></td>
<td>Fornisce i metodi utilizzati per recuperare determinate proprietà di un singolo utente incluso in un'interfaccia utente di accesso o credenziali.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/CredentialProvider/nn-credentialprovider-icredentialprovideruserarray"><strong>ICredentialProviderUserArray</strong></a><br/></td>
<td>Rappresenta il set di utenti che verrà visualizzato nell'interfaccia utente di accesso o credenziali. Queste informazioni consentono al provider di credenziali di enumerare il set per recuperare le informazioni sulle proprietà relative a ogni utente per popolare i campi o filtrare il set.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icurrentitem"><strong>ICurrentItem</strong></a><br/></td>
<td>Ottenuto chiamando <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> per un elemento. Se l'elemento rappresenta uno snapshot di un elemento in un momento precedente, questa interfaccia otterrà la versione corrente dell'elemento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj/nn-shlobj-icurrentworkingdirectory"><strong>ICurrentWorkingDirectory</strong></a><br/></td>
<td>Espone metodi che consentono a un client di recuperare o impostare la directory di lavoro corrente di un oggetto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist"><strong>ICustomDestinationList</strong></a><br/></td>
<td>Espone metodi che consentono a un'applicazione di fornire una Jump List personalizzata, incluse le destinazioni e le attività, da visualizzare nella barra delle applicazioni.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shldisp/nn-shldisp-idataobjectasynccapability"><strong>IDataObjectAsyncCapability</strong></a><br/></td>
<td>Abilita le interfacce che in genere sono sincrone per funzionare in modo asincrono. <br/>
<blockquote>
[!Note]<br />
Questa interfaccia è la versione corrente, rinominata di <a href="/previous-versions//bb776309(v=vs.85)"><strong>IAsyncOperation</strong></a>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idataobjectprovider"><strong>IDataObjectProvider</strong></a><br/></td>
<td>Fornisce metodi che consentono di impostare o recuperare l' <a href="/windows/desktop/api/objidl/nn-objidl-idataobject"><strong>interfaccia IDataObject</strong></a>di un oggetto <a href="/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage?view=winrt-19041">DataPackage</a> , utilizzata dal DataPackage per supportare l'interoperabilità. L'oggetto DataPackage viene usato da un'app per fornire i dati a un'altra app.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idatatransfermanagerinterop"><strong>IDataTransferManagerInterop</strong></a><br/></td>
<td>Consente l'accesso ai metodi <a href="/uwp/api/Windows.ApplicationModel.DataTransfer.DataTransferManager"><strong>DataTransferManager</strong></a> in un'app di Windows Store che gestisce più finestre.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idefaultextracticoninit"><strong>IDefaultExtractIconInit</strong></a><br/></td>
<td>Espone i metodi per impostare le icone predefinite associate a un oggetto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idefaultfoldermenuinitialize"><strong>IDefaultFolderMenuInitialize</strong></a><br/></td>
<td>Fornisce i metodi utilizzati per ottenere e impostare le informazioni sul menu di scelta rapida. Queste informazioni sono identiche a quelle fornite a <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu"><strong>SHCreateDefaultContextMenu</strong></a> tramite la struttura <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu"><strong>DEFCONTEXTMENU</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-idelayedpropertystorefactory"><strong>IDelayedPropertyStoreFactory</strong></a><br/></td>
<td>Espone un metodo per creare un oggetto <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a> specificato nei casi in cui l'accesso alle proprietà è potenzialmente lento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idelegatefolder"><strong>IDelegateFolder</strong></a><br/></td>
<td>Espone un metodo tramite il quale a una cartella delegata viene assegnata l'interfaccia <a href="/windows/desktop/api/objidl/nn-objidl-imalloc"><strong>IMalloc</strong></a> necessaria per allocare e liberare gli ID elemento.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idelegateitem"><strong>IDelegateItem</strong></a><br/></td>
<td>Utilizzato per ottenere la rappresentazione immediatamente sottostante del percorso di un elemento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-idesktopgadget"><strong>IDesktopGadget</strong></a><br/></td>
<td>Espone un metodo che consente l'aggiunta a livello di codice di un gadget installato sul desktop dell'utente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idesktopwallpaper"><strong>IDesktopWallpaper</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idestinationstreamfactory"><strong>IDestinationStreamFactory</strong></a><br/></td>
<td>Espone un metodo per copiare manualmente un flusso o un file prima di applicare le modifiche alle proprietà.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idisplayitem"><strong>IDisplayItem</strong></a><br/></td>
<td>Espone metodi che trovano una versione dell'elemento corrente da usare per ottenere le proprietà di visualizzazione, ad esempio il nome dell'elemento, che verrà visualizzato nell'interfaccia utente. Utilizzato dalle finestre di dialogo del motore di copia per fornire all'interfaccia utente un elemento appropriato da visualizzare. Se non è possibile trovare altre versioni, viene usato l'elemento corrente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow"><strong>IDockingWindow</strong></a><br/></td>
<td>Espone metodi che inviano notifiche all'oggetto finestra di ancoraggio delle modifiche, incluse la visualizzazione, l'occultamento e la rimozione imminente. Questa interfaccia viene implementata da oggetti finestra che possono essere ancorati all'interno dello spazio del bordo di una finestra di Esplora risorse.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj/nn-shlobj-idockingwindowframe"><strong>IDockingWindowFrame</strong></a><br/></td>
<td>Espone metodi che supportano l'aggiunta di oggetti <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow"><strong>IDockingWindow</strong></a> a un frame. Implementato dal browser.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-idockingwindowsite"><strong>IDockingWindowSite</strong></a><br/></td>
<td>Espone metodi che gestiscono lo spazio del bordo per uno o più oggetti <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow"><strong>IDockingWindow</strong></a> . Questa interfaccia viene implementata dal browser ed è simile all'interfaccia <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleinplaceuiwindow"><strong>oleinplaceuiwindow</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper"><strong>IDragSourceHelper</strong></a><br/></td>
<td>Esposto dalla Shell per consentire a un'applicazione di specificare l'immagine che verrà visualizzata durante un'operazione di trascinamento e rilascio della shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-idragsourcehelper2"><strong>IDragSourceHelper2</strong></a><br/></td>
<td>Espone un metodo che aggiunge funzionalità a <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper"><strong>IDragSourceHelper</strong></a>. Questo metodo imposta le caratteristiche di un'operazione di trascinamento della selezione su un oggetto <strong>IDragSourceHelper</strong> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idroptargethelper"><strong>IDropTargetHelper</strong></a><br/></td>
<td>Espone metodi che consentono a drop targets di visualizzare un'immagine di trascinamento mentre l'immagine si trova sulla finestra di destinazione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-idynamichwhandler"><strong>IDynamicHWHandler</strong></a><br/></td>
<td>Chiamato da AutoPlay. Espone metodi che ottengono informazioni dinamiche relative a un gestore registrato prima di visualizzarlo all'utente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumassochandlers"><strong>IEnumAssocHandlers</strong></a><br/></td>
<td>Espone un metodo che consente l'enumerazione di una raccolta di gestori associati a specifiche estensioni di file.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ienumerableview"><strong>IEnumerableView</strong></a><br/></td>
<td>Espone metodi che enumerano il contenuto di una visualizzazione e ricevono una notifica dal callback al completamento dell'enumerazione. Questa interfaccia consente ai client di una visualizzazione di provare a condividere l'elenco di contenuti della cartella della visualizzazione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumexplorercommand"><strong>IEnumExplorerCommand</strong></a><br/></td>
<td>Fornito da un <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a>. Questa interfaccia contiene l'enumerazione dei comandi da inserire nella barra dei comandi.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumextrasearch"><strong>IEnumExtraSearch</strong></a><br/></td>
<td>Enumeratore OLE standard utilizzato da un client per determinare gli oggetti di ricerca disponibili per una cartella.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumfullidlist"><strong>IEnumFullIDList</strong></a><br/></td>
<td>Espone un set standard di metodi che enumerano i puntatori agli elenchi di identificatori di elemento (PIDL) degli elementi in una cartella della shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist"><strong>IEnumIDList</strong></a><br/></td>
<td>Espone un set standard di metodi usati per enumerare l'PIDL degli elementi in una cartella della shell. Quando viene chiamato il metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects"><strong>IShellFolder:: EnumObjects</strong></a> di una cartella, viene creato un oggetto di enumerazione e viene passato un puntatore all'interfaccia <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist"><strong>IEnumIDList</strong></a> dell'oggetto all'applicazione chiamante.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumobjects"><strong>IEnumObjects</strong></a><br/></td>
<td>Espone metodi per enumerare oggetti sconosciuti.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ienumpublishedapps"><strong>IEnumPublishedApps</strong></a><br/></td>
<td>Espone metodi che enumerano le applicazioni pubblicate per aggiungere/rimuovere programmi nel pannello di controllo. L'oggetto che espone questa interfaccia viene richiesto tramite <a href="/windows/desktop/api/Shappmgr/nf-shappmgr-iapppublisher-enumapps"><strong>IAppPublisher:: EnumApps</strong></a>. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ienumreadycallback"><strong>IEnumReadyCallback</strong></a><br/></td>
<td>Espone metodi che consentono alla visualizzazione di notificare all'implementatore quando l'enumerazione è stata completata. La vista chiama questo metodo per indicare all'implementatore che l'enumerazione può essere recuperata tramite <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-ienumerableview-createenumidlistfromcontents"><strong>IEnumerableView:: CreateEnumIDListFromContents</strong></a>. Il callback consente all'implementatore di condividere l'enumerazione views.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumresources"><strong>IEnumResources</strong></a><br/></td>
<td>Espone i metodi di enumerazione delle risorse.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumshellitems"><strong>IEnumShellItems</strong></a><br/></td>
<td>Espone l'enumerazione delle interfacce <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> . Questa interfaccia viene in genere ottenuta chiamando il metodo <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumshellitems"><strong>IEnumShellItems</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrconflict"><strong>IEnumSyncMgrConflict</strong></a><br/></td>
<td>Espone i metodi di enumerazione dei conflitti.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrevents"><strong>IEnumSyncMgrEvents</strong></a><br/></td>
<td>Espone i metodi di enumerazione degli eventi di sincronizzazione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-ienumsyncmgrsyncitems"><strong>IEnumSyncMgrSyncItems</strong></a><br/></td>
<td>Espone metodi che enumerano gli oggetti dell'elemento di sincronizzazione gestiti dal gestore.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a><br/></td>
<td>Espone metodi che impostano uno stato o un parametro specifico correlato al verbo del comando, oltre a un metodo per richiamare tale verbo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommandapplicationhostenvironment"><strong>IExecuteCommandApplicationHostEnvironment</strong></a><br/></td>
<td>Fornisce un singolo metodo che consente a un'applicazione di determinare se l'host è in modalità desktop o immersiva.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommandhost"><strong>IExecuteCommandHost</strong></a><br/></td>
<td>Fornisce un metodo che consente a un gestore di verbi della shell basata su <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a>di eseguire una query sulla modalità dell'interfaccia utente del componente host da cui è stata richiamata l'applicazione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser"><strong>IExplorerBrowser</strong></a><br/></td>
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser"><strong>IExplorerBrowser</strong></a> è un oggetto browser che può essere esplorato o che può ospitare una visualizzazione di un oggetto dati. Come oggetto browser completo, supporta anche un log di viaggio automatico.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowserevents"><strong>IExplorerBrowserEvents</strong></a><br/></td>
<td>Espone metodi per la notifica degli eventi di esplorazione e visualizzazione del browser di Explorer.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a><br/></td>
<td>Espone metodi che ottengono l'aspetto del comando, enumerano i sottocomandi o richiamano il comando.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a><br/></td>
<td>Espone i metodi per creare comandi e enumeratori del comando di Explorer.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate"><strong>IExplorerCommandState</strong></a><br/></td>
<td>Espone un singolo metodo che consente il recupero dello stato del comando.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerpanevisibility"><strong>IExplorerPaneVisibility</strong></a><br/></td>
<td>Utilizzato in Esplora risorse da un'implementazione <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> per fornire suggerimenti sulla visualizzazione dei riquadri visibili. Inoltre, un host <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerbrowser"><strong>IExplorerBrowser</strong></a> può usare questa interfaccia per fornire informazioni sulla visibilità dei riquadri. L'host deve implementare <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a> con <strong>SID_ExplorerPaneVisibility</strong> come ID del servizio. L'host deve trovarsi nella catena di siti. <br/> L'implementazione di <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerpanevisibility"><strong>IExplorerPaneVisibility</strong></a> viene recuperata dalla cartella della shell. La cartella della shell, a sua volta, viene recuperata dalla visualizzazione. Un'estensione dello spazio dei nomi può scegliere di fornire una visualizzazione personalizzata (<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a>) anziché usare l'oggetto visualizzazione cartella di sistema (DefView). In tal caso, l'implementazione di <strong>IShellView</strong> deve includere un'implementazione di <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-getfolder"><strong>IFolderView:: GetFolder</strong></a> per restituire l'oggetto <strong>IExplorerPaneVisibility</strong> .<br/> Un'estensione dello spazio dei nomi può fornire una visualizzazione personalizzata mediante l'implementazione di <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a> , invece di usare l'oggetto visualizzazione cartella di sistema (DefView). In tal caso, l'implementazione di <strong>IShellView</strong> deve includere un'implementazione di <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview-getfolder"><strong>IFolderView:: GetFolder</strong></a> per usare <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerpanevisibility"><strong>IExplorerPaneVisibility</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iextracticona"><strong>IExtractIcon</strong></a><br/></td>
<td>Espone metodi che consentono a un client di recuperare l'icona associata a uno degli oggetti in una cartella.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage"><strong>IExtractImage</strong></a><br/></td>
<td>Espone metodi che richiedono un'immagine di anteprima da una cartella della shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage2"><strong>IExtractImage2</strong></a><br/></td>
<td>Estende le funzionalità di <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage"><strong>IExtractImage</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog"><strong>IFileDialog</strong></a><br/></td>
<td>Espone metodi che inizializzano, mostrano e ottengono risultati dalla finestra di dialogo file comune.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialog2"><strong>IFileDialog2</strong></a><br/></td>
<td>Estende l'interfaccia <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog"><strong>IFileDialog</strong></a> fornendo metodi che consentono al chiamante di assegnare un nome a una posizione specifica e limitata che può essere visualizzata nella finestra di dialogo file comune, nonché di specificare testo alternativo da visualizzare come etichetta sul pulsante <strong>Annulla</strong> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents"><strong>IFileDialogControlEvents</strong></a><br/></td>
<td>Espone metodi che consentono a un'applicazione di ricevere notifiche sugli eventi correlati a controlli che l'applicazione ha aggiunto a una finestra di dialogo file comune.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize"><strong>IFileDialogCustomize</strong></a><br/></td>
<td>Espone metodi che consentono a un'applicazione di aggiungere controlli a una finestra di dialogo file comune.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents"><strong>IFileDialogEvents</strong></a><br/></td>
<td>Espone metodi che consentono la notifica di eventi in una finestra di dialogo file comune.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileisinuse"><strong>IFileIsInUse</strong></a><br/></td>
<td>Espone metodi che possono essere chiamati per ottenere informazioni o chiudere un file utilizzato da un'altra applicazione. Quando un'applicazione tenta di accedere a un file e trova il file già in uso, può utilizzare i metodi di questa interfaccia per raccogliere informazioni da presentare all'utente in una finestra di dialogo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog"><strong>IFileOpenDialog</strong></a><br/></td>
<td>Estende l'interfaccia <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog"><strong>IFileDialog</strong></a> mediante l'aggiunta di metodi specifici per la finestra di dialogo Apri.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>IFileOperation</strong></a><br/></td>
<td>Espone metodi per la copia, lo spostamento, la ridenominazione, la creazione e l'eliminazione di elementi della shell, nonché metodi per fornire finestre di dialogo di stato e di errore. Questa interfaccia sostituisce la funzione <a href="/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa"><strong>SHFileOperation</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink"><strong>IFileOperationProgressSink</strong></a><br/></td>
<td>Espone metodi che forniscono un sistema di notifica avanzato utilizzato dai chiamanti di <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation"><strong>IFileOperation</strong></a> per monitorare i dettagli delle operazioni eseguite tramite tale interfaccia.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog"><strong>IFileSaveDialog</strong></a><br/></td>
<td>Estende l'interfaccia <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog"><strong>IFileDialog</strong></a> mediante l'aggiunta di metodi specifici per la finestra di dialogo Save, che includono quelli che forniscono supporto per la raccolta di metadati da rendere permanente con il file.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesyncmergehandler"><strong>IFileSyncMergeHandler</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata"><strong>IFileSystemBindData</strong></a><br/></td>
<td>Espone metodi che archiviano informazioni file system per l'ottimizzazione delle chiamate a <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata2"><strong>IFileSystemBindData2</strong></a><br/></td>
<td>Estende <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesystembinddata"><strong>IFileSystemBindData</strong></a>, in cui vengono archiviate file System informazioni per l'ottimizzazione delle chiamate a <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname"><strong>IShellFolder::P arsedisplayname</strong></a>. Questa interfaccia consente di aggiungere il set di funzionalità o ottenere l'ID del file o l'identificatore di classe di giunzione (CLSID).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/shell/schema-library-iconreference"><strong>IFileViewer</strong></a><br/></td>
<td>Espone metodi che designano un'interfaccia che consente a un visualizzatore di file registrato di ricevere una notifica quando deve visualizzare o stampare un file.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj/nn-shlobj-ifileviewersite"><strong>IFileViewerSite</strong></a><br/></td>
<td>Espone metodi che definiscono un'interfaccia che consente a un visualizzatore di file di recuperare l'handle per la finestra Aggiunta corrente o di impostare una nuova finestra bloccata. La finestra bloccata è la finestra in cui viene visualizzato un file nel Visualizzatore file corrente. Quando l'utente seleziona un nuovo file da visualizzare, la shell indirizza il Visualizzatore file per visualizzare il nuovo file nella finestra bloccata anziché creare una nuova finestra.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderfilter"><strong>IFolderFilter</strong></a><br/></td>
<td>Esposto da un client per specificare come filtrare l'enumerazione di una cartella della shell da un'applicazione server.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderfiltersite"><strong>IFolderFilterSite</strong></a><br/></td>
<td>Esportato da un host per consentire ai client di specificare come filtrare un'enumerazione di cartelle della shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview"><strong>IFolderView</strong></a><br/></td>
<td>Espone metodi che recuperano informazioni sulle opzioni di visualizzazione di una cartella, selezionano gli elementi specificati in tale cartella e impostano la modalità di visualizzazione della cartella.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview2"><strong>IFolderView2</strong></a><br/></td>
<td>Espone metodi che recuperano informazioni sulle opzioni di visualizzazione di una cartella, selezionano gli elementi specificati in tale cartella e impostano la modalità di visualizzazione della cartella.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifolderviewhost"><strong>IFolderViewHost</strong></a><br/></td>
<td>Espone un metodo che ospita un oggetto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview"><strong>IFolderView</strong></a> in una finestra.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ifolderviewoptions"><strong>IFolderViewOptions</strong></a><br/></td>
<td>Espone metodi che consentono di controllare le opzioni di visualizzazione cartelle specifiche per le visualizzazioni di Windows 7 e successive.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderviewsettings"><strong>IFolderViewSettings</strong></a><br/></td>
<td>Espone i metodi per ottenere le impostazioni della visualizzazione cartelle.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iframeworkinputpane"><strong>IFrameworkInputPane</strong></a><br/></td>
<td>Fornisce metodi che consentono alle app di essere informati delle modifiche di stato e della posizione del riquadro di input.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iframeworkinputpanehandler"><strong>IFrameworkInputPaneHandler</strong></a><br/></td>
<td>Consente a un'app di ricevere una notifica quando il riquadro di input (tastiera o pannello grafia) viene visualizzato o nascosto. Questo consente alla finestra dell'app di modificare la visualizzazione in modo che nessuna area di input (ad esempio una casella di testo) venga nascosta dal riquadro Input.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihandleractivationhost"><strong>IHandlerActivationHost</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihandlerinfo"><strong>IHandlerInfo</strong></a><br/></td>
<td>Fornisce metodi che forniscono informazioni sul gestore ai metodi dell'interfaccia <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihandleractivationhost"><strong>IHandlerActivationHost</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihomegroup"><strong>IHomeGroup</strong></a><br/></td>
<td>Espone metodi che determinano lo stato di appartenenza di un gruppo di computer e visualizzano la condivisione guidata.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler"><strong>IHWEventHandler</strong></a><br/></td>
<td>Chiamato da AutoPlay per implementare la gestione dei tipi di supporti registrati.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler2"><strong>IHWEventHandler2</strong></a><br/></td>
<td>Estende l'interfaccia <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler"><strong>IHWEventHandler</strong></a> per indirizzare l'elevazione del controllo dell'account utente per i gestori di dispositivi.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iidentityname"><strong>IIdentityName</strong></a><br/></td>
<td>Espone i metodi per confrontare due elementi per verificare se sono uguali.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iimagerecompress"><strong>IImageRecompress</strong></a><br/></td>
<td>Espone un metodo che ricomprime le immagini.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>IInitializeCommand</strong></a><br/></td>
<td>Espone un singolo metodo utilizzato per inizializzare gli oggetti che implementano <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate"><strong>IExplorerCommandState</strong></a>, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a> o <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a> con il nome del comando specificato dall'applicazione e le relative proprietà registrate.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shobjidl/nn-shobjidl-iinitializenetworkfolder"><strong>IInitializeNetworkFolder</strong></a><br/></td>
<td>Espone un metodo che Inizializza l'origine dati di rete CLSID_NetworkPlaces come specificato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithbindctx"><strong>IInitializeWithBindCtx</strong></a><br/></td>
<td>Espone un metodo che Inizializza un gestore, ad esempio un gestore di proprietà, un gestore di anteprime o un gestore di anteprime, con un contesto di associazione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile"><strong>IInitializeWithFile</strong></a><br/></td>
<td>Espone un metodo per inizializzare un gestore, ad esempio un gestore di proprietà, un gestore di anteprime o un gestore di anteprime, con un percorso di file.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem"><strong>IInitializeWithItem</strong></a><br/></td>
<td>Espone un metodo utilizzato per inizializzare un gestore, ad esempio un gestore di proprietà, un gestore di anteprime o un gestore di anteprime, con un <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithpropertystore"><strong>IInitializeWithPropertyStore</strong></a><br/></td>
<td>Espone un metodo che Inizializza un gestore, ad esempio un gestore di proprietà, un gestore di anteprime o un gestore di anteprime, con un archivio delle proprietà.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream"><strong>IInitializeWithStream</strong></a><br/></td>
<td>Espone un metodo che Inizializza un gestore, ad esempio un gestore di proprietà, un gestore di anteprime o un gestore di anteprime, con un flusso.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithwindow"><strong>IInitializeWithWindow</strong></a><br/></td>
<td>Espone un metodo tramite il quale un client può fornire una finestra proprietaria a un oggetto Windows Runtime utilizzato in un'applicazione desktop.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobject"><strong>IInputObject</strong></a><br/></td>
<td>Espone metodi che modificano l'attivazione dell'interfaccia utente e gli acceleratori di processo per un oggetto di input utente contenuto nella shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobject2"><strong>IInputObject2</strong></a><br/></td>
<td>Espone un metodo che estende <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobject"><strong>IInputObject</strong></a> gestendo gli acceleratori globali.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite"><strong>IInputObjectSite</strong></a><br/></td>
<td>Espone un metodo utilizzato per comunicare le modifiche dello stato attivo per un oggetto di input utente contenuto nella shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelconfiguration"><strong>IInputPanelConfiguration</strong></a><br/></td>
<td>Fornisce funzionalità per le app desktop per acconsentire esplicitamente al meccanismo di rilevamento dello stato attivo usato nelle app di Windows Store.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/inputpanelconfiguration/nn-inputpanelconfiguration-iinputpanelinvocationconfiguration"><strong>IInputPanelInvocationConfiguration</strong></a><br/></td>
<td>Consente alle app di Windows Store di rifiutare esplicitamente il comportamento di chiamata automatica.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iiocancelinformation"><strong>IIOCancelInformation</strong></a><br/></td>
<td>Espone metodi per l'invio di un messaggio di finestra Annulla al thread di processo dalla finestra di dialogo di stato. <br/> Questa interfaccia consente alla finestra di dialogo di avanzamento di inviare un messaggio di thread attraverso <a href="/windows/desktop/api/winuser/nf-winuser-postthreadmessagea"><strong>PostThreadMessage</strong></a> al thread di lavoro per annullare le operazioni. Il thread di lavoro deve controllare periodicamente la coda di messaggi tramite <a href="/windows/desktop/api/winuser/nf-winuser-getmessage"><strong>GetMessage</strong></a>, <a href="/windows/desktop/api/winuser/nf-winuser-peekmessagea"><strong>PeekMessage</strong></a> o <a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex"><strong>MsgWaitForMultipleObjectsEx</strong></a>.<br/> Il metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iiocancelinformation-setcancelinformation"><strong>IIOCancelInformation:: SetCancelInformation</strong></a> indica alla finestra di dialogo di stato l'ID del thread e il messaggio da <a href="/windows/desktop/api/winuser/nf-winuser-postthreadmessagea"><strong>PostThreadMessage</strong></a> quando l'utente fa clic su <strong>Annulla</strong>. Un ID di thread &quot; zero &quot; Disabilita l'operazione di invio per il messaggio di annullamento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iitemnamelimits"><strong>IItemNameLimits</strong></a><br/></td>
<td>Recupera un elenco di caratteri validi e non validi o la lunghezza massima di un nome nello spazio dei nomi. Usare questa interfaccia per l'analisi e la conversione della convalida.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder"><strong>IKnownFolder</strong></a><br/></td>
<td>Espone metodi che consentono a un'applicazione di recuperare informazioni sulla categoria, il tipo, il GUID, il valore PIDL, le funzionalità di reindirizzamento e la definizione di una cartella nota. Fornisce un metodo per il il recupero dell'oggetto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> di una cartella nota. Fornisce inoltre i metodi per ottenere o impostare il percorso della cartella nota.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager"><strong>IKnownFolderManager</strong></a><br/></td>
<td>Espone metodi che creano, enumerano o gestiscono cartelle note esistenti.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchsourceappusermodelid"><strong>ILaunchSourceAppUserModelId</strong></a><br/></td>
<td>Fornisce un metodo per il recupero di un <a href="appids.md">AppUserModelID</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchsourceviewsizepreference"><strong>ILaunchSourceViewSizePreference</strong></a><br/></td>
<td>Fornisce metodi per il recupero di informazioni sull'applicazione di origine.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchtargetmonitor"><strong>ILaunchTargetMonitor</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchtargetviewsizepreference"><strong>ILaunchTargetViewSizePreference</strong></a><br/></td>
<td>Fornisce un metodo per recuperare le dimensioni di visualizzazione preferite per una nuova finestra dell'applicazione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/shell/shell-extensibility-bumper"><strong>IMarkupCallback</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imenupopup"><strong>IMenuPopup</strong></a><br/></td>
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imenupopup"><strong>IMenuPopup</strong></a> può essere modificato o non disponibile.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow"><strong>IModalWindow</strong></a><br/></td>
<td>Espone un metodo che rappresenta una finestra modale. Questa interfaccia viene utilizzata nella procedura guidata Windows XP Passport.<br/></td>
</tr>
<tr class="odd">
<td><a href="imultimonitordockingsite.md"><strong>IMultiMonitorDockingSite</strong></a><br/></td>
<td>Implementato dal browser. Espone metodi che gestiscono il monitoraggio che contiene la barra delle applicazioni di Windows in un sistema a più monitor. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-inamedpropertybag"><strong>INamedPropertyBag</strong></a><br/></td>
<td>Espone metodi che forniscono un oggetto con un contenitore di proprietà specificato in cui l'oggetto può salvare le proprietà.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-inamedpropertystore"><strong>INamedPropertyStore</strong></a><br/></td>
<td>Espone metodi che ottengono e impostano proprietà denominate.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreeaccessible"><strong>INameSpaceTreeAccessible</strong></a><br/></td>
<td>Espone metodi che eseguono azioni di accessibilità su un elemento della shell da un controllo struttura ad albero dello spazio dei nomi.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol"><strong>INameSpaceTreeControl</strong></a><br/></td>
<td>Espone i metodi utilizzati per visualizzare e modificare i nodi in una struttura ad albero di elementi della shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrol2"><strong>INameSpaceTreeControl2</strong></a><br/></td>
<td>Estende l'interfaccia <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol"><strong>INameSpaceTreeControl</strong></a> fornendo metodi che ottengono e impostano gli stili di visualizzazione dei controlli TreeView da usare con gli elementi dello spazio dei nomi della shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrolcustomdraw"><strong>INameSpaceTreeControlCustomDraw</strong></a><br/></td>
<td>Espone metodi che consentono all'utente di creare un controllo struttura ad albero dello spazio dei nomi personalizzato e i relativi elementi.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontroldrophandler"><strong>INameSpaceTreeControlDropHandler</strong></a><br/></td>
<td>Espone i metodi del gestore per il trascinamento della selezione. Utilizzato dal controllo struttura ad albero dello spazio dei nomi per notificare al client qualsiasi operazione di trascinamento della selezione che si verifica all'interno del controllo. Consente a un client di intercettare un'operazione DROP ed eseguire un'azione personalizzata oppure di restituire l'effetto di rilascio desiderato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-inamespacetreecontrolevents"><strong>INameSpaceTreeControlEvents</strong></a><br/></td>
<td>Espone metodi per la gestione degli eventi <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrol"><strong>INameSpaceTreeControl</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacetreecontrolfoldercapabilities"><strong>INameSpaceTreeControlFolderCapabilities</strong></a><br/></td>
<td>Espone un singolo metodo che recupera lo stato del supporto del filtro <a href="/windows/desktop/properties/props-system-ispinnedtonamespacetree">System. IsPinnedToNameSpaceTree</a> di una cartella.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalk"><strong>INamespaceWalk</strong></a><br/></td>
<td>Espone metodi che procedono a uno spazio dei nomi da un nodo radice specificato. Viene specificata la profondità del percorso e viene restituita una matrice facoltativa contenente gli ID di tutti i nodi.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb"><strong>INamespaceWalkCB</strong></a><br/></td>
<td>Interfaccia di callback che espone i metodi utilizzati con <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalk"><strong>INamespaceWalk</strong></a>. Dopo aver eseguito una procedura con <strong>INamespaceWalk</strong>, un oggetto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> che rappresenta i nodi di cui è stato eseguito il walking viene passato ai metodi <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb"><strong>INamespaceWalkCB</strong></a> . Ciò che questi metodi eseguono con le informazioni dipendono dall'oggetto che li sta implementando.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb2"><strong>INamespaceWalkCB2</strong></a><br/></td>
<td>Estende <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inamespacewalkcb"><strong>INamespaceWalkCB</strong></a> con un metodo necessario per completare un percorso dello spazio dei nomi. Questo metodo rimuove i dati raccolti durante il percorso. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inewmenuclient"><strong>INewMenuClient</strong></a><br/></td>
<td>Espone metodi che consentono la manipolazione di elementi in un menu di Windows 7.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj/nn-shlobj-inewshortcuthooka"><strong>INewShortcutHook</strong></a><br/></td>
<td>Espone i metodi per creare un nuovo collegamento a Internet.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-inewwindowmanager"><strong>INewWindowManager</strong></a><br/></td>
<td>Espone un metodo che determina se una finestra avviata da un'altra finestra deve essere visualizzata o bloccata, consentendo il controllo delle finestre popup.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/reconcil/nn-reconcil-inotifyreplica"><strong>INotifyReplica</strong></a><br/></td>
<td>Espone un metodo che fornisce un creatore di un oggetto con i mezzi per notificare all'oggetto che può essere soggetto alla successiva riconciliazione. Il riconciliatore della valigetta è responsabile dell'implementazione di questa interfaccia.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Objectarray/nn-objectarray-iobjectarray"><strong>IObjectArray</strong></a><br/></td>
<td>Espone metodi che consentono ai client di accedere agli elementi di una raccolta di oggetti che supportano <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/objectarray/nn-objectarray-iobjectcollection"><strong>IObjectCollection</strong></a><br/></td>
<td>Estende l'interfaccia <a href="/windows/desktop/api/Objectarray/nn-objectarray-iobjectarray"><strong>IObjectArray</strong></a> fornendo metodi che consentono ai client di aggiungere e rimuovere oggetti che supportano <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> in una raccolta.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectprovider"><strong>IObjectProvider</strong></a><br/></td>
<td>Espone un metodo per individuare gli oggetti denominati con un <strong>GUID</strong> da un altro oggetto. A differenza di <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a> , questa interfaccia non delegherà la funzionalità ad altri oggetti.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithappusermodelid"><strong>IObjectWithAppUserModelID</strong></a><br/></td>
<td>Espone metodi che consentono ai responsabili dell'implementazione di un oggetto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandler"><strong>IAssocHandler</strong></a> personalizzato di fornire l'accesso all'ID del modello utente dell'applicazione esplicita (AppUserModelID). Queste informazioni vengono usate per determinare se un determinato tipo di file può essere aggiunto alla Jump List di un'applicazione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithbackreferences"><strong>IObjectWithBackReferences</strong></a><br/></td>
<td>Fornisce un metodo per l'interazione con i riferimenti indietro contenuti in un oggetto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithcancelevent"><strong>IObjectWithCancelEvent</strong></a><br/></td>
<td>Fornisce un chiamante con un evento che verrà segnalato dall'oggetto chiamato per indicare l'annullamento di un'attività.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithfolderenummode"><strong>IObjectWithFolderEnumMode</strong></a><br/></td>
<td>Espone metodi che ottengono e impostano le modalità di enumerazione di un elemento analizzato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithprogid"><strong>IObjectWithProgID</strong></a><br/></td>
<td>Espone metodi che consentono di accedere al ProgID associato a un oggetto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-iobjectwithpropertykey"><strong>IObjectWithPropertyKey</strong></a><br/></td>
<td>Espone metodi per ottenere e impostare la chiave della proprietà.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>IObjectWithSelection</strong></a><br/></td>
<td>Espone metodi che ottengono o impostano elementi selezionati rappresentati da una matrice di elementi della shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iobjmgr"><strong>IObjMgr</strong></a><br/></td>
<td>Espone metodi che consentono a un client di aggiungere o rimuovere un oggetto da una raccolta di oggetti gestiti da un oggetto server.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopencontrolpanel"><strong>IOpenControlPanel</strong></a><br/></td>
<td>Espone metodi che recuperano lo stato di visualizzazione del pannello di controllo, il percorso dei singoli elementi del pannello di controllo e che aprono il pannello di controllo stesso o un singolo elemento del pannello di controllo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopensearchsource"><strong>IOpenSearchSource</strong></a><br/></td>
<td>Espone un metodo per ottenere i risultati della ricerca da un'origine dati OpenSearch sul lato client personalizzata.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ioperationsprogressdialog"><strong>IOperationsProgressDialog</strong></a><br/></td>
<td>Espone i metodi per ottenere, impostare ed eseguire una query su una finestra di dialogo di stato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ipackagedebugsettings"><strong>IPackageDebugSettings</strong></a><br/></td>
<td>Consente agli sviluppatori del debugger di controllare il ciclo di vita di un'app di Windows Store, ad esempio la sospensione o la ripresa.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipackageexecutionstatechangenotification"><strong>IPackageExecutionStateChangeNotification</strong></a><br/></td>
<td>Abilita la ricezione delle notifiche di modifica dello stato del pacchetto durante il debug delle app di Windows Store.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparentanditem"><strong>IParentAndItem</strong></a><br/></td>
<td>Espone metodi che ottengono e impostano l'elemento padre e l'ID figlio dell'elemento padre. Mentre <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparentanditem"><strong>IParentAndItem</strong></a> viene in genere implementato in IShellItems, non è specifico di <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iparseandcreateitem"><strong>IParseAndCreateItem</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder"><strong>IPersistFolder</strong></a><br/></td>
<td>Espone un metodo che inizializza gli oggetti cartella della shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2"><strong>IPersistFolder2</strong></a><br/></td>
<td>Espone metodi che ottengono informazioni dagli oggetti cartella della shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder3"><strong>IPersistFolder3</strong></a><br/></td>
<td>Estende le interfacce <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder"><strong>IPersistFolder</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistfolder2"><strong>IPersistFolder2</strong></a> consentendo a un oggetto Folder di implementare una gestione non predefinita dei collegamenti alla cartella.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipersistidlist"><strong>IPersistIDList</strong></a><br/></td>
<td>Espone i metodi utilizzati per salvare in modo permanente gli elenchi di identificatori di elemento.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-ipersistserializedpropstorage"><strong>IPersistSerializedPropStorage</strong></a><br/></td>
<td>Espone i metodi per salvare in modo permanente i dati di archiviazione delle proprietà serializzati per un utilizzo successivo e per ripristinare i dati salvati in una nuova istanza di archivio delle proprietà.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Propsys/nn-propsys-ipersistserializedpropstorage2"><strong>IPersistSerializedPropStorage2</strong></a><br/></td>
<td>Espone i metodi per salvare in modo permanente i dati di archiviazione delle proprietà serializzati per un utilizzo successivo e per ripristinare i dati salvati in una nuova istanza di archivio delle proprietà.<br/></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/legacy/hh707033(v=vs.85)"><strong>IPlaybackManager</strong></a><br/></td>
<td>Fornisce metodi che consentono alle applicazioni multimediali di comunicare con Windows Playback Manager.<br/></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/legacy/hh707034(v=vs.85)"><strong>IPlaybackManagerEvents</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler"><strong>IPreviewHandler</strong></a><br/></td>
<td>Espone metodi per la visualizzazione di anteprime avanzate.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe"><strong>IPreviewHandlerFrame</strong></a><br/></td>
<td>Consente ai gestori di anteprime di passare i tasti di scelta rapida all'host. Questa interfaccia recupera un elenco di scelte rapide da tastiera e indirizza l'host alla gestione di un tasto di scelta rapida.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals"><strong>IPreviewHandlerVisuals</strong></a><br/></td>
<td>Espone i metodi per applicare informazioni sui colori e sui tipi di carattere ai gestori di anteprime.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipreviewitem"><strong>IPreviewItem</strong></a><br/></td>
<td>Identifica un elemento che verrà visualizzato nel riquadro di anteprima.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ipreviousversionsinfo"><strong>IPreviousVersionsInfo</strong></a><br/></td>
<td>Espone un metodo che controlla le versioni precedenti dei file o delle cartelle del server, archiviate per la riversione con la tecnologia delle <em>copie shadow</em> fornita con Windows Server 2003.<br/></td>
</tr>
<tr class="odd">
<td><a href="iprivateidentitymanager.md"><strong>IPrivateIdentityManager</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="iprivateidentitymanager2.md"><strong>IPrivateIdentityManager2</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iprofferservice"><strong>IProfferService</strong></a><br/></td>
<td>Espone un meccanismo generale per gli oggetti per offrire servizi ad altri oggetti nello stesso host.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iprogressdialog"><strong>IProgressDialog</strong></a><br/></td>
<td>Espone metodi che consentono a un'applicazione di visualizzare una finestra di dialogo di stato. Questa interfaccia viene esportata dall'oggetto finestra di dialogo di stato (CLSID_ProgressDialog). Questo oggetto è un modo generico per mostrare a un utente il modo in cui un'operazione sta procedendo. Viene in genere utilizzato per l'eliminazione, il caricamento, la copia, lo scaricamento o il download di un numero elevato di file.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp"><strong>IPublishedApp</strong></a><br/></td>
<td>Espone metodi che rappresentano applicazioni per aggiungere/rimuovere programmi nel pannello di controllo. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp2"><strong>IPublishedApp2</strong></a><br/></td>
<td>Estende l'interfaccia <a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ipublishedapp"><strong>IPublishedApp</strong></a> fornendo un metodo di installazione aggiuntivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ipublishingwizard"><strong>IPublishingWizard</strong></a><br/></td>
<td>Espone metodi per l'utilizzo della procedura guidata di stampa online, della pubblicazione guidata sul Web e dell'aggiunta guidata posizione di rete. In Windows Vista, <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ipublishingwizard"><strong>IPublishingWizard</strong></a> non supporta più la pubblicazione guidata sul Web o la procedura guidata di stampa online.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlwapi/nn-shlwapi-iqueryassociations"><strong>IQueryAssociations</strong></a><br/></td>
<td>Espone metodi che semplificano il processo di recupero delle informazioni archiviate nel registro di sistema in associazione alla definizione di un tipo di file o di un protocollo e di associazione a un'applicazione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iquerycancelautoplay"><strong>IQueryCancelAutoPlay</strong></a><br/></td>
<td>Espone un metodo che esegue l'override di <a href="autorun2k-intro.md">AutoPlay</a> o <a href="autoplay.md">Autorun</a>a livello di codice. In questo modo è possibile personalizzare il percorso e il tipo di contenuto che viene avviato quando si inserisce un supporto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iquerycodepage"><strong>IQueryCodePage</strong></a><br/></td>
<td>Ottiene e imposta il valore numerico (identificatore della tabella codici) della tabella codici ANSI.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iquerycontinue"><strong>IQueryContinue</strong></a><br/></td>
<td>Espone un metodo che fornisce un semplice meccanismo standard per gli oggetti per eseguire una query su un client per l'autorizzazione a continuare un'operazione. I client di <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification"><strong>IUserNotification</strong></a>, ad esempio, devono passare un'implementazione di <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iquerycontinue"><strong>IQueryContinue</strong></a> al metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iusernotification-show"><strong>IUserNotification:: Show</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Credentialprovider/nn-credentialprovider-iquerycontinuewithstatus"><strong>IQueryContinueWithStatus</strong></a><br/></td>
<td>Espone metodi che forniscono un meccanismo standard per i provider di credenziali per chiamare <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iquerycontinue-querycontinue"><strong>QueryContinue</strong></a> durante il tentativo di connessione alla rete per determinare se è necessario continuare questi tentativi. I provider di credenziali possono inoltre utilizzare questa interfaccia per visualizzare i messaggi all'utente durante il tentativo di stabilire una connessione di rete.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iqueryinfo"><strong>IQueryInfo</strong></a><br/></td>
<td>Espone i metodi utilizzati dalla Shell per recuperare i flag e le informazioni sulla descrizione comando per un elemento che risiede in un'implementazione di <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> . I suggerimenti per le informazioni vengono in genere visualizzati all'interno di un controllo <a href="/windows/desktop/Controls/tooltip-controls">ToolTip</a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-irelateditem"><strong>IRelatedItem</strong></a><br/></td>
<td>Espone metodi che derivano elementi correlati con relazioni specifiche.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iremotecomputer"><strong>IRemoteComputer</strong></a><br/></td>
<td>Espone un metodo che enumera o Inizializza un'estensione dello spazio dei nomi quando viene richiamata su un oggetto remoto. Questa interfaccia viene usata, ad esempio, per inizializzare la cartella virtuale stampanti remote.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iresolveshelllink"><strong>IResolveShellLink</strong></a><br/></td>
<td>Espone un metodo che consente a un'applicazione di richiedere che un oggetto cartella della shell risolva un collegamento per uno dei relativi elementi.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iresultsfolder"><strong>IResultsFolder</strong></a><br/></td>
<td>Espone metodi che contengono elementi da un oggetto dati.<br/> Un <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iresultsfolder"><strong>IResultsFolder</strong></a> è una cartella che può conservare elementi di tutto lo spazio dei nomi e rappresentarli per l'utente in un'unica cartella.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-irunnabletask"><strong>IRunnableTask</strong></a><br/></td>
<td>Interfaccia a thread libero che può essere esposta da un oggetto per consentire l'esecuzione di operazioni su un thread in background. Se, ad esempio, il metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iextractimage-getlocation"><strong>IExtractImage:: getLocation</strong></a> restituisce E_PENDING, l'applicazione chiamante può estrarre l'immagine in un thread in background.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-isearchboxinfo"><strong>ISearchBoxInfo</strong></a><br/></td>
<td>Espone metodi che consentono al chiamante di recuperare le informazioni immesse in una casella di ricerca.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-isearchcontext"><strong>ISearchContext</strong></a><br/></td>
<td>Espone i metodi che canalizzano le informazioni di personalizzazione negli hook di ricerca.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isearchfolderitemfactory"><strong>ISearchFolderItemFactory</strong></a><br/></td>
<td>Espone metodi che creano e modificano cartelle di ricerca. I metodi set vengono chiamati per primi per impostare i parametri della ricerca. Quando non viene chiamato, verranno utilizzati i valori predefiniti. <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-getidlist"><strong>ISearchFolderItemFactory:: GetIDList</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isearchfolderitemfactory-getshellitem"><strong>ISearchFolderItemFactory:: GetShellItem</strong></a> restituiscono le due forme della ricerca specificata da questi parametri. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Thumbcache/nn-thumbcache-isharedbitmap"><strong>ISharedBitmap</strong></a><br/></td>
<td>Espone metodi efficaci per la memoria per l'accesso alle bitmap. Questa interfaccia viene utilizzata come wrapper sottile per gli oggetti HBITMAP, consentendo a tali oggetti di essere conteggiati e protetti dal fatto che i dati sottostanti sono stati modificati.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isharingconfigurationmanager"><strong>ISharingConfigurationManager</strong></a><br/></td>
<td>Espone metodi che impostano e recuperano informazioni sulle impostazioni di condivisione predefinite di un computer per la cartella <strong>Users</strong> ( <code>C:\Users</code> ) o <strong>public</strong> ( <code>C:\Users\Public</code> ). Espone inoltre un set di metodi che consentono il controllo della condivisione delle stampanti.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shappmgr/nn-shappmgr-ishellapp"><strong>IShellApp</strong></a><br/></td>
<td>Espone metodi che forniscono informazioni generali su un'applicazione all'applicazione Aggiungi/Rimuovi programmi. Non è possibile utilizzarlo all'esterno dell'applicazione Installazione applicazioni. Le informazioni fornite da questa interfaccia includono un elenco di azioni di gestione supportate e se l'applicazione è attualmente installata. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser"><strong>IShellBrowser</strong></a><br/></td>
<td>Implementata dagli host delle visualizzazioni della shell (oggetti che implementano <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a>). Espone metodi che forniscono servizi per la vista ospitata e altri oggetti che vengono eseguiti nel contesto della finestra di esplorazione. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishellchangenotify"><strong>IShellChangeNotify</strong></a><br/></td>
<td>Espone un metodo che notifica a un'estensione dello spazio dei nomi della shell quando l'ID di un elemento è stato modificato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelldetails"><strong>IShellDetails</strong></a><br/></td>
<td>Esposto dalle cartelle della Shell per fornire informazioni dettagliate sugli elementi di una cartella. Si tratta delle stesse informazioni visualizzate da Esplora risorse quando la visualizzazione della cartella è impostata su Details. Per i sistemi Windows 2000 e versioni successive, <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelldetails"><strong>IShellDetails</strong></a> viene sostituito da <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2"><strong>IShellFolder2</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellextinit"><strong>IShellExtInit</strong></a><br/></td>
<td>Espone un metodo che Inizializza le estensioni della Shell per le finestre delle proprietà, i menu di scelta rapida e i gestori di trascinamento della selezione (estensioni che aggiungono elementi ai menu di scelta rapida durante le operazioni di trascinamento della selezione non predefinite).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a><br/></td>
<td>Esposto da tutti gli oggetti cartella dello spazio dei nomi della shell, i relativi metodi vengono usati per gestire le cartelle.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2"><strong>IShellFolder2</strong></a><br/></td>
<td>Estende le funzionalità di <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a>. I metodi forniscono un'ampia gamma di informazioni sul contenuto di una cartella della shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="ishellfoldersearchable.md"><strong>IShellFolderSearchable</strong></a><br/></td>
<td>Espone metodi che consentono a un'estensione della shell di fornire uno spazio dei nomi in cui è possibile eseguire ricerche.<br/></td>
</tr>
<tr class="even">
<td><a href="ishellfoldersearchablecallback.md"><strong>IShellFolderSearchableCallback</strong></a><br/></td>
<td>Espone le routine di callback per monitorare il processo di ricerca.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishellfolderviewcb"><strong>IShellFolderViewCB</strong></a><br/></td>
<td>Espone un metodo che consente la comunicazione tra Esplora risorse e una visualizzazione cartella implementata utilizzando l'oggetto visualizzazione cartella di sistema (l'oggetto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a> restituito tramite <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview"><strong>SHCreateShellFolderView</strong></a>) in modo che la visualizzazione cartelle possa ricevere notifiche degli eventi e modificarne la visualizzazione di conseguenza.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shldisp/nn-shldisp-ishellfolderviewdual"><strong>IShellFolderViewDual</strong></a><br/></td>
<td>Espone i metodi che modificano la visualizzazione e selezionano gli elementi nella cartella corrente. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shldisp/nn-shldisp-ishellfolderviewdual2"><strong>IShellFolderViewDual2</strong></a><br/></td>
<td>Espone i metodi che modificano la visualizzazione e selezionano gli elementi nella cartella corrente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shldisp/nn-shldisp-ishellfolderviewdual3"><strong>IShellFolderViewDual3</strong></a><br/></td>
<td>Espone i metodi che modificano la visualizzazione della cartella corrente.<br/></td>
</tr>
<tr class="odd">
<td><a href="ishellfolderviewtype.md"><strong>IShellFolderViewType</strong></a><br/></td>
<td>Espone metodi che consentono a una cartella della shell di supportare visualizzazioni diverse sul contenuto (layout gerarchici diversi dei dati).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellicon"><strong>IShellIcon</strong></a><br/></td>
<td>Espone un metodo che ottiene un indice di icona per un oggetto <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder"><strong>IShellFolder</strong></a> . <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishelliconoverlay"><strong>IShellIconOverlay</strong></a><br/></td>
<td>Espone i metodi utilizzati da un'estensione dello spazio dei nomi per specificare le sovrapposizioni di icone per gli oggetti in esso contenuti.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelliconoverlayidentifier"><strong>IShellIconOverlayIdentifier</strong></a><br/></td>
<td>Espone i metodi che gestiscono tutte le comunicazioni tra i gestori sovrapposti delle icone e la Shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shimgdata/nn-shimgdata-ishellimagedataabort"><strong>IShellImageDataAbort</strong></a><br/></td>
<td>Espone un singolo metodo usato per interrompere i processi <a href="/windows/desktop/api/Shimgdata/nn-shimgdata-ishellimagedata"><strong>IShellImageData</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shimgdata/nn-shimgdata-ishellimagedatafactory"><strong>IShellImageDataFactory</strong></a><br/></td>
<td>Espone metodi che creano istanze <a href="/windows/desktop/api/Shimgdata/nn-shimgdata-ishellimagedata"><strong>IShellImageData</strong></a> basate su varie origini di immagini.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a><br/></td>
<td>Espone metodi che recuperano informazioni su un elemento della shell. <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem2"><strong>IShellItem2</strong></a> sono le rappresentazioni preferite degli elementi in qualsiasi nuovo codice.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem2"><strong>IShellItem2</strong></a><br/></td>
<td>Estende <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a> con metodi che recuperano i vari valori delle proprietà dell'elemento. <strong>IShellItem</strong> e <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem2"><strong>IShellItem2</strong></a> sono le rappresentazioni preferite degli elementi in qualsiasi nuovo codice.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray"><strong>IShellItemArray</strong></a><br/></td>
<td>Espone metodi che creano e modificano matrici di <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>elementi della shell</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemfilter"><strong>IShellItemFilter</strong></a><br/></td>
<td>Esposto da un client per specificare come filtrare l'enumerazione di un <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>elemento della shell</strong></a> da un'applicazione server.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemimagefactory"><strong>IShellItemImageFactory</strong></a><br/></td>
<td>Espone un metodo per restituire icone o anteprime per gli elementi della shell. Se per l'elemento richiesto non sono disponibili anteprime o icone, è possibile che venga fornita un'icona per classe dalla Shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemresources"><strong>IShellItemResources</strong></a><br/></td>
<td>Espone metodi per modificare ed eseguire query sulle risorse degli elementi della shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary"><strong>IShellLibrary</strong></a><br/></td>
<td>Espone metodi per la creazione e la gestione di librerie.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka"><strong>IShellLink</strong></a><br/></td>
<td>Espone metodi che consentono di creare, modificare e risolvere i collegamenti della shell.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist"><strong>IShellLinkDataList</strong></a><br/></td>
<td>Espone metodi che consentono a un'applicazione di collegare blocchi di dati aggiuntivi a un <a href="/windows/desktop/shell/links">collegamento della shell</a>. Questi metodi aggiungono, copiano o rimuovono i blocchi di dati.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu"><strong>IShellMenu</strong></a><br/></td>
<td>Espone i metodi che interagiscono con i menu della shell, ad esempio il menu <strong>Start</strong> e il menu <strong>Preferiti</strong> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback"><strong>IShellMenuCallback</strong></a><br/></td>
<td>Interfaccia di callback che espone un metodo che riceve messaggi da una banda di menu.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext"><strong>IShellPropSheetExt</strong></a><br/></td>
<td>Espone metodi che consentono a un gestore della finestra delle proprietà di aggiungere o sostituire pagine nella finestra delle proprietà visualizzata per un oggetto file.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl/nn-shobjidl-ishellrundll"><strong>IShellRunDll</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a><br/></td>
<td>Espone i metodi che presentano una visualizzazione nelle finestre Esplora risorse o cartella.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview2"><strong>IShellView2</strong></a><br/></td>
<td>Estende le funzionalità di <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview"><strong>IShellView</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ishellview3"><strong>IShellView3</strong></a><br/></td>
<td>Estende le funzionalità di <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview2"><strong>IShellView2</strong></a> fornendo un metodo per sostituire <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview2-createviewwindow2"><strong>IShellView2:: CreateViewWindow2</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows"><strong>IShellWindows</strong></a><br/></td>
<td>Consente di accedere alla raccolta di finestre aperte della shell.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-istartmenupinnedlist"><strong>IStartMenuPinnedList</strong></a><br/></td>
<td>Espone un metodo che sblocca il collegamento di un'applicazione dal menu <strong>Start</strong> o dalla barra delle applicazioni.<br/></td>
</tr>
<tr class="odd">
<td><a href="nn-shobjidl-istorageprovidercopyhook.md"><strong>IStorageProviderCopyHook</strong></a><br/></td>
<td>Espone un metodo che determina se la shell sarà consentita per lo spostamento, la copia, l'eliminazione o la ridenominazione di una cartella nella radice di sincronizzazione di un provider di cloud.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/storageprovider/nn-storageprovider-istorageproviderhandler"><strong>IStorageProviderHandler</strong></a><br/></td>
<td>Recupera l'oggetto <a href="/windows/desktop/api/storageprovider/nn-storageprovider-istorageproviderpropertyhandler"><strong>IStorageProviderPropertyHandler</strong></a> associato a un file o a una cartella specifica.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/storageprovider/nn-storageprovider-istorageproviderpropertyhandler"><strong>IStorageProviderPropertyHandler</strong></a><br/></td>
<td>Fornisce una raccolta di proprietà associate a un file o a una cartella.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-istreamasync"><strong>IStreamAsync</strong></a><br/></td>
<td>Espone i metodi per gestire input/outbronct (I/O) in un flusso asincrono. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-istreamunbufferedinfo"><strong>IStreamUnbufferedInfo</strong></a><br/></td>
<td>Espone un metodo che determina le dimensioni del settore come supporto per l'allineamento dei byte.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-isuspensiondependencymanager"><strong>ISuspensionDependencyManager</strong></a><br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflict"><strong>ISyncMgrConflict</strong></a><br/></td>
<td>Espone metodi che forniscono informazioni su un conflitto recuperato da un archivio dei conflitti e consente la risoluzione del conflitto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictfolder"><strong>ISyncMgrConflictFolder</strong></a><br/></td>
<td>Espone un metodo che ottiene l'elenco di ID dei conflitti per un oggetto conflitto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictitems"><strong>ISyncMgrConflictItems</strong></a><br/></td>
<td>Espone metodi che ottengono i dati e il conteggio degli elementi in conflitto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictpresenter"><strong>ISyncMgrConflictPresenter</strong></a><br/></td>
<td>Espone un metodo che presenta un conflitto all'utente.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictresolutionitems"><strong>ISyncMgrConflictResolutionItems</strong></a><br/></td>
<td>Espone metodi che ottengono informazioni sull'elemento e il conteggio degli elementi.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictresolveinfo"><strong>ISyncMgrConflictResolveInfo</strong></a><br/></td>
<td>Espone metodi che ottengono e impostano informazioni sulla risoluzione dei conflitti di gestione sincronizzazione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictstore"><strong>ISyncMgrConflictStore</strong></a><br/></td>
<td>Espone metodi che consentono a un gestore di fornire conflitti che vengono visualizzati nella cartella dei conflitti.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrcontrol"><strong>ISyncMgrControl</strong></a><br/></td>
<td>Espone metodi che consentono a un'applicazione o a un gestore di avviare o arrestare una sincronizzazione, notificare al centro di sincronizzazione le modifiche apportate al set di gestori o elementi oppure notificare le modifiche ai valori delle proprietà.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems"><strong>ISyncMgrEnumItems</strong></a><br/></td>
<td>Espone metodi che enumerano una matrice di strutture <a href="/windows/win32/api/mobsync/ns-mobsync-syncmgritem"><strong>SYNCMGRITEM</strong></a> . Ognuna di queste strutture fornisce informazioni su un elemento che può essere sincronizzato. <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrenumitems"><strong>ISyncMgrEnumItems</strong></a> ha gli stessi metodi di tutte le interfacce dell'enumeratore standard: Next, Skip, reset e clone.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrevent"><strong>ISyncMgrEvent</strong></a><br/></td>
<td>Espone metodi che recuperano dati da un archivio eventi. Un archivio eventi consente al Centro sincronizzazione di ottenere un enumeratore di tutti gli eventi nell'archivio, oltre a recuperare singoli eventi.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgreventlinkuioperation"><strong>ISyncMgrEventLinkUIOperation</strong></a><br/></td>
<td>Fornisce un metodo che viene chiamato quando si fa clic sui collegamenti evento nella cartella dei risultati della sincronizzazione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgreventstore"><strong>ISyncMgrEventStore</strong></a><br/></td>
<td>Espone metodi che consentono a un gestore di fornire il proprio archivio eventi e gestire i propri eventi di sincronizzazione, anziché usare l'archivio eventi predefinito del Centro sincronizzazione. Questi eventi vengono visualizzati nella cartella Sync results.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandler"><strong>ISyncMgrHandler</strong></a><br/></td>
<td>Espone metodi che costituiscono l'interfaccia primaria implementata da un gestore di sincronizzazione. Centro sincronizzazione crea un'istanza del gestore tramite questa interfaccia per ottenere le proprietà, enumerare gli elementi di sincronizzazione e modificare lo stato. Il Centro sincronizzazione crea un'istanza separata del gestore in un thread separato per eseguire una sincronizzazione o un'operazione dell'interfaccia utente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandlercollection"><strong>ISyncMgrHandlerCollection</strong></a><br/></td>
<td>Espone metodi che forniscono un enumeratore di ID gestore di sincronizzazione e creano un'istanza di questi gestori di sincronizzazione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrhandlerinfo"><strong>ISyncMgrHandlerInfo</strong></a><br/></td>
<td>Espone metodi che consentono a un gestore di fornire informazioni sulla proprietà e sullo stato al centro di sincronizzazione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrregister"><strong>ISyncMgrRegister</strong></a><br/></td>
<td>Espone metodi che consentono a un'applicazione di registrarsi con Gestione sincronizzazione. Questa operazione può essere eseguita tramite l'interfaccia <a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrregister"><strong>ISyncMgrRegister</strong></a> o eseguendo la registrazione direttamente nel registro di sistema.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrresolutionhandler"><strong>ISyncMgrResolutionHandler</strong></a><br/></td>
<td>Espone i metodi che gestiscono i conflitti di sincronizzazione. Implementare questa interfaccia per costruire un gestore dei conflitti di sincronizzazione. L'interfaccia utente (UI) per la risoluzione dei conflitti chiamerà questa interfaccia per risolvere il conflitto presentato all'utente. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrschedulewizarduioperation"><strong>ISyncMgrScheduleWizardUIOperation</strong></a><br/></td>
<td>Espone un metodo che consente a un gestore di visualizzare la pianificazione guidata della sincronizzazione per il gestore.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsessioncreator"><strong>ISyncMgrSessionCreator</strong></a><br/></td>
<td>Espone un solo metodo tramite il quale un gestore o un'applicazione esterna può notificare al centro di sincronizzazione che la sincronizzazione è iniziata, nonché segnalare lo stato di avanzamento e gli eventi.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynccallback"><strong>ISyncMgrSyncCallback</strong></a><br/></td>
<td>Espone metodi che consentono a un processo di sincronizzazione di segnalare lo stato di avanzamento e gli eventi al centro di sincronizzazione o di eseguire una query su se il processo è stato annullato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronize"><strong>ISyncMgrSynchronize</strong></a><br/></td>
<td>Espone metodi che consentono all'applicazione o al servizio registrato di ricevere notifiche dalla gestione sincronizzazione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback"><strong>ISyncMgrSynchronizeCallback</strong></a><br/></td>
<td>Espone i metodi che gestiscono il processo di sincronizzazione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mobsync/nn-mobsync-isyncmgrsynchronizeinvoke"><strong>ISyncMgrSynchronizeInvoke</strong></a><br/></td>
<td>Espone metodi che consentono a un'applicazione registrata di richiamare Gestione sincronizzazione per aggiornare gli elementi.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitem"><strong>ISyncMgrSyncItem</strong></a><br/></td>
<td>Espone metodi che agiscono su e recuperano informazioni da un singolo elemento di sincronizzazione, consentendo ai gestori di gestire gli elementi di sincronizzazione come oggetti indipendenti.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncitemcontainer"><strong>ISyncMgrSyncItemContainer</strong></a><br/></td>
<td>Espone metodi che forniscono informazioni ai gestori sugli elementi in essi contenuti.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsynciteminfo"><strong>ISyncMgrSyncItemInfo</strong></a><br/></td>
<td>Espone metodi che forniscono informazioni sulla proprietà e sullo stato per un singolo elemento di sincronizzazione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrsyncresult"><strong>ISyncMgrSyncResult</strong></a><br/></td>
<td>Espone un metodo che le applicazioni che chiamano <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrcontrol"><strong>ISyncMgrControl</strong></a> possono usare per ottenere il risultato di una chiamata a <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrcontrol-starthandlersync"><strong>ISyncMgrControl:: StartHandlerSync</strong></a> o <a href="/windows/desktop/api/Syncmgr/nf-syncmgr-isyncmgrcontrol-startitemsync"><strong>ISyncMgrControl:: StartItemSync</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgruioperation"><strong>ISyncMgrUIOperation</strong></a><br/></td>
<td>Espone un metodo tramite il quale un gestore di sincronizzazione o un elemento di sincronizzazione può visualizzare un oggetto dell'interfaccia utente quando richiesto dal Centro sincronizzazione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist"><strong>ITaskbarList</strong></a><br/></td>
<td>Espone metodi che controllano la barra delle applicazioni. Consente di aggiungere, rimuovere e attivare dinamicamente elementi sulla barra delle applicazioni.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist2"><strong>ITaskbarList2</strong></a><br/></td>
<td>Estende l'interfaccia <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist"><strong>ITaskbarList</strong></a> esponendo un metodo per contrassegnare una finestra come schermo a schermo intero.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3"><strong>All'ITaskbarList3</strong></a><br/></td>
<td>Estende <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist2"><strong>ITaskbarList2</strong></a> esponendo metodi che supportano la funzionalità di avvio e cambio unificata del pulsante della barra delle applicazioni aggiunto in Windows 7. Questa funzionalità include rappresentazioni di anteprime e destinazioni switch basate su singole schede in un'applicazione a schede, sulle barre degli strumenti di anteprima, sulle sovrapposizioni di notifiche e sullo stato e sugli indicatori di stato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist4"><strong>ITaskbarList4</strong></a><br/></td>
<td>Estende <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3"><strong>all'ITaskbarList3</strong></a> fornendo un metodo che consente al chiamante di controllare due valori di proprietà per l'anteprima della scheda e la funzionalità di visualizzazione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailcache"><strong>IThumbnailCache</strong></a><br/></td>
<td>Espone i metodi per una cache di anteprima di sistema condivisa tra le applicazioni.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/thumbcache/nn-thumbcache-ithumbnailcacheprimer"><strong>IThumbnailCachePrimer</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ithumbnailhandlerfactory"><strong>IThumbnailHandlerFactory</strong></a><br/></td>
<td>Espone un metodo per il recupero del gestore di anteprime di un elemento. Implementare questa interfaccia se si desidera specificare quale estrazione viene utilizzata per un IDList figlio.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider"><strong>IThumbnailProvider</strong></a><br/></td>
<td>Espone un metodo per ottenere un'immagine di anteprima ed è destinato a essere implementato per i gestori di anteprime. L'oggetto che implementa questa interfaccia deve implementare anche <a href="/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream"><strong>IInitializeWithStream</strong></a>. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailsettings"><strong>IThumbnailSettings</strong></a><br/></td>
<td>Fornisce un metodo che consente a un provider di anteprime di determinare il contesto utente di una richiesta di anteprima.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/thumbnailstreamcache/nn-thumbnailstreamcache-ithumbnailstreamcache"><strong>IThumbnailStreamCache</strong></a><br/></td>
<td>Ottiene o imposta il flusso di anteprime. Questa interfaccia è solo per uso interno e può essere chiamata solo dall'applicazione Photos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shdeprecated/nn-shdeprecated-itrackshellmenu"><strong>ITrackShellMenu</strong></a><br/></td>
<td>Espone metodi che estendono l'interfaccia <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu"><strong>IShellMenu</strong></a> offrendo la possibilità di coordinare i pulsanti della barra degli strumenti con un menu e visualizzare un menu a comparsa.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Imagetranscode/nn-imagetranscode-itranscodeimage"><strong>ITranscodeImage</strong></a><br/></td>
<td>Espone un metodo che consente la conversione in formati di immagine JPEG o bitmap (BMP) da qualsiasi tipo di immagine supportato da Windows. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferadvisesink"><strong>ITransferAdviseSink</strong></a><br/></td>
<td>Espone metodi che supportano la raccolta di stato e le informazioni sull'errore.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferdestination"><strong>ITransferDestination</strong></a><br/></td>
<td>Espone metodi che creano un elemento della shell di destinazione per un'operazione di copia o spostamento. Questa interfaccia viene fornita per consentire un maggiore controllo sulle operazioni sui file fornendo un metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransferdestination-advise"><strong>ITransferDestination:: Advise</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfermediumitem"><strong>ITransferMediumItem</strong></a><br/></td>
<td>Utilizzato da un motore di copia per ottenere l'elemento sul quale chiamare <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>QueryInterface</strong></a> per restituire un puntatore all'interfaccia <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransferdestination"><strong>ITransferDestination</strong></a> o interfaccia <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfersource"><strong>ITransferSource</strong></a>. È possibile eseguire query su queste interfacce ed enumerarle per operazioni di copia, spostamento o eliminazione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itransfersource"><strong>ITransferSource</strong></a><br/></td>
<td>Espone i metodi per modificare <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem"><strong>IShellItem</strong></a>, inclusi copia, spostamento, riciclo e altro. Questa interfaccia viene offerta per fornire un maggiore controllo sulle operazioni sui file fornendo un metodo <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itransfersource-advise"><strong>ITransferSource:: Advise</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-itraydeskband"><strong>ITrayDeskBand</strong></a><br/></td>
<td>Espone metodi che mostrano, nascondono ed eseguono query su deskbands.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iupdateidlist"><strong>IUpdateIDList</strong></a><br/></td>
<td>Fornisce un metodo per aggiornare l' <a href="/windows/desktop/api/Shtypes/ns-shtypes-itemidlist"><strong>ID</strong></a> dell'elemento figlio di un oggetto Folder.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iurlsearchhook"><strong>IURLSearchHook</strong></a><br/></td>
<td>Espone un metodo utilizzato dal browser per convertire l'indirizzo di un protocollo URL sconosciuto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iurlsearchhook2"><strong>IURLSearchHook2</strong></a><br/></td>
<td>Espone un metodo utilizzato dal browser per convertire l'indirizzo di un protocollo URL sconosciuto utilizzando un oggetto del contesto di ricerca.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iuseraccountchangecallback"><strong>IUserAccountChangeCallback</strong></a><br/></td>
<td>Espone un metodo che viene chiamato quando viene modificata l'immagine che rappresenta un account utente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification"><strong>IUserNotification</strong></a><br/></td>
<td>Espone i metodi che impostano le informazioni di notifica e quindi visualizzano la notifica all'utente in un fumetto visualizzato insieme all'area di notifica della barra delle applicazioni. <br/>
<blockquote>
[!Note]<br />
<a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2"><strong>IUserNotification2</strong></a> differisce da <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification"><strong>IUserNotification</strong></a> solo nel metodo <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-iusernotification2-show"><strong>show</strong></a> , che aggiunge un parametro aggiuntivo per un'interfaccia di callback per comunicare con la notifica. In caso contrario, le due interfacce sono identiche nel form e nella funzione. CLSID_UserNotification implementa entrambe le versioni di <strong>show</strong> come overload.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2"><strong>IUserNotification2</strong></a><br/></td>
<td>Espone i metodi che impostano le informazioni di notifica e quindi visualizzano la notifica all'utente in un fumetto visualizzato insieme all'area di notifica della barra delle applicazioni. <br/>
<blockquote>
[!Note]<br />
<a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotification2"><strong>IUserNotification2</strong></a> non eredita da <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iusernotification"><strong>IUserNotification</strong></a>. <strong>IUserNotification2</strong> differisce da <strong>IUserNotification</strong> solo nel metodo <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-iusernotification2-show"><strong>show</strong></a> , che aggiunge un parametro aggiuntivo per un'interfaccia di callback per comunicare con la notifica. In caso contrario, le due interfacce sono identiche nel form e nella funzione. CLSID_UserNotification implementa entrambe le versioni di <strong>show</strong> come overload.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iusernotificationcallback"><strong>IUserNotificationCallback</strong></a><br/></td>
<td>Espone un metodo per la gestione dell'accesso di un clic del mouse o di un menu di scelta rapida in un fumetto di notifica. Usato con <a href="/windows/desktop/api/Shobjidl/nf-shobjidl-iusernotification2-show"><strong>IUserNotification2:: Show</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/shobjidl/nn-shobjidl-iusetobrowseitem"><strong>IUseToBrowseItem</strong></a><br/></td>
<td>Trova l'elemento da utilizzare per l'esplorazione di questo elemento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iviewstateidentityitem"><strong>IViewStateIdentityItem</strong></a><br/></td>
<td>Fornisce un elemento di persistenza canonico, ovvero un elemento per il quale verranno memorizzate le personalizzazioni della visualizzazione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shobjidl_core/nn-shobjidl_core-ivirtualdesktopmanager"><strong>IVirtualDesktopManager</strong></a><br/></td>
<td>Espone metodi che consentono a un'applicazione di interagire con gruppi di finestre che formano aree di lavoro virtuali.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-ivisualproperties"><strong>IVisualProperties</strong></a><br/></td>
<td>Espone metodi che impostano e ottengono proprietà visive.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iwebwizardextension"><strong>IWebWizardExtension</strong></a><br/></td>
<td>Estende l'interfaccia <a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iwizardextension"><strong>IWizardExtension</strong></a> esponendo i metodi per impostare l'URL iniziale dell'estensione della procedura guidata e un URL specifico in caso di errore.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iwizardextension"><strong>IWizardExtension</strong></a><br/></td>
<td>Utilizzato dalle procedure guidate quali la pubblicazione guidata sul Web e l'ordinamento guidato di stampa online che ospita le pagine di contenuto lato server. Questa interfaccia espone i metodi per specificare le pagine di estensione supportate e per spostarsi all'interno e all'esterno di tali pagine.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shobjidl/nn-shobjidl-iwizardsite"><strong>IWizardSite</strong></a><br/></td>
<td>Espone i metodi utilizzati da un'estensione della procedura guidata per spostarsi tra i bordi e il resto della procedura guidata.<br/></td>
</tr>
<tr class="odd">
<td><a href="taskcompletionclient.md"><strong>TaskCompletionClient</strong></a><br/></td>
<td>Consente il completamento dell'attività. <br/></td>
</tr>
</tbody>
</table>



 

 

 
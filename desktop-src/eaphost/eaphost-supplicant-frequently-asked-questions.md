---
title: Domande frequenti sul richiedente EAPHost
description: In questo argomento vengono fornite le risposte alle domande più comuni sull'API del richiedente EAPHost.
ms.assetid: bf8db711-386e-47c2-be47-4cfd6c4d8d9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c38e75220b186ef58f2b9f264f8f5fc0550a4119
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/18/2020
ms.locfileid: "103735298"
---
# <a name="eaphost-supplicant-frequently-asked-questions"></a>Domande frequenti sul richiedente EAPHost

In questo argomento vengono fornite le risposte alle domande più comuni sull'API del richiedente EAPHost.

### <a name="eaphost-supplicant-frequently-asked-questions"></a>Domande frequenti sul richiedente EAPHost



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Domanda</th>
<th>Risposta</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Perché è necessario chiamare [<strong>EapHostPeerInitialize</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerinitialize) e [<strong>EapHostPeerUninitialize</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeeruninitialize)?</td>
<td>[<strong>EapHostPeerInitialize</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerinitialize) e [<strong>EapHostPeerUninitialize</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeeruninitialize) inizializzare e annullare l'inizializzazione dell'ambiente com utilizzato per la comunicazione interprocesso (IPC) tra un supplicant e EAPHost.</td>
</tr>
<tr class="even">
<td>Quali funzioni devono essere richiamate sui thread con COM inizializzato per [Apartment a thread singolo](/previous-versions/ms810413(v=msdn.10)) (sta)?</td>
<td>[<strong>EapHostPeerInvokeConfigUI</strong>] è necessario chiamare (/Previous-Versions/Windows/Desktop/API/eaphostpeerconfigapis/NF-eaphostpeerconfigapis-eaphostpeerinvokeconfigui), [<strong>EapHostPeerInvokeInteractiveUI</strong>] (/Previous-Versions/Windows/Desktop/API/eaphostpeerconfigapis/NF-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) e [<strong>EapHostAuthenticatorInvokeConfigUI</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodauthenticatorapis/NF-eapmethodauthenticatorapis-eapmethodauthenticatorinvokeconfigui) sui thread con com inizializzato per sta. Questa operazione può essere eseguita chiamando l'API COM [<strong>CoInitialize</strong>] (/Windows/Win32/API/OBJBASE/NF-OBJBASE-CoInitialize); al termine del supplicante, il thread STA [<strong>CoUninitialize</strong>] (/Windows/Win32/API/combaseapi/NF-combaseapi-CoUninitialize) deve essere chiamato prima di uscire.</td>
</tr>
<tr class="odd">
<td>In che modo EAPHost Esporta il materiale delle chiavi?</td>
<td>I metodi EAP EAPHost esportano le chiavi della sessione master (MSKs) sotto forma di chiavi Microsoft Point-to-Point Encryption (MPPE) per i supplicant. I materiali per le chiavi aggiuntive, ad esempio le chiavi master pairwise (PMKs), possono essere generati dal supplicant usando MSK. Per i metodi per la generazione di altre chiavi durante l'autenticazione, i metodi possono fornire tali chiavi come attributi specifici del fornitore ai supplicant.</td>
</tr>
<tr class="even">
<td>Che cos'è una chiave della sessione master estesa (EMSK)?</td>
<td>EMSK è un materiale aggiuntivo per le chiavi esportato dal metodo EAP. La lunghezza di EMSK è di almeno 64 ottetti. EMSK viene condiviso tra il client e il server EAP, ma non viene condiviso con l'autenticatore o con altre terze parti. Attualmente, EMSK è riservato per un uso futuro. Per ulteriori informazioni, vedere [requisiti del metodo Extensible Authentication Protocol EAP) per le reti LAN wireless](https://go.microsoft.com/fwlink/p/?linkid=84064).<br/></td>
</tr>
<tr class="odd">
<td>Quando un metodo utilizza o genera un attributo?</td>
<td>Se un metodo EAP genera attributi o EMSK, il richiedente utilizzerà gli attributi. In genere, gli attributi utilizzati dai supplicant sono chiavi. Gli attributi utilizzati sono <strong>eatPeerId</strong>, <strong>eatServerId</strong>, <strong>eatMethodId</strong>, <strong>eatEMSK</strong>e <strong>eatCredentialsChanged</strong>. Per ulteriori informazioni, vedere [<strong>EAP_ATTRIBUTE_TYPE</strong>] (/Windows/Desktop/API/eaptypes/ne-eaptypes-eap_attribute_type). Un metodo EAP può esportare materiale EMSK aggiuntivo specifico dell'applicazione, ad esempio:
<ul>
<li>ID sessione</li>
<li>[Protezione accesso alla rete](/windows/desktop/NAP/network-access-protection-start-page) (NAP)</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Quali attributi utilizzano [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) ?</td>
<td>Il supplicant wireless [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) nativo utilizzerà gli attributi di autenticazione EAPHost seguenti:
<ul>
<li>Notifica di modifica della password</li>
<li>Chiavi di invio/ricezione di Microsoft Point-to-Point Encryption (MPPE). VendorId/VendorType = 331/16 e 311/1</li>
</ul>
Le chiavi di MPPE sono chiavi generate alla fine di un'autenticazione corretta, sia dal peer che dall'autenticatore. Queste chiavi vengono usate da [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) e dal server di accesso alla rete (NAS) per crittografare e decrittografare i pacchetti inviati e ricevuti.<br/></td>
</tr>
<tr class="odd">
<td>Qual è lo scopo del flag di EAP_PEER_FLAG_GUEST_ACCESS in EAPHost?</td>
<td>Quando questo flag è impostato in [<strong>EAPHostPeerBeginSession</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession), EAPHost lo interpreta come una richiesta di autorizzazione Guest e restituisce una risposta di identità <strong>null</strong> che viene quindi passata al supplicant e restituita al server EAP.</td>
</tr>
<tr class="even">
<td>In che modo il richiedente esegue l'autenticazione del computer?</td>
<td>L'autenticazione del computer viene richiesta impostando il flag [<strong>EAP_FLAG_MACHINE_AUTH</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession).</td>
</tr>
<tr class="odd">
<td>In che modo il supplicant richiede l'autenticazione utente?</td>
<td>L'autenticazione utente viene richiesta senza impostare il flag [<strong>EAP_FLAG_MACHINE_AUTH</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession).</td>
</tr>
<tr class="even">
<td>Quando si usa [<strong>EapHostPeerFreeErrorMemory</strong>] (/Previous-Versions/Windows/Desktop/API/eaphostpeerconfigapis/NF-eaphostpeerconfigapis-eaphostpeerfreeerrormemory) invece della funzione [<strong>EapHostFreeEapError</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerfreeeaperror)?</td>
<td>La funzione [<strong>EapHostPeerFreeErrorMemory</strong>] (/Previous-Versions/Windows/Desktop/API/eaphostpeerconfigapis/NF-eaphostpeerconfigapis-eaphostpeerfreeerrormemory) viene usata solo per liberare le strutture [<strong>EAP_ERROR</strong>] (/Windows/Desktop/API/eaptypes/NS-eaptypes-eap_error) restituite dalle API di configurazione EAPHost. Le API di configurazione EAPHost sono definite in EapHostPeerConfigApis. h. Al contrario, la funzione [<strong>EapHostPeerFreeEapError</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerfreeeaperror) viene usata per liberare le strutture <strong>EAP_ERROR</strong> restituite dalle API di runtime EAPHost. Le API di runtime EAPHost sono definite in EapPApis. h. Non usare mai la versione di run-time dell'API con la versione di configurazione delle API; a tale scopo, potrebbe produrre risultati imprevisti.<br/></td>
</tr>
<tr class="odd">
<td>Ho implementato l'interfaccia utente nello stesso thread usato per elaborare una sessione di autenticazione EAP nel supplicant. Dopo aver generato una finestra di dialogo dell'interfaccia utente interattiva per ottenere le credenziali o altri dati di input dell'utente, la chiamata successiva da EAPHost a un metodo peer EAP ha esito negativo con <strong>ERROR_OBJECT_DISCONNECTED</strong>. Perché si è verificato questo problema e come risolverlo?</td>
<td>Mentre le API lato client EAPHost sono tutte API di tipo C, queste API C sono solo wrapper di API COM corrispondenti. Le API di stile C vengono eseguite in un ambiente COM multithread. Il codice dell'interfaccia utente viene in genere eseguito nel modello di thread apartment. Poiché i due modelli di thread sono in conflitto tra loro, non eseguire il codice dell'interfaccia utente nello stesso thread che elabora le autenticazioni EAP.</td>
</tr>
<tr class="even">
<td>Perché l'API [<strong>EapHostPeerBeginSession</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession) accetta un puntatore alla funzione di callback [<em>NotificationHandler</em>] (/Previous-Versions/Windows/Desktop/API) come parametro?</td>
<td>[<em>NotificationHandler</em>] (/Previous-Versions/Windows/Desktop/API) è il meccanismo mediante il quale un supplicant riceve una notifica che deve eseguire di nuovo l'autenticazione. Esistono diversi scenari in cui è necessario che il richiedente esegua di nuovo l'autenticazione, inclusa l'autenticazione con [Protezione accesso alla rete](/windows/desktop/NAP/network-access-protection-start-page) (NAP).</td>
</tr>
<tr class="odd">
<td>Qual è lo scopo del parametro <em>pConnectionId</em> nell'API [<strong>EapHostPeerBeginSession</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession)?</td>
<td><em>pConnectionId</em> è un puntatore a un valore GUID definito dal richiedente utilizzato per identificare una connessione di rete appartenente al supplicante. Quando viene chiamata la funzione di callback [<em>NotificationHandler</em>] (/Previous-Versions/Windows/Desktop/API), questo GUID viene passato per identificare la connessione di rete che verrà usata dal supplicant per la riautenticazione delle richieste.</td>
</tr>
<tr class="even">
<td>Ricerca per categorie verificare se lo stato della quarantena è stato modificato?</td>
<td>L'utente riceverà una notifica visiva di una modifica dello stato di quarantena solo se nel sistema è presente almeno un'interfaccia registrata client di QEC (NAP) di protezione accesso alla rete. In tal caso, quando si tenta di ripetere l'autenticazione, l'utente riceverà una notifica relativa alla modifica dello stato di quarantena tramite una finestra popup.</td>
</tr>
<tr class="odd">
<td>Ricerca per categorie verificare se nel sistema è presente un'interfaccia registrata di protezione accesso alla rete QEC?</td>
<td>Aprire una finestra con privilegi elevati ed eseguire il comando netsh seguente: &quot; netsh nap client show state &quot; . Per ulteriori informazioni, vedere [comandi netsh](/previous-versions/windows/it-pro/windows-server-2003/cc779693(v=ws.10)).</td>
</tr>
<tr class="even">
<td>Se il richiedente esegue di nuovo l'autenticazione, quale ID di connessione deve usare QEC durante la riautenticazione?</td>
<td>QEC deve usare lo stesso ID di connessione usato per la sessione precedente.</td>
</tr>
<tr class="odd">
<td>Per visualizzare le finestre di dialogo dell'interfaccia utente è disponibile un solo metodo di supplicant EAPHost, ma i metodi EAP hanno diversi tipi di chiamate specifiche dell'interfaccia utente. Quale metodo deve chiamare il richiedente quando ottiene il codice dell'azione <strong>EapHostPeerResponseInvokeUI</strong> , che indica che il richiedente deve visualizzare una finestra di dialogo dell'interfaccia utente?</td>
<td>Non è richiesta alcuna azione da parte dell'utente perché EAPHost sa quale funzione del metodo chiamare. Ad esempio, quando viene restituito il codice di azione <strong>EapHostPeerResponseInvokeUI</strong> , il supplicant chiama queste tre funzioni nell'ordine seguente: [<strong>EapHostPeerGetUIContext</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeergetuicontext), [<strong>EapHostPeerInvokeInteractiveUI</strong>] (/Previous-Versions/Windows/Desktop/API/eaphostpeerconfigapis/NF-eaphostpeerconfigapis-eaphostpeerinvokeinteractiveui) e [<strong>EapHostPeerSetUIContext</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeersetuicontext).</td>
</tr>
<tr class="even">
<td>Qual è la differenza tra un BLOB di credenziali e un BLOB di configurazione?</td>
<td>Il BLOB di credenziali contiene solo dati utente, ad esempio nome utente, password e PIN. Il BLOB di configurazione contiene le impostazioni che controllano il comportamento del metodo.</td>
</tr>
<tr class="odd">
<td>È possibile abilitare la traccia sul lato client EAPHost?</td>
<td>Sì. Per ulteriori informazioni, vedere [Abilitazione della traccia](enabling-tracing.md).</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sull'API del richiedente EAPHost](eap-host-supplicant-api-reference.md)
</dt> <dt>

[Domande frequenti generali su EAPHost](general-frequently-asked-questions.md)
</dt> <dt>

[Domande frequenti sul metodo EAPHost](eap-method-frequently-asked-questions.md)
</dt> <dt>

[Domande frequenti sullo sviluppo di EAPHost](eaphost-development-frequently-asked-questions.md)
</dt> </dl>


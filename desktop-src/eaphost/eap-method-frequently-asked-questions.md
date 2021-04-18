---
title: Domande frequenti sul metodo EAP
description: Fornisce le risposte alle domande di programmazione più frequenti sulla creazione di metodi EAP.
ms.assetid: 244e048f-4cc0-4094-a2b9-0f84674a293c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fddcc2194f5fe68dc660e40331be1b790b73386
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "106300608"
---
# <a name="eap-method-frequently-asked-questions"></a>Domande frequenti sul metodo EAP

In questo argomento vengono fornite le risposte alle domande di programmazione più frequenti sulla creazione di metodi EAP.

## <a name="eap-method-frequently-asked-questions"></a>Domande frequenti sul metodo EAP



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
<td>Che cosa sono &quot; i dati di configurazione &quot; ?</td>
<td>I dati &quot; di configurazione &quot; e i dati di connessione dei termini &quot; &quot; sono sinonimi.</td>
</tr>
<tr class="even">
<td>&quot;Informazioni sui dati di &quot; connessione</td>
<td>&quot;I dati &quot; di connessione sono un BLOB opaco specifico del metodo EAP che contiene informazioni di configurazione per il metodo. Questi dati di connessione vengono creati dal metodo al momento della configurazione iniziale e non vengono mai interpretati o modificati da un altro componente rispetto al metodo EAP stesso.</td>
</tr>
<tr class="odd">
<td>Che cosa sono le &quot; credenziali &quot; ?</td>
<td>I termini &quot; credenziali &quot; e &quot; dati utente &quot; sono sinonimi.</td>
</tr>
<tr class="even">
<td>Che cosa sono &quot; i dati utente &quot; ?</td>
<td>&quot;I dati utente &quot; sono un BLOB opaco specifico del metodo EAP che contiene i dati delle credenziali utente, ad esempio un nome utente e una password. I dati utente non vengono mai interpretati o modificati da un altro componente rispetto al metodo EAP stesso. I termini &quot; dati utente &quot; e &quot; credenziali &quot; sono sinonimi.</td>
</tr>
<tr class="odd">
<td>Che cos'è un &quot; attributo EAP &quot; ?</td>
<td>Un &quot; attributo EAP &quot; è una struttura di dati che contiene un tipo di dati predeterminato. Gli attributi vengono utilizzati per comunicare le informazioni tra i metodi EAP e i supplicant o tra i metodi e gli autenticatori EAP. Le implementazioni peer e Authenticator di un metodo EAP possono scambiare questi attributi in una rete.</td>
</tr>
<tr class="even">
<td>È possibile visualizzare l'API di configurazione e l'API di runtime nella stessa DLL del metodo?</td>
<td>Sì. Assicurarsi di specificare la distinzione quando si configurano le voci del registro di sistema per il metodo EAP stesso. Il percorso di configurazione e il percorso peer devono essere uguali.</td>
</tr>
<tr class="odd">
<td>È possibile visualizzare l'API di configurazione e l'API di runtime in dll di metodi separate?</td>
<td>Sì. Assicurarsi di specificare la distinzione quando si configurano le voci del registro di sistema per il metodo EAP stesso. La configurazione e i percorsi peer devono puntare alle DLL corrette.</td>
</tr>
<tr class="even">
<td>Ricerca per categorie installare un metodo EAP?</td>
<td>Per installare un metodo EAP, è necessario implementare prima [<strong>DllRegisterServer</strong>] (/Windows/Win32/API/olectl/NF-olectl-DllRegisterServer) e [<strong>DllUnregisterServer</strong>] (/Windows/Win32/API/olectl/NF-olectl-DllUnregisterServer) nella dll del metodo EAP. Usare quindi <strong>regsvr32.exe</strong> per installare e disinstallare il metodo. È necessario impostare anche le chiavi del registro di sistema appropriate. Per ulteriori informazioni, vedere [installazione di un metodo EAP](installing-an-eap-method.md).<br/></td>
</tr>
<tr class="odd">
<td>Che cos'è il supporto di [Protezione accesso alla rete](/windows/desktop/NAP/network-access-protection-start-page) (NAP) in banda?</td>
<td>Quando è abilitato il supporto di protezione accesso alla rete in banda, i pacchetti NAP vengono trasportati all'interno di pacchetti di metodi EAP. Al contrario, quando è abilitato il supporto di protezione accesso alla rete fuori banda, il [rapporto di integrità di](https://go.microsoft.com/fwlink/p/?linkid=83917) protezione accesso alla rete (SOH) viene eseguito tramite mezzi diversi dai pacchetti del metodo EAP e i certificati generati da NAP vengono usati nell'autenticazione del metodo EAP.</td>
</tr>
<tr class="even">
<td>È possibile abilitare il supporto di protezione accesso alla rete in banda per il metodo EAP?</td>
<td>Sì, è possibile abilitare il supporto di protezione accesso alla rete in banda per il metodo EAP. Per ulteriori informazioni, vedere [Abilitazione del supporto di In-Band NAP per i metodi EAP](enabling-in-band-nap-support.md).</td>
</tr>
<tr class="odd">
<td>Come funziona l'autenticazione flessibile EAP tramite il tunneling sicuro (EAP-FAST)?</td>
<td>Lo scenario EAP-FAST funziona nel modo seguente. <br/>
<ul>
<li>Il metodo elabora una modifica della password in Single Sign-on (SSO) che usa l'interfaccia utente del metodo.</li>
<li>Il metodo restituisce l'attributo [<strong>eatCredentialsChanged</strong>] (/Windows/Desktop/API/eaptypes/ne-eaptypes-eap_attribute_type).</li>
<li>Il supplicant indica all'utente che le credenziali sono state modificate e richiede all'utente di immettere nuovamente le credenziali.</li>
<li>Il richiedente immette nuovamente le credenziali dell'utente e le invia al metodo.</li>
</ul>
Per ulteriori informazioni su EAP-FAST, vedere [autenticazione flessibile EAP tramite il tunneling sicuro](https://go.microsoft.com/fwlink/p/?linkid=84010) (EAP-FAST).</td>
</tr>
<tr class="even">
<td>Che cos'è la chiave precondivisa (PSK)?</td>
<td>Metodo di trasmissione e ricezione di segnali digitali in cui la fase di un segnale trasmesso è variata per trasmettere le informazioni. Il campo di input [<strong>EAPConfigInputPSK</strong>] (/Windows/Desktop/API/eaptypes/ne-eaptypes-eap_config_input_field_type) contiene la PSK di EAP-FAST dell'utente.</td>
</tr>
<tr class="odd">
<td>Che cos'è WOW e in che modo è rilevante per EAPHost?</td>
<td>Microsoft Windows-32-bit-on-Windows-64-bit (WOW) è un componente del sistema operativo in Windows a 64 bit che supporta l'applicazione della piattaforma x86 a 32 bit. In genere, un autore del metodo EAP definisce una forma di struttura C/C++ per incapsulare i dati di configurazione, i dati delle credenziali e i dati interattivi dell'interfaccia utente. Per evitare incompatibilità in WOW e in altri scenari, è importante assicurarsi che le strutture di dati siano allineate in modo analogo in architetture di processori diverse (processori a 32 bit e a 64 bit). In genere, il riempimento fittizio viene usato per allineare i campi in modo che i dati di configurazione, credenziale e interfaccia utente interattiva siano identici nei processori 32 e 64 bit.</td>
</tr>
<tr class="even">
<td>Che cosa sono i &quot; codici &quot; di azione e in quali condizioni vengono restituiti questi codici di azione?</td>
<td>&quot;I codici azione &quot; consentono ai metodi di controllare il flusso di autenticazione e sono parte integrante della macchina a Stati. Si tratta di valori restituiti da un metodo EAP per indicare l'azione successiva che deve essere eseguita da EAPHost. Ad esempio, un codice di azione potrebbe indicare a EAPHost che il metodo EAP dispone di un pacchetto pronto per la trasmissione. Il supplicant rispetta tutti i codici di azione restituiti da un metodo EAP, ma non rilascia mai codici di azione. Per altre informazioni, vedere [codici di azione dei supplicant peer EAP](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction).<br/></td>
</tr>
<tr class="odd">
<td>Quando un metodo restituisce [<strong>EapPeerMethodResponseActionDiscard</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) e cosa significa questo codice di azione per EAPHost?</td>
<td>[<strong>EapPeerMethodResponseActionDiscard</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) viene restituito da un metodo EAP per indicare a EAPHost che deve eliminare il pacchetto fornito al metodo. In particolare, il metodo ha determinato che il pacchetto non è valido. EAPHost attende quindi il pacchetto successivo.</td>
</tr>
<tr class="even">
<td>Quando un metodo restituisce [<strong>EapPeerMethodResponseActionSend</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) e cosa significa questo codice di azione per EAPHost?</td>
<td>[<strong>EapPeerMethodResponseActionSend</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) viene restituito da un metodo EAP per indicare a EAPHost che il pacchetto successivo ricevuto da EAPHost deve essere inviato al server di accesso alla rete (NAS).</td>
</tr>
<tr class="odd">
<td>Quando un metodo restituisce [<strong>EapPeerMethodResponseActionResult</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) e cosa significa questo codice di azione per EAPHost?</td>
<td>[<strong>EapPeerMethodResponseActionResult</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) viene restituito da un metodo EAP per indicare al EAPHost che la sessione di autenticazione è stata conclusa e che i risultati della sessione sono disponibili.</td>
</tr>
<tr class="even">
<td>Quando un metodo restituisce [<strong>EapPeerMethodResponseActionInvokeUI</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) e cosa significa questo codice di azione per EAPHost?</td>
<td>[<strong>EapPeerMethodResponseActionInvokeUI</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) viene restituito da un metodo EAP per indicare a EAPHost che l'input dell'utente è necessario per continuare l'autenticazione e che è necessario visualizzare una finestra di dialogo dell'interfaccia utente per ottenere tale input. Una volta ottenuti i dati di input dell'utente, EAPHost può chiamare di nuovo il metodo EAP con i dati del contesto dell'interfaccia utente aggiornati.</td>
</tr>
<tr class="odd">
<td>Quando un metodo restituisce [<strong>EapPeerMethodResponseActionRespond</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) e cosa significa questo codice di azione per EAPHost?</td>
<td>[<strong>EapPeerMethodResponseActionRespond</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) viene restituito da un metodo EAP per indicare a EAPHost che il metodo EAP dispone di attributi disponibili per EAPHost da utilizzare durante l'autenticazione. EAPHost ottiene gli attributi chiamando il metodo [<strong>EapPeerGetResponseAttributes</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeergetresponseattributes) seguito da una chiamata al metodo [<strong>EapPeerSetResponseAttributes</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeersetresponseattributes).</td>
</tr>
<tr class="even">
<td>Quando un metodo restituisce [<strong>EapPeerMethodResponseActionNone</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) e cosa significa questo codice di azione per EAPHost?</td>
<td>[<strong>EapPeerMethodResponseActionNone</strong>] (/Windows/Win32/API/eapauthenticatoractiondefine/ne-eapauthenticatoractiondefine-eappeermethodresponseaction) viene restituito da un metodo EAP per indicare a EAPHost che al momento non è richiesta alcuna azione.</td>
</tr>
<tr class="odd">
<td>È possibile abilitare la traccia sul lato Authenticator?</td>
<td>Sì. Per ulteriori informazioni, vedere [Abilitazione della traccia](enabling-tracing.md).</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento all'API del metodo peer EAPHost](eap-host-peer-method-api-reference.md)
</dt> <dt>

[Domande frequenti generali su EAPHost](general-frequently-asked-questions.md)
</dt> <dt>

[Domande frequenti sul supplicant EAPHost](eaphost-supplicant-frequently-asked-questions.md)
</dt> <dt>

[Domande frequenti sullo sviluppo di EAPHost](eaphost-development-frequently-asked-questions.md)
</dt> </dl>

 


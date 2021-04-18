---
title: Domande frequenti generali
description: Leggi le risposte alle domande frequenti sulle API EAPHost, ad esempio "Qual è la durata di un'autenticazione?".
ms.assetid: 4025e8da-8cb1-477b-86bb-7756d9636224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eb0dd9b3b997d8682c3cab1ba91afc3ee2db7ba
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/18/2020
ms.locfileid: "106300718"
---
# <a name="general-frequently-asked-questions"></a>Domande frequenti generali

Nell'argomento seguente vengono fornite le risposte alle domande frequenti sulle API EAPHost.

### <a name="general-frequently-asked-questions"></a>Domande frequenti generali



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
<td>Che cos'è un supplicant?</td>
<td>Il supplicant è l'entità da autenticare usando EAPHost. I supplicant tipici sono client [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) , client 802,3 e servizio Routing e accesso remoto (RRAS), client Point-to-Point (PPP).</td>
</tr>
<tr class="even">
<td>Che cos'è un peer?</td>
<td>Il peer è il lato client di un'autenticazione EAP.</td>
</tr>
<tr class="odd">
<td>In che modo un peer è diverso da un supplicant?</td>
<td>Il richiedente trasporta pacchetti, mentre un peer non lo è. Tuttavia, i termini peer, supplicant e client sono in gran parte sinonimi.</td>
</tr>
<tr class="even">
<td>Che cos'è un autenticatore?</td>
<td>L'autenticatore è il punto di accesso wireless, il server di accesso alla rete (NAS) o il dispositivo di accesso alla rete (NAD) che autentica il supplicante. L'autenticatore è noto anche come server EAP.</td>
</tr>
<tr class="odd">
<td>Qual è la durata di un'autenticazione?</td>
<td>Il ciclo di vita di una singola sessione di autenticazione sul lato client è tutto ciò che si verifica tra le funzioni [<strong>EapHostPeerBeginSession</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession) e [<strong>EapHostPeerEndSession</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerendsession) chiamate. La durata sul lato Authenticator è tutto ciò che si verifica tra le funzioni [<strong>EapPeerBeginSession</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeerbeginsession) e [<strong>EapPeerEndSession</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeerendsession).</td>
</tr>
<tr class="even">
<td>Che cos'è un BLOB? Perché convertire un BLOB di configurazione (binario) in XML?</td>
<td>Un BLOB è un oggetto binario di grandi dimensioni. XML presenta diversi vantaggi rispetto a un BLOB di configurazione binaria. I dati di configurazione archiviati in XML sono leggibili, modificabili in formato umano e multipiattaforma.</td>
</tr>
<tr class="odd">
<td>Quando si converte un BLOB XML archiviato in un BLOB binario?</td>
<td>È possibile archiviare un BLOB binario o XML, ma è sempre necessario convertire di nuovo il BLOB XML in un BLOB binario prima di usarlo con le API di Runtime. le API di runtime non accettano una directory XML.</td>
</tr>
<tr class="even">
<td>Che cosa sono i metodi nativi?</td>
<td>I metodi EAP nativi usano la nuova API EAPHost.</td>
</tr>
<tr class="odd">
<td>Che cosa sono i metodi legacy?</td>
<td>I metodi EAP legacy sono definiti nella Guida di [riferimento al protocollo Extensible Authentication](/previous-versions/windows/desktop/eap/extensible-authentication-protocol-reference). I metodi EAP legacy sono disponibili per l'utilizzo in Windows Vista e Windows Server 2008. Questi metodi potrebbero non essere disponibili per l'utilizzo nelle versioni successive del sistema operativo.</td>
</tr>
<tr class="even">
<td>Qual è la differenza tra i metodi legacy e native?</td>
<td>Le API native sono più semplici e presentano meno funzionalità. Tutti i nuovi metodi EAP devono essere scritti usando l'API EAPHost.</td>
</tr>
<tr class="odd">
<td>Che cosa sono i &quot; criteri di gruppo &quot; ?</td>
<td>Per una descrizione dei criteri di gruppo, vedere [criteri di gruppo Collection](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)).</td>
</tr>
<tr class="even">
<td>Le funzioni EAPHost possono eseguire l'override dei criteri di configurazione specificati da criteri di gruppo?</td>
<td>No, mai. Se criteri di gruppo è in uso, le impostazioni di criteri di gruppo eseguiranno sempre l'override delle impostazioni di configurazione EAPHost.</td>
</tr>
<tr class="odd">
<td>Che cos'è Single Sign-on (SSO)?</td>
<td>[802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) è un meccanismo di autenticazione di livello 2. A seconda della configurazione SSO, SSO consente agli utenti di eseguire l'autenticazione alla rete utilizzando l'autenticazione [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) prima o immediatamente dopo l'accesso a Windows. SSO può essere configurato in modo da utilizzare le credenziali di Windows per l'autenticazione di rete (in tal caso, gli utenti immettono le credenziali una sola volta) o utilizzano credenziali diverse per Windows e l'autenticazione di rete. Per ulteriori informazioni, vedere [SSO e PLAP](understanding-sso-and-plap.md).<br/></td>
</tr>
<tr class="even">
<td>Informazioni sul provider di accesso con pre-accesso (PLAP)</td>
<td>Per ulteriori informazioni, vedere [SSO e PLAP](understanding-sso-and-plap.md).</td>
</tr>
<tr class="odd">
<td>Che cos'è PEAP (Protected Extensible Authentication Protocol)?</td>
<td>Per ulteriori informazioni, vedere [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)) e [informazioni sul protocollo di autenticazione estendibile](/previous-versions/windows/desktop/eap/about-extensible-authentication-protocol).</td>
</tr>
<tr class="even">
<td>In che modo PEAP affronta la ripresa della sessione e la nuova autenticazione?</td>
<td>Il ripristino e la riautenticazione della sessione si verificano in genere durante il roaming su una rete wireless. Windows Data Protection API (DPAPI) fornisce un modo per proteggere e associare dati a un utente e, facoltativamente, alla sessione di accesso. Il chiamante assegna a [<strong>CryptProtectMemory</strong>] (/Windows/Desktop/API/DPAPI/NF-DPAPI-cryptprotectmemory) un buffer non crittografato e DPAPI crittografa la memoria sul posto. In un secondo momento, il chiamante può passare il buffer crittografato a [<strong>CryptUnprotectMemory</strong>] (/Windows/Desktop/API/DPAPI/NF-DPAPI-cryptunprotectmemory) e DPAPI decrittografare la memoria, ancora una volta sul posto. Per ulteriori informazioni, vedere [estensione dell'applicazione TLS interna (TSL/IA)](https://go.microsoft.com/fwlink/p/?linkid=84011) e [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).<br/></td>
</tr>
<tr class="odd">
<td>Che cos'è la sicurezza a livello di EAP-Transport (EAP-TLS)?</td>
<td>EAP-TLS è un protocollo client-server in cui i profili certificato distinti vengono in genere usati per il client e il server. Per ulteriori informazioni, vedere [IETF RTC 2716](/previous-versions/windows/embedded/ms885336(v=msdn.10)).<br/></td>
</tr>
<tr class="even">
<td>Ricerca per categorie implementare una modifica della password con l'API dell'autorità di protezione locale (LSA)?</td>
<td>Usare la funzione [<strong>LsaCallAuthenticationPackage</strong>] (/Windows/Desktop/API/ntsecapi/NF-ntsecapi-LsaCallAuthenticationPackage) per implementare una modifica della password.</td>
</tr>
<tr class="odd">
<td>Perché si vuole abilitare la traccia in EAPHost?</td>
<td>I log di traccia contengono informazioni di debug (disponibili solo in inglese) che possono aiutare gli sviluppatori e i partner Microsoft a trovare le cause principali di eventuali problemi riscontrati durante il processo di autenticazione. Per ulteriori informazioni, vedere [Abilitazione della traccia](enabling-tracing.md).<br/></td>
</tr>
<tr class="even">
<td>Perché si verifica il codice di errore NTE_BAD_KEY_STATE (0x8009000BL) quando si usa l'API di [crittografia](/windows/desktop/SecCrypto/cryptography-portal) per accedere allo scambio EAP-TLS?</td>
<td>In Winerror. h NTE_BAD_KEY_STATE (0x8009000BL) è definito come &quot; chiave non valida per l'utilizzo nello stato specificato &quot; . Questo errore viene in genere restituito negli scenari seguenti.
<ul>
<li>Quando si tenta di esportare un BLOB di chiave privata non esportabile</li>
<li>Quando si tenta di generare un handle di hash PRF (pseudo-random Function) utilizzando [<strong>CryptCreateHash</strong>] (/Windows/Desktop/API/Wincrypt/NF-Wincrypt-CryptCreateHash).</li>
</ul>
Per ulteriori informazioni, vedere la pagina relativa alla [fine dei messaggi nel protocollo TLS 1,0](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).</td>
</tr>
<tr class="odd">
<td>Che cos'è una funzione pseudo-casuale (PRF)?</td>
<td>Funzione che accetta una chiave, un'etichetta e un valore di inizializzazione come input, quindi produce un output di lunghezza arbitraria. Per ulteriori informazioni, vedere la pagina relativa alla [fine dei messaggi nel protocollo TLS 1,0](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).<br/></td>
</tr>
<tr class="even">
<td>Come è possibile associare EAPHost alle schede di rete?</td>
<td>EAPHost consente il funzionamento simultaneo di più supplicant e ogni supplicant può essere associato a più schede di rete. I supplicant EAPHost forniscono il binding ai livelli di rete e guidano il processo di autenticazione. I supplicant contengono la configurazione dell'autenticazione. I supplicant salvano inoltre lo stato e forniscono la successiva sicurezza della connessione. Poiché EAPHost non è associato direttamente ad alcun meccanismo di rete, l'estendibilità dei supplicant è possibile.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Domande frequenti sul supplicant EAPHost](eaphost-supplicant-frequently-asked-questions.md)
</dt> <dt>

[Domande frequenti sul metodo EAPHost](eap-method-frequently-asked-questions.md)
</dt> <dt>

[Domande frequenti sullo sviluppo di EAPHost](eaphost-development-frequently-asked-questions.md)
</dt> </dl>


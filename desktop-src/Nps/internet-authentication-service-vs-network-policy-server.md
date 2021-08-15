---
title: Servizio di autenticazione Internet & Server dei criteri di rete
description: Informazioni sul servizio di autenticazione Internet e sul server dei criteri di rete. Il servizio di autenticazione Internet (IAS) è stato rinominato Server dei criteri di rete.
ms.assetid: c7c6d1a3-d0c8-469e-ae1e-a848ef7fee2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f46e4052b2c7277f49f898a290d689928b5838c0562042c0ba8937c5daf00210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118362317"
---
# <a name="internet-authentication-service--network-policy-server"></a>Servizio di autenticazione Internet & Server dei criteri di rete

Il servizio di autenticazione Internet (IAS) è stato rinominato Server dei criteri di rete.

## <a name="internet-authentication-service"></a>Servizio di autenticazione Internet

Il servizio di autenticazione Internet è l'implementazione Microsoft di un server RADIUS e di un proxy.

Il servizio di autenticazione Internet supporta due set di API: [l'API delle estensioni del server dei](ias-extensions.md) criteri di rete e l'API oggetti dati del [server](server-data-objects.md).

Per altre informazioni su IAS, vedere [TechNet: Servizio](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) di autenticazione Internet.

## <a name="network-policy-server"></a>Server dei criteri di rete

Server dei criteri di rete è l'implementazione Microsoft di un server e proxy RADIUS ed è disponibile nei server Windows a partire da Windows Server 2008.

Server dei criteri di rete supporta gli stessi due set di API di IAS: [l'API delle](ias-extensions.md) estensioni del server dei criteri di rete e l'API oggetti dati del [server](server-data-objects.md).

Server dei criteri di rete contiene anche un set di nuove funzionalità che espandono le funzionalità IAS.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funzionalità</th>
<th>Novità di Server dei criteri di rete</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/NAP/network-access-protection-start-page">Protezione accesso alla rete (NAP)</a><br/></td>
<td>Server dei criteri di rete è il server centrale di Protezione accesso alla rete.<br/> Server dei criteri di rete supporta la creazione di criteri utilizzando le condizioni aggiuntive seguenti:<br/>
<ul>
<li>Scadenza dei criteri.</li>
<li>Versione del sistema operativo.</li>
<li>Accedere all'indirizzo IP del client.</li>
<li>Criteri di integrità.</li>
<li>Tipi EAP consentiti.</li>
<li>Hcap.</li>
</ul>
Server dei criteri di rete supporta la creazione di criteri usando le impostazioni aggiuntive seguenti:<br/>
<ul>
<li>Prova.</li>
<li>Accesso limitato.</li>
<li>Stato esteso per accesso limitato.</li>
</ul>
Server dei criteri di rete, tramite Protezione accesso alla rete, interagisce con CISCO NAC.<br/> IAS non supporta Protezione accesso alla rete.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/eap/eap-start-page">EAP</a> Supporto di <a href="/windows/win32/eaphost/portal">criteri ed EAPHost</a><br/></td>
<td>Server dei criteri di rete usa EAPHost per l'estendibilità dei metodi EAP. Inoltre, gli amministratori possono configurare i criteri di accesso alla rete per EAP.<br/> IAS non supporta l'integrazione EAPHost o le condizioni di filtro del tipo EAP per i criteri.<br/></td>
</tr>
<tr class="odd">
<td>Supporto IPv6<br/></td>
<td>Server dei criteri di rete supporta la distribuzione in ambienti IPv6.<br/> IAS non supporta gli indirizzi di rete IPv6.<br/></td>
</tr>
<tr class="even">
<td>Configurazione XML<br/></td>
<td>La configurazione di Server dei criteri di rete può essere importata ed esportata in formato XML.<br/> IAS usa un database Jet per archiviare la configurazione del servizio.<br/></td>
</tr>
<tr class="odd">
<td><a href="https://www.niap-ccevs.org/cc-scheme/">Criteri comuni</a> Supporto<br/></td>
<td>Server dei criteri di rete è stato aggiornato per supportare la distribuzione in ambienti che devono soddisfare gli standard di sicurezza dei criteri comuni.<br/></td>
</tr>
<tr class="even">
<td><a href="ias-extensions.md">NPS Extensions API</a><br/></td>
<td>Le DLL dell'estensione NPS vengono eseguite in un processo separato dal servizio Server dei criteri di rete. In caso di arresto anomalo della DLL di estensione, Server dei criteri di rete continuerà a essere in esecuzione e le richieste future verranno rifiutate.<br/> Le DLL di estensione IAS vengono eseguite nello stesso processo del servizio IAS e possono influire negativamente sul servizio.<br/></td>
</tr>
<tr class="odd">
<td>Gestione Interfaccia utente<br/></td>
<td>La console di gestione server dei criteri di rete (nps.msc) ha un nuovo aspetto, usabilità migliorata e copre tutte le nuove funzionalità aggiunte a Server dei criteri di rete.<br/> IAS usa la console di gestione ias.msc.<br/></td>
</tr>
<tr class="even">
<td>Strumento di gestione dei ruoli e integrazione Server Manager ruoli<br/></td>
<td>Server dei criteri di rete è integrato con Server Manager e lo strumento di gestione dei ruoli. Questa integrazione facilita la configurazione e la gestione di Server dei criteri di rete e degli scenari correlati.<br/> Server Manager non è disponibile nei computer che eseguono IAS.<br/></td>
</tr>
<tr class="odd">
<td>Aggiornamento dello scripting della riga di comando <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)">con Netsh</a>.<br/></td>
<td>Server dei criteri di rete supporta &quot; l'interfaccia della riga di comando netsh nps. &quot; &quot;Netsh nps contiene nuovi comandi che consentono di configurare completamente Server dei criteri di &quot; rete, incluse le funzionalità di Protezione accesso alla rete.<br/> IAS supporta l'interfaccia della riga di comando &quot; Netsh aaaa. &quot;<br/></td>
</tr>
<tr class="even">
<td>Isolamento dei criteri<br/></td>
<td>Server dei criteri di rete consente l'implementazione dell'isolamento dei criteri impostando l'origine dei criteri di rete. È possibile configurare criteri applicabili solo a un tipo NAS predeterminato.<br/> IAS non supporta l'isolamento dei criteri.<br/></td>
</tr>
</tbody>
</table>



 

Per altre informazioni su Server dei criteri di rete, vedere [TechNet: Server](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) dei criteri di rete.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Autenticazione, autorizzazione e accounting RADIUS](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[Registrazione con server dei criteri di rete](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[Utilizzo di un server di stato](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>


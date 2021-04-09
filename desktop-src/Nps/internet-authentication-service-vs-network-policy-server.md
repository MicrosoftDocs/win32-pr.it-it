---
title: Servizio di autenticazione Internet & server dei criteri di rete
description: Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS).
ms.assetid: c7c6d1a3-d0c8-469e-ae1e-a848ef7fee2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca657da17e823caa51e8401905a8a0a3e307e975
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "104047511"
---
# <a name="internet-authentication-service--network-policy-server"></a>Servizio di autenticazione Internet & server dei criteri di rete

Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS).

## <a name="internet-authentication-service"></a>Servizio di autenticazione Internet

Il servizio di autenticazione Internet è l'implementazione Microsoft di un server e un proxy RADIUS.

Il servizio di autenticazione Internet supporta due set di API: API per le [estensioni server dei criteri di rete](ias-extensions.md) e [API oggetti dati server](server-data-objects.md).

Per ulteriori informazioni su IAS, vedere [TechNet: servizio di autenticazione Internet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) .

## <a name="network-policy-server"></a>Server dei criteri di rete

Server dei criteri di rete è l'implementazione Microsoft di un server e un proxy RADIUS ed è disponibile nei server Windows a partire da Windows Server 2008.

Server dei criteri di rete supporta gli stessi due set di API IAS: API per le [estensioni del server dei criteri di rete](ias-extensions.md) e API per [oggetti dati del server](server-data-objects.md)

Server dei criteri di gruppo contiene inoltre un set di nuove funzionalità che espandono le funzionalità IAS.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funzionalità</th>
<th>Novità per NPS</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/NAP/network-access-protection-start-page">Protezione accesso alla rete (NAP)</a><br/></td>
<td>NPS è il server centrale di protezione accesso alla rete.<br/> NPS supporta la creazione di criteri utilizzando le condizioni aggiuntive seguenti:<br/>
<ul>
<li>Scadenza dei criteri.</li>
<li>Versione del sistema operativo.</li>
<li>Accedere all'indirizzo IP del client.</li>
<li>Criteri di integrità.</li>
<li>Tipi EAP consentiti.</li>
<li>HCAP.</li>
</ul>
NPS supporta la creazione di criteri usando le seguenti impostazioni aggiuntive:<br/>
<ul>
<li>Prova.</li>
<li>Accesso limitato.</li>
<li>Stato esteso per accesso limitato.</li>
</ul>
Server dei criteri di rete, tramite NAP, interagisce con CISCO NAC.<br/> IAS non supporta NAP.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/eap/eap-start-page">EAP</a> Criteri e supporto <a href="/windows/win32/eaphost/portal">EAPHost</a><br/></td>
<td>NPS USA EAPHost per l'estendibilità del metodo EAP. Inoltre, gli amministratori possono configurare i criteri di accesso alla rete per EAP.<br/> IAS non supporta l'integrazione EAPHost o le condizioni di filtro del tipo EAP per i criteri.<br/></td>
</tr>
<tr class="odd">
<td>Supporto IPv6<br/></td>
<td>NPS supporta la distribuzione in ambienti IPv6.<br/> IAS non supporta indirizzi di rete IPv6.<br/></td>
</tr>
<tr class="even">
<td>Configurazione XML<br/></td>
<td>La configurazione NPS può essere importata ed esportata in formato XML.<br/> IAS utilizza un database Jet per l'archiviazione della configurazione del servizio.<br/></td>
</tr>
<tr class="odd">
<td><a href="https://www.niap-ccevs.org/cc-scheme/">Criteri comuni</a> Supporto<br/></td>
<td>NPS è stato aggiornato per supportare la distribuzione in ambienti che devono soddisfare gli standard di sicurezza dei criteri comuni.<br/></td>
</tr>
<tr class="even">
<td><a href="ias-extensions.md">API delle estensioni NPS</a><br/></td>
<td>Le DLL di estensione NPS vengono eseguite in un processo separato dal servizio NPS. In caso di arresto anomalo di una DLL di estensione, NPS continuerà a funzionare e le richieste future verranno rifiutate.<br/> Le DLL di estensione IAS vengono eseguite nello stesso processo del servizio IAS e possono influire negativamente sul servizio.<br/></td>
</tr>
<tr class="odd">
<td>Interfaccia utente di gestione<br/></td>
<td>La console di gestione NPS (NPS. msc) ha un nuovo aspetto, una migliore usabilità e tutte le nuove funzionalità aggiunte al server dei criteri di server.<br/> IAS utilizza la console di gestione IAS. msc.<br/></td>
</tr>
<tr class="even">
<td>Strumento di gestione dei ruoli e integrazione Server Manager<br/></td>
<td>NPS è integrato con il Server Manager e lo strumento di gestione dei ruoli. Questa integrazione semplifica la configurazione e la gestione di NPS e di scenari correlati.<br/> Server Manager non è disponibile nei computer che eseguono IAS.<br/></td>
</tr>
<tr class="odd">
<td>Aggiornamento dello script della riga di comando con <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)">netsh</a>.<br/></td>
<td>NPS supporta l' &quot; interfaccia della &quot; riga di comando netsh NPS. &quot;Netsh NPS &quot; contiene nuovi comandi che consentono di configurare completamente NPS, incluse le funzionalità di protezione accesso alla rete.<br/> IAS supporta l' &quot; interfaccia della &quot; riga di comando netsh aaaa.<br/></td>
</tr>
<tr class="even">
<td>Isolamento dei criteri<br/></td>
<td>NPS consente l'implementazione dell'isolamento dei criteri impostando l'origine dei criteri di rete. È possibile configurare i criteri che sono applicabili solo a un tipo NAS predeterminato.<br/> IAS non supporta l'isolamento dei criteri.<br/></td>
</tr>
</tbody>
</table>



 

Per ulteriori informazioni su NPS, vedere [TechNet: Server dei criteri di rete](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Autenticazione, autorizzazione e accounting RADIUS](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[Registrazione con server dei criteri di rete](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[Utilizzo di un server di stato](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>


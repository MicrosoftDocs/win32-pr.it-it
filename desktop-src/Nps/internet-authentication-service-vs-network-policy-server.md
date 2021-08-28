---
title: Servizio di autenticazione Internet & Server dei criteri di rete
description: Informazioni sul servizio di autenticazione Internet e sul server dei criteri di rete. Il servizio Autenticazione Internet (IAS) è stato rinominato Server dei criteri di rete.
ms.assetid: c7c6d1a3-d0c8-469e-ae1e-a848ef7fee2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36751c66b525749afce0d5546f61fa35c1cbb856
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122483047"
---
# <a name="internet-authentication-service--network-policy-server"></a>Servizio di autenticazione Internet & Server dei criteri di rete

Il servizio Autenticazione Internet (IAS) è stato rinominato Server dei criteri di rete.

## <a name="internet-authentication-service"></a>Servizio di autenticazione Internet

Il servizio di autenticazione Internet è l'implementazione Microsoft di un server RADIUS e di un proxy.

Il servizio di autenticazione Internet supporta due set di API: [l'API Estensioni del server di](ias-extensions.md) Criteri di rete e l'API Oggetti dati del [server](server-data-objects.md).

Per altre informazioni su IAS, vedere [TechNet: Servizio](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) di autenticazione Internet.

## <a name="network-policy-server"></a>Server dei criteri di rete

Server dei criteri di rete è l'implementazione Microsoft di un server RADIUS e di un proxy ed è disponibile Windows server a partire da Windows Server 2008.

Server dei criteri di rete supporta gli stessi due set di API di IAS: API estensioni [del server](ias-extensions.md) di Criteri di rete e API Oggetti dati [server](server-data-objects.md).

Inoltre, Server dei criteri di rete contiene un set di nuove funzionalità che espandono le funzionalità IAS.




| Funzionalità | Novità di Server dei criteri di rete | 
|---------|--------------------|
| <a href="/windows/desktop/NAP/network-access-protection-start-page">Protezione accesso alla rete (NAP)</a><br /> | Server dei criteri di rete è il server centrale di Protezione accesso alla rete.<br /> Server dei criteri di rete supporta la creazione di criteri usando le condizioni aggiuntive seguenti:<br /><ul><li>Scadenza dei criteri.</li><li>Versione del sistema operativo.</li><li>Accedere all'indirizzo IP del client.</li><li>Criteri di integrità.</li><li>Tipi EAP consentiti.</li><li>HCAP.</li></ul>Server dei criteri di rete supporta la creazione di criteri usando le impostazioni aggiuntive seguenti:<br /><ul><li>Prova.</li><li>Accesso limitato.</li><li>Stato esteso per l'accesso limitato.</li></ul>Server dei criteri di rete, tramite Protezione accesso alla rete, interagisce con CISCO NAC.<br /> IAS non supporta Protezione accesso alla rete.<br /> | 
| <a href="/windows/win32/eap/eap-start-page">EAP</a> Criteri ed <a href="/windows/win32/eaphost/portal">EAPHost</a> Support<br /> | Server dei criteri di rete usa EAPHost per l'estendibilità del metodo EAP. Inoltre, gli amministratori possono configurare i criteri di accesso alla rete per EAP.<br /> IAS non supporta l'integrazione EAPHost o le condizioni di filtro del tipo EAP per i criteri.<br /> | 
| Supporto IPv6<br /> | Server dei criteri di rete supporta la distribuzione in ambienti IPv6.<br /> IAS non supporta gli indirizzi di rete IPv6.<br /> | 
| Configurazione XML<br /> | La configurazione di Server dei criteri di rete può essere importata ed esportata in formato XML.<br /> IAS usa un database Jet per archiviare la configurazione del servizio.<br /> | 
| <a href="https://www.niap-ccevs.org/cc-scheme/">Criteri comuni</a> Supporto<br /> | Server dei criteri di rete è stato aggiornato per supportare la distribuzione in ambienti che devono soddisfare gli standard di sicurezza di Criteri comuni.<br /> | 
| <a href="ias-extensions.md">API Estensioni Server dei criteri di rete</a><br /> | Le DLL dell'estensione NPS vengono eseguite in un processo separato dal servizio Server dei criteri di rete. In caso di arresto anomalo della DLL di estensione, Server dei criteri di rete continuerà a essere in esecuzione e le richieste future verranno rifiutate.<br /> Le DLL di estensione IAS vengono eseguite nello stesso processo del servizio IAS e possono influire negativamente sul servizio.<br /> | 
| Gestione Interfaccia utente<br /> | La console di gestione di Server dei criteri di rete (nps.msc) ha un nuovo aspetto, un'usabilità migliorata e copre tutte le nuove funzionalità aggiunte a Server dei criteri di rete.<br /> IAS usa la console di gestione ias.msc.<br /> | 
| Strumento di gestione dei ruoli e integrazione Server Manager ruoli<br /> | Server dei criteri di rete è integrato con il Server Manager e lo strumento di gestione dei ruoli. Questa integrazione facilita la configurazione e la gestione dei server dei criteri di rete e degli scenari correlati.<br /> Server Manager non è disponibile nei computer che eseguono IAS.<br /> | 
| Aggiornamento dello scripting della riga di comando <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)">con Netsh</a>.<br /> | Server dei criteri di rete supporta l'interfaccia della riga di comando "Netsh nps". "Netsh nps" contiene nuovi comandi che consentono di configurare completamente server dei criteri di rete, incluse le funzionalità di Protezione accesso alla rete.<br /> IAS supporta l'interfaccia della riga di comando "Netsh aaaa".<br /> | 
| Isolamento dei criteri<br /> | Server dei criteri di rete consente l'implementazione dell'isolamento dei criteri impostando l'origine dei criteri di rete. È possibile configurare criteri applicabili solo a un tipo NAS predeterminato.<br /> IAS non supporta l'isolamento dei criteri.<br /> | 




 

Per altre informazioni su Server dei criteri di rete, vedere [TechNet: Server](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) dei criteri di rete.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Autenticazione, autorizzazione e accounting RADIUS](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[Registrazione con il server dei criteri di rete](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[Uso di un server di stato](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>


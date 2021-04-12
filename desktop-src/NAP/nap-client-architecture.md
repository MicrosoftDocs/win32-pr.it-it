---
title: Architettura client NAP
description: Un client di protezione accesso alla rete è un computer che esegue Windows XP con Service Pack 3 (SP3), Windows Vista o Windows Server 2008 che include la piattaforma NAP.
ms.assetid: 163c33c9-b18b-49f9-a2a1-fd90a1dc0826
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15862eaa6ae4f4c1f79c53cf9d540aedec295e8a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331900"
---
# <a name="nap-client-architecture"></a>Architettura client NAP

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Un client di protezione accesso alla rete è un computer che esegue Windows XP con Service Pack 3 (SP3), Windows Vista o Windows Server 2008 che include la piattaforma NAP.

In questa figura viene illustrata l'architettura della piattaforma NAP in un client di protezione accesso alla rete.

![architettura della piattaforma NAP in un client di protezione accesso alla rete](images/nap-client-side-arch.png)

L'architettura client di protezione accesso alla rete è costituita dagli elementi seguenti:

-   Un livello di componenti del client di imposizione (EC)

    Ogni sistema di protezione accesso alla rete è definito per un tipo diverso di accesso alla rete. È ad esempio disponibile una protezione accesso alla rete (NAP) per la configurazione DHCP e una protezione accesso alla rete EC per le connessioni VPN di accesso remoto. È possibile trovare la corrispondenza di NAP EC con un tipo specifico di punto di imposizione NAP. Ad esempio, la protezione accesso alla rete DHCP è progettata per funzionare con un punto di imposizione di protezione accesso alla rete basato su DHCP. Alcune funzionalità di protezione accesso alla rete sono fornite con la piattaforma NAP e i fornitori di software di terze parti oppure Microsoft possono fornire altri utenti.

-   Un livello di componenti dell'agente integrità sistema (SHA)

    Un componente SHA mantiene e segnala uno o più elementi di integrità del sistema. Ad esempio, potrebbe essere presente un SHA per le firme antivirus e un SHA per gli aggiornamenti del sistema operativo. Un SHA può essere associato a un server di monitoraggio e aggiornamento, ovvero un computer che contiene le risorse di aggiornamento dell'integrità ai quali i client di protezione accesso alla rete possono accedere per correggere lo stato non conforme. Ad esempio, un SHA per la verifica delle firme antivirus viene associato al server che contiene il file della firma antivirus più recente. Non è necessario che SHAs disponga di un server di monitoraggio e aggiornamento corrispondente. Ad esempio, un SHA può verificare solo le impostazioni di sistema locale per assicurarsi che sia abilitato un firewall basato su host. Windows Vista e Windows XP Service Pack 3 includono il Agente integrità protezione di Windows (Agente integrità sicurezza) che monitora le impostazioni del Centro sicurezza PC Windows. I fornitori di software di terze parti o Microsoft possono fornire SHAs aggiuntive alla piattaforma NAP.

-   Agente NAP

    Mantiene le informazioni sullo stato di integrità corrente del client di protezione accesso alla rete e facilita la comunicazione tra i livelli di protezione accesso alla rete EC e SHA. L'agente NAP viene fornito con la piattaforma NAP.

-   API dell'agente integrità sistema

    Fornisce un set di funzioni che consentono la registrazione di SHAs con l'agente NAP, per indicare lo stato di integrità del sistema, rispondere alle query per lo stato di integrità del sistema dall'agente NAP e affinché l'agente NAP passi le informazioni di monitoraggio e aggiornamento dell'integrità del sistema a un SHA. L'API SHA consente ai fornitori di creare e installare SHAs aggiuntive. L'API SHA viene fornita con la piattaforma NAP. Vedere le interfacce NAP seguenti: [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md), [**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)e [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md).

Per indicare lo stato di integrità di un SHA specifico, un SHA crea un rapporto [**di integrità e**](/windows/win32/api/naptypes/ns-naptypes-soh)lo passa all'agente NAP. Un rapporto di integrità può contenere uno o più elementi di integrità del sistema. Ad esempio, l'SHA per un programma antivirus può creare un rapporto di integrità contenente lo stato del software antivirus in esecuzione nel computer, la versione e l'ultimo aggiornamento della firma antivirus ricevuto. Ogni volta che un SHA aggiorna il proprio stato, viene creato un nuovo rapporto di integrità e passato all'agente NAP. Per indicare lo stato di integrità generale di un client di protezione accesso alla rete, l'agente protezione accesso alla rete utilizza un rapporto di integrità del sistema (SSoH), che include le informazioni sulla versione per il client di protezione accesso alla rete e il set di invieranno per il SHAs installato.

Le sezioni seguenti descrivono in modo dettagliato i componenti dell'architettura client di protezione accesso alla rete.

## <a name="nap-enforcement-client"></a>Client di imposizione Protezione accesso alla rete

Un client di imposizione di protezione accesso alla rete richiede un certo livello di accesso a una rete, passa lo stato di integrità del computer a un punto di imposizione di protezione accesso alla rete che fornisce l'accesso alla rete. I punti di imposizione di protezione accesso alla rete sono computer o dispositivi di accesso alla rete che utilizzano NAP oppure possono essere utilizzati con protezione accesso alla rete per richiedere la valutazione dello stato di integrità di un client di protezione accesso alla rete e la comunicazione con restrizioni. Se l'integrità del computer non è conforme, NAP EC indica lo stato limitato del client di protezione accesso alla rete per altri componenti dell'architettura client di protezione accesso alla rete.

NAP ECs per la piattaforma NAP fornita in Windows XP con SP3, Windows Vista e Windows Server 2008 è il seguente:

-   Protezione accesso alla rete IPsec per le comunicazioni protette da IPsec.
-   Rete di protezione accesso alla rete (NAP) EAPHost per le connessioni autenticate con 802.1 X.
-   Protezione accesso alla rete VPN per le connessioni VPN di accesso remoto.
-   Una protezione accesso alla rete DHCP per la configurazione degli indirizzi IPv4 basata su DHCP.
-   Un gateway di protezione accesso alla rete gateway di Servizi terminal per le connessioni gateway Servizi terminal

Per Windows XP con SP3, sono disponibili NAP ECs per le connessioni cablate e wireless autenticate tramite 802.1 X.

### <a name="ipsec-nap-ec"></a>Protezione accesso alla rete IPsec

Protezione accesso alla rete IPsec è un componente che ottiene il SSoH dall'agente protezione accesso alla rete e lo invia a un'Autorità registrazione integrità, un computer che esegue Windows Server 2008 e Internet Information Services (IIS) che ottiene i certificati di integrità da un'autorità di certificazione (CA) per i computer conformi. La protezione accesso alla rete IPsec è nota come EC relying party IPsec nello snap-in configurazione client di protezione accesso alla rete. Inoltre, la protezione accesso alla rete IPsec interagisce con quanto segue:

-   Archivio certificati in cui archiviare il certificato di integrità.
-   Componenti IPsec di Windows per garantire che il certificato di integrità venga utilizzato per le comunicazioni protette da IPsec.
-   Il firewall basato su host, ad esempio Windows Firewall, in modo che il traffico protetto da IPsec sia consentito dal firewall.

### <a name="eaphost-nap-ec"></a>NAP NAP EC

EAPHost NAP è un componente che ottiene il SSoH dall'agente NAP e lo invia come messaggio PEAP-Type-Length-Value (TLV) per le connessioni autenticate tramite 802.1 X. Il protocollo di protezione accesso alla rete EAPHost è noto come la quarantena EAP EC nello snap-in configurazione client di protezione accesso alla rete.

### <a name="vpn-nap-ec"></a>PROTEZIONE ACCESSO ALLA RETE VPN EC

La protezione accesso alla rete VPN è una funzionalità nel servizio gestione connessione di accesso remoto che ottiene il SSoH dall'agente protezione accesso alla rete e lo invia come messaggio PEAP-TLV per le connessioni VPN di accesso remoto. La protezione accesso alla rete VPN è nota come quarantena di accesso remoto EC nello snap-in configurazione client di protezione accesso alla rete.

### <a name="dhcp-nap-ec"></a>PROTEZIONE ACCESSO ALLA RETE DHCP

La protezione accesso alla rete DHCP è una funzionalità del servizio client DHCP che utilizza messaggi DHCP standard del settore per scambiare messaggi di integrità del sistema e informazioni limitate sull'accesso alla rete. Il protocollo EC DHCP IPsec è noto come "quarantena DHCP" nello snap-in configurazione client di protezione accesso alla rete. Il SSoH di protezione accesso alla rete DHCP consente di ottenere l'agente protezione accesso alla rete. Il servizio client DHCP frammenta la SSoH, se necessario, e inserisce ogni frammento in un'opzione DHCP specifica del fornitore Microsoft che viene inviata nei messaggi DHCPDiscover, DHCPRequest o DHCPInform. I messaggi DHCPDecline e DHCPRelease non contengono SSoH.

## <a name="system-health-agent"></a>Agente integrità sistema

Un agente integrità sistema esegue gli aggiornamenti dell'integrità del sistema e ne pubblica lo stato sotto forma di rapporto di integrità con l'agente NAP. Il rapporto di integrità contiene informazioni che possono essere utilizzate dal server criteri di integrità protezione accesso alla rete per verificare che il computer client sia nello stato di integrità richiesto. Un servizio di convalida dell'integrità di sistema è associato a un servizio di convalida dell'integrità di sistema sul lato server dell'architettura della piattaforma NAP. Il servizio di convalida dell'integrità di sistema corrispondente può restituire una risposta a rapporto di integrità (SoHR) al client di protezione accesso alla rete, che viene passato dall'agente di protezione accesso alla rete e dall'agente NAP al servizio SHA, indicando le operazioni da eseguire se SHA non è in uno stato di integrità obbligatorio. Ad esempio, il SoHR inviato da un servizio di convalida dell'integrità del sistema antivirus potrebbe indicare all'SHA del virus corrispondente di eseguire una query su un server di firma antivirus per ottenere la versione più recente del file di firma antivirus. Il SoHR può includere anche il nome o l'indirizzo IP del server di firma antivirus su cui eseguire una query.

Un SHA può utilizzare un client di criteri installato localmente per supportare le funzioni di gestione dell'integrità del sistema insieme a un server dei criteri. Ad esempio, un aggiornamento software SHA può usare il software client del software installato localmente (il client dei criteri) per eseguire il controllo della versione e le funzioni di installazione e aggiornamento con il server di aggiornamento software (il server dei criteri).

## <a name="nap-agent"></a>Agente NAP

L'agente NAP fornisce i servizi seguenti:

-   Raccoglie i invieranno da ogni SHA e li memorizza nella cache. La cache del rapporto di integrità viene aggiornata ogni volta che un oggetto SHA fornisce un rapporto di integrità nuovo o aggiornato.
-   Archivia il SSoH e lo fornisce a NAP ECs su richiesta.
-   Passa le notifiche a SHAs quando viene modificato lo stato con restrizioni.
-   Mantiene lo stato con restrizioni del sistema e raccoglie informazioni sullo stato da ogni SHA.
-   Passa SoHRs all'oggetto SHA appropriato.

 

 





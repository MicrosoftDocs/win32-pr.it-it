---
title: Architettura lato server NAP
description: Architettura lato server NAP
ms.assetid: b05c52d5-1f90-41d4-a540-d20e70e54bcb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dac585d3c455a1a40f2037b71c0e33cd2bd4847
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104117406"
---
# <a name="nap-server-side-architecture"></a>Architettura lato server NAP

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

L'architettura della piattaforma lato server NAP usa computer che eseguono Windows Server 2008. Nella figura seguente viene illustrata l'architettura del supporto lato server per la piattaforma NAP, costituito da punti di imposizione di protezione accesso alla rete basati su Windows e da un server criteri di integrità protezione accesso alla rete.

![architettura del supporto lato server per la piattaforma NAP](images/nap-server-side-arch.png)

Un punto di imposizione di protezione accesso alla rete basato su Windows dispone di un livello di componenti server di imposizione Protezione accesso alla rete. Ogni protezione accesso alla rete viene definita per un tipo diverso di accesso alla rete o di comunicazione. Ad esempio, esiste un NAP per le connessioni VPN di accesso remoto e un ES NAP per la configurazione DHCP. L'ES NAP viene in genere abbinato a un tipo specifico di client che supporta protezione accesso alla rete. Ad esempio, l'ES NAP DHCP è progettato per funzionare con un client di imposizione di protezione accesso alla rete (EC) basato su DHCP. I fornitori di software di terze parti o Microsoft possono fornire un SSE aggiuntivo di protezione accesso alla rete per la piattaforma NAP. Un'ES NAP ottiene il rapporto di integrità del sistema (SSoH) dal corrispondente EC di protezione accesso alla rete e lo invia a un server criteri di integrità di protezione accesso alla rete come un attributo (VSA) specifico del fornitore (RADIUS) del [messaggio di Access-Request RADIUS](https://www.ietf.org/rfc/rfc2865.txt?number=2865) (Remote Authentication Dial-in User Service).

Come illustrato nella figura relativa all'architettura lato server, il server criteri di integrità protezione accesso alla rete include i componenti seguenti:

-   Servizio Server dei criteri di rete

    Riceve il messaggio di Access-Request RADIUS, estrae il SSoH e lo passa al componente server di amministrazione NAP. Il servizio NPS viene fornito con Windows Server 2008.

-   Server di amministrazione NAP

    Facilita la comunicazione tra il servizio Server dei criteri di rete e i validator di integrità di sistema (SHV). Il componente server di amministrazione NAP viene fornito con la piattaforma protezione accesso alla rete.

-   Livello dei componenti di convalida integrità sistema

    Ogni servizio di convalida dell'integrità di sistema è definito per uno o più tipi di informazioni sull'integrità del sistema e può essere associato a un SHA. Ad esempio, potrebbe essere disponibile un servizio di convalida dell'integrità per un programma antivirus. Un servizio di convalida dell'integrità di sistema può corrispondere a uno o più server di requisiti di integrità. Ad esempio, un servizio di convalida dell'integrità di sistema per la verifica delle firme antivirus viene associato al server che contiene il file della firma più recente. Non è necessario che SHV disponga di un server del requisito di integrità corrispondente. Un servizio di convalida dell'integrità di sistema può solo indicare ai client che supportano NAP di controllare le impostazioni di sistema locale per assicurarsi che sia abilitato un firewall basato su host. Windows Server 2008 include il Convalida integrità sicurezza di Windows (convalida integrità protezione). SHV aggiuntive sono fornite da fornitori di software di terze parti o da Microsoft come componenti aggiuntivi per la piattaforma NAP.

-   API DI CONVALIDA INTEGRITÀ SISTEMA

    Fornisce un set di chiamate di funzione che consentono a SHV di registrarsi con il componente server di amministrazione NAP, ricevere i rapporti di integrità (invieranno) dal componente server di amministrazione NAP e inviare il rendiconto delle risposte di integrità (SoHRs) al componente server di amministrazione NAP. L'API di convalida dell'integrità di sistema viene fornita con la piattaforma NAP. Vedere le interfacce NAP seguenti: [**INapSystemHealthValidator**](inapsystemhealthvalidator.md) e [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md).

Come descritto in precedenza, la configurazione più comune per l'infrastruttura lato server di protezione accesso alla rete è costituita dai punti di imposizione di protezione accesso alla rete che forniscono l'accesso alla rete o la comunicazione di un tipo specifico e server criteri di integrità distinti che forniscono la convalida dell'integrità del sistema È possibile installare il servizio NPS come server dei criteri di integrità di protezione accesso alla rete nei singoli punti di imposizione di protezione accesso alla rete basata su Windows. Tuttavia, in questa configurazione, ogni punto di imposizione di protezione accesso alla rete deve essere configurato separatamente con l'accesso alla rete e i criteri di integrità. La configurazione consigliata consiste nell'utilizzare server dei criteri di integrità di protezione accesso alla rete separati.

L'architettura di protezione accesso alla rete complessiva è costituita dai seguenti set di componenti:

-   I tre componenti client di protezione accesso alla rete (un livello SHA, l'agente NAP e un livello EC di NAP).
-   I quattro componenti lato server NAP, ovvero un livello di convalida integrità di sistema, il server di amministrazione NAP, il servizio Server dei criteri di rete e un livello di protezione accesso alla rete basati su Windows.
-   Requisiti di integrità, ovvero computer che possono fornire i requisiti di integrità del sistema correnti per i server dei criteri di integrità di protezione accesso alla rete.
-   Server di monitoraggio e aggiornamento, ovvero computer che contengono risorse di aggiornamento dell'integrità ai quali i client NAP possono accedere per correggere lo stato non conforme.

Nella figura seguente sono illustrate le relazioni tra i componenti della piattaforma NAP.

![relazioni tra i componenti della piattaforma NAP](images/nap-components.png)

Si noti la corrispondenza dei seguenti set di componenti:

-   Vengono in genere abbinate le funzionalità di protezione accesso alla rete ECs e NAP.

    Ad esempio, la protezione accesso alla rete DHCP nel client NAP viene confrontata con l'ES NAP DHCP nel server DHCP.

-   È possibile trovare una corrispondenza tra i server SHA e i server di monitoraggio e aggiornamento.

    Ad esempio, un SHA antivirus sul client viene associato a un server di monitoraggio e aggiornamento delle firme antivirus.

-   È possibile trovare una corrispondenza tra i server SHV e i requisiti di integrità.

    Ad esempio, un servizio di convalida dell'integrità di sistema per il server criteri di integrità protezione accesso alla rete può corrispondere a un server dei requisiti di integrità del virus.

I fornitori di software di terze parti possono estendere la piattaforma NAP nei modi seguenti:

-   Creare un nuovo metodo in base al quale viene valutato lo stato di integrità di un client di protezione accesso alla rete.

    I fornitori di software di terze parti devono creare un SHA per il client NAP, un servizio di convalida dell'integrità per il server criteri di integrità protezione accesso alla rete e, se necessario, i requisiti di integrità e i server di monitoraggio e aggiornamento Se i requisiti di integrità o i server di monitoraggio e aggiornamento esistono già, ad esempio un server di distribuzione delle firme antivirus, è necessario creare solo i componenti SHA e di convalida integrità corrispondenti. In alcuni casi, i requisiti di integrità o i server di monitoraggio e aggiornamento non sono necessari.

-   Creare un nuovo metodo per applicare i requisiti di integrità per l'accesso alla rete o la comunicazione.

    I fornitori di software di terze parti devono creare una rete di protezione accesso alla rete per il client NAP. Se il metodo di imposizione utilizza un servizio basato su Windows, i fornitori di software di terze parti devono creare un'entità di protezione accesso alla rete corrispondente che comunica con un server criteri di integrità protezione accesso alla rete utilizzando il protocollo RADIUS o il servizio NPS installato nel punto di imposizione di protezione accesso alla rete come proxy RADIUS.

Le sezioni seguenti descrivono in modo dettagliato i componenti dell'architettura lato server di NAP.

## <a name="nap-enforcement-server"></a>Server di imposizione NAP

Un server di imposizione NAP consente un certo livello di accesso alla rete o di comunicazione, può passare lo stato di integrità di un client NAP al server dei criteri di integrità della rete per la valutazione e, in base alla risposta, può fornire l'imposizione di un accesso limitato alla rete.

Il ESs di protezione accesso alla rete incluso in Windows Server 2008 è il seguente:

-   Protezione accesso alla rete IPsec per le comunicazioni protette da IPsec.

    Per le comunicazioni protette con IPsec, Autorità registrazione integrità, un computer che esegue Windows Server 2008 e Internet Information Services (IIS) che ottiene i certificati di integrità da un'autorità di certificazione (CA) per i computer conformi, passa le informazioni sullo stato di integrità del client NAP al server criteri di integrità protezione accesso alla rete.

-   Protezione accesso alla rete DHCP per la configurazione di indirizzi IP basati su DHCP.

    Il servizio protezione accesso alla rete DHCP è una funzionalità del servizio server DHCP che utilizza messaggi DHCP standard del settore per comunicare con la protezione accesso alla rete DHCP in un client di protezione accesso alla rete. L'imposizione DHCP per un accesso limitato alla rete viene eseguita tramite le opzioni DHCP.

-   Protezione accesso alla rete del gateway di Servizi terminal (TS) per le connessioni basate su server Gateway Servizi terminal.

Per le connessioni VPN di accesso remoto e 802.1 X, le funzionalità del servizio Server dei criteri di rete usano messaggi PEAP-TLV tra client NAP e il server criteri di integrità protezione accesso alla rete. L'imposizione VPN viene eseguita tramite i filtri pacchetti IP applicati alla connessione VPN. l'imposizione 802.1 x viene eseguita al dispositivo di accesso alla rete 802.1 X applicando filtri di pacchetti IP alla connessione o assegnando alla connessione un ID VLAN corrispondente alla rete con restrizioni.

## <a name="nap-administration-server"></a>Server di amministrazione NAP

Il componente server di amministrazione NAP fornisce i servizi seguenti:

-   Ottiene il SSoHs dal servizio di protezione accesso alla rete tramite il servizio Server dei criteri di rete.
-   Distribuisce invieranno in SSoHs ai validator di integrità di sistema appropriati.
-   Raccoglie SoHRs da SHV e li passa al servizio NPS per la valutazione.

## <a name="nps-service"></a>Servizio Server dei criteri di rete

RADIUS è un protocollo ampiamente distribuito che consente l'autenticazione centralizzata, l'autorizzazione e l'accounting per l'accesso alla rete descritto in RFC (requests for Comments) 2865 e 2866. Sviluppato originariamente per l'accesso remoto in modalità remota, RADIUS è ora supportato da punti di accesso wireless, autenticazione di commutatori Ethernet, server VPN, server di accesso DSL (Digital Subscriber Line) e altri server di accesso alla rete.

NPS è l'implementazione di un server RADIUS e di un proxy in Windows Server 2008. NPS sostituisce il servizio di autenticazione Internet (IAS) in Windows Server 2003. Per la piattaforma NAP, il servizio Server dei criteri di rete include il componente server amministratore NAP, il supporto per l'API di convalida integrità sistema e SHV installabile e le opzioni per la configurazione dei criteri di integrità.

In base a SoHRs di SHV e ai criteri di integrità configurati, il servizio Server dei criteri di rete crea un rapporto di sistema di risposta di integrità (risposta al rapporto) che indica se il client NAP è conforme o non conforme e include il set di SoHRs da SHV.

## <a name="system-health-validator-shv"></a>Servizio di convalida dell'integrità di sistema (SHV)

Un servizio di convalida dell'integrità riceve un rapporto di integrità dal server di amministrazione NAP e confronta le informazioni sullo stato di integrità del sistema con lo stato di integrità del sistema richiesto. Se, ad esempio, il rapporto di integrità è da un SHA dell'antivirus e contiene il numero di versione dell'ultimo file della firma del virus, il servizio di convalida dell'integrità di sistema corrispondente può verificare con il server dei requisiti di integrità antivirus il numero di versione più recente per convalidare l'integrità del client NAP.

Il servizio di convalida dell'integrità di sistema restituisce un SoHR al server di amministrazione NAP. SoHR possono contenere informazioni sul modo in cui l'SHA corrispondente nel client NAP può soddisfare i requisiti di integrità del sistema correnti. Ad esempio, il SoHR inviato dal servizio di convalida dell'integrità di sistema antivirus potrebbe indicare all'SHA del virus sul client di protezione accesso alla rete di richiedere la versione più recente del file della firma antivirus da uno specifico server di firma antivirus per nome o indirizzo IP.

 

 





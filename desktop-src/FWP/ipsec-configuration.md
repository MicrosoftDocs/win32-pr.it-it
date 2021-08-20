---
title: Configurazione IPsec
description: Windows Piattaforma filtro (WFP) è la piattaforma sottostante per Windows firewall con sicurezza avanzata.
ms.assetid: d54b5caa-daea-4231-9909-7a8d388df661
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34cf20fc8c95aafe3c387195b02468cec3ce884cc97287adde44a594305ee189
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069016"
---
# <a name="ipsec-configuration"></a>Configurazione IPsec

Windows Piattaforma filtro (WFP) è la piattaforma sottostante per Windows firewall con sicurezza avanzata. WFP viene usato per configurare le regole di filtro di rete, che includono regole che regolano la protezione del traffico di rete con IPsec. Gli sviluppatori di applicazioni possono configurare IPsec direttamente usando l'API WFP, per sfruttare un modello di filtro del traffico di rete più granulare rispetto al modello esposto tramite lo snap-in Microsoft Management Console (MMC) per Windows Firewall con sicurezza avanzata.

## <a name="what-is-ipsec"></a>Che cos'è IPsec

Internet Protocol Security (IPsec) è un set di protocolli di sicurezza usati per trasferire i pacchetti IP in modo riservato su Internet. IPsec è obbligatorio per tutte le implementazioni IPv6 e facoltativo per IPv4.

Il traffico IP protetto ha due intestazioni IPsec facoltative, che identificano i tipi di protezione crittografica applicati al pacchetto IP e includono informazioni per la decodifica del pacchetto protetto.

L'intestazione ESP (Encapsulating Security Payload) viene usata per la privacy e la protezione da modifiche dannose eseguendo l'autenticazione e la crittografia facoltativa. Può essere usato per il traffico che attraversa i router NAT (Network Address Translation).

L'intestazione di autenticazione (AH) viene usata solo per la protezione da modifiche dannose eseguendo l'autenticazione. Non può essere usato per il traffico che attraversa i router NAT.

Per altre informazioni su IPsec, vedere anche:

<dl>

[Informazioni di riferimento tecniche su IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc740240(v=ws.10))  
</dl>

## <a name="what-is-ike"></a>Che cos'è IKE

Internet Key Exchange (IKE) è un protocollo di scambio delle chiavi che fa parte del set di protocolli IPsec. IKE viene usato durante la configurazione di una connessione sicura e consente lo scambio sicuro di chiavi segrete e altri parametri correlati alla protezione senza l'intervento dell'utente.

Per altre informazioni su IKE, vedere anche:

<dl>

[Chiave Internet Exchange](/previous-versions/windows/it-pro/windows-server-2003/cc784994(v=ws.10))  
</dl>

## <a name="what-is-authip"></a>Che cos'è AuthIP

Authenticated Internet Protocol (AuthIP) è un nuovo protocollo di scambio delle chiavi che espande IKE come indicato di seguito.

<dl> Anche se IKE supporta solo le credenziali di autenticazione del computer, AuthIP supporta anche:

-   Credenziali utente: NTLM, Kerberos, certificati.
-   Certificati di integrità di Protezione accesso alla rete.
-   Credenziali anonime, usate per l'autenticazione facoltativa.
-   Combinazione di credenziali; ad esempio una combinazione di credenziali Kerberos del computer e dell'utente.

  
AuthIP ha un meccanismo di autenticazione-ripetizione dei tentativi che verifica tutti i metodi di autenticazione configurati prima dell'esito negativo della connessione.  
AuthIP può essere usato con socket sicuri per implementare il traffico protetto IPsec basato sull'applicazione. Fornisce:

-   Autenticazione e crittografia per socket. Per [**altre informazioni, vedere WSASetSocketSecurity.**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity)
-   Rappresentazione del client. IPsec rappresenta il contesto di sicurezza in cui viene creato il socket.
-   Convalida dei nomi peer in ingresso e in uscita. Per [**altre informazioni, vedere WSASetSocketPeerTargetName.**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)

  
</dl>

Per altre informazioni su AuthIP, vedere anche:

<dl>

[AuthIP in Windows Vista](https://www.microsoft.com/technet/community/columns/cableguy/cg0806.mspx)  
</dl>

## <a name="what-is-an-ipsec-policy"></a>Che cos'è un criterio IPsec

Un criterio IPsec è un set di regole che determinano quale tipo di traffico IP deve essere protetto tramite IPsec e come proteggere il traffico. In un computer è attivo un solo criterio IPsec alla volta.

Per altre informazioni sull'implementazione dei criteri IPsec, aprire lo snap-in MMC Criteri di sicurezza locali (secpol.msc), premere F1 per visualizzare la Guida e quindi selezionare Creazione e utilizzo dei criteri IPsec dal sommario.

Per altre informazioni sui criteri IPsec, vedere anche:

<dl>

[Panoramica dei concetti relativi ai criteri IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))  
[Descrizione di un criterio IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc781593(v=ws.10))  
</dl>

## <a name="how-to-use-wfp-to-configure-ipsec-policies"></a>Come usare WFP per configurare i criteri IPsec

L'implementazione Microsoft di IPsec usa Windows filtering platform per configurare i criteri IPsec. I criteri IPsec vengono implementati aggiungendo filtri a vari livelli wfp come indicato di seguito.

-   Ai livelli FWPM LAYER IKEEXT V{4 6} aggiungere filtri che specificano i criteri di negoziazione usati dai moduli di \_ \_ \_ keying (IKE/AuthIP) durante gli scambi in modalità \| principale (MM). A questi livelli vengono specificati i metodi di autenticazione e gli algoritmi di crittografia.
-   Ai livelli FWPM \_ LAYER \_ IPSEC V{4 6} aggiungere filtri che specificano i criteri di negoziazione usati dai moduli di keying durante gli scambi in modalità rapida \_ \| (QM) ed EM (Extended Mode). Le intestazioni IPsec (AH/ESP) e gli algoritmi crittografici vengono specificati a questi livelli.

    I criteri di negoziazione vengono specificati come contesto del provider di criteri associato al filtro. Il modulo di keying enumera i contesti del provider di criteri in base alle caratteristiche del traffico e ottiene i criteri da usare per la negoziazione di sicurezza.

    > [!Note]  
    > L'API WFP può essere usata per specificare direttamente le associazioni di sicurezza (SA) e pertanto ignorare i criteri di negoziazione del modulo di keying.

     

-   Ai livelli FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V{4 \| 6} e FWPM \_ LAYER OUTBOUND TRANSPORT \_ \_ \_ V{4 \| 6} aggiungere filtri che richiamano i callout e determinare quale flusso di traffico deve essere protetto.
-   Ai livelli FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6} aggiungere filtri che implementano il filtro delle identità e i criteri per applicazione.

Il diagramma seguente illustra l'interazione dei vari componenti del Wfp, in relazione all'operazione IPsec.![Configurazione ipsec tramite la piattaforma di filtro di Windows](images/ipsec-configuration.jpg)

Dopo la configurazione, IPsec si integra con wfp ed estende le funzionalità di filtro del WFP fornendo informazioni da usare come condizioni di filtro ai livelli di autorizzazione application layer enforcement (ALE). Ad esempio, IPsec fornisce l'utente remoto e l'identità del computer remoto, che il WFP espone ai livelli di connessione e accettazione dell'autorizzazione ALE. Queste informazioni possono essere usate per l'autorizzazione di identità remota con granularità fine da un'implementazione del firewall basata su WFP.

Di seguito è riportato un esempio di criteri di isolamento che possono essere implementati tramite IPsec:

-   Livelli FWPM \_ LAYER \_ IKEEXT \_ V{4 \| 6} - Autenticazione Kerberos.
-   Livelli FWPM \_ LAYER \_ IPSEC \_ V{4 \| 6} - AH/SHA-1.
-   Livelli FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V{4 \| 6} e FWPM \_ LAYER OUTBOUND TRANSPORT \_ \_ \_ V{4 \| 6}: individuazione della negoziazione per tutto il traffico di rete.
-   Livelli FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6} - IPsec necessario per tutto il traffico di rete.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Livelli WFP**
</dt> <dt>

[**Filtro degli identificatori di livello**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[Livelli ALE](ale-layers.md)
</dt> <dt>

**Scenari di criteri IPsec implementati tramite l'API WFP:**
</dt> <dt>

[modalità di sicurezza trasporto](regular-transport-mode.md)
</dt> <dt>

[Modalità di trasporto individuazione negoziazione](negotiation-discovery-transport-mode.md)
</dt> <dt>

[Modalità trasporto individuazione negoziazione in modalità limite](negotiation-discovery-transport-mode-in-boundary-mode.md)
</dt> <dt>

[Tunnel Modalità](tunnel-mode.md)
</dt> <dt>

[Crittografia garantita](guaranteed-encryption.md)
</dt> <dt>

[Autorizzazione dell'identità remota](remote-identity-authorization.md)
</dt> <dt>

[SA IPsec manuali](manual-ipsec-sas.md)
</dt> <dt>

[Esenzioni IKE/AuthIP](ike-exemptions.md)
</dt> <dt>

**Soluzioni IPsec:**
</dt> <dt>

[Isolamento del dominio e del server](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))
</dt> </dl>

 

 
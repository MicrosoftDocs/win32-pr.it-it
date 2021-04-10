---
title: Configurazione IPsec
description: Windows Filtering Platform (WFP) è la piattaforma sottostante per Windows Firewall con sicurezza avanzata.
ms.assetid: d54b5caa-daea-4231-9909-7a8d388df661
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78af8e3d0a23713c0505082555fe260bc562dfa4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963025"
---
# <a name="ipsec-configuration"></a>Configurazione IPsec

Windows Filtering Platform (WFP) è la piattaforma sottostante per Windows Firewall con sicurezza avanzata. Il WFP viene usato per configurare le regole di filtro di rete, che includono regole che regolano la protezione del traffico di rete con IPsec. Gli sviluppatori di applicazioni possono configurare IPsec direttamente tramite l'API WFP, per sfruttare i vantaggi di un modello di filtro del traffico di rete più granulare rispetto al modello esposto tramite lo snap-in MMC (Microsoft Management Console) per Windows Firewall con sicurezza avanzata.

## <a name="what-is-ipsec"></a>Informazioni su IPsec

Internet Protocol Security (IPsec) è un set di protocolli di sicurezza usati per trasferire i pacchetti IP in modo riservato in Internet. IPsec è obbligatorio per tutte le implementazioni IPv6 e facoltativo per IPv4.

Il traffico IP protetto presenta due intestazioni IPsec facoltative, che identificano i tipi di protezione crittografica applicati al pacchetto IP e includono informazioni per la decodifica del pacchetto protetto.

L'intestazione ESP (Encapsulating Security Payload) viene utilizzata per la privacy e la protezione da modifiche dannose eseguendo l'autenticazione e la crittografia facoltativa. Può essere usato per il traffico che attraversa i router NAT (Network Address Translation).

L'intestazione di autenticazione (AH) viene utilizzata solo per la protezione da modifiche dannose eseguendo l'autenticazione. Non può essere usato per il traffico che attraversa i router NAT.

Per ulteriori informazioni su IPsec, vedere anche:

<dl>

[Riferimento tecnico per IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc740240(v=ws.10))  
</dl>

## <a name="what-is-ike"></a>Che cos'è IKE

Protocollo IKE (IKE) è un protocollo di scambio di chiave che fa parte del set di protocolli IPsec. IKE viene usato durante la configurazione di una connessione protetta ed esegue lo scambio sicuro di chiavi segrete e altri parametri correlati alla protezione senza l'intervento dell'utente.

Per ulteriori informazioni su IKE, vedere anche:

<dl>

[protocollo IKE](/previous-versions/windows/it-pro/windows-server-2003/cc784994(v=ws.10))  
</dl>

## <a name="what-is-authip"></a>Informazioni su AuthIP

Authenticated Internet Protocol (AuthIP) è un nuovo protocollo di scambio delle chiavi che espande IKE come indicato di seguito.

<dl> Sebbene IKE supporti solo le credenziali di autenticazione del computer, AuthIP supporta anche:

-   Credenziali utente: NTLM, Kerberos, certificati.
-   Certificati di integrità di protezione accesso alla rete (NAP).
-   Credenziali anonime, usate per l'autenticazione facoltativa.
-   Combinazione di credenziali; ad esempio, una combinazione di credenziali Kerberos del computer e dell'utente.

  
AuthIP dispone di un meccanismo di tentativi di autenticazione che verifica tutti i metodi di autenticazione configurati prima di eseguire la connessione.  
AuthIP può essere usato con socket protetti per implementare il traffico protetto con IPsec basato sull'applicazione. Fornisce:

-   Autenticazione e crittografia per socket. Per ulteriori informazioni, vedere [**WSASetSocketSecurity**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) .
-   Rappresentazione client. (IPsec rappresenta il contesto di sicurezza in cui viene creato il socket).
-   Convalida del nome peer in ingresso e in uscita. Per ulteriori informazioni, vedere [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) .

  
</dl>

Per ulteriori informazioni su AuthIP, vedere anche:

<dl>

[AuthIP in Windows Vista](https://www.microsoft.com/technet/community/columns/cableguy/cg0806.mspx)  
</dl>

## <a name="what-is-an-ipsec-policy"></a>Informazioni sui criteri IPsec

Un criterio IPsec è un set di regole che determinano il tipo di traffico IP che deve essere protetto tramite IPsec e come proteggere il traffico. Solo un criterio IPsec è attivo in un computer contemporaneamente.

Per ulteriori informazioni sull'implementazione dei criteri IPsec, aprire lo snap-in MMC Criteri di sicurezza locali (secpol. msc), premere F1 per visualizzare la guida, quindi selezionare Creazione e utilizzo di criteri IPsec dal sommario.

Per ulteriori informazioni sui criteri IPsec, vedere anche:

<dl>

[Panoramica dei concetti relativi ai criteri IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))  
[Descrizione di un criterio IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc781593(v=ws.10))  
</dl>

## <a name="how-to-use-wfp-to-configure-ipsec-policies"></a>Come utilizzare WFP per configurare i criteri IPsec

L'implementazione Microsoft di IPsec usa la piattaforma filtro Windows per configurare i criteri IPsec. I criteri IPsec vengono implementati aggiungendo filtri a diversi livelli di PAM come indicato di seguito.

-   Ai livelli FWPM \_ Layer \_ IKEEXT \_ V {4 \| 6} aggiungere filtri che specificano i criteri di negoziazione usati dai moduli di chiavi (IKE/AuthIP) durante gli scambi in modalità principale (mm). I metodi di autenticazione e gli algoritmi di crittografia vengono specificati a livello di questi livelli.
-   Ai livelli FWPM \_ Layer \_ IPSec \_ V {4 \| 6} aggiungere filtri che specificano i criteri di negoziazione usati dai moduli di chiave in modalità rapida (QM) e gli scambi in modalità estesa (em). Le intestazioni IPsec (AH/ESP) e gli algoritmi di crittografia vengono specificati a questi livelli.

    Un criterio di negoziazione viene specificato come contesto del provider di criteri associato al filtro. Il modulo di trasparenza enumera i contesti del provider di criteri in base alle caratteristiche del traffico e ottiene il criterio da utilizzare per la negoziazione di sicurezza.

    > [!Note]  
    > L'API PAM può essere usata per specificare direttamente le associazioni di sicurezza (SAs) e pertanto ignorare i criteri di negoziazione del modulo di chiave.

     

-   Ai livelli del \_ trasporto in ingresso FWPM layer \_ \_ \_ v {4 \| 6} e FWPM \_ Layer trasporto in \_ uscita \_ \_ v {4 \| 6} livelli aggiungere filtri che richiamano i callout e determinano il flusso del traffico da proteggere.
-   A livello di FWPM level \_ \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6} livelli Aggiungi filtri che implementano il filtro delle identità e i criteri per ogni applicazione.

Nel diagramma seguente viene illustrata l'interazione tra i vari componenti di WFP, rispetto all'operazione IPsec.![configurazione IPSec con Windows Filtering Platform](images/ipsec-configuration.jpg)

Una volta configurato IPsec, si integra con WFP ed estende le funzionalità di filtro WFP fornendo le informazioni da usare come condizioni di filtro ai livelli di autorizzazione di Application Layer Enforcement (ALE). IPsec, ad esempio, fornisce l'utente remoto e l'identità del computer remoto, che viene esposta da WFP in ALE Connect e accettano i livelli di autorizzazione. Queste informazioni possono essere usate per l'autorizzazione di identità remota con granularità fine da un'implementazione del firewall basata su PAM.

Di seguito sono riportati i criteri di isolamento di esempio che possono essere implementati tramite IPsec:

-   FWPM \_ Layer \_ IKEEXT \_ V {4 \| 6} livelli: autenticazione Kerberos.
-   FWPM \_ Layer \_ IPSec \_ V {4 \| 6} livelli-Ah/SHA-1.
-   FWPM \_ Layer \_ \_ trasporto in ingresso \_ v {4 \| 6} e FWPM \_ Layer \_ \_ trasporto in uscita \_ v {4 \| 6} livelli-individuazione negoziazione per tutto il traffico di rete.
-   FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6} livelli-IPSec obbligatorio per tutto il traffico di rete.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Livelli WFP**
</dt> <dt>

[**Filtraggio degli identificatori del livello**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[Livelli ALE](ale-layers.md)
</dt> <dt>

**Scenari di criteri IPsec implementati tramite l'API PAM:**
</dt> <dt>

[modalità di sicurezza trasporto](regular-transport-mode.md)
</dt> <dt>

[Modalità trasporto individuazione negoziazione](negotiation-discovery-transport-mode.md)
</dt> <dt>

[Modalità di trasporto individuazione negoziazione in modalità limite](negotiation-discovery-transport-mode-in-boundary-mode.md)
</dt> <dt>

[Modalità tunnel](tunnel-mode.md)
</dt> <dt>

[Crittografia garantita](guaranteed-encryption.md)
</dt> <dt>

[Autorizzazione identità remota](remote-identity-authorization.md)
</dt> <dt>

[SAs manuale IPsec](manual-ipsec-sas.md)
</dt> <dt>

[Esenzioni IKE/AuthIP](ike-exemptions.md)
</dt> <dt>

**Soluzioni IPsec:**
</dt> <dt>

[Isolamento del dominio e del server](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))
</dt> </dl>

 

 
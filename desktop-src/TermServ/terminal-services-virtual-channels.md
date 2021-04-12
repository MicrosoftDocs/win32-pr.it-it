---
title: Servizi Desktop remoto canali virtuali
description: I canali virtuali sono estensioni software che possono essere usate per aggiungere miglioramenti funzionali a un'applicazione Servizi Desktop remoto.
ms.assetid: f7bdebec-ecc3-4f28-9327-f0d2f169c142
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce78331841a41502aa337de19e9879d42d85fe1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329700"
---
# <a name="remote-desktop-services-virtual-channels"></a>Servizi Desktop remoto canali virtuali

I *canali virtuali* sono estensioni software che possono essere usate per aggiungere miglioramenti funzionali a un'applicazione Servizi Desktop remoto. Esempi di miglioramenti funzionali possono includere: supporto per tipi speciali di hardware, audio o altre aggiunte alle funzionalità di base fornite dalla Servizi Desktop remoto [Remote Desktop Protocol](remote-desktop-protocol.md) (RDP). Il protocollo RDP fornisce la gestione multiplexata di più canali virtuali.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[Uso di Servizi Desktop remoto canali virtuali](using-terminal-services-virtual-channels.md)
</dt> <dd>

Per implementare un canale virtuale, fornire i moduli server e client dell'applicazione di un canale virtuale.

</dd> <dt>

[Guida di riferimento ai canali virtuali dinamici](dynamic-virtual-channels-reference.md)
</dt> <dd>

Le interfacce client dinamiche del canale virtuale (DVC) sono supportate da Servizi Desktop remoto.

</dd> <dt>

[Informazioni di riferimento sui canali virtuali grafici](graphics-virtual-channels-reference.md)
</dt> <dd>

La Guida di riferimento ai canali virtuali grafici contiene elementi di programmazione che consentono di creare un canale di grafica virtuale.

</dd> </dl>

Un'applicazione di canale virtuale è costituita da due parti, un modulo client e un modulo server. Il modulo server è un programma eseguibile in esecuzione nel server host sessione Desktop remoto (host sessione Desktop remoto). Il modulo client è una DLL che deve essere caricata in memoria sul computer client durante l'esecuzione del programma client di Connessione Desktop remoto (RDC).

I canali virtuali possono aggiungere miglioramenti funzionali a un client Connessione Desktop remoto (RDC), indipendentemente dal protocollo RDP. Con il supporto dei canali virtuali, è possibile aggiungere nuove funzionalità senza dover aggiornare il software client o server o il protocollo RDP.

Sono state identificate quattro classi principali di utenti di canali virtuali:

-   Driver in modalità kernel generale, ad esempio driver seriale o stampanti.
-   Reindirizzamento del file System (questo è solo un caso speciale di un driver in modalità kernel generale).
-   Applicazioni in modalità utente, ad esempio Cut-and-paste remote.
-   Dispositivi audio.

Per ulteriori informazioni, vedere [utilizzo di Servizi Desktop remoto canali virtuali](using-terminal-services-virtual-channels.md).

Se è stata abilitata un'applicazione per i canali virtuali nella distribuzione di Servizi Desktop remoto, è possibile rendere disponibile l'applicazione ai computer client che accedono al server Host sessione Desktop remoto tramite il Desktop remoto controllo ActiveX Microsoft. Per altre informazioni, vedere [canali virtuali con script](scriptable-virtual-channels.md) e [uso del controllo ActiveX Desktop remoto con i canali virtuali](using-the-remote-desktop-activex-control-with-virtual-channels.md).

 

 





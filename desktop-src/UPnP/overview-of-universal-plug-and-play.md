---
title: Panoramica dell'architettura UPnP
description: L'architettura UPnP definisce la connettività di rete peer-to-peer di Appliance intelligenti, dispositivi e punti di controllo.
ms.assetid: 09aba033-6229-4a55-9421-a7b967508bf4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10ce11009bfecfe03fa176c1e6c75be173fbde86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872794"
---
# <a name="overview-of-upnp-architecture"></a>Panoramica dell'architettura UPnP

L'architettura UPnP definisce la connettività di rete peer-to-peer di Appliance intelligenti, dispositivi e [*punti di controllo*](c-gly.md). È progettato per fornire connettività di facile utilizzo, flessibile e basata su standard ad reti ad hoc, gestite o non gestite, sia che si tratti di reti domestiche, piccole imprese o collegate direttamente a Internet. L'architettura UPnP è un'architettura di rete aperta e distribuita che usa le tecnologie TCP/IP e Web esistenti per consentire la rete con prossimità senza problemi, oltre a controllare e trasferire i dati tra i dispositivi in rete.

UPnP è una suite di protocolli basata su IP basata su versioni preliminari di protocolli di servizi Web quali XML e Simple Object Access Protocol (SOAP). Con UPnP, un dispositivo può essere aggiunto dinamicamente a una rete, ottenere un indirizzo IP, fornire le funzionalità e individuare la presenza e le funzionalità di altri dispositivi nella rete.

Un dispositivo UPnP è un contenitore di servizi e dispositivi annidati. Un VCR, ad esempio, può essere costituito da un servizio di trasporto nastro, un servizio Tuner e un servizio clock. Diverse categorie di dispositivi UPnP sono associate a diversi set di servizi e dispositivi incorporati. I servizi all'interno di un VCR, ad esempio, sono diversi da quelli all'interno di una stampante. Le informazioni sul set di servizi che un particolare tipo di dispositivo può fornire sono acquisite in un documento di descrizione del dispositivo XML che ospita il dispositivo. Nella descrizione del dispositivo sono inoltre elencate le proprietà, ad esempio il nome del dispositivo e le icone associate al dispositivo. Microsoft ha migliorato il supporto UPnP per includere l'integrazione con [PnP-X](/previous-versions/windows/desktop/fundisc/pnp-x) e l' [individuazione di funzioni](/previous-versions/windows/desktop/fundisc/fd-portal).

L'architettura UPnP è più di una semplice estensione del modello di periferica Plug and Play. Supporta la configurazione zero, la rete invisibile e l'individuazione automatica per una gamma di categorie di dispositivi da un'ampia gamma di fornitori. Ciò consente a un dispositivo di partecipare dinamicamente a una rete, ottenere un indirizzo IP e fornire le proprie funzionalità su richiesta. Quindi, altri punti di controllo possono usare l'API del punto di controllo con la tecnologia UPnP per apprendere la presenza e le funzionalità di altri dispositivi. Un dispositivo può lasciare una rete in modo semplice e automatico quando non è più in uso.

Cosa è universale sulla tecnologia UPnP?

-   Indipendenza del dispositivo e dei supporti. La tecnologia UPnP può essere eseguita su qualsiasi supporto, ad esempio una linea telefonica, una linea di alimentazione, Ethernet, RF e 1394.
-   Indipendenza dalla piattaforma. I fornitori utilizzano qualsiasi sistema operativo e qualsiasi linguaggio di programmazione per compilare prodotti basati su UPnP.
-   Tecnologie basate su Internet. La tecnologia UPnP si basa su IP, TCP, UDP, HTTP e XML, tra gli altri.
-   Controllo dell'interfaccia utente. L'architettura UPnP consente al fornitore di controllare l'interfaccia utente del dispositivo e l'interazione con il browser.
-   Controllo a livello di codice. L'architettura UPnP consente anche il controllo a livello di programmazione dell'applicazione convenzionale.
-   Protocolli di base comuni. I fornitori accettano i set di protocolli di base per ogni singolo dispositivo.
-   Allungabile. Ogni prodotto basato su UPnP può avere servizi a valore aggiunto sovrapposti all'architettura del dispositivo di base da parte dei singoli produttori.

La tecnologia UPnP è molto ampia in quanto è destinata a reti domestiche, reti di prossimità e reti di piccole imprese e edifici commerciali. Consente la comunicazione dati tra due dispositivi qualsiasi sotto il comando di qualsiasi dispositivo di controllo nella rete. La tecnologia UPnP è indipendente da qualsiasi sistema operativo, linguaggio di programmazione o supporto fisico specifico.

Microsoft fornisce due API per l'utilizzo di dispositivi basati su UPnP:

-   [API del punto di controllo](control-point-api.md) : fornisce un set di interfacce com che consentono alle applicazioni di trovare e controllare i dispositivi basati su UPnP.
-   [API dell'host del dispositivo](device-host-api.md) : fornisce un set di interfacce com che consentono agli sviluppatori di scrivere le funzionalità di base dei dispositivi e di registrare il dispositivo con l'host del dispositivo. L'host del dispositivo gestisce le parti di individuazione, descrizione, controllo ed eventi della funzionalità del dispositivo basato su UPnP.

 

 
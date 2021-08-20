---
title: Panoramica dell'architettura UPnP
description: L'architettura UPnP definisce la connettività di rete peer-to-peer di appliance intelligenti, dispositivi e punti di controllo.
ms.assetid: 09aba033-6229-4a55-9421-a7b967508bf4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5866d3e701f53e95225538655ca45d159fb7c5f67d00e3c46c97357c7a9ee6a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126454"
---
# <a name="overview-of-upnp-architecture"></a>Panoramica dell'architettura UPnP

L'architettura UPnP definisce la connettività di rete peer-to-peer di appliance intelligenti, dispositivi e punti [*di controllo.*](c-gly.md) È progettato per consentire connettività semplice, flessibile e basata su standard a reti ad hoc, gestite o non gestite, indipendentemente dal fatto che queste reti siano in casa, in aziende di piccole dimensioni o collegate direttamente a Internet. L'architettura UPnP è un'architettura di rete distribuita e aperta che usa tecnologie TCP/IP e Web esistenti per consentire una rete di prossimità trasparente, oltre al controllo e al trasferimento dei dati tra i dispositivi di rete.

UPnP è una suite di protocolli basata su IP basata su versioni preliminari dei protocolli dei servizi Web, ad esempio XML e Simple Object Access Protocol (SOAP). Con UPnP, un dispositivo può aggiungersi dinamicamente a una rete, ottenere un indirizzo IP, comunicarne le funzionalità e individuare la presenza e le funzionalità di altri dispositivi nella rete.

Un dispositivo UPnP è un contenitore di servizi e dispositivi annidati. Ad esempio, un videoregistratore può essere costituito da un servizio di trasporto su nastro, un servizio di tuner e un servizio orologio. Diverse categorie di dispositivi UPnP sono associate a diversi set di servizi e dispositivi incorporati. Ad esempio, i servizi all'interno di un videoregistratore sono diversi da quelli all'interno di una stampante. Le informazioni sul set di servizi che un particolare tipo di dispositivo può fornire vengono acquisite in un documento di descrizione del dispositivo XML che il dispositivo ospita. La descrizione del dispositivo elenca anche le proprietà, ad esempio il nome del dispositivo e le icone associate al dispositivo. Microsoft ha migliorato il supporto UPnP per includere l'integrazione [con PnP-X](/previous-versions/windows/desktop/fundisc/pnp-x) e [Individuazione funzioni.](/previous-versions/windows/desktop/fundisc/fd-portal)

L'architettura UPnP non è solo una semplice estensione del modello di periferiche plug-and-play. Supporta funzionalità di rete senza configurazione e invisibili e l'individuazione automatica per una gamma di categorie di dispositivi di un'ampia gamma di fornitori. Ciò consente a un dispositivo di aggiungersi dinamicamente a una rete, ottenere un indirizzo IP e trasmetterne le funzionalità su richiesta. Altri punti di controllo possono quindi usare l'API del punto di controllo con la tecnologia UPnP per ottenere informazioni sulla presenza e sulle funzionalità di altri dispositivi. Un dispositivo può lasciare una rete senza problemi e automaticamente quando non è più in uso.

Informazioni universali sulla tecnologia UPnP

-   Indipendenza dei supporti e dei dispositivi. La tecnologia UPnP può essere eseguita su qualsiasi supporto, tra cui linea telefonica, linea elettrica, Ethernet, RF e 1394.
-   Indipendenza dalla piattaforma. I fornitori usano qualsiasi sistema operativo e qualsiasi linguaggio di programmazione per creare prodotti basati su UPnP.
-   Tecnologie basate su Internet. La tecnologia UPnP si basa su IP, TCP, UDP, HTTP e XML, tra gli altri.
-   Controllo dell'interfaccia utente. L'architettura UPnP consente al fornitore di controllare l'interfaccia utente del dispositivo e l'interazione tramite il browser.
-   Controllo a livello di codice. L'architettura UPnP consente anche il controllo a livello di codice dell'applicazione convenzionale.
-   Protocolli di base comuni. I fornitori concordano sui set di protocolli di base per ogni dispositivo.
-   Estensibile. Ogni prodotto basato su UPnP può avere servizi a valore aggiunto a più livelli sull'architettura di dispositivo di base dei singoli produttori.

La tecnologia UPnP ha un ampio ambito in quanto è destinata a reti domestiche, reti di prossimità e reti in piccole aziende e edifici commerciali. Consente la comunicazione dei dati tra due dispositivi qualsiasi sotto il comando di qualsiasi dispositivo di controllo nella rete. La tecnologia UPnP è indipendente da qualsiasi sistema operativo, linguaggio di programmazione o supporto fisico specifico.

Microsoft offre due API per l'uso di dispositivi basati su UPnP:

-   [API del punto di](control-point-api.md) controllo: fornisce un set di interfacce COM che consentono alle applicazioni di trovare e controllare i dispositivi basati su UPnP.
-   [API Host dispositivo:](device-host-api.md) fornisce un set di interfacce COM che consentono agli sviluppatori di scrivere le funzionalità principali del dispositivo e registrare il dispositivo con l'host del dispositivo. L'host del dispositivo gestisce le parti di individuazione, descrizione, controllo e gestione degli eventi delle funzionalità del dispositivo basate su UPnP.

 

 
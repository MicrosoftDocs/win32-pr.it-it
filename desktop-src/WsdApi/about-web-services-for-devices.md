---
description: L'API Servizio Web nei dispositivi (WSDAPI) è un'implementazione del profilo dispositivi per i servizi Web (DPWS) per Windows Vista e Windows Server 2008.
ms.assetid: 8eaeacb3-43db-4a57-8548-e5b81213269c
title: Informazioni sui servizi Web nei dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c7facef3bfed004a834e151db0c58c83a1576e515ed89fa0d690813bc4c18bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118552516"
---
# <a name="about-web-services-on-devices"></a>Informazioni sui servizi Web nei dispositivi

L'API Servizio Web nei dispositivi (WSDAPI) è un'implementazione del profilo dispositivi per i servizi [Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) per Windows Vista e Windows Server 2008. DPWS vincola le specifiche dei servizi Web in modo che i client possano individuare facilmente i dispositivi. Dopo aver individuato un dispositivo, un client può recuperare una descrizione dei servizi ospitati in tale dispositivo e usarli.

## <a name="devices-and-services"></a>Dispositivi e servizi

*I* dispositivi sono componenti, in genere hardware, collegati alla rete. Ad esempio stampanti, fotocamere Web e sistemi video.

I dispositivi possono includere zero o più *servizi*. Ad esempio, un dispositivo video può includere servizi che supportano l'accensione e lo spento, il controllo di riproduzione, l'espulsione di contenuti multimediali e lo streaming video. Il controllo di riproduzione può supportare azioni come riproduzione, sospensione, riavvolgimento e avanzamento rapido.

## <a name="discovering-and-manipulating-a-device"></a>Individuazione e manipolazione di un dispositivo

WSDAPI estende il modello Plug and Play locale consentendo a un client di individuare e accedere a un dispositivo remoto e ai relativi servizi associati in una rete. Supporta la messaggistica di individuazione, la messaggistica di controllo unidirezione e bidirezione e gli eventi.

![Diagramma che illustra come WSDAPI consente a un client di individuare e accedere a un dispositivo remoto.](images/overview01.png)

I dispositivi DPWS annunciano la propria presenza ed espongono i servizi (se presenti) usando un indirizzo univoco e un set standardizzato di messaggi XML. I client DPWS possono usare il processo di individuazione per trovare il dispositivo, enumerare i servizi e connettersi a tali servizi per eseguire azioni specifiche.

Un client WSDAPI esegue innanzitutto una query sul dispositivo per una descrizione completa dei relativi servizi, inclusi i tipi di servizio , ad esempio un tipo di servizio stampante o un tipo di servizio scanner. Il client controlla quindi il dispositivo chiamando i comandi definiti da un tipo di servizio, ad esempio chiamando **CreatePrintJob** in un dispositivo con un tipo di servizio stampante. Facoltativamente, il client può anche monitorare le modifiche dello stato in ogni servizio sottoscrivendo gli eventi che si verificano durante l'esecuzione del comando.

![Diagramma che mostra come un client WSDAPI esegue query e interagisce con un dispositivo.](images/netdevice01.png)

Per altre informazioni sui modelli di messaggistica dei dispositivi, vedere [Individuazione e metadati Exchange di messaggi.](discovery-and-metadata-exchange-message-patterns.md)

## <a name="logical-and-physical-addressing"></a>Indirizzamento logico e fisico

L'indirizzamento logico viene usato per identificare in modo univoco i dispositivi indipendentemente dai relativi indirizzi fisici. WS-Discovery un meccanismo per risolvere gli indirizzi logici in indirizzi fisici, consentendo la messaggistica da client a dispositivo. Un esempio è l'archiviazione con collegamento di rete (NAS) che si porta con sé. Se si dispone di un portatile e di un NAS, il portatile dovrebbe essere in grado di riconoscere che si tratta dello stesso dispositivo, indipendentemente dall'indirizzo fisico (indirizzo IP) ottenuto dal NAS durante lo spostamento tra le subnet. A tale scopo, è necessario che il dispositivo abbia un'identità indipendente dall'indirizzo IP ottenuto; Poiché i meccanismi tradizionali come DNS non sono disponibili in uno scenario di roaming normale, WS-Addressing e WS-Discovery forniscono l'indirizzamento logico e la risoluzione come alternativa ad hoc.

Quando un dispositivo viene prodotto, viene assegnato un identificatore univoco globale, rappresentato come URI UUID. Questo identificatore non cambierà mai per il dispositivo. Quando il dispositivo è acceso, annuncerà sempre il proprio indirizzo logico tramite un messaggio hello WS-Discovery e accetterà le richieste di convertirlo [in](hello-message.md) un indirizzo fisico (in genere HTTP) tramite messaggi di WS-Discovery [Resolve](resolve-message.md) o [Probe.](probe-message.md) Una volta ottenuto un indirizzo fisico (indirizzo IP) valido, tutta la messaggistica viene eseguita su tale indirizzo e WS-Discovery viene usato solo se l'indirizzo cambia, il dispositivo cambia stato e i client devono ricevere una notifica o il dispositivo passa offline.

## <a name="building-applications"></a>Compilazione di applicazioni

WSDAPI fornisce uno stack SOAP DPWS generico per l'uso da parte di applicazioni client e di servizio. Il [generatore di](web-services-for-devices-code-generator.md) codice dei servizi Web nei dispositivi (WsdCodeGen.exe) può essere usato per convertire una descrizione del servizio (WSDL) in codice proxy e stub che le applicazioni possono chiamare direttamente. Questo codice generato trasforma automaticamente le chiamate di funzione e i parametri in messaggi SOAP e campi XML e quindi chiama WSDAPI per inviare richieste al dispositivo o al client remoto.

L'individuazione delle funzioni può essere usata durante la compilazione di applicazioni WSDAPI per creare e attivare istanze di funzione restituite da PnP. Queste istanze di funzione contengono dati che possono essere usati per ottenere altre informazioni tramite le API PnP quando è necessaria più di una semplice individuazione. Per altre informazioni, vedere [Individuazione delle funzioni](/previous-versions/windows/desktop/fundisc/fd-portal) e [PnP-X.](/previous-versions/windows/desktop/fundisc/pnp-x)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Criteri di individuazione e Exchange dei messaggi](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Conformità alle specifiche WSDAPI](wsdapi-specification-compliance.md)
</dt> <dt>

[Panoramica delle interfacce WSDAPI](overview-of-the-wsdapi-interfaces.md)
</dt> </dl>

 

 

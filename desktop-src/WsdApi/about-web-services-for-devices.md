---
description: Il servizio Web on Devices API (WSDAPI) è un'implementazione del profilo Devices per i servizi Web (DPWS) per Windows Vista e Windows Server 2008.
ms.assetid: 8eaeacb3-43db-4a57-8548-e5b81213269c
title: Informazioni sui servizi Web nei dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dca7f7dc97dabd3dde7af12f3cece992b4f0ef6d
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "103885928"
---
# <a name="about-web-services-on-devices"></a>Informazioni sui servizi Web nei dispositivi

Il servizio Web on Devices API (WSDAPI) è un'implementazione del [profilo Devices per i servizi Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) per Windows Vista e windows Server 2008. DPWS vincola le specifiche dei servizi Web in modo che i client possano individuare facilmente i dispositivi. Una volta individuato un dispositivo, un client può recuperare una descrizione dei servizi ospitati nel dispositivo e usarli.

## <a name="devices-and-services"></a>Dispositivi e servizi

I *dispositivi* sono componenti, in genere hardware, collegati alla rete. Tra gli esempi sono incluse stampanti, fotocamere Web e sistemi video.

I dispositivi possono includere zero o più *Servizi*. Ad esempio, un dispositivo video può includere servizi che supportano l'accensione e la disattivazione, il controllo di riproduzione, l'espulsione dei supporti e il flusso video. Il controllo Play può supportare azioni quali riproduzione, sospensione, riavvolgimento e avanzamento rapido.

## <a name="discovering-and-manipulating-a-device"></a>Individuazione e manipolazione di un dispositivo

WSDAPI estende il modello di Plug and Play locale consentendo a un client di individuare e accedere a un dispositivo remoto e ai relativi servizi associati in una rete. Supporta l'individuazione, la messaggistica unidirezionale e bidirezionale e la gestione degli eventi.

![Diagramma che illustra come WSDAPI consente a un client di individuare e accedere a un dispositivo remoto.](images/overview01.png)

I dispositivi DPWS annunciano la loro presenza ed espongono i servizi, se presenti, usando un indirizzo univoco e un set standardizzato di messaggi XML. I client DPWS possono usare il processo di individuazione per trovare il dispositivo, enumerarne i servizi e connettersi a tali servizi per eseguire azioni specifiche.

Un client WSDAPI esegue prima una query sul dispositivo per completare una descrizione dei servizi, inclusi i tipi di servizio, ad esempio un tipo di servizio di stampa o un tipo di servizio scanner. Il client controlla quindi il dispositivo chiamando i comandi definiti da un tipo di servizio, ad esempio chiamando **CreatePrintJob** su un dispositivo con un tipo di servizio di stampa. Facoltativamente, il client può anche monitorare le modifiche dello stato in ogni servizio sottoscrivendo gli eventi che si verificano durante l'esecuzione del comando.

![Diagramma che illustra il modo in cui un client WSDAPI esegue una query e interagisce con un dispositivo.](images/netdevice01.png)

Per altre informazioni sui modelli di messaggistica del dispositivo, vedere [modelli di messaggio di scambio di metadati e individuazione](discovery-and-metadata-exchange-message-patterns.md).

## <a name="logical-and-physical-addressing"></a>Indirizzamento logico e fisico

L'indirizzamento logico viene usato per identificare in modo univoco i dispositivi indipendenti dai rispettivi indirizzi fisici. WS-Discovery fornisce un meccanismo per risolvere gli indirizzi logici in indirizzi fisici, consentendo la messaggistica da client a dispositivo. Un esempio è il NAS (Network Attached Storage) che viene utilizzato. Se si dispone di un portatile e di un NAS, il computer portatile dovrebbe essere in grado di riconoscere che è lo stesso dispositivo, indipendentemente dall'indirizzo fisico (indirizzo IP) ottenuto dal NAS durante lo spostamento tra le subnet. Per eseguire questa operazione è necessario che il dispositivo disponga di un'identità indipendente dall'indirizzo IP ottenuto. Poiché i meccanismi tradizionali come il DNS non sono disponibili in uno scenario comune, WS-Addressing e WS-Discovery forniscono la risoluzione e l'indirizzamento logici come alternativa ad hoc.

Quando un dispositivo viene prodotto, viene assegnato un identificatore univoco globale, rappresentato come un URI UUID. Questo identificatore non verrà mai modificato per il dispositivo. Quando il dispositivo è acceso, l'indirizzo logico viene sempre annunciato tramite un messaggio WS-Discovery [Hello](hello-message.md) e accetta le richieste per convertirlo in un indirizzo fisico (in genere http) tramite WS-Discovery i messaggi di [risoluzione](resolve-message.md) o [Probe](probe-message.md) . Una volta ottenuto un indirizzo fisico (indirizzo IP) valido, tutti i messaggi avvengono su tale indirizzo e WS-Discovery viene usato solo se l'indirizzo cambia, il dispositivo cambia stato e i client devono ricevere una notifica oppure il dispositivo passa alla modalità offline.

## <a name="building-applications"></a>Compilazione di applicazioni

WSDAPI fornisce uno stack SOAP DPWS generico per l'uso da applicazioni client e di servizio. Il [Generatore di codice dei servizi Web in dispositivi](web-services-for-devices-code-generator.md) (WsdCodeGen.exe) può essere usato per convertire una descrizione del servizio (WSDL) in codice di proxy e stub che le applicazioni possono chiamare direttamente. Questo codice generato trasforma automaticamente le chiamate di funzione e i parametri in messaggi SOAP e campi XML, quindi chiama WSDAPI per emettere richieste al dispositivo remoto o al client.

L'individuazione della funzione può essere utilizzata per la compilazione di applicazioni WSDAPI per la creazione e l'attivazione di istanze di funzione restituite da PnP. Queste istanze di funzioni contengono dati che possono essere utilizzati per ottenere ulteriori informazioni tramite le API PnP quando è necessaria una sola individuazione semplice. Per ulteriori informazioni, vedere [individuazione di funzioni](/previous-versions/windows/desktop/fundisc/fd-portal) e [PnP-X](/previous-versions/windows/desktop/fundisc/pnp-x).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modelli di messaggi di individuazione e scambio di metadati](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Conformità della specifica WSDAPI](wsdapi-specification-compliance.md)
</dt> <dt>

[Panoramica delle interfacce WSDAPI](overview-of-the-wsdapi-interfaces.md)
</dt> </dl>

 

 

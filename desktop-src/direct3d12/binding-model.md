---
title: Differenze nel modello di associazione da Direct3D 11
description: Una delle principali decisioni di progettazione alla base dell'associazione DirectX12 consiste nel separarla da altre attività di gestione. Questa operazione impone alcuni requisiti nell'app per gestire determinati rischi potenziali.
ms.assetid: 3EE7E9AE-203D-40D4-9F12-4313ED179035
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b2785da6497fd4e775d9f88847928e7c4c08e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104068"
---
# <a name="differences-in-the-binding-model-from-direct3d-11"></a>Differenze nel modello di associazione da Direct3D 11

Una delle principali decisioni di progettazione alla base dell'associazione DirectX12 consiste nel separarla da altre attività di gestione. Questa operazione impone alcuni requisiti nell'app per gestire determinati rischi potenziali.

Il vantaggio principale del modello di associazione D3D12 è che consente alle app di modificare spesso le associazioni di trame, senza costi elevati in termini di prestazioni della CPU. Altri vantaggi sono che gli shader hanno accesso a un numero molto elevato di risorse. gli shader non devono essere in grado di stabilire in anticipo quante risorse saranno associate e che è possibile usare un modello di associazione di risorse unificato indipendentemente dall'hardware o dal flusso di contenuto delle app.

Per migliorare le prestazioni, il modello di associazione non richiede al sistema di tenere traccia dei binding che un'app ha richiesto alla GPU per l'uso ed è disponibile un'integrazione pulita tra gli elenchi di comandi di binding e multithread.

Le sezioni seguenti elencano alcune delle modifiche apportate al modello di associazione delle risorse a partire da D3D11.

-   [Gestione della residenza di memoria separata dall'associazione](#memory-residency-management-separated-from-binding)
-   [Gestione della durata degli oggetti separata dall'associazione](#object-lifetime-management-separated-from-binding)
-   [Rilevamento dello stato delle risorse del driver separato dal binding](#driver-resource-state-tracking-separated-from-binding)
-   [Sincronizzazione della memoria mappata GPU CPU separata dal binding](#cpu-gpu-mapped-memory-synchronization-separated-from-binding)
-   [Argomenti correlati](#related-topics)

## <a name="memory-residency-management-separated-from-binding"></a>Gestione della residenza di memoria separata dall'associazione

Le applicazioni hanno il controllo esplicito sulle superfici che devono essere disponibili per la GPU da usare direttamente (chiamato "residente"). Viceversa, possono applicare altri Stati alle risorse, ad esempio renderli esplicitamente non residenti o consentire al sistema operativo di scegliere alcune classi di applicazioni che richiedono un footprint di memoria minimo. Il punto importante è che la gestione dell'applicazione di ciò che è residente è completamente separata dal modo in cui fornisce l'accesso alle risorse agli shader.

Il disaccoppiamento della gestione della residenza dal meccanismo per concedere agli shader l'accesso alle risorse riduce il costo del sistema o dell'hardware per il rendering poiché il sistema operativo non deve esaminare costantemente lo stato dell'associazione locale per sapere cosa fare. Inoltre, non è più necessario che gli shader conoscano le superfici esatte a cui possono fare riferimento, purché l'intero set di risorse eventualmente accessibili sia stato reso residente in anticipo.

## <a name="object-lifetime-management-separated-from-binding"></a>Gestione della durata degli oggetti separata dall'associazione

Diversamente dalle API precedenti, il sistema non tiene più traccia delle associazioni di risorse alla pipeline. Questa operazione consente al sistema di mantenere le risorse attive rilasciate dall'applicazione, perché ancora fanno riferimento a un lavoro GPU in attesa.

Prima di liberare qualsiasi risorsa, ad esempio una trama, le applicazioni devono ora verificare che la GPU abbia completato il riferimento. Questo significa che prima che un'applicazione possa liberare in modo sicuro una risorsa, la GPU deve avere completato l'esecuzione dell'elenco dei comandi che fa riferimento alla risorsa.

## <a name="driver-resource-state-tracking-separated-from-binding"></a>Rilevamento dello stato delle risorse del driver separato dal binding

Il sistema non controlla più le associazioni di risorse per capire quando si sono verificate le transizioni di risorse che richiedono un driver o un lavoro GPU aggiuntivo. Un esempio comune per molte GPU e driver è che è necessario rilevare quando una superficie passa dall'uso come visualizzazione di destinazione di rendering (RTV) a Shader Resource View (SRV). Le applicazioni devono ora identificare quando si verificano transizioni di risorse che il sistema potrebbe preoccuparsi di eseguire tramite API dedicate.

## <a name="cpu-gpu-mapped-memory-synchronization-separated-from-binding"></a>Sincronizzazione della memoria mappata GPU CPU separata dal binding

Il sistema non controlla più le associazioni di risorse per capire se è necessario ritardare il rendering perché dipende da una risorsa di cui è stato eseguito il mapping per l'accesso alla CPU, ma non ne è ancora stato eseguito il mapping. Le applicazioni ora hanno la responsabilità di sincronizzare gli accessi alla memoria CPU e GPU. Per semplificare questa operazione, il sistema fornisce meccanismi che consentono all'applicazione di richiedere la sospensione di un thread della CPU fino al completamento del lavoro. Il polling può essere eseguito anche se è meno efficiente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Associazione di risorse](resource-binding.md)
</dt> </dl>

 

 





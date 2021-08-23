---
title: Differenze nel modello di associazione rispetto a Direct3D 11
description: Una delle principali decisioni di progettazione alla base dell'associazione DirectX12 è separarla da altre attività di gestione. In questo modo l'app deve soddisfare alcuni requisiti per gestire determinati potenziali rischi.
ms.assetid: 3EE7E9AE-203D-40D4-9F12-4313ED179035
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a625bd1b79766990658feba9bf18ddf7f46c3788ca20aea1de0b4ab80ae0a71f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632523"
---
# <a name="differences-in-the-binding-model-from-direct3d-11"></a>Differenze nel modello di associazione rispetto a Direct3D 11

Una delle principali decisioni di progettazione alla base dell'associazione DirectX12 è separarla da altre attività di gestione. In questo modo l'app deve soddisfare alcuni requisiti per gestire determinati potenziali rischi.

Il vantaggio principale del modello di associazione D3D12 è che consente alle app di modificare spesso le associazioni trame, senza un costo elevato per le prestazioni della CPU. Altri vantaggi sono che gli shader hanno accesso a un numero molto elevato di risorse, gli shader non devono sapere in anticipo quante risorse verranno associate e che un modello di associazione di risorse unificato può essere usato indipendentemente dall'hardware o dal flusso del contenuto delle app.

Per migliorare le prestazioni, il modello di associazione non richiede al sistema di tenere traccia delle associazioni che un'app ha richiesto l'uso della GPU ed è disponibile un'integrazione pulita tra l'associazione e gli elenchi di comandi multi-thread.

Le sezioni seguenti elencano alcune delle modifiche apportate al modello di associazione di risorse dopo D3D11.

-   [Gestione della residenza della memoria separata dall'associazione](#memory-residency-management-separated-from-binding)
-   [Gestione della durata degli oggetti separata dall'associazione](#object-lifetime-management-separated-from-binding)
-   [Rilevamento dello stato della risorsa del driver separato dall'associazione](#driver-resource-state-tracking-separated-from-binding)
-   [Sincronizzazione della memoria mappata alla GPU della CPU separata dall'associazione](#cpu-gpu-mapped-memory-synchronization-separated-from-binding)
-   [Argomenti correlati](#related-topics)

## <a name="memory-residency-management-separated-from-binding"></a>Gestione della residenza della memoria separata dall'associazione

Le applicazioni hanno il controllo esplicito sulle superfici che devono essere disponibili per l'uso diretto da parte della GPU (detto "residente"). Al contrario, possono applicare altri stati alle risorse, ad esempio renderle non residenti in modo esplicito o lasciare che il sistema operativo scenda per determinate classi di applicazioni che richiedono un footprint di memoria minimo. Il punto importante è che la gestione dell'applicazione di ciò che è residente è completamente disaccodata dal modo in cui fornisce l'accesso alle risorse agli shader.

La separazione della gestione della residenza dal meccanismo per concedere agli shader l'accesso alle risorse riduce il costo di sistema/hardware per il rendering perché il sistema operativo non deve controllare costantemente lo stato di associazione locale per sapere cosa rendere residente. Inoltre, gli shader non devono più conoscere le superfici esatte a cui devono fare riferimento, purché l'intero set di risorse possibilmente accessibili sia stato reso residente in anticipo.

## <a name="object-lifetime-management-separated-from-binding"></a>Gestione della durata degli oggetti separata dall'associazione

A differenza delle API precedenti, il sistema non tiene più traccia delle associazioni di risorse alla pipeline. Usato per consentire al sistema di mantenere in vita le risorse rilasciate dall'applicazione perché vi fa ancora riferimento il lavoro gpu in sospeso.

Prima di liberare una risorsa, ad esempio una trama, le applicazioni devono ora assicurarsi che la GPU abbia completato il riferimento. Ciò significa che prima che un'applicazione possa liberare in modo sicuro una risorsa, la GPU deve aver completato l'esecuzione dell'elenco di comandi che fa riferimento alla risorsa.

## <a name="driver-resource-state-tracking-separated-from-binding"></a>Rilevamento dello stato della risorsa del driver separato dall'associazione

Il sistema non controlla più le associazioni di risorse per comprendere quando si sono verificate transizioni di risorse che richiedono un lavoro aggiuntivo del driver o della GPU. Un esempio comune per molte GPU e driver è la necessità di sapere quando una superficie passa dall'uso come visualizzazione di destinazione di rendering (RTV) a Shader Resource View (SRV). Le applicazioni stesse devono ora identificare quando si verificano transizioni di risorse che potrebbero interessare al sistema tramite API dedicate.

## <a name="cpu-gpu-mapped-memory-synchronization-separated-from-binding"></a>Sincronizzazione della memoria mappata alla GPU della CPU separata dall'associazione

Il sistema non controlla più le associazioni di risorse per capire se il rendering deve essere ritardato perché dipende da una risorsa di cui è stato eseguito il mapping per l'accesso alla CPU ma non è stato ancora decompresso. Le applicazioni hanno ora la responsabilità di sincronizzare gli accessi alla memoria di CPU e GPU. A tale scopo, il sistema fornisce meccanismi che consentono all'applicazione di richiedere la sospensione di un thread della CPU fino al completamento del lavoro. È anche possibile eseguire il polling, ma può essere meno efficiente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Associazione di risorse](resource-binding.md)
</dt> </dl>

 

 





---
title: Architettura del WFP
description: Questa sezione offre una breve panoramica dell'architettura Windows Filtering Platform.
ms.assetid: 17a90f5c-ef82-4b14-b7f1-dd025d5f7303
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41989a11ff5412b3185f6987f9588f0309c3fde3ca386c71e4613ab6bc8237f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766606"
---
# <a name="wfp-architecture"></a>Architettura del WFP

La figura seguente illustra l'architettura di base di Windows Filtering Platform (WFP).

![Architettura di base del diagramma della piattaforma di filtro di Windows](images/wfp-architecture.png)

## <a name="filter-engine"></a>Motore di filtro

Il motore di filtro contiene un componente in modalità utente e un componente in modalità kernel, che insieme eseguono tutte le operazioni di filtro sui dati di rete. Il motore di filtro contiene più livelli di filtro che vengono mappati in modo libero ai livelli dello stack di rete del sistema operativo. I livelli del motore di filtro sono suddivisi in livelli in modalità utente e livelli in modalità kernel in base al componente del motore di filtro proprietario.

Il componente in modalità utente esegue il filtro RPC e IPsec. Il motore di filtro contiene circa 10 livelli di filtro in modalità utente.

Il componente in modalità kernel esegue il filtro a livello di rete e trasporto dello stack TC/IP. Questo componente chiama anche le funzioni callout disponibili durante il processo [di](basic-operation.md) classificazione. Il motore di filtro contiene circa 50 livelli di filtro in modalità kernel.

Per [**una descrizione di**](management-filtering-layer-identifiers-.md) ogni livello del motore di filtro, vedere Identificatori dei livelli di filtro.

## <a name="base-filtering-engine"></a>Base Filtering Engine

Il Base Filtering Engine (BFE) è un servizio in modalità utente (bfe.dll in esecuzione in un svchost.exe processo) che coordina i componenti WFP. Le attività principali eseguite da BFE sono l'aggiunta e la rimozione di filtri dal sistema, l'archiviazione della configurazione dei filtri e l'applicazione della sicurezza della configurazione wfp. Le applicazioni comunicano con BFE tramite le [funzioni di gestione del WFP.](fwp-mgmt-functions.md)

## <a name="callout-drivers"></a>Driver callout

I driver callout forniscono funzionalità di filtro aggiuntive aggiungendo funzioni di callout personalizzate al motore di filtro in uno o più livelli di filtro in modalità kernel. I callout supportano l'ispezione approfondita, il pacchetto e la modifica del flusso. Dopo che un driver di callout ha aggiunto le funzioni di callout al motore di filtro, i filtri che specificano una determinata funzione di callout del driver possono essere aggiunti al processo di filtro. Tali filtri possono essere aggiunti da un'applicazione di gestione in modalità utente o dal driver di callout stesso. L'interfaccia in modalità kernel, disponibile nel kit di sviluppo Windows, deve essere usata solo quando necessario e non in sostituzione dell'API in modalità utente.

> [!Note]  
> Per altre informazioni sui driver callout, vedere la sezione Windows Filtering Platform di [Windows Development Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2).

 

La Windows Filtering Platform include una serie di funzioni callout predefinite che possono essere usate per la comunicazione sicura dei dati IPsec, le impostazioni di filtro con stato e il filtro in modalità maschera. Per un elenco completo delle funzioni [**di callout incorporate,**](built-in-callout-identifiers.md) vedere Identificatori callout predefiniti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello a oggetti](object-model.md)
</dt> <dt>

[Operazione WFP](basic-operation.md)
</dt> <dt>

[Windows Filtro dei driver callout della piattaforma - Guida alla progettazione](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[Windows Filtro dei driver callout della piattaforma - Informazioni di riferimento](/windows-hardware/drivers/ddi/_netvista/)
</dt> </dl>

 

 
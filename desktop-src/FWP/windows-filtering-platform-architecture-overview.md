---
title: Architettura WFP
description: In questa sezione viene fornita una breve panoramica dell'architettura di piattaforma filtro Windows.
ms.assetid: 17a90f5c-ef82-4b14-b7f1-dd025d5f7303
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8740fed254aca97ab77566e2a7f0ace9a6679d56
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104223849"
---
# <a name="wfp-architecture"></a>Architettura WFP

Nella figura seguente viene illustrata l'architettura di base di Windows Filtering Platform (PAM).

![architettura di base del diagramma della piattaforma filtro Windows](images/wfp-architecture.png)

## <a name="filter-engine"></a>Motore di filtro

Il motore di filtro contiene un componente in modalità utente e un componente in modalità kernel, che insieme eseguono tutte le operazioni di filtro sui dati di rete. Il motore di filtro contiene più livelli di filtro che vengono mappati in modo libero ai livelli dello stack di rete del sistema operativo. I livelli del motore di filtro sono divisi in livelli in modalità utente e livelli in modalità kernel basati sul componente del motore di filtro che li possiede.

Il componente in modalità utente esegue il filtro RPC e IPsec. Il motore di filtro contiene circa 10 livelli di filtro in modalità utente.

Il componente in modalità kernel esegue il filtro ai livelli di rete e trasporto dello stack TC/IP. Questo componente chiama anche le funzioni di callout disponibili durante il processo di [classificazione](basic-operation.md) . Il motore di filtro contiene circa 50 livelli di filtro in modalità kernel.

Vedere [**filtro degli identificatori di livello**](management-filtering-layer-identifiers-.md) per una descrizione di ognuno dei livelli del motore di filtro.

## <a name="base-filtering-engine"></a>Base Filtering Engine

Il motore di filtro di base (BFE) è un servizio in modalità utente (bfe.dll in esecuzione in un processo di svchost.exe) che coordina i componenti Pam. Le attività principali eseguite da BFE sono l'aggiunta e la rimozione di filtri dal sistema, l'archiviazione della configurazione del filtro e l'applicazione della sicurezza della configurazione di Pam. Le applicazioni comunicano con BFE tramite le [funzioni di gestione del PAM](fwp-mgmt-functions.md).

## <a name="callout-drivers"></a>Driver di callout

I driver di callout forniscono funzionalità di filtro aggiuntive aggiungendo funzioni di callout personalizzate al motore di filtro in uno o più livelli di filtro in modalità kernel. I callout supportano l'ispezione approfondita e il pacchetto, nonché la modifica dei flussi. Dopo che un driver di callout ha aggiunto le funzioni di callout al motore di filtro, è possibile aggiungere filtri che specificano la funzione di callout di un determinato driver al processo di filtraggio. Tali filtri possono essere aggiunti da un'applicazione di gestione in modalità utente o dal driver di callout. L'interfaccia in modalità kernel, fornita in Windows Development Kit, deve essere utilizzata solo se necessario e non come sostituto per l'API in modalità utente.

> [!Note]  
> Per ulteriori informazioni sui driver di callout, vedere la sezione Windows Filtering Platform di [Windows Development Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2).

 

La piattaforma filtro Windows include una serie di funzioni di callout predefinite che possono essere utilizzate per la comunicazione dati protetta IPsec, le impostazioni di filtro con stato e il filtro in modalità stealth. Per un elenco completo delle funzioni di callout predefinite, vedere [**identificatori di callout predefiniti**](built-in-callout-identifiers.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modello a oggetti](object-model.md)
</dt> <dt>

[Operazione PAM](basic-operation.md)
</dt> <dt>

[Driver di callout della piattaforma filtro Windows-Guida alla progettazione](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2)
</dt> <dt>

[Driver di callout della piattaforma filtro Windows-informazioni di riferimento](/windows-hardware/drivers/ddi/_netvista/)
</dt> </dl>

 

 
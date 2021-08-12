---
description: Interfacce di streaming multimediale di base
ms.assetid: a94dbb64-dfca-4c24-8c11-761835faf8a8
title: Interfacce di streaming multimediale di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de5268855231169c6c0a7ffab02aa5145a7c1813511421b04b2420773e1588ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662921"
---
# <a name="base-multimedia-streaming-interfaces"></a>Interfacce di streaming multimediale di base

> [!Note]  
> Queste API sono deprecate. Le applicazioni devono usare il [**filtro Sample Grabber**](sample-grabber-filter.md) o implementare un filtro personalizzato per ottenere i dati da un grafico DirectShow filtro personalizzato.

 

Le interfacce di streaming multimediale di base offrono un modo programmatico per accedere ai flussi multimediali. Tuttavia, l'uso di un'interfaccia di base per accedere a un tipo specifico di dati può limitare la quantità di controllo sui dati, pertanto gli sviluppatori di contenuti multimediali devono creare versioni derivate di queste interfacce che offrono un controllo più potente sulle funzionalità univoche del tipo di supporto.



| Interfaccia                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) | Definisce come accedere all'oggetto flusso multimediale di livello superiore. Questo oggetto contiene e fornisce l'accesso ad altri oggetti flusso. [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) include metodi che enumerano o recuperano flussi specifici, oltre a controllare la durata totale del flusso e la ricerca all'interno del flusso.                                                                                                       |
| [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)           | Definisce un oggetto flusso generico. Usare i relativi metodi per recuperare un puntatore al flusso, ottenere informazioni sul flusso e creare esempi dai dati del flusso. È anche possibile creare esempi di flussi condivisi, a cui possono accedere più flussi senza duplicare i dati dell'esempio.                                                                                                                                                  |
| [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample)         | Controlla il comportamento di un esempio di flusso specifico. È possibile recuperare il flusso che ha creato l'esempio, controllare l'ora di inizio e di fine e lo stato di completamento dell'esempio ed eseguire una funzione definita dall'utente sull'esempio stesso (tramite il [**metodo Update).**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) In genere, il metodo Update elabora i dati di esempio in modo appropriato, ad esempio per il rendering dei dati video o per la riproduzione di dati audio. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elenco di interfacce di streaming multimediale](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 




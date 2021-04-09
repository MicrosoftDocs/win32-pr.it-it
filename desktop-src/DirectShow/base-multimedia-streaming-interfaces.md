---
description: Interfacce di streaming multimediali di base
ms.assetid: a94dbb64-dfca-4c24-8c11-761835faf8a8
title: Interfacce di streaming multimediali di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b715a68bd65a2fa3a3923edf10f0e2d1f6c22edb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968974"
---
# <a name="base-multimedia-streaming-interfaces"></a>Interfacce di streaming multimediali di base

> [!Note]  
> Queste API sono deprecate. Le applicazioni devono usare il filtro [**grabber di esempio**](sample-grabber-filter.md) o implementare un filtro personalizzato per ottenere i dati da un grafico filtro DirectShow.

 

Le interfacce di streaming multimediali di base forniscono un modo programmatico per accedere ai flussi multimediali. Tuttavia, l'uso di un'interfaccia di base per accedere a un tipo specifico di dati può limitare la quantità di controllo sui dati, quindi gli sviluppatori di contenuti multimediali devono creare versioni derivate di queste interfacce che offrono un controllo più efficace sulle funzionalità esclusive del tipo di supporto.



| Interfaccia                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) | Definisce come accedere all'oggetto flusso multimediale di livello più alto. Questo oggetto contiene e fornisce l'accesso ad altri oggetti del flusso. [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) dispone di metodi che enumerano o recuperano flussi specifici, oltre a controllare la durata totale del flusso e la ricerca all'interno del flusso.                                                                                                       |
| [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)           | Definisce un oggetto flusso generico. Usare i relativi metodi per recuperare un puntatore al flusso, ottenere informazioni sul flusso e creare esempi dai dati del flusso. È anche possibile creare esempi di flusso condiviso a cui possono accedere più flussi senza duplicare i dati dell'esempio.                                                                                                                                                  |
| [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample)         | Controlla il comportamento di un esempio di flusso specifico. È possibile recuperare il flusso che ha creato l'esempio, controllare l'ora di inizio e di fine dell'esempio e lo stato di completamento ed eseguire una funzione definita dall'utente nell'esempio stesso (tramite il metodo [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) ). In genere, il metodo Update elabora i dati di esempio in modo appropriato, ad esempio il rendering dei dati video o la riproduzione di dati audio. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elenco di interfacce di streaming multimediali](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 




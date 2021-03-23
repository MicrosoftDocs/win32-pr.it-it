---
title: Riepilogo di configurabilità heap descrittore
description: Nella tabella seguente sono riepilogate le informazioni sullo shader e sul supporto dell'heap visibile non shader.
ms.assetid: DF266915-6224-4FFB-BE3E-34A44F7318DD
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ce6718e95b774f83d25a84476616643c77c119
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104409"
---
# <a name="descriptor-heap-configurability-summary"></a>Riepilogo di configurabilità heap descrittore

Nella tabella seguente sono riepilogate le informazioni sullo shader e sul supporto dell'heap visibile non shader.



|                               | Heap descrittore visibile dello shader                                                 | Heap descrittore non visibile per shader                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tipi di heap supportati          | CBV \_ SRV \_ UAV, campionatore                                                         | Tutti                                                                                                                                                                                                                                                                                                                                                                 |
| Proprietà della pagina CPU supportate | NON \_ disponibile, scrittura \_ combinata                                                 | Scrivi \_ indietro                                                                                                                                                                                                                                                                                                                                                         |
| Gestione della residenza per app   | Sì, app responsabile                                                           | Non applicabile (non visibile GPU).                                                                                                                                                                                                                                                                                                                                   |
| Supporto per la modifica del descrittore       | Solo destinazione di copia, tramite l'aggiornamento dell'elenco dei comandi e/o la copia della CPU se la CPU è visibile. | CPU di sola lettura e scrittura. Nessun accesso diretto alla GPU. Può essere usato per la copia immediata della CPU (come origine e destinazione). Può essere usato come origine di aggiornamento in un elenco di comandi. in questo modo, i descrittori verranno copiati nell'archiviazione dell'elenco dei comandi durante il record dell'elenco dei comandi. Durante l'esecuzione, la copia archiviata verrà copiata nella destinazione, che deve essere un heap visibile dello shader. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Heap descrittore](descriptor-heaps.md)
</dt> </dl>

 

 





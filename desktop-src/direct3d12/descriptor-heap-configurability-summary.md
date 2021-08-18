---
title: Riepilogo della configurazione dell'heap dei descrittori
description: La tabella seguente riepiloga le informazioni sul supporto degli heap visibili agli shader e non shader.
ms.assetid: DF266915-6224-4FFB-BE3E-34A44F7318DD
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c974516a09552fc5e3b301ca3ef91a3aea3d1752d0177f34d5fc94928ee8f293
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530553"
---
# <a name="descriptor-heap-configurability-summary"></a>Riepilogo della configurazione dell'heap dei descrittori

La tabella seguente riepiloga le informazioni sul supporto degli heap visibili agli shader e non shader.



|                               | Heap descrittore visibile shader                                                 | Heap del descrittore non visibile allo shader                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Tipi di heap supportati**          | CBV \_ SRV \_ UAV, Sampler                                                         | Tutti                                                                                                                                                                                                                                                                                                                                                                 |
| **Proprietà della pagina CPU supportate** | NON \_ DISPONIBILE, COMBINAZIONE DI \_ SCRITTURA                                                 | WRITE \_ BACK                                                                                                                                                                                                                                                                                                                                                         |
| **Gestione della residenza per app**   | Sì, responsabile dell'app                                                           | Non applicabile (non visibile alla GPU).                                                                                                                                                                                                                                                                                                                                   |
| **Supporto per la modifica del descrittore**       | Copiare solo la destinazione, tramite l'aggiornamento dell'elenco dei comandi e/o la copia della CPU se la CPU è visibile. | Solo lettura e scrittura della CPU. Nessun accesso diretto alla GPU. Può essere usato per la copia immediata della CPU (come origine e destinazione). Può essere usato come origine di aggiornamento in un elenco di comandi. I descrittori verranno copiati nell'archivio dell'elenco dei comandi durante il record dell'elenco dei comandi. Durante l'esecuzione, la copia archiviata verrà copiata nella destinazione, che deve essere un heap visibile allo shader. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Heap dei descrittori](descriptor-heaps.md)
</dt> </dl>

 

 





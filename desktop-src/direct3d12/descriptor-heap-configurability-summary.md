---
title: Riepilogo della configurazione dell'heap dei descrittori
description: La tabella seguente riepiloga le informazioni sul supporto degli heap visibili agli shader e non shader.
ms.assetid: DF266915-6224-4FFB-BE3E-34A44F7318DD
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cfef479e88e5c77df0732113597a4742ecb909c
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335571"
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

 

 





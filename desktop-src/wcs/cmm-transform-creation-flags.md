---
title: Flag di creazione della trasformazione CMM
description: CMM usare i flag di creazione della trasformazione come hint per la creazione di una trasformazione colore. Per determinare il modo migliore di usare questi flag, spetta alla CMM.
ms.assetid: f3942929-272c-4f08-98ac-a4d14d2f6ac4
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 852ef5c080c361bfffb6915d808787d46e63ba5c
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/02/2021
ms.locfileid: "106320183"
---
# <a name="cmm-transform-creation-flags"></a>Flag di creazione della trasformazione CMM

CMM usare i flag di creazione della trasformazione come hint per la creazione di una trasformazione colore. Per determinare il modo migliore di usare questi flag, spetta alla CMM.

Tutte le funzioni che utilizzano questi flag passano o ricevono valori di flag tramite un parametro denominato *dwFlags*. La **parola** più ordinata di *dwFlags* deve essere impostata su un valore della tabella seguente.



| Costante                    | Descrizione                                                                                                                                  |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Abilita \_ \_ controllo gamut     | Usare questa trasformazione per il controllo della gamma.                                                                                                       |
| USA \_ \_ colorimetrico relativo | Non mantenere il punto bianco. Se la gamma di output non supporta un determinato colore, utilizzare il colore supportato più vicino. Vedere rendering di Intent. |
| \_conversione veloce             | Cerca solo il colore. Non interpolare il colore.                                                                                            |
| PRESERVEBLACK               | Inserisce il GMMP di generazione nera appropriato come ultimo GMMP nella sequenza di trasformazione                                                     |
| WCS \_ Always                 | Usare il percorso del codice WCS anche per le trasformazioni ICC.                                                                                               |
| trasformazione SEQUENZIAle \_       | Flag di creazione trasformazione per la creazione di una trasformazione colore sequenziale (non ottimizzata).                                                           |



 

La **parola** più bassa può avere uno dei valori costanti seguenti.



| Costante     | Descrizione                                                                                        |
|--------------|----------------------------------------------------------------------------------------------------|
| modalità di prova \_  | La trasformazione verrà utilizzata per visualizzare l'anteprima dell'immagine. Qualità dell'immagine ridotta.                                    |
| \_modalità normale | La trasformazione verrà usata per la visualizzazione dell'immagine normale. Qualità media dell'immagine.                            |
| \_modalità migliore   | La trasformazione verrà usata per la visualizzazione dell'immagine di qualità massima possibile sul dispositivo di destinazione. |



 

Passaggio dalla \_ modalità di prova alla \_ modalità migliore, la qualità di output migliora in genere e trasforma la velocità diminuisce.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti di base sulla gestione dei colori](basic-color-management-concepts.md)
</dt> <dt>

[Costanti ICM](wcs-constants.md)
</dt> </dl>

 

 





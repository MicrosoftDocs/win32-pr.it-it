---
description: Uno spazio delle coordinate è uno spazio planare basato sul sistema di coordinate cartesiano.
ms.assetid: 1a232030-8561-4b57-b274-dca0a8b3e3a1
title: Trasformazione degli spazi delle coordinate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27ffaec6a6dab09b841f95f4704048a4145d2b2bd84c232658b2b659d26d37be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965161"
---
# <a name="transformation-of-coordinate-spaces"></a>Trasformazione degli spazi delle coordinate

Uno *spazio delle coordinate* è uno spazio planare basato sul sistema di coordinate cartesiano. Questo sistema consente di specificare la posizione di ogni punto su un piano. Richiede due assi perpendicolari e di lunghezza uguale. Nella figura seguente viene illustrato uno spazio delle coordinate.

![illustrazione di uno spazio delle coordinate, che mostra l'origine, entrambi gli assi e i valori massimo e minimo di ogni asse](images/cstrn-07.png)

Il sistema supporta quattro spazi delle coordinate, come descritto nella tabella seguente.



| Spazio delle coordinate | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| world            | Utilizzato facoltativamente come spazio delle coordinate iniziale per le trasformazioni grafiche. Consente scalabilità, traslazione, rotazione, traslazione e reflection. Lo spazio mondiale misura 2^32 unità di altezza per 2^32 unità di larghezza.                                                                                                                                                                                                                                                                |
| pagina             | Utilizzato come spazio successivo dopo lo spazio globale o come spazio iniziale per le trasformazioni grafiche. Imposta la modalità di mapping. Lo spazio pagina misura anche 2^32 unità di altezza per 2^32 unità di larghezza.                                                                                                                                                                                                                                                                              |
| device           | Utilizzato come spazio successivo dopo lo spazio della pagina. Consente solo la traduzione, che garantisce che l'origine dello spazio del dispositivo sia mappata alla posizione corretta nello spazio fisico del dispositivo. Lo spazio del dispositivo misura 2^27 unità di altezza per 2^27 unità di larghezza.                                                                                                                                                                                                                                          |
| dispositivo fisico  | Spazio finale (output) per le trasformazioni grafiche. In genere si riferisce all'area client della finestra dell'applicazione. Tuttavia, può includere anche l'intero desktop, una finestra completa (inclusi il frame, la barra del titolo e la barra dei menu) o una pagina di carta della stampante o del tracciatore, a seconda della funzione che ha ottenuto l'handle per il contesto di dispositivo. Le dimensioni del dispositivo fisico variano in base alle dimensioni impostate dalla tecnologia di visualizzazione, stampante o tracciatore. |



 

Lo spazio della pagina funziona con lo spazio del dispositivo per fornire alle applicazioni unità indipendenti dal dispositivo, ad esempio millimetri e pollici. Questa panoramica fa riferimento sia allo spazio del mondo che allo spazio della pagina come spazio logico.

Per rappresentare l'output in un dispositivo fisico, il sistema copia (o esegue il mapping) un'area rettangolare da uno spazio delle coordinate all'altro usando una trasformazione fino a quando l'output non viene visualizzato per intero nel dispositivo fisico. Il mapping inizia nello spazio dell'mondo dell'applicazione se l'applicazione ha chiamato la [**funzione SetWorldTransform;**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) In caso contrario, il mapping viene eseguito nello spazio della pagina. Quando il sistema copia ogni punto all'interno dell'area rettangolare da uno spazio a un altro, applica un algoritmo denominato trasformazione. Una *trasformazione* modifica (o trasforma) le dimensioni, l'orientamento e la forma degli oggetti copiati da uno spazio delle coordinate a un altro. Sebbene una trasformazione influisca su un oggetto nel suo complesso, viene applicata a ogni punto o a ogni riga dell'oggetto.

La figura seguente illustra una trasformazione tipica eseguita usando la [**funzione SetWorldTransform.**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform)

![illustrazione che mostra un rettangolo che cambia le dimensioni e la posizione nello spazio del mondo, nello spazio della pagina, nello spazio del dispositivo e nel dispositivo](images/cstrn-08.png)

 

 




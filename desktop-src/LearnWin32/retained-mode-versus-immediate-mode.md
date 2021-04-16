---
title: Modalità mantenuta rispetto alla modalità immediata
description: Le API grafiche possono essere divise in API in modalità mantenuta e in modalità immediata.
ms.assetid: 0a98e8ee-4bc1-490c-867e-42bceae8a1f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec3b89cd300f957211a9d4990c35ccbb70fa2b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104551441"
---
# <a name="retained-mode-versus-immediate-mode"></a>Modalità mantenuta rispetto alla modalità immediata

Le API grafiche possono essere divise in API in *modalità mantenuta* e in *modalità immediata* . Direct2D è un'API in modalità immediata. Windows Presentation Foundation (WPF) è un esempio di un'API in modalità mantenuta.

Un'API in modalità mantenuta è dichiarativa. L'applicazione crea una scena dalle primitive grafiche, ad esempio forme e linee. La libreria grafica archivia un modello della scena in memoria. Per disegnare un frame, la libreria grafica trasforma la scena in un set di comandi di disegno. Tra i frame, la libreria grafica mantiene la scena in memoria. Per modificare gli elementi di cui viene eseguito il rendering, l'applicazione emette un comando per aggiornare la scena, ad esempio per aggiungere o rimuovere una forma. La libreria è quindi responsabile del ridisegno della scena.

![diagramma che mostra la grafica in modalità mantenuta.](images/graphics06.png)

Un'API in modalità immediata è procedurale. Ogni volta che viene disegnato un nuovo frame, l'applicazione invia direttamente i comandi di disegno. La libreria grafica non archivia un modello di scena tra i frame. Al contrario, l'applicazione tiene traccia della scena.

![diagramma che mostra la grafica in modalità immediata.](images/graphics07.png)

Le API in modalità mantenuta possono essere più semplici da usare, perché l'API esegue più attività, ad esempio l'inizializzazione, la manutenzione dello stato e la pulizia. D'altra parte, sono spesso meno flessibili, perché l'API impone il proprio modello di scena. Inoltre, un'API in modalità mantenuta può disporre di requisiti di memoria più elevati, perché deve fornire un modello di scena di uso generale. Con un'API in modalità immediata, è possibile implementare le ottimizzazioni di destinazione.

## <a name="next"></a>Prossima

[Primo programma Direct2D](your-first-direct2d-program.md)

 

 





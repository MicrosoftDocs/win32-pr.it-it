---
description: Un'applicazione può usare il ritaglio e i tracciati per creare effetti grafici speciali. La figura seguente mostra una stringa di testo disegnata con un tipo di carattere Arial di grandi dimensioni.
ms.assetid: fda0d627-406c-44f9-9061-7aea3e2d7f66
title: Tracciati di ritaglio ed effetti grafici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c80605f4dc58846f3a9e8440801d46768384c103ff6e3f9df5e3d448d9b12aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038159"
---
# <a name="clip-paths-and-graphic-effects"></a>Tracciati di ritaglio ed effetti grafici

Un'applicazione può usare il ritaglio e i tracciati per creare effetti grafici speciali. La figura seguente mostra una stringa di testo disegnata con un tipo di carattere Arial di grandi dimensioni.

![illustrazione che mostra il testo nero su sfondo bianco](images/cspth-02.png)

La figura seguente mostra il risultato della selezione del testo come tracciato di ritaglio e del disegno di linee radiali per un cerchio il cui centro si trova sopra e a sinistra della stringa.

![illustrazione che mostra lo stesso testo, ma riempita con righe invece di nero a tinta unita](images/cspth-03.png)

> [!Note]  
> Prima di aggiungere testo creato con un tipo di carattere bitmap a un tracciato, L'interfaccia GDI (Graphics Device Interface) converte il tipo di carattere in un carattere vettoriale o di contorno.

 

Un'applicazione crea un percorso di ritaglio generando una parentesi di percorso e quindi chiamando la [**funzione SelectClipPath.**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) Dopo aver selezionato un tracciato di ritaglio in un controller di dominio, l'output viene visualizzato solo all'interno dei bordi del tracciato.

Oltre a creare effetti grafici speciali, i tracciati di ritaglio sono utili anche nelle applicazioni che salvano le immagini come metafile migliorati. Usando un tracciato di ritaglio, un'applicazione è in grado di garantire l'indipendenza del dispositivo perché le unità usate per specificare un percorso sono unità logiche.

 

 




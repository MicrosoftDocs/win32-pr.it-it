---
description: Un'applicazione può usare il ritaglio e i percorsi per creare effetti grafici speciali. Nella figura seguente viene illustrata una stringa di testo disegnata con un tipo di carattere Arial di grandi dimensioni.
ms.assetid: fda0d627-406c-44f9-9061-7aea3e2d7f66
title: Tracciare percorsi ed effetti grafici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8156a8670747175502b2385e6c24a340345a54f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528392"
---
# <a name="clip-paths-and-graphic-effects"></a>Tracciare percorsi ed effetti grafici

Un'applicazione può usare il ritaglio e i percorsi per creare effetti grafici speciali. Nella figura seguente viene illustrata una stringa di testo disegnata con un tipo di carattere Arial di grandi dimensioni.

![illustrazione che mostra il testo nero in uno sfondo bianco](images/cspth-02.png)

La figura seguente mostra il risultato della selezione del testo come tracciato di ritaglio e disegno di linee radiali per un cerchio il cui centro si trova sopra e a sinistra della stringa.

![illustrazione che mostra lo stesso testo, ma con righe invece di nero solido](images/cspth-03.png)

> [!Note]  
> Prima che Graphics Device Interface (GDI) Aggiunga il testo creato con un tipo di carattere bitmap in un percorso, il tipo di carattere viene convertito in un tipo di carattere vettoriale o contorno.

 

Un'applicazione crea un tracciato di ritaglio generando una parentesi del percorso e chiamando la funzione [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) . Dopo aver selezionato un tracciato di ritaglio in un controller di dominio, l'output viene visualizzato solo all'interno dei bordi del percorso.

Oltre a creare effetti grafici speciali, i percorsi di ritaglio sono utili anche nelle applicazioni che salvano le immagini come metafile avanzati. Usando un percorso di ritaglio, un'applicazione è in grado di garantire l'indipendenza del dispositivo perché le unità usate per specificare un percorso sono unità logiche.

 

 




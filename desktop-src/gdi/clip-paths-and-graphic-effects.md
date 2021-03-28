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
# <a name="clip-paths-and-graphic-effects"></a><span data-ttu-id="924ca-104">Tracciare percorsi ed effetti grafici</span><span class="sxs-lookup"><span data-stu-id="924ca-104">Clip Paths and Graphic Effects</span></span>

<span data-ttu-id="924ca-105">Un'applicazione può usare il ritaglio e i percorsi per creare effetti grafici speciali.</span><span class="sxs-lookup"><span data-stu-id="924ca-105">An application can use clipping and paths to create special graphic effects.</span></span> <span data-ttu-id="924ca-106">Nella figura seguente viene illustrata una stringa di testo disegnata con un tipo di carattere Arial di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="924ca-106">The following illustration shows a string of text drawn with a large Arial font.</span></span>

![illustrazione che mostra il testo nero in uno sfondo bianco](images/cspth-02.png)

<span data-ttu-id="924ca-108">La figura seguente mostra il risultato della selezione del testo come tracciato di ritaglio e disegno di linee radiali per un cerchio il cui centro si trova sopra e a sinistra della stringa.</span><span class="sxs-lookup"><span data-stu-id="924ca-108">The next illustration shows the result of selecting the text as a clip path and drawing radial lines for a circle whose center is located above and left of the string.</span></span>

![illustrazione che mostra lo stesso testo, ma con righe invece di nero solido](images/cspth-03.png)

> [!Note]  
> <span data-ttu-id="924ca-110">Prima che Graphics Device Interface (GDI) Aggiunga il testo creato con un tipo di carattere bitmap in un percorso, il tipo di carattere viene convertito in un tipo di carattere vettoriale o contorno.</span><span class="sxs-lookup"><span data-stu-id="924ca-110">Before graphics device interface (GDI) adds text created with a bitmapped font to a path, it converts the font to an outline or vector font.</span></span>

 

<span data-ttu-id="924ca-111">Un'applicazione crea un tracciato di ritaglio generando una parentesi del percorso e chiamando la funzione [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) .</span><span class="sxs-lookup"><span data-stu-id="924ca-111">An application creates a clip path by generating a path bracket and then calling the [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) function.</span></span> <span data-ttu-id="924ca-112">Dopo aver selezionato un tracciato di ritaglio in un controller di dominio, l'output viene visualizzato solo all'interno dei bordi del percorso.</span><span class="sxs-lookup"><span data-stu-id="924ca-112">After a clip path is selected into a DC, output only appears within the borders of the path.</span></span>

<span data-ttu-id="924ca-113">Oltre a creare effetti grafici speciali, i percorsi di ritaglio sono utili anche nelle applicazioni che salvano le immagini come metafile avanzati.</span><span class="sxs-lookup"><span data-stu-id="924ca-113">In addition to creating special graphics effects, clip paths are also useful in applications that save images as enhanced metafiles.</span></span> <span data-ttu-id="924ca-114">Usando un percorso di ritaglio, un'applicazione è in grado di garantire l'indipendenza del dispositivo perché le unità usate per specificare un percorso sono unità logiche.</span><span class="sxs-lookup"><span data-stu-id="924ca-114">By using a clip path, an application is able to ensure device independence because the units used to specify a path are logical units.</span></span>

 

 




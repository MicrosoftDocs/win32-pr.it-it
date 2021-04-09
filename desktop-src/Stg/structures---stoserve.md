---
title: Strutture-StoServe
description: Il foglio di lavoro consente di impacchettare il colore, la larghezza e le coordinate della penna in strutture INKDATA e di archiviarle in una matrice allocata in modo dinamico che gestisce in memoria.
ms.assetid: 25e68c39-5306-4ad6-85dd-a8a5e256abf0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9868f38d7915185b8d3511bd1bf6faa9c7a1e1b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955370"
---
# <a name="structures---stoserve"></a>Strutture-StoServe

Il foglio di lavoro consente di impacchettare il colore, la larghezza e le coordinate della penna in strutture **INKDATA** e di archiviarle in una matrice allocata in modo dinamico che gestisce in memoria.

## <a name="inkdata-structure"></a>Struttura INKDATA

Di seguito sono riportate le dichiarazioni per la struttura **INKDATA** da Paper. H.

``` syntax
// The types of Ink Data.
#define INKTYPE_NONE  0
#define INKTYPE_START 1
#define INKTYPE_DRAW  2
#define INKTYPE_STOP  3

  // The Ink Data structure.
  typedef struct _INKDATA
  {
    SHORT nType;            // Ink Type.
    SHORT nX;               // X-coordinate of ink point.
    SHORT nY;               // Y-coordinate of ink point.
    SHORT nWidth;           // Ink line width in pixels.
    COLORREF crColor;       // Ink color.
  } INKDATA;
```

Alla matrice dinamica di questi pacchetti **INKDATA** viene fatto riferimento da m \_ paInkData, un membro della classe di implementazione [**iPaper**](ipaper-methods.md) . La matrice viene creata all'interno del metodo **iPaper:: InitPaper** con un'allocazione iniziale. Per informazioni dettagliate, vedere il metodo **InitPaper** e il metodo di utilità NextSlot privato dell'implementazione di CIMPIPAPER in paper. H. I metodi [**InkStart**](inkstart-method.md), [**InkDraw**](inkdraw-method.md)e [**InkStop**](cguipaper-methods.md) usano NextSlot per ottenere nuovi slot nella matrice. La matrice viene espansa in modo dinamico da NextSlot in base alla necessità.

Il client chiama il metodo [**iPaper:: erase**](ipaper-methods.md) per cancellare il disegno corrente. Questo metodo non consente di riallocare la matrice. contrassegna semplicemente tutti i dati Ink correnti come INKTYPE \_ None e Reimposta l'indice di fine dei dati della matrice su zero.

Il client chiama i metodi [**iPaper:: Lock**](ipaper-methods.md) e **Unlock** per gestire la proprietà del documento per il disegno. Questi metodi vengono forniti per organizzare l'accesso tra più client al disegno contenuto in un documento condiviso.

## <a name="paper_properties-structure"></a>\_Struttura della proprietà paper

Il client chiama il metodo [**iPaper:: Resize**](ipaper-methods.md) per indicare al documento che l'utente ha ridimensionato il rettangolo di disegno corrente. I dati delle coordinate vengono conservati in una struttura di **\_ proprietà della carta** , archiviata con i dati di input penna quando tutti i dati cartacei vengono archiviati in un file composto.

Di seguito è riportata la dichiarazione delle **\_ proprietà della carta** da Paper. H.

``` syntax
#define PAPER_TITLE_SIZE 64
  typedef struct _PAPER_PROPERTIES
  {
    LONG lInkDataVersion;
    LONG lInkArraySize;
    COLORREF crWinColor;
    RECT WinRect;
    WCHAR wszTitle[PAPER_TITLE_SIZE];
    WCHAR wszAuthor[PAPER_TITLE_SIZE];
    WCHAR wszReserved1[PAPER_TITLE_SIZE];
    WCHAR wszReserved2[PAPER_TITLE_SIZE];
  } PAPER_PROPERTIES;
```

La struttura della **\_ Proprietà paper** è progettata in modo che i nuovi formati di dati Ink possano essere aggiunti in qualsiasi momento quando il componente DllPaper si evolve. L'interfaccia [**iPaper**](ipaper-methods.md) è sufficientemente generale da consentire a una versione successiva del componente DllPaper di archiviare un formato di dati Ink diverso durante l'implementazione della stessa interfaccia **iPaper** . Poiché i metodi di **iPaper** non dipendono da un formato di dati Ink specifico, una nuova versione del componente DllPaper che supporta un formato di dati Ink diverso può utilizzare la stessa interfaccia.

Le proprietà della carta archiviate in un file composto registrano la dimensione corrente della matrice di dati di input penna. È quindi possibile allocare le dimensioni corrette della matrice per contenere i dati dell'input penna letti dal file.

La struttura della **\_ Proprietà paper** archivia anche le dimensioni del rettangolo di disegno e del colore della finestra di sfondo della carta.

Sebbene non venga usato negli  / esempi **StoClien** di StoServe, è possibile archiviare anche un titolo del disegno e un nome di autore.

La data di creazione e le date dell'Ultima modifica non sono incluse nelle proprietà della carta, perché l'interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) usata per accedere ai file composti gestisce queste informazioni.

 

 





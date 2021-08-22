---
title: Strutture - StoServe
description: COPaper crea un pacchetto di colore, larghezza e coordinate della penna in strutture INKDATA e li archivia in una matrice allocata dinamicamente che gestisce in memoria.
ms.assetid: 25e68c39-5306-4ad6-85dd-a8a5e256abf0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f81b46f2f0a992f27ed405361734fe53db98cf9272697b88866451ef1d7d4b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796891"
---
# <a name="structures---stoserve"></a>Strutture - StoServe

COPaper crea un pacchetto di colore, larghezza e coordinate della penna in strutture **INKDATA** e li archivia in una matrice allocata dinamicamente che gestisce in memoria.

## <a name="inkdata-structure"></a>Struttura INKDATA

Di seguito sono riportate le dichiarazioni per la **struttura INKDATA** da PAPER.H.

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

La matrice dinamica di questi **pacchetti INKDATA** è a cui punta m paInkData, un membro della classe di implementazione \_ [**IPaper.**](ipaper-methods.md) La matrice viene creata all'interno **del metodo IPaper::InitPaper** con un'allocazione iniziale. Per informazioni dettagliate, vedere **il metodo InitPaper** e il metodo di utilità NextSlot privato dell'implementazione di CImpIPaper in PAPER.H. I [**metodi InkStart**](inkstart-method.md), [**InkDraw**](inkdraw-method.md)e [**InkStop**](cguipaper-methods.md) usano NextSlot per ottenere nuovi slot nella matrice. La matrice viene espansa dinamicamente da NextSlot in base alle necessità.

Il client chiama [**il metodo IPaper::Erase**](ipaper-methods.md) per cancellare il disegno corrente. Questo metodo non rialloca la matrice. contrassegna semplicemente tutti i dati dell'input penna correnti come INKTYPE NONE e reimposta l'indice di fine dati \_ della matrice su zero.

Il client chiama i [**metodi IPaper::Lock**](ipaper-methods.md) e **Unlock** per gestire la proprietà di COPaper per il disegno. Questi metodi vengono forniti per organizzare l'accesso tra più client al disegno contenuto in un COPaper condiviso.

## <a name="paper_properties-structure"></a>Struttura \_ PAPER PROPERTIES

Il client chiama il [**metodo IPaper::Resize**](ipaper-methods.md) per indicare a COPaper che l'utente ha ridimensionato il rettangolo della carta da disegno corrente. Questi dati delle coordinate vengono mantenuti in una struttura **PAPER \_ PROPERTIES,** che viene archiviata con i dati dell'input penna quando tutti i dati della carta vengono archiviati in un file composto.

Di seguito è riportata **la dichiarazione PAPER \_ PROPERTIES** di PAPER.H.

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

La **struttura \_ PAPER PROPERTIES** è progettata in modo che sia possibile aggiungere nuovi formati di dati input penna in qualsiasi momento man mano che il componente DllPaper si evolve. [**L'interfaccia IPaper**](ipaper-methods.md) è sufficientemente generica che una versione successiva del componente DllPaper può archiviare un formato dati input penna diverso durante l'implementazione della **stessa interfaccia IPaper.** Poiché i metodi di **IPaper** non dipendono da un formato dati input penna specifico, una nuova versione del componente DllPaper che supporta un formato dati input penna diverso può usare questa stessa interfaccia.

Le proprietà della carta archiviate in un file composto registrano le dimensioni correnti della matrice di dati dell'input penna. È quindi possibile allocare le dimensioni di matrice appropriate per contenere i dati dell'input penna letti dal file.

La **struttura PAPER \_ PROPERTIES** archivia anche le dimensioni del rettangolo di disegno e il colore della finestra di sfondo della superficie della carta.

Anche se non viene usato negli **esempi StoServe** / **StoClien,** è possibile archiviare anche un titolo di disegno e un nome di autore.

La data di creazione e le date dell'ultima modifica non sono incluse in queste proprietà del documento, perché [**l'interfaccia IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) usata per accedere ai file composti gestisce queste informazioni.

 

 





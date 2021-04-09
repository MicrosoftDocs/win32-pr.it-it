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
# <a name="structures---stoserve"></a><span data-ttu-id="b2edc-103">Strutture-StoServe</span><span class="sxs-lookup"><span data-stu-id="b2edc-103">Structures - StoServe</span></span>

<span data-ttu-id="b2edc-104">Il foglio di lavoro consente di impacchettare il colore, la larghezza e le coordinate della penna in strutture **INKDATA** e di archiviarle in una matrice allocata in modo dinamico che gestisce in memoria.</span><span class="sxs-lookup"><span data-stu-id="b2edc-104">COPaper packages the pen color, width, and coordinates into **INKDATA** structures and stores them in a dynamically allocated array that it manages in memory.</span></span>

## <a name="inkdata-structure"></a><span data-ttu-id="b2edc-105">Struttura INKDATA</span><span class="sxs-lookup"><span data-stu-id="b2edc-105">INKDATA Structure</span></span>

<span data-ttu-id="b2edc-106">Di seguito sono riportate le dichiarazioni per la struttura **INKDATA** da Paper. H.</span><span class="sxs-lookup"><span data-stu-id="b2edc-106">The following are the declarations for the **INKDATA** structure from PAPER.H.</span></span>

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

<span data-ttu-id="b2edc-107">Alla matrice dinamica di questi pacchetti **INKDATA** viene fatto riferimento da m \_ paInkData, un membro della classe di implementazione [**iPaper**](ipaper-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="b2edc-107">The dynamic array of these **INKDATA** packets is pointed to by m\_paInkData, a member of the [**IPaper**](ipaper-methods.md) implementation class.</span></span> <span data-ttu-id="b2edc-108">La matrice viene creata all'interno del metodo **iPaper:: InitPaper** con un'allocazione iniziale.</span><span class="sxs-lookup"><span data-stu-id="b2edc-108">The array is created within the **IPaper::InitPaper** method with an initial allocation.</span></span> <span data-ttu-id="b2edc-109">Per informazioni dettagliate, vedere il metodo **InitPaper** e il metodo di utilità NextSlot privato dell'implementazione di CIMPIPAPER in paper. H.</span><span class="sxs-lookup"><span data-stu-id="b2edc-109">For details, see the **InitPaper** method and the private NextSlot utility method of the CImpIPaper implementation in PAPER.H.</span></span> <span data-ttu-id="b2edc-110">I metodi [**InkStart**](inkstart-method.md), [**InkDraw**](inkdraw-method.md)e [**InkStop**](cguipaper-methods.md) usano NextSlot per ottenere nuovi slot nella matrice.</span><span class="sxs-lookup"><span data-stu-id="b2edc-110">The [**InkStart**](inkstart-method.md), [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) methods use NextSlot to obtain new slots in the array.</span></span> <span data-ttu-id="b2edc-111">La matrice viene espansa in modo dinamico da NextSlot in base alla necessità.</span><span class="sxs-lookup"><span data-stu-id="b2edc-111">The array is expanded dynamically by NextSlot as the need arises.</span></span>

<span data-ttu-id="b2edc-112">Il client chiama il metodo [**iPaper:: erase**](ipaper-methods.md) per cancellare il disegno corrente.</span><span class="sxs-lookup"><span data-stu-id="b2edc-112">The client calls the [**IPaper::Erase**](ipaper-methods.md) method to erase the current drawing.</span></span> <span data-ttu-id="b2edc-113">Questo metodo non consente di riallocare la matrice. contrassegna semplicemente tutti i dati Ink correnti come INKTYPE \_ None e Reimposta l'indice di fine dei dati della matrice su zero.</span><span class="sxs-lookup"><span data-stu-id="b2edc-113">This method does not reallocate the array; it simply marks all current ink data as INKTYPE\_NONE and resets the array's end-of-data index to zero.</span></span>

<span data-ttu-id="b2edc-114">Il client chiama i metodi [**iPaper:: Lock**](ipaper-methods.md) e **Unlock** per gestire la proprietà del documento per il disegno.</span><span class="sxs-lookup"><span data-stu-id="b2edc-114">The client calls the [**IPaper::Lock**](ipaper-methods.md) and **Unlock** methods to manage ownership of COPaper for drawing.</span></span> <span data-ttu-id="b2edc-115">Questi metodi vengono forniti per organizzare l'accesso tra più client al disegno contenuto in un documento condiviso.</span><span class="sxs-lookup"><span data-stu-id="b2edc-115">These methods are provided to organize access among multiple clients to the drawing held in a shared COPaper.</span></span>

## <a name="paper_properties-structure"></a><span data-ttu-id="b2edc-116">\_Struttura della proprietà paper</span><span class="sxs-lookup"><span data-stu-id="b2edc-116">PAPER\_PROPERTIES Structure</span></span>

<span data-ttu-id="b2edc-117">Il client chiama il metodo [**iPaper:: Resize**](ipaper-methods.md) per indicare al documento che l'utente ha ridimensionato il rettangolo di disegno corrente.</span><span class="sxs-lookup"><span data-stu-id="b2edc-117">The client calls the [**IPaper::Resize**](ipaper-methods.md) method to tell COPaper that the user resized the current drawing paper rectangle.</span></span> <span data-ttu-id="b2edc-118">I dati delle coordinate vengono conservati in una struttura di **\_ proprietà della carta** , archiviata con i dati di input penna quando tutti i dati cartacei vengono archiviati in un file composto.</span><span class="sxs-lookup"><span data-stu-id="b2edc-118">This coordinate data is kept in a **PAPER\_PROPERTIES** structure, which is stored with the ink data when all the paper data is stored in a compound file.</span></span>

<span data-ttu-id="b2edc-119">Di seguito è riportata la dichiarazione delle **\_ proprietà della carta** da Paper. H.</span><span class="sxs-lookup"><span data-stu-id="b2edc-119">The following is the **PAPER\_PROPERTIES** declaration from PAPER.H.</span></span>

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

<span data-ttu-id="b2edc-120">La struttura della **\_ Proprietà paper** è progettata in modo che i nuovi formati di dati Ink possano essere aggiunti in qualsiasi momento quando il componente DllPaper si evolve.</span><span class="sxs-lookup"><span data-stu-id="b2edc-120">The **PAPER\_PROPERTIES** structure is designed so that new ink data formats can be added at any time as the DllPaper component evolves.</span></span> <span data-ttu-id="b2edc-121">L'interfaccia [**iPaper**](ipaper-methods.md) è sufficientemente generale da consentire a una versione successiva del componente DllPaper di archiviare un formato di dati Ink diverso durante l'implementazione della stessa interfaccia **iPaper** .</span><span class="sxs-lookup"><span data-stu-id="b2edc-121">The [**IPaper**](ipaper-methods.md) interface is general enough that a subsequent version of the DllPaper component may store a different ink data format while implementing the same **IPaper** interface.</span></span> <span data-ttu-id="b2edc-122">Poiché i metodi di **iPaper** non dipendono da un formato di dati Ink specifico, una nuova versione del componente DllPaper che supporta un formato di dati Ink diverso può utilizzare la stessa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b2edc-122">Because the methods of **IPaper** do not depend on a specific ink data format, a new version of the DllPaper component that does support a different ink data format can use this same interface.</span></span>

<span data-ttu-id="b2edc-123">Le proprietà della carta archiviate in un file composto registrano la dimensione corrente della matrice di dati di input penna.</span><span class="sxs-lookup"><span data-stu-id="b2edc-123">The paper properties stored in a compound file record the current size of the ink data array.</span></span> <span data-ttu-id="b2edc-124">È quindi possibile allocare le dimensioni corrette della matrice per contenere i dati dell'input penna letti dal file.</span><span class="sxs-lookup"><span data-stu-id="b2edc-124">The proper array size can then be allocated to accommodate the ink data read from the file.</span></span>

<span data-ttu-id="b2edc-125">La struttura della **\_ Proprietà paper** archivia anche le dimensioni del rettangolo di disegno e del colore della finestra di sfondo della carta.</span><span class="sxs-lookup"><span data-stu-id="b2edc-125">The **PAPER\_PROPERTIES** structure also stores the paper surface's drawing rectangle size and background window color.</span></span>

<span data-ttu-id="b2edc-126">Sebbene non venga usato negli  / esempi **StoClien** di StoServe, è possibile archiviare anche un titolo del disegno e un nome di autore.</span><span class="sxs-lookup"><span data-stu-id="b2edc-126">Though not used in the **StoServe**/**StoClien** samples, a drawing title and an author name can also be stored.</span></span>

<span data-ttu-id="b2edc-127">La data di creazione e le date dell'Ultima modifica non sono incluse nelle proprietà della carta, perché l'interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) usata per accedere ai file composti gestisce queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="b2edc-127">Creation date and last modified dates are not included in these paper properties, because the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface used to access compound files manages this information.</span></span>

 

 





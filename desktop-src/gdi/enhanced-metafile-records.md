---
description: Un metafile migliorato è una matrice di record.
ms.assetid: af3261c7-2113-4777-97c0-504f23022550
title: Record metafile avanzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2097fd59497838c2a77a0209f6ae715dff2e1cf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978618"
---
# <a name="enhanced-metafile-records"></a><span data-ttu-id="9ba06-103">Record metafile avanzati</span><span class="sxs-lookup"><span data-stu-id="9ba06-103">Enhanced Metafile Records</span></span>

<span data-ttu-id="9ba06-104">Un metafile migliorato è una matrice di record.</span><span class="sxs-lookup"><span data-stu-id="9ba06-104">An enhanced metafile is an array of records.</span></span> <span data-ttu-id="9ba06-105">Un record metafile è una struttura [**ENHMETARECORD**](/windows/win32/api/wingdi/ns-wingdi-enhmetarecord) a lunghezza variabile.</span><span class="sxs-lookup"><span data-stu-id="9ba06-105">A metafile record is a variable-length [**ENHMETARECORD**](/windows/win32/api/wingdi/ns-wingdi-enhmetarecord) structure.</span></span> <span data-ttu-id="9ba06-106">All'inizio di ogni record del metafile migliorato si tratta di una struttura [**EMR**](/windows/win32/api/wingdi/ns-wingdi-emr) , che contiene due membri.</span><span class="sxs-lookup"><span data-stu-id="9ba06-106">At the beginning of every enhanced metafile record is an [**EMR**](/windows/win32/api/wingdi/ns-wingdi-emr) structure, which contains two members.</span></span> <span data-ttu-id="9ba06-107">Il primo membro, iType, identifica il tipo di record, ovvero la funzione GDI i cui parametri sono contenuti nel record.</span><span class="sxs-lookup"><span data-stu-id="9ba06-107">The first member, iType, identifies the record type that is, the GDI function whose parameters are contained in the record.</span></span> <span data-ttu-id="9ba06-108">Poiché le strutture sono di lunghezza variabile, l'altro membro, nSize, contiene le dimensioni del record.</span><span class="sxs-lookup"><span data-stu-id="9ba06-108">Because the structures are variable in length, the other member, nSize, contains the size of the record.</span></span> <span data-ttu-id="9ba06-109">Immediatamente dopo il membro nSize sono i parametri rimanenti, se presenti, della funzione GDI.</span><span class="sxs-lookup"><span data-stu-id="9ba06-109">Immediately following the nSize member are the remaining parameters, if any, of the GDI function.</span></span> <span data-ttu-id="9ba06-110">Il resto della struttura contiene dati aggiuntivi che dipendono dal tipo di record.</span><span class="sxs-lookup"><span data-stu-id="9ba06-110">The remainder of the structure contains additional data that is dependent on the record type.</span></span>

<span data-ttu-id="9ba06-111">Il primo record in un metafile migliorato è sempre la struttura [**ENHMETAHEADER**](/windows/win32/api/wingdi/ns-wingdi-enhmetaheader) , che è l'intestazione Enhanced-Metafile.</span><span class="sxs-lookup"><span data-stu-id="9ba06-111">The first record in an enhanced metafile is always the [**ENHMETAHEADER**](/windows/win32/api/wingdi/ns-wingdi-enhmetaheader) structure, which is the enhanced-metafile header.</span></span> <span data-ttu-id="9ba06-112">L'intestazione specifica le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="9ba06-112">The header specifies the following information:</span></span>

-   <span data-ttu-id="9ba06-113">Dimensioni del metafile, in byte</span><span class="sxs-lookup"><span data-stu-id="9ba06-113">Size of the metafile, in bytes</span></span>
-   <span data-ttu-id="9ba06-114">Dimensioni del frame immagine, in unità dispositivo</span><span class="sxs-lookup"><span data-stu-id="9ba06-114">Dimensions of the picture frame, in device units</span></span>
-   <span data-ttu-id="9ba06-115">Dimensioni del frame immagine, in unità. 01-mm</span><span class="sxs-lookup"><span data-stu-id="9ba06-115">Dimensions of the picture frame, in .01-millimeter units</span></span>
-   <span data-ttu-id="9ba06-116">Numero di record nel metafile</span><span class="sxs-lookup"><span data-stu-id="9ba06-116">Number of records in the metafile</span></span>
-   <span data-ttu-id="9ba06-117">Offset a una descrizione di testo facoltativa</span><span class="sxs-lookup"><span data-stu-id="9ba06-117">Offset to an optional text description</span></span>
-   <span data-ttu-id="9ba06-118">Dimensioni della tavolozza facoltativa</span><span class="sxs-lookup"><span data-stu-id="9ba06-118">Size of the optional palette</span></span>
-   <span data-ttu-id="9ba06-119">Risoluzione del dispositivo originale, in pixel</span><span class="sxs-lookup"><span data-stu-id="9ba06-119">Resolution of the original device, in pixels</span></span>
-   <span data-ttu-id="9ba06-120">Risoluzione del dispositivo originale, in millimetri</span><span class="sxs-lookup"><span data-stu-id="9ba06-120">Resolution of the original device, in millimeters</span></span>

<span data-ttu-id="9ba06-121">Una descrizione di testo facoltativa può seguire il record di intestazione.</span><span class="sxs-lookup"><span data-stu-id="9ba06-121">An optional text description can follow the header record.</span></span> <span data-ttu-id="9ba06-122">La descrizione del testo descrive l'immagine e il nome dell'autore.</span><span class="sxs-lookup"><span data-stu-id="9ba06-122">The text description describes the picture and the author's name.</span></span> <span data-ttu-id="9ba06-123">La tavolozza facoltativa specifica i colori utilizzati per creare il metafile avanzato.</span><span class="sxs-lookup"><span data-stu-id="9ba06-123">The optional palette specifies the colors used to create the enhanced metafile.</span></span> <span data-ttu-id="9ba06-124">I record rimanenti identificano le funzioni GDI utilizzate per la creazione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="9ba06-124">The remaining records identify the GDI functions used to create the picture.</span></span> <span data-ttu-id="9ba06-125">Il seguente output esadecimale corrisponde a un record generato per una chiamata alla funzione [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) .</span><span class="sxs-lookup"><span data-stu-id="9ba06-125">The following hexadecimal output corresponds to a record generated for a call to the [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) function.</span></span>


```C++
00000011 0000000C 00000004 
```



<span data-ttu-id="9ba06-126">Il valore 0x00000011 specifica il tipo di record (corrisponde alla \_ costante SETMAPMODE di EMR definita nel file wingdi. h).</span><span class="sxs-lookup"><span data-stu-id="9ba06-126">The value 0x00000011 specifies the record type (corresponds to the EMR\_SETMAPMODE constant defined in the file Wingdi.h).</span></span> <span data-ttu-id="9ba06-127">Il valore 0x0000000C specifica la lunghezza, in byte, del record.</span><span class="sxs-lookup"><span data-stu-id="9ba06-127">The value 0x0000000C specifies the length of the record, in bytes.</span></span> <span data-ttu-id="9ba06-128">Il valore 0x00000004 identifica la modalità di mapping (corrisponde alla \_ costante mm LOENGLISH definita nella funzione [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) ).</span><span class="sxs-lookup"><span data-stu-id="9ba06-128">The value 0x00000004 identifies the mapping mode (corresponds to the MM\_LOENGLISH constant defined in the [**SetMapMode**](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode) function).</span></span>

<span data-ttu-id="9ba06-129">Per un elenco di altri tipi di record, vedere [strutture di metafile](metafile-structures.md).</span><span class="sxs-lookup"><span data-stu-id="9ba06-129">For a list of additional record types, see [Metafile Structures](metafile-structures.md).</span></span>

 

 




---
description: Analogamente a un'area di ridimensionamento, un percorso di ritaglio è un altro oggetto grafico che un'applicazione può selezionare in un contesto di dispositivo.
ms.assetid: 35c4052b-3f11-40bc-9cc9-6f999326a656
title: Percorsi di ritaglio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc4a93b0047110a6adb2f68d413e89cb1e97fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978770"
---
# <a name="clip-paths"></a><span data-ttu-id="828ad-103">Percorsi di ritaglio</span><span class="sxs-lookup"><span data-stu-id="828ad-103">Clip Paths</span></span>

<span data-ttu-id="828ad-104">Analogamente a un'area di ridimensionamento, un percorso di ritaglio è un altro oggetto grafico che un'applicazione può selezionare in un contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="828ad-104">Like a clipping region, a clip path is another graphics object that an application can select into a device context.</span></span> <span data-ttu-id="828ad-105">A differenza di un'area di ridimensionamento, un tracciato di ritaglio viene sempre creato da un'applicazione e viene usato per il ritaglio a una o più forme irregolari.</span><span class="sxs-lookup"><span data-stu-id="828ad-105">Unlike a clipping region, a clip path is always created by an application and it is used for clipping to one or more irregular shapes.</span></span> <span data-ttu-id="828ad-106">Ad esempio, un'applicazione può usare le linee e le curve che formano i contorni dei caratteri di una stringa di testo per definire un percorso di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="828ad-106">For example, an application can use the lines and curves that form the outlines of characters in a string of text to define a clip path.</span></span>

<span data-ttu-id="828ad-107">Per creare un tracciato di ritaglio, è prima necessario creare un percorso che descriva la forma irregolare richiesta.</span><span class="sxs-lookup"><span data-stu-id="828ad-107">To create a clip path, it's first necessary to create a path that describes the required irregular shape.</span></span> <span data-ttu-id="828ad-108">I percorsi vengono creati chiamando le funzioni di disegno GDI (Graphics Device Interface) appropriate dopo aver chiamato la funzione [**beginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) e prima di chiamare la funzione [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) .</span><span class="sxs-lookup"><span data-stu-id="828ad-108">Paths are created by calling the appropriate graphics device interface (GDI) drawing functions after calling the [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) function and before calling the [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) function.</span></span> <span data-ttu-id="828ad-109">Questa raccolta di funzioni è detta parentesi del percorso.</span><span class="sxs-lookup"><span data-stu-id="828ad-109">This collection of functions is called a path bracket.</span></span> <span data-ttu-id="828ad-110">Per ulteriori informazioni sui percorsi e sulle parentesi quadre, vedere [percorsi](paths.md).</span><span class="sxs-lookup"><span data-stu-id="828ad-110">For more information about paths and path brackets, see [Paths](paths.md).</span></span>

<span data-ttu-id="828ad-111">Una volta creato il percorso, è possibile convertirlo in un percorso di clip chiamando la funzione [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) , identificando un contesto di dispositivo e specificando una modalità di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="828ad-111">After the path is created, it can be converted to a clip path by calling the [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) function, identifying a device context, and specifying a usage mode.</span></span> <span data-ttu-id="828ad-112">La modalità di utilizzo determina il modo in cui il sistema combina il nuovo tracciato di ritaglio con l'area di ritaglio originale del contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="828ad-112">The usage mode determines how the system combines the new clip path with the device context's original clipping region.</span></span> <span data-ttu-id="828ad-113">Nella tabella seguente vengono descritte le modalità di utilizzo di.</span><span class="sxs-lookup"><span data-stu-id="828ad-113">The following table describes the usage modes.</span></span>



| <span data-ttu-id="828ad-114">Mode</span><span class="sxs-lookup"><span data-stu-id="828ad-114">Mode</span></span>      | <span data-ttu-id="828ad-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="828ad-115">Description</span></span>                                                                                                                  |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="828ad-116">RGN \_ e</span><span class="sxs-lookup"><span data-stu-id="828ad-116">RGN\_AND</span></span>  | <span data-ttu-id="828ad-117">Il percorso di ritaglio include l'intersezione (aree sovrapposte) dell'area di ridimensionamento del contesto di dispositivo e il percorso corrente.</span><span class="sxs-lookup"><span data-stu-id="828ad-117">The clip path includes the intersection (overlapping areas) of the device context's clipping region and the current path.</span></span>    |
| <span data-ttu-id="828ad-118">copia di RGN \_</span><span class="sxs-lookup"><span data-stu-id="828ad-118">RGN\_COPY</span></span> | <span data-ttu-id="828ad-119">Il percorso di ritaglio è il percorso corrente.</span><span class="sxs-lookup"><span data-stu-id="828ad-119">The clip path is the current path.</span></span>                                                                                           |
| <span data-ttu-id="828ad-120">\_diff RGN</span><span class="sxs-lookup"><span data-stu-id="828ad-120">RGN\_DIFF</span></span> | <span data-ttu-id="828ad-121">Il percorso della clip include l'area di ridimensionamento del contesto di dispositivo con le parti di intersezione del percorso corrente escluse.</span><span class="sxs-lookup"><span data-stu-id="828ad-121">The clip path includes the device context's clipping region with any intersecting parts of the current path excluded.</span></span>        |
| <span data-ttu-id="828ad-122">RGN \_ o</span><span class="sxs-lookup"><span data-stu-id="828ad-122">RGN\_OR</span></span>   | <span data-ttu-id="828ad-123">Il percorso di ritaglio include l'Unione (aree combinate) dell'area di ridimensionamento del contesto di dispositivo e il percorso corrente.</span><span class="sxs-lookup"><span data-stu-id="828ad-123">The clip path includes the union (combined areas) of the device context's clipping region and the current path.</span></span>              |
| <span data-ttu-id="828ad-124">\_Xor RGN</span><span class="sxs-lookup"><span data-stu-id="828ad-124">RGN\_XOR</span></span>  | <span data-ttu-id="828ad-125">Il percorso della clip include l'Unione dell'area di ridimensionamento del contesto di dispositivo e il percorso corrente, ma esclude l'intersezione.</span><span class="sxs-lookup"><span data-stu-id="828ad-125">The clip path includes the union of the device context's clipping region and the current path but excludes the intersection.</span></span> |



 

 

 




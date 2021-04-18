---
title: Dati di input
description: Per la pipeline OpenGL è necessario inserire diversi tipi di dati
ms.assetid: e820d093-3e39-4feb-ab2a-0c28e298bde4
keywords:
- Pipeline di elaborazione OpenGL, dati di input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 121cf032e0e718b95fd42f3001d2ff8efee1f6b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298057"
---
# <a name="input-data"></a><span data-ttu-id="cffb9-104">Dati di input</span><span class="sxs-lookup"><span data-stu-id="cffb9-104">Input Data</span></span>

<span data-ttu-id="cffb9-105">Per la pipeline OpenGL è necessario inserire diversi tipi di dati:</span><span class="sxs-lookup"><span data-stu-id="cffb9-105">The OpenGL pipeline requires you to input several types of data:</span></span>

-   <span data-ttu-id="cffb9-106">**Vertici**.</span><span class="sxs-lookup"><span data-stu-id="cffb9-106">**Vertices**.</span></span> <span data-ttu-id="cffb9-107">I vertici descrivono la forma dell'oggetto geometrico desiderato.</span><span class="sxs-lookup"><span data-stu-id="cffb9-107">Vertices describe the shape of the desired geometric object.</span></span> <span data-ttu-id="cffb9-108">Per specificare i vertici, usare le funzioni [**glVertex \***](glvertex-functions.md) insieme a [**glBegin**](glbegin.md) e [**glEnd**](glend.md) per creare un punto, una linea o un poligono.</span><span class="sxs-lookup"><span data-stu-id="cffb9-108">To specify vertices, use [**glVertex\***](glvertex-functions.md) functions in conjunction with [**glBegin**](glbegin.md) and [**glEnd**](glend.md) to create a point, line, or polygon.</span></span> <span data-ttu-id="cffb9-109">È anche possibile usare [**glRect**](glrect-functions.md) per descrivere un intero rettangolo in una sola volta.</span><span class="sxs-lookup"><span data-stu-id="cffb9-109">You can also use [**glRect**](glrect-functions.md) to describe an entire rectangle at one time.</span></span>
-   <span data-ttu-id="cffb9-110">**Flag Edge**.</span><span class="sxs-lookup"><span data-stu-id="cffb9-110">**Edge flag**.</span></span> <span data-ttu-id="cffb9-111">Per impostazione predefinita, tutti i bordi dei poligoni sono bordi limite.</span><span class="sxs-lookup"><span data-stu-id="cffb9-111">By default, all edges of polygons are boundary edges.</span></span> <span data-ttu-id="cffb9-112">Usare [**glEdgeFlag \***](gledgeflag-functions.md) per impostare in modo esplicito il flag Edge.</span><span class="sxs-lookup"><span data-stu-id="cffb9-112">Use [**glEdgeFlag\***](gledgeflag-functions.md) to explicitly set the edge flag.</span></span>
-   <span data-ttu-id="cffb9-113">**Posizione raster corrente**.</span><span class="sxs-lookup"><span data-stu-id="cffb9-113">**Current raster position**.</span></span> <span data-ttu-id="cffb9-114">Specificata con [**glRasterPos \***](glrasterpos-functions.md), la posizione raster corrente viene usata per determinare le coordinate raster per le operazioni di disegno pixel e bitmap.</span><span class="sxs-lookup"><span data-stu-id="cffb9-114">Specified with [**glRasterPos\***](glrasterpos-functions.md), the current raster position is used to determine raster coordinates for pixel- and bitmap-drawing operations.</span></span>
-   <span data-ttu-id="cffb9-115">**Normale corrente**.</span><span class="sxs-lookup"><span data-stu-id="cffb9-115">**Current normal**.</span></span> <span data-ttu-id="cffb9-116">Un vettore normale associato a un vertice particolare determina il modo in cui una superficie a tale vertice è orientata allo spazio tridimensionale. Ciò a sua volta influiscono sulla quantità di luce ricevuta da un vertice specifico.</span><span class="sxs-lookup"><span data-stu-id="cffb9-116">A normal vector associated with a particular vertex determines how a surface at that vertex is oriented in three-dimensional space; this in turn affects how much light that particular vertex receives.</span></span> <span data-ttu-id="cffb9-117">Usare [**glNormal \***](glnormal-functions.md) per specificare un vettore normale.</span><span class="sxs-lookup"><span data-stu-id="cffb9-117">Use [**glNormal\***](glnormal-functions.md) to specify a normal vector.</span></span>
-   <span data-ttu-id="cffb9-118">**Colore corrente**.</span><span class="sxs-lookup"><span data-stu-id="cffb9-118">**Current color**.</span></span> <span data-ttu-id="cffb9-119">Il colore di un vertice, insieme alle condizioni di illuminazione, determina il colore finale illuminato.</span><span class="sxs-lookup"><span data-stu-id="cffb9-119">The color of a vertex, together with the lighting conditions, determine the final, lit color.</span></span> <span data-ttu-id="cffb9-120">Il colore viene specificato [**con \* glColor**](glcolor-functions.md) se in modalità RGBA o con [**glIndex \***](glindex-functions.md) se si trova in modalità di indice a colori.</span><span class="sxs-lookup"><span data-stu-id="cffb9-120">Color is specified with [**glColor\***](glcolor-functions.md) if in RGBA mode, or with [**glIndex\***](glindex-functions.md) if in color-index mode.</span></span>
-   <span data-ttu-id="cffb9-121">**Coordinate di trama correnti**.</span><span class="sxs-lookup"><span data-stu-id="cffb9-121">**Current texture coordinates**.</span></span> <span data-ttu-id="cffb9-122">Specificata con [**glTexCoord \***](gltexcoord-functions.md), le coordinate di trama determinano la posizione in una mappa di trama da associare a un vertice di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="cffb9-122">Specified with [**glTexCoord\***](gltexcoord-functions.md), texture coordinates determine the location in a texture map to associate with a vertex of an object.</span></span>

> [!Note]  
> <span data-ttu-id="cffb9-123">Quando viene chiamato **glVertex \*** , il vertice risultante eredita il flag del bordo, il normale, il colore e le coordinate di trama correnti.</span><span class="sxs-lookup"><span data-stu-id="cffb9-123">When **glVertex\*** is called, the resulting vertex inherits the current edge flag, normal, color, and texture coordinates.</span></span> <span data-ttu-id="cffb9-124">Pertanto, **glEdgeFlag \***, **glNormal \***, **glColor \*** e **\* glTexCoord** devono essere chiamati prima di **glVertex \***, se hanno effetto sul vertice risultante.</span><span class="sxs-lookup"><span data-stu-id="cffb9-124">Therefore, **glEdgeFlag\***, **glNormal\***, **glColor\***, and **glTexCoord\*** must be called before **glVertex\***, if they are to affect the resulting vertex.</span></span>

 

 

 





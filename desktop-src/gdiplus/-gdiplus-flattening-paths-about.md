---
description: Un oggetto GraphicsPath archivia una sequenza di linee e B&\# 233; Zier spline.
ms.assetid: 8ce77146-dc28-4c0b-bcf0-dad4bf3d86e8
title: Percorsi Flat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7caee9b8d760d9702b6a3ea7711090f001a57912
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987712"
---
# <a name="flattening-paths"></a><span data-ttu-id="7f3ad-103">Percorsi Flat</span><span class="sxs-lookup"><span data-stu-id="7f3ad-103">Flattening Paths</span></span>

<span data-ttu-id="7f3ad-104">Un oggetto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) archivia una sequenza di linee e spline di Bézier.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-104">A [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object stores a sequence of lines and Bézier splines.</span></span> <span data-ttu-id="7f3ad-105">È possibile aggiungere diversi tipi di curve (ellissi, archi, spline cardinali) a un tracciato, ma ogni curva viene convertita in una spline di Bézier prima di essere archiviata nel percorso.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-105">You can add several types of curves (ellipses, arcs, cardinal splines) to a path, but each curve is converted to a Bézier spline before it is stored in the path.</span></span> <span data-ttu-id="7f3ad-106">L'appiattimento di un tracciato è costituito dalla conversione di ogni spline di Bézier nel percorso a una sequenza di linee rette.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-106">Flattening a path consists of converting each Bézier spline in the path to a sequence of straight lines.</span></span>

<span data-ttu-id="7f3ad-107">Per rendere flat un tracciato, chiamare il metodo [**GraphicsPath:: Flat**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-flatten) di un oggetto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) .</span><span class="sxs-lookup"><span data-stu-id="7f3ad-107">To flatten a path, call the [**GraphicsPath::Flatten**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-flatten) method of a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object.</span></span> <span data-ttu-id="7f3ad-108">Il metodo **GraphicsPath:: Flat** riceve un argomento flat che specifica la distanza massima tra il percorso bidimensionale e il percorso originale.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-108">The **GraphicsPath::Flatten** method receives a flatness argument that specifies the maximum distance between the flattened path and the original path.</span></span> <span data-ttu-id="7f3ad-109">Nella figura seguente viene illustrato un percorso prima e dopo l'appiattimento.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-109">The following illustration shows a path before and after flattening.</span></span>

![illustrazione che mostra una sequenza di spline di Bezier connesse in blu e le righe corrispondenti in rosso](images/aboutgdip02-art32a.png)

 

 




---
description: I record di polilinea sono una serie di punti; le linee tracciate tra i punti descrivono il contorno del carattere.
ms.assetid: 6f0de0bb-ad23-471f-9771-8f28614ee28d
title: Record polilinea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20e9a9e87a730d06d15eae219f6f626f1d6d3848
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226672"
---
# <a name="polyline-records"></a><span data-ttu-id="11c1f-103">Record polilinea</span><span class="sxs-lookup"><span data-stu-id="11c1f-103">Polyline Records</span></span>

<span data-ttu-id="11c1f-104">I record di [polilinea](/windows/desktop/api/Wingdi/nf-wingdi-polyline) sono una serie di punti; le linee tracciate tra i punti descrivono il contorno del carattere.</span><span class="sxs-lookup"><span data-stu-id="11c1f-104">[Polyline](/windows/desktop/api/Wingdi/nf-wingdi-polyline) records are a series of points; lines drawn between the points describe the outline of the character.</span></span> <span data-ttu-id="11c1f-105">Un record di polilinea inizia con l'ultimo punto del record precedente (o, per il primo record nel contorno, il punto iniziale).</span><span class="sxs-lookup"><span data-stu-id="11c1f-105">A polyline record begins with the last point in the previous record (or, for the first record in the contour, the starting point).</span></span> <span data-ttu-id="11c1f-106">Ogni punto del record si trova nella struttura del glifo e può essere connesso semplicemente utilizzando linee rette.</span><span class="sxs-lookup"><span data-stu-id="11c1f-106">Each point in the record is on the glyph outline and can be connected simply by using straight lines.</span></span>

 

 




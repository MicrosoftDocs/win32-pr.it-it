---
description: Le dimensioni di una penna cosmetica sono specificate in unità dispositivo.
ms.assetid: d4386681-3523-4872-b048-2a5cfbf7d039
title: Penne cosmetiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbb312ed0b3825397ff79ebc32d363956ad04519
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754466"
---
# <a name="cosmetic-pens"></a><span data-ttu-id="e28a2-103">Penne cosmetiche</span><span class="sxs-lookup"><span data-stu-id="e28a2-103">Cosmetic Pens</span></span>

<span data-ttu-id="e28a2-104">Le dimensioni di una penna cosmetica sono specificate in unità dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e28a2-104">The dimensions of a cosmetic pen are specified in device units.</span></span> <span data-ttu-id="e28a2-105">Pertanto, le linee disegnate con una penna cosmetica hanno sempre una larghezza fissa.</span><span class="sxs-lookup"><span data-stu-id="e28a2-105">Therefore, lines drawn with a cosmetic pen always have a fixed width.</span></span> <span data-ttu-id="e28a2-106">Le linee disegnate con una penna cosmetica vengono in genere disegnate da 3 a 10 volte più velocemente rispetto alle linee disegnate con una penna geometrica.</span><span class="sxs-lookup"><span data-stu-id="e28a2-106">Lines drawn with a cosmetic pen are generally drawn 3 to 10 times faster than lines drawn with a geometric pen.</span></span> <span data-ttu-id="e28a2-107">Le penne cosmetiche hanno tre attributi: larghezza, stile e colore.</span><span class="sxs-lookup"><span data-stu-id="e28a2-107">Cosmetic pens have three attributes: width, style, and color.</span></span> <span data-ttu-id="e28a2-108">Per ulteriori informazioni su questi attributi, vedere [attributi di penna](pen-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="e28a2-108">For more information about these attributes, see [Pen Attributes](pen-attributes.md).</span></span>

<span data-ttu-id="e28a2-109">Per creare una penna cosmetica, usare la funzione [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)o [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) .</span><span class="sxs-lookup"><span data-stu-id="e28a2-109">To create a cosmetic pen, use the [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect), or [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) function.</span></span> <span data-ttu-id="e28a2-110">Per recuperare una delle tre penne cosmetiche predefinite gestite dal sistema, usare la funzione [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) .</span><span class="sxs-lookup"><span data-stu-id="e28a2-110">To retrieve one of the three stock cosmetic pens managed by the system, use the [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) function.</span></span>

<span data-ttu-id="e28a2-111">Dopo la creazione di una penna (o l'ottenimento di un handle per una delle penne predefinite), selezionare la penna nel contesto di dispositivo (DC) dell'applicazione usando la funzione [**SelezionaOggetto**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) .</span><span class="sxs-lookup"><span data-stu-id="e28a2-111">After you create a pen (or obtain a handle to one of the stock pens), select the pen into the application's device context (DC) using the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function.</span></span> <span data-ttu-id="e28a2-112">Da questo punto in poi, l'applicazione usa questa penna per tutte le operazioni di disegno di riga nell'area client.</span><span class="sxs-lookup"><span data-stu-id="e28a2-112">From this point on, the application uses this pen for any line-drawing operations in its client area.</span></span>

 

 




---
description: Le dimensioni di una penna geometrica sono specificate in unità logiche.
ms.assetid: e7030490-d10c-4d1c-87ae-5b4cc4858ee1
title: Penne geometriche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9725f6440f62458d4c87232400f16e27f9b978ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993997"
---
# <a name="geometric-pens"></a><span data-ttu-id="207e1-103">Penne geometriche</span><span class="sxs-lookup"><span data-stu-id="207e1-103">Geometric Pens</span></span>

<span data-ttu-id="207e1-104">Le dimensioni di una penna geometrica sono specificate in unità logiche.</span><span class="sxs-lookup"><span data-stu-id="207e1-104">The dimensions of a geometric pen are specified in logical units.</span></span> <span data-ttu-id="207e1-105">Pertanto, le linee disegnate con una penna geometrica possono essere ridimensionate, ovvero possono apparire più larghe o più strette, a seconda della trasformazione mondiale corrente.</span><span class="sxs-lookup"><span data-stu-id="207e1-105">Therefore, lines drawn with a geometric pen can be scaled that is, they may appear wider or narrower, depending on the current world transformation.</span></span> <span data-ttu-id="207e1-106">Per ulteriori informazioni sulla trasformazione globale, vedere [spazi di coordinate e trasformazioni](coordinate-spaces-and-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="207e1-106">For more information about world transformation, see [Coordinate Spaces and Transformations](coordinate-spaces-and-transformations.md).</span></span>

<span data-ttu-id="207e1-107">Oltre ai tre attributi condivisi con le penne cosmetiche (larghezza, stile e colore), le penne geometriche posseggono i quattro attributi seguenti: pattern, Hatch facoltativo, stile finale e stile join.</span><span class="sxs-lookup"><span data-stu-id="207e1-107">In addition to the three attributes shared with cosmetic pens (width, style, and color), geometric pens possess the following four attributes: pattern, optional hatch, end style, and join style.</span></span> <span data-ttu-id="207e1-108">Per ulteriori informazioni su questi attributi, vedere [attributi di penna](pen-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="207e1-108">For more information about these attributes, see [Pen Attributes](pen-attributes.md).</span></span>

<span data-ttu-id="207e1-109">Per creare una penna geometrica, un'applicazione usa la funzione [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) .</span><span class="sxs-lookup"><span data-stu-id="207e1-109">To create a geometric pen, an application uses the [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) function.</span></span> <span data-ttu-id="207e1-110">Come per le penne cosmetiche, la funzione [**SelezionaOggetto**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) seleziona una penna geometrica nel controller di dominio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="207e1-110">As with cosmetic pens, the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function selects a geometric pen into the application's DC.</span></span>

 

 




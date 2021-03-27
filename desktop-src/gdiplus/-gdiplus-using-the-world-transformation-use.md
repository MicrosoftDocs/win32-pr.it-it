---
description: La trasformazione globale è una proprietà della classe Graphics.
ms.assetid: 22f43b29-ea7b-4faf-9795-2242bf704ed3
title: Utilizzo della trasformazione di tipo World
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2138df1bbd2be6d3329695fc6898da49da93b3b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226060"
---
# <a name="using-the-world-transformation"></a><span data-ttu-id="d0d0a-103">Utilizzo della trasformazione di tipo World</span><span class="sxs-lookup"><span data-stu-id="d0d0a-103">Using the World Transformation</span></span>

<span data-ttu-id="d0d0a-104">La trasformazione globale è una proprietà della classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="d0d0a-104">The world transformation is a property of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="d0d0a-105">I numeri che specificano la trasformazione globale vengono archiviati in un oggetto [**matrice**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) , che rappresenta una matrice 3 × 3.</span><span class="sxs-lookup"><span data-stu-id="d0d0a-105">The numbers that specify the world transformation are stored in a [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) object, which represents a 3 ×3 matrix.</span></span> <span data-ttu-id="d0d0a-106">Le classi **Matrix** e **Graphics** hanno diversi metodi per impostare i numeri nella matrice di trasformazione mondiale.</span><span class="sxs-lookup"><span data-stu-id="d0d0a-106">The **Matrix** and **Graphics** classes have several methods for setting the numbers in the world transformation matrix.</span></span> <span data-ttu-id="d0d0a-107">Gli esempi in questa sezione modificano i rettangoli perché i rettangoli sono facili da creare ed è facile vedere gli effetti delle trasformazioni sui rettangoli.</span><span class="sxs-lookup"><span data-stu-id="d0d0a-107">The examples in this section manipulate rectangles because rectangles are easy to draw and it is easy to see the effects of transformations on rectangles.</span></span>

<span data-ttu-id="d0d0a-108">Per iniziare, si crea un rettangolo 50 per 50 e lo si individua all'origine (0,0).</span><span class="sxs-lookup"><span data-stu-id="d0d0a-108">We start by creating a 50 by 50 rectangle and locating it at the origin (0, 0).</span></span> <span data-ttu-id="d0d0a-109">L'origine si trova nell'angolo superiore sinistro dell'area client.</span><span class="sxs-lookup"><span data-stu-id="d0d0a-109">The origin is at the upper-left corner of the client area.</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="d0d0a-110">Il codice seguente applica una trasformazione di ridimensionamento che espande il rettangolo per un fattore di 1,75 nella direzione x e compatta il rettangolo per un fattore di 0,5 nella direzione y:</span><span class="sxs-lookup"><span data-stu-id="d0d0a-110">The following code applies a scaling transformation that expands the rectangle by a factor of 1.75 in the x direction and shrinks the rectangle by a factor of 0.5 in the y direction:</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.ScaleTransform(1.75f, 0.5f);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="d0d0a-111">Il risultato è un rettangolo più lungo nella direzione x e più breve nella direzione y rispetto all'originale.</span><span class="sxs-lookup"><span data-stu-id="d0d0a-111">The result is a rectangle that is longer in the x direction and shorter in the y direction than the original.</span></span>

<span data-ttu-id="d0d0a-112">Per ruotare il rettangolo anziché ridimensionarlo, usare il codice seguente anziché il codice precedente:</span><span class="sxs-lookup"><span data-stu-id="d0d0a-112">To rotate the rectangle instead of scaling it, use the following code instead of the preceding code:</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.RotateTransform(28.0f);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="d0d0a-113">Per tradurre il rettangolo, usare il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="d0d0a-113">To translate the rectangle, use the following code:</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f);
graphics.DrawRectangle(&pen, rect);
```



 

 




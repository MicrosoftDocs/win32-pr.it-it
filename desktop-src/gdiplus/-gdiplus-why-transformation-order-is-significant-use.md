---
description: Un singolo oggetto Matrix può archiviare una singola trasformazione o una sequenza di trasformazioni.
ms.assetid: 1dc68ff8-6b17-4934-82da-ab2fc612aafa
title: Importanza dell'ordine delle trasformazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7350d63456902ff47183faa08170b3b2fef481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977527"
---
# <a name="why-transformation-order-is-significant"></a><span data-ttu-id="4c2ef-103">Importanza dell'ordine delle trasformazioni</span><span class="sxs-lookup"><span data-stu-id="4c2ef-103">Why Transformation Order Is Significant</span></span>

<span data-ttu-id="4c2ef-104">Un singolo oggetto [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) può archiviare una singola trasformazione o una sequenza di trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="4c2ef-104">A single [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) object can store a single transformation or a sequence of transformations.</span></span> <span data-ttu-id="4c2ef-105">Quest'ultimo è denominato *trasformazione* *composita*.  </span><span class="sxs-lookup"><span data-stu-id="4c2ef-105">The latter is called a *composite*  *transformation*.</span></span> <span data-ttu-id="4c2ef-106">La matrice di una trasformazione composita viene ottenuta moltiplicando le matrici delle singole trasformazioni.</span><span class="sxs-lookup"><span data-stu-id="4c2ef-106">The matrix of a composite transformation is obtained by multiplying the matrices of the individual transformations.</span></span>

<span data-ttu-id="4c2ef-107">In una trasformazione composita, l'ordine delle singole trasformazioni è importante.</span><span class="sxs-lookup"><span data-stu-id="4c2ef-107">In a composite transformation, the order of the individual transformations is important.</span></span> <span data-ttu-id="4c2ef-108">Se, ad esempio, si esegue prima la rotazione, quindi si esegue la scalabilità e si traduce, si ottiene un risultato diverso da quello in cui si esegue la prima conversione, quindi si ruota e quindi si ridimensiona.</span><span class="sxs-lookup"><span data-stu-id="4c2ef-108">For example, if you first rotate, then scale, then translate, you get a different result than if you first translate, then rotate, then scale.</span></span> <span data-ttu-id="4c2ef-109">In Windows GDI+ le trasformazioni composite vengono compilate da sinistra a destra.</span><span class="sxs-lookup"><span data-stu-id="4c2ef-109">In Windows GDI+, composite transformations are built from left to right.</span></span> <span data-ttu-id="4c2ef-110">Se S, R e T sono rispettivamente matrici di scala, rotazione e conversione, il prodotto SRT (in questo ordine) è la matrice della trasformazione composita che si ridimensiona prima di tutto, quindi ruota e quindi trasla.</span><span class="sxs-lookup"><span data-stu-id="4c2ef-110">If S, R, and T are scale, rotation, and translation matrices respectively, then the product SRT (in that order) is the matrix of the composite transformation that first scales, then rotates, then translates.</span></span> <span data-ttu-id="4c2ef-111">La matrice prodotta dal prodotto SRT è diversa dalla matrice prodotta dal prodotto TRS.</span><span class="sxs-lookup"><span data-stu-id="4c2ef-111">The matrix produced by the product SRT is different from the matrix produced by the product TRS.</span></span>

<span data-ttu-id="4c2ef-112">Un ordine è significativo perché le trasformazioni come la rotazione e la scalabilità vengono eseguite rispetto all'origine del sistema di coordinate.</span><span class="sxs-lookup"><span data-stu-id="4c2ef-112">One reason order is significant is that transformations like rotation and scaling are done with respect to the origin of the coordinate system.</span></span> <span data-ttu-id="4c2ef-113">Il ridimensionamento di un oggetto centrato nell'origine produce un risultato diverso rispetto alla scalabilità di un oggetto che è stato rimosso dall'origine.</span><span class="sxs-lookup"><span data-stu-id="4c2ef-113">Scaling an object that is centered at the origin produces a different result than scaling an object that has been moved away from the origin.</span></span> <span data-ttu-id="4c2ef-114">Analogamente, la rotazione di un oggetto centrato nell'origine produce un risultato diverso rispetto alla rotazione di un oggetto che è stato rimosso dall'origine.</span><span class="sxs-lookup"><span data-stu-id="4c2ef-114">Similarly, rotating an object that is centered at the origin produces a different result than rotating an object that has been moved away from the origin.</span></span>

<span data-ttu-id="4c2ef-115">Nell'esempio seguente vengono combinate la scala, la rotazione e la conversione (in questo ordine) per formare una trasformazione composita.</span><span class="sxs-lookup"><span data-stu-id="4c2ef-115">The following example combines scaling, rotation and translation (in that order) to form a composite transformation.</span></span> <span data-ttu-id="4c2ef-116">L'argomento [\* \* \* \* MatrixOrderAppend \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) \* \* \* passato al metodo [**Graphics:: RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform) specifica che la rotazione deve seguire la scala.</span><span class="sxs-lookup"><span data-stu-id="4c2ef-116">The argument [\*\*\*\*MatrixOrderAppend\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) passed to the [**Graphics::RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform) method specifies that the rotation will follow the scaling.</span></span> <span data-ttu-id="4c2ef-117">Analogamente, l'argomento \* \* \* \* [MatrixOrderAppend \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) \* \* passato al metodo [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) specifica che la conversione seguirà la rotazione.</span><span class="sxs-lookup"><span data-stu-id="4c2ef-117">Likewise, the argument [\*\*\*\*MatrixOrderAppend\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) passed to the [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) method specifies that the translation will follow the rotation.</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.ScaleTransform(1.75f, 0.5f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.TranslateTransform(150.0f, 150.0f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="4c2ef-118">Nell'esempio seguente vengono eseguite le stesse chiamate al metodo dell'esempio precedente, ma l'ordine delle chiamate viene invertito.</span><span class="sxs-lookup"><span data-stu-id="4c2ef-118">The following example makes the same method calls as the previous example, but the order of the calls is reversed.</span></span> <span data-ttu-id="4c2ef-119">L'ordine delle operazioni risultante viene innanzitutto convertito, quindi ruotato, quindi ridimensionato, che produce un risultato molto diverso dalla prima scala, quindi ruota e quindi trasla:</span><span class="sxs-lookup"><span data-stu-id="4c2ef-119">The resulting order of operations is first translate, then rotate, then scale, which produces a very different result than first scale, then rotate, then translate:</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="4c2ef-120">Un modo per invertire l'ordine delle singole trasformazioni in una trasformazione composita consiste nell'invertire l'ordine di una sequenza di chiamate al metodo.</span><span class="sxs-lookup"><span data-stu-id="4c2ef-120">One way to reverse the order of the individual transformations in a composite transformation is to reverse the order of a sequence of method calls.</span></span> <span data-ttu-id="4c2ef-121">Un secondo modo per controllare l'ordine delle operazioni consiste nel modificare l'argomento dell'ordine della matrice.</span><span class="sxs-lookup"><span data-stu-id="4c2ef-121">A second way to control the order of operations is to change the matrix order argument.</span></span> <span data-ttu-id="4c2ef-122">L'esempio seguente è identico a quello dell'esempio precedente, ad eccezione del fatto che [\* \* \* \* MatrixOrderAppend \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) \* \* è stato modificato in \* \* \* [\* MatrixOrderPrepend \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder)\* \*.</span><span class="sxs-lookup"><span data-stu-id="4c2ef-122">The following example is the same as the previous example, except that [\*\*\*\*MatrixOrderAppend\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) has been changed to [\*\*\*\*MatrixOrderPrepend\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder).</span></span> <span data-ttu-id="4c2ef-123">La moltiplicazione di matrici viene eseguita nell'ordine SRT, dove S, R e T sono rispettivamente le matrici per la scala, la rotazione e la conversione.</span><span class="sxs-lookup"><span data-stu-id="4c2ef-123">The matrix multiplication is done in the order SRT, where S, R, and T are the matrices for scale, rotate, and translate, respectively.</span></span> <span data-ttu-id="4c2ef-124">L'ordine della trasformazione composita è la prima scala, quindi ruota e quindi trasla.</span><span class="sxs-lookup"><span data-stu-id="4c2ef-124">The order of the composite transformation is first scale, then rotate, then translate.</span></span>


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f,MatrixOrderPrepend);
graphics.RotateTransform(28.0f, MatrixOrderPrepend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderPrepend);
graphics.DrawRectangle(&pen, rect);
```



<span data-ttu-id="4c2ef-125">Il risultato dell'esempio precedente è lo stesso risultato ottenuto nel primo esempio di questa sezione.</span><span class="sxs-lookup"><span data-stu-id="4c2ef-125">The result of the preceding example is the same result that we achieved in the first example of this section.</span></span> <span data-ttu-id="4c2ef-126">Questo è dovuto al fatto che è stato invertito sia l'ordine delle chiamate al metodo che l'ordine della moltiplicazione di matrici.</span><span class="sxs-lookup"><span data-stu-id="4c2ef-126">This is because we reversed both the order of the method calls and the order of the matrix multiplication.</span></span>

 

 




---
description: Windows GDI+ espone un'API flat costituita da circa 600 funzioni. Microsoft .NET Framework fornisce un set di classi wrapper di codice gestito per GDI+.
ms.assetid: afd8cf81-8a20-4592-bd0a-46341742cc9b
title: API semplice GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65f91c3c925b7de31f27e91c70cbd1bf0cbbb2a4
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394986"
---
# <a name="gdi-flat-api"></a><span data-ttu-id="d6d39-104">API semplice GDI+</span><span class="sxs-lookup"><span data-stu-id="d6d39-104">GDI+ Flat API</span></span>

<span data-ttu-id="d6d39-105">Windows GDI+ espone un'API flat costituita da circa 600 funzioni, implementate in Gdiplus.dll e dichiarate in Gdiplusflat.h.</span><span class="sxs-lookup"><span data-stu-id="d6d39-105">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="d6d39-106">Le funzioni nell'API flat GDI+ vengono incapsulate da una raccolta di circa 40 classi C++.</span><span class="sxs-lookup"><span data-stu-id="d6d39-106">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="d6d39-107">È consigliabile non chiamare direttamente le funzioni nell'API flat.</span><span class="sxs-lookup"><span data-stu-id="d6d39-107">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="d6d39-108">Ogni volta che si effettuano chiamate a GDI+, è necessario eseguire questa operazione chiamando i metodi e le funzioni forniti dai wrapper C++.</span><span class="sxs-lookup"><span data-stu-id="d6d39-108">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="d6d39-109">Il Servizio Supporto Tecnico Clienti Microsoft non fornirà supporto per il codice che chiama direttamente l'API flat.</span><span class="sxs-lookup"><span data-stu-id="d6d39-109">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span>

<span data-ttu-id="d6d39-110">In alternativa ai wrapper C++, Microsoft .NET Framework fornisce un set di classi wrapper di codice gestito per GDI+.</span><span class="sxs-lookup"><span data-stu-id="d6d39-110">As an alternative to the C++ wrappers, the Microsoft .NET Framework provides a set of managed-code wrapper classes for GDI+.</span></span> <span data-ttu-id="d6d39-111">I wrapper di codice gestito per GDI+ appartengono agli spazi dei nomi seguenti.</span><span class="sxs-lookup"><span data-stu-id="d6d39-111">The managed-code wrappers for GDI+ belong to the following namespaces.</span></span>

-   [<span data-ttu-id="d6d39-112">System.Drawing</span><span class="sxs-lookup"><span data-stu-id="d6d39-112">System.Drawing</span></span>](/dotnet/api/system.drawing?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [<span data-ttu-id="d6d39-113">System.Drawing.Drawing2D</span><span class="sxs-lookup"><span data-stu-id="d6d39-113">System.Drawing.Drawing2D</span></span>](/dotnet/api/system.drawing.drawing2d?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [<span data-ttu-id="d6d39-114">System.drawing.imaging</span><span class="sxs-lookup"><span data-stu-id="d6d39-114">System.Drawing.Imaging</span></span>](/dotnet/api/system.drawing.imaging?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [<span data-ttu-id="d6d39-115">System.Drawing.Text</span><span class="sxs-lookup"><span data-stu-id="d6d39-115">System.Drawing.Text</span></span>](/dotnet/api/system.drawing.text?view=dotnet-plat-ext-3.1&preserve-view=true)

<span data-ttu-id="d6d39-116">Entrambi i set di wrapper (C++ e codice gestito) usano un approccio orientato a oggetti, quindi esistono alcune differenze tra il modo in cui i parametri vengono passati ai metodi wrapper e il modo in cui i parametri vengono passati alle funzioni nell'API flat.</span><span class="sxs-lookup"><span data-stu-id="d6d39-116">Both sets of wrappers (C++ and managed code) use an object-oriented approach, so there are some differences between the way parameters are passed to the wrapper methods and the way parameters are passed to functions in the flat API.</span></span> <span data-ttu-id="d6d39-117">Ad esempio, uno dei wrapper C++ è la [**classe Matrix.**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix)</span><span class="sxs-lookup"><span data-stu-id="d6d39-117">For example, one of the C++ wrappers is the [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) class.</span></span> <span data-ttu-id="d6d39-118">Ogni **oggetto Matrix** ha un campo, **nativeMatrix**, che punta a una variabile interna di tipo **GpMatrix.**</span><span class="sxs-lookup"><span data-stu-id="d6d39-118">Each **Matrix** object has a field, **nativeMatrix**, that points to an internal variable of type **GpMatrix**.</span></span> <span data-ttu-id="d6d39-119">Quando si passano parametri a un metodo di un oggetto **Matrix,** tale metodo passa tali parametri (o un set di parametri correlati) a una delle funzioni nell'API flat GDI+.</span><span class="sxs-lookup"><span data-stu-id="d6d39-119">When you pass parameters to a method of a **Matrix** object, that method passes those parameters (or a set of related parameters) along to one of the functions in the GDI+ flat API.</span></span> <span data-ttu-id="d6d39-120">Ma questo metodo passa anche il **campo nativeMatrix** (come parametro di input) alla funzione API flat.</span><span class="sxs-lookup"><span data-stu-id="d6d39-120">But that method also passes the **nativeMatrix** field (as an input parameter) to the flat API function.</span></span> <span data-ttu-id="d6d39-121">Il codice seguente illustra come il [**metodo Matrix::Shear**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear) chiama la funzione **GdipShearMatrix(GpMatrix \* matrix, REAL shearX, REAL shearY, GpMatrixOrder order).**</span><span class="sxs-lookup"><span data-stu-id="d6d39-121">The following code shows how the [**Matrix::Shear**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear) method calls the **GdipShearMatrix(GpMatrix \*matrix, REAL shearX, REAL shearY, GpMatrixOrder order)** function.</span></span>


```
Status Shear(
      IN REAL shearX, 
      IN REAL shearY,
      IN MatrixOrder order = MatrixOrderPrepend)
{
   ...
   GdipShearMatrix(nativeMatrix, shearX, shearY, order);
   ...
}
```



<span data-ttu-id="d6d39-122">I [**costruttori Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) passano l'indirizzo di una variabile puntatore **GpMatrix** (come parametro di output) alla **funzione GdipCreateMatrix(GpMatrix \* \* matrix).**</span><span class="sxs-lookup"><span data-stu-id="d6d39-122">The [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) constructors pass the address of a **GpMatrix** pointer variable (as an output parameter) to the **GdipCreateMatrix(GpMatrix \*\*matrix)** function.</span></span> <span data-ttu-id="d6d39-123">**GdipCreateMatrix** crea e inizializza una variabile **GpMatrix** interna e quindi assegna l'indirizzo di **GpMatrix** alla variabile puntatore.</span><span class="sxs-lookup"><span data-stu-id="d6d39-123">**GdipCreateMatrix** creates and initializes an internal **GpMatrix** variable and then assigns the address of the **GpMatrix** to the pointer variable.</span></span> <span data-ttu-id="d6d39-124">Il costruttore copia quindi il valore del puntatore nel **campo nativeMatrix.**</span><span class="sxs-lookup"><span data-stu-id="d6d39-124">Then the constructor copies the value of the pointer to the **nativeMatrix** field.</span></span>


```
Matrix()
{
   GpMatrix *matrix = NULL;
   lastResult = DllExports::GdipCreateMatrix(&matrix);
   SetNativeMatrix(matrix);
}

VOID SetNativeMatrix(GpMatrix *nativeMatrix)
{
   this->nativeMatrix = nativeMatrix;
}
```



<span data-ttu-id="d6d39-125">I metodi clone nelle classi wrapper non ricevono parametri, ma spesso passano due parametri alla funzione sottostante nell'API flat GDI+.</span><span class="sxs-lookup"><span data-stu-id="d6d39-125">Clone methods in the wrapper classes receive no parameters but often pass two parameters to the underlying function in the GDI+ flat API.</span></span> <span data-ttu-id="d6d39-126">Ad esempio, il metodo [**Matrix::Clone**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-clone) passa **nativeMatrix** (come parametro di input) e l'indirizzo di una variabile puntatore **GpMatrix** (come parametro di output) alla funzione **GdipCloneMatrix.**</span><span class="sxs-lookup"><span data-stu-id="d6d39-126">For example, the [**Matrix::Clone**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-clone) method passes **nativeMatrix** (as an input parameter) and the address of a **GpMatrix** pointer variable (as an output parameter) to the **GdipCloneMatrix** function.</span></span> <span data-ttu-id="d6d39-127">Il codice seguente illustra come il **metodo Matrix::Clone** chiama la **funzione GdipCloneMatrix(GpMatrix \* matrix, GpMatrix \* \* cloneMatrix).**</span><span class="sxs-lookup"><span data-stu-id="d6d39-127">The following code shows how the **Matrix::Clone** method calls the **GdipCloneMatrix(GpMatrix \*matrix, GpMatrix \*\*cloneMatrix)** function.</span></span>


```
Matrix *Clone() const
{
   GpMatrix *cloneMatrix = NULL;
   ...
   GdipCloneMatrix(nativeMatrix, &cloneMatrix));
   ...
   return new Matrix(cloneMatrix);
 }
```



<span data-ttu-id="d6d39-128">Le funzioni nell'API flat restituiscono un valore di tipo GpStatus.</span><span class="sxs-lookup"><span data-stu-id="d6d39-128">The functions in the flat API return a value of type GpStatus.</span></span> <span data-ttu-id="d6d39-129">L'enumerazione GpStatus è identica [**all'enumerazione Status**](/windows/win32/api/Gdiplustypes/ne-gdiplustypes-status) usata dai metodi wrapper.</span><span class="sxs-lookup"><span data-stu-id="d6d39-129">The GpStatus enumeration is identical to the [**Status**](/windows/win32/api/Gdiplustypes/ne-gdiplustypes-status) enumeration used by the wrapper methods.</span></span> <span data-ttu-id="d6d39-130">In GdiplusGpStubs.h GpStatus è definito come segue:</span><span class="sxs-lookup"><span data-stu-id="d6d39-130">In GdiplusGpStubs.h, GpStatus is defined as follows:</span></span>

`typedef Status GpStatus;`

<span data-ttu-id="d6d39-131">La maggior parte dei metodi nelle classi wrapper restituisce un valore di stato che indica se il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="d6d39-131">Most of the methods in the wrapper classes return a status value that indicates whether the method succeeded.</span></span> <span data-ttu-id="d6d39-132">Tuttavia, alcuni dei metodi wrapper restituiscono valori di stato.</span><span class="sxs-lookup"><span data-stu-id="d6d39-132">However, some of the wrapper methods return state values.</span></span> <span data-ttu-id="d6d39-133">Quando si chiama un metodo wrapper che restituisce un valore di stato, il metodo wrapper passa i parametri appropriati alla funzione sottostante nell'API flat GDI+.</span><span class="sxs-lookup"><span data-stu-id="d6d39-133">When you call a wrapper method that returns a state value, the wrapper method passes the appropriate parameters to the underlying function in the GDI+ flat API.</span></span> <span data-ttu-id="d6d39-134">Ad esempio, la classe [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) ha un metodo [**Matrix::IsInvertible**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-isinvertible) che passa il campo **nativeMatrix** e l'indirizzo di una variabile **BOOL** (come parametro di output) alla funzione **GdipIsMatrixInvertible.**</span><span class="sxs-lookup"><span data-stu-id="d6d39-134">For example, the [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) class has an [**Matrix::IsInvertible**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-isinvertible) method that passes the **nativeMatrix** field and and the address of a **BOOL** variable (as an output parameter) to the **GdipIsMatrixInvertible** function.</span></span> <span data-ttu-id="d6d39-135">Il codice seguente illustra come il **metodo Matrix::IsInvertible** chiama la funzione **GdipIsMatrixInvertible(GDIPCONST GpMatrix \* matrix, BOOL \* result).**</span><span class="sxs-lookup"><span data-stu-id="d6d39-135">The following code shows how the **Matrix::IsInvertible** method calls the **GdipIsMatrixInvertible(GDIPCONST GpMatrix \*matrix, BOOL \*result)** function.</span></span>


```
BOOL IsInvertible() const
{
   BOOL result = FALSE;
   ...
   GdipIsMatrixInvertible(nativeMatrix, &result);
   return result;
}
```



<span data-ttu-id="d6d39-136">Un altro wrapper è la [**classe Color.**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color)</span><span class="sxs-lookup"><span data-stu-id="d6d39-136">Another one of the wrappers is the [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) class.</span></span> <span data-ttu-id="d6d39-137">Un **oggetto Color** ha un singolo campo di tipo **ARGB,** definito come **DWORD.**</span><span class="sxs-lookup"><span data-stu-id="d6d39-137">A **Color** object has a single field of type **ARGB**, which is defined as a **DWORD**.</span></span> <span data-ttu-id="d6d39-138">Quando passi un **oggetto Color** a uno dei metodi wrapper, tale metodo passa il campo **ARGB** alla funzione sottostante nell'API flat GDI+.</span><span class="sxs-lookup"><span data-stu-id="d6d39-138">When you pass a **Color** object to one of the wrapper methods, that method passes the **ARGB** field along to the underlying function in the GDI+ flat API.</span></span> <span data-ttu-id="d6d39-139">Il codice seguente illustra come il [**metodo Pen::SetColor**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setcolor) chiama la **funzione GdipSetPenColor(GpPen \* pen, ARGB argb).**</span><span class="sxs-lookup"><span data-stu-id="d6d39-139">The following code shows how the [**Pen::SetColor**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setcolor) method calls the **GdipSetPenColor(GpPen \*pen, ARGB argb)** function.</span></span> <span data-ttu-id="d6d39-140">Il [**metodo Color::GetValue**](/windows/win32/api/Gdipluscolor/nf-gdipluscolor-color-getvalue) restituisce il valore del **campo ARGB.**</span><span class="sxs-lookup"><span data-stu-id="d6d39-140">The [**Color::GetValue**](/windows/win32/api/Gdipluscolor/nf-gdipluscolor-color-getvalue) method returns the value of the **ARGB** field.</span></span>


```
Status SetColor(IN const Color& color)
{
   ...
   GdipSetPenColor(nativePen, color.GetValue());
}
```



<span data-ttu-id="d6d39-141">Gli argomenti seguenti illustrano la relazione tra l'API flat GDI+ e i metodi wrapper C++.</span><span class="sxs-lookup"><span data-stu-id="d6d39-141">The following topics show the relationship between the GDI+ flat API and the C++ wrapper methods.</span></span>

-   [<span data-ttu-id="d6d39-142">Funzioni AdjustableArrowCap</span><span class="sxs-lookup"><span data-stu-id="d6d39-142">AdjustableArrowCap Functions</span></span>](-gdiplus-adjustablearrowcap-flat.md)
-   [<span data-ttu-id="d6d39-143">Funzioni bitmap</span><span class="sxs-lookup"><span data-stu-id="d6d39-143">Bitmap Functions</span></span>](-gdiplus-bitmap-flat.md)
-   [<span data-ttu-id="d6d39-144">Funzioni brush</span><span class="sxs-lookup"><span data-stu-id="d6d39-144">Brush Functions</span></span>](-gdiplus-brush-flat.md)
-   [<span data-ttu-id="d6d39-145">Funzioni CachedBitmap</span><span class="sxs-lookup"><span data-stu-id="d6d39-145">CachedBitmap Functions</span></span>](-gdiplus-cachedbitmap-flat.md)
-   [<span data-ttu-id="d6d39-146">Funzioni CustomLineCap</span><span class="sxs-lookup"><span data-stu-id="d6d39-146">CustomLineCap Functions</span></span>](-gdiplus-customlinecap-flat.md)
-   [<span data-ttu-id="d6d39-147">Funzioni per i tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="d6d39-147">Font Functions</span></span>](-gdiplus-font-flat.md)
-   [<span data-ttu-id="d6d39-148">FontFamilyFunctions</span><span class="sxs-lookup"><span data-stu-id="d6d39-148">FontFamilyFunctions</span></span>](-gdiplus-fontfamily-flat.md)
-   [<span data-ttu-id="d6d39-149">Funzioni di oggetti Graphics</span><span class="sxs-lookup"><span data-stu-id="d6d39-149">Graphics Functions</span></span>](-gdiplus-graphics-flat.md)
-   [<span data-ttu-id="d6d39-150">Funzioni GraphicsPath</span><span class="sxs-lookup"><span data-stu-id="d6d39-150">GraphicsPath Functions</span></span>](-gdiplus-graphicspath-flat.md)
-   [<span data-ttu-id="d6d39-151">Funzioni HatchBrush</span><span class="sxs-lookup"><span data-stu-id="d6d39-151">HatchBrush Functions</span></span>](-gdiplus-hatchbrush-flat.md)
-   [<span data-ttu-id="d6d39-152">Funzioni per le immagini</span><span class="sxs-lookup"><span data-stu-id="d6d39-152">Image Functions</span></span>](-gdiplus-image-flat.md)
-   [<span data-ttu-id="d6d39-153">Funzioni ImageAttributes</span><span class="sxs-lookup"><span data-stu-id="d6d39-153">ImageAttributes Functions</span></span>](-gdiplus-imageattributes-flat.md)
-   [<span data-ttu-id="d6d39-154">Funzioni LinearGradientBrush</span><span class="sxs-lookup"><span data-stu-id="d6d39-154">LinearGradientBrush Functions</span></span>](-gdiplus-lineargradientbrush-flat.md)
-   [<span data-ttu-id="d6d39-155">Funzioni di matrice</span><span class="sxs-lookup"><span data-stu-id="d6d39-155">Matrix Functions</span></span>](-gdiplus-matrix-flat.md)
-   [<span data-ttu-id="d6d39-156">Funzioni di memoria</span><span class="sxs-lookup"><span data-stu-id="d6d39-156">Memory Functions</span></span>](-gdiplus-memory-flat.md)
-   [<span data-ttu-id="d6d39-157">Funzioni di notifica</span><span class="sxs-lookup"><span data-stu-id="d6d39-157">Notification Functions</span></span>](-gdiplus-notification-flat.md)
-   [<span data-ttu-id="d6d39-158">Funzioni PathGradientBrush</span><span class="sxs-lookup"><span data-stu-id="d6d39-158">PathGradientBrush Functions</span></span>](-gdiplus-pathgradientbrush-flat.md)
-   [<span data-ttu-id="d6d39-159">Funzioni PathIterator</span><span class="sxs-lookup"><span data-stu-id="d6d39-159">PathIterator Functions</span></span>](-gdiplus-pathiterator-flat.md)
-   [<span data-ttu-id="d6d39-160">Funzioni pen</span><span class="sxs-lookup"><span data-stu-id="d6d39-160">Pen Functions</span></span>](-gdiplus-pen-flat.md)
-   [<span data-ttu-id="d6d39-161">Funzioni di area</span><span class="sxs-lookup"><span data-stu-id="d6d39-161">Region Functions</span></span>](-gdiplus-region-flat.md)
-   [<span data-ttu-id="d6d39-162">Funzioni SolidBrush</span><span class="sxs-lookup"><span data-stu-id="d6d39-162">SolidBrush Functions</span></span>](-gdiplus-solidbrush-flat.md)
-   [<span data-ttu-id="d6d39-163">Funzioni di formato stringa</span><span class="sxs-lookup"><span data-stu-id="d6d39-163">String Format Functions</span></span>](-gdiplus-stringformat-flat.md)
-   [<span data-ttu-id="d6d39-164">Funzioni di testo</span><span class="sxs-lookup"><span data-stu-id="d6d39-164">Text Functions</span></span>](-gdiplus-text-flat.md)
-   [<span data-ttu-id="d6d39-165">Funzioni del pennello trama</span><span class="sxs-lookup"><span data-stu-id="d6d39-165">Texture Brush Functions</span></span>](-gdiplus-texturebrush-flat.md)

 

 

---
description: Windows GDI+ espone un'API Flat costituita da circa 600 funzioni, implementate in Gdiplus.dll e dichiarate in Gdiplusflat. h.
ms.assetid: afd8cf81-8a20-4592-bd0a-46341742cc9b
title: API semplice GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 450f89439b6ead3b8cd9a49f52a6620571f6db54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994248"
---
# <a name="gdi-flat-api"></a><span data-ttu-id="9831b-103">API semplice GDI+</span><span class="sxs-lookup"><span data-stu-id="9831b-103">GDI+ Flat API</span></span>

<span data-ttu-id="9831b-104">Windows GDI+ espone un'API Flat costituita da circa 600 funzioni, implementate in Gdiplus.dll e dichiarate in Gdiplusflat. h.</span><span class="sxs-lookup"><span data-stu-id="9831b-104">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="9831b-105">Le funzioni nell'API flat di GDI+ sono racchiuse tra una raccolta di circa 40 classi C++.</span><span class="sxs-lookup"><span data-stu-id="9831b-105">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="9831b-106">Si consiglia di non chiamare direttamente le funzioni nell'API flat.</span><span class="sxs-lookup"><span data-stu-id="9831b-106">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="9831b-107">Quando si effettuano chiamate a GDI+, è necessario chiamare i metodi e le funzioni forniti dai wrapper C++.</span><span class="sxs-lookup"><span data-stu-id="9831b-107">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="9831b-108">Il servizio supporto tecnico Microsoft non fornirà il supporto per il codice che chiama direttamente l'API flat.</span><span class="sxs-lookup"><span data-stu-id="9831b-108">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span>

<span data-ttu-id="9831b-109">In alternativa ai wrapper C++, il Microsoft .NET Framework fornisce un set di classi wrapper di codice gestito per GDI+.</span><span class="sxs-lookup"><span data-stu-id="9831b-109">As an alternative to the C++ wrappers, the Microsoft .NET Framework provides a set of managed-code wrapper classes for GDI+.</span></span> <span data-ttu-id="9831b-110">I wrapper di codice gestito per GDI+ appartengono agli spazi dei nomi seguenti.</span><span class="sxs-lookup"><span data-stu-id="9831b-110">The managed-code wrappers for GDI+ belong to the following namespaces.</span></span>

-   [<span data-ttu-id="9831b-111">System.Drawing</span><span class="sxs-lookup"><span data-stu-id="9831b-111">System.Drawing</span></span>](/dotnet/api/system.drawing?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [<span data-ttu-id="9831b-112">System. Drawing. Drawing2D</span><span class="sxs-lookup"><span data-stu-id="9831b-112">System.Drawing.Drawing2D</span></span>](/dotnet/api/system.drawing.drawing2d?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [<span data-ttu-id="9831b-113">System. Drawing. Imaging</span><span class="sxs-lookup"><span data-stu-id="9831b-113">System.Drawing.Imaging</span></span>](/dotnet/api/system.drawing.imaging?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [<span data-ttu-id="9831b-114">System. Drawing. Text</span><span class="sxs-lookup"><span data-stu-id="9831b-114">System.Drawing.Text</span></span>](/dotnet/api/system.drawing.text?view=dotnet-plat-ext-3.1&preserve-view=true)

<span data-ttu-id="9831b-115">Entrambi i set di wrapper (C++ e codice gestito) utilizzano un approccio orientato agli oggetti, quindi esistono alcune differenze tra il modo in cui i parametri vengono passati ai metodi wrapper e il modo in cui i parametri vengono passati alle funzioni nell'API flat.</span><span class="sxs-lookup"><span data-stu-id="9831b-115">Both sets of wrappers (C++ and managed code) use an object-oriented approach, so there are some differences between the way parameters are passed to the wrapper methods and the way parameters are passed to functions in the flat API.</span></span> <span data-ttu-id="9831b-116">Ad esempio, uno dei wrapper C++ è la classe [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) .</span><span class="sxs-lookup"><span data-stu-id="9831b-116">For example, one of the C++ wrappers is the [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) class.</span></span> <span data-ttu-id="9831b-117">Ogni oggetto **Matrix** dispone di un campo, **nativeMatrix**, che punta a una variabile interna di tipo **GpMatrix**.</span><span class="sxs-lookup"><span data-stu-id="9831b-117">Each **Matrix** object has a field, **nativeMatrix**, that points to an internal variable of type **GpMatrix**.</span></span> <span data-ttu-id="9831b-118">Quando si passano parametri a un metodo di un oggetto **Matrix** , il metodo passa tali parametri (o un set di parametri correlati) a una delle funzioni nell'API flat di GDI+.</span><span class="sxs-lookup"><span data-stu-id="9831b-118">When you pass parameters to a method of a **Matrix** object, that method passes those parameters (or a set of related parameters) along to one of the functions in the GDI+ flat API.</span></span> <span data-ttu-id="9831b-119">Questo metodo passa anche il campo **nativeMatrix** (come parametro di input) alla funzione API flat.</span><span class="sxs-lookup"><span data-stu-id="9831b-119">But that method also passes the **nativeMatrix** field (as an input parameter) to the flat API function.</span></span> <span data-ttu-id="9831b-120">Nel codice seguente viene illustrato il modo in cui il metodo [**Matrix:: Shear**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear) chiama la funzione **GdipShearMatrix (GPMATRIX \* Matrix, Real shearX, Real shearY, GpMatrixOrder Order)** .</span><span class="sxs-lookup"><span data-stu-id="9831b-120">The following code shows how the [**Matrix::Shear**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear) method calls the **GdipShearMatrix(GpMatrix \*matrix, REAL shearX, REAL shearY, GpMatrixOrder order)** function.</span></span>


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



<span data-ttu-id="9831b-121">I costruttori di [**matrici**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) passano l'indirizzo di una variabile puntatore **GpMatrix** (come parametro di output) alla funzione **GdipCreateMatrix ( \* \* matrice GpMatrix)** .</span><span class="sxs-lookup"><span data-stu-id="9831b-121">The [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) constructors pass the address of a **GpMatrix** pointer variable (as an output parameter) to the **GdipCreateMatrix(GpMatrix \*\*matrix)** function.</span></span> <span data-ttu-id="9831b-122">**GdipCreateMatrix** crea e Inizializza una variabile **GpMatrix** interna e quindi assegna l'indirizzo del **GpMatrix** alla variabile puntatore.</span><span class="sxs-lookup"><span data-stu-id="9831b-122">**GdipCreateMatrix** creates and initializes an internal **GpMatrix** variable and then assigns the address of the **GpMatrix** to the pointer variable.</span></span> <span data-ttu-id="9831b-123">Il costruttore copia quindi il valore del puntatore nel campo **nativeMatrix** .</span><span class="sxs-lookup"><span data-stu-id="9831b-123">Then the constructor copies the value of the pointer to the **nativeMatrix** field.</span></span>


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



<span data-ttu-id="9831b-124">I metodi Clone nelle classi wrapper non ricevono parametri, ma spesso passano due parametri alla funzione sottostante nell'API flat di GDI+.</span><span class="sxs-lookup"><span data-stu-id="9831b-124">Clone methods in the wrapper classes receive no parameters but often pass two parameters to the underlying function in the GDI+ flat API.</span></span> <span data-ttu-id="9831b-125">Ad esempio, il metodo [**Matrix:: Clone**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-clone) passa **nativeMatrix** (come parametro di input) e l'indirizzo di una variabile puntatore **GpMatrix** (come parametro di output) alla funzione **GdipCloneMatrix** .</span><span class="sxs-lookup"><span data-stu-id="9831b-125">For example, the [**Matrix::Clone**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-clone) method passes **nativeMatrix** (as an input parameter) and the address of a **GpMatrix** pointer variable (as an output parameter) to the **GdipCloneMatrix** function.</span></span> <span data-ttu-id="9831b-126">Nel codice seguente viene illustrato il modo in cui il metodo **Matrix:: Clone** chiama la funzione **GdipCloneMatrix (GpMatrix \* Matrix, GpMatrix \* \* cloneMatrix)** .</span><span class="sxs-lookup"><span data-stu-id="9831b-126">The following code shows how the **Matrix::Clone** method calls the **GdipCloneMatrix(GpMatrix \*matrix, GpMatrix \*\*cloneMatrix)** function.</span></span>


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



<span data-ttu-id="9831b-127">Le funzioni nell'API Flat restituiscono un valore di tipo GpStatus.</span><span class="sxs-lookup"><span data-stu-id="9831b-127">The functions in the flat API return a value of type GpStatus.</span></span> <span data-ttu-id="9831b-128">L'enumerazione GpStatus è identica all'enumerazione di [**stato**](/windows/win32/api/Gdiplustypes/ne-gdiplustypes-status) utilizzata dai metodi wrapper.</span><span class="sxs-lookup"><span data-stu-id="9831b-128">The GpStatus enumeration is identical to the [**Status**](/windows/win32/api/Gdiplustypes/ne-gdiplustypes-status) enumeration used by the wrapper methods.</span></span> <span data-ttu-id="9831b-129">In GdiplusGpStubs. h, GpStatus è definito come segue:</span><span class="sxs-lookup"><span data-stu-id="9831b-129">In GdiplusGpStubs.h, GpStatus is defined as follows:</span></span>

`typedef Status GpStatus;`

<span data-ttu-id="9831b-130">La maggior parte dei metodi nelle classi wrapper restituisce un valore di stato che indica se il metodo ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="9831b-130">Most of the methods in the wrapper classes return a status value that indicates whether the method succeeded.</span></span> <span data-ttu-id="9831b-131">Tuttavia, alcuni dei metodi wrapper restituiscono valori di stato.</span><span class="sxs-lookup"><span data-stu-id="9831b-131">However, some of the wrapper methods return state values.</span></span> <span data-ttu-id="9831b-132">Quando si chiama un metodo wrapper che restituisce un valore di stato, il metodo wrapper passa i parametri appropriati alla funzione sottostante nell'API flat di GDI+.</span><span class="sxs-lookup"><span data-stu-id="9831b-132">When you call a wrapper method that returns a state value, the wrapper method passes the appropriate parameters to the underlying function in the GDI+ flat API.</span></span> <span data-ttu-id="9831b-133">Ad esempio, la classe [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) dispone di un metodo [**Matrix:: IsInvertible**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-isinvertible) che passa il campo **nativeMatrix** e e l'indirizzo di una variabile **bool** (come parametro di output) alla funzione **GdipIsMatrixInvertible** .</span><span class="sxs-lookup"><span data-stu-id="9831b-133">For example, the [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) class has an [**Matrix::IsInvertible**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-isinvertible) method that passes the **nativeMatrix** field and and the address of a **BOOL** variable (as an output parameter) to the **GdipIsMatrixInvertible** function.</span></span> <span data-ttu-id="9831b-134">Il codice seguente illustra come il metodo **Matrix:: IsInvertible** chiama la funzione **GdipIsMatrixInvertible (GDIPCONST GpMatrix \* Matrix, \* result bool)** .</span><span class="sxs-lookup"><span data-stu-id="9831b-134">The following code shows how the **Matrix::IsInvertible** method calls the **GdipIsMatrixInvertible(GDIPCONST GpMatrix \*matrix, BOOL \*result)** function.</span></span>


```
BOOL IsInvertible() const
{
   BOOL result = FALSE;
   ...
   GdipIsMatrixInvertible(nativeMatrix, &result);
   return result;
}
```



<span data-ttu-id="9831b-135">Un altro wrapper è la classe [**color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) .</span><span class="sxs-lookup"><span data-stu-id="9831b-135">Another one of the wrappers is the [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) class.</span></span> <span data-ttu-id="9831b-136">Un oggetto **color** ha un solo campo di tipo **ARGB**, che è definito come un **valore DWORD**.</span><span class="sxs-lookup"><span data-stu-id="9831b-136">A **Color** object has a single field of type **ARGB**, which is defined as a **DWORD**.</span></span> <span data-ttu-id="9831b-137">Quando si passa un oggetto **color** a uno dei metodi wrapper, il metodo passa il campo **ARGB** insieme alla funzione sottostante nell'API flat di GDI+.</span><span class="sxs-lookup"><span data-stu-id="9831b-137">When you pass a **Color** object to one of the wrapper methods, that method passes the **ARGB** field along to the underlying function in the GDI+ flat API.</span></span> <span data-ttu-id="9831b-138">Il codice seguente illustra come il metodo [**Pen:: Secolor**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setcolor) chiama la funzione **GdipSetPenColor (GPPEN \* Pen, ARGB ARGB)** .</span><span class="sxs-lookup"><span data-stu-id="9831b-138">The following code shows how the [**Pen::SetColor**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setcolor) method calls the **GdipSetPenColor(GpPen \*pen, ARGB argb)** function.</span></span> <span data-ttu-id="9831b-139">Il metodo [**color:: GetValue**](/windows/win32/api/Gdipluscolor/nf-gdipluscolor-color-getvalue) restituisce il valore del campo **ARGB** .</span><span class="sxs-lookup"><span data-stu-id="9831b-139">The [**Color::GetValue**](/windows/win32/api/Gdipluscolor/nf-gdipluscolor-color-getvalue) method returns the value of the **ARGB** field.</span></span>


```
Status SetColor(IN const Color& color)
{
   ...
   GdipSetPenColor(nativePen, color.GetValue());
}
```



<span data-ttu-id="9831b-140">Negli argomenti seguenti viene illustrata la relazione tra l'API Flat GDI+ e i metodi wrapper C++.</span><span class="sxs-lookup"><span data-stu-id="9831b-140">The following topics show the relationship between the GDI+ flat API and the C++ wrapper methods.</span></span>

-   [<span data-ttu-id="9831b-141">Funzioni AdjustableArrowCap</span><span class="sxs-lookup"><span data-stu-id="9831b-141">AdjustableArrowCap Functions</span></span>](-gdiplus-adjustablearrowcap-flat.md)
-   [<span data-ttu-id="9831b-142">Funzioni bitmap</span><span class="sxs-lookup"><span data-stu-id="9831b-142">Bitmap Functions</span></span>](-gdiplus-bitmap-flat.md)
-   [<span data-ttu-id="9831b-143">Funzioni pennello</span><span class="sxs-lookup"><span data-stu-id="9831b-143">Brush Functions</span></span>](-gdiplus-brush-flat.md)
-   [<span data-ttu-id="9831b-144">Funzioni CachedBitmap</span><span class="sxs-lookup"><span data-stu-id="9831b-144">CachedBitmap Functions</span></span>](-gdiplus-cachedbitmap-flat.md)
-   [<span data-ttu-id="9831b-145">Funzioni CustomLineCap</span><span class="sxs-lookup"><span data-stu-id="9831b-145">CustomLineCap Functions</span></span>](-gdiplus-customlinecap-flat.md)
-   [<span data-ttu-id="9831b-146">Funzioni dei tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="9831b-146">Font Functions</span></span>](-gdiplus-font-flat.md)
-   [<span data-ttu-id="9831b-147">FontFamilyFunctions</span><span class="sxs-lookup"><span data-stu-id="9831b-147">FontFamilyFunctions</span></span>](-gdiplus-fontfamily-flat.md)
-   [<span data-ttu-id="9831b-148">Funzioni di oggetti Graphics</span><span class="sxs-lookup"><span data-stu-id="9831b-148">Graphics Functions</span></span>](-gdiplus-graphics-flat.md)
-   [<span data-ttu-id="9831b-149">Funzioni GraphicsPath</span><span class="sxs-lookup"><span data-stu-id="9831b-149">GraphicsPath Functions</span></span>](-gdiplus-graphicspath-flat.md)
-   [<span data-ttu-id="9831b-150">Funzioni HatchBrush</span><span class="sxs-lookup"><span data-stu-id="9831b-150">HatchBrush Functions</span></span>](-gdiplus-hatchbrush-flat.md)
-   [<span data-ttu-id="9831b-151">Funzioni per le immagini</span><span class="sxs-lookup"><span data-stu-id="9831b-151">Image Functions</span></span>](-gdiplus-image-flat.md)
-   [<span data-ttu-id="9831b-152">Funzioni ImageAttributes</span><span class="sxs-lookup"><span data-stu-id="9831b-152">ImageAttributes Functions</span></span>](-gdiplus-imageattributes-flat.md)
-   [<span data-ttu-id="9831b-153">Funzioni LinearGradientBrush</span><span class="sxs-lookup"><span data-stu-id="9831b-153">LinearGradientBrush Functions</span></span>](-gdiplus-lineargradientbrush-flat.md)
-   [<span data-ttu-id="9831b-154">Funzioni Matrix</span><span class="sxs-lookup"><span data-stu-id="9831b-154">Matrix Functions</span></span>](-gdiplus-matrix-flat.md)
-   [<span data-ttu-id="9831b-155">Funzioni di memoria</span><span class="sxs-lookup"><span data-stu-id="9831b-155">Memory Functions</span></span>](-gdiplus-memory-flat.md)
-   [<span data-ttu-id="9831b-156">Funzioni di notifica</span><span class="sxs-lookup"><span data-stu-id="9831b-156">Notification Functions</span></span>](-gdiplus-notification-flat.md)
-   [<span data-ttu-id="9831b-157">Funzioni PathGradientBrush</span><span class="sxs-lookup"><span data-stu-id="9831b-157">PathGradientBrush Functions</span></span>](-gdiplus-pathgradientbrush-flat.md)
-   [<span data-ttu-id="9831b-158">Funzioni PathIterator</span><span class="sxs-lookup"><span data-stu-id="9831b-158">PathIterator Functions</span></span>](-gdiplus-pathiterator-flat.md)
-   [<span data-ttu-id="9831b-159">Funzioni Pen</span><span class="sxs-lookup"><span data-stu-id="9831b-159">Pen Functions</span></span>](-gdiplus-pen-flat.md)
-   [<span data-ttu-id="9831b-160">Funzioni Region</span><span class="sxs-lookup"><span data-stu-id="9831b-160">Region Functions</span></span>](-gdiplus-region-flat.md)
-   [<span data-ttu-id="9831b-161">Funzioni SolidBrush</span><span class="sxs-lookup"><span data-stu-id="9831b-161">SolidBrush Functions</span></span>](-gdiplus-solidbrush-flat.md)
-   [<span data-ttu-id="9831b-162">Funzioni in formato stringa</span><span class="sxs-lookup"><span data-stu-id="9831b-162">String Format Functions</span></span>](-gdiplus-stringformat-flat.md)
-   [<span data-ttu-id="9831b-163">Funzioni di testo</span><span class="sxs-lookup"><span data-stu-id="9831b-163">Text Functions</span></span>](-gdiplus-text-flat.md)
-   [<span data-ttu-id="9831b-164">Funzioni pennello trama</span><span class="sxs-lookup"><span data-stu-id="9831b-164">Texture Brush Functions</span></span>](-gdiplus-texturebrush-flat.md)

 

 

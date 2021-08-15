---
description: Windows GDI+ espone un'API flat costituita da circa 600 funzioni. Microsoft .NET Framework fornisce un set di classi wrapper di codice gestito per GDI+.
ms.assetid: afd8cf81-8a20-4592-bd0a-46341742cc9b
title: API semplice GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37dee1288bdbbf86c39d201d5ccc066c1eab16cb600950edd5e848cd250e0ed8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977551"
---
# <a name="gdi-flat-api"></a>API semplice GDI+

Windows GDI+ espone un'API flat costituita da circa 600 funzioni, implementate in Gdiplus.dll e dichiarate in Gdiplusflat.h. Le funzioni nell'API GDI+ sono incapsulate da una raccolta di circa 40 classi C++. È consigliabile non chiamare direttamente le funzioni nell'API flat. Ogni volta che si effettuano GDI+, è necessario eseguire questa operazione chiamando i metodi e le funzioni forniti dai wrapper C++. Il Servizio Supporto Tecnico Clienti Microsoft non fornirà supporto per il codice che chiama direttamente l'API flat.

In alternativa ai wrapper C++, Microsoft .NET Framework fornisce un set di classi wrapper di codice gestito per GDI+. I wrapper di codice gestito per GDI+ appartengono agli spazi dei nomi seguenti.

-   [System.Drawing](/dotnet/api/system.drawing?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [System.Drawing.Drawing2D](/dotnet/api/system.drawing.drawing2d?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [System.drawing.imaging](/dotnet/api/system.drawing.imaging?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [System.Drawing.Text](/dotnet/api/system.drawing.text?view=dotnet-plat-ext-3.1&preserve-view=true)

Entrambi i set di wrapper (C++ e codice gestito) usano un approccio orientato a oggetti, quindi esistono alcune differenze tra il modo in cui i parametri vengono passati ai metodi wrapper e il modo in cui i parametri vengono passati alle funzioni nell'API flat. Ad esempio, uno dei wrapper C++ è la [**classe Matrix.**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) Ogni **oggetto Matrix** ha un campo, **nativeMatrix**, che punta a una variabile interna di tipo **GpMatrix.** Quando si passano parametri a un metodo di un oggetto **Matrix,** tale metodo passa tali parametri (o un set di parametri correlati) a una delle funzioni nell'API GDI+ flat. Ma questo metodo passa anche il **campo nativeMatrix** (come parametro di input) alla funzione API flat. Il codice seguente illustra come il [**metodo Matrix::Shear**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear) chiama la funzione **GdipShearMatrix(GpMatrix \* matrix, REAL shearX, REAL shearY, GpMatrixOrder order).**


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



I [**costruttori Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) passano l'indirizzo di una variabile puntatore **GpMatrix** (come parametro di output) alla **funzione GdipCreateMatrix(GpMatrix \* \* matrix).** **GdipCreateMatrix** crea e inizializza una variabile **GpMatrix** interna e quindi assegna l'indirizzo di **GpMatrix** alla variabile puntatore. Il costruttore copia quindi il valore del puntatore nel **campo nativeMatrix.**


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



I metodi clone nelle classi wrapper non ricevono parametri, ma spesso passano due parametri alla funzione sottostante nell'API GDI+ semplice. Ad esempio, il metodo [**Matrix::Clone**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-clone) passa **nativeMatrix** (come parametro di input) e l'indirizzo di una variabile puntatore **GpMatrix** (come parametro di output) alla funzione **GdipCloneMatrix.** Il codice seguente illustra come il **metodo Matrix::Clone** chiama la **funzione GdipCloneMatrix(GpMatrix \* matrix, GpMatrix \* \* cloneMatrix).**


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



Le funzioni nell'API flat restituiscono un valore di tipo GpStatus. L'enumerazione GpStatus è identica [**all'enumerazione Status**](/windows/win32/api/Gdiplustypes/ne-gdiplustypes-status) usata dai metodi wrapper. In GdiplusGpStubs.h GpStatus viene definito come segue:

`typedef Status GpStatus;`

La maggior parte dei metodi nelle classi wrapper restituisce un valore di stato che indica se il metodo è riuscito. Tuttavia, alcuni dei metodi wrapper restituiscono valori di stato. Quando si chiama un metodo wrapper che restituisce un valore di stato, il metodo wrapper passa i parametri appropriati alla funzione sottostante nell'API GDI+ semplice. Ad esempio, la classe [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) ha un metodo [**Matrix::IsInvertible**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-isinvertible) che passa il campo **nativeMatrix** e l'indirizzo di una variabile **BOOL** (come parametro di output) alla funzione **GdipIsMatrixInvertible.** Il codice seguente illustra come il **metodo Matrix::IsInvertible** chiama la funzione **GdipIsMatrixInvertible(GDIPCONST GpMatrix \* matrix, BOOL \* result).**


```
BOOL IsInvertible() const
{
   BOOL result = FALSE;
   ...
   GdipIsMatrixInvertible(nativeMatrix, &result);
   return result;
}
```



Un altro wrapper è la [**classe Color.**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) Un **oggetto Color** ha un singolo campo di tipo **ARGB,** definito come **DWORD.** Quando passi un **oggetto Color** a uno dei metodi wrapper, tale metodo passa il campo **ARGB** alla funzione sottostante nell'API GDI+ flat. Il codice seguente illustra come il [**metodo Pen::SetColor**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setcolor) chiama la **funzione GdipSetPenColor(GpPen \* pen, ARGB argb).** Il [**metodo Color::GetValue**](/windows/win32/api/Gdipluscolor/nf-gdipluscolor-color-getvalue) restituisce il valore del **campo ARGB.**


```
Status SetColor(IN const Color& color)
{
   ...
   GdipSetPenColor(nativePen, color.GetValue());
}
```



Negli argomenti seguenti viene illustrata la relazione tra l GDI+aPI flat e i metodi wrapper C++.

-   [Funzioni AdjustableArrowCap](-gdiplus-adjustablearrowcap-flat.md)
-   [Funzioni bitmap](-gdiplus-bitmap-flat.md)
-   [Funzioni brush](-gdiplus-brush-flat.md)
-   [Funzioni CachedBitmap](-gdiplus-cachedbitmap-flat.md)
-   [Funzioni CustomLineCap](-gdiplus-customlinecap-flat.md)
-   [Funzioni per i tipi di carattere](-gdiplus-font-flat.md)
-   [FontFamilyFunctions](-gdiplus-fontfamily-flat.md)
-   [Funzioni di oggetti Graphics](-gdiplus-graphics-flat.md)
-   [Funzioni GraphicsPath](-gdiplus-graphicspath-flat.md)
-   [Funzioni HatchBrush](-gdiplus-hatchbrush-flat.md)
-   [Funzioni per le immagini](-gdiplus-image-flat.md)
-   [Funzioni ImageAttributes](-gdiplus-imageattributes-flat.md)
-   [Funzioni LinearGradientBrush](-gdiplus-lineargradientbrush-flat.md)
-   [Funzioni di matrice](-gdiplus-matrix-flat.md)
-   [Funzioni di memoria](-gdiplus-memory-flat.md)
-   [Funzioni di notifica](-gdiplus-notification-flat.md)
-   [Funzioni PathGradientBrush](-gdiplus-pathgradientbrush-flat.md)
-   [Funzioni PathIterator](-gdiplus-pathiterator-flat.md)
-   [Funzioni pen](-gdiplus-pen-flat.md)
-   [Funzioni di area](-gdiplus-region-flat.md)
-   [Funzioni SolidBrush](-gdiplus-solidbrush-flat.md)
-   [Funzioni di formato stringa](-gdiplus-stringformat-flat.md)
-   [Funzioni di testo](-gdiplus-text-flat.md)
-   [Funzioni del pennello trama](-gdiplus-texturebrush-flat.md)

 

 

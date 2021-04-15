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
# <a name="gdi-flat-api"></a>API semplice GDI+

Windows GDI+ espone un'API Flat costituita da circa 600 funzioni, implementate in Gdiplus.dll e dichiarate in Gdiplusflat. h. Le funzioni nell'API flat di GDI+ sono racchiuse tra una raccolta di circa 40 classi C++. Si consiglia di non chiamare direttamente le funzioni nell'API flat. Quando si effettuano chiamate a GDI+, è necessario chiamare i metodi e le funzioni forniti dai wrapper C++. Il servizio supporto tecnico Microsoft non fornirà il supporto per il codice che chiama direttamente l'API flat.

In alternativa ai wrapper C++, il Microsoft .NET Framework fornisce un set di classi wrapper di codice gestito per GDI+. I wrapper di codice gestito per GDI+ appartengono agli spazi dei nomi seguenti.

-   [System.Drawing](/dotnet/api/system.drawing?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [System. Drawing. Drawing2D](/dotnet/api/system.drawing.drawing2d?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [System. Drawing. Imaging](/dotnet/api/system.drawing.imaging?view=dotnet-plat-ext-3.1&preserve-view=true)
-   [System. Drawing. Text](/dotnet/api/system.drawing.text?view=dotnet-plat-ext-3.1&preserve-view=true)

Entrambi i set di wrapper (C++ e codice gestito) utilizzano un approccio orientato agli oggetti, quindi esistono alcune differenze tra il modo in cui i parametri vengono passati ai metodi wrapper e il modo in cui i parametri vengono passati alle funzioni nell'API flat. Ad esempio, uno dei wrapper C++ è la classe [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) . Ogni oggetto **Matrix** dispone di un campo, **nativeMatrix**, che punta a una variabile interna di tipo **GpMatrix**. Quando si passano parametri a un metodo di un oggetto **Matrix** , il metodo passa tali parametri (o un set di parametri correlati) a una delle funzioni nell'API flat di GDI+. Questo metodo passa anche il campo **nativeMatrix** (come parametro di input) alla funzione API flat. Nel codice seguente viene illustrato il modo in cui il metodo [**Matrix:: Shear**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear) chiama la funzione **GdipShearMatrix (GPMATRIX \* Matrix, Real shearX, Real shearY, GpMatrixOrder Order)** .


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



I costruttori di [**matrici**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) passano l'indirizzo di una variabile puntatore **GpMatrix** (come parametro di output) alla funzione **GdipCreateMatrix ( \* \* matrice GpMatrix)** . **GdipCreateMatrix** crea e Inizializza una variabile **GpMatrix** interna e quindi assegna l'indirizzo del **GpMatrix** alla variabile puntatore. Il costruttore copia quindi il valore del puntatore nel campo **nativeMatrix** .


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



I metodi Clone nelle classi wrapper non ricevono parametri, ma spesso passano due parametri alla funzione sottostante nell'API flat di GDI+. Ad esempio, il metodo [**Matrix:: Clone**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-clone) passa **nativeMatrix** (come parametro di input) e l'indirizzo di una variabile puntatore **GpMatrix** (come parametro di output) alla funzione **GdipCloneMatrix** . Nel codice seguente viene illustrato il modo in cui il metodo **Matrix:: Clone** chiama la funzione **GdipCloneMatrix (GpMatrix \* Matrix, GpMatrix \* \* cloneMatrix)** .


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



Le funzioni nell'API Flat restituiscono un valore di tipo GpStatus. L'enumerazione GpStatus è identica all'enumerazione di [**stato**](/windows/win32/api/Gdiplustypes/ne-gdiplustypes-status) utilizzata dai metodi wrapper. In GdiplusGpStubs. h, GpStatus è definito come segue:

`typedef Status GpStatus;`

La maggior parte dei metodi nelle classi wrapper restituisce un valore di stato che indica se il metodo ha avuto esito positivo. Tuttavia, alcuni dei metodi wrapper restituiscono valori di stato. Quando si chiama un metodo wrapper che restituisce un valore di stato, il metodo wrapper passa i parametri appropriati alla funzione sottostante nell'API flat di GDI+. Ad esempio, la classe [**Matrix**](/windows/win32/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) dispone di un metodo [**Matrix:: IsInvertible**](/windows/win32/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-isinvertible) che passa il campo **nativeMatrix** e e l'indirizzo di una variabile **bool** (come parametro di output) alla funzione **GdipIsMatrixInvertible** . Il codice seguente illustra come il metodo **Matrix:: IsInvertible** chiama la funzione **GdipIsMatrixInvertible (GDIPCONST GpMatrix \* Matrix, \* result bool)** .


```
BOOL IsInvertible() const
{
   BOOL result = FALSE;
   ...
   GdipIsMatrixInvertible(nativeMatrix, &result);
   return result;
}
```



Un altro wrapper è la classe [**color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) . Un oggetto **color** ha un solo campo di tipo **ARGB**, che è definito come un **valore DWORD**. Quando si passa un oggetto **color** a uno dei metodi wrapper, il metodo passa il campo **ARGB** insieme alla funzione sottostante nell'API flat di GDI+. Il codice seguente illustra come il metodo [**Pen:: Secolor**](/windows/win32/api/Gdipluspen/nf-gdipluspen-pen-setcolor) chiama la funzione **GdipSetPenColor (GPPEN \* Pen, ARGB ARGB)** . Il metodo [**color:: GetValue**](/windows/win32/api/Gdipluscolor/nf-gdipluscolor-color-getvalue) restituisce il valore del campo **ARGB** .


```
Status SetColor(IN const Color& color)
{
   ...
   GdipSetPenColor(nativePen, color.GetValue());
}
```



Negli argomenti seguenti viene illustrata la relazione tra l'API Flat GDI+ e i metodi wrapper C++.

-   [Funzioni AdjustableArrowCap](-gdiplus-adjustablearrowcap-flat.md)
-   [Funzioni bitmap](-gdiplus-bitmap-flat.md)
-   [Funzioni pennello](-gdiplus-brush-flat.md)
-   [Funzioni CachedBitmap](-gdiplus-cachedbitmap-flat.md)
-   [Funzioni CustomLineCap](-gdiplus-customlinecap-flat.md)
-   [Funzioni dei tipi di carattere](-gdiplus-font-flat.md)
-   [FontFamilyFunctions](-gdiplus-fontfamily-flat.md)
-   [Funzioni di oggetti Graphics](-gdiplus-graphics-flat.md)
-   [Funzioni GraphicsPath](-gdiplus-graphicspath-flat.md)
-   [Funzioni HatchBrush](-gdiplus-hatchbrush-flat.md)
-   [Funzioni per le immagini](-gdiplus-image-flat.md)
-   [Funzioni ImageAttributes](-gdiplus-imageattributes-flat.md)
-   [Funzioni LinearGradientBrush](-gdiplus-lineargradientbrush-flat.md)
-   [Funzioni Matrix](-gdiplus-matrix-flat.md)
-   [Funzioni di memoria](-gdiplus-memory-flat.md)
-   [Funzioni di notifica](-gdiplus-notification-flat.md)
-   [Funzioni PathGradientBrush](-gdiplus-pathgradientbrush-flat.md)
-   [Funzioni PathIterator](-gdiplus-pathiterator-flat.md)
-   [Funzioni Pen](-gdiplus-pen-flat.md)
-   [Funzioni Region](-gdiplus-region-flat.md)
-   [Funzioni SolidBrush](-gdiplus-solidbrush-flat.md)
-   [Funzioni in formato stringa](-gdiplus-stringformat-flat.md)
-   [Funzioni di testo](-gdiplus-text-flat.md)
-   [Funzioni pennello trama](-gdiplus-texturebrush-flat.md)

 

 

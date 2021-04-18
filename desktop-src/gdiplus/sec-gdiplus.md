---
description: In questo argomento vengono fornite informazioni sulle considerazioni sulla sicurezza correlate alla programmazione con Windows GDI+.
ms.assetid: 411e16e4-ad8f-4567-8964-564f08283ba5
title: 'Considerazioni sulla sicurezza: GDI+'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d8c9d50393708e58651566ee90adcb4339cb9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994165"
---
# <a name="security-considerations-gdi"></a><span data-ttu-id="5a78e-103">Considerazioni sulla sicurezza: GDI+</span><span class="sxs-lookup"><span data-stu-id="5a78e-103">Security Considerations: GDI+</span></span>

<span data-ttu-id="5a78e-104">In questo argomento vengono fornite informazioni sulle considerazioni sulla sicurezza correlate alla programmazione con Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="5a78e-104">This topic provides information about security considerations related to programming with Windows GDI+.</span></span> <span data-ttu-id="5a78e-105">Questo argomento non fornisce tutte le informazioni necessarie per i problemi di sicurezza, ma è possibile usarlo come punto di partenza e riferimento per questa area tecnologica.</span><span class="sxs-lookup"><span data-stu-id="5a78e-105">This topic doesn't provide all you need to know about security issues—instead, use it as a starting point and reference for this technology area.</span></span>

-   [<span data-ttu-id="5a78e-106">Verifica della riuscita dei costruttori</span><span class="sxs-lookup"><span data-stu-id="5a78e-106">Verifying the Success of Constructors</span></span>](#verifying-the-success-of-constructors)
-   [<span data-ttu-id="5a78e-107">Allocazione di buffer</span><span class="sxs-lookup"><span data-stu-id="5a78e-107">Allocating Buffers</span></span>](#allocating-buffers)
-   [<span data-ttu-id="5a78e-108">Controllo errori</span><span class="sxs-lookup"><span data-stu-id="5a78e-108">Error Checking</span></span>](#error-checking)
-   [<span data-ttu-id="5a78e-109">Sincronizzazione di thread</span><span class="sxs-lookup"><span data-stu-id="5a78e-109">Thread Synchronization</span></span>](#thread-synchronization)
-   [<span data-ttu-id="5a78e-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5a78e-110">Related topics</span></span>](#related-topics)

## <a name="verifying-the-success-of-constructors"></a><span data-ttu-id="5a78e-111">Verifica della riuscita dei costruttori</span><span class="sxs-lookup"><span data-stu-id="5a78e-111">Verifying the Success of Constructors</span></span>

<span data-ttu-id="5a78e-112">Molte classi GDI+ forniscono un metodo [**Image:: GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) che è possibile chiamare per determinare se i metodi richiamati in un oggetto hanno esito positivo.</span><span class="sxs-lookup"><span data-stu-id="5a78e-112">Many of the GDI+ classes provide a [**Image::GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) method that you can call to determine whether methods invoked on an object are successful.</span></span> <span data-ttu-id="5a78e-113">È anche possibile chiamare **Image:: GetLastStatus** per determinare se un costruttore ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="5a78e-113">You can also call **Image::GetLastStatus** to determine whether a constructor is successful.</span></span>

<span data-ttu-id="5a78e-114">Nell'esempio seguente viene illustrato come costruire un oggetto [**immagine**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e chiamare il metodo [**Image:: GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) per determinare se il costruttore è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="5a78e-114">The following example shows how to construct an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and call the [**Image::GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) method to determine whether the constructor was successful.</span></span> <span data-ttu-id="5a78e-115">I valori **OK** e **invalidparameter** sono elementi dell'enumerazione [**status**](/windows/desktop/api/Gdiplustypes/ne-gdiplustypes-status) .</span><span class="sxs-lookup"><span data-stu-id="5a78e-115">The values **Ok** and **InvalidParameter** are elements of the [**Status**](/windows/desktop/api/Gdiplustypes/ne-gdiplustypes-status) enumeration.</span></span>


```C++
Image myImage(L"Climber.jpg");
Status st = myImage.GetLastStatus();

if(Ok == st)
   // The constructor was successful. Use myImage.
else if(InvalidParameter == st)
   // The constructor failed because of an invalid parameter.
else
   // Compare st to other elements of the Status 
   // enumeration or do general error processing.
```



## <a name="allocating-buffers"></a><span data-ttu-id="5a78e-116">Allocazione di buffer</span><span class="sxs-lookup"><span data-stu-id="5a78e-116">Allocating Buffers</span></span>

<span data-ttu-id="5a78e-117">Diversi metodi GDI+ restituiscono dati numerici o di tipo carattere in un buffer allocato dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="5a78e-117">Several GDI+ methods return numeric or character data in a buffer that is allocated by the caller.</span></span> <span data-ttu-id="5a78e-118">Per ognuno di questi metodi è disponibile un metodo complementare che fornisce la dimensione del buffer richiesto.</span><span class="sxs-lookup"><span data-stu-id="5a78e-118">For each of those methods, there is a companion method that gives the size of the required buffer.</span></span> <span data-ttu-id="5a78e-119">Ad esempio, il metodo [**GraphicsPath:: GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) restituisce una matrice di oggetti [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) .</span><span class="sxs-lookup"><span data-stu-id="5a78e-119">For example, the [**GraphicsPath::GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) method returns an array of [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) objects.</span></span> <span data-ttu-id="5a78e-120">Prima di chiamare **GraphicsPath:: GetPathPoints**, è necessario allocare un buffer sufficientemente grande da mantenere tale matrice.</span><span class="sxs-lookup"><span data-stu-id="5a78e-120">Before you call **GraphicsPath::GetPathPoints**, you must allocate a buffer large enough to hold that array.</span></span> <span data-ttu-id="5a78e-121">È possibile determinare le dimensioni del buffer necessario chiamando il metodo [**GraphicsPath:: GetPointCount**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-getpointcount) di un oggetto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) .</span><span class="sxs-lookup"><span data-stu-id="5a78e-121">You can determine the size of the required buffer by calling the [**GraphicsPath::GetPointCount**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-getpointcount) method of a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object.</span></span>

<span data-ttu-id="5a78e-122">Nell'esempio seguente viene illustrato come determinare il numero di punti in un oggetto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) , allocare un buffer sufficientemente grande da poter essere utilizzato in molti punti e quindi chiamare [**GraphicsPath:: GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) per riempire il buffer.</span><span class="sxs-lookup"><span data-stu-id="5a78e-122">The following example shows how to determine the number of points in a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object, allocate a buffer large enough to hold that many points, and then call [**GraphicsPath::GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) to fill the buffer.</span></span> <span data-ttu-id="5a78e-123">Prima che il codice chiami **GraphicsPath:: GetPathPoints**, verifica che l'allocazione del buffer abbia avuto esito positivo assicurandosi che il puntatore del buffer non sia **null**.</span><span class="sxs-lookup"><span data-stu-id="5a78e-123">Before the code calls **GraphicsPath::GetPathPoints**, it verifies that the buffer allocation was successful by making sure that the buffer pointer is not **NULL**.</span></span>


```C++
GraphicsPath path;
path.AddEllipse(10, 10, 200, 100);

INT count = path.GetPointCount();          // get the size
Point* pointArray = new Point[count];      // allocate the buffer

if(pointArray)  // Check for successful allocation.
{
   path.GetPathPoints(pointArray, count);  // get the data
   ...                                     // use pointArray
   delete[] pointArray;                    // release the buffer
   pointArray = NULL;
}
```



<span data-ttu-id="5a78e-124">Nell'esempio precedente viene usato l'operatore New per allocare un buffer.</span><span class="sxs-lookup"><span data-stu-id="5a78e-124">The previous example uses the new operator to allocate a buffer.</span></span> <span data-ttu-id="5a78e-125">L'operatore New è stato utile perché il buffer è stato riempito con un numero noto di oggetti [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) .</span><span class="sxs-lookup"><span data-stu-id="5a78e-125">The new operator was convenient because the buffer was filled with a known number of [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) objects.</span></span> <span data-ttu-id="5a78e-126">In alcuni casi, GDI+ scrive più nel buffer rispetto a una matrice di oggetti GDI+.</span><span class="sxs-lookup"><span data-stu-id="5a78e-126">In some cases, GDI+ writes more into buffer than an array of GDI+ objects.</span></span> <span data-ttu-id="5a78e-127">A volte un buffer viene riempito con una matrice di oggetti GDI+ insieme a dati aggiuntivi a cui puntano i membri di tali oggetti.</span><span class="sxs-lookup"><span data-stu-id="5a78e-127">Sometimes a buffer is filled with an array of GDI+ objects along with additional data that is pointed to by members of those objects.</span></span> <span data-ttu-id="5a78e-128">Ad esempio, il metodo [**Image:: GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) restituisce una matrice di oggetti [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) , uno per ogni elemento di proprietà (porzione di metadati) archiviato nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="5a78e-128">For example, the [**Image::GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) method returns an array of [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) objects, one for each property item (piece of metadata) stored in the image.</span></span> <span data-ttu-id="5a78e-129">Tuttavia **Image:: GetAllPropertyItems** restituisce solo la matrice di oggetti **PropertyItem** ; aggiunge la matrice con dati aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="5a78e-129">But **Image::GetAllPropertyItems** returns more than just the array of **PropertyItem** objects; it appends the array with additional data.</span></span>

<span data-ttu-id="5a78e-130">Prima di chiamare [**Image:: GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems), è necessario allocare un buffer sufficientemente grande da ospitare la matrice di oggetti [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) insieme ai dati aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="5a78e-130">Before you call [**Image::GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems), you must allocate a buffer large enough to hold the array of [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) objects along with the additional data.</span></span> <span data-ttu-id="5a78e-131">È possibile chiamare il metodo [**Image:: GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) di un oggetto Image per determinare la dimensione totale del buffer richiesto.</span><span class="sxs-lookup"><span data-stu-id="5a78e-131">You can call the [**Image::GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) method of an Image object to determine the total size of the required buffer.</span></span>

<span data-ttu-id="5a78e-132">Nell'esempio seguente viene illustrato come creare un oggetto [**immagine**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e successivamente chiamare il metodo [**Image:: GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) di tale oggetto **Image** per recuperare tutti gli elementi di proprietà (metadati) archiviati nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="5a78e-132">The following example shows how to create an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and later call the [**Image::GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) method of that **Image** object to retrieve all the property items (metadata) stored in the image.</span></span> <span data-ttu-id="5a78e-133">Il codice alloca un buffer in base a un valore di dimensione restituito dal metodo [**Image:: GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) .</span><span class="sxs-lookup"><span data-stu-id="5a78e-133">The code allocates a buffer based on a size value returned by the [**Image::GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) method.</span></span> <span data-ttu-id="5a78e-134">**Image:: GetPropertySize** restituisce anche un valore Count che fornisce il numero di elementi della proprietà nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="5a78e-134">**Image::GetPropertySize** also returns a count value that gives the number of property items in the image.</span></span> <span data-ttu-id="5a78e-135">Si noti che il codice non calcola le dimensioni del buffer come `count*sizeof(PropertyItem)` .</span><span class="sxs-lookup"><span data-stu-id="5a78e-135">Notice that the code does not calculate the buffer size as `count*sizeof(PropertyItem)`.</span></span> <span data-ttu-id="5a78e-136">Un buffer calcolato in questo modo sarebbe troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="5a78e-136">A buffer calculated that way would be too small.</span></span>


```C++
UINT count = 0;
UINT size = 0;
Image myImage(L"FakePhoto.jpg");
myImage.GetPropertySize(&size, &count);

// GetAllPropertyItems returns an array of PropertyItem objects
// along with additional data. Allocate a buffer large enough to 
// receive the array and the additional data.
PropertyItem* propBuffer =(PropertyItem*)malloc(size);

if(propBuffer)
{
   myImage.GetAllPropertyItems(size, count, propBuffer);
   ...
   free(propBuffer);
   propBuffer = NULL;
}
```



## <a name="error-checking"></a><span data-ttu-id="5a78e-137">Controllo errori</span><span class="sxs-lookup"><span data-stu-id="5a78e-137">Error Checking</span></span>

<span data-ttu-id="5a78e-138">La maggior parte degli esempi di codice nella documentazione di GDI+ non Mostra il controllo degli errori.</span><span class="sxs-lookup"><span data-stu-id="5a78e-138">Most of the code examples in the GDI+ documentation do not show error checking.</span></span> <span data-ttu-id="5a78e-139">Il controllo completo degli errori rende un esempio di codice molto più lungo e può nascondere il punto illustrato nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="5a78e-139">Complete error checking makes a code example much longer and can obscure the point being illustrated by the example.</span></span> <span data-ttu-id="5a78e-140">Non è consigliabile incollare esempi dalla documentazione direttamente nel codice di produzione; è invece consigliabile migliorare gli esempi aggiungendo il controllo degli errori.</span><span class="sxs-lookup"><span data-stu-id="5a78e-140">You should not paste examples from the documentation directly into production code; rather, you should enhance the examples by adding your own error checking.</span></span>

<span data-ttu-id="5a78e-141">Nell'esempio seguente viene illustrato un modo per implementare il controllo degli errori con GDI+.</span><span class="sxs-lookup"><span data-stu-id="5a78e-141">The following example shows one way of implementing error checking with GDI+.</span></span> <span data-ttu-id="5a78e-142">Ogni volta che viene costruito un oggetto GDI+, il codice verifica se il costruttore ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="5a78e-142">Each time a GDI+ object is constructed, the code checks to see whether the constructor was successful.</span></span> <span data-ttu-id="5a78e-143">Questo controllo è particolarmente importante per il costruttore di [**Immagini**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , che si basa sulla lettura di un file.</span><span class="sxs-lookup"><span data-stu-id="5a78e-143">That check is especially important for the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) constructor, which relies on reading a file.</span></span> <span data-ttu-id="5a78e-144">Se tutti e quattro gli oggetti GDI+ ([**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath), **Image** e [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush)) vengono costruiti correttamente, il codice chiama i metodi su tali oggetti.</span><span class="sxs-lookup"><span data-stu-id="5a78e-144">If all four of the GDI+ objects ([**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath), **Image**, and [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush)) are constructed successfully, the code calls methods on those objects.</span></span> <span data-ttu-id="5a78e-145">Ogni chiamata al metodo viene verificata correttamente e, in caso di errore, le chiamate al metodo rimanenti vengono ignorate.</span><span class="sxs-lookup"><span data-stu-id="5a78e-145">Each method call is checked for success, and in the event of failure, the remaining method calls are skipped.</span></span>


```C++
Status GdipExample(HDC hdc)
{
   Status status = GenericError;
   INT count = 0;
   Point* points = NULL;

   Graphics graphics(hdc);
   status = graphics.GetLastStatus();
   if(Ok != status)
      return status;

   GraphicsPath path;
   status = path.GetLastStatus();
   if(Ok != status)
      return status;

   Image image(L"MyTexture.bmp");
   status = image.GetLastStatus();
   if(Ok != status)
      return status;

   TextureBrush brush(&image);
   status = brush.GetLastStatus();
   if(Ok != status)
      return status;

   status = path.AddEllipse(10, 10, 200, 100);

   if(Ok == status)
   {
      status = path.AddBezier(40, 130, 200, 130, 200, 200, 60, 200);
   }
  
   if(Ok == status)
   {
      count = path.GetPointCount();
      status = path.GetLastStatus();
   }

   if(Ok == status)
   {
      points = new Point[count];

      if(NULL == points)
         status = OutOfMemory;
   }

   if(Ok == status)
   {
      status = path.GetPathPoints(points, count);  
   }
  
   if(Ok == status)
   {
      status = graphics.FillPath(&brush, &path);
   }
   
   if(Ok == status)
   {
      for(int j = 0; j < count; ++j)
      {
         status = graphics.FillEllipse(
         &brush, points[j].X - 5, points[j].Y - 5, 10, 10);
      }
   }

   if(points)
   {
      delete[] points;
      points = NULL;
   }

   return status;
}
```



## <a name="thread-synchronization"></a><span data-ttu-id="5a78e-146">Sincronizzazione di thread</span><span class="sxs-lookup"><span data-stu-id="5a78e-146">Thread Synchronization</span></span>

<span data-ttu-id="5a78e-147">È possibile che più di un thread possa accedere a un singolo oggetto GDI+.</span><span class="sxs-lookup"><span data-stu-id="5a78e-147">It is possible for more than one thread to have access to a single GDI+ object.</span></span> <span data-ttu-id="5a78e-148">Tuttavia, GDI+ non fornisce alcun meccanismo di sincronizzazione automatica.</span><span class="sxs-lookup"><span data-stu-id="5a78e-148">However, GDI+ does not provide any automatic synchronization mechanism.</span></span> <span data-ttu-id="5a78e-149">Quindi, se due thread nell'applicazione hanno un puntatore allo stesso oggetto GDI+, è responsabilità dell'utente sincronizzare l'accesso a tale oggetto.</span><span class="sxs-lookup"><span data-stu-id="5a78e-149">So if two threads in your application have a pointer to the same GDI+ object, it is your responsibility to synchronize access to that object.</span></span>

<span data-ttu-id="5a78e-150">Alcuni metodi GDI+ restituiscono **ObjectBusy** se un thread tenta di chiamare un metodo mentre un altro thread esegue un metodo sullo stesso oggetto.</span><span class="sxs-lookup"><span data-stu-id="5a78e-150">Some GDI+ methods return **ObjectBusy** if a thread attempts to call a method while another thread is executing a method on the same object.</span></span> <span data-ttu-id="5a78e-151">Non tentare di sincronizzare l'accesso a un oggetto in base al valore restituito di **ObjectBusy** .</span><span class="sxs-lookup"><span data-stu-id="5a78e-151">Do not try to synchronize access to an object based on the **ObjectBusy** return value.</span></span> <span data-ttu-id="5a78e-152">Al contrario, ogni volta che si accede a un membro o si chiama un metodo dell'oggetto, inserire la chiamata all'interno di una sezione critica o utilizzare un'altra tecnica di sincronizzazione standard.</span><span class="sxs-lookup"><span data-stu-id="5a78e-152">Instead, each time you access a member or call a method of the object, place the call inside a critical section, or use some other standard synchronization technique.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a78e-153">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5a78e-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a78e-154">centro per sviluppatori sulla sicurezza MSDN</span><span class="sxs-lookup"><span data-stu-id="5a78e-154">MSDN Security Developer Center</span></span>](https://msdn.microsoft.com/security/)
</dt> <dt>

<span data-ttu-id="5a78e-155">[Risorse How-To sicurezza](/previous-versions/msp-n-p/ff650055(v=pandp.10))</span><span class="sxs-lookup"><span data-stu-id="5a78e-155">[Security How-To Resources](/previous-versions/msp-n-p/ff650055(v=pandp.10))</span></span>
</dt> <dt>

[<span data-ttu-id="5a78e-156">Centro sicurezza TechNet</span><span class="sxs-lookup"><span data-stu-id="5a78e-156">TechNet Security Center</span></span>](https://technet.microsoft.com/security/)
</dt> </dl>

 

 

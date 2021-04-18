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
# <a name="security-considerations-gdi"></a>Considerazioni sulla sicurezza: GDI+

In questo argomento vengono fornite informazioni sulle considerazioni sulla sicurezza correlate alla programmazione con Windows GDI+. Questo argomento non fornisce tutte le informazioni necessarie per i problemi di sicurezza, ma è possibile usarlo come punto di partenza e riferimento per questa area tecnologica.

-   [Verifica della riuscita dei costruttori](#verifying-the-success-of-constructors)
-   [Allocazione di buffer](#allocating-buffers)
-   [Controllo errori](#error-checking)
-   [Sincronizzazione di thread](#thread-synchronization)
-   [Argomenti correlati](#related-topics)

## <a name="verifying-the-success-of-constructors"></a>Verifica della riuscita dei costruttori

Molte classi GDI+ forniscono un metodo [**Image:: GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) che è possibile chiamare per determinare se i metodi richiamati in un oggetto hanno esito positivo. È anche possibile chiamare **Image:: GetLastStatus** per determinare se un costruttore ha esito positivo.

Nell'esempio seguente viene illustrato come costruire un oggetto [**immagine**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e chiamare il metodo [**Image:: GetLastStatus**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getlaststatus) per determinare se il costruttore è stato eseguito correttamente. I valori **OK** e **invalidparameter** sono elementi dell'enumerazione [**status**](/windows/desktop/api/Gdiplustypes/ne-gdiplustypes-status) .


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



## <a name="allocating-buffers"></a>Allocazione di buffer

Diversi metodi GDI+ restituiscono dati numerici o di tipo carattere in un buffer allocato dal chiamante. Per ognuno di questi metodi è disponibile un metodo complementare che fornisce la dimensione del buffer richiesto. Ad esempio, il metodo [**GraphicsPath:: GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) restituisce una matrice di oggetti [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) . Prima di chiamare **GraphicsPath:: GetPathPoints**, è necessario allocare un buffer sufficientemente grande da mantenere tale matrice. È possibile determinare le dimensioni del buffer necessario chiamando il metodo [**GraphicsPath:: GetPointCount**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-getpointcount) di un oggetto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) .

Nell'esempio seguente viene illustrato come determinare il numero di punti in un oggetto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) , allocare un buffer sufficientemente grande da poter essere utilizzato in molti punti e quindi chiamare [**GraphicsPath:: GetPathPoints**](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)) per riempire il buffer. Prima che il codice chiami **GraphicsPath:: GetPathPoints**, verifica che l'allocazione del buffer abbia avuto esito positivo assicurandosi che il puntatore del buffer non sia **null**.


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



Nell'esempio precedente viene usato l'operatore New per allocare un buffer. L'operatore New è stato utile perché il buffer è stato riempito con un numero noto di oggetti [**Point**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) . In alcuni casi, GDI+ scrive più nel buffer rispetto a una matrice di oggetti GDI+. A volte un buffer viene riempito con una matrice di oggetti GDI+ insieme a dati aggiuntivi a cui puntano i membri di tali oggetti. Ad esempio, il metodo [**Image:: GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) restituisce una matrice di oggetti [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) , uno per ogni elemento di proprietà (porzione di metadati) archiviato nell'immagine. Tuttavia **Image:: GetAllPropertyItems** restituisce solo la matrice di oggetti **PropertyItem** ; aggiunge la matrice con dati aggiuntivi.

Prima di chiamare [**Image:: GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems), è necessario allocare un buffer sufficientemente grande da ospitare la matrice di oggetti [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) insieme ai dati aggiuntivi. È possibile chiamare il metodo [**Image:: GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) di un oggetto Image per determinare la dimensione totale del buffer richiesto.

Nell'esempio seguente viene illustrato come creare un oggetto [**immagine**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e successivamente chiamare il metodo [**Image:: GetAllPropertyItems**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getallpropertyitems) di tale oggetto **Image** per recuperare tutti gli elementi di proprietà (metadati) archiviati nell'immagine. Il codice alloca un buffer in base a un valore di dimensione restituito dal metodo [**Image:: GetPropertySize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertysize) . **Image:: GetPropertySize** restituisce anche un valore Count che fornisce il numero di elementi della proprietà nell'immagine. Si noti che il codice non calcola le dimensioni del buffer come `count*sizeof(PropertyItem)` . Un buffer calcolato in questo modo sarebbe troppo piccolo.


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



## <a name="error-checking"></a>Controllo errori

La maggior parte degli esempi di codice nella documentazione di GDI+ non Mostra il controllo degli errori. Il controllo completo degli errori rende un esempio di codice molto più lungo e può nascondere il punto illustrato nell'esempio. Non è consigliabile incollare esempi dalla documentazione direttamente nel codice di produzione; è invece consigliabile migliorare gli esempi aggiungendo il controllo degli errori.

Nell'esempio seguente viene illustrato un modo per implementare il controllo degli errori con GDI+. Ogni volta che viene costruito un oggetto GDI+, il codice verifica se il costruttore ha avuto esito positivo. Questo controllo è particolarmente importante per il costruttore di [**Immagini**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , che si basa sulla lettura di un file. Se tutti e quattro gli oggetti GDI+ ([**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics), [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath), **Image** e [**TextureBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush)) vengono costruiti correttamente, il codice chiama i metodi su tali oggetti. Ogni chiamata al metodo viene verificata correttamente e, in caso di errore, le chiamate al metodo rimanenti vengono ignorate.


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



## <a name="thread-synchronization"></a>Sincronizzazione di thread

È possibile che più di un thread possa accedere a un singolo oggetto GDI+. Tuttavia, GDI+ non fornisce alcun meccanismo di sincronizzazione automatica. Quindi, se due thread nell'applicazione hanno un puntatore allo stesso oggetto GDI+, è responsabilità dell'utente sincronizzare l'accesso a tale oggetto.

Alcuni metodi GDI+ restituiscono **ObjectBusy** se un thread tenta di chiamare un metodo mentre un altro thread esegue un metodo sullo stesso oggetto. Non tentare di sincronizzare l'accesso a un oggetto in base al valore restituito di **ObjectBusy** . Al contrario, ogni volta che si accede a un membro o si chiama un metodo dell'oggetto, inserire la chiamata all'interno di una sezione critica o utilizzare un'altra tecnica di sincronizzazione standard.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[centro per sviluppatori sulla sicurezza MSDN](https://msdn.microsoft.com/security/)
</dt> <dt>

[Risorse How-To sicurezza](/previous-versions/msp-n-p/ff650055(v=pandp.10))
</dt> <dt>

[Centro sicurezza TechNet](https://technet.microsoft.com/security/)
</dt> </dl>

 

 

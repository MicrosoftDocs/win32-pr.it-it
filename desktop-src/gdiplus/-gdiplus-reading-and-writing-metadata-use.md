---
description: Alcuni file di immagine contengono metadati che è possibile leggere per determinare le funzionalità dell'immagine.
ms.assetid: 2febea35-3fea-4a2d-baaf-7a4f935fc81f
title: Lettura e scrittura di metadati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2f599c1134efc8768d0b6ed59deaae8adf9f6f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751314"
---
# <a name="reading-and-writing-metadata"></a>Lettura e scrittura di metadati

Alcuni file di immagine contengono metadati che è possibile leggere per determinare le funzionalità dell'immagine. Ad esempio, una fotografia digitale potrebbe contenere metadati che è possibile leggere per determinare la marca e il modello della fotocamera usata per acquisire l'immagine. Con Windows GDI+ è possibile leggere i metadati esistenti ed è anche possibile scrivere nuovi metadati nei file di immagine.

GDI+ fornisce un modo uniforme per archiviare e recuperare i metadati dai file di immagine in vari formati. In GDI+, un frammento di metadati viene chiamato *elemento proprietà*. È possibile archiviare e recuperare i metadati chiamando i metodi **SetPropertyItem** e **GetPropertyItem** della classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e non è necessario preoccuparsi dei dettagli del modo in cui un particolare formato di file archivia tali metadati.

GDI+ supporta attualmente i metadati per i formati di file TIFF, JPEG, EXIF e PNG. Il formato EXIF, che specifica come archiviare le immagini acquisite dalle fotocamere digitali ancora, si basa sui formati TIFF e JPEG. EXIF usa il formato TIFF per i dati pixel non compressi e il formato JPEG per i dati pixel compressi.

GDI+ definisce un set di tag di proprietà che identificano gli elementi di proprietà. Alcuni tag sono di uso generale; ovvero sono supportati da tutti i formati di file indicati nel paragrafo precedente. Gli altri tag sono specifici per scopi specifici e si applicano solo a determinati formati. Se si tenta di salvare un elemento di proprietà in un file che non supporta tale elemento della proprietà, GDI+ ignora la richiesta. In particolare, il metodo [**Image:: SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) restituisce PropertyNotSupported.

È possibile determinare gli elementi delle proprietà archiviati in un file di immagine chiamando [**Image:: GetPropertyIdList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyidlist). Se si tenta di recuperare un elemento della proprietà che non è presente nel file, GDI+ ignora la richiesta. In particolare, il metodo [**Image:: GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) restituisce PropertyNotFound.

## <a name="reading-metadata-from-a-file"></a>Lettura dei metadati da un file

La seguente applicazione console chiama il metodo **GetPropertySize** di un oggetto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) per determinare il numero di parti di metadati presenti nel file FakePhoto.jpg.


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;
INT main()
{
   // Initialize <tla rid="tla_gdiplus"/>.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);
   UINT    size = 0;
   UINT    count = 0;
   Bitmap* bitmap = new Bitmap(L"FakePhoto.jpg");
   bitmap->GetPropertySize(&size, &count);
   printf("There are %d pieces of metadata in the file.\n", count);
   printf("The total size of the metadata is %d bytes.\n", size);
 
   delete bitmap;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



Il codice precedente, insieme a un determinato file FakePhoto.jpg, ha prodotto l'output seguente:


```
There are 7 pieces of metadata in the file.
The total size of the metadata is 436 bytes.
```



In GDI+ viene archiviato un singolo elemento di metadati in un oggetto [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) . È possibile chiamare il metodo **GetAllPropertyItems** della classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) per recuperare tutti i metadati da un file. Il metodo **GetAllPropertyItems** restituisce una matrice di oggetti **PropertyItem** . Prima di chiamare **GetAllPropertyItems**, è necessario allocare un buffer sufficientemente grande da ricevere tale matrice. È possibile chiamare il metodo **GetPropertySize** della classe **Image** per ottenere la dimensione (in byte) del buffer richiesto.

Un oggetto [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) dispone dei quattro membri pubblici seguenti:



|            |                                                                                                                                                                                                                                                                                                        |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **id**     | Tag che identifica l'elemento dei metadati. I valori che possono essere assegnati all' **ID** (PropertyTagImageTitle, PropertyTagEquipMake, PropertyTagExifExposureTime e like) sono definiti in Gdiplusimaging. h.                                                                                           |
| **length** | Lunghezza, in byte, della matrice di valori a cui punta il membro dati del **valore** . Si noti che se il membro dati **Type** è impostato su PropertyTagTypeASCII, il membro dati length è la **lunghezza** di una stringa di caratteri con terminazione null, incluso il terminatore null.                        |
| **type**   | Tipo di dati dei valori nella matrice a cui punta il membro dati value. Le costanti (PropertyTagTypeByte, PropertyTagTypeASCII e like) che rappresentano vari tipi di dati sono descritte in [**costanti di tipo di tag della proprietà Image**](-gdiplus-constant-image-property-tag-type-constants.md). |
| **value**  | Puntatore a una matrice di valori.                                                                                                                                                                                                                                                                       |



 

La seguente applicazione console legge e visualizza le sette parti di metadati nel file FakePhoto.jpg. La funzione Main si basa sulla funzione helper PropertyTypeFromWORD, che viene mostrata dopo la funzione Main.


```
#include <windows.h>
#include <gdiplus.h>
#include <strsafe.h>
using namespace Gdiplus;

INT main()
{
   // Initialize GDI+
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   UINT  size = 0;
   UINT  count = 0;

   #define MAX_PROPTYPE_SIZE 30
   WCHAR strPropertyType[MAX_PROPTYPE_SIZE] = L"";

   Bitmap* bitmap = new Bitmap(L"FakePhoto.jpg");

   bitmap->GetPropertySize(&size, &count);
   printf("There are %d pieces of metadata in the file.\n\n", count);

   // GetAllPropertyItems returns an array of PropertyItem objects.
   // Allocate a buffer large enough to receive that array.
   PropertyItem* pPropBuffer =(PropertyItem*)malloc(size);

   // Get the array of PropertyItem objects.
   bitmap->GetAllPropertyItems(size, count, pPropBuffer);

   // For each PropertyItem in the array, display the id, type, and length.
   for(UINT j = 0; j < count; ++j)
   {
      // Convert the property type from a WORD to a string.
      PropertyTypeFromWORD(
         pPropBuffer[j].type, strPropertyType, MAX_PROPTYPE_SIZE);

      printf("Property Item %d\n", j);
      printf("  id: 0x%x\n", pPropBuffer[j].id);
      wprintf(L"  type: %s\n", strPropertyType);
      printf("  length: %d bytes\n\n", pPropBuffer[j].length);
   }

   free(pPropBuffer);
   delete bitmap;
   GdiplusShutdown(gdiplusToken);
   return 0;
} // main

// Helper function
HRESULT PropertyTypeFromWORD(WORD index, WCHAR* string, UINT maxChars)
{
   HRESULT hr = E_FAIL;

   WCHAR* propertyTypes[] = {
      L"Nothing",                   // 0
      L"PropertyTagTypeByte",       // 1
      L"PropertyTagTypeASCII",      // 2
      L"PropertyTagTypeShort",      // 3
      L"PropertyTagTypeLong",       // 4
      L"PropertyTagTypeRational",   // 5
      L"Nothing",                   // 6
      L"PropertyTagTypeUndefined",  // 7
      L"Nothing",                   // 8
      L"PropertyTagTypeSLONG",      // 9
      L"PropertyTagTypeSRational"}; // 10

   hr = StringCchCopyW(string, maxChars, propertyTypes[index]);
   return hr;
}
```



L'applicazione console precedente produce l'output seguente:


```
Property Item 0
  id: 0x320
  type: PropertyTagTypeASCII
  length: 16 bytes
Property Item 1
  id: 0x10f
  type: PropertyTagTypeASCII
  length: 17 bytes
Property Item 2
  id: 0x110
  type: PropertyTagTypeASCII
  length: 7 bytes
Property Item 3
  id: 0x9003
  type: PropertyTagTypeASCII
  length: 20 bytes
Property Item 4
  id: 0x829a
  type: PropertyTagTypeRational
  length: 8 bytes
Property Item 5
  id: 0x5090
  type: PropertyTagTypeShort
  length: 128 bytes
Property Item 6
  id: 0x5091
  type: PropertyTagTypeShort
  length: 128 bytes
```



L'output precedente mostra un numero ID esadecimale per ogni elemento di proprietà. È possibile cercare i numeri ID nelle [costanti dei tag delle proprietà dell'immagine](-gdiplus-constant-image-property-tag-constants.md) e scoprire che rappresentano i tag di proprietà seguenti.



| Valore esadecimale                                                                                                       | Tag proprietà                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x010F 0x0320<br/>  0x0110<br/>  0x9003<br/>  0x829a<br/>  0x5090<br/>  0x5091<br/> | PropertyTagImageTitle PropertyTagEquipMake<br/>  PropertyTagEquipModel<br/>  PropertyTagExifDTOriginal<br/>  PropertyTagExifExposureTime<br/>  PropertyTagLuminanceTable<br/>  PropertyTagChrominanceTable<br/> |



 

Il secondo elemento della proprietà (indice 1) nell'elenco contiene l' **ID** PropertyTagEquipMake e il **tipo** PropertyTagTypeASCII. Nell'esempio seguente, che è una continuazione dell'applicazione console precedente, viene visualizzato il valore di tale elemento della proprietà:


```
printf("The equipment make is %s.\n", pPropBuffer[1].value);
```



La riga di codice precedente produce l'output seguente:


```
The equipment make is Northwind Traders.
```



Il quinto elemento della proprietà (indice 4) nell'elenco contiene l' **ID** PropertyTagExifExposureTime e il **tipo** PropertyTagTypeRational. Il tipo di dati (PropertyTagTypeRational) è una coppia di **Long** s. Nell'esempio seguente, che è una continuazione dell'applicazione console precedente, Visualizza i due valori **Long** come frazione. Tale frazione, 1/125, è il tempo di esposizione espresso in secondi.


```
long* ptrLong = (long*)(pPropBuffer[4].value);
printf("The exposure time is %d/%d.\n", ptrLong[0], ptrLong[1]);
```



L'output del codice precedente è il seguente:


```
The exposure time is 1/125.
```



## <a name="writing-metadata-to-a-file"></a>Scrittura di metadati in un file

Per scrivere un elemento di metadati in un oggetto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) , inizializzare un oggetto [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) e quindi passare l'indirizzo dell'oggetto **PropertyItem** al metodo **SetPropertyItem** dell'oggetto **Image** .

La seguente applicazione console scrive un elemento, ovvero il titolo dell'immagine, dei metadati in un oggetto [**immagine**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e quindi Salva l'immagine nel file su disco FakePhoto2.jpg. La funzione Main si basa sulla funzione helper GetEncoderClsid, illustrata nell'argomento [recupero dell'identificatore di classe per un codificatore](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;
INT main()
{
   // Initialize <tla rid="tla_gdiplus"/>.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);
   Status stat;
   CLSID  clsid;
   char   propertyValue[] = "Fake Photograph";
   Bitmap* bitmap = new Bitmap(L"FakePhoto.jpg");
   PropertyItem* propertyItem = new PropertyItem;
   // Get the CLSID of the JPEG encoder.
   GetEncoderClsid(L"image/jpeg", &clsid);
   propertyItem->id = PropertyTagImageTitle;
   propertyItem->length = 16;  // string length including NULL terminator
   propertyItem->type = PropertyTagTypeASCII; 
   propertyItem->value = propertyValue;
   bitmap->SetPropertyItem(propertyItem);
   stat = bitmap->Save(L"FakePhoto2.jpg", &clsid, NULL);
   if(stat == Ok)
      printf("FakePhoto2.jpg saved successfully.\n");
   
   delete propertyItem;
   delete bitmap;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



 

 

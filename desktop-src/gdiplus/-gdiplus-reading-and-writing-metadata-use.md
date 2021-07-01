---
description: Alcuni file di immagine contengono metadati che è possibile leggere per determinare le caratteristiche dell'immagine.
ms.assetid: 2febea35-3fea-4a2d-baaf-7a4f935fc81f
title: Lettura e scrittura di metadati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e4ea0a8f389f31870b31a0b15480815bdd7cf1f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118296"
---
# <a name="reading-and-writing-metadata"></a><span data-ttu-id="bc821-103">Lettura e scrittura di metadati</span><span class="sxs-lookup"><span data-stu-id="bc821-103">Reading and Writing Metadata</span></span>

<span data-ttu-id="bc821-104">Alcuni file di immagine contengono metadati che è possibile leggere per determinare le caratteristiche dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="bc821-104">Some image files contain metadata that you can read to determine features of the image.</span></span> <span data-ttu-id="bc821-105">Ad esempio, una fotografia digitale potrebbe contenere metadati che è possibile leggere per determinare la make e il modello della fotocamera usata per acquisire l'immagine.</span><span class="sxs-lookup"><span data-stu-id="bc821-105">For example, a digital photograph might contain metadata that you can read to determine the make and model of the camera used to capture the image.</span></span> <span data-ttu-id="bc821-106">Con GDI+ di Windows è possibile leggere i metadati esistenti ed è anche possibile scrivere nuovi metadati nei file di immagine.</span><span class="sxs-lookup"><span data-stu-id="bc821-106">With Windows GDI+, you can read existing metadata, and you can also write new metadata to image files.</span></span>

<span data-ttu-id="bc821-107">GDI+ offre un modo uniforme per archiviare e recuperare metadati dai file di immagine in vari formati.</span><span class="sxs-lookup"><span data-stu-id="bc821-107">GDI+ provides a uniform way of storing and retrieving metadata from image files in various formats.</span></span> <span data-ttu-id="bc821-108">In GDI+, una parte di metadati è denominata elemento *di proprietà*.</span><span class="sxs-lookup"><span data-stu-id="bc821-108">In GDI+, a piece of metadata is called a *property item*.</span></span> <span data-ttu-id="bc821-109">È possibile archiviare e recuperare metadati chiamando i metodi **SetPropertyItem** e **GetPropertyItem** della classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e non è necessario preoccuparsi dei dettagli del modo in cui un particolare formato di file archivia i metadati.</span><span class="sxs-lookup"><span data-stu-id="bc821-109">You can store and retrieve metadata by calling the **SetPropertyItem** and **GetPropertyItem** methods of the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class, and you don't have to be concerned about the details of how a particular file format stores that metadata.</span></span>

<span data-ttu-id="bc821-110">GDI+ supporta attualmente i metadati per i formati di file TIFF, JPEG, Exif e PNG.</span><span class="sxs-lookup"><span data-stu-id="bc821-110">GDI+ currently supports metadata for the TIFF, JPEG, Exif, and PNG file formats.</span></span> <span data-ttu-id="bc821-111">Il formato Exif, che specifica come archiviare le immagini acquisite da fotocamere digitali, è basato sui formati TIFF e JPEG.</span><span class="sxs-lookup"><span data-stu-id="bc821-111">The Exif format, which specifies how to store images captured by digital still cameras, is built on top of the TIFF and JPEG formats.</span></span> <span data-ttu-id="bc821-112">Exif usa il formato TIFF per i dati pixel non compressi e il formato JPEG per i dati pixel compressi.</span><span class="sxs-lookup"><span data-stu-id="bc821-112">Exif uses the TIFF format for uncompressed pixel data and the JPEG format for compressed pixel data.</span></span>

<span data-ttu-id="bc821-113">GDI+ definisce un set di tag di proprietà che identificano gli elementi delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="bc821-113">GDI+ defines a set of property tags that identify property items.</span></span> <span data-ttu-id="bc821-114">Alcuni tag sono per utilizzo generico. sono supportati da tutti i formati di file indicati nel paragrafo precedente.</span><span class="sxs-lookup"><span data-stu-id="bc821-114">Certain tags are general-purpose; that is, they are supported by all of the file formats mentioned in the preceding paragraph.</span></span> <span data-ttu-id="bc821-115">Altri tag sono a scopo speciale e si applicano solo a determinati formati.</span><span class="sxs-lookup"><span data-stu-id="bc821-115">Other tags are special-purpose and apply only to certain formats.</span></span> <span data-ttu-id="bc821-116">Se si tenta di salvare un elemento proprietà in un file che non supporta tale elemento proprietà, GDI+ ignora la richiesta.</span><span class="sxs-lookup"><span data-stu-id="bc821-116">If you try to save a property item to a file that does not support that property item, GDI+ ignores the request.</span></span> <span data-ttu-id="bc821-117">In particolare, il [**metodo Image::SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) restituisce PropertyNotSupported.</span><span class="sxs-lookup"><span data-stu-id="bc821-117">More specifically, the [**Image::SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) method returns PropertyNotSupported.</span></span>

<span data-ttu-id="bc821-118">È possibile determinare gli elementi delle proprietà archiviati in un file di immagine chiamando [**Image::GetPropertyIdList.**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyidlist)</span><span class="sxs-lookup"><span data-stu-id="bc821-118">You can determine the property items that are stored in an image file by calling [**Image::GetPropertyIdList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyidlist).</span></span> <span data-ttu-id="bc821-119">Se si tenta di recuperare un elemento di proprietà che non si trova nel file, GDI+ ignora la richiesta.</span><span class="sxs-lookup"><span data-stu-id="bc821-119">If you try to retrieve a property item that is not in the file, GDI+ ignores the request.</span></span> <span data-ttu-id="bc821-120">In particolare, il [**metodo Image::GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) restituisce PropertyNotFound.</span><span class="sxs-lookup"><span data-stu-id="bc821-120">More specifically, the [**Image::GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) method returns PropertyNotFound.</span></span>

## <a name="reading-metadata-from-a-file"></a><span data-ttu-id="bc821-121">Lettura di metadati da un file</span><span class="sxs-lookup"><span data-stu-id="bc821-121">Reading Metadata from a File</span></span>

<span data-ttu-id="bc821-122">L'applicazione console seguente chiama **il metodo GetPropertySize** di un oggetto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) per determinare il numero di metadati presenti nel file FakePhoto.jpg.</span><span class="sxs-lookup"><span data-stu-id="bc821-122">The following console application calls the **GetPropertySize** method of an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object to determine how many pieces of metadata are in the file FakePhoto.jpg.</span></span>


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



<span data-ttu-id="bc821-123">Il codice precedente, insieme a un particolare file, FakePhoto.jpg, ha prodotto l'output seguente:</span><span class="sxs-lookup"><span data-stu-id="bc821-123">The preceding code, along with a particular file, FakePhoto.jpg, produced the following output:</span></span>


```
There are 7 pieces of metadata in the file.
The total size of the metadata is 436 bytes.
```



<span data-ttu-id="bc821-124">GDI+ archivia una singola parte di metadati in un [**oggetto PropertyItem.**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem)</span><span class="sxs-lookup"><span data-stu-id="bc821-124">GDI+ stores an individual piece of metadata in a [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) object.</span></span> <span data-ttu-id="bc821-125">È possibile chiamare il **metodo GetAllPropertyItems** della [**classe Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) per recuperare tutti i metadati da un file.</span><span class="sxs-lookup"><span data-stu-id="bc821-125">You can call the **GetAllPropertyItems** method of the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class to retrieve all the metadata from a file.</span></span> <span data-ttu-id="bc821-126">Il **metodo GetAllPropertyItems** restituisce una matrice di **oggetti PropertyItem.**</span><span class="sxs-lookup"><span data-stu-id="bc821-126">The **GetAllPropertyItems** method returns an array of **PropertyItem** objects.</span></span> <span data-ttu-id="bc821-127">Prima di chiamare **GetAllPropertyItems,** è necessario allocare un buffer sufficientemente grande per ricevere tale matrice.</span><span class="sxs-lookup"><span data-stu-id="bc821-127">Before you call **GetAllPropertyItems**, you must allocate a buffer large enough to receive that array.</span></span> <span data-ttu-id="bc821-128">È possibile chiamare il **metodo GetPropertySize** della **classe Image** per ottenere le dimensioni (in byte) del buffer richiesto.</span><span class="sxs-lookup"><span data-stu-id="bc821-128">You can call the **GetPropertySize** method of the **Image** class to get the size (in bytes) of the required buffer.</span></span>

<span data-ttu-id="bc821-129">Un [**oggetto PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) ha i quattro membri pubblici seguenti:</span><span class="sxs-lookup"><span data-stu-id="bc821-129">A [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) object has the following four public members:</span></span>



|            | <span data-ttu-id="bc821-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc821-130">Description</span></span>                                                                                                                                                                                                                                                                                                       |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc821-131">**id**</span><span class="sxs-lookup"><span data-stu-id="bc821-131">**id**</span></span>     | <span data-ttu-id="bc821-132">Tag che identifica l'elemento di metadati.</span><span class="sxs-lookup"><span data-stu-id="bc821-132">A tag that identifies the metadata item.</span></span> <span data-ttu-id="bc821-133">I valori che possono essere assegnati a **id** (PropertyTagImageTitle, PropertyTagEquipMake, PropertyTagExifExposureTime e simili) sono definiti in Gdiplusimaging.h.</span><span class="sxs-lookup"><span data-stu-id="bc821-133">The values that can be assigned to **id** (PropertyTagImageTitle, PropertyTagEquipMake, PropertyTagExifExposureTime, and the like) are defined in Gdiplusimaging.h.</span></span>                                                                                           |
| <span data-ttu-id="bc821-134">**length**</span><span class="sxs-lookup"><span data-stu-id="bc821-134">**length**</span></span> | <span data-ttu-id="bc821-135">Lunghezza, in byte, della matrice di valori a cui punta il membro **dati** value.</span><span class="sxs-lookup"><span data-stu-id="bc821-135">The length, in bytes, of the array of values pointed to by the **value** data member.</span></span> <span data-ttu-id="bc821-136">Si noti  che se il membro dati type è impostato su PropertyTagTypeASCII, il membro dati length è la lunghezza di una stringa di caratteri con terminazione Null, incluso il carattere di terminazione NULL. </span><span class="sxs-lookup"><span data-stu-id="bc821-136">Note that if the **type** data member is set to PropertyTagTypeASCII, then the length data member is the **length** of a null-terminated character string, including the NULL terminator.</span></span>                        |
| <span data-ttu-id="bc821-137">**type**</span><span class="sxs-lookup"><span data-stu-id="bc821-137">**type**</span></span>   | <span data-ttu-id="bc821-138">Tipo di dati dei valori nella matrice a cui punta il membro dati value.</span><span class="sxs-lookup"><span data-stu-id="bc821-138">The data type of the values in the array pointed to by the value data member.</span></span> <span data-ttu-id="bc821-139">Le costanti (PropertyTagTypeByte, PropertyTagTypeASCII e simili) che rappresentano vari tipi di dati sono descritte in Costanti del tipo di tag delle proprietà [**dell'immagine.**](-gdiplus-constant-image-property-tag-type-constants.md)</span><span class="sxs-lookup"><span data-stu-id="bc821-139">Constants (PropertyTagTypeByte, PropertyTagTypeASCII, and the like) that represent various data types are described in [**Image Property Tag Type Constants**](-gdiplus-constant-image-property-tag-type-constants.md).</span></span> |
| <span data-ttu-id="bc821-140">**value**</span><span class="sxs-lookup"><span data-stu-id="bc821-140">**value**</span></span>  | <span data-ttu-id="bc821-141">Puntatore a una matrice di valori.</span><span class="sxs-lookup"><span data-stu-id="bc821-141">A pointer to an array of values.</span></span>                                                                                                                                                                                                                                                                       |



 

<span data-ttu-id="bc821-142">L'applicazione console seguente legge e visualizza i sette metadati nel file FakePhoto.jpg.</span><span class="sxs-lookup"><span data-stu-id="bc821-142">The following console application reads and displays the seven pieces of metadata in the file FakePhoto.jpg.</span></span> <span data-ttu-id="bc821-143">La funzione main si basa sulla funzione helper PropertyTypeFromWORD, illustrata dopo la funzione main.</span><span class="sxs-lookup"><span data-stu-id="bc821-143">The main function relies on the helper function PropertyTypeFromWORD, which is shown following the main function.</span></span>


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



<span data-ttu-id="bc821-144">L'applicazione console precedente produce l'output seguente:</span><span class="sxs-lookup"><span data-stu-id="bc821-144">The preceding console application produces the following output:</span></span>


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



<span data-ttu-id="bc821-145">L'output precedente mostra un numero ID esadecimale per ogni elemento di proprietà.</span><span class="sxs-lookup"><span data-stu-id="bc821-145">The preceding output shows a hexadecimal ID number for each property item.</span></span> <span data-ttu-id="bc821-146">È possibile cercare i numeri ID in [Costanti tag](-gdiplus-constant-image-property-tag-constants.md) proprietà immagine e scoprire che rappresentano i tag di proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="bc821-146">You can look up those ID numbers in [Image Property Tag Constants](-gdiplus-constant-image-property-tag-constants.md) and find out that they represent the following property tags.</span></span>



| <span data-ttu-id="bc821-147">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="bc821-147">Hexadecimal value</span></span>                                                                                                       | <span data-ttu-id="bc821-148">Tag di proprietà</span><span class="sxs-lookup"><span data-stu-id="bc821-148">Property tag</span></span>                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc821-149">0x0320 0x010f</span><span class="sxs-lookup"><span data-stu-id="bc821-149">0x0320 0x010f</span></span><br/>  <span data-ttu-id="bc821-150">0x0110</span><span class="sxs-lookup"><span data-stu-id="bc821-150">0x0110</span></span><br/>  <span data-ttu-id="bc821-151">0x9003</span><span class="sxs-lookup"><span data-stu-id="bc821-151">0x9003</span></span><br/>  <span data-ttu-id="bc821-152">0x829a</span><span class="sxs-lookup"><span data-stu-id="bc821-152">0x829a</span></span><br/>  <span data-ttu-id="bc821-153">0x5090</span><span class="sxs-lookup"><span data-stu-id="bc821-153">0x5090</span></span><br/>  <span data-ttu-id="bc821-154">0x5091</span><span class="sxs-lookup"><span data-stu-id="bc821-154">0x5091</span></span><br/> | <span data-ttu-id="bc821-155">PropertyTagImageTitle PropertyTagEquipMake</span><span class="sxs-lookup"><span data-stu-id="bc821-155">PropertyTagImageTitle PropertyTagEquipMake</span></span><br/>  <span data-ttu-id="bc821-156">PropertyTagEquipModel</span><span class="sxs-lookup"><span data-stu-id="bc821-156">PropertyTagEquipModel</span></span><br/>  <span data-ttu-id="bc821-157">PropertyTagExifDTOriginal</span><span class="sxs-lookup"><span data-stu-id="bc821-157">PropertyTagExifDTOriginal</span></span><br/>  <span data-ttu-id="bc821-158">PropertyTagExifExposureTime</span><span class="sxs-lookup"><span data-stu-id="bc821-158">PropertyTagExifExposureTime</span></span><br/>  <span data-ttu-id="bc821-159">PropertyTagLuminanceTable</span><span class="sxs-lookup"><span data-stu-id="bc821-159">PropertyTagLuminanceTable</span></span><br/>  <span data-ttu-id="bc821-160">PropertyTagChrominanceTable</span><span class="sxs-lookup"><span data-stu-id="bc821-160">PropertyTagChrominanceTable</span></span><br/> |



 

<span data-ttu-id="bc821-161">Il secondo elemento della proprietà (indice 1) nell'elenco ha **ID** PropertyTagEquipMake e **tipo** PropertyTagTypeASCII.</span><span class="sxs-lookup"><span data-stu-id="bc821-161">The second (index 1) property item in the list has **id** PropertyTagEquipMake and **type** PropertyTagTypeASCII.</span></span> <span data-ttu-id="bc821-162">Nell'esempio seguente, che è una continuazione dell'applicazione console precedente, viene visualizzato il valore di tale elemento di proprietà:</span><span class="sxs-lookup"><span data-stu-id="bc821-162">The following example, which is a continuation of the previous console application, displays the value of that property item:</span></span>


```
printf("The equipment make is %s.\n", pPropBuffer[1].value);
```



<span data-ttu-id="bc821-163">La riga di codice precedente produce l'output seguente:</span><span class="sxs-lookup"><span data-stu-id="bc821-163">The preceding line of code produces the following output:</span></span>


```
The equipment make is Northwind Traders.
```



<span data-ttu-id="bc821-164">Il quinto elemento della proprietà (indice 4) nell'elenco ha **ID** PropertyTagExifExposureTime e **tipo** PropertyTagTypeRational.</span><span class="sxs-lookup"><span data-stu-id="bc821-164">The fifth (index 4) property item in the list has **id** PropertyTagExifExposureTime and **type** PropertyTagTypeRational.</span></span> <span data-ttu-id="bc821-165">Il tipo di dati (PropertyTagTypeRational) è una coppia di **valori LONG.**</span><span class="sxs-lookup"><span data-stu-id="bc821-165">That data type (PropertyTagTypeRational) is a pair of **LONG** s.</span></span> <span data-ttu-id="bc821-166">Nell'esempio seguente, che è una continuazione dell'applicazione console precedente, vengono visualizzati i due **valori LONG** come frazione.</span><span class="sxs-lookup"><span data-stu-id="bc821-166">The following example, which is a continuation of the previous console application, displays those two **LONG** values as a fraction.</span></span> <span data-ttu-id="bc821-167">Tale frazione, 1/125, è il tempo di esposizione misurato in secondi.</span><span class="sxs-lookup"><span data-stu-id="bc821-167">That fraction, 1/125, is the exposure time measured in seconds.</span></span>


```
long* ptrLong = (long*)(pPropBuffer[4].value);
printf("The exposure time is %d/%d.\n", ptrLong[0], ptrLong[1]);
```



<span data-ttu-id="bc821-168">L'output del codice precedente è il seguente:</span><span class="sxs-lookup"><span data-stu-id="bc821-168">The preceding code produces the following output:</span></span>


```
The exposure time is 1/125.
```



## <a name="writing-metadata-to-a-file"></a><span data-ttu-id="bc821-169">Scrittura di metadati in un file</span><span class="sxs-lookup"><span data-stu-id="bc821-169">Writing Metadata to a File</span></span>

<span data-ttu-id="bc821-170">Per scrivere un elemento di metadati in un oggetto [**Image,**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) inizializzare un oggetto [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) e quindi passare l'indirizzo di tale oggetto **PropertyItem** al **metodo SetPropertyItem** dell'oggetto **Image.**</span><span class="sxs-lookup"><span data-stu-id="bc821-170">To write an item of metadata to an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object, initialize a [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) object and then pass the address of that **PropertyItem** object to the **SetPropertyItem** method of the **Image** object.</span></span>

<span data-ttu-id="bc821-171">L'applicazione console seguente scrive un elemento (il titolo dell'immagine) dei metadati in un oggetto [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e quindi salva l'immagine nel file su disco FakePhoto2.jpg.</span><span class="sxs-lookup"><span data-stu-id="bc821-171">The following console application writes one item (the image title) of metadata to an [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) object and then saves the image in the disk file FakePhoto2.jpg.</span></span> <span data-ttu-id="bc821-172">La funzione main si basa sulla funzione helper GetEncoderClsid, illustrata nell'argomento Recupero dell'identificatore di classe per [un codificatore.](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)</span><span class="sxs-lookup"><span data-stu-id="bc821-172">The main function relies on the helper function GetEncoderClsid, which is shown in the topic [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


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



 

 

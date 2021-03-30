---
description: 'La classe Image fornisce il metodo Image:: getencoderparametername, in modo che sia possibile determinare i parametri supportati da un codificatore di immagini specificato.'
ms.assetid: 2e1a5279-dd9d-46de-822c-d356a344f340
title: Determinazione dei parametri supportati da un codificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9bd76abb0b9f01bf55fd738df77cd086bc757c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994280"
---
# <a name="determining-the-parameters-supported-by-an-encoder"></a><span data-ttu-id="6a4ee-103">Determinazione dei parametri supportati da un codificatore</span><span class="sxs-lookup"><span data-stu-id="6a4ee-103">Determining the Parameters Supported by an Encoder</span></span>

<span data-ttu-id="6a4ee-104">La classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) fornisce il metodo [**Image:: getencoderparametername**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist) , in modo che sia possibile determinare i parametri supportati da un codificatore di immagini specificato.</span><span class="sxs-lookup"><span data-stu-id="6a4ee-104">The [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class provides the [**Image::GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist) method so that you can determine the parameters that are supported by a given image encoder.</span></span> <span data-ttu-id="6a4ee-105">Il metodo **Image:: Getencoderparametername** restituisce una matrice di oggetti [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) .</span><span class="sxs-lookup"><span data-stu-id="6a4ee-105">The **Image::GetEncoderParameterList** method returns an array of [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) objects.</span></span> <span data-ttu-id="6a4ee-106">È necessario allocare un buffer per ricevere la matrice prima di chiamare **Image:: getencoderparameter**.</span><span class="sxs-lookup"><span data-stu-id="6a4ee-106">You must allocate a buffer to receive that array before you call **Image::GetEncoderParameterList**.</span></span> <span data-ttu-id="6a4ee-107">È possibile chiamare [**Image:: GetEncoderParameterListSize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlistsize) per determinare le dimensioni del buffer richiesto.</span><span class="sxs-lookup"><span data-stu-id="6a4ee-107">You can call [**Image::GetEncoderParameterListSize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlistsize) to determine the size of the required buffer.</span></span>

<span data-ttu-id="6a4ee-108">L'applicazione console seguente ottiene l'elenco di parametri per il codificatore JPEG.</span><span class="sxs-lookup"><span data-stu-id="6a4ee-108">The following console application obtains the parameter list for the JPEG encoder.</span></span> <span data-ttu-id="6a4ee-109">La funzione Main si basa sulla funzione helper GetEncoderClsid, che viene mostrata durante il [recupero dell'identificatore di classe per un codificatore](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span><span class="sxs-lookup"><span data-stu-id="6a4ee-109">The main function relies on the helper function GetEncoderClsid, which is shown in [Retrieving the Class Identifier for an Encoder](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).</span></span>


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT GetEncoderClsid(const WCHAR* format, CLSID* pClsid);  // helper function

INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   // Create Bitmap (inherited from Image) object so that we can call
   // GetParameterListSize and GetParameterList.
   Bitmap* bitmap = new Bitmap(1, 1);

   // Get the JPEG encoder CLSID.
   CLSID encoderClsid;
   GetEncoderClsid(L"image/jpeg", &encoderClsid);

   // How big (in bytes) is the JPEG encoder's parameter list?
   UINT listSize = 0; 
   listSize = bitmap->GetEncoderParameterListSize(&encoderClsid);
   printf("The parameter list requires %d bytes.\n", listSize);

   // Allocate a buffer large enough to hold the parameter list.
   EncoderParameters* pEncoderParameters = NULL;
   pEncoderParameters = (EncoderParameters*)malloc(listSize);

   // Get the parameter list for the JPEG encoder.
   bitmap->GetEncoderParameterList(
      &encoderClsid, listSize, pEncoderParameters);

   // pEncoderParameters points to an EncoderParameters object, which
   // has a Count member and an array of EncoderParameter objects.
   // How many EncoderParameter objects are in the array?
   printf("There are %d EncoderParameter objects in the array.\n", 
      pEncoderParameters->Count);

   free(pEncoderParameters);
   delete(bitmap);
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



<span data-ttu-id="6a4ee-110">Quando si esegue l'applicazione console precedente, si otterrà un output simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="6a4ee-110">When you run the preceding console application, you get an output similar to the following:</span></span>


```
The parameter list requires 172 bytes.
There are 4 EncoderParameter objects in the array.
```



<span data-ttu-id="6a4ee-111">Ogni oggetto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) della matrice ha i quattro membri dati pubblici seguenti:</span><span class="sxs-lookup"><span data-stu-id="6a4ee-111">Each of the [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) objects in the array has the following four public data members:</span></span>

<span data-ttu-id="6a4ee-112">Il codice seguente è una continuazione dell'applicazione console mostrata nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="6a4ee-112">The following code is a continuation of the console application shown in the preceding example.</span></span> <span data-ttu-id="6a4ee-113">Il codice esamina il secondo oggetto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) nella matrice restituita da [**Image:: getencoderparameter**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist).</span><span class="sxs-lookup"><span data-stu-id="6a4ee-113">The code looks at the second [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object in the array returned by [**Image::GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist).</span></span> <span data-ttu-id="6a4ee-114">Il codice chiama [StringFromGUID2](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2), che è una funzione di sistema dichiarata in OBJBASE. h, per convertire il membro **GUID** dell'oggetto **EncoderParameter** in una stringa.</span><span class="sxs-lookup"><span data-stu-id="6a4ee-114">The code calls [StringFromGUID2](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2), which is a system function declared in Objbase.h, to convert the **Guid** member of the **EncoderParameter** object to a string.</span></span>


```
// Look at the second (index 1) EncoderParameter object in the array.
printf("Parameter[1]\n");

WCHAR strGuid[39];
StringFromGUID2(pEncoderParameters->Parameter[1].Guid, strGuid, 39);
wprintf(L"   The GUID is %s.\n", strGuid);

printf("   The value type is %d.\n", 
   pEncoderParameters->Parameter[1].Type);

printf("   The number of values is %d.\n",
   pEncoderParameters->Parameter[1].NumberOfValues);
```



<span data-ttu-id="6a4ee-115">L'output del codice precedente è il seguente:</span><span class="sxs-lookup"><span data-stu-id="6a4ee-115">The preceding code produces the following output:</span></span>


```
Parameter[1]
   The GUID is {1D5BE4B5-FA4A-452D-9CDD-5DB35105E7EB}.
   The value type is 6.
   The number of values is 1.
```



<span data-ttu-id="6a4ee-116">È possibile cercare il GUID in Gdiplusimaging. h e scoprire che la categoria di questo oggetto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) è EncoderQuality.</span><span class="sxs-lookup"><span data-stu-id="6a4ee-116">You can look up the GUID in Gdiplusimaging.h and find out that the category of this [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object is EncoderQuality.</span></span> <span data-ttu-id="6a4ee-117">È possibile utilizzare questa categoria (EncoderQuality) del parametro per impostare il livello di compressione di un'immagine JPEG.</span><span class="sxs-lookup"><span data-stu-id="6a4ee-117">You can use this category (EncoderQuality) of parameter to set the compression level of a JPEG image.</span></span>

<span data-ttu-id="6a4ee-118">In Gdiplusenums. h, l'enumerazione [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) indica che il tipo di dati 6 è **ValueLongRange**.</span><span class="sxs-lookup"><span data-stu-id="6a4ee-118">In Gdiplusenums.h, the [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) enumeration indicates that data type 6 is **ValueLongRange**.</span></span> <span data-ttu-id="6a4ee-119">Un intervallo lungo è una coppia di valori **ULONG** .</span><span class="sxs-lookup"><span data-stu-id="6a4ee-119">A long range is a pair of **ULONG** values.</span></span>

<span data-ttu-id="6a4ee-120">Il numero di valori è uno, quindi sappiamo che il membro del **valore** dell'oggetto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) è un puntatore a una matrice con un elemento.</span><span class="sxs-lookup"><span data-stu-id="6a4ee-120">The number of values is one, so we know that the **Value** member of the [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object is a pointer to an array that has one element.</span></span> <span data-ttu-id="6a4ee-121">Un elemento è una coppia di valori **ULONG** .</span><span class="sxs-lookup"><span data-stu-id="6a4ee-121">That one element is a pair of **ULONG** values.</span></span>

<span data-ttu-id="6a4ee-122">Il codice seguente è una continuazione dell'applicazione console mostrata nei due esempi precedenti.</span><span class="sxs-lookup"><span data-stu-id="6a4ee-122">The following code is a continuation of the console application that is shown in the preceding two examples.</span></span> <span data-ttu-id="6a4ee-123">Il codice definisce un tipo di dati denominato **PLONGRANGE** (puntatore a un intervallo lungo).</span><span class="sxs-lookup"><span data-stu-id="6a4ee-123">The code defines a data type called **PLONGRANGE** (pointer to a long range).</span></span> <span data-ttu-id="6a4ee-124">Una variabile di tipo **PLONGRANGE** viene utilizzata per estrarre i valori minimo e massimo che possono essere passati come impostazione di qualità al codificatore JPEG.</span><span class="sxs-lookup"><span data-stu-id="6a4ee-124">A variable of type **PLONGRANGE** is used to extract the minimum and maximum values that can be passed as a quality setting to the JPEG encoder.</span></span>


```
typedef struct
   {
      long min;
      long max;
   }* PLONGRANGE;

   PLONGRANGE pLongRange = 
      (PLONGRANGE)(pEncoderParameters->Parameter[1].Value);

   printf("   The minimum possible quality value is %d.\n",
      pLongRange->min);

   printf("   The maximum possible quality value is %d.\n",
      pLongRange->max);
```



<span data-ttu-id="6a4ee-125">L'output del codice precedente è il seguente:</span><span class="sxs-lookup"><span data-stu-id="6a4ee-125">The preceding code produces the following output:</span></span>


```
The minimum possible quality value is 0.
The maximum possible quality value is 100.
```



<span data-ttu-id="6a4ee-126">Nell'esempio precedente, il valore restituito nell'oggetto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) è una coppia di valori **ULONG** che indica i valori minimi e massimi possibili per il parametro Quality.</span><span class="sxs-lookup"><span data-stu-id="6a4ee-126">In the preceding example, the value returned in the [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) object is a pair of **ULONG** values that indicate the minimum and maximum possible values for the quality parameter.</span></span> <span data-ttu-id="6a4ee-127">In alcuni casi, i valori restituiti in un oggetto **EncoderParameter** sono membri dell'enumerazione [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) .</span><span class="sxs-lookup"><span data-stu-id="6a4ee-127">In some cases, the values returned in an **EncoderParameter** object are members of the [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) enumeration.</span></span> <span data-ttu-id="6a4ee-128">Negli argomenti seguenti vengono illustrati i metodi e l'enumerazione **EncoderValue** per elencare i possibili valori di parametro in modo più dettagliato:</span><span class="sxs-lookup"><span data-stu-id="6a4ee-128">The following topics discuss the **EncoderValue** enumeration and methods for listing possible parameter values in more detail:</span></span>

-   [<span data-ttu-id="6a4ee-129">Utilizzo dell'enumerazione EncoderValue</span><span class="sxs-lookup"><span data-stu-id="6a4ee-129">Using the EncoderValue Enumeration</span></span>](-gdiplus-using-the-encodervalue-enumeration-use.md)
-   [<span data-ttu-id="6a4ee-130">Elenco di parametri e valori per tutti i codificatori</span><span class="sxs-lookup"><span data-stu-id="6a4ee-130">Listing Parameters and Values for All Encoders</span></span>](-gdiplus-listing-parameters-and-values-for-all-encoders-use.md)

 

 

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
# <a name="determining-the-parameters-supported-by-an-encoder"></a>Determinazione dei parametri supportati da un codificatore

La classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) fornisce il metodo [**Image:: getencoderparametername**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist) , in modo che sia possibile determinare i parametri supportati da un codificatore di immagini specificato. Il metodo **Image:: Getencoderparametername** restituisce una matrice di oggetti [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) . È necessario allocare un buffer per ricevere la matrice prima di chiamare **Image:: getencoderparameter**. È possibile chiamare [**Image:: GetEncoderParameterListSize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlistsize) per determinare le dimensioni del buffer richiesto.

L'applicazione console seguente ottiene l'elenco di parametri per il codificatore JPEG. La funzione Main si basa sulla funzione helper GetEncoderClsid, che viene mostrata durante il [recupero dell'identificatore di classe per un codificatore](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md).


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



Quando si esegue l'applicazione console precedente, si otterrà un output simile al seguente:


```
The parameter list requires 172 bytes.
There are 4 EncoderParameter objects in the array.
```



Ogni oggetto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) della matrice ha i quattro membri dati pubblici seguenti:

Il codice seguente è una continuazione dell'applicazione console mostrata nell'esempio precedente. Il codice esamina il secondo oggetto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) nella matrice restituita da [**Image:: getencoderparameter**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist). Il codice chiama [StringFromGUID2](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2), che è una funzione di sistema dichiarata in OBJBASE. h, per convertire il membro **GUID** dell'oggetto **EncoderParameter** in una stringa.


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



L'output del codice precedente è il seguente:


```
Parameter[1]
   The GUID is {1D5BE4B5-FA4A-452D-9CDD-5DB35105E7EB}.
   The value type is 6.
   The number of values is 1.
```



È possibile cercare il GUID in Gdiplusimaging. h e scoprire che la categoria di questo oggetto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) è EncoderQuality. È possibile utilizzare questa categoria (EncoderQuality) del parametro per impostare il livello di compressione di un'immagine JPEG.

In Gdiplusenums. h, l'enumerazione [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) indica che il tipo di dati 6 è **ValueLongRange**. Un intervallo lungo è una coppia di valori **ULONG** .

Il numero di valori è uno, quindi sappiamo che il membro del **valore** dell'oggetto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) è un puntatore a una matrice con un elemento. Un elemento è una coppia di valori **ULONG** .

Il codice seguente è una continuazione dell'applicazione console mostrata nei due esempi precedenti. Il codice definisce un tipo di dati denominato **PLONGRANGE** (puntatore a un intervallo lungo). Una variabile di tipo **PLONGRANGE** viene utilizzata per estrarre i valori minimo e massimo che possono essere passati come impostazione di qualità al codificatore JPEG.


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



L'output del codice precedente è il seguente:


```
The minimum possible quality value is 0.
The maximum possible quality value is 100.
```



Nell'esempio precedente, il valore restituito nell'oggetto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) è una coppia di valori **ULONG** che indica i valori minimi e massimi possibili per il parametro Quality. In alcuni casi, i valori restituiti in un oggetto **EncoderParameter** sono membri dell'enumerazione [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) . Negli argomenti seguenti vengono illustrati i metodi e l'enumerazione **EncoderValue** per elencare i possibili valori di parametro in modo più dettagliato:

-   [Utilizzo dell'enumerazione EncoderValue](-gdiplus-using-the-encodervalue-enumeration-use.md)
-   [Elenco di parametri e valori per tutti i codificatori](-gdiplus-listing-parameters-and-values-for-all-encoders-use.md)

 

 

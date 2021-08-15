---
description: La classe Image fornisce il metodo Image::GetEncoderParameterList in modo che sia possibile determinare i parametri supportati da un codificatore di immagini specificato.
ms.assetid: 2e1a5279-dd9d-46de-822c-d356a344f340
title: Determinazione dei parametri supportati da un codificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c842b14a2d14af578eede428e79018a2d266ea6133ed61a9bd0736e8dadc97e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977571"
---
# <a name="determining-the-parameters-supported-by-an-encoder"></a>Determinazione dei parametri supportati da un codificatore

La [**classe Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) fornisce il metodo [**Image::GetEncoderParameterList**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist) in modo che sia possibile determinare i parametri supportati da un codificatore di immagini specificato. Il **metodo Image::GetEncoderParameterList** restituisce una matrice di [**oggetti EncoderParameter.**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) È necessario allocare un buffer per ricevere tale matrice prima di chiamare **Image::GetEncoderParameterList**. È possibile chiamare [**Image::GetEncoderParameterListSize**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlistsize) per determinare le dimensioni del buffer richiesto.

L'applicazione console seguente ottiene l'elenco di parametri per il codificatore JPEG. La funzione main si basa sulla funzione helper GetEncoderClsid, illustrata in Recupero dell'identificatore di classe [per un codificatore.](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)


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



Quando si esegue l'applicazione console precedente, si ottiene un output simile al seguente:


```
The parameter list requires 172 bytes.
There are 4 EncoderParameter objects in the array.
```



Ogni oggetto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) nella matrice ha i quattro membri dati pubblici seguenti:

Il codice seguente è una continuazione dell'applicazione console illustrata nell'esempio precedente. Il codice esamina il secondo [**oggetto EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) nella matrice restituita da [**Image::GetEncoderParameterList.**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist) Il codice chiama [StringFromGUID2,](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2)una funzione di sistema dichiarata in Objbase.h, per convertire il membro **Guid** dell'oggetto **EncoderParameter** in una stringa.


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



È possibile cercare il GUID in Gdiplusimaging.h e scoprire che la categoria di questo oggetto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) è EncoderQuality. È possibile usare questa categoria (EncoderQuality) del parametro per impostare il livello di compressione di un'immagine JPEG.

In Gdiplusenums.h l'enumerazione [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) indica che il tipo di dati 6 è **ValueLongRange.** Un intervallo lungo è una coppia di **valori ULONG.**

Il numero di valori è uno, quindi si sa che il membro **Value** dell'oggetto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) è un puntatore a una matrice che ha un elemento. Tale elemento è una coppia di **valori ULONG.**

Il codice seguente è una continuazione dell'applicazione console illustrata nei due esempi precedenti. Il codice definisce un tipo di dati denominato **PLONGRANGE** (puntatore a un intervallo lungo). Una variabile di tipo **PLONGRANGE viene** usata per estrarre i valori minimo e massimo che possono essere passati come impostazione di qualità al codificatore JPEG.


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



Nell'esempio precedente il valore restituito nell'oggetto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) è una coppia di valori **ULONG** che indicano i valori minimo e massimo possibili per il parametro quality. In alcuni casi, i valori restituiti in un **oggetto EncoderParameter** sono membri dell'enumerazione [**EncoderValue.**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) Negli argomenti seguenti vengono illustrati **l'enumerazione EncoderValue** e i metodi per elencare in modo più dettagliato i valori dei parametri possibili:

-   [Uso dell'enumerazione EncoderValue](-gdiplus-using-the-encodervalue-enumeration-use.md)
-   [Elenco di parametri e valori per tutti i codificatori](-gdiplus-listing-parameters-and-values-for-all-encoders-use.md)

 

 

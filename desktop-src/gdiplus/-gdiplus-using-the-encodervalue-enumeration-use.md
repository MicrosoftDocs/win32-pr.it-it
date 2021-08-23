---
description: Un codificatore specificato supporta determinate categorie di parametri e per ognuna di queste categorie il codificatore consente determinati valori.
ms.assetid: cb9552e9-e807-4b07-b315-4550762e7026
title: Uso dell'enumerazione EncoderValue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 488d465d27f7884ecc5999d38fea10afdac06b74b77d29338c8d0944a1261b92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666321"
---
# <a name="using-the-encodervalue-enumeration"></a>Uso dell'enumerazione EncoderValue

Un codificatore specificato supporta determinate categorie di parametri e per ognuna di queste categorie il codificatore consente determinati valori. Ad esempio, il codificatore JPEG supporta la categoria di parametri EncoderValueQuality e i valori dei parametri consentiti sono i numeri interi da 0 a 100. Alcuni dei valori dei parametri consentiti sono gli stessi in diversi codificatori. Questi valori standard sono definiti nell'enumerazione [**EncoderValue**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) in Gdiplusenums.h:


```
enum EncoderValue
{
   EncoderValueColorTypeCMYK,             // 0
   EncoderValueColorTypeYCCK,             // 1
   EncoderValueCompressionLZW,            // 2
   EncoderValueCompressionCCITT3,         // 3
   EncoderValueCompressionCCITT4,         // 4
   EncoderValueCompressionRle,            // 5
   EncoderValueCompressionNone,           // 6
   EncoderValueScanMethodInterlaced,      // 7
   EncoderValueScanMethodNonInterlaced,   // 8
   EncoderValueVersionGif87,              // 9
   EncoderValueVersionGif89,              // 10
   EncoderValueRenderProgressive,         // 11
   EncoderValueRenderNonProgressive,      // 12
   EncoderValueTransformRotate90,         // 13
   EncoderValueTransformRotate180,        // 14
   EncoderValueTransformRotate270,        // 15
   EncoderValueTransformFlipHorizontal,   // 16
   EncoderValueTransformFlipVertical,     // 17
   EncoderValueMultiFrame,                // 18
   EncoderValueLastFrame,                 // 19
   EncoderValueFlush,                     // 20
   EncoderValueFrameDimensionTime,        // 21
   EncoderValueFrameDimensionResolution,  // 22
   EncoderValueFrameDimensionPage         // 23
};
```



Una delle categorie di parametri supportate dal codificatore JPEG è la categoria EncoderTransformation. Esaminando [**l'enumerazione EncoderValue,**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue) è possibile speculare (e sarebbe corretto) che la categoria EncoderTransformation consenta i cinque valori seguenti:


```
EncoderValueTransformRotate90,          // 13
EncoderValueTransformRotate180,         // 14
EncoderValueTransformRotate270,         // 15
EncoderValueTransformFlipHorizontal,    // 16
EncoderValueTransformFlipVertical,      // 17
```



L'applicazione console seguente verifica che il codificatore JPEG supporti la categoria di parametri EncoderTransformation e che siano disponibili cinque valori consentiti per tale parametro. La funzione main si basa sulla funzione helper GetEncoderClsid, illustrata in Recupero dell'identificatore di classe [per un codificatore.](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)


```
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;
INT GetEncoderClsid(const WCHAR* format, CLSID* pClsid);
INT main()
{
   // Initialize GDI+.
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);
   // Create a Bitmap (inherited from Image) object so that we can call
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
   // Look at the first (index 0) EncoderParameter object in the array.
   printf("Parameter[0]\n");
   WCHAR strGuid[39];
   StringFromGUID2(pEncoderParameters->Parameter[0].Guid, strGuid, 39);
   wprintf(L"   The guid is %s.\n", strGuid);
   printf("   The data type is %d.\n", 
      pEncoderParameters->Parameter[0].Type);
   printf("   The number of values is %d.\n",
      pEncoderParameters->Parameter[0].NumberOfValues);
   free(pEncoderParameters);
   delete bitmap;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```



Quando si esegue l'applicazione console precedente, si ottiene un output simile al seguente:


```
The parameter list requires 172 bytes.
There are 4 EncoderParameter objects in the array.
Parameter[0]
   The GUID is {8D0EB2D1-A58E-4EA8-AA14-108074B7B6F9}.
   The value type is 4.
   The number of values is 5.
```



È possibile cercare il GUID in Gdiplusimaging.h e scoprire che la categoria di questo oggetto [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) è EncoderTransformation. In Gdiplusenums.h l'enumerazione [**EncoderParameterValueType**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encoderparametervaluetype) indica che il tipo di dati 4 è ValueLong (intero senza segno a 32 bit). Il numero di valori è cinque, quindi è possibile sapere che il membro **Value** dell'oggetto **EncoderParameter** è un puntatore a una matrice di cinque **valori ULONG.**

Il codice seguente è una continuazione dell'applicazione console illustrata nell'esempio precedente. Il codice elenca i valori consentiti per un parametro EncoderTransformation:


```
ULONG* pUlong = (ULONG*)(pEncoderParameters->Parameter[0].Value);
ULONG numVals = pEncoderParameters->Parameter[0].NumberOfValues;
printf("%s", "   The allowable values are");
for(ULONG j = 0; j < numVals; ++j)
{
   printf("  %d", pUlong[j]);
}
```



L'output del codice precedente è il seguente:


```
The allowable values are  13  14  15  16  17
```



I valori consentiti (13, 14, 15, 16 e 17) corrispondono ai membri seguenti dell'enumerazione [**EncoderValue:**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-encodervalue)


```
EncoderValueTransformRotate90,        // 13
EncoderValueTransformRotate180,       // 14
EncoderValueTransformRotate270,       // 15
EncoderValueTransformFlipHorizontal,  // 16
EncoderValueTransformFlipVertical,    // 17
```



 

 

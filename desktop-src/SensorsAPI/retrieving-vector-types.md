---
description: Alcune proprietà e campi dati contengono matrici di informazioni.
ms.assetid: 85e3b953-be36-4d60-b04e-4f572d0b9564
title: Recupero di tipi di vettore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4945b45e4e78b6c4f9f9e0fb4b3848f813549105
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525651"
---
# <a name="retrieving-vector-types"></a>Recupero di tipi di vettore

Alcune proprietà e campi dati contengono matrici di informazioni. Ad esempio, la \_ proprietà della curva della risposta chiara della proprietà del sensore \_ \_ \_ contiene una matrice di interi senza segno a 4 byte. Tuttavia, quando si ricevono tali matrici tramite l'API del sensore, vengono sempre rappresentate come tipo VT \_ vector \| Ui1, una matrice di caratteri a byte singolo, indipendentemente dal tipo effettivo dei dati nella matrice. Per questi tipi, è necessario prestare attenzione a eseguire il cast delle variabili di matrice al tipo di dati corretto per la proprietà o il campo dati.

Per informazioni sulle proprietà, sui campi dati e sui relativi tipi, vedere [costanti](constants.md).

Il codice di esempio seguente illustra come eseguire il cast dei dati recuperati nella \_ \_ curva di risposta leggera della proprietà del sensore \_ \_ al tipo corretto.


```C++
PROPVARIANT pvCurve;
PropVariantInit(&pvCurve);

// Retrieve the property value.
hr = pSensor->GetProperty(SENSOR_PROPERTY_LIGHT_RESPONSE_CURVE, &pvCurve);
if (SUCCEEDED(hr))
{
    if ((VT_UI1|VT_VECTOR) == V_VT(pvCurve)) // Note actual type of UI1
    {
        // Cast the array to UINT, a 4-byte unsigned integer.

        // Item count for the array.
        UINT  cElement = pvCurve.caub.cElems/sizeof(UINT);
        // Array pointer.
        UINT* pElement = (UINT*)(pvCurve.caub.pElems);

        // Use the array.
    }
}

// Remember to free the PROPVARIANT when done.
PropVariantClear(&pvCurve);
```



 

 




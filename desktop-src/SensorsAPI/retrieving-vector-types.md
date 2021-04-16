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
# <a name="retrieving-vector-types"></a><span data-ttu-id="34975-103">Recupero di tipi di vettore</span><span class="sxs-lookup"><span data-stu-id="34975-103">Retrieving Vector Types</span></span>

<span data-ttu-id="34975-104">Alcune proprietà e campi dati contengono matrici di informazioni.</span><span class="sxs-lookup"><span data-stu-id="34975-104">Some properties and data fields contain arrays of information.</span></span> <span data-ttu-id="34975-105">Ad esempio, la \_ proprietà della curva della risposta chiara della proprietà del sensore \_ \_ \_ contiene una matrice di interi senza segno a 4 byte.</span><span class="sxs-lookup"><span data-stu-id="34975-105">For example, the SENSOR\_PROPERTY\_LIGHT\_RESPONSE\_CURVE property contains an array of 4-byte unsigned integers.</span></span> <span data-ttu-id="34975-106">Tuttavia, quando si ricevono tali matrici tramite l'API del sensore, vengono sempre rappresentate come tipo VT \_ vector \| Ui1, una matrice di caratteri a byte singolo, indipendentemente dal tipo effettivo dei dati nella matrice.</span><span class="sxs-lookup"><span data-stu-id="34975-106">However, when you receive such arrays through the Sensor API, they are always represented as type VT\_VECTOR\|UI1, an array of single-byte characters, regardless of the actual type of the data in the array.</span></span> <span data-ttu-id="34975-107">Per questi tipi, è necessario prestare attenzione a eseguire il cast delle variabili di matrice al tipo di dati corretto per la proprietà o il campo dati.</span><span class="sxs-lookup"><span data-stu-id="34975-107">For these types, you must be careful to cast array variables to the correct data type for the property or data field.</span></span>

<span data-ttu-id="34975-108">Per informazioni sulle proprietà, sui campi dati e sui relativi tipi, vedere [costanti](constants.md).</span><span class="sxs-lookup"><span data-stu-id="34975-108">For information about properties, data fields, and their types, see [Constants](constants.md).</span></span>

<span data-ttu-id="34975-109">Il codice di esempio seguente illustra come eseguire il cast dei dati recuperati nella \_ \_ curva di risposta leggera della proprietà del sensore \_ \_ al tipo corretto.</span><span class="sxs-lookup"><span data-stu-id="34975-109">The following example code shows how to cast the data retrieved in SENSOR\_PROPERTY\_LIGHT\_RESPONSE\_CURVE to the correct type.</span></span>


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



 

 




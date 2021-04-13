---
description: È possibile determinare il numero di colori supportati da un dispositivo e quali sono i colori recuperando il numero di colori per il dispositivo ed enumerando i colori delle penne solide.
ms.assetid: cbaa3732-e55e-42af-93de-390450d38fc9
title: Enumerazione dei colori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dca39ec9817ecab07c2c2bc42b08fbee83333f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978615"
---
# <a name="enumerating-colors"></a><span data-ttu-id="31c40-103">Enumerazione dei colori</span><span class="sxs-lookup"><span data-stu-id="31c40-103">Enumerating Colors</span></span>

<span data-ttu-id="31c40-104">È possibile determinare il numero di colori supportati da un dispositivo e quali sono i colori recuperando il numero di colori per il dispositivo ed enumerando i colori delle penne solide.</span><span class="sxs-lookup"><span data-stu-id="31c40-104">You can determine how many colors a device supports and what those colors are by retrieving the count of colors for the device and enumerating the colors of the solid pens.</span></span> <span data-ttu-id="31c40-105">Per recuperare il numero di colori, usare la funzione [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) con il valore NUMCOLORS.</span><span class="sxs-lookup"><span data-stu-id="31c40-105">To retrieve the number of colors, use the [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) function with the NUMCOLORS value.</span></span> <span data-ttu-id="31c40-106">Per enumerare le penne solide, usare la funzione [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) e una funzione di callback corrispondente che riceve informazioni su ogni penna.</span><span class="sxs-lookup"><span data-stu-id="31c40-106">To enumerate solid pens, use the [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) function and a corresponding callback function that receives information about each pen.</span></span>


```C++
// GetTheColors - returns the count and color values of solid colors 
// Returns a pointer to the array containing colors 
// hdc - handle to device context 

COLORREF *GetTheColors(HDC hdc)
{
    int cColors;
    COLORREF *aColors;

    // Get the number of colors. 
    cColors = GetDeviceCaps(hdc, NUMCOLORS);

    // Allocate space for the array. 
    aColors = (COLORREF *)LocalAlloc(LPTR, sizeof(COLORREF) * 
        (cColors+1));

    // Save the count of colors in first element. 
    aColors[0] = (LONG)cColors;

    // Enumerate all pens and save solid colors in the array. 
    EnumObjects(hdc, OBJ_PEN, (GOBJENUMPROC)MyEnumProc, (LONG)aColors);

    // Refresh the count of colors. 
    aColors[0] = (LONG)cColors;

    return aColors;
}

int MyEnumProc(LPVOID lp, LPBYTE lpb)
{
    LPLOGPEN lopn;
    COLORREF *aColors;
    int iColor;

    lopn = (LPLOGPEN)lp;
    aColors = (COLORREF *)lpb;

    if (lopn->lopnStyle==PS_SOLID) 
    {
        // Check for too many colors. 
        if ((iColor = (int)aColors[0]) <= 0)
             return 0;
        aColors[iColor] = lopn->lopnColor;
        aColors[0]--;
    }
    return 1;
}
```



 

 




---
description: La funzione ByteToStr converte una matrice di valori di BYTE in una stringa di caratteri esadecimali.
ms.assetid: b1320e0f-fb67-4ed8-af3c-8ca7f0145468
title: ByteToStr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f6a4284a9ac56db9e7d74d27206c98d4db1894d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058309"
---
# <a name="bytetostr"></a><span data-ttu-id="5465c-103">ByteToStr</span><span class="sxs-lookup"><span data-stu-id="5465c-103">ByteToStr</span></span>

<span data-ttu-id="5465c-104">La funzione **ByteToStr** converte una matrice di valori di **byte** in una stringa di caratteri esadecimali.</span><span class="sxs-lookup"><span data-stu-id="5465c-104">The **ByteToStr** function converts an array of **BYTE** values to a hexadecimal character string.</span></span>


```C++
#include <windows.h>

void ByteToStr(
     DWORD cb, 
     void* pv, 
     LPSTR sz)
//--------------------------------------------------------------------
// Parameters passed are:
//    pv is the array of BYTES to be converted.
//    cb is the number of BYTEs in the array.
//    sz is a pointer to the string to be returned.

{
//--------------------------------------------------------------------
//  Declare and initialize local variables.

BYTE* pb = (BYTE*) pv; // local pointer to a BYTE in the BYTE array
DWORD i;               // local loop counter
int b;                 // local variable

//--------------------------------------------------------------------
//  Begin processing loop.

for (i = 0; i<cb; i++)
{
   b = (*pb & 0xF0) >> 4;
   *sz++ = (b <= 9) ? b + '0' : (b - 10) + 'A';
   b = *pb & 0x0F;
   *sz++ = (b <= 9) ? b + '0' : (b - 10) + 'A';
   pb++;
}
*sz++ = 0;
}
```



 

 




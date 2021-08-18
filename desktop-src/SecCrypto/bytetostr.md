---
description: La funzione ByteToStr converte una matrice di valori BYTE in una stringa di caratteri esadecimali.
ms.assetid: b1320e0f-fb67-4ed8-af3c-8ca7f0145468
title: ByteToStr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e231756725a697d933699af970b164869a973aa9ddb8199467bb6a9941313625
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772966"
---
# <a name="bytetostr"></a>ByteToStr

La **funzione ByteToStr** converte una matrice di valori **BYTE** in una stringa di caratteri esadecimali.


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



 

 




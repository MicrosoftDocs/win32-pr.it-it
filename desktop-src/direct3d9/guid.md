---
description: Definisce un GUID che può essere utilizzato in altri modelli.
ms.assetid: dbfdd307-310f-4c80-b4aa-f16a81a9a372
title: GUID (DirectX 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e83e45d6e993153cf293a2ad55080c74f2e6049d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521433"
---
# <a name="guid-directx-9"></a>GUID (DirectX 9)

Definisce un GUID che può essere utilizzato in altri modelli.

``` syntax
template Guid
{
    < a42790e0-7810-11cf-8f52-0040333594a3 >
    DWORD data1;
    WORD data2;
    WORD data3;
    array UCHAR data4[8];
} 
```

Dove i parametri formano il formato di archiviazione binario per un GUID:

-   Data1-valore dati Unsigned Integer a 32 bit
-   data2-valore dati Unsigned Integer a 16 bit
-   data3-valore dati Unsigned Integer a 16 bit
-   DATA4: matrice di caratteri non firmati

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Modelli](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 




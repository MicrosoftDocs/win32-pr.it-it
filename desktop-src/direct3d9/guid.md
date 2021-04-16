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
# <a name="guid-directx-9"></a><span data-ttu-id="6bad5-103">GUID (DirectX 9)</span><span class="sxs-lookup"><span data-stu-id="6bad5-103">Guid (DirectX 9)</span></span>

<span data-ttu-id="6bad5-104">Definisce un GUID che può essere utilizzato in altri modelli.</span><span class="sxs-lookup"><span data-stu-id="6bad5-104">Defines a GUID that can be used in other templates.</span></span>

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

<span data-ttu-id="6bad5-105">Dove i parametri formano il formato di archiviazione binario per un GUID:</span><span class="sxs-lookup"><span data-stu-id="6bad5-105">Where the parameters together form the binary storage format for a GUID:</span></span>

-   <span data-ttu-id="6bad5-106">Data1-valore dati Unsigned Integer a 32 bit</span><span class="sxs-lookup"><span data-stu-id="6bad5-106">data1 - 32-bit unsigned integer data value</span></span>
-   <span data-ttu-id="6bad5-107">data2-valore dati Unsigned Integer a 16 bit</span><span class="sxs-lookup"><span data-stu-id="6bad5-107">data2 - 16-bit unsigned integer data value</span></span>
-   <span data-ttu-id="6bad5-108">data3-valore dati Unsigned Integer a 16 bit</span><span class="sxs-lookup"><span data-stu-id="6bad5-108">data3 - 16-bit unsigned integer data value</span></span>
-   <span data-ttu-id="6bad5-109">DATA4: matrice di caratteri non firmati</span><span class="sxs-lookup"><span data-stu-id="6bad5-109">data4 - An array of unsigned characters</span></span>

## <a name="see-also"></a><span data-ttu-id="6bad5-110">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6bad5-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bad5-111">Modelli</span><span class="sxs-lookup"><span data-stu-id="6bad5-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 




---
title: Tipi semplici
description: Tutti i tipi semplici sono rappresentati da un singolo carattere di formato che indica il tipo in base al nome.
ms.assetid: 77c293a1-70c4-4825-bb2e-de36e01d3abb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afe123ca7c06a0522a139dc0cca8a9e24d1d585d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712745"
---
# <a name="simple-types"></a>Tipi semplici

Tutti i tipi semplici sono rappresentati da un singolo carattere di formato che indica il tipo in base al nome. Sono inclusi tutti i tipi numerici e altri tipi IDL speciali. L'elenco è il seguente:

``` syntax
FC_BYTE,                    // 0x01
FC_CHAR,                    // 0x02
FC_SMALL,                   // 0x03
FC_USMALL,                  // 0x04
FC_WCHAR,                   // 0x05
FC_SHORT,                   // 0x06
FC_USHORT,                  // 0x07
FC_LONG,                    // 0x08
FC_ULONG,                   // 0x09
FC_FLOAT,                   // 0x0a
FC_HYPER,                   // 0x0b
FC_DOUBLE,                  // 0x0c
FC_ENUM16,                  // 0x0d
FC_ENUM32,                  // 0x0e
FC_ERROR_STATUS_T,          // 0x10
FC_INT3264,                 // 0xb8
FC_UINT3264,                // 0xb9
```

I tipi SMALL, WCHAR, HYPER, ERROR \_ status \_ T, \_ \_ INT3264 sono intrinseci MIDL con interpretazioni RPC speciali. I tipi INT e \_ \_ Int32 vengono mappati a FC \_ Long, unsigned int e unsigned \_ \_ Int32 map to FC \_ ULong, \_ \_ Int64 e unsigned \_ \_ Int64 map to FC \_ Hyper.

I \_ \_ tipi INT128, FLOAT128 e FLOAT80 non sono supportati.

 

 





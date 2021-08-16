---
title: Tipi semplici
description: Tutti i tipi semplici sono rappresentati da un singolo carattere di formato che indica il tipo in base al nome.
ms.assetid: 77c293a1-70c4-4825-bb2e-de36e01d3abb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e265c24d1eaf4b85ab67c7f8997c656257522bfc8290e73596a8628bdd4215c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925161"
---
# <a name="simple-types"></a>Tipi semplici

Tutti i tipi semplici sono rappresentati da un singolo carattere di formato che indica il tipo in base al nome. Sono inclusi tutti i tipi numerici e alcuni altri tipi IDL speciali. L'elenco è il seguente:

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

I tipi SMALL, WCHAR, HYPER, ERROR \_ STATUS \_ T, \_ \_ INT3264 sono intrinseci MIDL con interpretazioni RPC speciali. I tipi INT e INT32 eseguono il mapping a \_ \_ FC \_ LONG, unsigned INT e unsigned \_ \_ INT32 a FC \_ ULONG, \_ \_ INT64 e UNsigned \_ \_ INT64 a FC \_ HYPER.

I \_ \_ tipi INT128, FLOAT128 e FLOAT80 non sono supportati.

 

 





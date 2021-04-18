---
description: Allocatore di memoria
ms.assetid: 2dc055a2-b77a-443d-b602-d9636cbe4db3
title: Allocatore di memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be12e25886eda968a00b10386a6eac3fd36e7279
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522202"
---
# <a name="memory-allocator"></a>Allocatore di memoria

L'oggetto allocatore di memoria alloca i buffer per gli esempi di supporti. I filtri possono utilizzare questo oggetto per allocare buffer di memoria condivisi. Tuttavia, un filtro con requisiti speciali può implementare anche il proprio oggetto allocatore di memoria. Creare questo oggetto chiamando **CoCreateInstance**.



|                  |                                        |
|------------------|----------------------------------------|
| Identificatore di classe | \_MEMORYALLOCATOR CLSID                 |
| Interfacce       | [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti DirectShow](directshow-objects.md)
</dt> </dl>

 

 




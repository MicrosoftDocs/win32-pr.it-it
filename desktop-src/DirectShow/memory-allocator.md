---
description: Allocatore di memoria
ms.assetid: 2dc055a2-b77a-443d-b602-d9636cbe4db3
title: Allocatore di memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2412adb78be18ac8c14eb4706624424f97ff13
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909420"
---
# <a name="memory-allocator"></a>Allocatore di memoria

L'oggetto allocatore di memoria alloca buffer per campioni di supporti. I filtri possono usare questo oggetto per allocare buffer di memoria condivisa. Tuttavia, un filtro con requisiti speciali può anche implementare il proprio oggetto allocatore di memoria. Creare questo oggetto chiamando **CoCreateInstance.**



| Label | Valore |
|------------------|----------------------------------------|
| Identificatore di classe | CLSID \_ MemoryAllocator                 |
| Interfacce       | [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Objects](directshow-objects.md)
</dt> </dl>

 

 




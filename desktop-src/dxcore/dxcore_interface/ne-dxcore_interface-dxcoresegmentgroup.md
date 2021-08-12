---
title: DXCoreSegmentGroup
description: Definisce le costanti che specificano il raggruppamento dei segmenti di memoria di un adattatore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 2474f8084035ddb67f7081ea45cd1d1743c053415a7bbade68ecff3d4527636c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279623"
---
# <a name="dxcoresegmentgroup-enum"></a>Enumerazione DXCoreSegmentGroup

Definisce le costanti che specificano il raggruppamento dei segmenti di memoria di un adattatore.

## <a name="syntax"></a>Sintassi

```cpp
enum class DXCoreSegmentGroup : uint32_t
{
  Local = 0,
  NonLocal = 1
};
```

## <a name="constants"></a>Costanti

### <a name="local"></a>Locale

Specifica un raggruppamento di segmenti che viene considerato locale per la scheda e rappresenta la memoria più veloce disponibile per la GPU. L'applicazione deve avere come destinazione il gruppo di segmenti locale come dimensione di destinazione per il working set.

### <a name="nonlocal"></a>Non locale

Specifica un raggruppamento di segmenti che viene considerato non locale per l'adapter e può avere prestazioni più lente rispetto al gruppo di segmenti locale.

## <a name="see-also"></a>Vedi anche

[Riferimento DXCore](../dxcore-reference.md), [Uso di DXCore per enumerare gli adattatori](../dxcore-enum-adapters.md)
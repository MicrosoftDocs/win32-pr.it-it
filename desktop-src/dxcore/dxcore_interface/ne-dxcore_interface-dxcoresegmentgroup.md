---
title: DXCoreSegmentGroup
description: Definisce le costanti che specificano il raggruppamento del segmento di memoria di un adapter.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: ce94d5f806879ea84f64c88d3a62b074a5c5415b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299996"
---
# <a name="dxcoresegmentgroup-enum"></a>Enumerazione DXCoreSegmentGroup

Definisce le costanti che specificano il raggruppamento del segmento di memoria di un adapter.

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

Specifica un raggruppamento di segmenti considerati locali per l'adapter e rappresenta la memoria più veloce disponibile per la GPU. L'applicazione deve essere destinata al gruppo di segmenti locale come dimensione di destinazione per la relativa working set.

### <a name="nonlocal"></a>Non locali

Specifica un raggruppamento di segmenti considerati non locali per l'adapter e può avere prestazioni più lente rispetto al gruppo di segmenti locale.

## <a name="see-also"></a>Vedi anche

Guida di [riferimento a DXCore](../dxcore-reference.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)
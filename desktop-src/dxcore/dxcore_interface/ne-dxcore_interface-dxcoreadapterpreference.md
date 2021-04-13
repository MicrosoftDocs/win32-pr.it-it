---
title: DXCoreAdapterPreference
description: Definisce le costanti che specificano le preferenze della scheda DXCore da usare come criteri di ordinamento degli elenchi.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 4301bdc1fe0ece8d9594ec3287e2ea8ddcce8f0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399453"
---
# <a name="dxcoreadapterpreference-enum"></a>Enumerazione DXCoreAdapterPreference

## <a name="description"></a>Descrizione

Definisce le costanti che specificano le preferenze della scheda DXCore da usare come criteri di ordinamento degli elenchi. È possibile ordinare un elenco di adapter DXCore passando una matrice di **DXCoreAdapterPreference** a [IDXCoreAdapterList:: Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).

## <a name="syntax"></a>Sintassi

```cpp
enum class DXCoreAdapterPreference : uint32_t
{
  Hardware = 0,
  MinimumPower = 1,
  HighPerformance = 2
};
```

## <a name="enum-fields"></a>Campi enum

### <a name="hardware"></a>Hardware

Specifica una preferenza per le schede hardware (anziché le schede software).

### <a name="minimumpower"></a>MinimumPower

Specifica una preferenza per la GPU a consumo minimo (ad esempio un processore grafico integrato o iGPU).

### <a name="highperformance"></a>HighPerformance

Specifica una preferenza per la GPU con prestazioni più elevate, ad esempio un processore di grafica esterno (xGPU), se disponibile, o dGPU (Discrete Graphics Processor), se disponibile.

## <a name="see-also"></a>Vedi anche

Riferimento a [IDXCoreAdapterList:: Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md), [DXCore](../dxcore-reference.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)
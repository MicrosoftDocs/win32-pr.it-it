---
title: DXCoreAdapterPreference
description: Definisce costanti che specificano le preferenze dell'adapter DXCore da usare come criteri di ordinamento degli elenchi.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: a58f2c948751d5217a89e52bc862057ac6a67c85bdf2fabed96c2b5ad68364cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117731"
---
# <a name="dxcoreadapterpreference-enum"></a>Enumerazione DXCoreAdapterPreference

## <a name="description"></a>Descrizione

Definisce costanti che specificano le preferenze dell'adapter DXCore da usare come criteri di ordinamento degli elenchi. È possibile ordinare un elenco di adattatori DXCore passando una matrice **di DXCoreAdapterPreference** a [IDXCoreAdapterList::Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).

## <a name="syntax"></a>Sintassi

```cpp
enum class DXCoreAdapterPreference : uint32_t
{
  Hardware = 0,
  MinimumPower = 1,
  HighPerformance = 2
};
```

## <a name="enum-fields"></a>Campi di enumerazione

### <a name="hardware"></a>Hardware

Specifica una preferenza per le schede hardware (anziché per le schede software).

### <a name="minimumpower"></a>MinimumPower

Specifica una preferenza per la GPU con alimentazione minima, ad esempio un processore di grafica integrato o iGPU.

### <a name="highperformance"></a>HighPerformance

Specifica una preferenza per la GPU con prestazioni più elevate, ad esempio un processore di grafica esterno (xGPU), se disponibile, o dGPU (Discrete Graphics Processor), se disponibile.

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapterList::Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md), [Riferimento DXCore](../dxcore-reference.md), [Uso di DXCore per enumerare gli adattatori](../dxcore-enum-adapters.md)
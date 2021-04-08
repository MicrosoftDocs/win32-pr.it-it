---
title: IDXCoreAdapterList::IsAdapterPreferenceSupported
description: Determina se un valore [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) specificato viene riconosciuto dal sistema operativo.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 1678568eb17c0dd833c130e6184931c8896261e9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728039"
---
# <a name="idxcoreadapterlistisadapterpreferencesupported-method"></a>Metodo IDXCoreAdapterList:: IsAdapterPreferenceSupported

## <a name="description"></a>Descrizione

Determina se un valore [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) specificato viene riconosciuto dal sistema operativo corrente. È possibile chiamare **IsAdapterPreferenceSupported** prima di chiamare [IDXCoreAdapterList:: Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).

## <a name="syntax"></a>Sintassi

```cpp
bool IsAdapterPreferenceSupported(
  DXCoreAdapterPreference preference
);
```

## <a name="parameters"></a>Parametri

### <a name="preference"></a>preference

Tipo: **[DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md)**

Valore [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) che verrà controllato per verificare se è supportato dal sistema operativo.

## <a name="returns"></a>Restituisce

Tipo: **bool**

Restituisce `true` se il tipo di ordinamento viene riconosciuto dal sistema operativo corrente. In caso contrario, restituisce `false`.

## <a name="see-also"></a>Vedi anche

Guida di [riferimento](../dxcore-reference.md)a [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), DXCore, [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)
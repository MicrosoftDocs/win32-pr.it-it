---
title: IDXCoreAdapterList::IsAdapterPreferenceSupported
description: Determina se un [valore DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) specificato viene compreso dal sistema operativo.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: f8a42040ecd6c5667a3d33fb506fd97cfdfe53e8950c2e42b6068bbed6c19467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118502582"
---
# <a name="idxcoreadapterlistisadapterpreferencesupported-method"></a>Metodo IDXCoreAdapterList::IsAdapterPreferenceSupported

## <a name="description"></a>Descrizione

Determina se un [valore DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) specificato viene compreso dal sistema operativo corrente. È possibile chiamare **IsAdapterPreferenceSupported prima** di chiamare [IDXCoreAdapterList::Sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).

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

Restituisce `true` se il tipo di ordinamento è compreso dal sistema operativo corrente. In caso contrario, restituisce `false`.

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [Riferimento DXCore](../dxcore-reference.md), [Uso di DXCore per enumerare gli adattatori](../dxcore-enum-adapters.md)
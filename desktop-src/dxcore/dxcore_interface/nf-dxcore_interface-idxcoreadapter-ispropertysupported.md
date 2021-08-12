---
title: IDXCoreAdapter::IsPropertySupported
description: Determina se questo oggetto adattatore DXCore e il sistema operativo corrente supportano la proprietà dell'adapter specificata.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: ddee6bea5af8fb64dfa2bfc15392e92239e7326b34cbd93cbd112559a6027912
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279232"
---
# <a name="idxcoreadapterispropertysupported-method"></a>Metodo IDXCoreAdapter::IsPropertySupported

Determina se questo oggetto adattatore DXCore e il sistema operativo corrente supportano la proprietà dell'adapter specificata.

## <a name="syntax"></a>Sintassi

```cpp
virtual bool STDMETHODCALLTYPE IsPropertySupported( 
  DXCoreAdapterProperty property) = 0;
```

## <a name="parameters"></a>Parametri

### <a name="property"></a>proprietà

Tipo: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**

Tipo di proprietà per cui si esegue una query sul supporto. Per altre informazioni su ogni proprietà dell'adapter, vedere la tabella in [DXCoreAdapterProperty.](./ne-dxcore_interface-dxcoreadapterproperty.md)

## <a name="returns"></a>Restituisce

Tipo: **bool**

Restituisce `true` se questo oggetto adapter DXCore e il sistema operativo corrente supportano la proprietà dell'adapter specificata. In caso contrario, restituisce `false`.

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [Riferimento DXCore](../dxcore-reference.md), GUID degli attributi dell'adattatore [DXCore](../dxcore-adapter-attribute-guids.md), [Uso di DXCore per enumerare gli adattatori](../dxcore-enum-adapters.md)
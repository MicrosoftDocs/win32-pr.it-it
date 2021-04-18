---
title: IDXCoreAdapter::IsPropertySupported
description: Determina se questo oggetto adapter DXCore e il sistema operativo corrente supportano la proprietà dell'adapter specificata.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: b960d96515d4aee85520a6def70a8f0e9349e131
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300218"
---
# <a name="idxcoreadapterispropertysupported-method"></a>Metodo IDXCoreAdapter:: IsPropertySupported

Determina se questo oggetto adapter DXCore e il sistema operativo corrente supportano la proprietà dell'adapter specificata.

## <a name="syntax"></a>Sintassi

```cpp
virtual bool STDMETHODCALLTYPE IsPropertySupported( 
  DXCoreAdapterProperty property) = 0;
```

## <a name="parameters"></a>Parametri

### <a name="property"></a>proprietà

Tipo: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**

Tipo di proprietà su cui si sta eseguendo una query sul supporto per. Per ulteriori informazioni su ogni proprietà dell'adapter, vedere la tabella in [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) .

## <a name="returns"></a>Restituisce

Tipo: **bool**

Restituisce  `true`   se l'oggetto adattatore DXCore e il sistema operativo corrente supportano la proprietà dell'adapter specificata. In caso contrario, restituisce  `false` .

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [riferimento a DXCore](../dxcore-reference.md), [GUID dell'attributo della scheda DXCore](../dxcore-adapter-attribute-guids.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)
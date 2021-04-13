---
title: IDXCoreAdapter::IsSetStateSupported
description: Determina se questo oggetto adattatore DXCore e il sistema operativo corrente supportano l'impostazione del valore dello stato dell'adapter specificato.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 284e38a622c882fce04278d9134908f55c9a25cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399452"
---
# <a name="idxcoreadapterissetstatesupported-method"></a>Metodo IDXCoreAdapter:: IsSetStateSupported

Determina se questo oggetto adattatore DXCore e il sistema operativo corrente supportano l'impostazione del valore dello stato dell'adapter specificato.

## <a name="syntax"></a>Sintassi

```cpp
virtual bool STDMETHODCALLTYPE IsSetStateSupported( 
  DXCoreAdapterState property) = 0;
```

## <a name="parameters"></a>Parametri

### <a name="state"></a>state

Tipo: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**

Tipo di elemento di stato su cui si sta eseguendo una query sul supporto per. Per ulteriori informazioni su ogni tipo di stato dell'adapter, vedere la tabella in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) .

## <a name="returns"></a>Restituisce

Tipo: **bool**

Restituisce  `true`   se l'oggetto adattatore DXCore e il sistema operativo corrente (sistema operativo) supportano l'impostazione dello stato dell'adapter specificato. In caso contrario, restituisce  `false` .

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [riferimento a DXCore](../dxcore-reference.md), [GUID dell'attributo della scheda DXCore](../dxcore-adapter-attribute-guids.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)
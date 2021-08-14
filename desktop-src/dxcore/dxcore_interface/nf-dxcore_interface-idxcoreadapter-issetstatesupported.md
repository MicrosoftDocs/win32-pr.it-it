---
title: IDXCoreAdapter::IsSetStateSupported
description: Determina se questo oggetto adattatore DXCore e il sistema operativo corrente supportano l'impostazione del valore dello stato dell'adattatore specificato.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: dc63b541a552f1b01792e9f503acc7aeee03ce5ac6cc92e7b70e271ae62a50ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118278979"
---
# <a name="idxcoreadapterissetstatesupported-method"></a>Metodo IDXCoreAdapter::IsSetStateSupported

Determina se questo oggetto adattatore DXCore e il sistema operativo corrente supportano l'impostazione del valore dello stato dell'adattatore specificato.

## <a name="syntax"></a>Sintassi

```cpp
virtual bool STDMETHODCALLTYPE IsSetStateSupported( 
  DXCoreAdapterState property) = 0;
```

## <a name="parameters"></a>Parametri

### <a name="state"></a>state

Tipo: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**

Tipo di elemento di stato per cui si esegue una query sul supporto. Vedere la tabella in [DXCoreAdapterState per](./ne-dxcore_interface-dxcoreadapterstate.md) altre informazioni su ogni tipo di stato dell'adapter.

## <a name="returns"></a>Restituisce

Tipo: **bool**

Restituisce se questo oggetto adattatore DXCore e il sistema operativo `true` corrente supportano l'impostazione dello stato della scheda specificato. In caso contrario, restituisce `false`.

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [Riferimento DXCore](../dxcore-reference.md), GUID degli attributi dell'adapter [DXCore](../dxcore-adapter-attribute-guids.md), [Uso di DXCore per enumerare gli adattatori](../dxcore-enum-adapters.md)
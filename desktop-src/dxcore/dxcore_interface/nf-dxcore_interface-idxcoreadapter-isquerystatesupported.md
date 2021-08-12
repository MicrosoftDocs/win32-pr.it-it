---
title: IDXCoreAdapter::IsQueryStateSupported
description: Determina se questo oggetto adattatore DXCore e il sistema operativo corrente supportano l'esecuzione di query sul valore dello stato dell'adattatore specificato.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 8ae77c308cb251982947d91e23eaef8f6d828c1233df442cb013bf9737e3c57d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279222"
---
# <a name="idxcoreadapterisquerystatesupported-method"></a>Metodo IDXCoreAdapter::IsQueryStateSupported

Determina se questo oggetto adattatore DXCore e il sistema operativo corrente supportano l'esecuzione di query sul valore dello stato dell'adattatore specificato.

## <a name="syntax"></a>Sintassi

```cpp
virtual bool STDMETHODCALLTYPE IsQueryStateSupported( 
  DXCoreAdapterState property) = 0;
```

## <a name="parameters"></a>Parametri

### <a name="state"></a>state

Tipo: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**

Tipo di elemento di stato per cui si esegue una query sul supporto. Vedere la tabella in [DXCoreAdapterState per](./ne-dxcore_interface-dxcoreadapterstate.md) altre informazioni su ogni tipo di stato dell'adapter.

## <a name="returns"></a>Restituisce

Tipo: **bool**

Restituisce se questo oggetto adattatore DXCore e il sistema operativo corrente supportano `true` l'esecuzione di query sullo stato dell'adattatore specificato. In caso contrario, restituisce `false`.

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [Riferimento DXCore](../dxcore-reference.md), GUID degli attributi dell'adapter [DXCore](../dxcore-adapter-attribute-guids.md), [Uso di DXCore per enumerare gli adattatori](../dxcore-enum-adapters.md)
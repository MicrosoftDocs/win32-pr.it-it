---
title: IDXCoreAdapter::IsQueryStateSupported
description: Determina se questo oggetto adapter DXCore e il sistema operativo corrente supportano l'esecuzione di query sul valore dello stato dell'adapter specificato.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: d154597f9b3ddbec24cff230317d881b9595bcde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118151"
---
# <a name="idxcoreadapterisquerystatesupported-method"></a>Metodo IDXCoreAdapter:: IsQueryStateSupported

Determina se questo oggetto adapter DXCore e il sistema operativo corrente supportano l'esecuzione di query sul valore dello stato dell'adapter specificato.

## <a name="syntax"></a>Sintassi

```cpp
virtual bool STDMETHODCALLTYPE IsQueryStateSupported( 
  DXCoreAdapterState property) = 0;
```

## <a name="parameters"></a>Parametri

### <a name="state"></a>state

Tipo: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**

Tipo di elemento di stato su cui si sta eseguendo una query sul supporto per. Per ulteriori informazioni su ogni tipo di stato dell'adapter, vedere la tabella in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) .

## <a name="returns"></a>Restituisce

Tipo: **bool**

Restituisce  `true`   se l'oggetto adattatore DXCore e il sistema operativo corrente supportano l'esecuzione di query sullo stato dell'adapter specificato. In caso contrario, restituisce  `false` .

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [riferimento a DXCore](../dxcore-reference.md), [GUID dell'attributo della scheda DXCore](../dxcore-adapter-attribute-guids.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)
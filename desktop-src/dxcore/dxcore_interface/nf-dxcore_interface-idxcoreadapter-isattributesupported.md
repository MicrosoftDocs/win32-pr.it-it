---
title: IDXCoreAdapter::IsAttributeSupported
description: Determina se questo oggetto adattatore DXCore supporta l'attributo dell'adattatore specificato.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 9dda05ca9dc1d3b7a7a84792c7ac122bb64144d5fdba3ad630be1a3f4d9ddf24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787081"
---
# <a name="idxcoreadapterisattributesupported-method"></a>Metodo IDXCoreAdapter::IsAttributeSupported

Determina se questo oggetto adattatore DXCore supporta l'attributo dell'adattatore specificato.

## <a name="syntax"></a>Sintassi

```cpp
virtual bool STDMETHODCALLTYPE IsAttributeSupported( 
  REFGUID attributeGUID) = 0;
```

## <a name="parameters"></a>Parametri

### <a name="attributeguid"></a>attributeGUID

Tipo: **REFGUID**

Riferimento a un GUID dell'attributo dell'adapter. Per un elenco di GUID di attributo, vedere GUID degli attributi [dell'adapter DXCore.](../dxcore-adapter-attribute-guids.md)

## <a name="returns"></a>Restituisce

Tipo: **bool**

Restituisce `true` se questo oggetto adattatore DXCore supporta l'attributo dell'adattatore specificato. In caso contrario, restituisce `false`.

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [Riferimento DXCore](../dxcore-reference.md), GUID degli attributi dell'adapter [DXCore](../dxcore-adapter-attribute-guids.md), [Uso di DXCore per enumerare gli adattatori](../dxcore-enum-adapters.md)
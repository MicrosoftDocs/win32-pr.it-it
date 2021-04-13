---
title: IDXCoreAdapter::IsAttributeSupported
description: Determina se questo oggetto adapter DXCore supporta l'attributo dell'adattatore specificato.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 9824595326f9e81bfa21ab198a3f5b2e6eae74bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399169"
---
# <a name="idxcoreadapterisattributesupported-method"></a>Metodo IDXCoreAdapter:: IsAttributeSupported

Determina se questo oggetto adapter DXCore supporta l'attributo dell'adattatore specificato.

## <a name="syntax"></a>Sintassi

```cpp
virtual bool STDMETHODCALLTYPE IsAttributeSupported( 
  REFGUID attributeGUID) = 0;
```

## <a name="parameters"></a>Parametri

### <a name="attributeguid"></a>attributeGUID

Tipo: **REFGUID**

Riferimento a un GUID dell'attributo dell'adapter. Per un elenco di GUID di attributo, vedere i [GUID dell'attributo della scheda DXCore](../dxcore-adapter-attribute-guids.md).

## <a name="returns"></a>Restituisce

Tipo: **bool**

Restituisce  `true`   se l'oggetto adattatore DXCore supporta l'attributo dell'adattatore specificato. In caso contrario, restituisce  `false` .

## <a name="see-also"></a>Vedi anche

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [riferimento a DXCore](../dxcore-reference.md), [GUID dell'attributo della scheda DXCore](../dxcore-adapter-attribute-guids.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)
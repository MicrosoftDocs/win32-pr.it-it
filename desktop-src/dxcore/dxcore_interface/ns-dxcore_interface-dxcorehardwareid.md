---
title: DXCoreHardwareID
description: Rappresenta le parti dell'ID hardware PnP per un adapter.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6882d9aa16bf72fb33f9a254a6434becb37f9cb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117882"
---
# <a name="dxcorehardwareid-structure"></a>Struttura DXCoreHardwareID

Rappresenta le parti dell'ID hardware PnP per un adapter.

## <a name="syntax"></a>Sintassi

```cpp
struct DXCoreHardwareID
{
  uint32_t vendorID;
  uint32_t deviceID;
  uint32_t subSysID;
  uint32_t revision;
};
```

## <a name="members"></a>Members

### <a name="vendorid"></a>vendorId

Tipo: **uint32_t \***

ID PCI del fornitore dell'hardware della scheda.

### <a name="deviceid"></a>deviceId

Tipo: **uint32_t \***

ID PCI del dispositivo hardware della scheda.

### <a name="subsysid"></a>subSysId

Tipo: **uint32_t \***

ID PCI del sottosistema hardware della scheda.

### <a name="revision"></a>revision

Tipo: **uint32_t \***

ID PCI del numero di revisione della scheda.

## <a name="see-also"></a>Vedi anche

Guida di [riferimento a DXCore](../dxcore-reference.md), [uso di DXCore per enumerare gli adapter](../dxcore-enum-adapters.md)
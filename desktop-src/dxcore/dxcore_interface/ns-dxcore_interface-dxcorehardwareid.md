---
title: DXCoreHardwareID
description: Rappresenta le parti ID hardware PnP per una scheda.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 68cdb130dd6f0c0338e5b94da2f68c58f98bb91d404871e18ac82e817881117c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118628"
---
# <a name="dxcorehardwareid-structure"></a>Struttura DXCoreHardwareID

Rappresenta le parti ID hardware PnP per una scheda.

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

ID PCI del numero di revisione dell'adattatore.

## <a name="see-also"></a>Vedi anche

[Riferimento DXCore](../dxcore-reference.md), [Uso di DXCore per enumerare gli adattatori](../dxcore-enum-adapters.md)
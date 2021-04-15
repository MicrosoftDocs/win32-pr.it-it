---
title: Proprietà ActiveBasicDevice PhysicalNetworkInterface (PlayToDevice. h)
description: Ottiene l'ID dell'interfaccia di rete fisica.
ms.assetid: F426462F-CE26-4EE1-B679-A4C80B2919A5
keywords:
- API di streaming multimediale della proprietà PhysicalNetworkInterface
- API di streaming multimediale della proprietà PhysicalNetworkInterface, interfaccia ActiveBasicDevice
- API di streaming multimediale dell'interfaccia ActiveBasicDevice, proprietà PhysicalNetworkInterface
topic_type:
- apiref
api_name:
- ActiveBasicDevice.PhysicalNetworkInterface
- ActiveBasicDevice.get_PhysicalNetworkInterface
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479618ed4d22a3d78a351fb88fcb1108a27c618f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477368"
---
# <a name="activebasicdevicephysicalnetworkinterface-property"></a>ActiveBasicDevice::P proprietà hysicalNetworkInterface

Ottiene l'ID dell'interfaccia di rete fisica.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_PhysicalNetworkInterface(
  [out] GUID *value
);
```



## <a name="property-value"></a>Valore proprietà

Puntatore a un **GUID** che specifica l'ID dell'interfaccia di rete fisica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>PlayToDevice. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>PlayToDevice. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 


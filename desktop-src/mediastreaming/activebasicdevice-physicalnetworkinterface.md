---
title: Proprietà ActiveBasicDevice PhysicalNetworkInterface (PlayToDevice.h)
description: Ottiene l'ID dell'interfaccia di rete fisica.
ms.assetid: F426462F-CE26-4EE1-B679-A4C80B2919A5
keywords:
- Proprietà PhysicalNetworkInterface API Streaming multimediale
- Proprietà PhysicalNetworkInterface API Streaming multimediale, interfaccia ActiveBasicDevice
- Interfaccia ActiveBasicDevice API Di streaming multimediale, proprietà PhysicalNetworkInterface
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
ms.openlocfilehash: 5bd9eb004607d93b92d502d22b253258bf39e501969e6b3952a58b0a03a1eec1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736207"
---
# <a name="activebasicdevicephysicalnetworkinterface-property"></a>Proprietà ActiveBasicDevice::P hysicalNetworkInterface

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
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows Server 2012 Solo \[ app desktop R2\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>PlayToDevice.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>PlayToDevice.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 


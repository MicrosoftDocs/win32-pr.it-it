---
title: Proprietà ActiveBasicDevice LogicalNetworkInterface (PlayToDevice.h)
description: Ottiene l'ID dell'interfaccia di rete logica.
ms.assetid: 47C2E0BE-D3E3-4A9F-9FC6-873882811506
keywords:
- Proprietà LogicalNetworkInterface API streaming multimediale
- Proprietà LogicalNetworkInterface API Streaming multimediale, interfaccia ActiveBasicDevice
- Interfaccia ActiveBasicDevice API Streaming multimediale, proprietà LogicalNetworkInterface
topic_type:
- apiref
api_name:
- ActiveBasicDevice.LogicalNetworkInterface
- ActiveBasicDevice.get_LogicalNetworkInterface
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41ee3e2b23a43e29daf2438cee517220f895ad601607dbdc6a61497f8ef1afa7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736387"
---
# <a name="activebasicdevicelogicalnetworkinterface-property"></a>Proprietà ActiveBasicDevice::LogicalNetworkInterface

Ottiene l'ID dell'interfaccia di rete logica.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_LogicalNetworkInterface(
  [out] GUID *value
);
```



## <a name="property-value"></a>Valore proprietà

Puntatore a un **GUID che** specifica l'ID dell'interfaccia di rete logica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows Server 2012 Solo app desktop R2 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>PlayToDevice.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>PlayToDevice.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 


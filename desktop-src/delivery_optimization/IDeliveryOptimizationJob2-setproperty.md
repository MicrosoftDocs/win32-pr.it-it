---
title: 'Metodo IDeliveryOptimizationJob2:: SetProperty'
description: Questo metodo non è utilizzato.
keywords:
- Metodo SetProperty
- Metodo SetProperty, interfaccia IDeliveryOptimizationJob2
- Interfaccia IDeliveryOptimizationJob2, metodo SetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 41375ac3949dd4bcbdd22944f1f1a11d461fc3ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400683"
---
# <a name="ideliveryoptimizationjob2setproperty-method"></a>Metodo IDeliveryOptimizationJob2:: SetProperty

Questo metodo non è utilizzato.

## <a name="syntax"></a>Sintassi

```C++
HRESULT SetProperty(
  [in]               DOJobPropertyId propId,
  [in, unique] const VARIANT         *propValue
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*propid* \[ in\]
</dt> <dd>

Non utilizzato.

</dd> <dt>

*PropValue* \[ in\]
</dt> <dd>

Non utilizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se propId è **DOJobPropertyId_ExtendedErrorInfo**, il valore restituito viene **DO_E_READ_ONLY_PROPERTY**. in caso contrario, la funzione restituisce **DO_E_UNKNOWN_PROPERTY_ID**.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|---------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato  | Solo app desktop Windows 10 versione 1803 \[\]                                   |
| Server minimo supportato  | Windows Server, versione 1709 \[ solo per le app desktop\]                               |
| Intestazione                    | Deliveryoptimization. h                                                           |
| IDL                       | DeliveryOptimization. idl                                                         |
| Libreria                   | Dosvc. lib                                                                        |
| DLL                       | Dosvc.dll                                                                        |
| IID                       | IID_IDeliveryOptimizationJob2 viene definito come 18995A26-BF59-4ABE-9F8B-D5092D5A2405 |

## <a name="see-also"></a>Vedi anche

[**IDeliveryOptimizationJob2**](ideliveryoptimizationjob2.md)

---
title: 'Metodo IDeliveryOptimizationJob2:: GetProperty'
description: Restituisce una singola proprietà del processo di esecuzione.
keywords:
- Metodo GetProperty
- Metodo GetProperty, interfaccia IDeliveryOptimizationJob2
- Interfaccia IDeliveryOptimizationJob2, metodo GetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 52e405685534c0dbae7c8c205dc5e114a3dbe68b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475934"
---
# <a name="ideliveryoptimizationjob2getproperty-method"></a>Metodo IDeliveryOptimizationJob2:: GetProperty

Questo metodo restituisce una singola proprietà del processo DO.

## <a name="syntax"></a>Sintassi

```C++
HRESULT GetProperty(
  [in]  DOJobPropertyId propId,
  [out] VARIANT         *propValue
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*propid* \[ in\]
</dt> <dd>

ID di proprietà obbligatorio da ottenere. È supportata solo **DOJobPropertyId_ExtendedErrorInfo** di tipo VT_BSTR.

</dd> <dt>

*PropValue* \[ out\]
</dt> <dd>

Valore della proprietà risultante, archiviato in un tipo VARIANT.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori HRESULT seguenti.

| Codice restituito                  | Descrizione          |
|------------------------------|----------------------|
| **S_OK**                     | Operazione riuscita              |
| **DO_E_UNKNOWN_PROPERTY_ID** | ID proprietà sconosciuto. |

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

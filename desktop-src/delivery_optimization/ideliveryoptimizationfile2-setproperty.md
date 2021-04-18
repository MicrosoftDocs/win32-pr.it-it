---
title: 'Metodo IDeliveryOptimizationFile2:: SetProperty'
description: 'Questo metodo restituisce una singola proprietà del file DO. | Metodo IDeliveryOptimizationFile2:: SetProperty'
keywords:
- Metodo SetProperty
- Metodo SetProperty, interfaccia IDeliveryOptimizationFile2
- Interfaccia IDeliveryOptimizationFile2, metodo SetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 74113fca944e79e9ecba8f822f73769775631821
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321671"
---
# <a name="ideliveryoptimizationfile2setproperty-method"></a>Metodo IDeliveryOptimizationFile2:: SetProperty

Questo metodo restituisce una singola proprietà del file DO.

## <a name="syntax"></a>Sintassi

```C++
HRESULT SetProperty(
  [in]               DOFilePropertyId propId,
  [in, unique] const VARIANT          *propValue
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*propid* \[ in\]
</dt> <dd>

ID di proprietà obbligatorio da impostare di tipo DOFilePropertyId.

</dd> <dt>

*PropValue* \[ in\]
</dt> <dd>

Valore della proprietà da impostare, di tipo VARIANT.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori HRESULT seguenti.

| Codice restituito                  | Descrizione                                                        |
|------------------------------|--------------------------------------------------------------------|
| **S_OK**                     | Operazione riuscita                                                            |
| **DO_E_UNKNOWN_PROPERTY_ID** | ID proprietà sconosciuto                                                |
| **DO_E_INVALID_STATE**       | Il processo non si trova attualmente in uno stato che consente l'impostazione di una proprietà |

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

[**IDeliveryOptimizationFile2**](ideliveryoptimizationfile2.md)

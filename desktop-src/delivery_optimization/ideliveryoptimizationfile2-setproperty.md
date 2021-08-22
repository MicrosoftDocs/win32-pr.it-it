---
title: Metodo IDeliveryOptimizationFile2::SetProperty
description: Questo metodo restituisce una singola proprietà del file DO. | Metodo IDeliveryOptimizationFile2::SetProperty
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
ms.openlocfilehash: 99ed42acb94f260e229abfe9df428aaa61d3658cb887892b84bb73fd6e7e63e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635721"
---
# <a name="ideliveryoptimizationfile2setproperty-method"></a>Metodo IDeliveryOptimizationFile2::SetProperty

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

*propId* \[ Pollici\]
</dt> <dd>

ID di proprietà richiesto per il set di tipo DOFilePropertyId.

</dd> <dt>

*propValue* \[ Pollici\]
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
| Client minimo supportato  | Windows 10, solo app desktop versione 1803 \[\]                                   |
| Server minimo supportato  | Windows Server, solo app desktop versione 1709 \[\]                               |
| Intestazione                    | Deliveryoptimization.h                                                           |
| Idl                       | DeliveryOptimization.idl                                                         |
| Libreria                   | Dosvc.lib                                                                        |
| DLL                       | Dosvc.dll                                                                        |
| IID                       | IID_IDeliveryOptimizationJob2 è definito come 18995A26-BF59-4ABE-9F8B-D5092D5A2405 |

## <a name="see-also"></a>Vedi anche

[**IDeliveryOptimizationFile2**](ideliveryoptimizationfile2.md)

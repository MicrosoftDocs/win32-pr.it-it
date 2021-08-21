---
title: Metodo IDeliveryOptimizationJob2::GetProperty
description: Restituisce una singola proprietà del processo DO.
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
ms.openlocfilehash: cdca86cb374eded0eabcc1d623d2218a6dc1f4cd5613a18e16b4ec9ab93156b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118811252"
---
# <a name="ideliveryoptimizationjob2getproperty-method"></a>Metodo IDeliveryOptimizationJob2::GetProperty

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

*propId* \[ Pollici\]
</dt> <dd>

ID di proprietà obbligatorio da ottenere. È **supportato DOJobPropertyId_ExtendedErrorInfo** solo un VT_BSTR di tipo .

</dd> <dt>

*propValue* \[ Cambio\]
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
| Client minimo supportato  | Windows 10, solo app desktop versione 1803 \[\]                                   |
| Server minimo supportato  | Windows Server, solo app desktop versione 1709 \[\]                               |
| Intestazione                    | Deliveryoptimization.h                                                           |
| Idl                       | DeliveryOptimization.idl                                                         |
| Libreria                   | Dosvc.lib                                                                        |
| DLL                       | Dosvc.dll                                                                        |
| IID                       | IID_IDeliveryOptimizationJob2 è definito come 18995A26-BF59-4ABE-9F8B-D5092D5A2405 |

## <a name="see-also"></a>Vedi anche

[**IDeliveryOptimizationJob2**](ideliveryoptimizationjob2.md)

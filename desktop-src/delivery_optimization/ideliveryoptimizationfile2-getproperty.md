---
title: Metodo IDeliveryOptimizationFile2::GetProperty
description: Questo metodo restituisce una singola proprietà del file DO. | Metodo IDeliveryOptimizationFile2::GetProperty
keywords:
- Metodo GetProperty
- Metodo GetProperty, interfaccia IDeliveryOptimizationFile2
- Interfaccia IDeliveryOptimizationFile2, metodo GetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d0f181eebe2aff8ccbbbf6d5400e3d5a78f123e2304567a413ecf4a35357229b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542091"
---
# <a name="ideliveryoptimizationfile2getproperty-method"></a>Metodo IDeliveryOptimizationFile2::GetProperty

Questo metodo restituisce una singola proprietà del file DO.

## <a name="syntax"></a>Sintassi

```C++
HRESULT GetProperty(
  [in]  DOFilePropertyId propId,
  [out] VARIANT          *propValue
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*propId* \[ Pollici\]
</dt> <dd>

ID proprietà obbligatorio da ottenere di tipo DOFilePropertyId.

</dd> <dt>

*propValue* \[ Cambio\]
</dt> <dd>

Valore della proprietà archiviato in un elemento VARIANT.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori HRESULT seguenti.

| Codice restituito                  | Descrizione                                         |
|------------------------------|-----------------------------------------------------|
| **S_OK**                     | Operazione riuscita                                             |
| **DO_E_UNKNOWN_PROPERTY_ID** | ID proprietà sconosciuto.                                |
| **DO_E_WRITE_ONLY_PROPERTY** | La proprietà è di sola scrittura e non può essere letta.      |
| **E_NOT_SET**                | Nessuna proprietà è stata impostata tramite il metodo SetProperty. |
| **E_OUTOFMEMORY**            |  Errore di allocazione della memoria                          |

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|---------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato  | Windows 10, solo app desktop versione 1803 \[\]                                   |
| Server minimo supportato  | Windows Server, solo app desktop versione 1709 \[\]                               |
| Intestazione                    | Deliveryoptimization.h                                                           |
| Idl                       | DeliveryOptimization.idl                                                         |
| Libreria                   | Dosvc.lib                                                                        |
| DLL                       | Dosvc.dll                                                                        |
| IID                       | IID_IDeliveryOptimizationJob2 definito come 18995A26-BF59-4ABE-9F8B-D5092D5A2405 |

## <a name="see-also"></a>Vedi anche

[**IDeliveryOptimizationFile2**](ideliveryoptimizationfile2.md)

---
title: 'Metodo IDeliveryOptimizationFile2:: GetProperty'
description: 'Questo metodo restituisce una singola proprietà del file DO. | Metodo IDeliveryOptimizationFile2:: GetProperty'
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
ms.openlocfilehash: c53167287cf821ceca26782dab9b8011d40a1785
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353726"
---
# <a name="ideliveryoptimizationfile2getproperty-method"></a>Metodo IDeliveryOptimizationFile2:: GetProperty

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

*propid* \[ in\]
</dt> <dd>

ID di proprietà obbligatorio da ottenere di tipo DOFilePropertyId.

</dd> <dt>

*PropValue* \[ out\]
</dt> <dd>

Valore della proprietà Archiviato in una variante.

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
| Client minimo supportato  | Solo app desktop Windows 10 versione 1803 \[\]                                   |
| Server minimo supportato  | Windows Server, versione 1709 \[ solo per le app desktop\]                               |
| Intestazione                    | Deliveryoptimization. h                                                           |
| IDL                       | DeliveryOptimization. idl                                                         |
| Libreria                   | Dosvc. lib                                                                        |
| DLL                       | Dosvc.dll                                                                        |
| IID                       | IID_IDeliveryOptimizationJob2 viene definito come 18995A26-BF59-4ABE-9F8B-D5092D5A2405 |

## <a name="see-also"></a>Vedi anche

[**IDeliveryOptimizationFile2**](ideliveryoptimizationfile2.md)

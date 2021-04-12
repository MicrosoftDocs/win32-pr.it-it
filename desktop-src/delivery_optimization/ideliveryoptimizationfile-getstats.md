---
title: Metodo GetStats di IDeliveryOptimizationFile (Deliveryoptimization. h)
description: Restituisce le statistiche di download e caricamento per un file specifico.
ms.assetid: 8A3AD658-F1AD-4EA5-B010-AB7B88126FD6
keywords:
- GetStats (metodo)
- Metodo GetStats, interfaccia IDeliveryOptimizationFile
- Interfaccia IDeliveryOptimizationFile, Metodo GetStats
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile.GetStats
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 08c5cff0672130049c325a00cb63c8dbc5c2e8ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400839"
---
# <a name="ideliveryoptimizationfilegetstats-method"></a>Metodo IDeliveryOptimizationFile:: GetStats

Restituisce le statistiche di download e caricamento per un file specifico.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetStats(
  [out] DOSwarmStats *swarmStats
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*swarmStats* \[ out\]
</dt> <dd>

Restituisce le statistiche di download e caricamento per un file specifico. Per informazioni dettagliate, vedere la struttura [**DOSwarmStats**](doswarmstats.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo deve restituire **S_OK**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationFile viene definito come B76B9699-E99E-4101-803F-A20E325D93E2<br/>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDeliveryOptimizationFile**](ideliveryoptimizationfile.md)
</dt> </dl>

 

 






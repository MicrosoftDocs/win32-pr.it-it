---
title: Metodo GetStats IDeliveryOptimizationFile (Deliveryoptimization.h)
description: Restituisce le statistiche di download e caricamento per un file specifico.
ms.assetid: 8A3AD658-F1AD-4EA5-B010-AB7B88126FD6
keywords:
- GetStats (metodo)
- Metodo GetStats, interfaccia IDeliveryOptimizationFile
- Interfaccia IDeliveryOptimizationFile, metodo GetStats
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
ms.openlocfilehash: f4e2f0a3b680e682944740cb570bfb4889b22ba8e7ec56d3aefc9e34fcdd6a37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635761"
---
# <a name="ideliveryoptimizationfilegetstats-method"></a>Metodo IDeliveryOptimizationFile::GetStats

Restituisce le statistiche di download e caricamento per un file specifico.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetStats(
  [out] DOSwarmStats *swarmStats
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*swarmStats* \[ Cambio\]
</dt> <dd>

Restituisce le statistiche di download e caricamento per un file specifico. Per informazioni [**dettagliate, vedere la struttura DOSwarmStats.**](doswarmstats.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo deve restituire **S_OK**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationFile è definito come B76B9699-E99E-4101-803F-A20E325D93E2<br/>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDeliveryOptimizationFile**](ideliveryoptimizationfile.md)
</dt> </dl>

 

 






---
description: Reimposta lo stato di integrità per tutte le applicazioni in una macchina virtuale.
ms.assetid: DB0B2FB3-87EB-44B2-9C4E-849BCE594E89
title: Metodo IVmApplicationHealthMonitor::ResetAllApplicationState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor.ResetAllApplicationState
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 4e97d5d16200501d77acf8b0b02cc5562d51706fcc46298421ad7f7e8fc0dfac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694351"
---
# <a name="ivmapplicationhealthmonitorresetallapplicationstate-method"></a>Metodo IVmApplicationHealthMonitor::ResetAllApplicationState

Reimposta lo stato di integrità per tutte le applicazioni in una macchina virtuale. In caso di esito positivo, lo stato di integrità per tutte le applicazioni monitorate verrà impostato su **ApplicationStateHealthy.**

## <a name="syntax"></a>Sintassi


```C++
HRESULT ResetAllApplicationState();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Per usare questo elemento di programmazione, Windows 8 componenti di integrazione devono essere installati nella macchina virtuale in cui è in esecuzione l'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                                |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                      |
| Versione<br/>                  | Componenti di integrazione per Windows 8<br/>                                                           |
| Idl<br/>                      | <dl> <dt>VmApplicationHealthMonitor.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVmApplicationHealthMonitor**](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 





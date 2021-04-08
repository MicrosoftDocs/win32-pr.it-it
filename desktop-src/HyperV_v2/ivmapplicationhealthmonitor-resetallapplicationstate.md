---
description: Reimposta lo stato di integrità di tutte le applicazioni in una macchina virtuale.
ms.assetid: DB0B2FB3-87EB-44B2-9C4E-849BCE594E89
title: 'Metodo IVmApplicationHealthMonitor:: ResetAllApplicationState'
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
ms.openlocfilehash: b13781d26c256e41ea6685b19a3097236ebbdb91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880210"
---
# <a name="ivmapplicationhealthmonitorresetallapplicationstate-method"></a>Metodo IVmApplicationHealthMonitor:: ResetAllApplicationState

Reimposta lo stato di integrità di tutte le applicazioni in una macchina virtuale. In caso di esito positivo, lo stato di integrità di tutte le applicazioni monitorate verrà impostato su **ApplicationStateHealthy**.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ResetAllApplicationState();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Per utilizzare questo elemento di programmazione, è necessario installare i componenti di integrazione di Windows 8 nella macchina virtuale in cui è in esecuzione l'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                                |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                      |
| Versione<br/>                  | Componenti di integrazione per Windows 8<br/>                                                           |
| IDL<br/>                      | <dl> <dt>VmApplicationHealthMonitor. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVmApplicationHealthMonitor**](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 





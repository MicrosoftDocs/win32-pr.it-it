---
description: Specifica lo stato di integrità di un'applicazione.
ms.assetid: CA06AA34-A549-4CFC-9B52-D2E0B200C3E9
title: APPLICATION_STATE enumerazione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- APPLICATION_STATE
api_type:
- IDLDef
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 5f873e7a30a4cff6dc4cc89eaea225201a367f7c24ead11ad95da04c2ff1ab32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914161"
---
# <a name="application_state-enumeration"></a>Enumerazione APPLICATION \_ STATE

Specifica lo stato di integrità di un'applicazione.

## <a name="syntax"></a>Sintassi


```C++
typedef enum _APPLICATION_STATE { 
  ApplicationStateHealthy   = 0,
  ApplicationStateCritical
} APPLICATION_STATE, *PAPPLICATION_STATE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="ApplicationStateHealthy"></span><span id="applicationstatehealthy"></span><span id="APPLICATIONSTATEHEALTHY"></span>**ApplicationStateHealthy**
</dt> <dd>

Lo stato dell'applicazione è integro.

</dd> <dt>

<span id="ApplicationStateCritical"></span><span id="applicationstatecritical"></span><span id="APPLICATIONSTATECRITICAL"></span>**ApplicationStateCritical**
</dt> <dd>

Lo stato dell'applicazione è critico.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per usare questo elemento di programmazione, è necessario Windows 8 componenti di integrazione di nella macchina virtuale in cui è in esecuzione l'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                                |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                      |
| Versione<br/>                  | Componenti di integrazione per Windows 8<br/>                                                           |
| Idl<br/>                      | <dl> <dt>VmApplicationHealthMonitor.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SetApplicationState**](ivmapplicationhealthmonitor-setapplicationstate.md)
</dt> </dl>

 

 





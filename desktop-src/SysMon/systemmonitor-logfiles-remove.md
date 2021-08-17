---
title: Metodo LogFiles.Remove
description: Rimuove l'istanza di LogFileItem specificata dalla raccolta.
ms.assetid: d2885ffd-5957-472c-9a67-2f1469d9b48b
keywords:
- Metodo Remove SysMon
- Metodo Remove SysMon , classe LogFiles
- Metodo SysMon , Remove della classe LogFiles
topic_type:
- apiref
api_name:
- LogFiles.Remove
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c12c0bae91df3baf421638665a5587612e6d1404c3300cf02b0308b7bef7d016
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117955435"
---
# <a name="logfilesremove-method"></a>Metodo LogFiles.Remove

Rimuove [**l'istanza di LogFileItem**](logfileitem.md) specificata dalla raccolta.

## <a name="syntax"></a>Sintassi


```VB
LogFiles.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*index* \[ Pollici\]
</dt> <dd>

Indice intero del file di log da rimuovere dalla raccolta. L'indice è in base uno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

**Prima di Windows Vista:** Non è possibile rimuovere i file di log dalla raccolta [**di file**](systemmonitor-logfiles.md) di log se il valore di [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) è impostato su sysmonLogFiles.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[LogFiles](logfiles.md)
</dt> <dt>

[**LogFileItem**](logfileitem.md)
</dt> <dt>

[**LogFiles**](systemmonitor-logfiles.md)
</dt> </dl>

 

 






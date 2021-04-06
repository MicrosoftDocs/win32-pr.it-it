---
title: LogFiles. Remove (metodo)
description: Rimuove l'istanza di LogFileItem specificata dalla raccolta.
ms.assetid: d2885ffd-5957-472c-9a67-2f1469d9b48b
keywords:
- Rimuovere il metodo SysMon
- Metodo Remove SysMon, classe LogFiles
- Classe LogFiles SysMon, Remove (metodo)
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
ms.openlocfilehash: 057607c57db600ca7a28c8a5bb6d75d5570829cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742935"
---
# <a name="logfilesremove-method"></a>LogFiles. Remove (metodo)

Rimuove l'istanza di [**LogFileItem**](logfileitem.md) specificata dalla raccolta.

## <a name="syntax"></a>Sintassi


```VB
LogFiles.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ di in\]
</dt> <dd>

Indice integer del file di log da rimuovere dalla raccolta. L'indice è in base uno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

**Prima di Windows Vista:** Non è possibile rimuovere i file di log dalla [**raccolta dei file di log**](systemmonitor-logfiles.md) se il valore di [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) è impostato su sysmonLogFiles.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[LogFiles](logfiles.md)
</dt> <dt>

[**LogFileItem**](logfileitem.md)
</dt> <dt>

[**LogFiles**](systemmonitor-logfiles.md)
</dt> </dl>

 

 






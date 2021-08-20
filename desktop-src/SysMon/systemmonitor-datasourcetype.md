---
title: SystemMonitor DataSourceType - proprietà
description: Recupera o imposta l'origine dei dati del contatore delle prestazioni.
ms.assetid: 53c1e9bc-dafd-445c-8d82-13a74f6c488a
keywords:
- Proprietà DataSourceType SysMon
- Proprietà DataSourceType SysMon , interfaccia SystemMonitor
- Interfaccia SystemMonitor SysMon , proprietà DataSourceType
topic_type:
- apiref
api_name:
- SystemMonitor.DataSourceType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e60a8d41afe454d0d84d7854716d26709986af358e9528e6c86ed06adc0cef6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117955951"
---
# <a name="systemmonitordatasourcetype-property"></a>Proprietà SystemMonitor::D ataSourceType

Recupera o imposta l'origine dei dati del contatore delle prestazioni.

## <a name="syntax"></a>Sintassi


```VB
Property DataSourceType As DataSourceTypeConstants
```



## <a name="property-value"></a>Valore proprietà

Origine dei dati del contatore delle prestazioni. Per i valori possibili, vedere [**DataSourceTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-datasourcetypeconstants).

## <a name="exceptions"></a>Eccezioni



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo di eccezione</th>
<th>Condizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>System.ArgumentException</strong></td>
<td>È possibile ricevere questa eccezione per uno dei motivi seguenti:
<ul>
<li>Il valore dell'origine dati specificato non è valido.</li>
<li>Se l'origine dati è un file di log, SYSMON non riesce a trovare uno dei file specificati. Il valore Err.Number è 0xC0000BD1.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

**Prima di Windows Vista:** Non è possibile aggiungere o rimuovere un file di log dalla raccolta [**di file**](systemmonitor-logfiles.md) di log se il valore di questa proprietà è impostato su sysmonLogFiles. Impostare il valore di questa proprietà su sysmonLogFiles solo dopo aver creato o modificato la raccolta di file di log.

Inoltre, non è possibile modificare le [**proprietà SqlDsnName**](systemmonitor-sqldsnname.md) e [**SqlLogSetName**](systemmonitor-sqllogsetname.md) se il valore di questa proprietà non deve essere impostato su sysmonSqlLog. Impostare il valore di questa proprietà su sysmonSqlLog solo dopo aver modificato i nomi del server e del database.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 






---
title: Proprietà DataSourceType di SystemMonitor
description: Recupera o imposta l'origine dei dati del contatore delle prestazioni.
ms.assetid: 53c1e9bc-dafd-445c-8d82-13a74f6c488a
keywords:
- Proprietà DataSourceType SysMon
- Proprietà DataSourceType SysMon, interfaccia SystemMonitor
- Interfaccia SystemMonitor SysMon, proprietà DataSourceType
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
ms.openlocfilehash: 7a111d1e617745de1109f8359da158e642e93d17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048579"
---
# <a name="systemmonitordatasourcetype-property"></a>SystemMonitor::D Proprietà ataSourceType

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
<td><strong>System. ArgumentException</strong></td>
<td>È possibile ricevere questa eccezione per uno dei motivi seguenti:
<ul>
<li>Il valore dell'origine dati specificato non è valido.</li>
<li>Se l'origine dati è un file di log, SYSMON non è in grado di trovare uno dei file specificati. Il valore ERR. Number è 0xC0000BD1.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

**Prima di Windows Vista:** Se il valore di questa proprietà è impostato su sysmonLogFiles, non è possibile aggiungere o rimuovere i file di log dalla [**raccolta dei file di log**](systemmonitor-logfiles.md) . Impostare il valore di questa proprietà su sysmonLogFiles solo dopo la creazione o la modifica della raccolta di file di log.

Inoltre, non è possibile modificare le proprietà [**SqlDsnName**](systemmonitor-sqldsnname.md) e [**SqlLogSetName**](systemmonitor-sqllogsetname.md) se il valore di questa proprietà non deve essere impostato su sysmonSqlLog. Impostare il valore di questa proprietà su sysmonSqlLog solo dopo aver modificato i nomi del server e del database.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 






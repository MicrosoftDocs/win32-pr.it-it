---
title: Proprietà SqlDsnName di SystemMonitor
description: Recupera o imposta il nome dell'origine dati (DSN) ODBC.
ms.assetid: 7906204a-a208-42c7-855b-c29689b4d36a
keywords:
- Proprietà SqlDsnName SysMon
- Proprietà SqlDsnName SysMon, interfaccia SystemMonitor
- Interfaccia SystemMonitor SysMon, proprietà SqlDsnName
topic_type:
- apiref
api_name:
- SystemMonitor.SqlDsnName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 666b10ad91956adf7148e54b68f2b6db98e9a5b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400208"
---
# <a name="systemmonitorsqldsnname-property"></a>Proprietà SystemMonitor:: SqlDsnName

Recupera o imposta il nome dell'origine dati (DSN) ODBC.

## <a name="syntax"></a>Sintassi


```VB
Property SqlDsnName As String
```



## <a name="property-value"></a>Valore proprietà

Nome dell'origine dati ODBC che punta a un database contenente le tabelle PerfMon corrette. Il formato è SQL: DSN.

## <a name="remarks"></a>Commenti

Per generare il file di log SQL, è necessario utilizzare lo snap-in MMC Perfmon. msc. I registri dei contatori si trovano in **avvisi e registri di prestazioni**. Per specificare un log SQL, fare clic con il pulsante destro del mouse sul file di log creato e scegliere **Proprietà** dal menu. Nella pagina delle proprietà **file di registro** selezionare **database SQL** dall'elenco a discesa **tipo file di log** .

**Prima di Windows Vista:** Non è possibile modificare questa proprietà se il valore di [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) è impostato su [**DataSourceTypeConstants.sysmonSqlLog**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants). È necessario innanzitutto specificare il nome e quindi impostare **SystemMonitor. DataSourceType** su **DataSourceTypeConstants.sysmonSqlLog**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor. SqlLogSetName**](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 






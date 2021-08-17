---
description: Il qualificatore CounterType contiene il valore intero per il tipo di contatore delle proprietà per le proprietà nelle classi \_ Win32 PerfRawData. Il valore di CookingType contiene le costanti per i tipi di formula delle proprietà nelle classi \_ Win32 PerfFormattedData.
ms.assetid: aa79fcdb-503f-4928-b2b7-f07baeaf9fb5
ms.tgt_platform: multiple
title: Qualificatore CounterType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterType
api_type:
- NA
api_location: ''
ms.openlocfilehash: 7795633355eccdc19da235a56d211f4913ac532e9df51f6d30f33635f9b2d39a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131442"
---
# <a name="countertype-qualifier"></a>Qualificatore CounterType

Il **qualificatore CounterType** contiene il valore intero per il tipo di contatore delle proprietà per le proprietà nelle [**classi \_ Win32 PerfRawData.**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) **Il valore di CookingType** contiene le costanti per i tipi di formula delle proprietà nelle classi [**\_ Win32 PerfFormattedData.**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)

Per altre informazioni e una suddivisione dei tipi di contatore per funzione, vedere [Tipi di contatore](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).



| CounterType | Tipo di cucina                              |
|-------------|------------------------------------------|
| 0           | PERF \_ COUNTER \_ RAWCOUNT \_ HEX             |
| 256         | PERF \_ COUNTER \_ LARGE \_ RAWCOUNT \_ HEX      |
| 2816        | TESTO \_ CONTATORE PERF \_                      |
| 65536       | RAWCOUNT \_ DEL CONTATORE PERF \_                  |
| 65792       | RAWCOUNT \_ DI GRANDI DIMENSIONI DEL \_ CONTATORE PERF \_           |
| 73728       | PERF \_ DOUBLE \_ RAW                        |
| 4195328     | DELTA DEL \_ CONTATORE DI PERF \_                     |
| 4195584     | DIFFERENZIALE \_ PERF COUNTER \_ LARGE \_              |
| 4260864     | CONTATORE DI ESEMPIO DI \_ \_ PERF                    |
| 4523008     | TIPO \_ QUEUELEN DEL \_ CONTATORE \_ PERF            |
| 4523264     | PERF \_ COUNTER \_ LARGE \_ QUEUELEN \_ TYPE     |
| 5571840     | PERF \_ COUNTER \_ 100NS \_ QUEUELEN \_ TYPE     |
| 6620416     | PERF \_ COUNTER \_ OBJ \_ TIME \_ QUEUELEN \_ TYPE |
| 272696320   | CONTATORE DI \_ \_ PERF                   |
| 272696576   | CONTEGGIO \_ BULK DEL CONTATORE DI \_ \_ PERF               |
| 537003008   | FRAZIONE NON ELABORATA PERF \_ \_                      |
| 541132032   | TIMER \_ CONTATORE PERF \_                     |
| 541525248   | TIMER DI SISTEMA \_ PERF PRECISION \_ \_           |
| 542180608   | PERF \_ 100NSEC \_ TIMER                     |
| 542573824   | PERF \_ PRECISION \_ 100NS \_ TIMER            |
| 543229184   | TIMER TEMPO \_ OBJ PERF \_ \_                   |
| 543622400   | TIMER \_ DELL'OGGETTO PRECISIONE \_ PERF \_           |
| 549585920   | FRAZIONE DEL CAMPIONE DI PERF \_ \_                   |
| 557909248   | TIMER \_ CONTATORE \_ \_ PERF INV                |
| 558957824   | PERF \_ 100NSEC \_ TIMER \_ INV                |
| 574686464   | TIMER MULTI \_ CONTATORE PERF \_ \_              |
| 575735040   | PERF \_ 100NSEC \_ MULTI \_ TIMER              |
| 591463680   | CONTATORE PERF \_ \_ MULTI TIMER \_ \_ INV         |
| 592512256   | PERF \_ 100NSEC \_ MULTI \_ TIMER \_ INV         |
| 805438464   | TIMER \_ MEDIO PERF \_                     |
| 807666944   | TEMPO \_ TRASCORSO PERF \_                      |
| 1073742336  | PERF \_ COUNTER \_ NODATA                    |
| 1073874176  | PERF \_ AVERAGE \_ BULK                      |
| 1073939457  | BASE DI \_ ESEMPIO DI \_ PERF                       |
| 1073939458  | BASE MEDIA \_ \_ PERF                      |
| 1073939459  | BASE NON ELABORATA DI PERF \_ \_                          |
| 1073939712  | TIMESTAMP DI PRECISIONE PERF \_ \_               |
| 1073939715  | BASE NON \_ ELABORATA PERF \_ LARGE \_                   |
| 1107494144  | PERF \_ COUNTER \_ MULTI \_ BASE               |
| 2147483648  | TIPO DI \_ \_ ISTOGRAMMA CONTATORE \_ PERF           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Qualificatori specifici delle classi di prestazioni WMI](qualifiers-specific-to-wmi-performance-classes.md)
</dt> </dl>

 


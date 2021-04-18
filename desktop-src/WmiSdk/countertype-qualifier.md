---
description: Il qualificatore CounterType contiene il valore integer per il tipo di contatore di proprietà per le proprietà nelle \_ classi PerfRawData Win32. CookingType contiene le costanti per i tipi di formule di proprietà nelle \_ classi PerfFormattedData Win32.
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
ms.openlocfilehash: 883ee7aa2f230756d62294d46e6402fe7f962d4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310404"
---
# <a name="countertype-qualifier"></a>Qualificatore CounterType

Il qualificatore **CounterType** contiene il valore integer per il tipo di contatore di proprietà per le proprietà nelle classi [**\_ PerfRawData Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) . **CookingType** contiene le costanti per i tipi di formule di proprietà nelle classi [**\_ PerfFormattedData Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) .

Per ulteriori informazioni e per una suddivisione dei tipi di contatore per funzione, vedere [tipi di contatori](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).



| CounterType | CookingType                              |
|-------------|------------------------------------------|
| 0           | \_ \_ RAWCOUNT Hex contatore \_ prestazioni             |
| 256         | \_ \_ \_ RAWCOUNT Hex contatore di grandi dimensioni \_      |
| 2816        | \_testo contatore \_ prestazioni                      |
| 65536       | \_RAWCOUNT contatore \_ prestazioni                  |
| 65792       | \_contatore prestazioni \_ RAWCOUNT di grandi dimensioni \_           |
| 73728       | PRESTAZIONI \_ doppie \_ RAW                        |
| 4195328     | \_Delta contatore \_ prestazioni                     |
| 4195584     | \_Delta contatore prestazioni \_ elevate \_              |
| 4260864     | \_contatore di esempio delle prestazioni \_                    |
| 4523008     | \_tipo di \_ QUEUELEN del contatore delle prestazioni \_            |
| 4523264     | \_tipo di \_ QUEUELEN di grandi dimensioni contatore prestazioni \_ \_     |
| 5571840     | \_ \_ \_ Tipo QUEUELEN del contatore delle prestazioni 100 NS \_     |
| 6620416     | \_ \_ \_ \_ tipo QUEUELEN ora obj contatore \_ prestazioni |
| 272696320   | contatore delle prestazioni \_ \_                   |
| 272696576   | \_ \_ conteggio bulk del contatore delle prestazioni \_               |
| 537003008   | \_frazione RAW \_ prestazioni                      |
| 541132032   | \_timer contatore \_ prestazioni                     |
| 541525248   | \_timer di \_ sistema per precisione prestazioni \_           |
| 542180608   | \_Timer 100NSEC \_ perf                     |
| 542573824   | \_ \_ Timer 100 ns precisione \_ prestazioni            |
| 543229184   | \_ \_ timer ora obj \_ perf                   |
| 543622400   | \_ \_ timer oggetto precisione \_ prestazioni           |
| 549585920   | \_frazione campione \_ prestazioni                   |
| 557909248   | \_timer contatore \_ prestazioni \_ inv                |
| 558957824   | \_Timer di 100NSEC Perf \_ \_                |
| 574686464   | \_contatore prestazioni \_ \_ multitimer              |
| 575735040   | PRESTAZIONI \_ 100NSEC \_ \_ multitimer              |
| 591463680   | \_contatore delle \_ prestazioni \_ multitimer \_ inv         |
| 592512256   | PERF \_ 100NSEC \_ \_ multitimer \_ inv         |
| 805438464   | \_timer medio \_ prestazioni                     |
| 807666944   | \_tempo trascorso prestazioni \_                      |
| 1073742336  | contatori delle prestazioni \_ \_ NoData                    |
| 1073874176  | media prestazioni in \_ \_ blocco                      |
| 1073939457  | \_base di esempio delle prestazioni \_                       |
| 1073939458  | \_base media \_ prestazioni                      |
| 1073939459  | \_base prestazioni raw \_                          |
| 1073939712  | \_timestamp precisione \_ prestazioni               |
| 1073939715  | \_ \_ base grezza per prestazioni elevate \_                   |
| 1107494144  | \_contatori delle \_ prestazioni \_ multibase               |
| 2147483648  | \_tipo di \_ istogramma del contatore delle prestazioni \_           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Qualificatori specifici delle classi di prestazioni WMI](qualifiers-specific-to-wmi-performance-classes.md)
</dt> </dl>

 


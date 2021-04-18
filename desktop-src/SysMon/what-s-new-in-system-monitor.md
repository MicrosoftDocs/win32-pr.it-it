---
title: Novità di monitoraggio di sistema
description: Nella tabella seguente sono riportate le novità per ogni versione di monitoraggio di sistema (SYSMON).
ms.assetid: 9cb0e0db-0933-4993-a995-74a36a24eccb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3662e83954630232e3fe30c26a3f6d94aa9cc7
ms.sourcegitcommit: 780d4b1601c45658ef0b799b80d13f45a53d808d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/26/2020
ms.locfileid: "104398689"
---
# <a name="whats-new-in-system-monitor"></a>Novità di monitoraggio di sistema

Nella tabella seguente sono riportate le novità per ogni versione di monitoraggio di sistema (SYSMON).



| Versione     | Descrizione delle funzionalità                                                                                                                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione 3,7 | Questa versione aggiunge nuovi tipi di grafico, la possibilità di selezionare più contatori, di recuperare i valori dei contatori da un punto nel grafico, di salvare i valori dei contatori con grafici in un file di log e l'opzione per fare in modo che un grafico a linee scorra continuamente nella finestra del grafico anziché eseguire il wrapping su se stesso. Incluso in Windows Server 2008 e Windows Vista.<br/> |



 

## <a name="version-37"></a>Versione 3,7

Nuovi metodi e proprietà aggiunti a [**CounterItem**](counteritem.md).

-   [**GetDataAt**](counteritem-getdataat.md)
-   [**Selezionato**](counteritem-selected.md)
-   [**Visible**](counteritem-visible.md)
-   Intervallo di valori validi modificato per [ **CounterItem. Width**](counteritem-width.md)

Nuovi metodi e proprietà aggiunti a [**SystemMonitor**](systemmonitor.md).

-   [**BatchingLock**](systemmonitor-batchinglock.md)
-   [**ChartScroll**](systemmonitor-chartscroll.md)
-   [**ClearData**](systemmonitor-cleardata.md)
-   [**DataPointCount**](systemmonitor-datapointcount.md)
-   [**EnableDigitGrouping**](systemmonitor-enabledigitgrouping.md)
-   [**EnableToolTips**](systemmonitor-enabletooltips.md)
-   [**GetLogViewRange**](systemmonitor-getlogviewrange.md)
-   [**LoadSettings**](systemmonitor-loadsettings.md)
-   [**LogSourceStartTime**](systemmonitor-logsourcestarttime.md)
-   [**LogSourceStopTime**](systemmonitor-logsourcestoptime.md)
-   [**Relog**](systemmonitor-relog.md)
-   [**SaveAs**](systemmonitor-saveas.md)
-   [**ScaleToFit**](systemmonitor-scaletofit.md)
-   [**SetLogViewRange**](systemmonitor-setlogviewrange.md)
-   [**ShowTimeAxisLables**](systemmonitor-showtimeaxislabels.md)

Nuove enumerazioni aggiunte.

-   [**SysmonDataType**](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype)
-   [**SysmonFileType**](/windows/win32/api/isysmon/ne-isysmon-sysmonfiletype)
-   Sono stati aggiunti nuovi valori del tipo di visualizzazione a [ **DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants)

 

 






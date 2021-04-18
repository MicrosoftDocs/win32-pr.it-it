---
title: Utilizzo di monitoraggio di sistema
description: È possibile includere monitor di sistema (SYSMON) in qualsiasi applicazione che supporti ActiveX \ 174; controlli. È ad esempio possibile includere SYSMON in un'applicazione Microsoft Visual Basic o in un documento HTML.
ms.assetid: 36931aae-b608-42d9-a3e3-09784e80f386
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abd636c8b984f7c891c2222b4674dd8d0d7e747d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298399"
---
# <a name="using-system-monitor"></a>Utilizzo di monitoraggio di sistema

È possibile includere monitor di sistema (SYSMON) in qualsiasi applicazione che supporti i controlli ActiveX®. È ad esempio possibile includere SYSMON in un'applicazione Microsoft Visual Basic o in un documento HTML.

Nell'esempio seguente viene illustrato come includere SYSMON in un documento HTML. Nell'esempio viene utilizzato VBScript per aggiungere contatori i cui valori vengono recuperati dal computer locale, vengono modificate alcune delle proprietà di SYSMON che controllano la modalità di visualizzazione del monitoraggio e viene elaborato l'evento OnCounterAdd. Nell'esempio viene usato il carattere jolly ( \* ) per aggiungere tutte le istanze del contatore di processi.

``` syntax
<HTML>
<BODY BGCOLOR=#C0C0C0>

<SCRIPT LANGUAGE="VBScript">
  Sub Monitor_OnCounterAdded(index)
    Monitor.Counters.Item(1).Width = 8
  End Sub
</Script>
<OBJECT
  CLASSID="clsid:C4D2D8E0-D1DD-11CE-940F-008029004347"
  ID="Monitor"
  HEIGHT=80%
  WIDTH=100%>
</OBJECT>

<SCRIPT LANGUAGE="VBScript">
  Sub Window_OnLoad
    On Error Resume Next
    Monitor.ShowValueBar = False
    Monitor.ShowHorizontalGrid = True
    Monitor.Counters.Add("\Process(*)\% Processor Time")
    Monitor.DisplayType=sysmonLineGraph
    Monitor.GraphTitle="System Performance Overview"
  End Sub
</SCRIPT>

</BODY>
</HTML>
```

 

 





---
description: 'Altre informazioni su: impostazione della consapevolezza DPI predefinita per un processo'
title: Impostazione della consapevolezza DPI predefinita per un processo (Windows)
TOCTitle: Setting the default DPI awareness for a process
ms:assetid: C9488338-D863-45DF-B5CB-7ED9B869A5E2
ms:mtpsurl: https://msdn.microsoft.com/library/Mt846517(v=VS.85)
ms:contentKeyID: 74520139
ms.date: 03/30/2018
ms.topic: article
mtps_version: v=VS.85
ms.openlocfilehash: ff869974e6d9aa2eec2b3251832c061d7b6826da
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321028"
---
# <a name="setting-the-default-dpi-awareness-for-a-process"></a>Impostazione della consapevolezza DPI predefinita per un processo

Le applicazioni desktop in Windows possono essere eseguite in modalità di riconoscimento DPI diverse. Queste modalità consentono un comportamento di scalabilità DPI diverso e possono usare spazi delle coordinate diversi. Per ulteriori informazioni sulla compatibilità con DPI, vedere [sviluppo di applicazioni desktop con DPI elevato in Windows.](https://msdn.microsoft.com/library/mt843498\(v=vs.85\)) È importante impostare in modo esplicito la modalità di riconoscimento DPI predefinita del processo in modo da evitare un comportamento imprevisto.

Esistono due metodi principali per specificare la consapevolezza DPI predefinita di un processo:

da 1 a \) un'impostazione del manifesto dell'applicazione

2 \) a livello di codice tramite una chiamata API

Si consiglia di specificare la consapevolezza predefinita del processo DPI tramite un'impostazione del manifesto. Quando si specifica il valore predefinito tramite l'API è supportata, non è consigliabile.

## <a name="setting-default-awareness-with-the-application-manifest"></a>Impostazione della consapevolezza predefinita con il manifesto dell'applicazione

Sono disponibili due impostazioni del manifesto che consentono di specificare la modalità di riconoscimento DPI predefinita del processo: \<dpiAwareness\> e \<dpiAware\> . \<dpiAware\> è stato introdotto in Windows Vista e consente di impostare l'impostazione predefinita del processo solo su riconoscimento sistema. \<dpiAwareness\> è stato introdotto in Windows 10, versione 1607 e consente di specificare un elenco ordinato di modalità di riconoscimento DPI predefinite del processo. Questo consente di impostare le modalità di riconoscimento DPI di backup, che verranno usate se l'applicazione viene eseguita in una versione di Windows non è in grado di supportare la prima modalità di riconoscimento specificata. Nelle versioni precedenti di Windows il tag più recente \<dpiAwareness\> verrà ignorato. Ciò significa che è possibile usare entrambe le impostazioni del manifesto per abilitare uno scenario in cui l'impostazione predefinita del processo potrebbe essere la consapevolezza del sistema in una versione precedente di Windows, mentre Per-Monitor nelle versioni successive a Windows 10, versione 1607. In Windows 10, versione 1607 e su, l' \<dpiAware\> impostazione viene ignorata se l' \<dpiAwareness\> elemento è presente.

La tabella seguente illustra come specificare diverse modalità di riconoscimento DPI predefinite del processo usando le due impostazioni del manifesto:

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Modalità di riconoscimento DPI predefinita del processo</th>
<th>&lt;&gt;impostazione dpiAware</th>
<th>&lt;&gt;impostazione di dpiAwareness (Windows 10, versione 1607 e successive)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>a conoscenza</td>
<td><p>N/d (nessuna impostazione dpiAware nel manifesto)</p>
<p>oppure</p>
<p>&lt;dpiAware &gt; false &lt; /dpiAware&gt;</p></td>
<td>&lt;&gt;/DpiAwareness dpiAwareness incompatibili &lt;&gt;</td>
</tr>
<tr class="even">
<td>Compatibile con il sistema</td>
<td>&lt;dpiAware &gt; true &lt; /dpiAware&gt;</td>
<td>&lt;&gt;/dpiAwareness di sistema dpiAwareness &lt;&gt;</td>
</tr>
<tr class="odd">
<td>Per monitoraggio</td>
<td>&lt;dpiAware &gt; true/PM &lt; dpiAware&gt;</td>
<td>&lt;dpiAwareness &gt; PerMonitor &lt; /dpiAwareness&gt;</td>
</tr>
<tr class="even">
<td>Per monitor V2</td>
<td>Non supportato</td>
<td>&lt;dpiAwareness &gt; PerMonitorV2 &lt; /dpiAwareness&gt;</td>
</tr>
</tbody>
</table>

 

Nell'esempio seguente vengono illustrate le \<dpiAwareness\> \<dpiAware\> Impostazioni e utilizzate nello stesso file manifesto per configurare il comportamento di riconoscimento dpi predefinito del processo per le diverse versioni di Windows.

```xml
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
  <asmv3:application>
    <asmv3:windowsSettings>
      <dpiAware xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">true</dpiAware>
      <dpiAwareness xmlns="http://schemas.microsoft.com/SMI/2016/WindowsSettings">PerMonitorV2</dpiAwareness>
    </asmv3:windowsSettings>
  </asmv3:application>
</assembly>
```

## <a name="setting-default-awareness-programmatically"></a>Impostazione della consapevolezza predefinita a livello di codice

Sebbene non sia consigliato, è possibile impostare la consapevolezza DPI predefinita a livello di codice. Una volta creata una finestra (HWND) nel processo, la modifica della modalità di riconoscimento DPI non è più supportata. Se si imposta la modalità di riconoscimento DPI predefinita del processo a livello di codice, è necessario chiamare l'API corrispondente prima che siano stati creati HWND.

Sono disponibili più API che consentono di specificare la consapevolezza DPI predefinita per il processo. L'API consigliata corrente è [**SetProcessDpiAwarenessContext**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\)), perché le API precedenti offrono meno funzionalità.

 

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th>API</th>
<th>Versione minima di Windows</th>
<th>DPI non a conoscenza</th>
<th>Compatibile con DPI di sistema</th>
<th>Compatibile con DPI per monitor</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDpiAware</a></td>
<td>Windows Vista</td>
<td>N/D</td>
<td>SetProcessDpiAware()</td>
<td>N/D</td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>SetProcessDpiAwareness</strong></a></td>
<td>Windows 8.1</td>
<td>SetProcessDpiAwareness (PROCESS_DPI_UNAWARE)</td>
<td>SetProcessDpiAwareness (PROCESS_DPI_SYSTEM_DPI_AWARE)</td>
<td>SetProcessDpiAwareness (PROCESS_DPI_PER_MONITOR_DPI_AWARE)</td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>SetProcessDpiAwarenessContext</strong></a></td>
<td>Windows 10 versione 1607</td>
<td>SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_UNAWARE)</td>
<td>SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_SYSTEM_AWARE)</td>
<td><p>SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)</p>
<p>SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)</p></td>
</tr>
</tbody>
</table>

 

## <a name="process-default-vs-thread-default"></a>Processo-predefinito rispetto a thread predefinito

Questo documento si riferisce all'impostazione della consapevolezza DPI predefinita per il processo. Questo è dovuto al fatto che in Windows 10 è stato introdotto il supporto per l'esecuzione di più di una modalità di riconoscimento DPI all'interno di un singolo processo (prima di Windows 10, l'intero processo doveva essere conforme a una sola modalità di riconoscimento DPI). Il supporto per l'esecuzione di più modalità di riconoscimento DPI all'interno di un processo viene definito "scalabilità DPI in modalità mista". Quando si usa il ridimensionamento DPI in modalità mista all'interno del processo, ogni finestra di primo livello può essere eseguita in una modalità di riconoscimento DPI che può essere diversa da quella del processo predefinito. A meno che non venga specificato in modo esplicito, al momento della creazione ogni thread utilizzerà per impostazione predefinita il processo predefinito. Per altre informazioni sul ridimensionamento DPI in modalità mista, vedere l'articolo relativo alla [scalabilità dpi in modalità mista](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) .

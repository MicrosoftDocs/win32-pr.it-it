---
description: 'Altre informazioni su: Impostazione della sensibilità DPI predefinita per un processo'
title: Impostazione della sensibilità DPI predefinita per un processo (Windows)
TOCTitle: Setting the default DPI awareness for a process
ms:assetid: C9488338-D863-45DF-B5CB-7ED9B869A5E2
ms:mtpsurl: https://msdn.microsoft.com/library/Mt846517(v=VS.85)
ms:contentKeyID: 74520139
ms.date: 03/30/2018
ms.topic: article
mtps_version: v=VS.85
ms.openlocfilehash: c9192bf650588b7c21f17afb45149fe460f91bea
ms.sourcegitcommit: ecd0ba4732f5264aab9baa2839c11f7fea36318f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/07/2021
ms.locfileid: "113481866"
---
# <a name="setting-the-default-dpi-awareness-for-a-process"></a>Impostazione della sensibilità DPI predefinita per un processo

Le applicazioni desktop in Windows possono essere eseguite in modalità di riconoscimento DPI diverse. Queste modalità consentono un comportamento di ridimensionamento DPI diverso e possono usare spazi di coordinate diversi. Per altre informazioni sul riconoscimento DPI, vedere Sviluppo di applicazioni desktop con [valori DPI](https://msdn.microsoft.com/library/mt843498\(v=vs.85\)) alti Windows. È importante impostare in modo esplicito la modalità di riconoscimento DPI predefinita del processo per evitare comportamenti imprevisti.

Esistono due metodi principali per specificare il riconoscimento DPI predefinito di un processo:

Da 1 \) a un'impostazione del manifesto dell'applicazione

2 a \) livello di codice tramite una chiamata API

È consigliabile specificare il riconoscimento DPI del processo predefinito tramite un'impostazione del manifesto. Anche se è supportata la specifica dell'impostazione predefinita tramite API, non è consigliabile.

## <a name="setting-default-awareness-with-the-application-manifest"></a>Impostazione della consapevolezza predefinita con il manifesto dell'applicazione

Sono disponibili due impostazioni del manifesto che consentono di specificare la modalità di riconoscimento DPI predefinita del processo: \<dpiAwareness\> e \<dpiAware\> . \<dpiAware\>è stato introdotto in Windows Vista e consente solo l'impostazione predefinita del processo sulla consapevolezza del sistema. \<dpiAwareness\>è stato introdotto in Windows 10 versione 1607 e consente di specificare un elenco ordinato di modalità di riconoscimento DPI predefinite del processo. In questo modo è possibile impostare le modalità di riconoscimento DPI di backup, che verranno usate se l'applicazione viene eseguita in una versione di Windows non è in grado di supportare la prima modalità di riconoscimento specificata. Nelle versioni precedenti di Windows, il tag più \<dpiAwareness\> recente verrà ignorato. Ciò significa che è possibile usare entrambe queste impostazioni del manifesto per abilitare uno scenario in cui l'impostazione predefinita del processo potrebbe essere il riconoscimento del sistema per la versione precedente di Windows mentre è Per-Monitor in versioni successive a Windows 10, versione 1607. In Windows 10 versione 1607 e attivata, l'impostazione viene ignorata \<dpiAware\> se \<dpiAwareness\> l'elemento è presente.

La tabella seguente illustra come specificare diverse modalità di riconoscimento DPI predefinite del processo usando le due impostazioni del manifesto:

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Elaborare la modalità di riconoscimento DPI predefinita</th>
<th>&lt;Impostazione &gt; dpiAware</th>
<th>&lt;Impostazione dpiAwareness &gt; (Windows 10, versione 1607 e successive)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ignari</td>
<td><p>N/D (nessuna impostazione dpiAware nel manifesto)</p>
<p>oppure</p>
<p>&lt;dpiAware &gt; false &lt; /dpiAware&gt;</p></td>
<td>&lt;dpiAwareness &gt; unware &lt; /dpiAwareness&gt;</td>
</tr>
<tr class="even">
<td>In grado di riconoscere il sistema</td>
<td>&lt;dpiAware &gt; true &lt; /dpiAware&gt;</td>
<td>&lt;dpiAwareness &gt; system &lt; /dpiAwareness&gt;</td>
</tr>
<tr class="odd">
<td>Per Monitor</td>
<td>&lt;dpiAware &gt; true/pm &lt; dpiAware&gt;</td>
<td>&lt;dpiAwareness &gt; PerMonitor &lt; /dpiAwareness&gt;</td>
</tr>
<tr class="even">
<td>Per Monitor V2</td>
<td>Non supportato</td>
<td>&lt;dpiAwareness &gt; PerMonitorV2 &lt; /dpiAwareness&gt;</td>
</tr>
</tbody>
</table>

 

L'esempio seguente illustra le impostazioni e usate all'interno dello stesso file manifesto per configurare il comportamento di riconoscimento DPI predefinito del processo per versioni diverse \<dpiAwareness\> \<dpiAware\> di Windows.

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

Anche se non è consigliabile, è possibile impostare la consapevolezza DPI predefinita a livello di codice. Dopo aver creato una finestra (HWND) nel processo, la modifica della modalità di riconoscimento DPI non è più supportata. Se si imposta la modalità di riconoscimento DPI predefinita del processo a livello di codice, è necessario chiamare l'API corrispondente prima di creare gli HWND.

Sono disponibili più API che consentono di specificare la consapevolezza DPI predefinita per il processo. L'API consigliata corrente [**è SetProcessDpiAwarenessContext,**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\))perché le API meno recenti offrono meno funzionalità.

 

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
<th>DPI inconsapevole</th>
<th>In grado di riconoscere DPI di sistema</th>
<th>Supporto DPI per monitor</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDPIAware</a></td>
<td>Windows Vista</td>
<td>N/D</td>
<td>SetProcessDPIAware()</td>
<td>N/D</td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>SetProcessDpiAwareness</strong></a></td>
<td>Windows 8.1</td>
<td>SetProcessDpiAwareness(PROCESS_DPI_UNAWARE)</td>
<td>SetProcessDpiAwareness(PROCESS_SYSTEM_DPI_AWARE)</td>
<td>SetProcessDpiAwareness(PROCESS_PER_MONITOR_DPI_AWARE)</td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>SetProcessDpiAwarenessContext</strong></a></td>
<td>Windows 10 versione 1607</td>
<td>SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_UNAWARE)</td>
<td>SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_SYSTEM_AWARE)</td>
<td><p>SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)</p>
<p>SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)</p></td>
</tr>
</tbody>
</table>

 

## <a name="process-default-vs-thread-default"></a>Impostazione predefinita del processo e impostazione predefinita del thread

Questo documento si riferisce all'impostazione della sensibilità DPI predefinita per il processo. Ciò è dovuto al fatto che Windows 10 introdotto il supporto per l'esecuzione di più modalità di riconoscimento DPI all'interno di un singolo processo (prima di Windows 10, l'intero processo doveva essere conforme a una singola modalità di riconoscimento DPI). Il supporto per l'esecuzione di più modalità di riconoscimento DPI all'interno di un processo è detto "ridimensionamento DPI in modalità mista". Quando si usa il ridimensionamento DPI in modalità mista all'interno del processo, ogni finestra di primo livello può essere eseguita in una modalità di riconoscimento DPI che può essere diversa da quella predefinita del processo. Se non specificato in modo esplicito, ogni thread verrà impostato sul valore predefinito del processo al momento della creazione. Per altre informazioni sul ridimensionamento DPI in modalità mista, vedere l'articolo [Ridimensionamento DPI](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) in modalità mista.

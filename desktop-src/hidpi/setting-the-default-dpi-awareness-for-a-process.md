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
# <a name="setting-the-default-dpi-awareness-for-a-process"></a><span data-ttu-id="ffc11-103">Impostazione della consapevolezza DPI predefinita per un processo</span><span class="sxs-lookup"><span data-stu-id="ffc11-103">Setting the default DPI awareness for a process</span></span>

<span data-ttu-id="ffc11-104">Le applicazioni desktop in Windows possono essere eseguite in modalità di riconoscimento DPI diverse.</span><span class="sxs-lookup"><span data-stu-id="ffc11-104">Desktop applications on Windows can run in different DPI awareness modes.</span></span> <span data-ttu-id="ffc11-105">Queste modalità consentono un comportamento di scalabilità DPI diverso e possono usare spazi delle coordinate diversi.</span><span class="sxs-lookup"><span data-stu-id="ffc11-105">These modes enable different DPI scaling behavior and can use different coordinate spaces.</span></span> <span data-ttu-id="ffc11-106">Per ulteriori informazioni sulla compatibilità con DPI, vedere [sviluppo di applicazioni desktop con DPI elevato in Windows.](https://msdn.microsoft.com/library/mt843498\(v=vs.85\))</span><span class="sxs-lookup"><span data-stu-id="ffc11-106">For more information on DPI awareness, see [High DPI Desktop Application Development on Windows.](https://msdn.microsoft.com/library/mt843498\(v=vs.85\))</span></span> <span data-ttu-id="ffc11-107">È importante impostare in modo esplicito la modalità di riconoscimento DPI predefinita del processo in modo da evitare un comportamento imprevisto.</span><span class="sxs-lookup"><span data-stu-id="ffc11-107">It is important that you explicitly set the default DPI awareness mode of your process so as to avoid unexpected behavior.</span></span>

<span data-ttu-id="ffc11-108">Esistono due metodi principali per specificare la consapevolezza DPI predefinita di un processo:</span><span class="sxs-lookup"><span data-stu-id="ffc11-108">There are two main methods to specify the default DPI awareness of a process:</span></span>

<span data-ttu-id="ffc11-109">da 1 a \) un'impostazione del manifesto dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="ffc11-109">1\) through an application manifest setting</span></span>

<span data-ttu-id="ffc11-110">2 \) a livello di codice tramite una chiamata API</span><span class="sxs-lookup"><span data-stu-id="ffc11-110">2\) programmatically through an API call</span></span>

<span data-ttu-id="ffc11-111">Si consiglia di specificare la consapevolezza predefinita del processo DPI tramite un'impostazione del manifesto.</span><span class="sxs-lookup"><span data-stu-id="ffc11-111">We recommended that you specify the default process DPI awareness via a manifest setting.</span></span> <span data-ttu-id="ffc11-112">Quando si specifica il valore predefinito tramite l'API è supportata, non è consigliabile.</span><span class="sxs-lookup"><span data-stu-id="ffc11-112">While specifying the default via API is supported, it is not recommended.</span></span>

## <a name="setting-default-awareness-with-the-application-manifest"></a><span data-ttu-id="ffc11-113">Impostazione della consapevolezza predefinita con il manifesto dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="ffc11-113">Setting default awareness with the application manifest</span></span>

<span data-ttu-id="ffc11-114">Sono disponibili due impostazioni del manifesto che consentono di specificare la modalità di riconoscimento DPI predefinita del processo: \<dpiAwareness\> e \<dpiAware\> .</span><span class="sxs-lookup"><span data-stu-id="ffc11-114">There are two manifest settings that enable you to specify the process default DPI awareness mode: \<dpiAwareness\> and \<dpiAware\>.</span></span> <span data-ttu-id="ffc11-115">\<dpiAware\> è stato introdotto in Windows Vista e consente di impostare l'impostazione predefinita del processo solo su riconoscimento sistema.</span><span class="sxs-lookup"><span data-stu-id="ffc11-115">\<dpiAware\> was introduced in Windows Vista and only enables your process default to be set to system awareness.</span></span> <span data-ttu-id="ffc11-116">\<dpiAwareness\> è stato introdotto in Windows 10, versione 1607 e consente di specificare un elenco ordinato di modalità di riconoscimento DPI predefinite del processo.</span><span class="sxs-lookup"><span data-stu-id="ffc11-116">\<dpiAwareness\> was introduced in Windows 10, version 1607 and enables you to specify an ordered list of process-default DPI awareness modes.</span></span> <span data-ttu-id="ffc11-117">Questo consente di impostare le modalità di riconoscimento DPI di backup, che verranno usate se l'applicazione viene eseguita in una versione di Windows non è in grado di supportare la prima modalità di riconoscimento specificata.</span><span class="sxs-lookup"><span data-stu-id="ffc11-117">This enables you to set backup DPI awareness modes, which will be used if your application is ran on a version of Windows unable to support the first awareness mode specified.</span></span> <span data-ttu-id="ffc11-118">Nelle versioni precedenti di Windows il tag più recente \<dpiAwareness\> verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="ffc11-118">On older versions of Windows, the newer \<dpiAwareness\> tag will be ignored.</span></span> <span data-ttu-id="ffc11-119">Ciò significa che è possibile usare entrambe le impostazioni del manifesto per abilitare uno scenario in cui l'impostazione predefinita del processo potrebbe essere la consapevolezza del sistema in una versione precedente di Windows, mentre Per-Monitor nelle versioni successive a Windows 10, versione 1607.</span><span class="sxs-lookup"><span data-stu-id="ffc11-119">This means that you can use both of these manifest settings to enable a scenario where your process default could be system awareness on older version of Windows while being Per-Monitor on versions greater than Windows 10, version 1607.</span></span> <span data-ttu-id="ffc11-120">In Windows 10, versione 1607 e su, l' \<dpiAware\> impostazione viene ignorata se l' \<dpiAwareness\> elemento è presente.</span><span class="sxs-lookup"><span data-stu-id="ffc11-120">On Windows 10, version 1607, and on, the \<dpiAware\> setting is ignored if the \<dpiAwareness\> element is present.</span></span>

<span data-ttu-id="ffc11-121">La tabella seguente illustra come specificare diverse modalità di riconoscimento DPI predefinite del processo usando le due impostazioni del manifesto:</span><span class="sxs-lookup"><span data-stu-id="ffc11-121">The table below shows how to specify different process-default DPI awareness modes using the two manifest settings:</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ffc11-122">Modalità di riconoscimento DPI predefinita del processo</span><span class="sxs-lookup"><span data-stu-id="ffc11-122">Process default DPI awareness mode</span></span></th>
<th><span data-ttu-id="ffc11-123">&lt;&gt;impostazione dpiAware</span><span class="sxs-lookup"><span data-stu-id="ffc11-123">&lt;dpiAware&gt; setting</span></span></th>
<th><span data-ttu-id="ffc11-124">&lt;&gt;impostazione di dpiAwareness (Windows 10, versione 1607 e successive)</span><span class="sxs-lookup"><span data-stu-id="ffc11-124">&lt;dpiAwareness&gt; setting (Windows 10, version 1607 and later)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ffc11-125">a conoscenza</span><span class="sxs-lookup"><span data-stu-id="ffc11-125">unaware</span></span></td>
<td><p><span data-ttu-id="ffc11-126">N/d (nessuna impostazione dpiAware nel manifesto)</span><span class="sxs-lookup"><span data-stu-id="ffc11-126">N/A (no dpiAware setting in manifest)</span></span></p>
<p><span data-ttu-id="ffc11-127">oppure</span><span class="sxs-lookup"><span data-stu-id="ffc11-127">or</span></span></p>
<p><span data-ttu-id="ffc11-128">&lt;dpiAware &gt; false &lt; /dpiAware&gt;</span><span class="sxs-lookup"><span data-stu-id="ffc11-128">&lt;dpiAware&gt;false&lt;/dpiAware&gt;</span></span></p></td>
<td><span data-ttu-id="ffc11-129">&lt;&gt;/DpiAwareness dpiAwareness incompatibili &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="ffc11-129">&lt;dpiAwareness&gt;unaware&lt;/dpiAwareness&gt;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ffc11-130">Compatibile con il sistema</span><span class="sxs-lookup"><span data-stu-id="ffc11-130">System aware</span></span></td>
<td><span data-ttu-id="ffc11-131">&lt;dpiAware &gt; true &lt; /dpiAware&gt;</span><span class="sxs-lookup"><span data-stu-id="ffc11-131">&lt;dpiAware&gt;true&lt;/dpiAware&gt;</span></span></td>
<td><span data-ttu-id="ffc11-132">&lt;&gt;/dpiAwareness di sistema dpiAwareness &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="ffc11-132">&lt;dpiAwareness&gt;system&lt;/dpiAwareness&gt;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ffc11-133">Per monitoraggio</span><span class="sxs-lookup"><span data-stu-id="ffc11-133">Per Monitor</span></span></td>
<td><span data-ttu-id="ffc11-134">&lt;dpiAware &gt; true/PM &lt; dpiAware&gt;</span><span class="sxs-lookup"><span data-stu-id="ffc11-134">&lt;dpiAware&gt;true/pm&lt;dpiAware&gt;</span></span></td>
<td><span data-ttu-id="ffc11-135">&lt;dpiAwareness &gt; PerMonitor &lt; /dpiAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="ffc11-135">&lt;dpiAwareness&gt;PerMonitor&lt;/dpiAwareness&gt;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ffc11-136">Per monitor V2</span><span class="sxs-lookup"><span data-stu-id="ffc11-136">Per Monitor V2</span></span></td>
<td><span data-ttu-id="ffc11-137">Non supportato</span><span class="sxs-lookup"><span data-stu-id="ffc11-137">Not supported</span></span></td>
<td><span data-ttu-id="ffc11-138">&lt;dpiAwareness &gt; PerMonitorV2 &lt; /dpiAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="ffc11-138">&lt;dpiAwareness&gt;PerMonitorV2&lt;/dpiAwareness&gt;</span></span></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="ffc11-139">Nell'esempio seguente vengono illustrate le \<dpiAwareness\> \<dpiAware\> Impostazioni e utilizzate nello stesso file manifesto per configurare il comportamento di riconoscimento dpi predefinito del processo per le diverse versioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="ffc11-139">The sample below shows both the \<dpiAwareness\> and the \<dpiAware\> settings being used within the same manifest file to configure process-default DPI awareness behavior for different versions of Windows.</span></span>

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

## <a name="setting-default-awareness-programmatically"></a><span data-ttu-id="ffc11-140">Impostazione della consapevolezza predefinita a livello di codice</span><span class="sxs-lookup"><span data-stu-id="ffc11-140">Setting default awareness programmatically</span></span>

<span data-ttu-id="ffc11-141">Sebbene non sia consigliato, è possibile impostare la consapevolezza DPI predefinita a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="ffc11-141">Although it is not recommended, it is possible to set the default DPI awareness programmatically.</span></span> <span data-ttu-id="ffc11-142">Una volta creata una finestra (HWND) nel processo, la modifica della modalità di riconoscimento DPI non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="ffc11-142">Once a window (an HWND) has been created in your process, changing the DPI awareness mode is no longer supported.</span></span> <span data-ttu-id="ffc11-143">Se si imposta la modalità di riconoscimento DPI predefinita del processo a livello di codice, è necessario chiamare l'API corrispondente prima che siano stati creati HWND.</span><span class="sxs-lookup"><span data-stu-id="ffc11-143">If you are setting the process-default DPI awareness mode programmatically, you must call the corresponding API before any HWNDs have been created.</span></span>

<span data-ttu-id="ffc11-144">Sono disponibili più API che consentono di specificare la consapevolezza DPI predefinita per il processo.</span><span class="sxs-lookup"><span data-stu-id="ffc11-144">There are multiple APIs that let you specify the default DPI awareness for your process.</span></span> <span data-ttu-id="ffc11-145">L'API consigliata corrente è [**SetProcessDpiAwarenessContext**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\)), perché le API precedenti offrono meno funzionalità.</span><span class="sxs-lookup"><span data-stu-id="ffc11-145">The current recommended API is [**SetProcessDpiAwarenessContext**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\)), as older APIs offer less functionality.</span></span>

 

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
<th><span data-ttu-id="ffc11-146">API</span><span class="sxs-lookup"><span data-stu-id="ffc11-146">API</span></span></th>
<th><span data-ttu-id="ffc11-147">Versione minima di Windows</span><span class="sxs-lookup"><span data-stu-id="ffc11-147">Minimum version of Windows</span></span></th>
<th><span data-ttu-id="ffc11-148">DPI non a conoscenza</span><span class="sxs-lookup"><span data-stu-id="ffc11-148">DPI Unaware</span></span></th>
<th><span data-ttu-id="ffc11-149">Compatibile con DPI di sistema</span><span class="sxs-lookup"><span data-stu-id="ffc11-149">System DPI Aware</span></span></th>
<th><span data-ttu-id="ffc11-150">Compatibile con DPI per monitor</span><span class="sxs-lookup"><span data-stu-id="ffc11-150">Per Monitor DPI Aware</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ffc11-151"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDpiAware</a></span><span class="sxs-lookup"><span data-stu-id="ffc11-151"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDpiAware</a></span></span></td>
<td><span data-ttu-id="ffc11-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ffc11-152">Windows Vista</span></span></td>
<td><span data-ttu-id="ffc11-153">N/D</span><span class="sxs-lookup"><span data-stu-id="ffc11-153">N/A</span></span></td>
<td><span data-ttu-id="ffc11-154">SetProcessDpiAware()</span><span class="sxs-lookup"><span data-stu-id="ffc11-154">SetProcessDpiAware()</span></span></td>
<td><span data-ttu-id="ffc11-155">N/D</span><span class="sxs-lookup"><span data-stu-id="ffc11-155">N/A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ffc11-156"><a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>SetProcessDpiAwareness</strong></a></span><span class="sxs-lookup"><span data-stu-id="ffc11-156"><a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>SetProcessDpiAwareness</strong></a></span></span></td>
<td><span data-ttu-id="ffc11-157">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ffc11-157">Windows 8.1</span></span></td>
<td><span data-ttu-id="ffc11-158">SetProcessDpiAwareness (PROCESS_DPI_UNAWARE)</span><span class="sxs-lookup"><span data-stu-id="ffc11-158">SetProcessDpiAwareness(PROCESS_DPI_UNAWARE)</span></span></td>
<td><span data-ttu-id="ffc11-159">SetProcessDpiAwareness (PROCESS_DPI_SYSTEM_DPI_AWARE)</span><span class="sxs-lookup"><span data-stu-id="ffc11-159">SetProcessDpiAwareness(PROCESS_DPI_SYSTEM_DPI_AWARE)</span></span></td>
<td><span data-ttu-id="ffc11-160">SetProcessDpiAwareness (PROCESS_DPI_PER_MONITOR_DPI_AWARE)</span><span class="sxs-lookup"><span data-stu-id="ffc11-160">SetProcessDpiAwareness(PROCESS_DPI_PER_MONITOR_DPI_AWARE)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ffc11-161"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>SetProcessDpiAwarenessContext</strong></a></span><span class="sxs-lookup"><span data-stu-id="ffc11-161"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>SetProcessDpiAwarenessContext</strong></a></span></span></td>
<td><span data-ttu-id="ffc11-162">Windows 10 versione 1607</span><span class="sxs-lookup"><span data-stu-id="ffc11-162">Windows 10, version 1607</span></span></td>
<td><span data-ttu-id="ffc11-163">SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_UNAWARE)</span><span class="sxs-lookup"><span data-stu-id="ffc11-163">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_UNAWARE)</span></span></td>
<td><span data-ttu-id="ffc11-164">SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_SYSTEM_AWARE)</span><span class="sxs-lookup"><span data-stu-id="ffc11-164">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_SYSTEM_AWARE)</span></span></td>
<td><p><span data-ttu-id="ffc11-165">SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)</span><span class="sxs-lookup"><span data-stu-id="ffc11-165">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)</span></span></p>
<p><span data-ttu-id="ffc11-166">SetProcessDpiAwarenessContext (DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)</span><span class="sxs-lookup"><span data-stu-id="ffc11-166">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="process-default-vs-thread-default"></a><span data-ttu-id="ffc11-167">Processo-predefinito rispetto a thread predefinito</span><span class="sxs-lookup"><span data-stu-id="ffc11-167">Process-default vs. Thread default</span></span>

<span data-ttu-id="ffc11-168">Questo documento si riferisce all'impostazione della consapevolezza DPI predefinita per il processo.</span><span class="sxs-lookup"><span data-stu-id="ffc11-168">This document refers to setting the default DPI awareness for your process.</span></span> <span data-ttu-id="ffc11-169">Questo è dovuto al fatto che in Windows 10 è stato introdotto il supporto per l'esecuzione di più di una modalità di riconoscimento DPI all'interno di un singolo processo (prima di Windows 10, l'intero processo doveva essere conforme a una sola modalità di riconoscimento DPI).</span><span class="sxs-lookup"><span data-stu-id="ffc11-169">This is because Windows 10 introduced support for running more than one DPI awareness mode within a single process (prior to Windows 10, the entire process had to conform to a single DPI awareness mode).</span></span> <span data-ttu-id="ffc11-170">Il supporto per l'esecuzione di più modalità di riconoscimento DPI all'interno di un processo viene definito "scalabilità DPI in modalità mista".</span><span class="sxs-lookup"><span data-stu-id="ffc11-170">Support for running more than one DPI awareness mode within a process is referred to as "mixed-mode DPI scaling".</span></span> <span data-ttu-id="ffc11-171">Quando si usa il ridimensionamento DPI in modalità mista all'interno del processo, ogni finestra di primo livello può essere eseguita in una modalità di riconoscimento DPI che può essere diversa da quella del processo predefinito.</span><span class="sxs-lookup"><span data-stu-id="ffc11-171">When using mixed-mode DPI scaling within your process, each top-level Window can run in a DPI awareness mode that may be different than that of the process default.</span></span> <span data-ttu-id="ffc11-172">A meno che non venga specificato in modo esplicito, al momento della creazione ogni thread utilizzerà per impostazione predefinita il processo predefinito.</span><span class="sxs-lookup"><span data-stu-id="ffc11-172">Unless explicitly specified, each thread will default to the process default when created.</span></span> <span data-ttu-id="ffc11-173">Per altre informazioni sul ridimensionamento DPI in modalità mista, vedere l'articolo relativo alla [scalabilità dpi in modalità mista](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) .</span><span class="sxs-lookup"><span data-stu-id="ffc11-173">For more information about mixed-mode DPI scaling, refer to the [Mixed-Mode DPI Scaling](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) article.</span></span>

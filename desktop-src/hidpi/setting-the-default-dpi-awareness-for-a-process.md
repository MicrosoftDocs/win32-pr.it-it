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
# <a name="setting-the-default-dpi-awareness-for-a-process"></a><span data-ttu-id="f79da-103">Impostazione della sensibilità DPI predefinita per un processo</span><span class="sxs-lookup"><span data-stu-id="f79da-103">Setting the default DPI awareness for a process</span></span>

<span data-ttu-id="f79da-104">Le applicazioni desktop in Windows possono essere eseguite in modalità di riconoscimento DPI diverse.</span><span class="sxs-lookup"><span data-stu-id="f79da-104">Desktop applications on Windows can run in different DPI awareness modes.</span></span> <span data-ttu-id="f79da-105">Queste modalità consentono un comportamento di ridimensionamento DPI diverso e possono usare spazi di coordinate diversi.</span><span class="sxs-lookup"><span data-stu-id="f79da-105">These modes enable different DPI scaling behavior and can use different coordinate spaces.</span></span> <span data-ttu-id="f79da-106">Per altre informazioni sul riconoscimento DPI, vedere Sviluppo di applicazioni desktop con [valori DPI](https://msdn.microsoft.com/library/mt843498\(v=vs.85\)) alti Windows.</span><span class="sxs-lookup"><span data-stu-id="f79da-106">For more information on DPI awareness, see [High DPI Desktop Application Development on Windows.](https://msdn.microsoft.com/library/mt843498\(v=vs.85\))</span></span> <span data-ttu-id="f79da-107">È importante impostare in modo esplicito la modalità di riconoscimento DPI predefinita del processo per evitare comportamenti imprevisti.</span><span class="sxs-lookup"><span data-stu-id="f79da-107">It is important that you explicitly set the default DPI awareness mode of your process so as to avoid unexpected behavior.</span></span>

<span data-ttu-id="f79da-108">Esistono due metodi principali per specificare il riconoscimento DPI predefinito di un processo:</span><span class="sxs-lookup"><span data-stu-id="f79da-108">There are two main methods to specify the default DPI awareness of a process:</span></span>

<span data-ttu-id="f79da-109">Da 1 \) a un'impostazione del manifesto dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="f79da-109">1\) through an application manifest setting</span></span>

<span data-ttu-id="f79da-110">2 a \) livello di codice tramite una chiamata API</span><span class="sxs-lookup"><span data-stu-id="f79da-110">2\) programmatically through an API call</span></span>

<span data-ttu-id="f79da-111">È consigliabile specificare il riconoscimento DPI del processo predefinito tramite un'impostazione del manifesto.</span><span class="sxs-lookup"><span data-stu-id="f79da-111">We recommended that you specify the default process DPI awareness via a manifest setting.</span></span> <span data-ttu-id="f79da-112">Anche se è supportata la specifica dell'impostazione predefinita tramite API, non è consigliabile.</span><span class="sxs-lookup"><span data-stu-id="f79da-112">While specifying the default via API is supported, it is not recommended.</span></span>

## <a name="setting-default-awareness-with-the-application-manifest"></a><span data-ttu-id="f79da-113">Impostazione della consapevolezza predefinita con il manifesto dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="f79da-113">Setting default awareness with the application manifest</span></span>

<span data-ttu-id="f79da-114">Sono disponibili due impostazioni del manifesto che consentono di specificare la modalità di riconoscimento DPI predefinita del processo: \<dpiAwareness\> e \<dpiAware\> .</span><span class="sxs-lookup"><span data-stu-id="f79da-114">There are two manifest settings that enable you to specify the process default DPI awareness mode: \<dpiAwareness\> and \<dpiAware\>.</span></span> <span data-ttu-id="f79da-115">\<dpiAware\>è stato introdotto in Windows Vista e consente solo l'impostazione predefinita del processo sulla consapevolezza del sistema.</span><span class="sxs-lookup"><span data-stu-id="f79da-115">\<dpiAware\> was introduced in Windows Vista and only enables your process default to be set to system awareness.</span></span> <span data-ttu-id="f79da-116">\<dpiAwareness\>è stato introdotto in Windows 10 versione 1607 e consente di specificare un elenco ordinato di modalità di riconoscimento DPI predefinite del processo.</span><span class="sxs-lookup"><span data-stu-id="f79da-116">\<dpiAwareness\> was introduced in Windows 10, version 1607 and enables you to specify an ordered list of process-default DPI awareness modes.</span></span> <span data-ttu-id="f79da-117">In questo modo è possibile impostare le modalità di riconoscimento DPI di backup, che verranno usate se l'applicazione viene eseguita in una versione di Windows non è in grado di supportare la prima modalità di riconoscimento specificata.</span><span class="sxs-lookup"><span data-stu-id="f79da-117">This enables you to set backup DPI awareness modes, which will be used if your application is ran on a version of Windows unable to support the first awareness mode specified.</span></span> <span data-ttu-id="f79da-118">Nelle versioni precedenti di Windows, il tag più \<dpiAwareness\> recente verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="f79da-118">On older versions of Windows, the newer \<dpiAwareness\> tag will be ignored.</span></span> <span data-ttu-id="f79da-119">Ciò significa che è possibile usare entrambe queste impostazioni del manifesto per abilitare uno scenario in cui l'impostazione predefinita del processo potrebbe essere il riconoscimento del sistema per la versione precedente di Windows mentre è Per-Monitor in versioni successive a Windows 10, versione 1607.</span><span class="sxs-lookup"><span data-stu-id="f79da-119">This means that you can use both of these manifest settings to enable a scenario where your process default could be system awareness on older version of Windows while being Per-Monitor on versions greater than Windows 10, version 1607.</span></span> <span data-ttu-id="f79da-120">In Windows 10 versione 1607 e attivata, l'impostazione viene ignorata \<dpiAware\> se \<dpiAwareness\> l'elemento è presente.</span><span class="sxs-lookup"><span data-stu-id="f79da-120">On Windows 10, version 1607, and on, the \<dpiAware\> setting is ignored if the \<dpiAwareness\> element is present.</span></span>

<span data-ttu-id="f79da-121">La tabella seguente illustra come specificare diverse modalità di riconoscimento DPI predefinite del processo usando le due impostazioni del manifesto:</span><span class="sxs-lookup"><span data-stu-id="f79da-121">The table below shows how to specify different process-default DPI awareness modes using the two manifest settings:</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f79da-122">Elaborare la modalità di riconoscimento DPI predefinita</span><span class="sxs-lookup"><span data-stu-id="f79da-122">Process default DPI awareness mode</span></span></th>
<th><span data-ttu-id="f79da-123">&lt;Impostazione &gt; dpiAware</span><span class="sxs-lookup"><span data-stu-id="f79da-123">&lt;dpiAware&gt; setting</span></span></th>
<th><span data-ttu-id="f79da-124">&lt;Impostazione dpiAwareness &gt; (Windows 10, versione 1607 e successive)</span><span class="sxs-lookup"><span data-stu-id="f79da-124">&lt;dpiAwareness&gt; setting (Windows 10, version 1607 and later)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f79da-125">Ignari</span><span class="sxs-lookup"><span data-stu-id="f79da-125">unaware</span></span></td>
<td><p><span data-ttu-id="f79da-126">N/D (nessuna impostazione dpiAware nel manifesto)</span><span class="sxs-lookup"><span data-stu-id="f79da-126">N/A (no dpiAware setting in manifest)</span></span></p>
<p><span data-ttu-id="f79da-127">oppure</span><span class="sxs-lookup"><span data-stu-id="f79da-127">or</span></span></p>
<p><span data-ttu-id="f79da-128">&lt;dpiAware &gt; false &lt; /dpiAware&gt;</span><span class="sxs-lookup"><span data-stu-id="f79da-128">&lt;dpiAware&gt;false&lt;/dpiAware&gt;</span></span></p></td>
<td><span data-ttu-id="f79da-129">&lt;dpiAwareness &gt; unware &lt; /dpiAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="f79da-129">&lt;dpiAwareness&gt;unaware&lt;/dpiAwareness&gt;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f79da-130">In grado di riconoscere il sistema</span><span class="sxs-lookup"><span data-stu-id="f79da-130">System aware</span></span></td>
<td><span data-ttu-id="f79da-131">&lt;dpiAware &gt; true &lt; /dpiAware&gt;</span><span class="sxs-lookup"><span data-stu-id="f79da-131">&lt;dpiAware&gt;true&lt;/dpiAware&gt;</span></span></td>
<td><span data-ttu-id="f79da-132">&lt;dpiAwareness &gt; system &lt; /dpiAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="f79da-132">&lt;dpiAwareness&gt;system&lt;/dpiAwareness&gt;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f79da-133">Per Monitor</span><span class="sxs-lookup"><span data-stu-id="f79da-133">Per Monitor</span></span></td>
<td><span data-ttu-id="f79da-134">&lt;dpiAware &gt; true/pm &lt; dpiAware&gt;</span><span class="sxs-lookup"><span data-stu-id="f79da-134">&lt;dpiAware&gt;true/pm&lt;dpiAware&gt;</span></span></td>
<td><span data-ttu-id="f79da-135">&lt;dpiAwareness &gt; PerMonitor &lt; /dpiAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="f79da-135">&lt;dpiAwareness&gt;PerMonitor&lt;/dpiAwareness&gt;</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f79da-136">Per Monitor V2</span><span class="sxs-lookup"><span data-stu-id="f79da-136">Per Monitor V2</span></span></td>
<td><span data-ttu-id="f79da-137">Non supportato</span><span class="sxs-lookup"><span data-stu-id="f79da-137">Not supported</span></span></td>
<td><span data-ttu-id="f79da-138">&lt;dpiAwareness &gt; PerMonitorV2 &lt; /dpiAwareness&gt;</span><span class="sxs-lookup"><span data-stu-id="f79da-138">&lt;dpiAwareness&gt;PerMonitorV2&lt;/dpiAwareness&gt;</span></span></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="f79da-139">L'esempio seguente illustra le impostazioni e usate all'interno dello stesso file manifesto per configurare il comportamento di riconoscimento DPI predefinito del processo per versioni diverse \<dpiAwareness\> \<dpiAware\> di Windows.</span><span class="sxs-lookup"><span data-stu-id="f79da-139">The sample below shows both the \<dpiAwareness\> and the \<dpiAware\> settings being used within the same manifest file to configure process-default DPI awareness behavior for different versions of Windows.</span></span>

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

## <a name="setting-default-awareness-programmatically"></a><span data-ttu-id="f79da-140">Impostazione della consapevolezza predefinita a livello di codice</span><span class="sxs-lookup"><span data-stu-id="f79da-140">Setting default awareness programmatically</span></span>

<span data-ttu-id="f79da-141">Anche se non è consigliabile, è possibile impostare la consapevolezza DPI predefinita a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="f79da-141">Although it is not recommended, it is possible to set the default DPI awareness programmatically.</span></span> <span data-ttu-id="f79da-142">Dopo aver creato una finestra (HWND) nel processo, la modifica della modalità di riconoscimento DPI non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="f79da-142">Once a window (an HWND) has been created in your process, changing the DPI awareness mode is no longer supported.</span></span> <span data-ttu-id="f79da-143">Se si imposta la modalità di riconoscimento DPI predefinita del processo a livello di codice, è necessario chiamare l'API corrispondente prima di creare gli HWND.</span><span class="sxs-lookup"><span data-stu-id="f79da-143">If you are setting the process-default DPI awareness mode programmatically, you must call the corresponding API before any HWNDs have been created.</span></span>

<span data-ttu-id="f79da-144">Sono disponibili più API che consentono di specificare la consapevolezza DPI predefinita per il processo.</span><span class="sxs-lookup"><span data-stu-id="f79da-144">There are multiple APIs that let you specify the default DPI awareness for your process.</span></span> <span data-ttu-id="f79da-145">L'API consigliata corrente [**è SetProcessDpiAwarenessContext,**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\))perché le API meno recenti offrono meno funzionalità.</span><span class="sxs-lookup"><span data-stu-id="f79da-145">The current recommended API is [**SetProcessDpiAwarenessContext**](https://msdn.microsoft.com/library/mt807676\(v=vs.85\)), as older APIs offer less functionality.</span></span>

 

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
<th><span data-ttu-id="f79da-146">API</span><span class="sxs-lookup"><span data-stu-id="f79da-146">API</span></span></th>
<th><span data-ttu-id="f79da-147">Versione minima di Windows</span><span class="sxs-lookup"><span data-stu-id="f79da-147">Minimum version of Windows</span></span></th>
<th><span data-ttu-id="f79da-148">DPI inconsapevole</span><span class="sxs-lookup"><span data-stu-id="f79da-148">DPI Unaware</span></span></th>
<th><span data-ttu-id="f79da-149">In grado di riconoscere DPI di sistema</span><span class="sxs-lookup"><span data-stu-id="f79da-149">System DPI Aware</span></span></th>
<th><span data-ttu-id="f79da-150">Supporto DPI per monitor</span><span class="sxs-lookup"><span data-stu-id="f79da-150">Per Monitor DPI Aware</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f79da-151"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDPIAware</a></span><span class="sxs-lookup"><span data-stu-id="f79da-151"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiaware">SetProcessDPIAware</a></span></span></td>
<td><span data-ttu-id="f79da-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f79da-152">Windows Vista</span></span></td>
<td><span data-ttu-id="f79da-153">N/D</span><span class="sxs-lookup"><span data-stu-id="f79da-153">N/A</span></span></td>
<td><span data-ttu-id="f79da-154">SetProcessDPIAware()</span><span class="sxs-lookup"><span data-stu-id="f79da-154">SetProcessDPIAware()</span></span></td>
<td><span data-ttu-id="f79da-155">N/D</span><span class="sxs-lookup"><span data-stu-id="f79da-155">N/A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f79da-156"><a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>SetProcessDpiAwareness</strong></a></span><span class="sxs-lookup"><span data-stu-id="f79da-156"><a href="/windows/win32/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness"><strong>SetProcessDpiAwareness</strong></a></span></span></td>
<td><span data-ttu-id="f79da-157">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f79da-157">Windows 8.1</span></span></td>
<td><span data-ttu-id="f79da-158">SetProcessDpiAwareness(PROCESS_DPI_UNAWARE)</span><span class="sxs-lookup"><span data-stu-id="f79da-158">SetProcessDpiAwareness(PROCESS_DPI_UNAWARE)</span></span></td>
<td><span data-ttu-id="f79da-159">SetProcessDpiAwareness(PROCESS_SYSTEM_DPI_AWARE)</span><span class="sxs-lookup"><span data-stu-id="f79da-159">SetProcessDpiAwareness(PROCESS_SYSTEM_DPI_AWARE)</span></span></td>
<td><span data-ttu-id="f79da-160">SetProcessDpiAwareness(PROCESS_PER_MONITOR_DPI_AWARE)</span><span class="sxs-lookup"><span data-stu-id="f79da-160">SetProcessDpiAwareness(PROCESS_PER_MONITOR_DPI_AWARE)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f79da-161"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>SetProcessDpiAwarenessContext</strong></a></span><span class="sxs-lookup"><span data-stu-id="f79da-161"><a href="/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext"><strong>SetProcessDpiAwarenessContext</strong></a></span></span></td>
<td><span data-ttu-id="f79da-162">Windows 10 versione 1607</span><span class="sxs-lookup"><span data-stu-id="f79da-162">Windows 10, version 1607</span></span></td>
<td><span data-ttu-id="f79da-163">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_UNAWARE)</span><span class="sxs-lookup"><span data-stu-id="f79da-163">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_UNAWARE)</span></span></td>
<td><span data-ttu-id="f79da-164">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_SYSTEM_AWARE)</span><span class="sxs-lookup"><span data-stu-id="f79da-164">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_SYSTEM_AWARE)</span></span></td>
<td><p><span data-ttu-id="f79da-165">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)</span><span class="sxs-lookup"><span data-stu-id="f79da-165">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE)</span></span></p>
<p><span data-ttu-id="f79da-166">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)</span><span class="sxs-lookup"><span data-stu-id="f79da-166">SetProcessDpiAwarenessContext(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2)</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="process-default-vs-thread-default"></a><span data-ttu-id="f79da-167">Impostazione predefinita del processo e impostazione predefinita del thread</span><span class="sxs-lookup"><span data-stu-id="f79da-167">Process-default vs. Thread default</span></span>

<span data-ttu-id="f79da-168">Questo documento si riferisce all'impostazione della sensibilità DPI predefinita per il processo.</span><span class="sxs-lookup"><span data-stu-id="f79da-168">This document refers to setting the default DPI awareness for your process.</span></span> <span data-ttu-id="f79da-169">Ciò è dovuto al fatto che Windows 10 introdotto il supporto per l'esecuzione di più modalità di riconoscimento DPI all'interno di un singolo processo (prima di Windows 10, l'intero processo doveva essere conforme a una singola modalità di riconoscimento DPI).</span><span class="sxs-lookup"><span data-stu-id="f79da-169">This is because Windows 10 introduced support for running more than one DPI awareness mode within a single process (prior to Windows 10, the entire process had to conform to a single DPI awareness mode).</span></span> <span data-ttu-id="f79da-170">Il supporto per l'esecuzione di più modalità di riconoscimento DPI all'interno di un processo è detto "ridimensionamento DPI in modalità mista".</span><span class="sxs-lookup"><span data-stu-id="f79da-170">Support for running more than one DPI awareness mode within a process is referred to as "mixed-mode DPI scaling".</span></span> <span data-ttu-id="f79da-171">Quando si usa il ridimensionamento DPI in modalità mista all'interno del processo, ogni finestra di primo livello può essere eseguita in una modalità di riconoscimento DPI che può essere diversa da quella predefinita del processo.</span><span class="sxs-lookup"><span data-stu-id="f79da-171">When using mixed-mode DPI scaling within your process, each top-level Window can run in a DPI awareness mode that may be different than that of the process default.</span></span> <span data-ttu-id="f79da-172">Se non specificato in modo esplicito, ogni thread verrà impostato sul valore predefinito del processo al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="f79da-172">Unless explicitly specified, each thread will default to the process default when created.</span></span> <span data-ttu-id="f79da-173">Per altre informazioni sul ridimensionamento DPI in modalità mista, vedere l'articolo [Ridimensionamento DPI](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) in modalità mista.</span><span class="sxs-lookup"><span data-stu-id="f79da-173">For more information about mixed-mode DPI scaling, refer to the [Mixed-Mode DPI Scaling](https://msdn.microsoft.com/library/mt744321\(v=vs.85\)) article.</span></span>

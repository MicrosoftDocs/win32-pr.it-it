---
description: Classe del tipo di evento per l'evento di intestazione del file di log. Questa classe contiene informazioni sulla sessione di traccia eventi.
ms.assetid: 3d0c4044-da06-4850-95c4-99b4ea28fcd9
title: Classe EventTrace_Header
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventTrace_Header
- EventTrace_Header.BufferSize
- EventTrace_Header.Version
- EventTrace_Header.ProviderVersion
- EventTrace_Header.NumberOfProcessors
- EventTrace_Header.EndTime
- EventTrace_Header.TimerResolution
- EventTrace_Header.MaxFileSize
- EventTrace_Header.LogFileMode
- EventTrace_Header.BuffersWritten
- EventTrace_Header.StartBuffers
- EventTrace_Header.PointerSize
- EventTrace_Header.EventsLost
- EventTrace_Header.CPUSpeed
- EventTrace_Header.LoggerName
- EventTrace_Header.LogFileName
- EventTrace_Header.TimeZoneInformation
- EventTrace_Header.BootTime
- EventTrace_Header.PerfFreq
- EventTrace_Header.StartTime
- EventTrace_Header.ReservedFlags
- EventTrace_Header.BuffersLost
api_type:
- NA
api_location: ''
ms.openlocfilehash: dea803849d6aa15c2a3a14deb850d85ade569116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526863"
---
# <a name="eventtrace_header-class"></a><span data-ttu-id="2bb29-104">\_Classe di intestazione EventTrace</span><span class="sxs-lookup"><span data-stu-id="2bb29-104">EventTrace\_Header class</span></span>

<span data-ttu-id="2bb29-105">Classe del tipo di evento per l'evento di intestazione del file di log.</span><span class="sxs-lookup"><span data-stu-id="2bb29-105">The event type class for the log file header event.</span></span> <span data-ttu-id="2bb29-106">Questa classe contiene informazioni sulla sessione di traccia eventi.</span><span class="sxs-lookup"><span data-stu-id="2bb29-106">This class contains information about the event tracing session.</span></span>

<span data-ttu-id="2bb29-107">La sintassi seguente è semplificata dal codice MOF.</span><span class="sxs-lookup"><span data-stu-id="2bb29-107">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bb29-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2bb29-108">Syntax</span></span>

``` syntax
[EventType(0)]
class EventTrace_Header : EventTraceEvent
{
  uint32 BufferSize;
  uint32 Version;
  uint32 ProviderVersion;
  uint32 NumberOfProcessors;
  uint64 EndTime;
  uint32 TimerResolution;
  uint32 MaxFileSize;
  uint32 LogFileMode;
  uint32 BuffersWritten;
  uint32 StartBuffers;
  uint32 PointerSize;
  uint32 EventsLost;
  uint32 CPUSpeed;
  uint32 LoggerName;
  uint32 LogFileName;
  uint8  TimeZoneInformation[];
  uint64 BootTime;
  uint64 PerfFreq;
  uint64 StartTime;
  uint32 ReservedFlags;
  uint32 BuffersLost;
};
```

## <a name="members"></a><span data-ttu-id="2bb29-109">Members</span><span class="sxs-lookup"><span data-stu-id="2bb29-109">Members</span></span>

<span data-ttu-id="2bb29-110">La classe dell' **\_ intestazione EventTrace** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2bb29-110">The **EventTrace\_Header** class has these types of members:</span></span>

-   [<span data-ttu-id="2bb29-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2bb29-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2bb29-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2bb29-112">Properties</span></span>

<span data-ttu-id="2bb29-113">La classe dell' **\_ intestazione EventTrace** include queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2bb29-113">The **EventTrace\_Header** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2bb29-114">**BootTime**</span><span class="sxs-lookup"><span data-stu-id="2bb29-114">**BootTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb29-115">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2bb29-115">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bb29-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-117">Qualificatori: **WmiDataId** (17)</span><span class="sxs-lookup"><span data-stu-id="2bb29-117">Qualifiers: **WmiDataId** (17)</span></span>
</dt> </dl>

<span data-ttu-id="2bb29-118">Ora in cui il sistema è stato avviato, in intervalli di 100 nanosecondi dalla mezzanotte del 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="2bb29-118">Time at which the system was started, in 100-nanosecond intervals since midnight, January 1, 1601.</span></span>

</dd> <dt>

<span data-ttu-id="2bb29-119">**BufferSize**</span><span class="sxs-lookup"><span data-stu-id="2bb29-119">**BufferSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb29-120">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2bb29-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bb29-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-122">Qualificatori: **WmiDataId** (1)</span><span class="sxs-lookup"><span data-stu-id="2bb29-122">Qualifiers: **WmiDataId** (1)</span></span>
</dt> </dl>

<span data-ttu-id="2bb29-123">Dimensioni dei buffer della sessione di traccia eventi, in kilobyte.</span><span class="sxs-lookup"><span data-stu-id="2bb29-123">Size of the event tracing session's buffers, in kilobytes.</span></span>

</dd> <dt>

<span data-ttu-id="2bb29-124">**BuffersLost**</span><span class="sxs-lookup"><span data-stu-id="2bb29-124">**BuffersLost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb29-125">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2bb29-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bb29-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-127">Qualificatori: **WmiDataId** (21)</span><span class="sxs-lookup"><span data-stu-id="2bb29-127">Qualifiers: **WmiDataId** (21)</span></span>
</dt> </dl>

<span data-ttu-id="2bb29-128">Numero totale di buffer persi.</span><span class="sxs-lookup"><span data-stu-id="2bb29-128">Total number of buffers lost.</span></span>

</dd> <dt>

<span data-ttu-id="2bb29-129">**BuffersWritten**</span><span class="sxs-lookup"><span data-stu-id="2bb29-129">**BuffersWritten**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb29-130">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2bb29-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bb29-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-132">Qualificatori: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="2bb29-132">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="2bb29-133">Numero totale di buffer scritti dalla sessione di traccia eventi.</span><span class="sxs-lookup"><span data-stu-id="2bb29-133">Total number of buffers written by the event tracing session.</span></span>

</dd> <dt>

<span data-ttu-id="2bb29-134">**CPUSpeed**</span><span class="sxs-lookup"><span data-stu-id="2bb29-134">**CPUSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb29-135">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2bb29-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bb29-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-137">Qualificatori: **WmiDataId** (13)</span><span class="sxs-lookup"><span data-stu-id="2bb29-137">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="2bb29-138">Velocità della CPU, in megahertz.</span><span class="sxs-lookup"><span data-stu-id="2bb29-138">CPU speed, in megahertz.</span></span>

<span data-ttu-id="2bb29-139">**Windows 2000:** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="2bb29-139">**Windows 2000:** Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="2bb29-140">**EndTime**</span><span class="sxs-lookup"><span data-stu-id="2bb29-140">**EndTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb29-141">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2bb29-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bb29-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-143">Qualificatori: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="2bb29-143">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="2bb29-144">Ora di arresto della sessione di traccia eventi, in intervalli di 100 nanosecondi dalla mezzanotte del 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="2bb29-144">Time at which the event tracing session stopped, in 100-nanosecond intervals since midnight, January 1, 1601.</span></span> <span data-ttu-id="2bb29-145">Questo valore può essere 0 se si utilizzano eventi in tempo reale o da un file di log in cui l'oggetto fornisce ancora la registrazione degli eventi.</span><span class="sxs-lookup"><span data-stu-id="2bb29-145">This value may be 0 if you are consuming events in real time or from a log file to which the provide is still logging events.</span></span>

</dd> <dt>

<span data-ttu-id="2bb29-146">**EventsLost**</span><span class="sxs-lookup"><span data-stu-id="2bb29-146">**EventsLost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb29-147">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2bb29-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bb29-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-149">Qualificatori: **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="2bb29-149">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="2bb29-150">Numero di eventi persi durante la sessione di traccia eventi.</span><span class="sxs-lookup"><span data-stu-id="2bb29-150">Number of events lost during the event tracing session.</span></span>

</dd> <dt>

<span data-ttu-id="2bb29-151">**LogFileMode**</span><span class="sxs-lookup"><span data-stu-id="2bb29-151">**LogFileMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb29-152">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2bb29-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bb29-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-154">Qualificatori: **WmiDataId** (8), **Format ("x")**</span><span class="sxs-lookup"><span data-stu-id="2bb29-154">Qualifiers: **WmiDataId** (8), **Format("x")**</span></span>
</dt> </dl>

<span data-ttu-id="2bb29-155">Modalità di registrazione corrente per la sessione di traccia eventi.</span><span class="sxs-lookup"><span data-stu-id="2bb29-155">Current logging mode for the event tracing session.</span></span> <span data-ttu-id="2bb29-156">Per un elenco di valori, vedere costanti della modalità di registrazione.</span><span class="sxs-lookup"><span data-stu-id="2bb29-156">For a list of values, see Logging Mode Constants.</span></span>

</dd> <dt>

<span data-ttu-id="2bb29-157">**LogFileName**</span><span class="sxs-lookup"><span data-stu-id="2bb29-157">**LogFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb29-158">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2bb29-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bb29-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-160">Qualificatori: **WmiDataId** (15), **puntatore**</span><span class="sxs-lookup"><span data-stu-id="2bb29-160">Qualifiers: **WmiDataId** (15), **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="2bb29-161">Nome del file di log di traccia eventi che contiene gli eventi.</span><span class="sxs-lookup"><span data-stu-id="2bb29-161">Name of the event tracing log file that contains the events.</span></span>

</dd> <dt>

<span data-ttu-id="2bb29-162">**Loggername**</span><span class="sxs-lookup"><span data-stu-id="2bb29-162">**LoggerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb29-163">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2bb29-163">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bb29-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-165">Qualificatori: **WmiDataId** (14), **puntatore**</span><span class="sxs-lookup"><span data-stu-id="2bb29-165">Qualifiers: **WmiDataId** (14), **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="2bb29-166">Nome della sessione di traccia eventi.</span><span class="sxs-lookup"><span data-stu-id="2bb29-166">Name of the event tracing session.</span></span>

</dd> <dt>

<span data-ttu-id="2bb29-167">**MaxFileSize**</span><span class="sxs-lookup"><span data-stu-id="2bb29-167">**MaxFileSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb29-168">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2bb29-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bb29-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-170">Qualificatori: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="2bb29-170">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="2bb29-171">Dimensioni massime del file di log, in megabyte.</span><span class="sxs-lookup"><span data-stu-id="2bb29-171">Maximum size of the log file, in megabytes.</span></span>

</dd> <dt>

<span data-ttu-id="2bb29-172">**NumberOfProcessors**</span><span class="sxs-lookup"><span data-stu-id="2bb29-172">**NumberOfProcessors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb29-173">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2bb29-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bb29-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-175">Qualificatori: **WmiDataId** (4)</span><span class="sxs-lookup"><span data-stu-id="2bb29-175">Qualifiers: **WmiDataId** (4)</span></span>
</dt> </dl>

<span data-ttu-id="2bb29-176">Numero di processori nel sistema.</span><span class="sxs-lookup"><span data-stu-id="2bb29-176">Number of processors on the system.</span></span>

</dd> <dt>

<span data-ttu-id="2bb29-177">**PerfFreq**</span><span class="sxs-lookup"><span data-stu-id="2bb29-177">**PerfFreq**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb29-178">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2bb29-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bb29-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-180">Qualificatori: **WmiDataId** (18)</span><span class="sxs-lookup"><span data-stu-id="2bb29-180">Qualifiers: **WmiDataId** (18)</span></span>
</dt> </dl>

<span data-ttu-id="2bb29-181">Frequenza del contatore delle prestazioni ad alta risoluzione, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="2bb29-181">Frequency of the high-resolution performance counter, if one exists.</span></span>

</dd> <dt>

<span data-ttu-id="2bb29-182">**PointerSize**</span><span class="sxs-lookup"><span data-stu-id="2bb29-182">**PointerSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb29-183">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2bb29-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bb29-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-185">Qualificatori: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="2bb29-185">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="2bb29-186">Dimensioni in byte del tipo di dati di un puntatore.</span><span class="sxs-lookup"><span data-stu-id="2bb29-186">Size of a pointer data type, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2bb29-187">**ProviderVersion**</span><span class="sxs-lookup"><span data-stu-id="2bb29-187">**ProviderVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb29-188">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2bb29-188">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bb29-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-190">Qualificatori: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="2bb29-190">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="2bb29-191">Numero di build del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2bb29-191">Build number of the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="2bb29-192">**ReservedFlags**</span><span class="sxs-lookup"><span data-stu-id="2bb29-192">**ReservedFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb29-193">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2bb29-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bb29-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-195">Qualificatori: **WmiDataId** (20)</span><span class="sxs-lookup"><span data-stu-id="2bb29-195">Qualifiers: **WmiDataId** (20)</span></span>
</dt> </dl>

<span data-ttu-id="2bb29-196">Riservato.</span><span class="sxs-lookup"><span data-stu-id="2bb29-196">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="2bb29-197">**StartBuffers**</span><span class="sxs-lookup"><span data-stu-id="2bb29-197">**StartBuffers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb29-198">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2bb29-198">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-199">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bb29-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-200">Qualificatori: **WmiDataId** (10)</span><span class="sxs-lookup"><span data-stu-id="2bb29-200">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="2bb29-201">Riservato.</span><span class="sxs-lookup"><span data-stu-id="2bb29-201">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="2bb29-202">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="2bb29-202">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb29-203">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2bb29-203">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bb29-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-205">Qualificatori: **WmiDataId** (19)</span><span class="sxs-lookup"><span data-stu-id="2bb29-205">Qualifiers: **WmiDataId** (19)</span></span>
</dt> </dl>

<span data-ttu-id="2bb29-206">Ora di inizio della sessione di traccia eventi, in intervalli di 100 nanosecondi dalla mezzanotte del 1 ° gennaio 1601.</span><span class="sxs-lookup"><span data-stu-id="2bb29-206">Time at which the event tracing session started, in 100-nanosecond intervals since midnight, January 1, 1601.</span></span>

</dd> <dt>

<span data-ttu-id="2bb29-207">**TimerResolution**</span><span class="sxs-lookup"><span data-stu-id="2bb29-207">**TimerResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb29-208">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2bb29-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bb29-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-210">Qualificatori: **WmiDataId** (6)</span><span class="sxs-lookup"><span data-stu-id="2bb29-210">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="2bb29-211">Risoluzione del timer hardware, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="2bb29-211">Resolution of the hardware timer, in units of 100 nanoseconds.</span></span>

</dd> <dt>

<span data-ttu-id="2bb29-212">**TimeZoneInformation**</span><span class="sxs-lookup"><span data-stu-id="2bb29-212">**TimeZoneInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb29-213">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="2bb29-213">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-214">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bb29-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-215">Qualificatori: **WmiDataId** (16), **estensione ("NoPrint")**, **Max** (176)</span><span class="sxs-lookup"><span data-stu-id="2bb29-215">Qualifiers: **WmiDataId** (16), **Extension("NoPrint")**, **Max** (176)</span></span>
</dt> </dl>

<span data-ttu-id="2bb29-216">Struttura [**di \_ \_ informazioni sul fuso orario**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) che contiene il fuso orario per i membri **BootTime**, **EndTime** e **StartTime** .</span><span class="sxs-lookup"><span data-stu-id="2bb29-216">A [**TIME\_ZONE\_INFORMATION**](/windows/win32/api/timezoneapi/ns-timezoneapi-time_zone_information) structure that contains the time zone for the **BootTime**, **EndTime** and **StartTime** members.</span></span>

</dd> <dt>

<span data-ttu-id="2bb29-217">**Versione**</span><span class="sxs-lookup"><span data-stu-id="2bb29-217">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb29-218">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2bb29-218">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-219">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2bb29-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb29-220">Qualificatori: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="2bb29-220">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="2bb29-221">Numero di versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2bb29-221">Version number of the operating system.</span></span> <span data-ttu-id="2bb29-222">A partire dai byte di ordine inferiore, i primi due byte contengono la versione principale, i due byte successivi contengono la versione secondaria, i due byte successivi contengono Service Pack versione principale e gli ultimi due byte contengono Service Pack versione secondaria.</span><span class="sxs-lookup"><span data-stu-id="2bb29-222">Starting with the low-order bytes, the first two bytes contain major version, the next two bytes contain minor version, the next two bytes contain service pack major version, and the last two bytes contain service pack minor version.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2bb29-223">Commenti</span><span class="sxs-lookup"><span data-stu-id="2bb29-223">Remarks</span></span>

<span data-ttu-id="2bb29-224">In genere, si desidera salvare i valori per le seguenti proprietà da utilizzare in un secondo momento durante l'elaborazione degli eventi dal file di log.</span><span class="sxs-lookup"><span data-stu-id="2bb29-224">Typically, you want to save the values for the following properties for use later when processing events from the log file.</span></span>

-   <span data-ttu-id="2bb29-225">**TimerResolution**: utilizzare con i membri **KernelTime** e **UserTime** della struttura [**dell' \_ \_ intestazione della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) per determinare il costo della CPU per un set di istruzioni.</span><span class="sxs-lookup"><span data-stu-id="2bb29-225">**TimerResolution**—use with the **KernelTime** and **UserTime** members of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure to determine the CPU cost for a set of instructions.</span></span> <span data-ttu-id="2bb29-226">Per informazioni dettagliate, vedere la sezione Osservazioni [**dell' \_ \_ intestazione della traccia dell'evento**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header).</span><span class="sxs-lookup"><span data-stu-id="2bb29-226">For details, see the Remarks section of [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header).</span></span>
-   <span data-ttu-id="2bb29-227">**POINTERSIZE**: per le proprietà che contengono il qualificatore del **puntatore** , usare questo valore per determinare la dimensione del puntatore.</span><span class="sxs-lookup"><span data-stu-id="2bb29-227">**PointerSize**—for properties that contain the **Pointer** qualifier, use this value to determine the size of the pointer.</span></span> <span data-ttu-id="2bb29-228">Si noti che questo valore potrebbe non essere accurato.</span><span class="sxs-lookup"><span data-stu-id="2bb29-228">Note that this value may not be accurate.</span></span> <span data-ttu-id="2bb29-229">Ad esempio, in un computer a 64 bit, un'applicazione a 32 bit registrerà puntatori a 4 byte. Tuttavia, la sessione imposterà **POINTERSIZE** su 8.</span><span class="sxs-lookup"><span data-stu-id="2bb29-229">For example, on a 64-bit computer, a 32-bit application will log 4-byte pointers; however, the session will set **PointerSize** to 8.</span></span>
-   <span data-ttu-id="2bb29-230">**LogFileMode**: consente di determinare se questa sessione è una sessione di logger privata.</span><span class="sxs-lookup"><span data-stu-id="2bb29-230">**LogFileMode**—use to determine if this session is a private logger session.</span></span> <span data-ttu-id="2bb29-231">Sono disponibili alcune proprietà che non contengono dati per le sessioni di logger privati.</span><span class="sxs-lookup"><span data-stu-id="2bb29-231">There are some properties that do not contain data for private logger sessions.</span></span> <span data-ttu-id="2bb29-232">Ad esempio, i membri **KernelTime** e **UserTime** della struttura [**dell' \_ \_ intestazione della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) .</span><span class="sxs-lookup"><span data-stu-id="2bb29-232">For example, the **KernelTime** and **UserTime** members of the [**EVENT\_TRACE\_HEADER**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bb29-233">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2bb29-233">Requirements</span></span>



| <span data-ttu-id="2bb29-234">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bb29-234">Requirement</span></span> | <span data-ttu-id="2bb29-235">Valore</span><span class="sxs-lookup"><span data-stu-id="2bb29-235">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="2bb29-236">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2bb29-236">Minimum supported client</span></span><br/> | <span data-ttu-id="2bb29-237">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2bb29-237">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2bb29-238">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2bb29-238">Minimum supported server</span></span><br/> | <span data-ttu-id="2bb29-239">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2bb29-239">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="2bb29-240">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2bb29-240">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bb29-241">**EventTraceEvent**</span><span class="sxs-lookup"><span data-stu-id="2bb29-241">**EventTraceEvent**</span></span>](eventtraceevent.md)
</dt> <dt>

[<span data-ttu-id="2bb29-242">**\_intestazione logfile \_ traccia**</span><span class="sxs-lookup"><span data-stu-id="2bb29-242">**TRACE\_LOGFILE\_HEADER**</span></span>](/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header)
</dt> </dl>

 

 

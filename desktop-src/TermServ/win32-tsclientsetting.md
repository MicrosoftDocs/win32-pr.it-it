---
title: Classe Win32_TSClientSetting
description: Definisce le impostazioni di configurazione per la \_ classe terminale Win32 correlate ai criteri di connessione.
ms.assetid: 438baf22-adc2-410e-bf9b-4b17a05c5ce4
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSClientSetting Servizi Desktop remoto
- Classe Win32_TSClientSetting Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSClientSetting
- Win32_TSClientSetting.Caption
- Win32_TSClientSetting.Description
- Win32_TSClientSetting.InstallDate
- Win32_TSClientSetting.Name
- Win32_TSClientSetting.Status
- Win32_TSClientSetting.TerminalName
- Win32_TSClientSetting.ConnectionPolicy
- Win32_TSClientSetting.ConnectClientDrivesAtLogon
- Win32_TSClientSetting.ConnectPrinterAtLogon
- Win32_TSClientSetting.DefaultToClientPrinter
- Win32_TSClientSetting.PolicySourceDefaultToClientPrinter
- Win32_TSClientSetting.WindowsPrinterMapping
- Win32_TSClientSetting.PolicySourceWindowsPrinterMapping
- Win32_TSClientSetting.LPTPortMapping
- Win32_TSClientSetting.PolicySourceLPTPortMapping
- Win32_TSClientSetting.COMPortMapping
- Win32_TSClientSetting.PolicySourceCOMPortMapping
- Win32_TSClientSetting.DriveMapping
- Win32_TSClientSetting.PolicySourceDriveMapping
- Win32_TSClientSetting.AudioMapping
- Win32_TSClientSetting.PolicySourceAudioMapping
- Win32_TSClientSetting.ClipboardMapping
- Win32_TSClientSetting.PolicySourceClipboardMapping
- Win32_TSClientSetting.ColorDepthPolicy
- Win32_TSClientSetting.PolicySourceColorDepthPolicy
- Win32_TSClientSetting.ColorDepth
- Win32_TSClientSetting.PolicySourceColorDepth
- Win32_TSClientSetting.MaxMonitors
- Win32_TSClientSetting.MaxXResolution
- Win32_TSClientSetting.MaxYResolution
- Win32_TSClientSetting.PolicySourceMaxMonitors
- Win32_TSClientSetting.PolicySourceMaxResolution
- Win32_TSClientSetting.PNPRedirection
- Win32_TSClientSetting.PolicySourcePNPRedirection
- Win32_TSClientSetting.AudioCaptureRedir
- Win32_TSClientSetting.PolicySourceAudioCaptureRedir
- Win32_TSClientSetting.VideoPlaybackRedir
- Win32_TSClientSetting.PolicySourceVideoPlaybackRedir
- Win32_TSClientSetting.AllowDwm
- Win32_TSClientSetting.PolicySourceAllowDwm
- Win32_TSClientSetting.PolicyAdvancedRemoteAppGraphics
- Win32_TSClientSetting.AdvancedRemoteAppGraphics
- Win32_TSClientSetting.RemoteSessionProfile
- Win32_TSClientSetting.PolicySourceRemoteSessionProfile
- Win32_TSClientSetting.AVC444ModePreferred
- Win32_TSClientSetting.PolicySourceAvc444ModePreferred
- Win32_TSClientSetting.EncodeImageQuality
- Win32_TSClientSetting.PolicySourceEncodeImageQuality
- Win32_TSClientSetting.HardwareGraphicsAdapter
- Win32_TSClientSetting.PolicySourceHardwareGraphicsAdapter
- Win32_TSClientSetting.SelectTransport
- Win32_TSClientSetting.PolicySourceSelectTransport
- Win32_TSClientSetting.SelectNetworkDetect
- Win32_TSClientSetting.PolicySourceSelectNetworkDetect
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 204f38570e1e023ca070ed1845e4574d9570b8ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121207"
---
# <a name="win32_tsclientsetting-class"></a><span data-ttu-id="bf81d-105">Win32 \_ TSClientSetting (classe)</span><span class="sxs-lookup"><span data-stu-id="bf81d-105">Win32\_TSClientSetting class</span></span>

<span data-ttu-id="bf81d-106">La classe WMI **Win32 \_ TSClientSetting** definisce le impostazioni di configurazione per la classe [**\_ terminale Win32**](win32-terminal.md) correlate ai criteri di connessione.</span><span class="sxs-lookup"><span data-stu-id="bf81d-106">The **Win32\_TSClientSetting** WMI class defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class related to connection policy.</span></span>

<span data-ttu-id="bf81d-107">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà definite ed ereditate, in ordine alfabetico.</span><span class="sxs-lookup"><span data-stu-id="bf81d-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="bf81d-108">Per informazioni di riferimento sui metodi, vedere la tabella dei metodi più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="bf81d-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf81d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf81d-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSCLIENTSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSClientSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ConnectionPolicy;
  uint32   ConnectClientDrivesAtLogon;
  uint32   ConnectPrinterAtLogon;
  uint32   DefaultToClientPrinter;
  uint32   PolicySourceDefaultToClientPrinter;
  uint32   WindowsPrinterMapping;
  uint32   PolicySourceWindowsPrinterMapping;
  uint32   LPTPortMapping;
  uint32   PolicySourceLPTPortMapping;
  uint32   COMPortMapping;
  uint32   PolicySourceCOMPortMapping;
  uint32   DriveMapping;
  uint32   PolicySourceDriveMapping;
  uint32   AudioMapping;
  uint32   PolicySourceAudioMapping;
  uint32   ClipboardMapping;
  uint32   PolicySourceClipboardMapping;
  uint32   ColorDepthPolicy;
  uint32   PolicySourceColorDepthPolicy;
  uint32   ColorDepth;
  uint32   PolicySourceColorDepth;
  uint32   MaxMonitors;
  uint32   MaxXResolution;
  uint32   MaxYResolution;
  uint32   PolicySourceMaxMonitors;
  uint32   PolicySourceMaxResolution;
  uint32   PNPRedirection;
  uint32   PolicySourcePNPRedirection;
  uint32   AudioCaptureRedir;
  uint32   PolicySourceAudioCaptureRedir;
  uint32   VideoPlaybackRedir;
  uint32   PolicySourceVideoPlaybackRedir;
  uint32   AllowDwm;
  uint32   PolicySourceAllowDwm;
  uint32   PolicyAdvancedRemoteAppGraphics;
  uint32   AdvancedRemoteAppGraphics;
  uint32   RemoteSessionProfile;
  uint32   PolicySourceRemoteSessionProfile;
  uint32   AVC444ModePreferred;
  uint32   PolicySourceAvc444ModePreferred;
  uint32   EncodeImageQuality;
  uint32   PolicySourceEncodeImageQuality;
  uint32   HardwareGraphicsAdapter;
  uint32   PolicySourceHardwareGraphicsAdapter;
  uint32   SelectTransport;
  uint32   PolicySourceSelectTransport;
  uint32   SelectNetworkDetect;
  uint32   PolicySourceSelectNetworkDetect;
};
```

## <a name="members"></a><span data-ttu-id="bf81d-110">Members</span><span class="sxs-lookup"><span data-stu-id="bf81d-110">Members</span></span>

<span data-ttu-id="bf81d-111">La classe **Win32 \_ TSClientSetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bf81d-111">The **Win32\_TSClientSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="bf81d-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="bf81d-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="bf81d-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bf81d-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bf81d-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="bf81d-114">Methods</span></span>

<span data-ttu-id="bf81d-115">La classe **Win32 \_ TSClientSetting** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="bf81d-115">The **Win32\_TSClientSetting** class has these methods.</span></span>



| <span data-ttu-id="bf81d-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="bf81d-116">Method</span></span>                                                                   | <span data-ttu-id="bf81d-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf81d-117">Description</span></span>                                                                                                                                                  |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf81d-118">**ConnectionSettings**</span><span class="sxs-lookup"><span data-stu-id="bf81d-118">**ConnectionSettings**</span></span>](win32-tsclientsetting-connectionsettings.md)   | <span data-ttu-id="bf81d-119">Imposta le proprietà **ConnectClientDrivesAtLogon**, **ConnectPrinterAtLogon** e **DefaultToClientPrinter** di questa classe.</span><span class="sxs-lookup"><span data-stu-id="bf81d-119">Sets the **ConnectClientDrivesAtLogon**, **ConnectPrinterAtLogon**, and **DefaultToClientPrinter** properties of this class.</span></span><br/>                      |
| [<span data-ttu-id="bf81d-120">**SetAllowDwm**</span><span class="sxs-lookup"><span data-stu-id="bf81d-120">**SetAllowDwm**</span></span>](setallowdwm-win32-tsclientsetting.md)                 | <span data-ttu-id="bf81d-121">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="bf81d-121">Not supported.</span></span><br/> <span data-ttu-id="bf81d-122">**Windows 7 e Windows Server 2008 R2:** Imposta la proprietà **AllowDwm** .</span><span class="sxs-lookup"><span data-stu-id="bf81d-122">**Windows 7 and Windows Server 2008 R2:** Sets the **AllowDwm** property.</span></span><br/>                                               |
| [<span data-ttu-id="bf81d-123">**SetClientProperty**</span><span class="sxs-lookup"><span data-stu-id="bf81d-123">**SetClientProperty**</span></span>](win32-tsclientsetting-setclientproperty.md)     | <span data-ttu-id="bf81d-124">Imposta la proprietà **LPTPortMapping**, **COMPortMapping**, **AudioMapping**, **ClipboardMapping**, **DriveMapping** o **WindowsPrinterMapping** .</span><span class="sxs-lookup"><span data-stu-id="bf81d-124">Sets the **LPTPortMapping**, **COMPortMapping**, **AudioMapping**, **ClipboardMapping**, **DriveMapping**, or **WindowsPrinterMapping** property.</span></span><br/> |
| [<span data-ttu-id="bf81d-125">**SetColorDepth**</span><span class="sxs-lookup"><span data-stu-id="bf81d-125">**SetColorDepth**</span></span>](win32-tsclientsetting-setcolordepth.md)             | <span data-ttu-id="bf81d-126">Imposta la proprietà **ColorDepth** .</span><span class="sxs-lookup"><span data-stu-id="bf81d-126">Sets the **ColorDepth** property.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="bf81d-127">**SetColorDepthPolicy**</span><span class="sxs-lookup"><span data-stu-id="bf81d-127">**SetColorDepthPolicy**</span></span>](win32-tsclientsetting-setcolordepthpolicy.md) | <span data-ttu-id="bf81d-128">Imposta la proprietà **ColorDepthPolicy** .</span><span class="sxs-lookup"><span data-stu-id="bf81d-128">Sets the **ColorDepthPolicy** property.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="bf81d-129">**SetMaxMonitors**</span><span class="sxs-lookup"><span data-stu-id="bf81d-129">**SetMaxMonitors**</span></span>](setmaxmonitors-win32-tsclientsetting.md)           | <span data-ttu-id="bf81d-130">Imposta la proprietà **MaxMonitors** .</span><span class="sxs-lookup"><span data-stu-id="bf81d-130">Sets the **MaxMonitors** property.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="bf81d-131">**SetMaxXResolution**</span><span class="sxs-lookup"><span data-stu-id="bf81d-131">**SetMaxXResolution**</span></span>](setmaxxresolution-win32-tsclientsetting.md)     | <span data-ttu-id="bf81d-132">Imposta la proprietà **MaxXResolution** .</span><span class="sxs-lookup"><span data-stu-id="bf81d-132">Sets the **MaxXResolution** property.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="bf81d-133">**SetMaxYResolution**</span><span class="sxs-lookup"><span data-stu-id="bf81d-133">**SetMaxYResolution**</span></span>](setmaxyresolution-win32-tsclientsetting.md)     | <span data-ttu-id="bf81d-134">Imposta la proprietà **MaxYResolution** .</span><span class="sxs-lookup"><span data-stu-id="bf81d-134">Sets the **MaxYResolution** property.</span></span><br/>                                                                                                             |



 

### <a name="properties"></a><span data-ttu-id="bf81d-135">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bf81d-135">Properties</span></span>

<span data-ttu-id="bf81d-136">La classe **Win32 \_ TSClientSetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="bf81d-136">The **Win32\_TSClientSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bf81d-137">**AdvancedRemoteAppGraphics**</span><span class="sxs-lookup"><span data-stu-id="bf81d-137">**AdvancedRemoteAppGraphics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-138">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-139">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="bf81d-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-140">Specifica se abilitare la grafica RemoteFX avanzata per RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="bf81d-140">Specifies whether to enable advanced RemoteFX graphics for RemoteApp.</span></span>

<span data-ttu-id="bf81d-141">**Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è disponibile prima di Windows Server 2012 R2 e Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="bf81d-141">**Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2012 R2 and Windows 8.1.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="bf81d-142"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-142"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="bf81d-143">I grafici avanzati sono disabilitati.</span><span class="sxs-lookup"><span data-stu-id="bf81d-143">Advanced graphics are disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="bf81d-144"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-144"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="bf81d-145">I grafici avanzati sono abilitati.</span><span class="sxs-lookup"><span data-stu-id="bf81d-145">Advanced graphics are enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-146">**AllowDwm**</span><span class="sxs-lookup"><span data-stu-id="bf81d-146">**AllowDwm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-147">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-149">Questa proprietà non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="bf81d-149">This property is not available.</span></span>

<span data-ttu-id="bf81d-150">\* \* Windows 7 e Windows Server 2008 R2: \* \*</span><span class="sxs-lookup"><span data-stu-id="bf81d-150">\*\*Windows 7 and Windows Server 2008 R2:  \*\*</span></span>

<span data-ttu-id="bf81d-151">Specifica se abilitare o disabilitare la composizione del desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="bf81d-151">Specifies whether to enable or disable remote desktop composition.</span></span> <span data-ttu-id="bf81d-152">Lo zero disabilita la composizione del desktop remoto e un valore diverso da zero lo Abilita.</span><span class="sxs-lookup"><span data-stu-id="bf81d-152">Zero will disable remote desktop composition and a nonzero value will enable it.</span></span>

<span data-ttu-id="bf81d-153">Usare il metodo [**SetAllowDwm**](setallowdwm-win32-tsclientsetting.md) per modificare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="bf81d-153">Use the [**SetAllowDwm**](setallowdwm-win32-tsclientsetting.md) method to modify this property.</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-154">**AudioCaptureRedir**</span><span class="sxs-lookup"><span data-stu-id="bf81d-154">**AudioCaptureRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-155">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-157">Specifica se consentire il reindirizzamento dell'acquisizione audio.</span><span class="sxs-lookup"><span data-stu-id="bf81d-157">Specifies whether to allow audio capture redirection.</span></span>

<span data-ttu-id="bf81d-158">**Windows Server 2008 e Windows Vista:** Questa proprietà non è disponibile prima di Windows Server 2008 R2 e Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bf81d-158">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="bf81d-159">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-159">**FALSE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="bf81d-160">**True** (1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-160">**TRUE** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-161">**AudioMapping**</span><span class="sxs-lookup"><span data-stu-id="bf81d-161">**AudioMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-162">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-164">Specifica se il mapping audio è disabilitato o abilitato.</span><span class="sxs-lookup"><span data-stu-id="bf81d-164">Specifies whether audio mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="bf81d-165"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-165"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="bf81d-166">Il mapping audio è abilitato.</span><span class="sxs-lookup"><span data-stu-id="bf81d-166">Audio mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="bf81d-167"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-167"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="bf81d-168">Il mapping audio è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="bf81d-168">Audio mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-169">**AVC444ModePreferred**</span><span class="sxs-lookup"><span data-stu-id="bf81d-169">**AVC444ModePreferred**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-170">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-171">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="bf81d-171">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-172">Specifica se è preferibile la modalità AVC444.</span><span class="sxs-lookup"><span data-stu-id="bf81d-172">Specifies whether AVC444 mode is preferred.</span></span>

<span data-ttu-id="bf81d-173">**Windows 8.1, Windows server 2012 R2, Windows 8, Windows server 2012, Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa proprietà non è disponibile prima di Windows 10 o Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="bf81d-173">**Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 10 or Windows Server 2016.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="bf81d-174">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-174">**FALSE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="bf81d-175">**True** (1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-175">**TRUE** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-176">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="bf81d-176">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-177">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bf81d-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-178">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-179">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="bf81d-179">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-180">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bf81d-180">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="bf81d-181">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bf81d-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-182">**ClipboardMapping**</span><span class="sxs-lookup"><span data-stu-id="bf81d-182">**ClipboardMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-183">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-183">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-185">Specifica se il mapping degli Appunti è disabilitato o abilitato.</span><span class="sxs-lookup"><span data-stu-id="bf81d-185">Specifies whether clipboard mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="bf81d-186"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-186"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="bf81d-187">Il mapping degli Appunti è abilitato.</span><span class="sxs-lookup"><span data-stu-id="bf81d-187">Clipboard mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="bf81d-188"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-188"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="bf81d-189">Il mapping degli Appunti è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="bf81d-189">Clipboard mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-190">**ColorDepth**</span><span class="sxs-lookup"><span data-stu-id="bf81d-190">**ColorDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-191">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-191">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-193">Specifica la profondità del colore.</span><span class="sxs-lookup"><span data-stu-id="bf81d-193">Specifies the color depth.</span></span> <span data-ttu-id="bf81d-194">Per i valori possibili, vedere il metodo [**SetColorDepth**](win32-tsclientsetting-setcolordepth.md) .</span><span class="sxs-lookup"><span data-stu-id="bf81d-194">For possible values, see the [**SetColorDepth**](win32-tsclientsetting-setcolordepth.md) method.</span></span>

<dt>

<span id="8_bit"></span><span id="8_BIT"></span>

<span data-ttu-id="bf81d-195"><span id="8_bit"></span><span id="8_BIT"></span>**8 bit** (1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-195"><span id="8_bit"></span><span id="8_BIT"></span>**8 bit** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="15_bit"></span><span id="15_BIT"></span>

<span data-ttu-id="bf81d-196"><span id="15_bit"></span><span id="15_BIT"></span>**15 bit** (2)</span><span class="sxs-lookup"><span data-stu-id="bf81d-196"><span id="15_bit"></span><span id="15_BIT"></span>**15 bit** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="16_bit"></span><span id="16_BIT"></span>

<span data-ttu-id="bf81d-197"><span id="16_bit"></span><span id="16_BIT"></span>**16 bit** (3)</span><span class="sxs-lookup"><span data-stu-id="bf81d-197"><span id="16_bit"></span><span id="16_BIT"></span>**16 bit** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="24_bit"></span><span id="24_BIT"></span>

<span data-ttu-id="bf81d-198"><span id="24_bit"></span><span id="24_BIT"></span>**24 bit** (4)</span><span class="sxs-lookup"><span data-stu-id="bf81d-198"><span id="24_bit"></span><span id="24_BIT"></span>**24 bit** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="32_bit"></span><span id="32_BIT"></span>

<span data-ttu-id="bf81d-199"><span id="32_bit"></span><span id="32_BIT"></span>**bit 32** (5)</span><span class="sxs-lookup"><span data-stu-id="bf81d-199"><span id="32_bit"></span><span id="32_BIT"></span>**32 bit** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-200">**ColorDepthPolicy**</span><span class="sxs-lookup"><span data-stu-id="bf81d-200">**ColorDepthPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-201">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-202">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-203">Specifica se eseguire l'override dell'impostazione del colore massimo dell'utente.</span><span class="sxs-lookup"><span data-stu-id="bf81d-203">Specifies whether to override the user's maximum color setting.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="bf81d-204"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-204"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="bf81d-205">Non eseguire l'override dei criteri dell'utente.</span><span class="sxs-lookup"><span data-stu-id="bf81d-205">Do not override the user's policy.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="bf81d-206"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-206"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="bf81d-207">Eseguire l'override dei criteri dell'utente.</span><span class="sxs-lookup"><span data-stu-id="bf81d-207">Override the user's policy.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-208">**COMPortMapping**</span><span class="sxs-lookup"><span data-stu-id="bf81d-208">**COMPortMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-209">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-210">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-211">Specifica se il mapping delle porte COM è disabilitato o abilitato.</span><span class="sxs-lookup"><span data-stu-id="bf81d-211">Specifies whether COM port mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="bf81d-212"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-212"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="bf81d-213">Il mapping della porta COM è abilitato.</span><span class="sxs-lookup"><span data-stu-id="bf81d-213">COM port mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="bf81d-214"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-214"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="bf81d-215">Il mapping della porta COM è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="bf81d-215">COM port mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-216">**ConnectClientDrivesAtLogon**</span><span class="sxs-lookup"><span data-stu-id="bf81d-216">**ConnectClientDrivesAtLogon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-217">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-217">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-218">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-219">Specifica se le unità del client verranno connesse automaticamente durante il processo di accesso.</span><span class="sxs-lookup"><span data-stu-id="bf81d-219">Specifies whether the client's drives will be automatically connected during the logon process.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="bf81d-220"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-220"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="bf81d-221">Le unità non verranno connesse automaticamente.</span><span class="sxs-lookup"><span data-stu-id="bf81d-221">Drives will not be automatically connected.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="bf81d-222"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-222"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="bf81d-223">Le unità verranno connesse automaticamente.</span><span class="sxs-lookup"><span data-stu-id="bf81d-223">Drives will be automatically connected.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-224">**ConnectionPolicy**</span><span class="sxs-lookup"><span data-stu-id="bf81d-224">**ConnectionPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-225">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-226">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="bf81d-226">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-227">Il criterio utilizzato dal server per recuperare le impostazioni di connessione utente.</span><span class="sxs-lookup"><span data-stu-id="bf81d-227">The policy the server uses to retrieve the user connection settings.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="bf81d-228"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per utente** (0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-228"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="bf81d-229">Le impostazioni di connessione dell'utente sono attive.</span><span class="sxs-lookup"><span data-stu-id="bf81d-229">The user's connection settings are in effect.</span></span>

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="bf81d-230"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-override** (1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-230"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="bf81d-231">Le impostazioni di connessione dell'utente vengono sostituite dal server.</span><span class="sxs-lookup"><span data-stu-id="bf81d-231">The user's connection settings are overridden by the server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-232">**ConnectPrinterAtLogon**</span><span class="sxs-lookup"><span data-stu-id="bf81d-232">**ConnectPrinterAtLogon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-233">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-233">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-234">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-235">Specifica se tutte le stampanti locali mappate del client verranno connesse automaticamente durante il processo di accesso.</span><span class="sxs-lookup"><span data-stu-id="bf81d-235">Specifies whether all mapped local printers of the client will be automatically connected during the logon process.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="bf81d-236"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-236"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="bf81d-237">Le stampanti locali non verranno connesse automaticamente.</span><span class="sxs-lookup"><span data-stu-id="bf81d-237">Local printers will not be automatically connected.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="bf81d-238"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-238"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="bf81d-239">Le stampanti locali verranno connesse automaticamente.</span><span class="sxs-lookup"><span data-stu-id="bf81d-239">Local printers will be automatically connected.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-240">**DefaultToClientPrinter**</span><span class="sxs-lookup"><span data-stu-id="bf81d-240">**DefaultToClientPrinter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-241">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-242">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-243">Specifica se i processi di stampa verranno inviati automaticamente alla stampante locale del client.</span><span class="sxs-lookup"><span data-stu-id="bf81d-243">Specifies whether print jobs will be automatically sent to the client's local printer.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="bf81d-244"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-244"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="bf81d-245">I processi di stampa non devono essere inviati automaticamente alla stampante locale del client.</span><span class="sxs-lookup"><span data-stu-id="bf81d-245">Print jobs are not to be automatically sent to the client's local printer.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="bf81d-246"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-246"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="bf81d-247">I processi di stampa devono essere inviati automaticamente alla stampante locale del client.</span><span class="sxs-lookup"><span data-stu-id="bf81d-247">Print jobs are to be automatically sent to the client's local printer.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-248">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="bf81d-248">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-249">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bf81d-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-250">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-251">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bf81d-251">Description of the object.</span></span>

<span data-ttu-id="bf81d-252">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bf81d-252">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-253">**DriveMapping**</span><span class="sxs-lookup"><span data-stu-id="bf81d-253">**DriveMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-254">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-254">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-255">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-255">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-256">Specifica se il mapping delle unità è disabilitato o abilitato.</span><span class="sxs-lookup"><span data-stu-id="bf81d-256">Specifies whether drive mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="bf81d-257"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-257"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="bf81d-258">Il mapping delle unità è abilitato.</span><span class="sxs-lookup"><span data-stu-id="bf81d-258">Drive mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="bf81d-259"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-259"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="bf81d-260">Il mapping delle unità è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="bf81d-260">Drive mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-261">**EncodeImageQuality**</span><span class="sxs-lookup"><span data-stu-id="bf81d-261">**EncodeImageQuality**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-262">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-262">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-263">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="bf81d-263">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-264">Specifica la qualità dell'immagine per l'esperienza RDP.</span><span class="sxs-lookup"><span data-stu-id="bf81d-264">Specifies the image quality for RDP experience.</span></span>

<span data-ttu-id="bf81d-265">**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa proprietà non è disponibile prima di Windows 8 o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="bf81d-265">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span id="lossless"></span><span id="LOSSLESS"></span>

<span data-ttu-id="bf81d-266">**Lossless** (1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-266">**lossless** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="bf81d-267">**alta** (2)</span><span class="sxs-lookup"><span data-stu-id="bf81d-267">**high** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="bf81d-268">**media** (3)</span><span class="sxs-lookup"><span data-stu-id="bf81d-268">**medium** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-269">**HardwareGraphicsAdapter**</span><span class="sxs-lookup"><span data-stu-id="bf81d-269">**HardwareGraphicsAdapter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-270">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-270">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-271">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="bf81d-271">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-272">Specifica se il server Host sessione Desktop remoto utilizza il renderer della grafica hardware come adattatore predefinito.</span><span class="sxs-lookup"><span data-stu-id="bf81d-272">Specifies whether the RD Session Host server uses the hardware graphics renderer as the default adapter.</span></span>

<span data-ttu-id="bf81d-273">**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa proprietà non è disponibile prima di Windows 8 o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="bf81d-273">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="bf81d-274">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-274">**FALSE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="bf81d-275">**True** (1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-275">**TRUE** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-276">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="bf81d-276">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-277">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bf81d-277">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-278">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-279">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="bf81d-279">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-280">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bf81d-280">The date the object was installed.</span></span> <span data-ttu-id="bf81d-281">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="bf81d-281">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="bf81d-282">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bf81d-282">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-283">**LPTPortMapping**</span><span class="sxs-lookup"><span data-stu-id="bf81d-283">**LPTPortMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-284">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-284">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-285">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-286">Specifica se il mapping delle porte LPT è disabilitato o abilitato.</span><span class="sxs-lookup"><span data-stu-id="bf81d-286">Specifies whether LPT port mapping is disabled or enabled.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="bf81d-287"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-287"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="bf81d-288">Il mapping della porta LPT è abilitato.</span><span class="sxs-lookup"><span data-stu-id="bf81d-288">LPT port mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="bf81d-289"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-289"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="bf81d-290">Il mapping della porta LPT è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="bf81d-290">LPT port mapping is disabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-291">**MaxMonitors**</span><span class="sxs-lookup"><span data-stu-id="bf81d-291">**MaxMonitors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-292">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-292">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-293">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-293">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-294">Numero massimo di monitoraggi supportati dal server.</span><span class="sxs-lookup"><span data-stu-id="bf81d-294">The maximum number of monitors supported by the server.</span></span> <span data-ttu-id="bf81d-295">Usare il metodo [**SetMaxMonitors**](setmaxmonitors-win32-tsclientsetting.md) per modificare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="bf81d-295">Use the [**SetMaxMonitors**](setmaxmonitors-win32-tsclientsetting.md) method to modify this property.</span></span>

<span data-ttu-id="bf81d-296">**Windows Server 2008 e Windows Vista:** Questa proprietà non è disponibile prima di Windows Server 2008 R2 e Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bf81d-296">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-297">**MaxXResolution**</span><span class="sxs-lookup"><span data-stu-id="bf81d-297">**MaxXResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-298">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-298">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-299">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-300">Risoluzione X massima supportata dal server.</span><span class="sxs-lookup"><span data-stu-id="bf81d-300">The maximum X resolution supported by the server.</span></span> <span data-ttu-id="bf81d-301">Usare il metodo [**SetMaxXResolution**](setmaxxresolution-win32-tsclientsetting.md) per modificare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="bf81d-301">Use the [**SetMaxXResolution**](setmaxxresolution-win32-tsclientsetting.md) method to modify this property.</span></span>

<span data-ttu-id="bf81d-302">**Windows Server 2008 e Windows Vista:** Questa proprietà non è disponibile prima di Windows Server 2008 R2 e Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bf81d-302">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-303">**MaxYResolution**</span><span class="sxs-lookup"><span data-stu-id="bf81d-303">**MaxYResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-304">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-304">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-305">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-306">La risoluzione Y massima supportata dal server.</span><span class="sxs-lookup"><span data-stu-id="bf81d-306">The maximum Y resolution supported by the server.</span></span> <span data-ttu-id="bf81d-307">Usare il metodo [**SetMaxYResolution**](setmaxyresolution-win32-tsclientsetting.md) per modificare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="bf81d-307">Use the [**SetMaxYResolution**](setmaxyresolution-win32-tsclientsetting.md) method to modify this property.</span></span>

<span data-ttu-id="bf81d-308">**Windows Server 2008 e Windows Vista:** Questa proprietà non è disponibile prima di Windows Server 2008 R2 e Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bf81d-308">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-309">**Nome**</span><span class="sxs-lookup"><span data-stu-id="bf81d-309">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-310">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bf81d-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-311">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-312">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bf81d-312">The name of the object.</span></span>

<span data-ttu-id="bf81d-313">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bf81d-313">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-314">**PNPRedirection**</span><span class="sxs-lookup"><span data-stu-id="bf81d-314">**PNPRedirection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-315">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-315">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-316">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-316">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-317">Specifica se consentire il reindirizzamento Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="bf81d-317">Specifies whether to allow Plug and Play redirection.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="bf81d-318"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-318"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="bf81d-319">Consentire il reindirizzamento del Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="bf81d-319">Allow Plug and Play redirection.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="bf81d-320"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-320"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="bf81d-321">Non consentire il reindirizzamento del Plug and Play.</span><span class="sxs-lookup"><span data-stu-id="bf81d-321">Do not allow Plug and Play redirection.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-322">**PolicyAdvancedRemoteAppGraphics**</span><span class="sxs-lookup"><span data-stu-id="bf81d-322">**PolicyAdvancedRemoteAppGraphics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-323">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-323">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-324">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-325">Indica se la proprietà **AdvancedRemoteAppGraphics** è configurata dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="bf81d-325">Indicates whether the **AdvancedRemoteAppGraphics** property is configured by the server or group policy.</span></span>

<span data-ttu-id="bf81d-326">**Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Questa proprietà non è disponibile prima di Windows Server 2012 R2 e Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="bf81d-326">**Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2012 R2 and Windows 8.1.</span></span>

<dt>

<span data-ttu-id="bf81d-327">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-327">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-328">Server</span><span class="sxs-lookup"><span data-stu-id="bf81d-328">Server</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-329">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-329">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-330">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="bf81d-330">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-331">**PolicySourceAllowDwm**</span><span class="sxs-lookup"><span data-stu-id="bf81d-331">**PolicySourceAllowDwm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-332">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-332">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-333">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-334">Questa proprietà non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="bf81d-334">This property is not available.</span></span>

<span data-ttu-id="bf81d-335">\* \* Windows 7 e Windows Server 2008 R2: \* \*</span><span class="sxs-lookup"><span data-stu-id="bf81d-335">\*\*Windows 7 and Windows Server 2008 R2:  \*\*</span></span>

<span data-ttu-id="bf81d-336">Indica se la proprietà **AllowDwm** è configurata dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="bf81d-336">Indicates whether the **AllowDwm** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="bf81d-337">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-337">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-338">Server</span><span class="sxs-lookup"><span data-stu-id="bf81d-338">Server</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-339">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-339">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-340">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="bf81d-340">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-341">**PolicySourceAudioCaptureRedir**</span><span class="sxs-lookup"><span data-stu-id="bf81d-341">**PolicySourceAudioCaptureRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-342">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-342">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-343">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-344">Indica se la proprietà **AudioCaptureRedir** è configurata dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="bf81d-344">Indicates whether the **AudioCaptureRedir** property is configured by the server or group policy.</span></span>

<span data-ttu-id="bf81d-345">**Windows Server 2008 e Windows Vista:** Questa proprietà non è disponibile prima di Windows Server 2008 R2 e Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bf81d-345">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span data-ttu-id="bf81d-346">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-346">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-347">Server</span><span class="sxs-lookup"><span data-stu-id="bf81d-347">Server</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-348">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-348">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-349">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="bf81d-349">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-350">**PolicySourceAudioMapping**</span><span class="sxs-lookup"><span data-stu-id="bf81d-350">**PolicySourceAudioMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-351">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-351">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-352">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-353">Indica se la proprietà **AudioMapping** è configurata dal server, da criteri di gruppo o per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="bf81d-353">Indicates whether the **AudioMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="bf81d-354">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-354">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-355">Server</span><span class="sxs-lookup"><span data-stu-id="bf81d-355">Server</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-356">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-356">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-357">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="bf81d-357">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-358">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="bf81d-358">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-359">Predefinito</span><span class="sxs-lookup"><span data-stu-id="bf81d-359">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-360">**PolicySourceAvc444ModePreferred**</span><span class="sxs-lookup"><span data-stu-id="bf81d-360">**PolicySourceAvc444ModePreferred**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-361">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-361">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-362">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-363">Indica il modo in cui la proprietà **AVC444ModePreferredis** è configurata.</span><span class="sxs-lookup"><span data-stu-id="bf81d-363">Indicates how the **AVC444ModePreferredis** property is configured.</span></span>

<span data-ttu-id="bf81d-364">**Windows 8.1, Windows server 2012 R2, Windows 8, Windows server 2012, Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa proprietà non è disponibile prima di Windows 10 o Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="bf81d-364">**Windows 8.1, Windows Server 2012 R2, Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 10 or Windows Server 2016.</span></span>

<dt>

<span data-ttu-id="bf81d-365">0</span><span class="sxs-lookup"><span data-stu-id="bf81d-365">0</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-366">Server</span><span class="sxs-lookup"><span data-stu-id="bf81d-366">Server</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-367">1</span><span class="sxs-lookup"><span data-stu-id="bf81d-367">1</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-368">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="bf81d-368">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-369">**PolicySourceClipboardMapping**</span><span class="sxs-lookup"><span data-stu-id="bf81d-369">**PolicySourceClipboardMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-370">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-370">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-371">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-371">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-372">Indica se la proprietà **ClipboardMapping** è configurata dal server, da criteri di gruppo o per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="bf81d-372">Indicates whether the **ClipboardMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="bf81d-373">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-373">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-374">Server</span><span class="sxs-lookup"><span data-stu-id="bf81d-374">Server</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-375">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-375">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-376">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="bf81d-376">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-377">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="bf81d-377">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-378">Predefinito</span><span class="sxs-lookup"><span data-stu-id="bf81d-378">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-379">**PolicySourceColorDepth**</span><span class="sxs-lookup"><span data-stu-id="bf81d-379">**PolicySourceColorDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-380">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-380">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-381">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-382">Indica se la proprietà **ColorDepth** è configurata dal server, da criteri di gruppo o per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="bf81d-382">Indicates whether the **ColorDepth** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="bf81d-383">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-383">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-384">Server</span><span class="sxs-lookup"><span data-stu-id="bf81d-384">Server</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-385">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-385">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-386">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="bf81d-386">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-387">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="bf81d-387">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-388">Predefinito</span><span class="sxs-lookup"><span data-stu-id="bf81d-388">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-389">**PolicySourceColorDepthPolicy**</span><span class="sxs-lookup"><span data-stu-id="bf81d-389">**PolicySourceColorDepthPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-390">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-390">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-391">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-391">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-392">Indica se la proprietà **ColorDepthPolicy** è configurata dal server, da criteri di gruppo o per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="bf81d-392">Indicates whether the **ColorDepthPolicy** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="bf81d-393">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-393">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-394">Server</span><span class="sxs-lookup"><span data-stu-id="bf81d-394">Server</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-395">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-395">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-396">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="bf81d-396">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-397">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="bf81d-397">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-398">Predefinito</span><span class="sxs-lookup"><span data-stu-id="bf81d-398">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-399">**PolicySourceCOMPortMapping**</span><span class="sxs-lookup"><span data-stu-id="bf81d-399">**PolicySourceCOMPortMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-400">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-400">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-401">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-401">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-402">Indica se la proprietà **COMPortMapping** è configurata dal server, da criteri di gruppo o per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="bf81d-402">Indicates whether the **COMPortMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="bf81d-403">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-403">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-404">Server</span><span class="sxs-lookup"><span data-stu-id="bf81d-404">Server</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-405">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-405">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-406">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="bf81d-406">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-407">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="bf81d-407">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-408">Predefinito</span><span class="sxs-lookup"><span data-stu-id="bf81d-408">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-409">**PolicySourceDefaultToClientPrinter**</span><span class="sxs-lookup"><span data-stu-id="bf81d-409">**PolicySourceDefaultToClientPrinter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-410">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-410">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-411">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-411">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-412">Indica se la proprietà **DefaultToClientPrinter** è configurata dal server, da criteri di gruppo o per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="bf81d-412">Indicates whether the **DefaultToClientPrinter** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="bf81d-413">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-413">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-414">Server</span><span class="sxs-lookup"><span data-stu-id="bf81d-414">Server</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-415">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-415">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-416">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="bf81d-416">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-417">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="bf81d-417">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-418">Predefinito</span><span class="sxs-lookup"><span data-stu-id="bf81d-418">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-419">**PolicySourceDriveMapping**</span><span class="sxs-lookup"><span data-stu-id="bf81d-419">**PolicySourceDriveMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-420">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-420">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-421">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-422">Indica se la proprietà **DriveMapping** è configurata dal server, da criteri di gruppo o per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="bf81d-422">Indicates whether the **DriveMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="bf81d-423">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-423">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-424">Server</span><span class="sxs-lookup"><span data-stu-id="bf81d-424">Server</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-425">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-425">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-426">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="bf81d-426">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-427">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="bf81d-427">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-428">Predefinito</span><span class="sxs-lookup"><span data-stu-id="bf81d-428">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-429">**PolicySourceEncodeImageQuality**</span><span class="sxs-lookup"><span data-stu-id="bf81d-429">**PolicySourceEncodeImageQuality**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-430">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-430">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-431">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-432">Indica la modalità di configurazione di **EncodeImageQualityi** .</span><span class="sxs-lookup"><span data-stu-id="bf81d-432">Indicates how the **EncodeImageQualityi** is configured.</span></span>

<span data-ttu-id="bf81d-433">**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa proprietà non è disponibile prima di Windows 8 o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="bf81d-433">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="bf81d-434">0</span><span class="sxs-lookup"><span data-stu-id="bf81d-434">0</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-435">Server</span><span class="sxs-lookup"><span data-stu-id="bf81d-435">Server</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-436">1</span><span class="sxs-lookup"><span data-stu-id="bf81d-436">1</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-437">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="bf81d-437">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-438">**PolicySourceHardwareGraphicsAdapter**</span><span class="sxs-lookup"><span data-stu-id="bf81d-438">**PolicySourceHardwareGraphicsAdapter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-439">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-439">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-440">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-440">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-441">Indica la modalità di configurazione di **HardwareGraphicsAdapter** .</span><span class="sxs-lookup"><span data-stu-id="bf81d-441">Indicates how the **HardwareGraphicsAdapter** is configured.</span></span>

<span data-ttu-id="bf81d-442">**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa proprietà non è disponibile prima di Windows 8 o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="bf81d-442">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="bf81d-443">0</span><span class="sxs-lookup"><span data-stu-id="bf81d-443">0</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-444">Server</span><span class="sxs-lookup"><span data-stu-id="bf81d-444">Server</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-445">1</span><span class="sxs-lookup"><span data-stu-id="bf81d-445">1</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-446">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="bf81d-446">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-447">**PolicySourceLPTPortMapping**</span><span class="sxs-lookup"><span data-stu-id="bf81d-447">**PolicySourceLPTPortMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-448">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-448">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-449">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-449">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-450">Indica se la proprietà **LPTPortMapping** è configurata dal server, da criteri di gruppo o per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="bf81d-450">Indicates whether the **LPTPortMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="bf81d-451">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-451">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-452">Server</span><span class="sxs-lookup"><span data-stu-id="bf81d-452">Server</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-453">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-453">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-454">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="bf81d-454">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-455">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="bf81d-455">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-456">Predefinito</span><span class="sxs-lookup"><span data-stu-id="bf81d-456">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-457">**PolicySourceMaxMonitors**</span><span class="sxs-lookup"><span data-stu-id="bf81d-457">**PolicySourceMaxMonitors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-458">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-458">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-459">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-460">Indica se la proprietà **MaxMonitors** è configurata in base al server, ai criteri di gruppo o al valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="bf81d-460">Indicates whether the **MaxMonitors** property is configured by the server, group policy, or default.</span></span>

<dt>

<span data-ttu-id="bf81d-461">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-461">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-462">Server</span><span class="sxs-lookup"><span data-stu-id="bf81d-462">Server</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-463">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-463">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-464">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="bf81d-464">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-465">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="bf81d-465">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-466">Predefinito</span><span class="sxs-lookup"><span data-stu-id="bf81d-466">Default</span></span>

</dd> </dl>

<span data-ttu-id="bf81d-467">**Windows Server 2008 e Windows Vista:** Questa proprietà non è disponibile prima di Windows Server 2008 R2 e Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bf81d-467">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-468">**PolicySourceMaxResolution**</span><span class="sxs-lookup"><span data-stu-id="bf81d-468">**PolicySourceMaxResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-469">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-469">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-470">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-470">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-471">Indica se le proprietà **MaxXResolution** e **MaxYResolution** sono configurate dal server, dai criteri di gruppo o dal valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="bf81d-471">Indicates whether the **MaxXResolution** and **MaxYResolution** properties are configured by the server, group policy, or default.</span></span>

<span data-ttu-id="bf81d-472">**Windows Server 2008 e Windows Vista:** Questa proprietà non è disponibile prima di Windows Server 2008 R2 e Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bf81d-472">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span data-ttu-id="bf81d-473">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-473">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-474">Server</span><span class="sxs-lookup"><span data-stu-id="bf81d-474">Server</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-475">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-475">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-476">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="bf81d-476">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-477">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="bf81d-477">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-478">Predefinito</span><span class="sxs-lookup"><span data-stu-id="bf81d-478">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-479">**PolicySourcePNPRedirection**</span><span class="sxs-lookup"><span data-stu-id="bf81d-479">**PolicySourcePNPRedirection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-480">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-480">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-481">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-481">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-482">Indica se la proprietà **PNPRedirection** è configurata dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="bf81d-482">Indicates whether the **PNPRedirection** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="bf81d-483">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-483">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-484">Server</span><span class="sxs-lookup"><span data-stu-id="bf81d-484">Server</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-485">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-485">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-486">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="bf81d-486">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-487">**PolicySourceRemoteSessionProfile**</span><span class="sxs-lookup"><span data-stu-id="bf81d-487">**PolicySourceRemoteSessionProfile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-488">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-488">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-489">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-489">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-490">Indica la modalità di configurazione di **RemoteSessionProfile** .</span><span class="sxs-lookup"><span data-stu-id="bf81d-490">Indicates how the **RemoteSessionProfile** is configured.</span></span>

<span data-ttu-id="bf81d-491">**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa proprietà non è disponibile prima di Windows 8 o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="bf81d-491">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is unavailable prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="bf81d-492">0</span><span class="sxs-lookup"><span data-stu-id="bf81d-492">0</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-493">Server</span><span class="sxs-lookup"><span data-stu-id="bf81d-493">Server</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-494">1</span><span class="sxs-lookup"><span data-stu-id="bf81d-494">1</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-495">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="bf81d-495">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-496">**PolicySourceSelectNetworkDetect**</span><span class="sxs-lookup"><span data-stu-id="bf81d-496">**PolicySourceSelectNetworkDetect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-497">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-497">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-498">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-498">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-499">Indica il modo in cui la proprietà **SelectNetworkDetect** è configurata.</span><span class="sxs-lookup"><span data-stu-id="bf81d-499">Indicates how the property **SelectNetworkDetect** is configured.</span></span>

<span data-ttu-id="bf81d-500">**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa proprietà non è disponibile prima di Windows 8 o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="bf81d-500">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="bf81d-501">0</span><span class="sxs-lookup"><span data-stu-id="bf81d-501">0</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-502">Server</span><span class="sxs-lookup"><span data-stu-id="bf81d-502">Server</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-503">1</span><span class="sxs-lookup"><span data-stu-id="bf81d-503">1</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-504">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="bf81d-504">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-505">**PolicySourceSelectTransport**</span><span class="sxs-lookup"><span data-stu-id="bf81d-505">**PolicySourceSelectTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-506">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-506">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-507">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-508">Indica il modo in cui la proprietà **SelectTransport** è configurata.</span><span class="sxs-lookup"><span data-stu-id="bf81d-508">Indicates how the property **SelectTransport** is configured.</span></span>

<span data-ttu-id="bf81d-509">**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa proprietà non è disponibile prima di Windows 8 o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="bf81d-509">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="bf81d-510">0</span><span class="sxs-lookup"><span data-stu-id="bf81d-510">0</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-511">Server</span><span class="sxs-lookup"><span data-stu-id="bf81d-511">Server</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-512">1</span><span class="sxs-lookup"><span data-stu-id="bf81d-512">1</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-513">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="bf81d-513">Group Policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-514">**PolicySourceVideoPlaybackRedir**</span><span class="sxs-lookup"><span data-stu-id="bf81d-514">**PolicySourceVideoPlaybackRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-515">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-515">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-516">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-516">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-517">Indica se la proprietà **VideoPlaybackRedir** è configurata dal server o da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="bf81d-517">Indicates whether the **VideoPlaybackRedir** property is configured by the server or group policy.</span></span>

<span data-ttu-id="bf81d-518">**Windows Server 2008 e Windows Vista:** Questa proprietà non è disponibile prima di Windows Server 2008 R2 e Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bf81d-518">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span data-ttu-id="bf81d-519">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-519">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-520">Server</span><span class="sxs-lookup"><span data-stu-id="bf81d-520">Server</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-521">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-521">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-522">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="bf81d-522">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-523">**PolicySourceWindowsPrinterMapping**</span><span class="sxs-lookup"><span data-stu-id="bf81d-523">**PolicySourceWindowsPrinterMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-524">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-524">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-525">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-525">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-526">Indica se la proprietà **WindowsPrinterMapping** è configurata dal server, da criteri di gruppo o per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="bf81d-526">Indicates whether the **WindowsPrinterMapping** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="bf81d-527">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-527">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-528">Server</span><span class="sxs-lookup"><span data-stu-id="bf81d-528">Server</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-529">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-529">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-530">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="bf81d-530">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-531">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="bf81d-531">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-532">Predefinito</span><span class="sxs-lookup"><span data-stu-id="bf81d-532">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-533">**RemoteSessionProfile**</span><span class="sxs-lookup"><span data-stu-id="bf81d-533">**RemoteSessionProfile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-534">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-534">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-535">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="bf81d-535">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-536">Specifica il profilo per l'esperienza RDP.</span><span class="sxs-lookup"><span data-stu-id="bf81d-536">Specifies the profile for the RDP experience.</span></span>

<span data-ttu-id="bf81d-537">**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa proprietà non è disponibile prima di Windows 8 o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="bf81d-537">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span id="scale"></span><span id="SCALE"></span>

<span data-ttu-id="bf81d-538">**scala** (1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-538">**scale** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="experience"></span><span id="EXPERIENCE"></span>

<span data-ttu-id="bf81d-539">**esperienza** (2)</span><span class="sxs-lookup"><span data-stu-id="bf81d-539">**experience** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="bandwidth"></span><span id="BANDWIDTH"></span>

<span data-ttu-id="bf81d-540">**larghezza di banda** (3)</span><span class="sxs-lookup"><span data-stu-id="bf81d-540">**bandwidth** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-541">**SelectNetworkDetect**</span><span class="sxs-lookup"><span data-stu-id="bf81d-541">**SelectNetworkDetect**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-542">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-542">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-543">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="bf81d-543">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-544">Specifica se viene utilizzato il rilevamento di rete.</span><span class="sxs-lookup"><span data-stu-id="bf81d-544">Specifies whether network detection is used.</span></span>

<span data-ttu-id="bf81d-545">**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa proprietà non è disponibile prima di Windows 8 o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="bf81d-545">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="bf81d-546">0</span><span class="sxs-lookup"><span data-stu-id="bf81d-546">0</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-547">utilizzato in fase di connessione e in stato stabile.</span><span class="sxs-lookup"><span data-stu-id="bf81d-547">used at connect time and in steady state.</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-548">1</span><span class="sxs-lookup"><span data-stu-id="bf81d-548">1</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-549">disabilitato al momento della connessione</span><span class="sxs-lookup"><span data-stu-id="bf81d-549">disabled at connect time</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-550">2</span><span class="sxs-lookup"><span data-stu-id="bf81d-550">2</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-551">disabilitato in stato stazionario</span><span class="sxs-lookup"><span data-stu-id="bf81d-551">disabled in steady state</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-552">3</span><span class="sxs-lookup"><span data-stu-id="bf81d-552">3</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-553">disabilitato in fase di connessione e in stato stabile.</span><span class="sxs-lookup"><span data-stu-id="bf81d-553">disabled at connect time and in steady state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-554">**SelectTransport**</span><span class="sxs-lookup"><span data-stu-id="bf81d-554">**SelectTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-555">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-555">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-556">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="bf81d-556">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-557">Specifica i protocolli di trasporto che possono essere utilizzati per l'accesso RDP al server.</span><span class="sxs-lookup"><span data-stu-id="bf81d-557">Specifies which transport protocols can be used for RDP access to server.</span></span>

<span data-ttu-id="bf81d-558">**Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questa proprietà non è disponibile prima di Windows 8 o Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="bf81d-558">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available prior to Windows 8 or Windows Server 2012.</span></span>

<dt>

<span data-ttu-id="bf81d-559">0</span><span class="sxs-lookup"><span data-stu-id="bf81d-559">0</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-560">Usare sia UDP che TCP.</span><span class="sxs-lookup"><span data-stu-id="bf81d-560">Use both UDP and TCP.</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-561">1</span><span class="sxs-lookup"><span data-stu-id="bf81d-561">1</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-562">Utilizzare solo TCP.</span><span class="sxs-lookup"><span data-stu-id="bf81d-562">Use only TCP.</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-563">2</span><span class="sxs-lookup"><span data-stu-id="bf81d-563">2</span></span>
</dt> <dd>

<span data-ttu-id="bf81d-564">Utilizzare UDP o TCP.</span><span class="sxs-lookup"><span data-stu-id="bf81d-564">Use either UDP or TCP.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-565">**Status**</span><span class="sxs-lookup"><span data-stu-id="bf81d-565">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-566">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bf81d-566">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-567">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-567">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-568">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="bf81d-568">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-569">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bf81d-569">Current status of the object.</span></span> <span data-ttu-id="bf81d-570">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="bf81d-570">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="bf81d-571">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="bf81d-571">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="bf81d-572">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="bf81d-572">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="bf81d-573">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="bf81d-573">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="bf81d-574">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="bf81d-574">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="bf81d-575">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bf81d-575">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="bf81d-576">("OK")</span><span class="sxs-lookup"><span data-stu-id="bf81d-576">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bf81d-577">("Errore")</span><span class="sxs-lookup"><span data-stu-id="bf81d-577">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bf81d-578">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="bf81d-578">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bf81d-579">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="bf81d-579">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bf81d-580">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="bf81d-580">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bf81d-581">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="bf81d-581">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bf81d-582">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="bf81d-582">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bf81d-583">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="bf81d-583">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-584">**Terminale**</span><span class="sxs-lookup"><span data-stu-id="bf81d-584">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-585">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bf81d-585">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-586">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-586">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-587">Nome del terminale.</span><span class="sxs-lookup"><span data-stu-id="bf81d-587">The name of the terminal.</span></span>

<span data-ttu-id="bf81d-588">Questa proprietà viene ereditata da [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="bf81d-588">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> <dt>

<span data-ttu-id="bf81d-589">**VideoPlaybackRedir**</span><span class="sxs-lookup"><span data-stu-id="bf81d-589">**VideoPlaybackRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-590">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-590">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-591">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-591">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-592">Specifica se consentire il reindirizzamento della riproduzione video.</span><span class="sxs-lookup"><span data-stu-id="bf81d-592">Specifies whether to allow video playback redirection.</span></span>

<span data-ttu-id="bf81d-593">**Windows Server 2008 e Windows Vista:** Questa proprietà non è disponibile prima di Windows Server 2008 R2 e Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bf81d-593">**Windows Server 2008 and Windows Vista:** This property is not available before Windows Server 2008 R2 and Windows 7.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="bf81d-594">**False** (0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-594">**FALSE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="bf81d-595">**True** (1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-595">**TRUE** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bf81d-596">**WindowsPrinterMapping**</span><span class="sxs-lookup"><span data-stu-id="bf81d-596">**WindowsPrinterMapping**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf81d-597">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-597">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf81d-598">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bf81d-598">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bf81d-599">Specifica se il mapping della stampante è disabilitato o abilitato per la finestra del client.</span><span class="sxs-lookup"><span data-stu-id="bf81d-599">Specifies whether printer mapping is disabled or enabled for the client's window.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="bf81d-600"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="bf81d-600"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="bf81d-601">Il mapping della stampante è abilitato.</span><span class="sxs-lookup"><span data-stu-id="bf81d-601">Printer mapping is enabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="bf81d-602"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="bf81d-602"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="bf81d-603">Il mapping della stampante è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="bf81d-603">Printer mapping is disabled.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bf81d-604">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf81d-604">Remarks</span></span>

<span data-ttu-id="bf81d-605">Tenere presente che una stazione della finestra associata alla sessione della console non può accedere ai metodi e alle proprietà di questa classe.</span><span class="sxs-lookup"><span data-stu-id="bf81d-605">Be aware that a window station associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="bf81d-606">Se viene effettuato un tentativo di eseguire questa operazione specificando "console" come valore della proprietà **TerminalName** , i metodi di questo oggetto restituiranno **WBEM \_ E \_ non \_ supportati**.</span><span class="sxs-lookup"><span data-stu-id="bf81d-606">If an attempt is made to do so by specifying "Console" as the value of the **TerminalName** property, methods of this object will return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="bf81d-607">Questo codice di errore viene restituito anche se una stazione della finestra tenta di chiamare i metodi di questo oggetto per aggiungere o modificare le proprietà di sicurezza degli account LocalSystem, LocalService o NetworkService.</span><span class="sxs-lookup"><span data-stu-id="bf81d-607">This error code is also returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="bf81d-608">Per connettersi allo \\ \\ \\ spazio dei nomi CIMV2 TerminalServices radice, il livello di autenticazione deve includere la riservatezza dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="bf81d-608">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="bf81d-609">Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_ privacy**.</span><span class="sxs-lookup"><span data-stu-id="bf81d-609">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="bf81d-610">Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore di sei.</span><span class="sxs-lookup"><span data-stu-id="bf81d-610">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of six.</span></span>

<span data-ttu-id="bf81d-611">Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="bf81d-611">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="bf81d-612">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="bf81d-612">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bf81d-613">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="bf81d-613">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bf81d-614">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="bf81d-614">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bf81d-615">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="bf81d-615">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf81d-616">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf81d-616">Requirements</span></span>



| <span data-ttu-id="bf81d-617">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf81d-617">Requirement</span></span> | <span data-ttu-id="bf81d-618">Valore</span><span class="sxs-lookup"><span data-stu-id="bf81d-618">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf81d-619">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf81d-619">Minimum supported client</span></span><br/> | <span data-ttu-id="bf81d-620">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bf81d-620">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bf81d-621">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf81d-621">Minimum supported server</span></span><br/> | <span data-ttu-id="bf81d-622">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf81d-622">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bf81d-623">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bf81d-623">Namespace</span></span><br/>                | <span data-ttu-id="bf81d-624">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="bf81d-624">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="bf81d-625">MOF</span><span class="sxs-lookup"><span data-stu-id="bf81d-625">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf81d-626"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bf81d-626"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf81d-627">DLL</span><span class="sxs-lookup"><span data-stu-id="bf81d-627">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf81d-628"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf81d-628"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf81d-629">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf81d-629">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf81d-630">**\_Terminale Win32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-630">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="bf81d-631">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="bf81d-631">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dt>

[<span data-ttu-id="bf81d-632">**\_Impostazione CIM**</span><span class="sxs-lookup"><span data-stu-id="bf81d-632">**CIM\_Setting**</span></span>](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 


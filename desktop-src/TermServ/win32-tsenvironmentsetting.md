---
title: Classe Win32_TSEnvironmentSetting
description: Definisce le impostazioni di configurazione per la \_ classe terminale Win32, inclusi i criteri di programma iniziali.
ms.assetid: 2d310a1e-a1bd-4ccb-965e-8389aaa2e4c1
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSEnvironmentSetting Servizi Desktop remoto
- Classe Win32_TSEnvironmentSetting Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting
- Win32_TSEnvironmentSetting.Caption
- Win32_TSEnvironmentSetting.Description
- Win32_TSEnvironmentSetting.InstallDate
- Win32_TSEnvironmentSetting.Name
- Win32_TSEnvironmentSetting.Status
- Win32_TSEnvironmentSetting.TerminalName
- Win32_TSEnvironmentSetting.ClientWallPaper
- Win32_TSEnvironmentSetting.InitialProgramPath
- Win32_TSEnvironmentSetting.InitialProgramPolicy
- Win32_TSEnvironmentSetting.PolicySourceClientWallPaper
- Win32_TSEnvironmentSetting.PolicySourceInitialProgramPath
- Win32_TSEnvironmentSetting.PolicySourceStartIn
- Win32_TSEnvironmentSetting.Startin
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0689536385644ae3ef95d106e50ab198e5a57f93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518814"
---
# <a name="win32_tsenvironmentsetting-class"></a><span data-ttu-id="f9a1f-105">Win32 \_ TSEnvironmentSetting (classe)</span><span class="sxs-lookup"><span data-stu-id="f9a1f-105">Win32\_TSEnvironmentSetting class</span></span>

<span data-ttu-id="f9a1f-106">La classe WMI **Win32 \_ TSEnvironmentSetting** definisce le impostazioni di configurazione per la classe [**\_ terminale Win32**](win32-terminal.md) , inclusi i criteri di programma iniziali.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-106">The **Win32\_TSEnvironmentSetting** WMI class defines the configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class including initial program policy.</span></span>

<span data-ttu-id="f9a1f-107">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà definite ed ereditate, in ordine alfabetico.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="f9a1f-108">Per informazioni di riferimento sui metodi, vedere la tabella dei metodi più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9a1f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9a1f-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSENVIRONMENTSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSEnvironmentSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ClientWallPaper;
  string   InitialProgramPath;
  uint32   InitialProgramPolicy;
  uint32   PolicySourceClientWallPaper;
  uint32   PolicySourceInitialProgramPath;
  uint32   PolicySourceStartIn;
  string   Startin;
};
```

## <a name="members"></a><span data-ttu-id="f9a1f-110">Members</span><span class="sxs-lookup"><span data-stu-id="f9a1f-110">Members</span></span>

<span data-ttu-id="f9a1f-111">La classe **Win32 \_ TSEnvironmentSetting** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f9a1f-111">The **Win32\_TSEnvironmentSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="f9a1f-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="f9a1f-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="f9a1f-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f9a1f-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f9a1f-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="f9a1f-114">Methods</span></span>

<span data-ttu-id="f9a1f-115">La classe **Win32 \_ TSEnvironmentSetting** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-115">The **Win32\_TSEnvironmentSetting** class has these methods.</span></span>



| <span data-ttu-id="f9a1f-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="f9a1f-116">Method</span></span>                                                                      | <span data-ttu-id="f9a1f-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9a1f-117">Description</span></span>                                                            |
|:----------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="f9a1f-118">**InitialProgram**</span><span class="sxs-lookup"><span data-stu-id="f9a1f-118">**InitialProgram**</span></span>](win32-tsenvironmentsetting-initialprogram.md)         | <span data-ttu-id="f9a1f-119">Imposta le proprietà del programma di avvio incluse in questa classe.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-119">Sets the startup program properties included in this class.</span></span><br/> |
| [<span data-ttu-id="f9a1f-120">**SetClientWallPaper**</span><span class="sxs-lookup"><span data-stu-id="f9a1f-120">**SetClientWallPaper**</span></span>](win32-tsenvironmentsetting-setclientwallpaper.md) | <span data-ttu-id="f9a1f-121">Imposta la proprietà **ClientWallPaper** .</span><span class="sxs-lookup"><span data-stu-id="f9a1f-121">Sets the **ClientWallPaper** property.</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="f9a1f-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f9a1f-122">Properties</span></span>

<span data-ttu-id="f9a1f-123">La classe **Win32 \_ TSEnvironmentSetting** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-123">The **Win32\_TSEnvironmentSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f9a1f-124">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="f9a1f-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9a1f-125">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f9a1f-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9a1f-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f9a1f-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9a1f-127">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f9a1f-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f9a1f-128">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-128">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="f9a1f-129">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f9a1f-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9a1f-130">**ClientWallPaper**</span><span class="sxs-lookup"><span data-stu-id="f9a1f-130">**ClientWallPaper**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9a1f-131">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f9a1f-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9a1f-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f9a1f-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9a1f-133">Specifica se l'immagine dello sfondo viene visualizzata nel client.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-133">Specifies whether the wallpaper image is displayed on the client.</span></span> <span data-ttu-id="f9a1f-134">La mancata visualizzazione dell'immagine dello sfondo può ridurre le risorse di sistema riducendo il tempo necessario per ridisegnare lo schermo.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-134">Not displaying the wallpaper image can save system resources by decreasing the time required to repaint the screen.</span></span>

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span data-ttu-id="f9a1f-135"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="f9a1f-135"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f9a1f-136">L'immagine dello sfondo non viene visualizzata nel client.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-136">The wallpaper image is not displayed on the client.</span></span>

</dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span data-ttu-id="f9a1f-137"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="f9a1f-137"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f9a1f-138">L'immagine dello sfondo viene visualizzata nel client.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-138">The wallpaper image is displayed on the client.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f9a1f-139">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="f9a1f-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9a1f-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f9a1f-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9a1f-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f9a1f-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9a1f-142">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-142">Description of the object.</span></span>

<span data-ttu-id="f9a1f-143">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f9a1f-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9a1f-144">**InitialProgramPath**</span><span class="sxs-lookup"><span data-stu-id="f9a1f-144">**InitialProgramPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9a1f-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f9a1f-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9a1f-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f9a1f-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9a1f-147">Il nome e il percorso del programma che l'utente eseguirà immediatamente dopo l'accesso al server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-147">The name and the path of the program the user will run immediately after logging on to the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="f9a1f-148">**InitialProgramPolicy**</span><span class="sxs-lookup"><span data-stu-id="f9a1f-148">**InitialProgramPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9a1f-149">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f9a1f-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9a1f-150">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="f9a1f-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="f9a1f-151">Il criterio utilizzato dal server per determinare il percorso del programma di avvio e il nome del file e il nome della cartella in cui si trova.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-151">The policy the server uses to determine the startup program path and file name, and the name of the folder it is located in.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="f9a1f-152"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per utente** (0)</span><span class="sxs-lookup"><span data-stu-id="f9a1f-152"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f9a1f-153">Le impostazioni del programma di avvio dell'utente sono attive.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-153">The user's startup program settings are in effect.</span></span>

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="f9a1f-154"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-override** (1)</span><span class="sxs-lookup"><span data-stu-id="f9a1f-154"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f9a1f-155">Il server esegue l'override delle impostazioni del programma di avvio dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-155">The user's startup program settings are overridden by the server.</span></span>

</dd> <dt>

<span id="Single-App_Mode"></span><span id="single-app_mode"></span><span id="SINGLE-APP_MODE"></span>

<span data-ttu-id="f9a1f-156"><span id="Single-App_Mode"></span><span id="single-app_mode"></span><span id="SINGLE-APP_MODE"></span>**Modalità app singola** (2)</span><span class="sxs-lookup"><span data-stu-id="f9a1f-156"><span id="Single-App_Mode"></span><span id="single-app_mode"></span><span id="SINGLE-APP_MODE"></span>**Single-App Mode** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f9a1f-157">In questa sessione verrà eseguita una sola applicazione.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-157">Only a single application will be run in this session.</span></span> <span data-ttu-id="f9a1f-158">Le informazioni sul programma di avvio verranno ignorate.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-158">The startup program information is ignored.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f9a1f-159">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f9a1f-159">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9a1f-160">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f9a1f-160">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f9a1f-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f9a1f-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9a1f-162">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="f9a1f-162">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="f9a1f-163">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-163">The date the object was installed.</span></span> <span data-ttu-id="f9a1f-164">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-164">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f9a1f-165">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f9a1f-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9a1f-166">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f9a1f-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9a1f-167">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f9a1f-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9a1f-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f9a1f-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9a1f-169">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-169">The name of the object.</span></span>

<span data-ttu-id="f9a1f-170">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f9a1f-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9a1f-171">**PolicySourceClientWallPaper**</span><span class="sxs-lookup"><span data-stu-id="f9a1f-171">**PolicySourceClientWallPaper**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9a1f-172">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f9a1f-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9a1f-173">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f9a1f-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9a1f-174">Indica se la proprietà **ClientWallPaper** è configurata dal server, da criteri di gruppo o per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-174">Indicates whether the **ClientWallPaper** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="f9a1f-175">0</span><span class="sxs-lookup"><span data-stu-id="f9a1f-175">0</span></span>
</dt> <dd>

<span data-ttu-id="f9a1f-176">Server</span><span class="sxs-lookup"><span data-stu-id="f9a1f-176">Server</span></span>

</dd> <dt>

<span data-ttu-id="f9a1f-177">1</span><span class="sxs-lookup"><span data-stu-id="f9a1f-177">1</span></span>
</dt> <dd>

<span data-ttu-id="f9a1f-178">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="f9a1f-178">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="f9a1f-179">2</span><span class="sxs-lookup"><span data-stu-id="f9a1f-179">2</span></span>
</dt> <dd>

<span data-ttu-id="f9a1f-180">Predefinito</span><span class="sxs-lookup"><span data-stu-id="f9a1f-180">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f9a1f-181">**PolicySourceInitialProgramPath**</span><span class="sxs-lookup"><span data-stu-id="f9a1f-181">**PolicySourceInitialProgramPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9a1f-182">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f9a1f-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9a1f-183">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f9a1f-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9a1f-184">Indica se la proprietà **InitialProgramPath** è configurata dal server, da criteri di gruppo o per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-184">Indicates whether the **InitialProgramPath** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="f9a1f-185">0</span><span class="sxs-lookup"><span data-stu-id="f9a1f-185">0</span></span>
</dt> <dd>

<span data-ttu-id="f9a1f-186">Server</span><span class="sxs-lookup"><span data-stu-id="f9a1f-186">Server</span></span>

</dd> <dt>

<span data-ttu-id="f9a1f-187">1</span><span class="sxs-lookup"><span data-stu-id="f9a1f-187">1</span></span>
</dt> <dd>

<span data-ttu-id="f9a1f-188">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="f9a1f-188">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="f9a1f-189">2</span><span class="sxs-lookup"><span data-stu-id="f9a1f-189">2</span></span>
</dt> <dd>

<span data-ttu-id="f9a1f-190">Predefinito</span><span class="sxs-lookup"><span data-stu-id="f9a1f-190">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f9a1f-191">**PolicySourceStartIn**</span><span class="sxs-lookup"><span data-stu-id="f9a1f-191">**PolicySourceStartIn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9a1f-192">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f9a1f-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f9a1f-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f9a1f-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9a1f-194">Indica se la proprietà **Startin** è configurata dal server, da criteri di gruppo o per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-194">Indicates whether the **StartIn** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="f9a1f-195">0</span><span class="sxs-lookup"><span data-stu-id="f9a1f-195">0</span></span>
</dt> <dd>

<span data-ttu-id="f9a1f-196">Server</span><span class="sxs-lookup"><span data-stu-id="f9a1f-196">Server</span></span>

</dd> <dt>

<span data-ttu-id="f9a1f-197">1</span><span class="sxs-lookup"><span data-stu-id="f9a1f-197">1</span></span>
</dt> <dd>

<span data-ttu-id="f9a1f-198">Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="f9a1f-198">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="f9a1f-199">2</span><span class="sxs-lookup"><span data-stu-id="f9a1f-199">2</span></span>
</dt> <dd>

<span data-ttu-id="f9a1f-200">Predefinito</span><span class="sxs-lookup"><span data-stu-id="f9a1f-200">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f9a1f-201">**Startin**</span><span class="sxs-lookup"><span data-stu-id="f9a1f-201">**Startin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9a1f-202">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f9a1f-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9a1f-203">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f9a1f-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9a1f-204">Percorso della directory di lavoro del programma che l'utente eseguirà immediatamente dopo l'accesso al server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-204">The path of the working directory of the program the user will run immediately after logging on to the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="f9a1f-205">**Status**</span><span class="sxs-lookup"><span data-stu-id="f9a1f-205">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9a1f-206">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f9a1f-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9a1f-207">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f9a1f-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f9a1f-208">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="f9a1f-208">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="f9a1f-209">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-209">Current status of the object.</span></span> <span data-ttu-id="f9a1f-210">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-210">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="f9a1f-211">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="f9a1f-211">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="f9a1f-212">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="f9a1f-212">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f9a1f-213">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-213">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f9a1f-214">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-214">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f9a1f-215">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f9a1f-215">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="f9a1f-216">("OK")</span><span class="sxs-lookup"><span data-stu-id="f9a1f-216">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f9a1f-217">("Errore")</span><span class="sxs-lookup"><span data-stu-id="f9a1f-217">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f9a1f-218">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="f9a1f-218">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f9a1f-219">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="f9a1f-219">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f9a1f-220">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="f9a1f-220">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f9a1f-221">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="f9a1f-221">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f9a1f-222">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="f9a1f-222">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="f9a1f-223">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="f9a1f-223">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f9a1f-224">**Terminale**</span><span class="sxs-lookup"><span data-stu-id="f9a1f-224">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f9a1f-225">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f9a1f-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f9a1f-226">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f9a1f-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f9a1f-227">Nome del terminale.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-227">The name of the terminal.</span></span>

<span data-ttu-id="f9a1f-228">Questa proprietà viene ereditata da [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="f9a1f-228">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9a1f-229">Commenti</span><span class="sxs-lookup"><span data-stu-id="f9a1f-229">Remarks</span></span>

<span data-ttu-id="f9a1f-230">Tenere presente che i WinStations associati alla sessione della console non possono accedere ai metodi e alle proprietà di questa classe.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-230">Be aware that Winstations that are associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="f9a1f-231">Se viene effettuato un tentativo di eseguire questa operazione specificando "console" come valore della proprietà **TerminalName** , i metodi di questo oggetto restituiscono **WBEM \_ E \_ non \_ supportati**.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-231">If an attempt is made to do so by specifying "Console" as the value of the **TerminalName** property, methods of this object return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="f9a1f-232">Questo codice di errore viene restituito anche se una stazione della finestra tenta di chiamare i metodi di questo oggetto per aggiungere o modificare le proprietà di sicurezza degli account LocalSystem, LocalService o NetworkService.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-232">This error code is also returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="f9a1f-233">Per connettersi allo \\ \\ \\ spazio dei nomi CIMV2 TerminalServices radice, il livello di autenticazione deve includere la riservatezza dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-233">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="f9a1f-234">Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_ privacy**.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-234">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="f9a1f-235">Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore pari a 6.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-235">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="f9a1f-236">Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-236">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="f9a1f-237">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f9a1f-237">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f9a1f-238">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="f9a1f-238">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f9a1f-239">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="f9a1f-239">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f9a1f-240">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f9a1f-240">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9a1f-241">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9a1f-241">Requirements</span></span>



| <span data-ttu-id="f9a1f-242">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9a1f-242">Requirement</span></span> | <span data-ttu-id="f9a1f-243">Valore</span><span class="sxs-lookup"><span data-stu-id="f9a1f-243">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9a1f-244">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9a1f-244">Minimum supported client</span></span><br/> | <span data-ttu-id="f9a1f-245">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f9a1f-245">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f9a1f-246">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9a1f-246">Minimum supported server</span></span><br/> | <span data-ttu-id="f9a1f-247">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9a1f-247">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f9a1f-248">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f9a1f-248">Namespace</span></span><br/>                | <span data-ttu-id="f9a1f-249">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f9a1f-249">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f9a1f-250">MOF</span><span class="sxs-lookup"><span data-stu-id="f9a1f-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9a1f-251"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f9a1f-251"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f9a1f-252">DLL</span><span class="sxs-lookup"><span data-stu-id="f9a1f-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9a1f-253"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9a1f-253"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9a1f-254">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9a1f-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9a1f-255">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="f9a1f-255">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 


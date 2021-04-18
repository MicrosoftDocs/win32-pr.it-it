---
title: Classe Win32_TSPublishedApplication
description: Definisce le applicazioni rese disponibili per l'utilizzo remoto tramite Windows Server 2008 R2 RemoteApp.
ms.assetid: 5b9cb36b-3d8d-4105-acea-c79440d977fe
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSPublishedApplication Servizi Desktop remoto
- Classe Win32_TSPublishedApplication Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSPublishedApplication
- Win32_TSPublishedApplication.Caption
- Win32_TSPublishedApplication.Description
- Win32_TSPublishedApplication.InstallDate
- Win32_TSPublishedApplication.Name
- Win32_TSPublishedApplication.Status
- Win32_TSPublishedApplication.Alias
- Win32_TSPublishedApplication.SecurityDescriptor
- Win32_TSPublishedApplication.Path
- Win32_TSPublishedApplication.PathExists
- Win32_TSPublishedApplication.VPath
- Win32_TSPublishedApplication.IconPath
- Win32_TSPublishedApplication.IconIndex
- Win32_TSPublishedApplication.IconContents
- Win32_TSPublishedApplication.CommandLineSetting
- Win32_TSPublishedApplication.RequiredCommandLine
- Win32_TSPublishedApplication.ShowInPortal
- Win32_TSPublishedApplication.RDPFileContents
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3825087d05b622818c74f011f30b325ed8ff7f60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301440"
---
# <a name="win32_tspublishedapplication-class"></a><span data-ttu-id="bfd6c-105">Win32 \_ TSPublishedApplication (classe)</span><span class="sxs-lookup"><span data-stu-id="bfd6c-105">Win32\_TSPublishedApplication class</span></span>

<span data-ttu-id="bfd6c-106">Definisce le applicazioni rese disponibili per l'utilizzo remoto tramite Windows Server 2008 R2 RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-106">Defines the applications that are made available for remote use through Windows Server 2008 R2 RemoteApp.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfd6c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bfd6c-107">Syntax</span></span>

``` syntax
class Win32_TSPublishedApplication : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   Alias;
  string   SecurityDescriptor;
  string   Path;
  boolean  PathExists;
  string   VPath;
  string   IconPath;
  sint32   IconIndex;
  uint8    IconContents[];
  uint32   CommandLineSetting;
  string   RequiredCommandLine;
  boolean  ShowInPortal;
  string   RDPFileContents;
};
```

## <a name="members"></a><span data-ttu-id="bfd6c-108">Members</span><span class="sxs-lookup"><span data-stu-id="bfd6c-108">Members</span></span>

<span data-ttu-id="bfd6c-109">La classe **Win32 \_ TSPublishedApplication** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bfd6c-109">The **Win32\_TSPublishedApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="bfd6c-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bfd6c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bfd6c-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bfd6c-111">Properties</span></span>

<span data-ttu-id="bfd6c-112">La classe **Win32 \_ TSPublishedApplication** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-112">The **Win32\_TSPublishedApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bfd6c-113">**Alias**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-113">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfd6c-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bfd6c-115">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="bfd6c-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bfd6c-116">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-116">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="bfd6c-117">Alias dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-117">The alias of the application.</span></span> <span data-ttu-id="bfd6c-118">L'alias è un identificatore univoco per il programma che utilizza per impostazione predefinita il nome file del programma (senza l'estensione).</span><span class="sxs-lookup"><span data-stu-id="bfd6c-118">The alias is a unique identifier for the program that defaults to the program's file name (without the extension).</span></span>

</dd> <dt>

<span data-ttu-id="bfd6c-119">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfd6c-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bfd6c-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bfd6c-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bfd6c-122">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="bfd6c-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="bfd6c-123">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-123">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="bfd6c-124">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bfd6c-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bfd6c-125">**CommandLineSetting**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-125">**CommandLineSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfd6c-126">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bfd6c-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="bfd6c-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bfd6c-128">Impostazione degli argomenti della riga di comando per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-128">The command-line arguments setting for the application.</span></span> <span data-ttu-id="bfd6c-129">Sono possibili i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-129">The following values are possible.</span></span>

<dt>

<span data-ttu-id="bfd6c-130">0</span><span class="sxs-lookup"><span data-stu-id="bfd6c-130">0</span></span>
</dt> <dd>

<span data-ttu-id="bfd6c-131">Non consentire argomenti della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-131">Do not allow command-line arguments.</span></span>

</dd> <dt>

<span data-ttu-id="bfd6c-132">1</span><span class="sxs-lookup"><span data-stu-id="bfd6c-132">1</span></span>
</dt> <dd>

<span data-ttu-id="bfd6c-133">Consente qualsiasi argomento della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-133">Allow any command-line arguments.</span></span>

</dd> <dt>

<span data-ttu-id="bfd6c-134">2</span><span class="sxs-lookup"><span data-stu-id="bfd6c-134">2</span></span>
</dt> <dd>

<span data-ttu-id="bfd6c-135">Usare sempre gli argomenti della riga di comando necessari (specificati in **RequiredCommandLine**).</span><span class="sxs-lookup"><span data-stu-id="bfd6c-135">Always use the required command-line arguments (specified in **RequiredCommandLine**).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bfd6c-136">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-136">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfd6c-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bfd6c-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bfd6c-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfd6c-139">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-139">Description of the object.</span></span>

<span data-ttu-id="bfd6c-140">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bfd6c-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bfd6c-141">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-141">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfd6c-142">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-142">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="bfd6c-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bfd6c-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfd6c-144">Contenuto di byte dell'icona corrispondente all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-144">The byte contents of the icon that corresponds to the application.</span></span>

</dd> <dt>

<span data-ttu-id="bfd6c-145">**IconIndex**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-145">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfd6c-146">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-146">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bfd6c-147">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="bfd6c-147">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bfd6c-148">Indice o ID dell'icona.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-148">The index or ID of the icon.</span></span>

</dd> <dt>

<span data-ttu-id="bfd6c-149">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-149">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfd6c-150">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bfd6c-151">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="bfd6c-151">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bfd6c-152">Percorso dell'icona dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-152">The path of the application icon.</span></span>

</dd> <dt>

<span data-ttu-id="bfd6c-153">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-153">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfd6c-154">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-154">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bfd6c-155">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bfd6c-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bfd6c-156">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="bfd6c-156">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="bfd6c-157">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-157">The date the object was installed.</span></span> <span data-ttu-id="bfd6c-158">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-158">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="bfd6c-159">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bfd6c-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bfd6c-160">**Nome**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-160">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfd6c-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bfd6c-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bfd6c-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfd6c-163">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-163">The name of the object.</span></span>

<span data-ttu-id="bfd6c-164">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bfd6c-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bfd6c-165">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-165">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfd6c-166">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bfd6c-167">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="bfd6c-167">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bfd6c-168">Percorso dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-168">The path of the application.</span></span>

</dd> <dt>

<span data-ttu-id="bfd6c-169">**PathExists**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-169">**PathExists**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfd6c-170">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bfd6c-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bfd6c-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bfd6c-172">Indica se il percorso dell'applicazione è valido.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-172">Indicates whether the application path is valid.</span></span>

</dd> <dt>

<span data-ttu-id="bfd6c-173">**RDPFileContents**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-173">**RDPFileContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfd6c-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bfd6c-175">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="bfd6c-175">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bfd6c-176">Contenuto del file RDP corrispondente all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-176">The contents of the RDP file that correspond to the application.</span></span>

</dd> <dt>

<span data-ttu-id="bfd6c-177">**RequiredCommandLine**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-177">**RequiredCommandLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfd6c-178">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bfd6c-179">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="bfd6c-179">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bfd6c-180">Argomenti della riga di comando necessari per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-180">The command-line arguments that are required for the application.</span></span>

</dd> <dt>

<span data-ttu-id="bfd6c-181">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-181">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfd6c-182">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bfd6c-183">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="bfd6c-183">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bfd6c-184">Descrittore di sicurezza che controlla l'accesso all'applicazione in formato SDDL.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-184">A security descriptor that controls access to the application, in SDDL format.</span></span> <span data-ttu-id="bfd6c-185">Una stringa vuota implica l'autorizzazione All Access.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-185">An empty string implies allow all access.</span></span> <span data-ttu-id="bfd6c-186">Questo descrittore di sicurezza non supporta Ace DENY o ACE che fanno riferimento a utenti o gruppi non di dominio.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-186">This security descriptor does not support DENY ACEs, or ACEs that refer to nondomain users or groups.</span></span>

</dd> <dt>

<span data-ttu-id="bfd6c-187">**ShowInPortal**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-187">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfd6c-188">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-188">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bfd6c-189">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="bfd6c-189">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bfd6c-190">Indica se l'applicazione deve essere visualizzata in Accesso Web Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-190">Indicates whether the application should be shown in RD Web Access.</span></span>

</dd> <dt>

<span data-ttu-id="bfd6c-191">**Status**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-191">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfd6c-192">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bfd6c-193">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bfd6c-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bfd6c-194">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="bfd6c-194">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="bfd6c-195">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-195">Current status of the object.</span></span> <span data-ttu-id="bfd6c-196">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-196">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="bfd6c-197">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="bfd6c-197">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="bfd6c-198">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="bfd6c-198">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="bfd6c-199">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-199">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="bfd6c-200">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-200">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="bfd6c-201">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bfd6c-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="bfd6c-202">("OK")</span><span class="sxs-lookup"><span data-stu-id="bfd6c-202">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bfd6c-203">("Errore")</span><span class="sxs-lookup"><span data-stu-id="bfd6c-203">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bfd6c-204">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="bfd6c-204">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bfd6c-205">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="bfd6c-205">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bfd6c-206">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="bfd6c-206">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bfd6c-207">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="bfd6c-207">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bfd6c-208">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="bfd6c-208">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="bfd6c-209">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="bfd6c-209">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bfd6c-210">**VPath**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-210">**VPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfd6c-211">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="bfd6c-211">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bfd6c-212">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="bfd6c-212">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bfd6c-213">Percorso virtuale dell'applicazione, ovvero il percorso con le variabili di ambiente incluse.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-213">The virtual path of the application, meaning the path with environment variables included.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bfd6c-214">Commenti</span><span class="sxs-lookup"><span data-stu-id="bfd6c-214">Remarks</span></span>

<span data-ttu-id="bfd6c-215">Per impostare le proprietà tramite questa classe, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-215">You must be a member of the Administrators group to set properties by using this class.</span></span>

<span data-ttu-id="bfd6c-216">Per connettersi allo \\ \\ \\ spazio dei nomi CIMV2 TerminalServices radice, il livello di autenticazione deve includere la riservatezza dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-216">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="bfd6c-217">Per le chiamate C/C++, si tratta di un livello di autenticazione del livello di autenticazione **RPC \_ C \_ \_ \_ PKT \_**, che può essere impostato tramite la funzione com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="bfd6c-217">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="bfd6c-218">Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione di **WbemAuthenticationLevelPktPrivacy** o "su PktPrivacy", con un valore pari a 6.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-218">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="bfd6c-219">Il seguente esempio di Visual Basic Scripting Edition (VBScript) illustra come connettersi a un computer remoto con la privacy dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-219">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="bfd6c-220">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="bfd6c-220">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bfd6c-221">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="bfd6c-221">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bfd6c-222">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="bfd6c-222">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bfd6c-223">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="bfd6c-223">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="bfd6c-224">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bfd6c-224">Requirements</span></span>



| <span data-ttu-id="bfd6c-225">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfd6c-225">Requirement</span></span> | <span data-ttu-id="bfd6c-226">Valore</span><span class="sxs-lookup"><span data-stu-id="bfd6c-226">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfd6c-227">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bfd6c-227">Minimum supported client</span></span><br/> | <span data-ttu-id="bfd6c-228">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="bfd6c-228">None supported</span></span><br/>                                                               |
| <span data-ttu-id="bfd6c-229">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bfd6c-229">Minimum supported server</span></span><br/> | <span data-ttu-id="bfd6c-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bfd6c-230">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bfd6c-231">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bfd6c-231">Namespace</span></span><br/>                | <span data-ttu-id="bfd6c-232">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="bfd6c-232">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="bfd6c-233">MOF</span><span class="sxs-lookup"><span data-stu-id="bfd6c-233">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bfd6c-234"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bfd6c-234"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="bfd6c-235">DLL</span><span class="sxs-lookup"><span data-stu-id="bfd6c-235">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfd6c-236"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfd6c-236"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 


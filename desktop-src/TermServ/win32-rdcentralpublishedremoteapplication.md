---
title: Classe Win32_RDCentralPublishedRemoteApplication
description: Descrive un'applicazione pubblicata in un altro computer per l'utilizzo remoto tramite Servizi terminal.
ms.assetid: 8605bd1e-e825-4fd9-b14f-9d3bdac489f1
ms.tgt_platform: multiple
keywords:
- Classe Win32_RDCentralPublishedRemoteApplication Servizi Desktop remoto
- Classe Win32_RDCentralPublishedRemoteApplication Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedRemoteApplication
- Win32_RDCentralPublishedRemoteApplication.Caption
- Win32_RDCentralPublishedRemoteApplication.Description
- Win32_RDCentralPublishedRemoteApplication.InstallDate
- Win32_RDCentralPublishedRemoteApplication.Name
- Win32_RDCentralPublishedRemoteApplication.Status
- Win32_RDCentralPublishedRemoteApplication.PublishingFarm
- Win32_RDCentralPublishedRemoteApplication.Alias
- Win32_RDCentralPublishedRemoteApplication.SecurityDescriptor
- Win32_RDCentralPublishedRemoteApplication.Path
- Win32_RDCentralPublishedRemoteApplication.VPath
- Win32_RDCentralPublishedRemoteApplication.IconContents
- Win32_RDCentralPublishedRemoteApplication.CommandLineSetting
- Win32_RDCentralPublishedRemoteApplication.RequiredCommandLine
- Win32_RDCentralPublishedRemoteApplication.ShowInPortal
- Win32_RDCentralPublishedRemoteApplication.AppID
- Win32_RDCentralPublishedRemoteApplication.RDPFileContents
- Win32_RDCentralPublishedRemoteApplication.Folders
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd837f62d8d0787d992e8eed7316ed1ef3f199ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964084"
---
# <a name="win32_rdcentralpublishedremoteapplication-class"></a><span data-ttu-id="9b8cb-105">Win32 \_ RDCentralPublishedRemoteApplication (classe)</span><span class="sxs-lookup"><span data-stu-id="9b8cb-105">Win32\_RDCentralPublishedRemoteApplication class</span></span>

<span data-ttu-id="9b8cb-106">Descrive un'applicazione pubblicata in un altro computer per l'utilizzo remoto tramite Servizi terminal.</span><span class="sxs-lookup"><span data-stu-id="9b8cb-106">Describes an application published on another computer, for remote use through Terminal Services.</span></span>

<span data-ttu-id="9b8cb-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9b8cb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b8cb-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9b8cb-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_RDCentralPublishedRemoteApplication : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   PublishingFarm;
  string   Alias;
  string   SecurityDescriptor;
  string   Path;
  string   VPath;
  uint8    IconContents[];
  uint32   CommandLineSetting;
  string   RequiredCommandLine;
  boolean  ShowInPortal;
  string   AppID;
  string   RDPFileContents;
  string   Folders[];
};
```

## <a name="members"></a><span data-ttu-id="9b8cb-109">Members</span><span class="sxs-lookup"><span data-stu-id="9b8cb-109">Members</span></span>

<span data-ttu-id="9b8cb-110">La classe **Win32 \_ RDCentralPublishedRemoteApplication** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9b8cb-110">The **Win32\_RDCentralPublishedRemoteApplication** class has these types of members:</span></span>

-   [<span data-ttu-id="9b8cb-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9b8cb-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9b8cb-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9b8cb-112">Properties</span></span>

<span data-ttu-id="9b8cb-113">La classe **Win32 \_ RDCentralPublishedRemoteApplication** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9b8cb-113">The **Win32\_RDCentralPublishedRemoteApplication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9b8cb-114">**Alias**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-114">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b8cb-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b8cb-116">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9b8cb-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9b8cb-117">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9b8cb-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9b8cb-118">Alias dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b8cb-118">Alias of the application.</span></span>

</dd> <dt>

<span data-ttu-id="9b8cb-119">**AppID**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-119">**AppID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b8cb-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b8cb-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9b8cb-121">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9b8cb-122">AppID viene usato per l'aggiunta nei client.</span><span class="sxs-lookup"><span data-stu-id="9b8cb-122">AppID is used for pinning on the clients.</span></span>

</dd> <dt>

<span data-ttu-id="9b8cb-123">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b8cb-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b8cb-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9b8cb-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b8cb-126">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="9b8cb-126">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="9b8cb-127">Breve descrizione (stringa a una riga) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9b8cb-127">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="9b8cb-128">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9b8cb-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b8cb-129">**CommandLineSetting**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-129">**CommandLineSetting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b8cb-130">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9b8cb-131">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9b8cb-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9b8cb-132">Indica se sono necessari argomenti della riga di comando per questa applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b8cb-132">Whether command-line arguments are required for this application.</span></span>

<dt>

<span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>

<span data-ttu-id="9b8cb-133"><span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**DoNotAllow** (0)</span><span class="sxs-lookup"><span data-stu-id="9b8cb-133"><span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**DoNotAllow** (0)</span></span>


</dt> <dd>

<span data-ttu-id="9b8cb-134">Non consentire</span><span class="sxs-lookup"><span data-stu-id="9b8cb-134">Do not allow</span></span>

</dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span data-ttu-id="9b8cb-135"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Consenti** (1)</span><span class="sxs-lookup"><span data-stu-id="9b8cb-135"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Allow** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>

<span data-ttu-id="9b8cb-136"><span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**Richiedi** (2)</span><span class="sxs-lookup"><span data-stu-id="9b8cb-136"><span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**Require** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9b8cb-137">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-137">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b8cb-138">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b8cb-139">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9b8cb-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b8cb-140">Descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9b8cb-140">Description of the object.</span></span>

<span data-ttu-id="9b8cb-141">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9b8cb-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b8cb-142">**Cartelle**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-142">**Folders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b8cb-143">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-143">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9b8cb-144">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9b8cb-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9b8cb-145">Elenco delle cartelle in cui deve essere visualizzata la risorsa.</span><span class="sxs-lookup"><span data-stu-id="9b8cb-145">List of the folders where this resource should be displayed.</span></span>

</dd> <dt>

<span data-ttu-id="9b8cb-146">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-146">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b8cb-147">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-147">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="9b8cb-148">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9b8cb-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9b8cb-149">Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9b8cb-149">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9b8cb-150">Contenuto dell'icona corrispondente all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b8cb-150">Contents of the icon corresponding to the application.</span></span>

</dd> <dt>

<span data-ttu-id="9b8cb-151">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-151">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b8cb-152">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9b8cb-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9b8cb-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b8cb-154">Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="9b8cb-154">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="9b8cb-155">Data di installazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9b8cb-155">The date the object was installed.</span></span> <span data-ttu-id="9b8cb-156">La mancanza di un valore non indica che l'oggetto non è installato.</span><span class="sxs-lookup"><span data-stu-id="9b8cb-156">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="9b8cb-157">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9b8cb-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b8cb-158">**Nome**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b8cb-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b8cb-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9b8cb-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b8cb-161">Nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9b8cb-161">The name of the object.</span></span>

<span data-ttu-id="9b8cb-162">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9b8cb-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b8cb-163">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-163">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b8cb-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b8cb-165">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9b8cb-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9b8cb-166">Percorso dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="9b8cb-166">Path to the application</span></span>

</dd> <dt>

<span data-ttu-id="9b8cb-167">**PublishingFarm**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-167">**PublishingFarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b8cb-168">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b8cb-169">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9b8cb-169">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9b8cb-170">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9b8cb-170">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9b8cb-171">Alias della farm che ha pubblicato l'applicazione</span><span class="sxs-lookup"><span data-stu-id="9b8cb-171">Alias of the farm that published the Application</span></span>

</dd> <dt>

<span data-ttu-id="9b8cb-172">**RDPFileContents**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-172">**RDPFileContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b8cb-173">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b8cb-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9b8cb-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b8cb-175">Contenuto del file RDP corrispondente all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b8cb-175">Contents of the RDP file corresponding to the application.</span></span>

</dd> <dt>

<span data-ttu-id="9b8cb-176">**RequiredCommandLine**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-176">**RequiredCommandLine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b8cb-177">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b8cb-178">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9b8cb-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9b8cb-179">Argomenti della riga di comando necessari per questa applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b8cb-179">Command-line arguments required for this application.</span></span>

</dd> <dt>

<span data-ttu-id="9b8cb-180">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-180">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b8cb-181">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b8cb-182">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9b8cb-182">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="9b8cb-183">Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9b8cb-183">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9b8cb-184">Descrittore di sicurezza che controlla l'accesso all'applicazione in formato SDDL.</span><span class="sxs-lookup"><span data-stu-id="9b8cb-184">Security Descriptor controlling access to the application, in SDDL Format.</span></span> <span data-ttu-id="9b8cb-185">La stringa vuota implica l'autorizzazione All Access.</span><span class="sxs-lookup"><span data-stu-id="9b8cb-185">Empty string implies allow all access.</span></span>

</dd> <dt>

<span data-ttu-id="9b8cb-186">**ShowInPortal**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-186">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b8cb-187">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-187">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9b8cb-188">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9b8cb-188">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9b8cb-189">**true** se l'applicazione deve essere visualizzata nel accesso Web di Servizi terminal; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="9b8cb-189">**true** if this application should be shown in the TS Web Access; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="9b8cb-190">**Status**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-190">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b8cb-191">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b8cb-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9b8cb-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b8cb-193">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="9b8cb-193">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="9b8cb-194">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9b8cb-194">Current status of the object.</span></span> <span data-ttu-id="9b8cb-195">È possibile definire diversi stati operativi e non operativi.</span><span class="sxs-lookup"><span data-stu-id="9b8cb-195">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="9b8cb-196">Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro).</span><span class="sxs-lookup"><span data-stu-id="9b8cb-196">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="9b8cb-197">Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service".</span><span class="sxs-lookup"><span data-stu-id="9b8cb-197">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="9b8cb-198">Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative.</span><span class="sxs-lookup"><span data-stu-id="9b8cb-198">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="9b8cb-199">Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.</span><span class="sxs-lookup"><span data-stu-id="9b8cb-199">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="9b8cb-200">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9b8cb-200">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="9b8cb-201">("OK")</span><span class="sxs-lookup"><span data-stu-id="9b8cb-201">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9b8cb-202">("Errore")</span><span class="sxs-lookup"><span data-stu-id="9b8cb-202">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9b8cb-203">("Danneggiato")</span><span class="sxs-lookup"><span data-stu-id="9b8cb-203">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9b8cb-204">("Sconosciuto")</span><span class="sxs-lookup"><span data-stu-id="9b8cb-204">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9b8cb-205">("Errore di predazione")</span><span class="sxs-lookup"><span data-stu-id="9b8cb-205">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9b8cb-206">("Avvio")</span><span class="sxs-lookup"><span data-stu-id="9b8cb-206">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9b8cb-207">("Arresto")</span><span class="sxs-lookup"><span data-stu-id="9b8cb-207">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="9b8cb-208">("Servizio")</span><span class="sxs-lookup"><span data-stu-id="9b8cb-208">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9b8cb-209">**VPath**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-209">**VPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b8cb-210">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9b8cb-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9b8cb-211">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="9b8cb-211">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="9b8cb-212">Percorso virtuale dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b8cb-212">Virtual Path to the application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9b8cb-213">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b8cb-213">Requirements</span></span>



| <span data-ttu-id="9b8cb-214">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b8cb-214">Requirement</span></span> | <span data-ttu-id="9b8cb-215">Valore</span><span class="sxs-lookup"><span data-stu-id="9b8cb-215">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b8cb-216">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b8cb-216">Minimum supported client</span></span><br/> | <span data-ttu-id="9b8cb-217">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9b8cb-217">None supported</span></span><br/>                                                                |
| <span data-ttu-id="9b8cb-218">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b8cb-218">Minimum supported server</span></span><br/> | <span data-ttu-id="9b8cb-219">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9b8cb-219">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="9b8cb-220">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9b8cb-220">Namespace</span></span><br/>                | <span data-ttu-id="9b8cb-221">Radice \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="9b8cb-221">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="9b8cb-222">MOF</span><span class="sxs-lookup"><span data-stu-id="9b8cb-222">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b8cb-223"><dt>Tscpub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9b8cb-223"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="9b8cb-224">DLL</span><span class="sxs-lookup"><span data-stu-id="9b8cb-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b8cb-225"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b8cb-225"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 


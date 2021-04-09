---
description: Rappresenta il software di basso livello caricato in RAM per configurare e avviare il sistema.
ms.assetid: D123601A-DEE6-43EA-BD95-1F7F0F2C2B43
title: Classe Msvm_BIOSElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BIOSElement
- Msvm_BIOSElement.InstanceID
- Msvm_BIOSElement.Caption
- Msvm_BIOSElement.Description
- Msvm_BIOSElement.ElementName
- Msvm_BIOSElement.InstallDate
- Msvm_BIOSElement.OperationalStatus
- Msvm_BIOSElement.StatusDescriptions
- Msvm_BIOSElement.Status
- Msvm_BIOSElement.HealthState
- Msvm_BIOSElement.CommunicationStatus
- Msvm_BIOSElement.DetailedStatus
- Msvm_BIOSElement.OperatingStatus
- Msvm_BIOSElement.PrimaryStatus
- Msvm_BIOSElement.Name
- Msvm_BIOSElement.SoftwareElementState
- Msvm_BIOSElement.SoftwareElementID
- Msvm_BIOSElement.TargetOperatingSystem
- Msvm_BIOSElement.OtherTargetOS
- Msvm_BIOSElement.BuildNumber
- Msvm_BIOSElement.SerialNumber
- Msvm_BIOSElement.CodeSet
- Msvm_BIOSElement.IdentificationCode
- Msvm_BIOSElement.LanguageEdition
- Msvm_BIOSElement.Version
- Msvm_BIOSElement.Manufacturer
- Msvm_BIOSElement.PrimaryBIOS
- Msvm_BIOSElement.ListOfLanguages
- Msvm_BIOSElement.CurrentLanguage
- Msvm_BIOSElement.LoadedStartingAddress
- Msvm_BIOSElement.LoadedEndingAddress
- Msvm_BIOSElement.LoadUtilityInformation
- Msvm_BIOSElement.ReleaseDate
- Msvm_BIOSElement.RegistryURIs
- Msvm_BIOSElement.BIOSGUID
- Msvm_BIOSElement.BIOSSerialNumber
- Msvm_BIOSElement.BaseBoardSerialNumber
- Msvm_BIOSElement.ChassisSerialNumber
- Msvm_BIOSElement.ChassisAssetTag
- Msvm_BIOSElement.BIOSNumLock
- Msvm_BIOSElement.BootOrder
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d8d36ea50791bf6f1413815583fe1168f564d50d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879758"
---
# <a name="msvm_bioselement-class"></a><span data-ttu-id="76f78-103">\_Classe MSVM bioselement</span><span class="sxs-lookup"><span data-stu-id="76f78-103">Msvm\_BIOSElement class</span></span>

<span data-ttu-id="76f78-104">Rappresenta il software di basso livello caricato in RAM per configurare e avviare il sistema.</span><span class="sxs-lookup"><span data-stu-id="76f78-104">Represents the low-level software that is loaded into RAM to configure and start the system.</span></span> <span data-ttu-id="76f78-105">Il BIOS non è un dispositivo logico, quindi il BIOS virtuale non deve essere considerato come un dispositivo della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="76f78-105">The BIOS is not a logical device, hence the virtual BIOS should not be thought of as a virtual machine device.</span></span> <span data-ttu-id="76f78-106">Poiché non si tratta di un dispositivo, non dispone di un pool di risorse corrispondente.</span><span class="sxs-lookup"><span data-stu-id="76f78-106">As it is not a device, it does not have a corresponding resource pool.</span></span> <span data-ttu-id="76f78-107">L'oggetto BIOS è associato alla macchina virtuale tramite l'associazione [**\_ SystemBIOS di MSVM**](msvm-systembios.md) .</span><span class="sxs-lookup"><span data-stu-id="76f78-107">The BIOS object is associated with the virtual machine through the [**Msvm\_SystemBIOS**](msvm-systembios.md) association.</span></span>

<span data-ttu-id="76f78-108">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="76f78-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="76f78-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76f78-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BIOSElement : CIM_BIOSElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   Name = "BIOS";
  uint16   SoftwareElementState = 2;
  string   SoftwareElementID = "Microsoft:GUID\device-specific data";
  uint16   TargetOperatingSystem = 0;
  string   OtherTargetOS;
  string   BuildNumber = 14;
  string   SerialNumber;
  string   CodeSet;
  string   IdentificationCode;
  string   LanguageEdition;
  string   Version = "8.02.00";
  string   Manufacturer = "Microsoft Corporation";
  boolean  PrimaryBIOS = True;
  string   ListOfLanguages[] = "en|US|iso8859-1";
  string   CurrentLanguage = "en|US|iso8859-1";
  unit64   LoadedStartingAddress = 0xE0000;
  unit64   LoadedEndingAddress = 0xFFFFF;
  string   LoadUtilityInformation;
  datetime ReleaseDate;
  string   RegistryURIs[];
  string   BIOSGUID;
  string   BIOSSerialNumber;
  string   BaseBoardSerialNumber;
  string   ChassisSerialNumber;
  string   ChassisAssetTag;
  boolean  BIOSNumLock;
  uint16   BootOrder[];
};
```

## <a name="members"></a><span data-ttu-id="76f78-110">Members</span><span class="sxs-lookup"><span data-stu-id="76f78-110">Members</span></span>

<span data-ttu-id="76f78-111">La classe **MSVM \_ bioselement** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="76f78-111">The **Msvm\_BIOSElement** class has these types of members:</span></span>

-   [<span data-ttu-id="76f78-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="76f78-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="76f78-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="76f78-113">Properties</span></span>

<span data-ttu-id="76f78-114">La classe **MSVM \_ bioselement** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="76f78-114">The **Msvm\_BIOSElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="76f78-115">**BaseBoardSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="76f78-115">**BaseBoardSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="76f78-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76f78-118">Il numero di serie della lavagna di base nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="76f78-118">The serial number for the base board on the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="76f78-119">**BIOSGUID**</span><span class="sxs-lookup"><span data-stu-id="76f78-119">**BIOSGUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="76f78-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76f78-122">Identificatore univoco per il BIOS.</span><span class="sxs-lookup"><span data-stu-id="76f78-122">The unique identifier for the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="76f78-123">**BIOSNumLock**</span><span class="sxs-lookup"><span data-stu-id="76f78-123">**BIOSNumLock**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-124">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="76f78-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76f78-126">Stato abilitato del blocco num nel BIOS.</span><span class="sxs-lookup"><span data-stu-id="76f78-126">The enabled state of the Num Lock in the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="76f78-127">**BIOSSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="76f78-127">**BIOSSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="76f78-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76f78-130">Il numero di serie per il BIOS.</span><span class="sxs-lookup"><span data-stu-id="76f78-130">The serial number for the BIOS.</span></span>

</dd> <dt>

<span data-ttu-id="76f78-131">**BootOrder**</span><span class="sxs-lookup"><span data-stu-id="76f78-131">**BootOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-132">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76f78-132">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="76f78-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76f78-134">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato"), [**massimo**](/windows/desktop/WmiSdk/standard-qualifiers) (4)</span><span class="sxs-lookup"><span data-stu-id="76f78-134">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MAX**](/windows/desktop/WmiSdk/standard-qualifiers) (4)</span></span>
</dt> </dl>

<span data-ttu-id="76f78-135">Ordine in cui verrà eseguita la ricerca dei dispositivi per un settore di avvio all'avvio.</span><span class="sxs-lookup"><span data-stu-id="76f78-135">The order in which devices will be searched for a boot sector at startup.</span></span>

</dd> <dt>

<span data-ttu-id="76f78-136">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="76f78-136">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="76f78-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76f78-139">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="76f78-139">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="76f78-140">Identificatore interno per questa compilazione dell'elemento software.</span><span class="sxs-lookup"><span data-stu-id="76f78-140">The internal identifier for this compilation of software element.</span></span> <span data-ttu-id="76f78-141">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)ed è sempre impostata su 14.</span><span class="sxs-lookup"><span data-stu-id="76f78-141">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to 14.</span></span>

</dd> <dt>

<span data-ttu-id="76f78-142">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="76f78-142">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-143">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="76f78-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-144">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76f78-145">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="76f78-145">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="76f78-146">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="76f78-146">A short description of the object.</span></span> <span data-ttu-id="76f78-147">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="76f78-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="76f78-148">**ChassisAssetTag**</span><span class="sxs-lookup"><span data-stu-id="76f78-148">**ChassisAssetTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="76f78-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-150">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76f78-151">Popolato automaticamente dal BIOS quando viene creata la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="76f78-151">Automatically populated by the BIOS when the virtual machine is created.</span></span>

</dd> <dt>

<span data-ttu-id="76f78-152">**ChassisSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="76f78-152">**ChassisSerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-153">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="76f78-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76f78-155">Popolato automaticamente dal BIOS quando viene creata la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="76f78-155">Automatically populated by the BIOS when the virtual machine is created.</span></span>

</dd> <dt>

<span data-ttu-id="76f78-156">**CodeSet**</span><span class="sxs-lookup"><span data-stu-id="76f78-156">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="76f78-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76f78-159">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="76f78-159">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="76f78-160">Set di codici utilizzato dall'elemento software.</span><span class="sxs-lookup"><span data-stu-id="76f78-160">The code set used by the software element.</span></span> <span data-ttu-id="76f78-161">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="76f78-161">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="76f78-162">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="76f78-162">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-163">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76f78-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76f78-165">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="76f78-165">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="76f78-166">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="76f78-166">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="76f78-167">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="76f78-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="76f78-168">**CurrentLanguage**</span><span class="sxs-lookup"><span data-stu-id="76f78-168">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-169">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="76f78-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76f78-171">Lingua attualmente selezionata per il BIOS.</span><span class="sxs-lookup"><span data-stu-id="76f78-171">The currently selected language for the BIOS.</span></span> <span data-ttu-id="76f78-172">Questa proprietà viene ereditata da [**CIM \_ bioselement**](/windows/desktop/CIMWin32Prov/cim-bioselement)ed è sempre impostata su "en \| US \| ISO8859-1".</span><span class="sxs-lookup"><span data-stu-id="76f78-172">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to "en\|US\|iso8859-1".</span></span>

</dd> <dt>

<span data-ttu-id="76f78-173">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="76f78-173">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="76f78-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76f78-176">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="76f78-176">A description of the object.</span></span> <span data-ttu-id="76f78-177">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="76f78-177">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="76f78-178">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="76f78-178">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-179">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76f78-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76f78-181">Integra la proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="76f78-181">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="76f78-182">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="76f78-182">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="76f78-183">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="76f78-183">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="76f78-184">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="76f78-184">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-185">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="76f78-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-186">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76f78-187">Nome visualizzato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="76f78-187">A display name for the element.</span></span> <span data-ttu-id="76f78-188">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="76f78-188">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="76f78-189">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="76f78-189">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-190">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76f78-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-191">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76f78-192">Specifica lo stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="76f78-192">Specifies the current health of the element.</span></span> <span data-ttu-id="76f78-193">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="76f78-193">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span>

<span data-ttu-id="76f78-194">Quando si verifica un errore critico, controllare il registro eventi per informazioni dettagliate.</span><span class="sxs-lookup"><span data-stu-id="76f78-194">When a critical error occurs, check the event log for details.</span></span> <span data-ttu-id="76f78-195">La proprietà **EnabledState** può inoltre contenere ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="76f78-195">The **EnabledState** property can also contain more information.</span></span> <span data-ttu-id="76f78-196">Ad esempio, quando lo spazio su disco è insufficiente, **HealthState** è impostato su 25, la macchina virtuale viene sospesa e **EnabledState** è impostato su 32768 (in pausa).</span><span class="sxs-lookup"><span data-stu-id="76f78-196">For example, when disk space is critically low, **HealthState** is set to 25, the virtual machine pauses, and **EnabledState** is set to 32768 (Paused).</span></span>

<span data-ttu-id="76f78-197">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="76f78-197">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>



| <span data-ttu-id="76f78-198">Valore</span><span class="sxs-lookup"><span data-stu-id="76f78-198">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="76f78-199">Significato</span><span class="sxs-lookup"><span data-stu-id="76f78-199">Meaning</span></span>                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="76f78-200"><dt>**OK**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="76f78-200"><dt>**OK**</dt> <dt>5</dt></span></span> </dl>                                                                               | <span data-ttu-id="76f78-201">La macchina virtuale è completamente funzionante e funziona entro i normali parametri operativi e senza errori.</span><span class="sxs-lookup"><span data-stu-id="76f78-201">The virtual machine is fully functional and is operating within normal operational parameters and without error.</span></span><br/>                                                                                                                                                                                    |
| <span id="Major_Failure"></span><span id="major_failure"></span><span id="MAJOR_FAILURE"></span><dl> <span data-ttu-id="76f78-202"><dt>**Errore principale**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="76f78-202"><dt>**Major Failure**</dt> <dt>20</dt></span></span> </dl>             | <span data-ttu-id="76f78-203">Si è verificato un errore grave della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="76f78-203">The virtual machine has suffered a major failure.</span></span> <span data-ttu-id="76f78-204">Questo valore viene usato quando lo spazio su disco di uno o più dischi che contengono i VHD della macchina virtuale è insufficiente e la macchina virtuale è stata sospesa.</span><span class="sxs-lookup"><span data-stu-id="76f78-204">This value is used when one or more disks that contain the virtual machine's VHDs is low on disk space and the virtual machine has been paused.</span></span><br/>                                                                                                   |
| <span id="Critical_failure"></span><span id="critical_failure"></span><span id="CRITICAL_FAILURE"></span><dl> <span data-ttu-id="76f78-205"><dt>**Errore critico**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="76f78-205"><dt>**Critical failure**</dt> <dt>25</dt></span></span> </dl> | <span data-ttu-id="76f78-206">L'elemento è non funzionale e il ripristino potrebbe non essere possibile.</span><span class="sxs-lookup"><span data-stu-id="76f78-206">The element is nonfunctional, and recovery might not be possible.</span></span> <span data-ttu-id="76f78-207">Questo può indicare che il processo di lavoro della macchina virtuale (Vmwp.exe) non risponde alle richieste di controllo o informazioni oppure che uno o più dischi che contengono i dischi rigidi virtuali per la macchina virtuale hanno spazio su disco insufficiente.</span><span class="sxs-lookup"><span data-stu-id="76f78-207">This can indicate that the worker process for the virtual machine (Vmwp.exe) is not responding to control or information requests, or that one or more disks that contain the VHDs for the virtual machine are low on disk space.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="76f78-208">**IdentificationCode**</span><span class="sxs-lookup"><span data-stu-id="76f78-208">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-209">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="76f78-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-210">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76f78-211">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="76f78-211">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="76f78-212">Identificatore del produttore di questo elemento software.</span><span class="sxs-lookup"><span data-stu-id="76f78-212">The manufacturer's identifier for this software element.</span></span> <span data-ttu-id="76f78-213">Spesso si tratta di una SKU (Stock Keeping Unit) o di un numero di parte.</span><span class="sxs-lookup"><span data-stu-id="76f78-213">Often this will be a stock keeping unit (SKU) or a part number.</span></span> <span data-ttu-id="76f78-214">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="76f78-214">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="76f78-215">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="76f78-215">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-216">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="76f78-216">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-217">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76f78-218">Popolato automaticamente dal BIOS quando viene creata la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="76f78-218">Automatically populated by the BIOS when the virtual machine is created.</span></span> <span data-ttu-id="76f78-219">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="76f78-219">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="76f78-220">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="76f78-220">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-221">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="76f78-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-222">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76f78-223">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="76f78-223">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="76f78-224">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="76f78-224">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="76f78-225">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="76f78-225">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="76f78-226">**LanguageEdition**</span><span class="sxs-lookup"><span data-stu-id="76f78-226">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-227">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="76f78-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-228">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76f78-229">Qualificatori: **maxlen** (32)</span><span class="sxs-lookup"><span data-stu-id="76f78-229">Qualifiers: **MaxLen** (32)</span></span>
</dt> </dl>

<span data-ttu-id="76f78-230">Edizione del linguaggio di questo elemento software.</span><span class="sxs-lookup"><span data-stu-id="76f78-230">The language edition of this software element.</span></span> <span data-ttu-id="76f78-231">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="76f78-231">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="76f78-232">**ListOfLanguages**</span><span class="sxs-lookup"><span data-stu-id="76f78-232">**ListOfLanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-233">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="76f78-233">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="76f78-234">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76f78-235">Elenco di lingue installabili per il BIOS.</span><span class="sxs-lookup"><span data-stu-id="76f78-235">A list of installable languages for the BIOS.</span></span> <span data-ttu-id="76f78-236">Questa proprietà viene ereditata da [**CIM \_ bioselement**](/windows/desktop/CIMWin32Prov/cim-bioselement)ed è sempre impostata su "en \| US \| ISO8859-1".</span><span class="sxs-lookup"><span data-stu-id="76f78-236">THIS property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to "en\|US\|iso8859-1".</span></span>

</dd> <dt>

<span data-ttu-id="76f78-237">**LoadedEndingAddress**</span><span class="sxs-lookup"><span data-stu-id="76f78-237">**LoadedEndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-238">Tipo di dati: **unit64**</span><span class="sxs-lookup"><span data-stu-id="76f78-238">Data type: **unit64**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-239">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-239">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76f78-240">Indirizzo finale della memoria occupata da questo BIOS.</span><span class="sxs-lookup"><span data-stu-id="76f78-240">The ending address of the memory which this BIOS occupies.</span></span> <span data-ttu-id="76f78-241">Questa proprietà viene ereditata da [**CIM \_ bioselement**](/windows/desktop/CIMWin32Prov/cim-bioselement)ed è sempre impostata su 0xfffff.</span><span class="sxs-lookup"><span data-stu-id="76f78-241">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to 0xFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="76f78-242">**LoadedStartingAddress**</span><span class="sxs-lookup"><span data-stu-id="76f78-242">**LoadedStartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-243">Tipo di dati: **unit64**</span><span class="sxs-lookup"><span data-stu-id="76f78-243">Data type: **unit64**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-244">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76f78-245">Indirizzo iniziale della memoria occupata da questo BIOS.</span><span class="sxs-lookup"><span data-stu-id="76f78-245">The starting address of the memory which this BIOS occupies.</span></span> <span data-ttu-id="76f78-246">Questa proprietà viene ereditata da [**CIM \_ bioselement**](/windows/desktop/CIMWin32Prov/cim-bioselement)ed è sempre impostata su 0xE0000.</span><span class="sxs-lookup"><span data-stu-id="76f78-246">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to 0xE0000.</span></span>

</dd> <dt>

<span data-ttu-id="76f78-247">**LoadUtilityInformation**</span><span class="sxs-lookup"><span data-stu-id="76f78-247">**LoadUtilityInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-248">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="76f78-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-249">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76f78-250">Stringa che descrive l'utilità Flash/Load BIOS necessaria per aggiornare l'elemento BIOS.</span><span class="sxs-lookup"><span data-stu-id="76f78-250">A string that describes the BIOS flash/load utility that is required to update the BIOS element.</span></span> <span data-ttu-id="76f78-251">La versione e altre informazioni possono essere indicate in questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="76f78-251">Version and other information may be indicated in this property.</span></span> <span data-ttu-id="76f78-252">Questa proprietà viene ereditata da [**CIM \_ bioselement**](/windows/desktop/CIMWin32Prov/cim-bioselement)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="76f78-252">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="76f78-253">**Produttore**</span><span class="sxs-lookup"><span data-stu-id="76f78-253">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-254">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="76f78-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-255">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76f78-256">Qualificatori: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="76f78-256">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="76f78-257">Produttore del BIOS.</span><span class="sxs-lookup"><span data-stu-id="76f78-257">The manufacturer of this BIOS.</span></span> <span data-ttu-id="76f78-258">Questa proprietà viene ereditata da [**CIM \_ bioselement**](/windows/desktop/CIMWin32Prov/cim-bioselement)ed è sempre impostata su "Microsoft Corporation".</span><span class="sxs-lookup"><span data-stu-id="76f78-258">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to "Microsoft Corporation".</span></span>

</dd> <dt>

<span data-ttu-id="76f78-259">**Nome**</span><span class="sxs-lookup"><span data-stu-id="76f78-259">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-260">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="76f78-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-261">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76f78-262">Qualificatori: **maxlen** (1024)</span><span class="sxs-lookup"><span data-stu-id="76f78-262">Qualifiers: **MaxLen** (1024)</span></span>
</dt> </dl>

<span data-ttu-id="76f78-263">Nome utilizzato per identificare questo elemento software.</span><span class="sxs-lookup"><span data-stu-id="76f78-263">The name used to identify this software element.</span></span> <span data-ttu-id="76f78-264">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="76f78-264">When subclassed, this property can be overridden to be a key property.</span></span> <span data-ttu-id="76f78-265">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)ed è sempre impostata su "BIOS".</span><span class="sxs-lookup"><span data-stu-id="76f78-265">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to "BIOS".</span></span>

</dd> <dt>

<span data-ttu-id="76f78-266">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="76f78-266">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-267">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76f78-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-268">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76f78-269">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="76f78-269">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="76f78-270">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="76f78-270">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="76f78-271">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="76f78-271">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="76f78-272">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="76f78-272">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-273">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76f78-273">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="76f78-274">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76f78-275">Matrice che contiene gli stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="76f78-275">An array that contains the current statuses of the object.</span></span> <span data-ttu-id="76f78-276">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="76f78-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span> <span data-ttu-id="76f78-277">Il valore in corrispondenza dell'indice zero (0) corrisponde a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="76f78-277">The value at index zero (0) is one of the following values.</span></span>



| <span data-ttu-id="76f78-278">Valore</span><span class="sxs-lookup"><span data-stu-id="76f78-278">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="76f78-279">Significato</span><span class="sxs-lookup"><span data-stu-id="76f78-279">Meaning</span></span>                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <span data-ttu-id="76f78-280"><dt>**OK**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="76f78-280"><dt>**OK**</dt> <dt>2</dt></span></span> </dl>                                                                                      | <span data-ttu-id="76f78-281">La macchina virtuale è funzionante e funziona normalmente.</span><span class="sxs-lookup"><span data-stu-id="76f78-281">The virtual machine is functional and operating normally.</span></span><br/>                                                                                                                                                                                              |
| <span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span><dl> <span data-ttu-id="76f78-282"><dt></dt> Ridotto <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="76f78-282"><dt>**Degraded**</dt> <dt>3</dt></span></span> </dl>                                         | <span data-ttu-id="76f78-283">La macchina virtuale è solo parzialmente funzionante.</span><span class="sxs-lookup"><span data-stu-id="76f78-283">The virtual machine is only partially functional.</span></span> <span data-ttu-id="76f78-284">Ciò indica che non è possibile accedere alla risorsa di archiviazione che contiene la configurazione.</span><span class="sxs-lookup"><span data-stu-id="76f78-284">This indicates that the storage that contains the configuration is not accessible.</span></span> <span data-ttu-id="76f78-285">Una macchina virtuale in questo stato può essere disattivata o eliminata.</span><span class="sxs-lookup"><span data-stu-id="76f78-285">A virtual machine in this state may only be turned off or deleted.</span></span> <br/>                                               |
| <span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span><dl> <span data-ttu-id="76f78-286"><dt>**Errore predittivo**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="76f78-286"><dt>**Predictive Failure**</dt> <dt>5</dt></span></span> </dl> | <span data-ttu-id="76f78-287">La macchina virtuale è funzionante, ma potrebbe non riuscire in futuro.</span><span class="sxs-lookup"><span data-stu-id="76f78-287">The virtual machine is functional but may fail in the future.</span></span> <span data-ttu-id="76f78-288">Ciò indica che lo spazio disponibile nello spazio di archiviazione che contiene il disco rigido virtuale della macchina virtuale è insufficiente.</span><span class="sxs-lookup"><span data-stu-id="76f78-288">This indicates that the storage that contains the virtual machine's virtual hard disk is low on free space.</span></span> <span data-ttu-id="76f78-289">La macchina virtuale verrà sospesa se non viene reso disponibile più spazio su disco.</span><span class="sxs-lookup"><span data-stu-id="76f78-289">The virtual machine will be paused if more disk space is not made available.</span></span><br/> |
| <span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span><dl> <span data-ttu-id="76f78-290"><dt>**Arrestato**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="76f78-290"><dt>**Stopped**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="76f78-291">Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="76f78-291">This value is not supported.</span></span> <span data-ttu-id="76f78-292">Se la macchina virtuale viene arrestata, il valore della proprietà **EnabledState** sarà 3 (disabilitato).</span><span class="sxs-lookup"><span data-stu-id="76f78-292">If the virtual machine is stopped, the **EnabledState** property will have a value of 3 (Disabled).</span></span><br/>                                                                                                                       |
| <span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span><dl> <span data-ttu-id="76f78-293"><dt>**Nel servizio**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="76f78-293"><dt>**In Service**</dt> <dt>11</dt></span></span> </dl>                                | <span data-ttu-id="76f78-294">La macchina virtuale sta elaborando una richiesta.</span><span class="sxs-lookup"><span data-stu-id="76f78-294">The virtual machine is processing a request.</span></span><br/>                                                                                                                                                                                                           |
| <span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span><dl> <span data-ttu-id="76f78-295"><dt>15</dt> <dt>**inattivo**</dt></span><span class="sxs-lookup"><span data-stu-id="76f78-295"><dt>**Dormant**</dt> <dt>15</dt></span></span> </dl>                                            | <span data-ttu-id="76f78-296">Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="76f78-296">This value is not supported.</span></span> <span data-ttu-id="76f78-297">Se la macchina virtuale viene sospesa o sospesa, la proprietà **EnabledState** avrà il valore 32769 (Suspended) o 32768 (Paused).</span><span class="sxs-lookup"><span data-stu-id="76f78-297">If the virtual machine is suspended or paused, the **EnabledState** property will have a value of 32769 (Suspended) or 32768 (Paused).</span></span><br/>                                                                                    |



 

<span data-ttu-id="76f78-298">Il valore in corrispondenza dell'indice uno (1) è facoltativo e contiene informazioni sullo stato secondario.</span><span class="sxs-lookup"><span data-stu-id="76f78-298">The value at index one (1) is optional and contains secondary status information.</span></span> <span data-ttu-id="76f78-299">Un client deve usare lo stato primario da index zero (0) per determinare se una nuova richiesta può essere rilasciata alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="76f78-299">A client should use the primary status from index zero (0) to determine whether a new request can be issued to the virtual machine.</span></span> <span data-ttu-id="76f78-300">Se **OperationalStatus** \[ 0 \] è 2 (OK), l'operazione indicata da **OperationalStatus** \[ 1 \] può essere interrotta.</span><span class="sxs-lookup"><span data-stu-id="76f78-300">If **OperationalStatus**\[0\] is 2 (OK), then the operation indicated by **OperationalStatus**\[1\] can be interrupted.</span></span>

<span data-ttu-id="76f78-301">Il valore in **OperationalStatus** \[ 1 \] è uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="76f78-301">The value at **OperationalStatus**\[1\] is one of the following values.</span></span>



| <span data-ttu-id="76f78-302">Valore</span><span class="sxs-lookup"><span data-stu-id="76f78-302">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="76f78-303">Significato</span><span class="sxs-lookup"><span data-stu-id="76f78-303">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Creating_Snapshot"></span><span id="creating_snapshot"></span><span id="CREATING_SNAPSHOT"></span><dl> <span data-ttu-id="76f78-304"><dt>**Creazione dello Snapshot**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="76f78-304"><dt>**Creating Snapshot**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="76f78-305">È in corso la creazione di uno snapshot per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="76f78-305">A snapshot is in the process of being created for the virtual machine.</span></span><br/>             |
| <span id="Applying_Snapshot"></span><span id="applying_snapshot"></span><span id="APPLYING_SNAPSHOT"></span><dl> <span data-ttu-id="76f78-306"><dt>**Applicazione dello Snapshot**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="76f78-306"><dt>**Applying Snapshot**</dt> <dt>32769</dt></span></span> </dl>                                 | <span data-ttu-id="76f78-307">È in corso l'applicazione di uno snapshot alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="76f78-307">A snapshot is in the process of being applied to the virtual machine.</span></span><br/>              |
| <span id="Deleting_Snapshot"></span><span id="deleting_snapshot"></span><span id="DELETING_SNAPSHOT"></span><dl> <span data-ttu-id="76f78-308"><dt>**Eliminazione dello Snapshot**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="76f78-308"><dt>**Deleting Snapshot**</dt> <dt>32770</dt></span></span> </dl>                                 | <span data-ttu-id="76f78-309">È in corso l'eliminazione di uno snapshot dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="76f78-309">A snapshot is in the process of being deleted from the virtual machine.</span></span><br/>            |
| <span id="Waiting_to_Start"></span><span id="waiting_to_start"></span><span id="WAITING_TO_START"></span><dl> <span data-ttu-id="76f78-310"><dt>**In attesa dell'avvio**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="76f78-310"><dt>**Waiting to Start**</dt> <dt>32771</dt></span></span> </dl>                                     | <span data-ttu-id="76f78-311">La macchina virtuale verrà avviata dopo che è trascorso il ritardo di avvio automatico.</span><span class="sxs-lookup"><span data-stu-id="76f78-311">The virtual machine will be started after the automatic startup delay has elapsed.</span></span><br/> |
| <span id="Merging_Disks"></span><span id="merging_disks"></span><span id="MERGING_DISKS"></span><dl> <span data-ttu-id="76f78-312"><dt>**Unione di dischi**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="76f78-312"><dt>**Merging Disks**</dt> <dt>32772</dt></span></span> </dl>                                                 | <span data-ttu-id="76f78-313">I dischi rigidi virtuali degli snapshot eliminati in precedenza vengono uniti.</span><span class="sxs-lookup"><span data-stu-id="76f78-313">Virtual hard disks from previously deleted snapshots are being merged.</span></span><br/>             |
| <span id="Exporting_Virtual_Machine"></span><span id="exporting_virtual_machine"></span><span id="EXPORTING_VIRTUAL_MACHINE"></span><dl> <span data-ttu-id="76f78-314"><dt>**Esportazione della macchina virtuale**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="76f78-314"><dt>**Exporting Virtual Machine**</dt> <dt>32773</dt></span></span> </dl> | <span data-ttu-id="76f78-315">È in corso l'esportazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="76f78-315">The virtual machine is being exported.</span></span><br/>                                             |
| <span id="Migrating_Virtual_Machine"></span><span id="migrating_virtual_machine"></span><span id="MIGRATING_VIRTUAL_MACHINE"></span><dl> <span data-ttu-id="76f78-316"><dt>**Migrazione della macchina virtuale**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="76f78-316"><dt>**Migrating Virtual Machine**</dt> <dt>32774</dt></span></span> </dl> | <span data-ttu-id="76f78-317">È in corso la migrazione della macchina virtuale da un computer fisico a un altro.</span><span class="sxs-lookup"><span data-stu-id="76f78-317">The virtual machine is being migrated live from one physical computer to another.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="76f78-318">**OtherTargetOS**</span><span class="sxs-lookup"><span data-stu-id="76f78-318">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-319">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="76f78-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-320">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76f78-321">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="76f78-321">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="76f78-322">Il produttore e il sistema operativo per un elemento software quando la proprietà **TargetOperatingSystem** ha un valore 1 (other), che richiede che la proprietà **OtherTargetOS** disponga di un valore non **null** .</span><span class="sxs-lookup"><span data-stu-id="76f78-322">The manufacturer and operating system for a software element when the **TargetOperatingSystem** property has a value of 1 (Other), which requires the **OtherTargetOS** property to have a non-**Null** value.</span></span> <span data-ttu-id="76f78-323">Per tutti gli altri valori di **TargetOperatingSystem**, la proprietà **OtherTargetOS** deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="76f78-323">For all other values of **TargetOperatingSystem**, the **OtherTargetOS** property must be **Null**.</span></span> <span data-ttu-id="76f78-324">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="76f78-324">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="76f78-325">**PrimaryBIOS**</span><span class="sxs-lookup"><span data-stu-id="76f78-325">**PrimaryBIOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-326">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="76f78-326">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-327">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-327">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76f78-328">Se true, si tratta del BIOS principale del computer.</span><span class="sxs-lookup"><span data-stu-id="76f78-328">If True, this is the primary BIOS of the computer system.</span></span> <span data-ttu-id="76f78-329">Questa proprietà viene ereditata da [**CIM \_ bioselement**](/windows/desktop/CIMWin32Prov/cim-bioselement)ed è sempre impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="76f78-329">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="76f78-330">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="76f78-330">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-331">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76f78-331">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-332">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-332">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76f78-333">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="76f78-333">Provides high level status information.</span></span> <span data-ttu-id="76f78-334">Questa proprietà deve essere utilizzata insieme alla proprietà **DetailedStatus** per fornire informazioni dettagliate sullo stato di integrità per l'elemento e i relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="76f78-334">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="76f78-335">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="76f78-335">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="76f78-336">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="76f78-336">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="76f78-337">**RegistryURIs**</span><span class="sxs-lookup"><span data-stu-id="76f78-337">**RegistryURIs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-338">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="76f78-338">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="76f78-339">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-339">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76f78-340">Matrice di stringhe che rappresenta il percorso di pubblicazione del registro attributi BIOS o dei registri a cui è conforme l'implementazione.</span><span class="sxs-lookup"><span data-stu-id="76f78-340">An array of strings representing the publication location of the BIOS attribute registry or registries the implementation complies to.</span></span> <span data-ttu-id="76f78-341">Questa proprietà viene ereditata da [**CIM \_ bioselement**](/windows/desktop/CIMWin32Prov/cim-bioselement).</span><span class="sxs-lookup"><span data-stu-id="76f78-341">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement).</span></span>

</dd> <dt>

<span data-ttu-id="76f78-342">**ReleaseDate**</span><span class="sxs-lookup"><span data-stu-id="76f78-342">**ReleaseDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-343">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="76f78-343">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-344">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76f78-345">Data di rilascio del BIOS.</span><span class="sxs-lookup"><span data-stu-id="76f78-345">The date that the BIOS was released.</span></span> <span data-ttu-id="76f78-346">Questa proprietà viene ereditata da [**CIM \_ bioselement**](/windows/desktop/CIMWin32Prov/cim-bioselement).</span><span class="sxs-lookup"><span data-stu-id="76f78-346">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement).</span></span>

</dd> <dt>

<span data-ttu-id="76f78-347">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="76f78-347">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-348">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="76f78-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-349">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-349">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76f78-350">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="76f78-350">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="76f78-351">Il numero di serie assegnato del BIOS.</span><span class="sxs-lookup"><span data-stu-id="76f78-351">The assigned serial number of the BIOS.</span></span> <span data-ttu-id="76f78-352">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement).</span><span class="sxs-lookup"><span data-stu-id="76f78-352">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement).</span></span>

</dd> <dt>

<span data-ttu-id="76f78-353">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="76f78-353">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-354">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="76f78-354">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-355">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-355">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76f78-356">Qualificatori: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="76f78-356">Qualifiers: **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="76f78-357">Identificatore per l'elemento software.</span><span class="sxs-lookup"><span data-stu-id="76f78-357">An identifier for the software element.</span></span> <span data-ttu-id="76f78-358">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)ed è sempre impostata su "Microsoft:*GUID* \\ *dati specifici del dispositivo*".</span><span class="sxs-lookup"><span data-stu-id="76f78-358">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to "Microsoft:*GUID*\\*device-specific data*".</span></span>

</dd> <dt>

<span data-ttu-id="76f78-359">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="76f78-359">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-360">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76f78-360">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-361">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76f78-362">Stato del ciclo di vita di un elemento software.</span><span class="sxs-lookup"><span data-stu-id="76f78-362">The state of a software element's life cycle.</span></span> <span data-ttu-id="76f78-363">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)ed è sempre impostata su 2 (eseguibile).</span><span class="sxs-lookup"><span data-stu-id="76f78-363">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to 2 (Executable).</span></span>

</dd> <dt>

<span data-ttu-id="76f78-364">**Status**</span><span class="sxs-lookup"><span data-stu-id="76f78-364">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-365">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="76f78-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-366">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76f78-367">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="76f78-367">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="76f78-368">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="76f78-368">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-369">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="76f78-369">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="76f78-370">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76f78-371">Qualificatori: **arrayType** ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="76f78-371">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="76f78-372">Matrice contenente stringhe che descrivono i valori corrispondenti della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="76f78-372">An array that contains strings that describe the corresponding **OperationalStatus** array values.</span></span> <span data-ttu-id="76f78-373">Se ad esempio 11 (in servizio) è il valore assegnato a **OperationalStatus** \[ 0 \] , **StatusDescriptions** \[ 0 \] può contenere una spiegazione del motivo per cui la macchina virtuale sta elaborando una richiesta.</span><span class="sxs-lookup"><span data-stu-id="76f78-373">For example, if 11 (In Service) is the value assigned to **OperationalStatus**\[0\], then **StatusDescriptions**\[0\] may contain an explanation as to why the virtual machine is processing a request.</span></span> <span data-ttu-id="76f78-374">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="76f78-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="76f78-375">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="76f78-375">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-376">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="76f78-376">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-377">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="76f78-378">Ambiente del sistema operativo dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="76f78-378">The element's operating system environment.</span></span> <span data-ttu-id="76f78-379">Questa proprietà viene ereditata da [**CIM \_ SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement)ed è sempre impostata su 0 (Unknown).</span><span class="sxs-lookup"><span data-stu-id="76f78-379">This property is inherited from [**CIM\_SoftwareElement**](/windows/desktop/CIMWin32Prov/cim-softwareelement), and it is always set to 0 (Unknown).</span></span>

</dd> <dt>

<span data-ttu-id="76f78-380">**Versione**</span><span class="sxs-lookup"><span data-stu-id="76f78-380">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76f78-381">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="76f78-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="76f78-382">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76f78-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76f78-383">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="76f78-383">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="76f78-384">Versione del BIOS.</span><span class="sxs-lookup"><span data-stu-id="76f78-384">The version of the BIOS.</span></span> <span data-ttu-id="76f78-385">Questa proprietà viene ereditata da [**CIM \_ bioselement**](/windows/desktop/CIMWin32Prov/cim-bioselement)ed è sempre impostata su "8.02.00".</span><span class="sxs-lookup"><span data-stu-id="76f78-385">This property is inherited from [**CIM\_BIOSElement**](/windows/desktop/CIMWin32Prov/cim-bioselement), and it is always set to "8.02.00".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="76f78-386">Commenti</span><span class="sxs-lookup"><span data-stu-id="76f78-386">Remarks</span></span>

<span data-ttu-id="76f78-387">L'accesso alla classe **MSVM \_ bioselement** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="76f78-387">Access to the **Msvm\_BIOSElement** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="76f78-388">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="76f78-388">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="76f78-389">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76f78-389">Requirements</span></span>



| <span data-ttu-id="76f78-390">Requisito</span><span class="sxs-lookup"><span data-stu-id="76f78-390">Requirement</span></span> | <span data-ttu-id="76f78-391">Valore</span><span class="sxs-lookup"><span data-stu-id="76f78-391">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76f78-392">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76f78-392">Minimum supported client</span></span><br/> | <span data-ttu-id="76f78-393">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="76f78-393">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="76f78-394">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76f78-394">Minimum supported server</span></span><br/> | <span data-ttu-id="76f78-395">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="76f78-395">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="76f78-396">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="76f78-396">Namespace</span></span><br/>                | <span data-ttu-id="76f78-397">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="76f78-397">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="76f78-398">MOF</span><span class="sxs-lookup"><span data-stu-id="76f78-398">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76f78-399"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="76f78-399"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="76f78-400">DLL</span><span class="sxs-lookup"><span data-stu-id="76f78-400">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76f78-401"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="76f78-401"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="76f78-402">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76f78-402">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76f78-403">**CIM \_ bioselement**</span><span class="sxs-lookup"><span data-stu-id="76f78-403">**CIM\_BIOSElement**</span></span>](cim-bioselement.md)
</dt> <dt>

[<span data-ttu-id="76f78-404">Classi BIOS</span><span class="sxs-lookup"><span data-stu-id="76f78-404">BIOS Classes</span></span>](bios-classes.md)
</dt> <dt>

[<span data-ttu-id="76f78-405">**CIM \_ bioselement**</span><span class="sxs-lookup"><span data-stu-id="76f78-405">**CIM\_BIOSElement**</span></span>](/windows/desktop/CIMWin32Prov/cim-bioselement)
</dt> </dl>

 


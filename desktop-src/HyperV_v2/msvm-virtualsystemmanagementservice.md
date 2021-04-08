---
description: Rappresenta il servizio di virtualizzazione presente in un singolo sistema host.
ms.assetid: 7f4bd9e0-b034-4882-ad01-f7df740939ae
title: Classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService
- Msvm_VirtualSystemManagementService.InstanceID
- Msvm_VirtualSystemManagementService.Caption
- Msvm_VirtualSystemManagementService.Description
- Msvm_VirtualSystemManagementService.ElementName
- Msvm_VirtualSystemManagementService.InstallDate
- Msvm_VirtualSystemManagementService.Name
- Msvm_VirtualSystemManagementService.OperationalStatus
- Msvm_VirtualSystemManagementService.StatusDescriptions
- Msvm_VirtualSystemManagementService.Status
- Msvm_VirtualSystemManagementService.HealthState
- Msvm_VirtualSystemManagementService.CommunicationStatus
- Msvm_VirtualSystemManagementService.DetailedStatus
- Msvm_VirtualSystemManagementService.OperatingStatus
- Msvm_VirtualSystemManagementService.PrimaryStatus
- Msvm_VirtualSystemManagementService.EnabledState
- Msvm_VirtualSystemManagementService.OtherEnabledState
- Msvm_VirtualSystemManagementService.RequestedState
- Msvm_VirtualSystemManagementService.EnabledDefault
- Msvm_VirtualSystemManagementService.TimeOfLastStateChange
- Msvm_VirtualSystemManagementService.AvailableRequestedStates
- Msvm_VirtualSystemManagementService.TransitioningToState
- Msvm_VirtualSystemManagementService.SystemCreationClassName
- Msvm_VirtualSystemManagementService.SystemName
- Msvm_VirtualSystemManagementService.CreationClassName
- Msvm_VirtualSystemManagementService.PrimaryOwnerName
- Msvm_VirtualSystemManagementService.PrimaryOwnerContact
- Msvm_VirtualSystemManagementService.StartMode
- Msvm_VirtualSystemManagementService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7ee79b9690f1eacdf7dc57a2ebfc2133091a1d55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750170"
---
# <a name="msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="dd555-103">\_Classe MSVM VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="dd555-103">Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="dd555-104">Rappresenta il servizio di virtualizzazione presente in un singolo sistema host.</span><span class="sxs-lookup"><span data-stu-id="dd555-104">Represents the virtualization service present on a single host system.</span></span> <span data-ttu-id="dd555-105">**MSVM \_ VirtualSystemManagementService** viene usato per controllare la definizione, la modifica e l'eliminazione delle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="dd555-105">**Msvm\_VirtualSystemManagementService** is used to control the definition, modification, and deletion of virtual machines.</span></span> <span data-ttu-id="dd555-106">Dispone inoltre di metodi per l'esecuzione di operazioni sulle macchine virtuali, ad esempio la clonazione, istantanee, e l'importazione o l'esportazione di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="dd555-106">It also has methods for performing operations on virtual machines, such as cloning, snapshotting, and the importing or exporting of virtual machines.</span></span> <span data-ttu-id="dd555-107">Per recuperare le informazioni per macchina virtuale, usare [**MSVM \_ ComputerSystem**](msvm-computersystem.md).</span><span class="sxs-lookup"><span data-stu-id="dd555-107">To retrieve per-virtual machine information, use [**Msvm\_ComputerSystem**](msvm-computersystem.md).</span></span>

<span data-ttu-id="dd555-108">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="dd555-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd555-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dd555-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemManagementService : CIM_VirtualSystemManagementService
{
  string   InstanceID;
  string   Caption = "Virtual System Management Service";
  string   Description = "Service for creating, manipulating, and managing virtual machines";
  string   ElementName = "Hyper-V Virtual System Management Service";
  datetime InstallDate;
  string   Name = "vmms";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The service is running normally" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_VirtualSystemManagementService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a><span data-ttu-id="dd555-110">Members</span><span class="sxs-lookup"><span data-stu-id="dd555-110">Members</span></span>

<span data-ttu-id="dd555-111">La **classe \_ VirtualSystemManagementService di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="dd555-111">The **Msvm\_VirtualSystemManagementService** class has these types of members:</span></span>

-   [<span data-ttu-id="dd555-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="dd555-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="dd555-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dd555-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="dd555-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="dd555-114">Methods</span></span>

<span data-ttu-id="dd555-115">La **classe \_ VirtualSystemManagementService di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="dd555-115">The **Msvm\_VirtualSystemManagementService** class has these methods.</span></span>



| <span data-ttu-id="dd555-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="dd555-116">Method</span></span>                                                                                                                 | <span data-ttu-id="dd555-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd555-117">Description</span></span>                                                                                                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd555-118">**AddBootSourceSettings**</span><span class="sxs-lookup"><span data-stu-id="dd555-118">**AddBootSourceSettings**</span></span>](msvm-virtualsystemmanagementservice-addbootsourcesettings.md)                             | <span data-ttu-id="dd555-119">Aggiunge origini di avvio a una configurazione di sistema virtuale quando viene applicata a una configurazione di sistema virtuale "stato".</span><span class="sxs-lookup"><span data-stu-id="dd555-119">Adds boot sources to a virtual system configuration when applied to a "state" virtual system configuration.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="dd555-120">**AddFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="dd555-120">**AddFeatureSettings**</span></span>](addfeaturesettings-msvm-virtualsystemmanagementservice.md)                                   | <span data-ttu-id="dd555-121">Aggiunge le impostazioni delle funzionalità Ethernet alla configurazione di una connessione Ethernet della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dd555-121">Adds Ethernet feature settings to the configuration of a virtual machine Ethernet connection.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="dd555-122">**AddFibreChannelChap**</span><span class="sxs-lookup"><span data-stu-id="dd555-122">**AddFibreChannelChap**</span></span>](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)                                 | <span data-ttu-id="dd555-123">Aggiunge i parametri DH-CHAP a una porta Fibre Channel sintetica in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dd555-123">Adds DH-CHAP parameters to a synthetic Fibre Channel port in a virtual machine.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="dd555-124">**AddGuestServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="dd555-124">**AddGuestServiceSettings**</span></span>](msvm-virtualsystemmanagementservice-addguestservicesettings.md)                         | <span data-ttu-id="dd555-125">Aggiunge le impostazioni del servizio Guest a una configurazione di sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="dd555-125">Adds guest service settings to a virtual system configuration.</span></span><br/> <span data-ttu-id="dd555-126">Quando applicato alle parti di una configurazione di sistema virtuale "corrente", è possibile che vengano modificati i servizi guest di un effetto collaterale del sistema virtuale attivo.</span><span class="sxs-lookup"><span data-stu-id="dd555-126">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span><br/>              |
| [<span data-ttu-id="dd555-127">**AddKvpItems**</span><span class="sxs-lookup"><span data-stu-id="dd555-127">**AddKvpItems**</span></span>](addkvpitems-msvm-virtualsystemmanagementservice.md)                                                 | <span data-ttu-id="dd555-128">Aggiunge coppie chiave-valore a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dd555-128">Adds key-value pairs to a virtual machine.</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="dd555-129">**AddResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="dd555-129">**AddResourceSettings**</span></span>](addresourcesettings-msvm-virtualsystemmanagementservice.md)                                 | <span data-ttu-id="dd555-130">Aggiunge risorse a una configurazione di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dd555-130">Adds resources to a virtual machine configuration.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="dd555-131">**AddSystemComponentSettings**</span><span class="sxs-lookup"><span data-stu-id="dd555-131">**AddSystemComponentSettings**</span></span>](msvm-virtualsystemmanagementservice-addsystemcomponentsettings.md)                   | <span data-ttu-id="dd555-132">Aggiunge impostazioni generiche a una configurazione di sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="dd555-132">Adds generic settings to a virtual system configuration.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="dd555-133">**DefinePlannedSystem**</span><span class="sxs-lookup"><span data-stu-id="dd555-133">**DefinePlannedSystem**</span></span>](msvm-virtualsystemmanagementservice-defineplannedsystem.md)                                 | <span data-ttu-id="dd555-134">Definisce un sistema virtuale pianificato.</span><span class="sxs-lookup"><span data-stu-id="dd555-134">Defines a planned virtual system.</span></span><br/> <span data-ttu-id="dd555-135">L'input non completamente specificato può essere compilato con i valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="dd555-135">Input that is not completely specified may be filled out with default values.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="dd555-136">**DefineSystem**</span><span class="sxs-lookup"><span data-stu-id="dd555-136">**DefineSystem**</span></span>](definesystem-msvm-virtualsystemmanagementservice.md)                                               | <span data-ttu-id="dd555-137">Crea una nuova definizione di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dd555-137">Creates a new virtual machine definition.</span></span><br/>                                                                                                                                                                                               |
| [<span data-ttu-id="dd555-138">**DestroySystem**</span><span class="sxs-lookup"><span data-stu-id="dd555-138">**DestroySystem**</span></span>](destroysystem-msvm-virtualsystemmanagementservice.md)                                             | <span data-ttu-id="dd555-139">Elimina una definizione di macchina virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="dd555-139">Deletes an existing virtual machine definition.</span></span><br/>                                                                                                                                                                                         |
| [<span data-ttu-id="dd555-140">**DiagnoseNetworkConnection**</span><span class="sxs-lookup"><span data-stu-id="dd555-140">**DiagnoseNetworkConnection**</span></span>](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md)                     | <span data-ttu-id="dd555-141">Diagnostica la connettività di rete di una macchina virtuale in un ambiente di virtualizzazione rete Windows.</span><span class="sxs-lookup"><span data-stu-id="dd555-141">Diagnoses the network connectivity of a VM in a Windows Network Virtualization Environment.</span></span><br/>                                                                                                                                             |
| [<span data-ttu-id="dd555-142">**ExportSystemDefinition**</span><span class="sxs-lookup"><span data-stu-id="dd555-142">**ExportSystemDefinition**</span></span>](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="dd555-143">Esporta in un file una macchina virtuale o uno snapshot di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dd555-143">Exports a virtual machine, or a snapshot of a virtual machine, to a file.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="dd555-144">**FormatError**</span><span class="sxs-lookup"><span data-stu-id="dd555-144">**FormatError**</span></span>](formaterror-msvm-virtualsystemmanagementservice.md)                                                 | <span data-ttu-id="dd555-145">Restituisce una stringa del messaggio di errore formattato per la matrice specificata di istanze di [**\_ errore MSVM**](msvm-error.md) incorporate.</span><span class="sxs-lookup"><span data-stu-id="dd555-145">Returns a formatted error message string for the specified array of embedded [**Msvm\_Error**](msvm-error.md) instances.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="dd555-146">**GenerateWwpn**</span><span class="sxs-lookup"><span data-stu-id="dd555-146">**GenerateWwpn**</span></span>](generatewwpn-msvm-virtualsystemmanagementservice.md)                                               | <span data-ttu-id="dd555-147">Genera un set di nomi di porta universali (WWPNs).</span><span class="sxs-lookup"><span data-stu-id="dd555-147">Generates a set of World Wide Port Names (WWPNs).</span></span><br/>                                                                                                                                                                                       |
| [<span data-ttu-id="dd555-148">**GetCurrentWwpnFromGenerator**</span><span class="sxs-lookup"><span data-stu-id="dd555-148">**GetCurrentWwpnFromGenerator**</span></span>](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)                 | <span data-ttu-id="dd555-149">Offre la possibilità di visualizzare in anteprima il nome della porta universale (WWPN) corrente senza il WWPN riservato.</span><span class="sxs-lookup"><span data-stu-id="dd555-149">Provides the ability to preview the current World Wide Port Name (WWPN) without the WWPN being reserved.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="dd555-150">**GetDefinitionFileSummaryInformation**</span><span class="sxs-lookup"><span data-stu-id="dd555-150">**GetDefinitionFileSummaryInformation**</span></span>](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) | <span data-ttu-id="dd555-151">Restituisce le informazioni di riepilogo della macchina virtuale per i file di definizione della macchina virtuale specificati.</span><span class="sxs-lookup"><span data-stu-id="dd555-151">Returns virtual machine summary information for the specified virtual machine definition files.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="dd555-152">**GetSizeOfSystemFiles**</span><span class="sxs-lookup"><span data-stu-id="dd555-152">**GetSizeOfSystemFiles**</span></span>](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)                               | <span data-ttu-id="dd555-153">Recupera le dimensioni totali dei file di sistema della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dd555-153">Retrieves the total size of the system files of virtual machine.</span></span><br/>                                                                                                                                                                        |
| [<span data-ttu-id="dd555-154">**GetSummaryInformation**</span><span class="sxs-lookup"><span data-stu-id="dd555-154">**GetSummaryInformation**</span></span>](getsummaryinformation-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="dd555-155">Restituisce informazioni di riepilogo sulla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dd555-155">Returns virtual machine summary information.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="dd555-156">**GetVirtualSystemThumbnailImage**</span><span class="sxs-lookup"><span data-stu-id="dd555-156">**GetVirtualSystemThumbnailImage**</span></span>](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)           | <span data-ttu-id="dd555-157">Recupera un'immagine di anteprima di una macchina virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="dd555-157">Retrieves a thumbnail image of an existing virtual machine.</span></span><br/>                                                                                                                                                                             |
| [<span data-ttu-id="dd555-158">**ImportSnapshotDefinitions**</span><span class="sxs-lookup"><span data-stu-id="dd555-158">**ImportSnapshotDefinitions**</span></span>](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)                     | <span data-ttu-id="dd555-159">Cerca nella cartella specificata tutti i file di definizione dello snapshot associati al sistema del computer pianificato specificato e crea un nuovo snapshot nel sistema del computer pianificato per ogni file di definizione associato in questo percorso.</span><span class="sxs-lookup"><span data-stu-id="dd555-159">Searches the specified folder for any snapshot definition files associated with the specified planned computer system, and creates a new snapshot on the planned computer system for every associated definition file in this location.</span></span><br/> |
| [<span data-ttu-id="dd555-160">**ImportSystemDefinition**</span><span class="sxs-lookup"><span data-stu-id="dd555-160">**ImportSystemDefinition**</span></span>](importsystemdefinition-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="dd555-161">Crea un nuovo sistema di computer pianificato in base alla definizione della macchina virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="dd555-161">Creates a new planned computer system based on the specified virtual machine definition.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="dd555-162">**ModifyDiskMergeSettings**</span><span class="sxs-lookup"><span data-stu-id="dd555-162">**ModifyDiskMergeSettings**</span></span>](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)                         | <span data-ttu-id="dd555-163">Modifica i dati delle impostazioni di merge del disco.</span><span class="sxs-lookup"><span data-stu-id="dd555-163">Modifies the disk merge setting data.</span></span><br/>                                                                                                                                                                                                   |
| [<span data-ttu-id="dd555-164">**ModifyFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="dd555-164">**ModifyFeatureSettings**</span></span>](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="dd555-165">Modifica le impostazioni correnti della funzionalità di una connessione Ethernet della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dd555-165">Modifies the current feature settings of a virtual machine Ethernet connection.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="dd555-166">**ModifyGuestServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="dd555-166">**ModifyGuestServiceSettings**</span></span>](msvm-virtualsystemmanagementservice-modifyguestservicesettings.md)                   | <span data-ttu-id="dd555-167">Modifica le impostazioni del servizio Guest.</span><span class="sxs-lookup"><span data-stu-id="dd555-167">Modifies guest service settings.</span></span><br/> <span data-ttu-id="dd555-168">Quando applicato alle parti di una configurazione di sistema virtuale "corrente", è possibile che vengano modificati i servizi guest di un effetto collaterale del sistema virtuale attivo.</span><span class="sxs-lookup"><span data-stu-id="dd555-168">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span><br/>                                            |
| [<span data-ttu-id="dd555-169">**ModifyKvpItems**</span><span class="sxs-lookup"><span data-stu-id="dd555-169">**ModifyKvpItems**</span></span>](modifykvpitems-msvm-virtualsystemmanagementservice.md)                                           | <span data-ttu-id="dd555-170">Modifica le coppie chiave-valore esistenti in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dd555-170">Modifies existing key-value pairs on a virtual machine.</span></span><br/>                                                                                                                                                                                 |
| [<span data-ttu-id="dd555-171">**ModifyResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="dd555-171">**ModifyResourceSettings**</span></span>](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="dd555-172">Modifica le impostazioni delle risorse virtuali.</span><span class="sxs-lookup"><span data-stu-id="dd555-172">Modifies virtual resource settings.</span></span><br/>                                                                                                                                                                                                     |
| [<span data-ttu-id="dd555-173">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="dd555-173">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="dd555-174">Modifica i dati di impostazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="dd555-174">Modifies the service's setting data.</span></span><br/>                                                                                                                                                                                                    |
| [<span data-ttu-id="dd555-175">**ModifySystemComponentSettings**</span><span class="sxs-lookup"><span data-stu-id="dd555-175">**ModifySystemComponentSettings**</span></span>](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md)             | <span data-ttu-id="dd555-176">Modifica le impostazioni del componente di sistema generico.</span><span class="sxs-lookup"><span data-stu-id="dd555-176">Modifies generic system component settings.</span></span><br/>                                                                                                                                                                                             |
| [<span data-ttu-id="dd555-177">**ModifySystemSettings**</span><span class="sxs-lookup"><span data-stu-id="dd555-177">**ModifySystemSettings**</span></span>](modifysystemsettings-msvm-virtualsystemmanagementservice.md)                               | <span data-ttu-id="dd555-178">Modifica le impostazioni della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dd555-178">Modifies virtual machine settings.</span></span><br/>                                                                                                                                                                                                      |
| [<span data-ttu-id="dd555-179">**RealizePlannedSystem**</span><span class="sxs-lookup"><span data-stu-id="dd555-179">**RealizePlannedSystem**</span></span>](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)                               | <span data-ttu-id="dd555-180">Convalida la configurazione di una macchina virtuale pianificata e la converte in una macchina virtuale realizzata.</span><span class="sxs-lookup"><span data-stu-id="dd555-180">Validates the configuration of a planned virtual machine and converts it to a realized virtual machine.</span></span><br/>                                                                                                                                 |
| [<span data-ttu-id="dd555-181">**RemoveBootSourceSettings**</span><span class="sxs-lookup"><span data-stu-id="dd555-181">**RemoveBootSourceSettings**</span></span>](msvm-virtualsystemmanagementservice-removebootsourcesettings.md)                       | <span data-ttu-id="dd555-182">Rimuove le impostazioni delle risorse virtuali da una configurazione di sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="dd555-182">Removes virtual resource settings from a virtual system configuration.</span></span><br/> <span data-ttu-id="dd555-183">Quando applicato alle parti di una configurazione di sistema virtuale "corrente", è possibile che vengano rimosse le risorse degli effetti collaterali del sistema virtuale attivo.</span><span class="sxs-lookup"><span data-stu-id="dd555-183">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be removed.</span></span><br/>            |
| [<span data-ttu-id="dd555-184">**RemoveFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="dd555-184">**RemoveFeatureSettings**</span></span>](removefeaturesettings-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="dd555-185">Rimuove le impostazioni della funzionalità da una connessione Ethernet della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dd555-185">Removes feature settings from a virtual machine Ethernet connection.</span></span><br/>                                                                                                                                                                    |
| [<span data-ttu-id="dd555-186">**RemoveFibreChannelChap**</span><span class="sxs-lookup"><span data-stu-id="dd555-186">**RemoveFibreChannelChap**</span></span>](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="dd555-187">Rimuove i parametri DH-CHAP da una porta Fibre Channel sintetica in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dd555-187">Removes DH-CHAP parameters from a synthetic Fibre Channel port in a virtual machine.</span></span><br/>                                                                                                                                                    |
| [<span data-ttu-id="dd555-188">**RemoveGuestServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="dd555-188">**RemoveGuestServiceSettings**</span></span>](msvm-virtualsystemmanagementservice-removeguestservicesettings.md)                   | <span data-ttu-id="dd555-189">Rimuove le impostazioni del servizio Guest da una configurazione di sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="dd555-189">Removes guest service settings from a virtual system configuration.</span></span><br/> <span data-ttu-id="dd555-190">Quando applicato alle parti di una configurazione di sistema virtuale "corrente", è possibile che vengano modificati i servizi guest di un effetto collaterale del sistema virtuale attivo.</span><span class="sxs-lookup"><span data-stu-id="dd555-190">When applied to parts of a "current" virtual system configuration, as a side effect guest services of the active virtual system may be modified.</span></span><br/>         |
| [<span data-ttu-id="dd555-191">**RemoveKvpItems**</span><span class="sxs-lookup"><span data-stu-id="dd555-191">**RemoveKvpItems**</span></span>](removekvpitems-msvm-virtualsystemmanagementservice.md)                                           | <span data-ttu-id="dd555-192">Rimuove le coppie chiave-valore esistenti da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dd555-192">Removes existing key-value pairs from a virtual machine.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="dd555-193">**RemoveResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="dd555-193">**RemoveResourceSettings**</span></span>](removeresourcesettings-msvm-virtualsystemmanagementservice.md)                           | <span data-ttu-id="dd555-194">Rimuove le impostazioni delle risorse virtuali da una configurazione di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dd555-194">Removes virtual resource settings from a virtual machine configuration.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="dd555-195">**RemoveSystemComponentSettings**</span><span class="sxs-lookup"><span data-stu-id="dd555-195">**RemoveSystemComponentSettings**</span></span>](msvm-virtualsystemmanagementservice-removesystemcomponentsettings.md)             | <span data-ttu-id="dd555-196">Rimuove le impostazioni del componente generico da una configurazione di sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="dd555-196">Removes generic component settings from a virtual system configuration.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="dd555-197">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="dd555-197">**RequestStateChange**</span></span>](msvm-virtualsystemmanagementservice-requeststatechange.md)                                   | <span data-ttu-id="dd555-198">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="dd555-198">This method is not supported.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="dd555-199">**SetGuestNetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="dd555-199">**SetGuestNetworkAdapterConfiguration**</span></span>](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md) | <span data-ttu-id="dd555-200">Configura le schede di rete all'interno del sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="dd555-200">Configures the network adapters within the guest operating system.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="dd555-201">**SetInitialMachineConfigurationData**</span><span class="sxs-lookup"><span data-stu-id="dd555-201">**SetInitialMachineConfigurationData**</span></span>](msvm-virtualsystemmanagementservice-setinitialmachineconfigurationdata.md)   | <span data-ttu-id="dd555-202">Imposta i dati di configurazione iniziale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dd555-202">Sets a VM's initial machine configuration data.</span></span><br/>                                                                                                                                                                                         |
| [<span data-ttu-id="dd555-203">**StartService**</span><span class="sxs-lookup"><span data-stu-id="dd555-203">**StartService**</span></span>](msvm-virtualsystemmanagementservice-startservice.md)                                               | <span data-ttu-id="dd555-204">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="dd555-204">This method is not supported.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="dd555-205">**StopService**</span><span class="sxs-lookup"><span data-stu-id="dd555-205">**StopService**</span></span>](msvm-virtualsystemmanagementservice-stopservice.md)                                                 | <span data-ttu-id="dd555-206">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="dd555-206">This method is not supported.</span></span><br/>                                                                                                                                                                                                           |
| [<span data-ttu-id="dd555-207">**TestNetworkConnection**</span><span class="sxs-lookup"><span data-stu-id="dd555-207">**TestNetworkConnection**</span></span>](msvm-virtualsystemmanagementservice-testnetworkconnection.md)                             | <span data-ttu-id="dd555-208">Verifica la connettività di rete di una macchina virtuale in un ambiente di virtualizzazione rete Windows.</span><span class="sxs-lookup"><span data-stu-id="dd555-208">Tests the network connectivity of a VM in a Windows Network Virtualization Environment.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="dd555-209">**UpgradeSystemVersion**</span><span class="sxs-lookup"><span data-stu-id="dd555-209">**UpgradeSystemVersion**</span></span>](msvm-virtualsystemmanagementservice-upgradesystemversion.md)                               | <span data-ttu-id="dd555-210">Aggiorna il sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="dd555-210">Upgrades the virtual system.</span></span><br/> <span data-ttu-id="dd555-211">Quando applicato alle impostazioni di sistema di una configurazione di sistema virtuale "corrente"</span><span class="sxs-lookup"><span data-stu-id="dd555-211">When applied to the system settings of a "current" virtual system configuration</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="dd555-212">**ValidatePlannedSystem**</span><span class="sxs-lookup"><span data-stu-id="dd555-212">**ValidatePlannedSystem**</span></span>](validateplannedsystem-msvm-virtualsystemmanagementservice.md)                             | <span data-ttu-id="dd555-213">Convalida il sistema pianificato specificato.</span><span class="sxs-lookup"><span data-stu-id="dd555-213">Validates the specified planned system.</span></span><br/>                                                                                                                                                                                                 |



 

### <a name="properties"></a><span data-ttu-id="dd555-214">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dd555-214">Properties</span></span>

<span data-ttu-id="dd555-215">La **classe \_ VirtualSystemManagementService di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="dd555-215">The **Msvm\_VirtualSystemManagementService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dd555-216">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="dd555-216">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd555-217">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd555-217">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dd555-218">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd555-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd555-219">Indica i valori possibili per il parametro *RequestedState* del metodo **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="dd555-219">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="dd555-220">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="dd555-220">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="dd555-221">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="dd555-221">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd555-222">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dd555-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd555-223">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd555-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd555-224">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="dd555-224">A short description of the object.</span></span> <span data-ttu-id="dd555-225">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Hyper-V Virtual System Management Service".</span><span class="sxs-lookup"><span data-stu-id="dd555-225">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="dd555-226">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="dd555-226">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd555-227">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd555-227">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd555-228">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd555-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd555-229">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="dd555-229">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="dd555-230">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="dd555-230">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="dd555-231">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dd555-231">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="dd555-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="dd555-232"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-233"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="dd555-233"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-234"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicazione ok** (2)</span><span class="sxs-lookup"><span data-stu-id="dd555-234"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-235"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicazione persa** (3)</span><span class="sxs-lookup"><span data-stu-id="dd555-235"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-236"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Nessun contatto** (4)</span><span class="sxs-lookup"><span data-stu-id="dd555-236"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-237"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="dd555-237"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-238"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="dd555-238"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="dd555-239">)</span><span class="sxs-lookup"><span data-stu-id="dd555-239">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dd555-240">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dd555-240">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd555-241">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dd555-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd555-242">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd555-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd555-243">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="dd555-243">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="dd555-244">Nome della classe o della sottoclasse utilizzata per la creazione di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="dd555-244">The name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="dd555-245">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su "MSVM \_ VirtualSystemManagementService".</span><span class="sxs-lookup"><span data-stu-id="dd555-245">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_VirtualSystemManagementService".</span></span>

</dd> <dt>

<span data-ttu-id="dd555-246">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="dd555-246">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd555-247">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dd555-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd555-248">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd555-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd555-249">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="dd555-249">A description of the object.</span></span> <span data-ttu-id="dd555-250">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Service per la creazione, la manipolazione e la gestione delle macchine virtuali".</span><span class="sxs-lookup"><span data-stu-id="dd555-250">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Service for creating, manipulating, and managing virtual machines".</span></span>

</dd> <dt>

<span data-ttu-id="dd555-251">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="dd555-251">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd555-252">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd555-252">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd555-253">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd555-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd555-254">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="dd555-254">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="dd555-255">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="dd555-255">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="dd555-256">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dd555-256">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="dd555-257"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (0)</span><span class="sxs-lookup"><span data-stu-id="dd555-257"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-258"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Nessuna informazione aggiuntiva** (1)</span><span class="sxs-lookup"><span data-stu-id="dd555-258"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-259"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Sottolineato** (2)</span><span class="sxs-lookup"><span data-stu-id="dd555-259"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-260"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Errore predittivo** (3)</span><span class="sxs-lookup"><span data-stu-id="dd555-260"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-261"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Errore irreversibile** (4)</span><span class="sxs-lookup"><span data-stu-id="dd555-261"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-262"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entità di supporto in errore** (5)</span><span class="sxs-lookup"><span data-stu-id="dd555-262"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-263"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="dd555-263"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-264"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="dd555-264"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="dd555-265">)</span><span class="sxs-lookup"><span data-stu-id="dd555-265">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dd555-266">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="dd555-266">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd555-267">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dd555-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd555-268">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd555-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd555-269">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="dd555-269">A display name for the object.</span></span> <span data-ttu-id="dd555-270">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Hyper-V Virtual System Management Service".</span><span class="sxs-lookup"><span data-stu-id="dd555-270">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual System Management Service".</span></span>

</dd> <dt>

<span data-ttu-id="dd555-271">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="dd555-271">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd555-272">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd555-272">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd555-273">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd555-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd555-274">Configurazione predefinita o di avvio di un amministratore per lo stato abilitato di un elemento.</span><span class="sxs-lookup"><span data-stu-id="dd555-274">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="dd555-275">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 2 (Enabled).</span><span class="sxs-lookup"><span data-stu-id="dd555-275">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="dd555-276">Valore</span><span class="sxs-lookup"><span data-stu-id="dd555-276">Value</span></span>                                                                        | <span data-ttu-id="dd555-277">Significato</span><span class="sxs-lookup"><span data-stu-id="dd555-277">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="dd555-278"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="dd555-278"><dt>2</dt></span></span> </dl> | <span data-ttu-id="dd555-279">Abilitato</span><span class="sxs-lookup"><span data-stu-id="dd555-279">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="dd555-280">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="dd555-280">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd555-281">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd555-281">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd555-282">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd555-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd555-283">Stati abilitati e disabilitati di un elemento.</span><span class="sxs-lookup"><span data-stu-id="dd555-283">The enabled and disabled states of an element.</span></span> <span data-ttu-id="dd555-284">Questa proprietà può anche indicare le transizioni tra questi stati richiesti.</span><span class="sxs-lookup"><span data-stu-id="dd555-284">This property can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="dd555-285">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su 2 (Enabled).</span><span class="sxs-lookup"><span data-stu-id="dd555-285">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>



| <span data-ttu-id="dd555-286">Valore</span><span class="sxs-lookup"><span data-stu-id="dd555-286">Value</span></span>                                                                        | <span data-ttu-id="dd555-287">Significato</span><span class="sxs-lookup"><span data-stu-id="dd555-287">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="dd555-288"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="dd555-288"><dt>2</dt></span></span> </dl> | <span data-ttu-id="dd555-289">Abilitato</span><span class="sxs-lookup"><span data-stu-id="dd555-289">Enabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="dd555-290">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="dd555-290">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd555-291">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd555-291">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd555-292">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd555-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd555-293">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="dd555-293">The current health of the element.</span></span> <span data-ttu-id="dd555-294">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="dd555-294">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="dd555-295">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="dd555-295">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="dd555-296">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5 (OK).</span><span class="sxs-lookup"><span data-stu-id="dd555-296">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="dd555-297">Valore</span><span class="sxs-lookup"><span data-stu-id="dd555-297">Value</span></span>                                                                        | <span data-ttu-id="dd555-298">Significato</span><span class="sxs-lookup"><span data-stu-id="dd555-298">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="dd555-299"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="dd555-299"><dt>5</dt></span></span> </dl> | <span data-ttu-id="dd555-300">Lo stato di integrità è Normal.</span><span class="sxs-lookup"><span data-stu-id="dd555-300">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="dd555-301">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="dd555-301">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd555-302">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dd555-302">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dd555-303">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd555-303">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd555-304">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dd555-304">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="dd555-305">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dd555-305">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="dd555-306">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="dd555-306">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd555-307">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dd555-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd555-308">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd555-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd555-309">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="dd555-309">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="dd555-310">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="dd555-310">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="dd555-311">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dd555-311">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dd555-312">**Nome**</span><span class="sxs-lookup"><span data-stu-id="dd555-312">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd555-313">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dd555-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd555-314">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd555-314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd555-315">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="dd555-315">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="dd555-316">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="dd555-316">The label by which the object is known.</span></span> <span data-ttu-id="dd555-317">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su "VMMS".</span><span class="sxs-lookup"><span data-stu-id="dd555-317">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "vmms".</span></span>

</dd> <dt>

<span data-ttu-id="dd555-318">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="dd555-318">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd555-319">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd555-319">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd555-320">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd555-320">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd555-321">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="dd555-321">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="dd555-322">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="dd555-322">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="dd555-323">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dd555-323">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="dd555-324"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="dd555-324"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-325"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Non disponibile** (1)</span><span class="sxs-lookup"><span data-stu-id="dd555-325"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-326"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Manutenzione** (2)</span><span class="sxs-lookup"><span data-stu-id="dd555-326"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-327"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Avvio** (3)</span><span class="sxs-lookup"><span data-stu-id="dd555-327"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-328"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Arresto** in corso (4)</span><span class="sxs-lookup"><span data-stu-id="dd555-328"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-329"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Arrestato** (5)</span><span class="sxs-lookup"><span data-stu-id="dd555-329"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-330"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Interrotto** (6)</span><span class="sxs-lookup"><span data-stu-id="dd555-330"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-331"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inattivo** (7)</span><span class="sxs-lookup"><span data-stu-id="dd555-331"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-332"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completato** (8)</span><span class="sxs-lookup"><span data-stu-id="dd555-332"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-333"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrazione** (9)</span><span class="sxs-lookup"><span data-stu-id="dd555-333"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-334"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrazione** (10)</span><span class="sxs-lookup"><span data-stu-id="dd555-334"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-335"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migrazione** in corso (11)</span><span class="sxs-lookup"><span data-stu-id="dd555-335"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-336"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Istantanee** (12)</span><span class="sxs-lookup"><span data-stu-id="dd555-336"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-337"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Arresto** in corso (13)</span><span class="sxs-lookup"><span data-stu-id="dd555-337"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-338"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In test** (14)</span><span class="sxs-lookup"><span data-stu-id="dd555-338"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-339"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione** (15)</span><span class="sxs-lookup"><span data-stu-id="dd555-339"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-340"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**Nel servizio** (16)</span><span class="sxs-lookup"><span data-stu-id="dd555-340"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-341"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="dd555-341"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-342"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="dd555-342"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="dd555-343">)</span><span class="sxs-lookup"><span data-stu-id="dd555-343">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dd555-344">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="dd555-344">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd555-345">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd555-345">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="dd555-346">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd555-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd555-347">Stati correnti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="dd555-347">The current statuses of the object.</span></span> <span data-ttu-id="dd555-348">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su 2 (OK).</span><span class="sxs-lookup"><span data-stu-id="dd555-348">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="dd555-349">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="dd555-349">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd555-350">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dd555-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd555-351">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd555-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd555-352">Stringa che descrive lo stato abilitato o disabilitato dell'elemento quando la proprietà **EnabledState** è impostata su 1 ("altro").</span><span class="sxs-lookup"><span data-stu-id="dd555-352">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="dd555-353">Questa proprietà deve essere impostata su **null** quando **EnabledState** è un valore diverso da 1.</span><span class="sxs-lookup"><span data-stu-id="dd555-353">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="dd555-354">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="dd555-354">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="dd555-355">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="dd555-355">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd555-356">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dd555-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd555-357">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd555-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd555-358">Qualificatori: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="dd555-358">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="dd555-359">Tutte le informazioni sul modo in cui è possibile raggiungere il proprietario principale del servizio (ad esempio, numero di telefono, indirizzo di posta elettronica e così via).</span><span class="sxs-lookup"><span data-stu-id="dd555-359">Any information about how the primary owner of the service can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="dd555-360">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="dd555-360">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="dd555-361">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="dd555-361">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd555-362">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dd555-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd555-363">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd555-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd555-364">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="dd555-364">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="dd555-365">Nome del proprietario primario per il servizio, se ne è stato definito uno.</span><span class="sxs-lookup"><span data-stu-id="dd555-365">The name of the primary owner for the service, if one is defined.</span></span> <span data-ttu-id="dd555-366">Il proprietario primario è il contatto iniziale del supporto tecnico per il servizio.</span><span class="sxs-lookup"><span data-stu-id="dd555-366">The primary owner is the initial support contact for the service.</span></span> <span data-ttu-id="dd555-367">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="dd555-367">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="dd555-368">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="dd555-368">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd555-369">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd555-369">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd555-370">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd555-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd555-371">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="dd555-371">Provides high level status information.</span></span> <span data-ttu-id="dd555-372">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="dd555-372">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="dd555-373">Un valore **null** indica che questa proprietà non è implementata.</span><span class="sxs-lookup"><span data-stu-id="dd555-373">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="dd555-374">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="dd555-374">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="dd555-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="dd555-375"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-376"><span id="OK"></span><span id="ok"></span>**OK** (1)</span><span class="sxs-lookup"><span data-stu-id="dd555-376"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-377"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Danneggiato** (2)</span><span class="sxs-lookup"><span data-stu-id="dd555-377"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-378"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Errore** (3)</span><span class="sxs-lookup"><span data-stu-id="dd555-378"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-379"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="dd555-379"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="dd555-380"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Fornitore riservato** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="dd555-380"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="dd555-381">)</span><span class="sxs-lookup"><span data-stu-id="dd555-381">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dd555-382">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="dd555-382">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd555-383">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd555-383">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd555-384">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd555-384">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd555-385">Ultimo stato richiesto o desiderato per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="dd555-385">The last requested or desired state for the element.</span></span> <span data-ttu-id="dd555-386">Lo stato effettivo dell'elemento è rappresentato da **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="dd555-386">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="dd555-387">Questa proprietà viene fornita per confrontare gli ultimi stati richiesti e correnti per un elemento.</span><span class="sxs-lookup"><span data-stu-id="dd555-387">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="dd555-388">Una particolare istanza della classe [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) potrebbe non supportare la proprietà **RequestedState** .</span><span class="sxs-lookup"><span data-stu-id="dd555-388">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="dd555-389">In tal caso, viene utilizzato il valore 12 ("non applicabile").</span><span class="sxs-lookup"><span data-stu-id="dd555-389">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="dd555-390">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElement** ed è sempre impostata su 12 (non applicabile).</span><span class="sxs-lookup"><span data-stu-id="dd555-390">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="dd555-391">Valore</span><span class="sxs-lookup"><span data-stu-id="dd555-391">Value</span></span>                                                                         | <span data-ttu-id="dd555-392">Significato</span><span class="sxs-lookup"><span data-stu-id="dd555-392">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="dd555-393"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="dd555-393"><dt>12</dt></span></span> </dl> | <span data-ttu-id="dd555-394">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="dd555-394">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="dd555-395">**Avviato**</span><span class="sxs-lookup"><span data-stu-id="dd555-395">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd555-396">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="dd555-396">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dd555-397">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd555-397">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd555-398">Indica se il servizio è attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="dd555-398">Indicates whether the service is currently running.</span></span> <span data-ttu-id="dd555-399">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **true**.</span><span class="sxs-lookup"><span data-stu-id="dd555-399">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="dd555-400">**Modalità avvio**</span><span class="sxs-lookup"><span data-stu-id="dd555-400">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd555-401">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dd555-401">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd555-402">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd555-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd555-403">Qualificatori: **maxlen** (10)</span><span class="sxs-lookup"><span data-stu-id="dd555-403">Qualifiers: **MaxLen** ( 10 )</span></span>
</dt> </dl>

<span data-ttu-id="dd555-404">Valore stringa che indica se il servizio viene avviato automaticamente da un sistema, un sistema operativo o viene avviato solo su richiesta.</span><span class="sxs-lookup"><span data-stu-id="dd555-404">A string value that indicates whether the service is automatically started by a system, an operating system, or is started only upon request.</span></span> <span data-ttu-id="dd555-405">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="dd555-405">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="dd555-406">**Status**</span><span class="sxs-lookup"><span data-stu-id="dd555-406">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd555-407">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dd555-407">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd555-408">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd555-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd555-409">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), ma non viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="dd555-409">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="dd555-410">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="dd555-410">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd555-411">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="dd555-411">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dd555-412">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd555-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd555-413">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="dd555-413">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="dd555-414">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su "il servizio è in esecuzione normalmente".</span><span class="sxs-lookup"><span data-stu-id="dd555-414">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "The service is running normally".</span></span>

</dd> <dt>

<span data-ttu-id="dd555-415">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="dd555-415">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd555-416">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dd555-416">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd555-417">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd555-417">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd555-418">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="dd555-418">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="dd555-419">Nome della classe di creazione del sistema di ambito.</span><span class="sxs-lookup"><span data-stu-id="dd555-419">The scoping system's creation class name.</span></span> <span data-ttu-id="dd555-420">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)ed è sempre impostata su "MSVM \_ ComputerSystem".</span><span class="sxs-lookup"><span data-stu-id="dd555-420">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service), and it is always set to "Msvm\_ComputerSystem".</span></span>

</dd> <dt>

<span data-ttu-id="dd555-421">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="dd555-421">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd555-422">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="dd555-422">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd555-423">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd555-423">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd555-424">Qualificatori: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="dd555-424">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="dd555-425">Nome NetBIOS del sistema di hosting del computer.</span><span class="sxs-lookup"><span data-stu-id="dd555-425">The NetBIOS name of the hosting computer system.</span></span> <span data-ttu-id="dd555-426">Questa proprietà viene ereditata [**dal \_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="dd555-426">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="dd555-427">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="dd555-427">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd555-428">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="dd555-428">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="dd555-429">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd555-429">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd555-430">Data o ora dell'Ultima modifica dello stato abilitato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="dd555-430">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="dd555-431">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="dd555-431">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="dd555-432">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="dd555-432">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd555-433">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="dd555-433">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="dd555-434">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd555-434">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd555-435">Indica lo stato di destinazione a cui è in corso la transizione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="dd555-435">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="dd555-436">Questa proprietà viene ereditata da [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="dd555-436">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd555-437">Commenti</span><span class="sxs-lookup"><span data-stu-id="dd555-437">Remarks</span></span>

<span data-ttu-id="dd555-438">L'accesso alla **classe \_ VirtualSystemManagementService di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="dd555-438">Access to the **Msvm\_VirtualSystemManagementService** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="dd555-439">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="dd555-439">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="dd555-440">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd555-440">Requirements</span></span>



| <span data-ttu-id="dd555-441">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd555-441">Requirement</span></span> | <span data-ttu-id="dd555-442">Valore</span><span class="sxs-lookup"><span data-stu-id="dd555-442">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd555-443">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd555-443">Minimum supported client</span></span><br/> | <span data-ttu-id="dd555-444">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="dd555-444">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dd555-445">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd555-445">Minimum supported server</span></span><br/> | <span data-ttu-id="dd555-446">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="dd555-446">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dd555-447">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dd555-447">Namespace</span></span><br/>                | <span data-ttu-id="dd555-448">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="dd555-448">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dd555-449">MOF</span><span class="sxs-lookup"><span data-stu-id="dd555-449">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd555-450"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd555-450"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd555-451">DLL</span><span class="sxs-lookup"><span data-stu-id="dd555-451">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd555-452"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dd555-452"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dd555-453">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dd555-453">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd555-454">**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="dd555-454">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> <dt>

<span data-ttu-id="dd555-455">[**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**](/previous-versions//cc136952(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dd555-455">[**CIM\_VirtualSystemManagementService**](/previous-versions//cc136952(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="dd555-456">[**MSVM \_ VirtualSystemManagementService (V1)**](/previous-versions/windows/desktop/legacy/cc136940(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dd555-456">[**Msvm\_VirtualSystemManagementService (V1)**](/previous-versions/windows/desktop/legacy/cc136940(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="dd555-457">Classi di gestione del sistema virtuale</span><span class="sxs-lookup"><span data-stu-id="dd555-457">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 


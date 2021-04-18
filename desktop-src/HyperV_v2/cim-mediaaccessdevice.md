---
description: Rappresenta un dispositivo che può utilizzare supporti per archiviare e recuperare i dati.
ms.assetid: c63b1731-dbc0-4e5e-acb8-cd91b5569dd2
title: Classe CIM_MediaAccessDevice (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice
- CIM_MediaAccessDevice.Capabilities
- CIM_MediaAccessDevice.CapabilityDescriptions
- CIM_MediaAccessDevice.ErrorMethodology
- CIM_MediaAccessDevice.CompressionMethod
- CIM_MediaAccessDevice.NumberOfMediaSupported
- CIM_MediaAccessDevice.MaxMediaSize
- CIM_MediaAccessDevice.DefaultBlockSize
- CIM_MediaAccessDevice.MaxBlockSize
- CIM_MediaAccessDevice.MinBlockSize
- CIM_MediaAccessDevice.NeedsCleaning
- CIM_MediaAccessDevice.MediaIsLocked
- CIM_MediaAccessDevice.Security
- CIM_MediaAccessDevice.LastCleaned
- CIM_MediaAccessDevice.MaxAccessTime
- CIM_MediaAccessDevice.UncompressedDataRate
- CIM_MediaAccessDevice.LoadTime
- CIM_MediaAccessDevice.UnloadTime
- CIM_MediaAccessDevice.MountCount
- CIM_MediaAccessDevice.TimeOfLastMount
- CIM_MediaAccessDevice.TotalMountTime
- CIM_MediaAccessDevice.UnitsDescription
- CIM_MediaAccessDevice.MaxUnitsBeforeCleaning
- CIM_MediaAccessDevice.UnitsUsed
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 616148f6749f3ec00d019a903e8f9046d3aba602
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320468"
---
# <a name="cim_mediaaccessdevice-class-hyper-v-management"></a><span data-ttu-id="35404-103">Classe CIM_MediaAccessDevice (gestione Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="35404-103">CIM_MediaAccessDevice class (Hyper-V management)</span></span>

<span data-ttu-id="35404-104">Rappresenta un dispositivo che può utilizzare supporti per archiviare e recuperare i dati.</span><span class="sxs-lookup"><span data-stu-id="35404-104">Represents a device that can use media to store and retrieve data.</span></span>

## <a name="syntax"></a><span data-ttu-id="35404-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35404-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageDevices"), AMENDMENT]
class CIM_MediaAccessDevice : CIM_LogicalDevice
{
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   ErrorMethodology;
  string   CompressionMethod;
  uint32   NumberOfMediaSupported;
  uint64   MaxMediaSize;
  uint64   DefaultBlockSize;
  uint64   MaxBlockSize;
  uint64   MinBlockSize;
  boolean  NeedsCleaning;
  boolean  MediaIsLocked;
  uint16   Security;
  datetime LastCleaned;
  uint64   MaxAccessTime;
  uint32   UncompressedDataRate;
  uint64   LoadTime;
  uint64   UnloadTime;
  uint64   MountCount;
  datetime TimeOfLastMount;
  uint64   TotalMountTime;
  string   UnitsDescription;
  uint64   MaxUnitsBeforeCleaning;
  uint64   UnitsUsed;
};
```

## <a name="members"></a><span data-ttu-id="35404-106">Members</span><span class="sxs-lookup"><span data-stu-id="35404-106">Members</span></span>

<span data-ttu-id="35404-107">La classe **CIM \_ MediaAccessDevice** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="35404-107">The **CIM\_MediaAccessDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="35404-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="35404-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="35404-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="35404-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="35404-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="35404-110">Methods</span></span>

<span data-ttu-id="35404-111">La classe **CIM \_ MediaAccessDevice** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="35404-111">The **CIM\_MediaAccessDevice** class has these methods.</span></span>



| <span data-ttu-id="35404-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="35404-112">Method</span></span>                                               | <span data-ttu-id="35404-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35404-113">Description</span></span>                                                            |
|:-----------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="35404-114">**LockMedia**</span><span class="sxs-lookup"><span data-stu-id="35404-114">**LockMedia**</span></span>](cim-mediaaccessdevice-lockmedia.md) | <span data-ttu-id="35404-115">Blocca e sblocca i supporti rimovibili in un dispositivo di accesso multimediale.</span><span class="sxs-lookup"><span data-stu-id="35404-115">Locks and unlocks removable media in a media access device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="35404-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="35404-116">Properties</span></span>

<span data-ttu-id="35404-117">La classe **CIM \_ MediaAccessDevice** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="35404-117">The **CIM\_MediaAccessDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="35404-118">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="35404-118">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35404-119">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35404-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="35404-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35404-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35404-121">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivi di archiviazione DMTF \| 001,9 "," MIF. \|Dispositivi di archiviazione DMTF \| 001,11 "," MIF. \|Dispositivi di archiviazione DMTF \| 001,12 "," MIF. DMTF \| disks \| 003,7 "," MIF. \|Disco host DMTF \| 001,2 "," MIF. \|Disco host DMTF \| 001,4 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="35404-121">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Storage Devices\|001.9", "MIF.DMTF\|Storage Devices\|001.11", "MIF.DMTF\|Storage Devices\|001.12", "MIF.DMTF\|Disks\|003.7", "MIF.DMTF\|Host Disk\|001.2", "MIF.DMTF\|Host Disk\|001.4"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="35404-122">Matrice che contiene le funzionalità del dispositivo di accesso multimediale.</span><span class="sxs-lookup"><span data-stu-id="35404-122">An array that contains the capabilities of the media access device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="35404-123">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="35404-123">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="35404-124">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="35404-124">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequential_Access"></span><span id="sequential_access"></span><span id="SEQUENTIAL_ACCESS"></span>

<span data-ttu-id="35404-125">**Accesso sequenziale** (2)</span><span class="sxs-lookup"><span data-stu-id="35404-125">**Sequential Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Random_Access"></span><span id="random_access"></span><span id="RANDOM_ACCESS"></span>

<span data-ttu-id="35404-126">**Accesso casuale** (3)</span><span class="sxs-lookup"><span data-stu-id="35404-126">**Random Access** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Writing"></span><span id="supports_writing"></span><span id="SUPPORTS_WRITING"></span>

<span data-ttu-id="35404-127">**Supporta la scrittura** (4)</span><span class="sxs-lookup"><span data-stu-id="35404-127">**Supports Writing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Encryption"></span><span id="encryption"></span><span id="ENCRYPTION"></span>

<span data-ttu-id="35404-128">**Crittografia** (5)</span><span class="sxs-lookup"><span data-stu-id="35404-128">**Encryption** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Compression"></span><span id="compression"></span><span id="COMPRESSION"></span>

<span data-ttu-id="35404-129">**Compressione** (6)</span><span class="sxs-lookup"><span data-stu-id="35404-129">**Compression** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Removeable_Media"></span><span id="supports_removeable_media"></span><span id="SUPPORTS_REMOVEABLE_MEDIA"></span>

<span data-ttu-id="35404-130">**Supporta supporti rimuovibili** (7)</span><span class="sxs-lookup"><span data-stu-id="35404-130">**Supports Removeable Media** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Manual_Cleaning"></span><span id="manual_cleaning"></span><span id="MANUAL_CLEANING"></span>

<span data-ttu-id="35404-131">**Pulizia manuale** (8)</span><span class="sxs-lookup"><span data-stu-id="35404-131">**Manual Cleaning** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic_Cleaning"></span><span id="automatic_cleaning"></span><span id="AUTOMATIC_CLEANING"></span>

<span data-ttu-id="35404-132">**Pulizia automatica** (9)</span><span class="sxs-lookup"><span data-stu-id="35404-132">**Automatic Cleaning** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SMART_Notification"></span><span id="smart_notification"></span><span id="SMART_NOTIFICATION"></span>

<span data-ttu-id="35404-133">**Notifica intelligente** (10)</span><span class="sxs-lookup"><span data-stu-id="35404-133">**SMART Notification** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Supports_Dual_Sided_Media"></span><span id="supports_dual_sided_media"></span><span id="SUPPORTS_DUAL_SIDED_MEDIA"></span>

<span data-ttu-id="35404-134">**Supporta supporti a doppio lato** (11)</span><span class="sxs-lookup"><span data-stu-id="35404-134">**Supports Dual Sided Media** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Predismount_Eject_Not_Required"></span><span id="predismount_eject_not_required"></span><span id="PREDISMOUNT_EJECT_NOT_REQUIRED"></span>

<span data-ttu-id="35404-135">**Espulsione Predismount non obbligatoria** (12)</span><span class="sxs-lookup"><span data-stu-id="35404-135">**Predismount Eject Not Required** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="35404-136">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="35404-136">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35404-137">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="35404-137">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="35404-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35404-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35404-139">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**Funzionalità**")</span><span class="sxs-lookup"><span data-stu-id="35404-139">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="35404-140">Matrice di descrizioni delle funzionalità per gli elementi nella matrice di **funzionalità** .</span><span class="sxs-lookup"><span data-stu-id="35404-140">An array of feature descriptions for the items in the **Capabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="35404-141">**CompressionMethod**</span><span class="sxs-lookup"><span data-stu-id="35404-141">**CompressionMethod**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35404-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="35404-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35404-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35404-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35404-144">Nome dell'algoritmo o dello strumento utilizzato dal dispositivo per supportare la compressione.</span><span class="sxs-lookup"><span data-stu-id="35404-144">The name of the algorithm or tool used by the device to support compression.</span></span>

<span data-ttu-id="35404-145">Se non si specifica un tipo di compressione, è possibile usare uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="35404-145">If a compression type is not specified, one of the following values can be used:</span></span>

-   <span data-ttu-id="35404-146">Il supporto per la compressione "Unknown" è sconosciuto o non è specificato.</span><span class="sxs-lookup"><span data-stu-id="35404-146">"Unknown"   compression support is unknown or not specified.</span></span>
-   <span data-ttu-id="35404-147">La compressione "compresso" è supportata, ma il tipo è sconosciuto o non è specificato.</span><span class="sxs-lookup"><span data-stu-id="35404-147">"Compressed"   compression is supported but the type is unknown or unspecified.</span></span>
-   <span data-ttu-id="35404-148">"Non compresso" il dispositivo non supporta le funzionalità di compressione.</span><span class="sxs-lookup"><span data-stu-id="35404-148">"Not Compressed"   the device does not support compression capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="35404-149">**DefaultBlockSize**</span><span class="sxs-lookup"><span data-stu-id="35404-149">**DefaultBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35404-150">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="35404-150">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35404-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35404-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35404-152">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte"), **punito** ("byte")</span><span class="sxs-lookup"><span data-stu-id="35404-152">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="35404-153">Dimensioni del blocco predefinite, in byte, per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="35404-153">The default block size, in bytes, for the device.</span></span>

</dd> <dt>

<span data-ttu-id="35404-154">**ErrorMethodology**</span><span class="sxs-lookup"><span data-stu-id="35404-154">**ErrorMethodology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35404-155">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="35404-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35404-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35404-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35404-157">Tipo di rilevamento e correzione degli errori supportato dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="35404-157">The type of error detection and correction supported by the device.</span></span>

</dd> <dt>

<span data-ttu-id="35404-158">**LastCleaned**</span><span class="sxs-lookup"><span data-stu-id="35404-158">**LastCleaned**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35404-159">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="35404-159">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="35404-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35404-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35404-161">Data e ora dell'ultima pulizia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="35404-161">The date and time when the device was last cleaned.</span></span>

</dd> <dt>

<span data-ttu-id="35404-162">**LoadTime**</span><span class="sxs-lookup"><span data-stu-id="35404-162">**LoadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35404-163">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="35404-163">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35404-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35404-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35404-165">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("millisecondi"), **punito** ("secondo \* 10 ^-3")</span><span class="sxs-lookup"><span data-stu-id="35404-165">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")</span></span>
</dt> </dl>

<span data-ttu-id="35404-166">Tempo necessario, in millisecondi, per consentire al dispositivo di leggere o scrivere un supporto dopo l'avvio del caricamento del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="35404-166">The time it takes, in milliseconds, for the device to be able to read or write a media after the device starts loading.</span></span> <span data-ttu-id="35404-167">Ad esempio, per le unità disco, questo è l'intervallo tra un disco che non viene ruotato sul disco che è pronto per le operazioni di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="35404-167">For example, for disk drives, this is the interval between a disk not spinning to the disk reporting that it is ready for read/write operations.</span></span> <span data-ttu-id="35404-168">Per le unità nastro, questa operazione viene avviata quando si inserisce un supporto e termina quando l'unità segnala che è pronta per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="35404-168">For tape drives, this starts when media is inserted and ends when the drive reports that it is ready for an application.</span></span> <span data-ttu-id="35404-169">Si tratta in genere dell'area di BOT (inizio del nastro) del nastro.</span><span class="sxs-lookup"><span data-stu-id="35404-169">This is usually at the tape's beginning-of-tape (BOT) area.</span></span>

</dd> <dt>

<span data-ttu-id="35404-170">**MaxAccessTime**</span><span class="sxs-lookup"><span data-stu-id="35404-170">**MaxAccessTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35404-171">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="35404-171">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35404-172">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35404-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35404-173">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("millisecondi"), **punito** ("secondo \* 10 ^-3")</span><span class="sxs-lookup"><span data-stu-id="35404-173">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")</span></span>
</dt> </dl>

<span data-ttu-id="35404-174">Tempo di accesso massimo del supporto, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="35404-174">The maximum access time of the media, in milliseconds.</span></span> <span data-ttu-id="35404-175">Per un'unità disco, rappresenta la ricerca completa e il ritardo rotazionale completo.</span><span class="sxs-lookup"><span data-stu-id="35404-175">For a disk drive, this represents full seek and full rotational delay.</span></span> <span data-ttu-id="35404-176">Per le unità nastro, rappresenta una ricerca dall'inizio del nastro al punto più distante fisicamente.</span><span class="sxs-lookup"><span data-stu-id="35404-176">For tape drives, this represents a search from the beginning of the tape to the most physically distant point.</span></span>

</dd> <dt>

<span data-ttu-id="35404-177">**MaxBlockSize**</span><span class="sxs-lookup"><span data-stu-id="35404-177">**MaxBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35404-178">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="35404-178">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35404-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35404-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35404-180">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte"), **punito** ("byte")</span><span class="sxs-lookup"><span data-stu-id="35404-180">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="35404-181">Dimensione massima del blocco, in byte, per i file multimediali accessibili dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="35404-181">The maximum block size, in bytes, for media accessed by the device.</span></span>

</dd> <dt>

<span data-ttu-id="35404-182">**MaxMediaSize**</span><span class="sxs-lookup"><span data-stu-id="35404-182">**MaxMediaSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35404-183">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="35404-183">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35404-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35404-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35404-185">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF i \| dispositivi di accesso sequenziale \| 001,2 "," MIF. \|Disco host DMTF \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="35404-185">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Sequential Access Devices\|001.2", "MIF.DMTF\|Host Disk\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="35404-186">Dimensione massima, in kilobyte, del supporto supportato da questo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="35404-186">The maximum size, in kilobytes, of media supported by this device.</span></span>

</dd> <dt>

<span data-ttu-id="35404-187">**MaxUnitsBeforeCleaning**</span><span class="sxs-lookup"><span data-stu-id="35404-187">**MaxUnitsBeforeCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35404-188">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="35404-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35404-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35404-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35404-190">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**UnitsDescription**")</span><span class="sxs-lookup"><span data-stu-id="35404-190">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**UnitsDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="35404-191">Numero massimo di unità che è possibile utilizzare prima di pulire il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="35404-191">The maximum number of units that can be used before the device should be cleaned.</span></span> <span data-ttu-id="35404-192">**UnitsDescription** definisce il tipo di unità.</span><span class="sxs-lookup"><span data-stu-id="35404-192">**UnitsDescription** defines how the unit type.</span></span>

</dd> <dt>

<span data-ttu-id="35404-193">**MediaIsLocked**</span><span class="sxs-lookup"><span data-stu-id="35404-193">**MediaIsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35404-194">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="35404-194">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="35404-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35404-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35404-196">**true** se il supporto è bloccato nel dispositivo e non può essere espulso; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="35404-196">**true** if the media is locked in the device and can not be ejected; otherwise, **false**.</span></span> <span data-ttu-id="35404-197">Per i dispositivi non rimovibili, questo valore deve essere **true**.</span><span class="sxs-lookup"><span data-stu-id="35404-197">For non-removable devices, this value should be **true**.</span></span>

</dd> <dt>

<span data-ttu-id="35404-198">**MinBlockSize**</span><span class="sxs-lookup"><span data-stu-id="35404-198">**MinBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35404-199">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="35404-199">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35404-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35404-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35404-201">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("byte"), **punito** ("byte")</span><span class="sxs-lookup"><span data-stu-id="35404-201">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="35404-202">Dimensioni minime del blocco, in byte, per i file multimediali accessibili dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="35404-202">The minimum block size, in bytes, for media accessed by the device.</span></span>

</dd> <dt>

<span data-ttu-id="35404-203">**MountCount**</span><span class="sxs-lookup"><span data-stu-id="35404-203">**MountCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35404-204">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="35404-204">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35404-205">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35404-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35404-206">Qualificatori: **contatore**</span><span class="sxs-lookup"><span data-stu-id="35404-206">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="35404-207">Il numero di volte in cui il supporto è stato montato per il trasferimento dei dati o per la pulizia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="35404-207">The number of times that media has been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="35404-208">Se il dispositivo non supporta supporti rimovibili, questa proprietà deve essere impostata su zero.</span><span class="sxs-lookup"><span data-stu-id="35404-208">If the device does not support removable media, this property should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="35404-209">**NeedsCleaning**</span><span class="sxs-lookup"><span data-stu-id="35404-209">**NeedsCleaning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35404-210">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="35404-210">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="35404-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35404-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35404-212">**true** se il dispositivo deve essere pulito. in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="35404-212">**true** if the device needs cleaning; otherwise, **false**.</span></span>

> [!Note]  
> <span data-ttu-id="35404-213">La proprietà **capabilities** indica se è possibile la pulizia manuale o automatica.</span><span class="sxs-lookup"><span data-stu-id="35404-213">The **Capabilities** property indicates whether manual or automatic cleaning is possible.</span></span>

 

</dd> <dt>

<span data-ttu-id="35404-214">**NumberOfMediaSupported**</span><span class="sxs-lookup"><span data-stu-id="35404-214">**NumberOfMediaSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35404-215">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35404-215">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35404-216">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35404-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35404-217">Se il dispositivo supporta più supporti singoli, questa proprietà definisce il numero massimo che può essere supportato o inserito.</span><span class="sxs-lookup"><span data-stu-id="35404-217">If the device supports multiple individual media, this property defines the maximum number which can be supported or inserted.</span></span>

</dd> <dt>

<span data-ttu-id="35404-218">**Sicurezza**</span><span class="sxs-lookup"><span data-stu-id="35404-218">**Security**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35404-219">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="35404-219">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="35404-220">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35404-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35404-221">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dischi DMTF \| 003,22 ")</span><span class="sxs-lookup"><span data-stu-id="35404-221">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Disks\|003.22")</span></span>
</dt> </dl>

<span data-ttu-id="35404-222">Sicurezza operativa del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="35404-222">The operational security for the device.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="35404-223">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="35404-223">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="35404-224">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="35404-224">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="35404-225">**Nessuno** (3)</span><span class="sxs-lookup"><span data-stu-id="35404-225">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Only"></span><span id="read_only"></span><span id="READ_ONLY"></span>

<span data-ttu-id="35404-226">**Sola lettura** (4)</span><span class="sxs-lookup"><span data-stu-id="35404-226">**Read Only** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Locked_Out"></span><span id="locked_out"></span><span id="LOCKED_OUT"></span>

<span data-ttu-id="35404-227">**Bloccato** (5)</span><span class="sxs-lookup"><span data-stu-id="35404-227">**Locked Out** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_Bypass"></span><span id="boot_bypass"></span><span id="BOOT_BYPASS"></span>

<span data-ttu-id="35404-228">**Bypass di avvio** (6)</span><span class="sxs-lookup"><span data-stu-id="35404-228">**Boot Bypass** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_Bypass_and_Read_Only"></span><span id="boot_bypass_and_read_only"></span><span id="BOOT_BYPASS_AND_READ_ONLY"></span>

<span data-ttu-id="35404-229">**Bypass di avvio e di sola lettura** (7)</span><span class="sxs-lookup"><span data-stu-id="35404-229">**Boot Bypass and Read Only** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="35404-230">**TimeOfLastMount**</span><span class="sxs-lookup"><span data-stu-id="35404-230">**TimeOfLastMount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35404-231">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="35404-231">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="35404-232">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35404-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35404-233">Data e ora più recenti in cui il supporto è stato montato sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="35404-233">The most recent date and time when media was mounted on the device.</span></span> <span data-ttu-id="35404-234">Questa proprietà viene usata solo dai dispositivi che supportano supporti rimovibili.</span><span class="sxs-lookup"><span data-stu-id="35404-234">This property is only used by devices that support removable media.</span></span>

</dd> <dt>

<span data-ttu-id="35404-235">**TotalMountTime**</span><span class="sxs-lookup"><span data-stu-id="35404-235">**TotalMountTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35404-236">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="35404-236">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35404-237">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35404-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="35404-238">Tempo, in secondi, per cui il supporto è stato montato per il trasferimento dei dati o per la pulizia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="35404-238">The time, in seconds, that media has been mounted for data transfer or to clean the device.</span></span> <span data-ttu-id="35404-239">Se il dispositivo non supporta supporti rimovibili, questa proprietà deve essere impostata su zero.</span><span class="sxs-lookup"><span data-stu-id="35404-239">If the device does not support removable media, this property should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="35404-240">**UncompressedDataRate**</span><span class="sxs-lookup"><span data-stu-id="35404-240">**UncompressedDataRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35404-241">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="35404-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="35404-242">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35404-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35404-243">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("kilobyte al secondo"), **punito** ("byte/secondo \* 10 ^ 3")</span><span class="sxs-lookup"><span data-stu-id="35404-243">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("KiloBytes per Second"), **PUnit** ("byte / second \* 10^3")</span></span>
</dt> </dl>

<span data-ttu-id="35404-244">Velocità di trasferimento dati prolungata, espressa in kilobyte, in cui il dispositivo può leggere e scrivere su un supporto.</span><span class="sxs-lookup"><span data-stu-id="35404-244">The sustained data transfer rate in kilobytes at which the device can read and write to a media.</span></span> <span data-ttu-id="35404-245">Si tratta di una velocità dati continua e non elaborata.</span><span class="sxs-lookup"><span data-stu-id="35404-245">This is a sustained, raw data rate.</span></span> <span data-ttu-id="35404-246">In questa proprietà non devono essere segnalate le tariffe o le tariffe massime con compressione.</span><span class="sxs-lookup"><span data-stu-id="35404-246">Maximum rates or rates with compression should not be reported in this property.</span></span>

</dd> <dt>

<span data-ttu-id="35404-247">**UnitsDescription**</span><span class="sxs-lookup"><span data-stu-id="35404-247">**UnitsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35404-248">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="35404-248">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35404-249">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35404-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35404-250">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MediaAccessDevice**.**MaxUnitsBeforeCleaning**","**CIM \_ MediaAccessDevice**.**UnitsUsed**")</span><span class="sxs-lookup"><span data-stu-id="35404-250">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**MaxUnitsBeforeCleaning**", "**CIM\_MediaAccessDevice**.**UnitsUsed**")</span></span>
</dt> </dl>

<span data-ttu-id="35404-251">Descrive il tipo di unità delle proprietà **MaxUnitsBeforeCleaning** e **UnitsUsed** .</span><span class="sxs-lookup"><span data-stu-id="35404-251">Describes the unit type of the **MaxUnitsBeforeCleaning** and **UnitsUsed** properties.</span></span>

</dd> <dt>

<span data-ttu-id="35404-252">**UnitsUsed**</span><span class="sxs-lookup"><span data-stu-id="35404-252">**UnitsUsed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35404-253">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="35404-253">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35404-254">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35404-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35404-255">Qualificatori: [**misuratore**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM MediaAccessDevice**.**UnitsDescription**","**CIM \_ MediaAccessDevice**.**MaxUnitsBeforeCleaning**")</span><span class="sxs-lookup"><span data-stu-id="35404-255">Qualifiers: [**Gauge**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MediaAccessDevice**.**UnitsDescription**", "**CIM\_MediaAccessDevice**.**MaxUnitsBeforeCleaning**")</span></span>
</dt> </dl>

<span data-ttu-id="35404-256">Il numero di unità usate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="35404-256">The number of units used by the device.</span></span> <span data-ttu-id="35404-257">Questa proprietà viene usata per determinare quando il dispositivo deve essere pulito.</span><span class="sxs-lookup"><span data-stu-id="35404-257">This property is used to determine when the device should be cleaned.</span></span> <span data-ttu-id="35404-258">**UnitsDescription** definisce il tipo di unità.</span><span class="sxs-lookup"><span data-stu-id="35404-258">**UnitsDescription** defines how the unit type.</span></span>

</dd> <dt>

<span data-ttu-id="35404-259">**UnloadTime**</span><span class="sxs-lookup"><span data-stu-id="35404-259">**UnloadTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35404-260">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="35404-260">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="35404-261">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="35404-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35404-262">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("millisecondi"), **punito** ("secondo \* 10 ^-3")</span><span class="sxs-lookup"><span data-stu-id="35404-262">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds"), **PUnit** ("second \* 10^-3")</span></span>
</dt> </dl>

<span data-ttu-id="35404-263">Tempo necessario, in millisecondi, per la transizione del dispositivo alla lettura o alla scrittura di contenuti multimediali da scaricare.</span><span class="sxs-lookup"><span data-stu-id="35404-263">The time it takes, in milliseconds, for the device to transition from reading or writing media to unloading.</span></span> <span data-ttu-id="35404-264">Ad esempio, per le unità disco, questo è l'intervallo tra un disco con velocità nominale e un disco non in rotazione.</span><span class="sxs-lookup"><span data-stu-id="35404-264">For example, for disk drives, this is the interval between a disk spinning at nominal speeds and a disk not spinning.</span></span> <span data-ttu-id="35404-265">Per le unità nastro, questo è il momento in cui un supporto passa dal BOT a essere completamente espulso e accessibile a un elemento di selezione o a un operatore umano.</span><span class="sxs-lookup"><span data-stu-id="35404-265">For tape drives, this is the time for a media to go from its BOT to being fully ejected and accessible to a picker element or human operator.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35404-266">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35404-266">Requirements</span></span>



| <span data-ttu-id="35404-267">Requisito</span><span class="sxs-lookup"><span data-stu-id="35404-267">Requirement</span></span> | <span data-ttu-id="35404-268">Valore</span><span class="sxs-lookup"><span data-stu-id="35404-268">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35404-269">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35404-269">Minimum supported client</span></span><br/> | <span data-ttu-id="35404-270">Windows 8</span><span class="sxs-lookup"><span data-stu-id="35404-270">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="35404-271">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35404-271">Minimum supported server</span></span><br/> | <span data-ttu-id="35404-272">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="35404-272">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="35404-273">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="35404-273">Namespace</span></span><br/>                | <span data-ttu-id="35404-274">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="35404-274">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="35404-275">MOF</span><span class="sxs-lookup"><span data-stu-id="35404-275">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35404-276"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35404-276"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="35404-277">DLL</span><span class="sxs-lookup"><span data-stu-id="35404-277">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35404-278"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="35404-278"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="35404-279">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35404-279">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35404-280">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="35404-280">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 


---
description: Rappresenta le impostazioni per l'allocazione di spazio di archiviazione virtuale.
ms.assetid: 128fd3e9-8759-4b2f-a881-d34e89c539ac
title: Classe CIM_StorageAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageAllocationSettingData
- CIM_StorageAllocationSettingData.VirtualResourceBlockSize
- CIM_StorageAllocationSettingData.VirtualQuantity
- CIM_StorageAllocationSettingData.VirtualQuantityUnits
- CIM_StorageAllocationSettingData.Access
- CIM_StorageAllocationSettingData.HostResourceBlockSize
- CIM_StorageAllocationSettingData.Reservation
- CIM_StorageAllocationSettingData.Limit
- CIM_StorageAllocationSettingData.HostExtentStartingAddress
- CIM_StorageAllocationSettingData.HostExtentName
- CIM_StorageAllocationSettingData.HostExtentNameFormat
- CIM_StorageAllocationSettingData.OtherHostExtentNameFormat
- CIM_StorageAllocationSettingData.HostExtentNameNamespace
- CIM_StorageAllocationSettingData.OtherHostExtentNameNamespace
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e66322f20987e2d1f99042430f0f57cdc2e399d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756620"
---
# <a name="cim_storageallocationsettingdata-class"></a><span data-ttu-id="6a714-103">CIM \_ StorageAllocationSettingData (classe)</span><span class="sxs-lookup"><span data-stu-id="6a714-103">CIM\_StorageAllocationSettingData class</span></span>

<span data-ttu-id="6a714-104">Rappresenta le impostazioni per l'allocazione di spazio di archiviazione virtuale.</span><span class="sxs-lookup"><span data-stu-id="6a714-104">Represents settings for the allocation of virtual storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a714-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a714-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_StorageAllocationSettingData : CIM_ResourceAllocationSettingData
{
  uint64 VirtualResourceBlockSize;
  uint64 VirtualQuantity;
  string VirtualQuantityUnits = "count(fixed size block)";
  uint16 Access;
  uint64 HostResourceBlockSize;
  uint64 Reservation;
  uint64 Limit;
  uint64 HostExtentStartingAddress;
  string HostExtentName;
  uint16 HostExtentNameFormat;
  string OtherHostExtentNameFormat;
  uint16 HostExtentNameNamespace;
  string OtherHostExtentNameNamespace;
};
```

## <a name="members"></a><span data-ttu-id="6a714-106">Members</span><span class="sxs-lookup"><span data-stu-id="6a714-106">Members</span></span>

<span data-ttu-id="6a714-107">La classe **CIM \_ StorageAllocationSettingData** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6a714-107">The **CIM\_StorageAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="6a714-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6a714-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6a714-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6a714-109">Properties</span></span>

<span data-ttu-id="6a714-110">La classe **CIM \_ StorageAllocationSettingData** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6a714-110">The **CIM\_StorageAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6a714-111">**Accesso**</span><span class="sxs-lookup"><span data-stu-id="6a714-111">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a714-112">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6a714-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6a714-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a714-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a714-114">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**Accesso**")</span><span class="sxs-lookup"><span data-stu-id="6a714-114">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_StorageExtent**](cim-storageextent.md).**Access**")</span></span>
</dt> </dl>

<span data-ttu-id="6a714-115">Supporto di lettura/scrittura dell'allocazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6a714-115">The read/write support of the storage allocation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6a714-116">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="6a714-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span data-ttu-id="6a714-117">**Leggibile** (1)</span><span class="sxs-lookup"><span data-stu-id="6a714-117">**Readable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span data-ttu-id="6a714-118">**Scrivibile** (2)</span><span class="sxs-lookup"><span data-stu-id="6a714-118">**Writeable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span data-ttu-id="6a714-119">**Lettura/scrittura supportata** (3)</span><span class="sxs-lookup"><span data-stu-id="6a714-119">**Read/Write Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="6a714-120">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="6a714-120">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6a714-121">**HostExtentName**</span><span class="sxs-lookup"><span data-stu-id="6a714-121">**HostExtentName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a714-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6a714-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a714-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a714-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a714-124">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**","**CIM \_ StorageAllocationSettingData**.**HostExtentNameNamespace**","[**CIM \_ StorageExtent**](cim-storageextent.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="6a714-124">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentNameFormat**", "**CIM\_StorageAllocationSettingData**.**HostExtentNameNamespace**", "[**CIM\_StorageExtent**](cim-storageextent.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="6a714-125">Identificatore univoco dell'extent di archiviazione dell'host.</span><span class="sxs-lookup"><span data-stu-id="6a714-125">A unique identifier of the host storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="6a714-126">**HostExtentNameFormat**</span><span class="sxs-lookup"><span data-stu-id="6a714-126">**HostExtentNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a714-127">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6a714-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6a714-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a714-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a714-129">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentName**","**CIM \_ StorageAllocationSettingData**.**OtherHostExtentNameFormat**","[**CIM \_ StorageExtent**](cim-storageextent.md).**NameFormat**")</span><span class="sxs-lookup"><span data-stu-id="6a714-129">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentName**", "**CIM\_StorageAllocationSettingData**.**OtherHostExtentNameFormat**", "[**CIM\_StorageExtent**](cim-storageextent.md).**NameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="6a714-130">Formato del valore della proprietà **HostExtentName** .</span><span class="sxs-lookup"><span data-stu-id="6a714-130">The format that of the **HostExtentName** property value.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6a714-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="6a714-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6a714-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="6a714-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span data-ttu-id="6a714-133"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span><span class="sxs-lookup"><span data-stu-id="6a714-133"><span id="SNVM"></span><span id="snvm"></span>**SNVM** (7)</span></span>


</dt> <dd>

<span data-ttu-id="6a714-134">Il numero di serie/fornitore/modello (SNVM) SNVM è 3 stringhe che rappresentano il nome del fornitore, il nome del prodotto nello spazio dei nomi del fornitore e il numero di serie nello spazio dei nomi del modello.</span><span class="sxs-lookup"><span data-stu-id="6a714-134">Serial Number/Vendor/Model (SNVM) SNVM is 3 strings representing the vendor name, product name within the vendor namespace, and the serial number within the model namespace.</span></span> <span data-ttu-id="6a714-135">Le stringhe sono delimitate da' +'.</span><span class="sxs-lookup"><span data-stu-id="6a714-135">Strings are delimited with a '+'.</span></span> <span data-ttu-id="6a714-136">Gli spazi possono essere inclusi e sono significativi.</span><span class="sxs-lookup"><span data-stu-id="6a714-136">Spaces may be included and are significant.</span></span> <span data-ttu-id="6a714-137">Il numero di serie è la rappresentazione testuale del numero di serie in lettere maiuscole esadecimali.</span><span class="sxs-lookup"><span data-stu-id="6a714-137">The serial number is the text representation of the serial number in hexadecimal upper case.</span></span> <span data-ttu-id="6a714-138">Rappresenta il fornitore e l'ID modello dai dati di richiesta SCSI; il campo fornitore deve avere una larghezza di 8 caratteri e il campo prodotto deve avere una larghezza di 16 caratteri.</span><span class="sxs-lookup"><span data-stu-id="6a714-138">This represents the vendor and model ID from SCSI Inquiry data; the vendor field MUST be 8 characters wide and the product field MUST be 16 characters wide.</span></span> <span data-ttu-id="6a714-139">Ad esempio,</span><span class="sxs-lookup"><span data-stu-id="6a714-139">For example,</span></span>

<span data-ttu-id="6a714-140">' Acme \_ \_ \_ \_ + Super Disk \_ \_ \_ \_ \_ \_ + 124437458' ( \_ è un carattere spazio)</span><span class="sxs-lookup"><span data-stu-id="6a714-140">'ACME\_\_\_\_+SUPER DISK\_\_\_\_\_\_+124437458' (\_ is a space character)</span></span>

</dd> <dt>

<span id="NAA"></span><span id="naa"></span>

<span data-ttu-id="6a714-141"><span id="NAA"></span><span id="naa"></span>**NAA** (9)</span><span class="sxs-lookup"><span data-stu-id="6a714-141"><span id="NAA"></span><span id="naa"></span>**NAA** (9)</span></span>


</dt> <dd>

<span data-ttu-id="6a714-142">9 = NAA come formato generico.</span><span class="sxs-lookup"><span data-stu-id="6a714-142">9 = NAA as a generic format.</span></span> <span data-ttu-id="6a714-143">Vedere</span><span class="sxs-lookup"><span data-stu-id="6a714-143">See</span></span>

<span data-ttu-id="6a714-144"> https://standards.ieee.org/regauth/oui/tutorials/fibrecomp\_id.html.</span><span class="sxs-lookup"><span data-stu-id="6a714-144">https://standards.ieee.org/regauth/oui/tutorials/fibrecomp\_id.html.</span></span> <span data-ttu-id="6a714-145">Formattato come 16 o 32 caratteri esadecimali maiuscoli non separati (2 per byte binario).</span><span class="sxs-lookup"><span data-stu-id="6a714-145">Formatted as 16 or 32 unseparated uppercase hex characters (2 per binary byte).</span></span>

<span data-ttu-id="6a714-146">Ad esempio ' 21000020372D3C73'</span><span class="sxs-lookup"><span data-stu-id="6a714-146">For example '21000020372D3C73'</span></span>

</dd> <dt>

<span id="EUI64"></span><span id="eui64"></span>

<span data-ttu-id="6a714-147"><span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)</span><span class="sxs-lookup"><span data-stu-id="6a714-147"><span id="EUI64"></span><span id="eui64"></span>**EUI64** (10)</span></span>


</dt> <dd>

<span data-ttu-id="6a714-148">EUI come formato generico (EUI64) vedere</span><span class="sxs-lookup"><span data-stu-id="6a714-148">EUI as a generic format (EUI64) See</span></span>

<span data-ttu-id="6a714-149"> https://standards.ieee.org/content/dam/ieee-standards/standards/web/documents/tutorials/eui.pdf.</span><span class="sxs-lookup"><span data-stu-id="6a714-149">https://standards.ieee.org/content/dam/ieee-standards/standards/web/documents/tutorials/eui.pdf.</span></span>

</dd> <dt>

<span id="T10VID"></span><span id="t10vid"></span>

<span data-ttu-id="6a714-150"><span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)</span><span class="sxs-lookup"><span data-stu-id="6a714-150"><span id="T10VID"></span><span id="t10vid"></span>**T10VID** (11)</span></span>


</dt> <dd>

<span data-ttu-id="6a714-151">Formato dell'identificatore del fornitore T10 come restituito dalla richiesta SCSI Vital pagina 83, identificatore tipo 1.</span><span class="sxs-lookup"><span data-stu-id="6a714-151">T10 vendor identifier format as returned by SCSI Inquiry VPD page 83, identifier type 1.</span></span> <span data-ttu-id="6a714-152">Vedere la specifica di T10 SPC-3.</span><span class="sxs-lookup"><span data-stu-id="6a714-152">See T10 SPC-3 specification.</span></span> <span data-ttu-id="6a714-153">ID del fornitore ASCII a 8 byte dal registro di sistema T10 seguito da un identificatore ASCII specifico del fornitore. gli spazi sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="6a714-153">This is the 8-byte ASCII vendor ID from the T10 registry followed by a vendor specific ASCII identifier; spaces are permitted.</span></span> <span data-ttu-id="6a714-154">Per i volumi non SCSI,' SNVM ' può essere la scelta più appropriata.</span><span class="sxs-lookup"><span data-stu-id="6a714-154">For non SCSI volumes, 'SNVM' may be the most appropriate choice.</span></span>

</dd> <dt>

<span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>

<span data-ttu-id="6a714-155"><span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**Nome dispositivo del sistema operativo** (12)</span><span class="sxs-lookup"><span data-stu-id="6a714-155"><span id="OS_Device_Name"></span><span id="os_device_name"></span><span id="OS_DEVICE_NAME"></span>**OS Device Name** (12)</span></span>


</dt> <dd>

<span data-ttu-id="6a714-156">Nome del dispositivo del sistema operativo (per LogicalDisks).</span><span class="sxs-lookup"><span data-stu-id="6a714-156">OS Device Name (for LogicalDisks).</span></span> <span data-ttu-id="6a714-157">Per informazioni dettagliate, vedere la descrizione del nome disco logico.</span><span class="sxs-lookup"><span data-stu-id="6a714-157">See LogicalDisk Name description for details.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="6a714-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="6a714-158"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6a714-159">**HostExtentNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="6a714-159">**HostExtentNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a714-160">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6a714-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6a714-161">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a714-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a714-162">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentName**","**CIM \_ StorageAllocationSettingData**.**OtherHostExtentNameNamespace**","**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**","[**CIM \_ StorageExtent**](cim-storageextent.md).**Spazio dei nomi**")</span><span class="sxs-lookup"><span data-stu-id="6a714-162">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentName**", "**CIM\_StorageAllocationSettingData**.**OtherHostExtentNameNamespace**", "**CIM\_StorageAllocationSettingData**.**HostExtentNameFormat**", "[**CIM\_StorageExtent**](cim-storageextent.md).**Namespace**")</span></span>
</dt> </dl>

<span data-ttu-id="6a714-163">Formato di denominazione per la proprietà **Name** .</span><span class="sxs-lookup"><span data-stu-id="6a714-163">The naming format for the **Name** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6a714-164">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="6a714-164">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6a714-165">**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="6a714-165">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type3"></span><span id="vpd83type3"></span><span id="VPD83TYPE3"></span>

<span data-ttu-id="6a714-166">**VPD83Type3** (2)</span><span class="sxs-lookup"><span data-stu-id="6a714-166">**VPD83Type3** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type2"></span><span id="vpd83type2"></span><span id="VPD83TYPE2"></span>

<span data-ttu-id="6a714-167">**VPD83Type2** (3)</span><span class="sxs-lookup"><span data-stu-id="6a714-167">**VPD83Type2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD83Type1"></span><span id="vpd83type1"></span><span id="VPD83TYPE1"></span>

<span data-ttu-id="6a714-168">**VPD83Type1** (4)</span><span class="sxs-lookup"><span data-stu-id="6a714-168">**VPD83Type1** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="VPD80"></span><span id="vpd80"></span>

<span data-ttu-id="6a714-169">**VPD80** (5)</span><span class="sxs-lookup"><span data-stu-id="6a714-169">**VPD80** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="NodeWWN"></span><span id="nodewwn"></span><span id="NODEWWN"></span>

<span data-ttu-id="6a714-170">**NodeWWN** (6)</span><span class="sxs-lookup"><span data-stu-id="6a714-170">**NodeWWN** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SNVM"></span><span id="snvm"></span>

<span data-ttu-id="6a714-171">**SNVM** (7)</span><span class="sxs-lookup"><span data-stu-id="6a714-171">**SNVM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_Device_Namespace"></span><span id="os_device_namespace"></span><span id="OS_DEVICE_NAMESPACE"></span>

<span data-ttu-id="6a714-172">**Spazio dei nomi del dispositivo del sistema operativo** (8)</span><span class="sxs-lookup"><span data-stu-id="6a714-172">**OS Device Namespace** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="6a714-173">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="6a714-173">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6a714-174">**HostExtentStartingAddress**</span><span class="sxs-lookup"><span data-stu-id="6a714-174">**HostExtentStartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a714-175">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6a714-175">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6a714-176">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a714-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a714-177">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostResourceBlockSize**","[**CIM \_ BasedOn**](cim-basedon.md).**IndirizzoIniziale**")</span><span class="sxs-lookup"><span data-stu-id="6a714-177">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostResourceBlockSize**", "[**CIM\_BasedOn**](cim-basedon.md).**StartingAddress**")</span></span>
</dt> </dl>

<span data-ttu-id="6a714-178">Indirizzo iniziale nell'extent di archiviazione dell'host.</span><span class="sxs-lookup"><span data-stu-id="6a714-178">The starting address on the host storage extent.</span></span> <span data-ttu-id="6a714-179">Un valore NULL Val; UE indica che non esiste alcun mapping diretto tra l'extent di archiviazione virtuale e l'extent di archiviazione dell'host.</span><span class="sxs-lookup"><span data-stu-id="6a714-179">A NULL val;ue indicates that there is no direct mapping between the virtual storage extent and the host storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="6a714-180">**HostResourceBlockSize**</span><span class="sxs-lookup"><span data-stu-id="6a714-180">**HostResourceBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a714-181">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6a714-181">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6a714-182">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a714-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a714-183">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**BlockSize**"), **punito** (" byte ")</span><span class="sxs-lookup"><span data-stu-id="6a714-183">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_StorageExtent**](cim-storageextent.md).**BlockSize**"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="6a714-184">Dimensione, in byte, dei blocchi allocati nell'host per l'allocazione dell'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6a714-184">The size, in bytes, of the blocks that are allocated on the host for the storage allocation.</span></span> <span data-ttu-id="6a714-185">Se la dimensione del blocco è variabile, è necessario specificare la dimensione massima del blocco in byte.</span><span class="sxs-lookup"><span data-stu-id="6a714-185">If the block size is variable, then the maximum block size in bytes should be specified.</span></span> <span data-ttu-id="6a714-186">Se le dimensioni del blocco sono sconosciute o se non si applica un concetto di blocco, è necessario usare il valore "1" (sconosciuto).</span><span class="sxs-lookup"><span data-stu-id="6a714-186">If the block size is unknown or if a block concept does not apply, then the value "1" (unknown) should be used.</span></span>

</dd> <dt>

<span data-ttu-id="6a714-187">**Limite**</span><span class="sxs-lookup"><span data-stu-id="6a714-187">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a714-188">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6a714-188">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6a714-189">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a714-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a714-190">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("Limit"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostResourceBlockSize**")</span><span class="sxs-lookup"><span data-stu-id="6a714-190">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Limit"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostResourceBlockSize**")</span></span>
</dt> </dl>

<span data-ttu-id="6a714-191">Quantità massima di blocchi che verranno concessi per l'allocazione delle risorse di archiviazione nell'host.</span><span class="sxs-lookup"><span data-stu-id="6a714-191">The maximum amount of blocks that will be granted for the storage resource allocation on the host.</span></span> <span data-ttu-id="6a714-192">La dimensione del blocco viene specificata dalla proprietà **HostResourceBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="6a714-192">The block size is specified by the **HostResourceBlockSize** property.</span></span>

</dd> <dt>

<span data-ttu-id="6a714-193">**OtherHostExtentNameFormat**</span><span class="sxs-lookup"><span data-stu-id="6a714-193">**OtherHostExtentNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a714-194">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6a714-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a714-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a714-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a714-196">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentNameFormat**")</span><span class="sxs-lookup"><span data-stu-id="6a714-196">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentNameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="6a714-197">Formato della proprietà **HostExtentName** se la proprietà è impostata su "1" (other).</span><span class="sxs-lookup"><span data-stu-id="6a714-197">The format of the **HostExtentName** property if the property is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="6a714-198">**OtherHostExtentNameNamespace**</span><span class="sxs-lookup"><span data-stu-id="6a714-198">**OtherHostExtentNameNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a714-199">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6a714-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a714-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a714-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a714-201">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostExtentNameNamespace**")</span><span class="sxs-lookup"><span data-stu-id="6a714-201">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostExtentNameNamespace**")</span></span>
</dt> </dl>

<span data-ttu-id="6a714-202">Stringa che descrive lo spazio dei nomi della proprietà **HostExtentName** se il valore della proprietà **HostExtentNameNamespace** è "1" (other).</span><span class="sxs-lookup"><span data-stu-id="6a714-202">A string that describes the namespace of the **HostExtentName** property if the value of the **HostExtentNameNamespace** property is "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="6a714-203">**Prenotazione**</span><span class="sxs-lookup"><span data-stu-id="6a714-203">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a714-204">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6a714-204">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6a714-205">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a714-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a714-206">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("Reservation"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**HostResourceBlockSize**")</span><span class="sxs-lookup"><span data-stu-id="6a714-206">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Reservation"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**HostResourceBlockSize**")</span></span>
</dt> </dl>

<span data-ttu-id="6a714-207">Quantità di blocchi di cui è garantita la disponibilità per l'allocazione delle risorse di archiviazione nell'host.</span><span class="sxs-lookup"><span data-stu-id="6a714-207">The amount of blocks that are guaranteed to be available for the storage resource allocation on the host.</span></span> <span data-ttu-id="6a714-208">La dimensione del blocco viene specificata dalla proprietà **HostResourceBlockSize** .</span><span class="sxs-lookup"><span data-stu-id="6a714-208">The block size is specified by the **HostResourceBlockSize** property.</span></span>

</dd> <dt>

<span data-ttu-id="6a714-209">**VirtualQuantity**</span><span class="sxs-lookup"><span data-stu-id="6a714-209">**VirtualQuantity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a714-210">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6a714-210">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6a714-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a714-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a714-212">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("VirtualQuantity"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**Proprietà NumberOfBlocks**","**CIM \_ StorageAllocationSettingData**.**VirtualQuantityUnits**")</span><span class="sxs-lookup"><span data-stu-id="6a714-212">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("VirtualQuantity"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_StorageExtent**](cim-storageextent.md).**NumberOfBlocks**", "**CIM\_StorageAllocationSettingData**.**VirtualQuantityUnits**")</span></span>
</dt> </dl>

<span data-ttu-id="6a714-213">Il numero di blocchi che l'allocazione di archiviazione presenta al consumer.</span><span class="sxs-lookup"><span data-stu-id="6a714-213">The number of blocks that the storage allocation presents to the consumer.</span></span>

> [!Note]  
> <span data-ttu-id="6a714-214">La proprietà **VirtualQuantity** può specificare una dimensione di blocco pari a "1", anche se **VirtualResourceBlockSize** è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="6a714-214">The **VirtualQuantity** property can specify a block size of "1", even if **VirtualResourceBlockSize** is unknown.</span></span>

 

</dd> <dt>

<span data-ttu-id="6a714-215">**VirtualQuantityUnits**</span><span class="sxs-lookup"><span data-stu-id="6a714-215">**VirtualQuantityUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a714-216">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="6a714-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6a714-217">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a714-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a714-218">Qualificatori: [**override**](../wmisdk/standard-qualifiers.md) ("VirtualQuantityUnits"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM \_ StorageAllocationSettingData**.**VirtualQuantity**"), **IsPUnit**</span><span class="sxs-lookup"><span data-stu-id="6a714-218">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("VirtualQuantityUnits"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("**CIM\_StorageAllocationSettingData**.**VirtualQuantity**"), **IsPUnit**</span></span>
</dt> </dl>

<span data-ttu-id="6a714-219">Unità utilizzate dalla proprietà **VirtualQuantity** .</span><span class="sxs-lookup"><span data-stu-id="6a714-219">The units used by the **VirtualQuantity** property.</span></span> <span data-ttu-id="6a714-220">Questo valore deve essere impostato su "Count (blocco a dimensione fissa)" o "byte".</span><span class="sxs-lookup"><span data-stu-id="6a714-220">This value shall should be set to "count(fixed size block)" or "byte".</span></span> <span data-ttu-id="6a714-221">Il valore predefinito "Count (blocco a dimensione fissa)" deve essere utilizzato per una dimensione fissa del blocco e deve essere utilizzato "byte" per una dimensione del blocco sconosciuta o variabile.</span><span class="sxs-lookup"><span data-stu-id="6a714-221">The default value, "count(fixed size block)" should be used for a fixed block size, and "byte" should be used for an unknown or variable block size.</span></span>

</dd> <dt>

<span data-ttu-id="6a714-222">**VirtualResourceBlockSize**</span><span class="sxs-lookup"><span data-stu-id="6a714-222">**VirtualResourceBlockSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6a714-223">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6a714-223">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6a714-224">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6a714-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6a714-225">Qualificatori: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ StorageExtent**](cim-storageextent.md).**BlockSize**"), **punito** (" byte ")</span><span class="sxs-lookup"><span data-stu-id="6a714-225">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_StorageExtent**](cim-storageextent.md).**BlockSize**"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="6a714-226">Dimensione, in byte, dei blocchi che formano la richiesta di allocazione dell'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6a714-226">The size, in bytes, of the blocks that form the storage allocation request.</span></span> <span data-ttu-id="6a714-227">Se la dimensione del blocco è variabile, è necessario specificare la dimensione massima del blocco.</span><span class="sxs-lookup"><span data-stu-id="6a714-227">If the block size is variable, then the maximum block size should be specified.</span></span> <span data-ttu-id="6a714-228">Se la dimensione del blocco è sconosciuta o se non si applica un concetto di blocco, la dimensione del blocco deve essere "1" (sconosciuta).</span><span class="sxs-lookup"><span data-stu-id="6a714-228">If the block size is unknown or if a block concept does not apply, then the block size should be "1" (unknown).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6a714-229">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a714-229">Requirements</span></span>



| <span data-ttu-id="6a714-230">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a714-230">Requirement</span></span> | <span data-ttu-id="6a714-231">Valore</span><span class="sxs-lookup"><span data-stu-id="6a714-231">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a714-232">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a714-232">Minimum supported client</span></span><br/> | <span data-ttu-id="6a714-233">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6a714-233">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="6a714-234">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a714-234">Minimum supported server</span></span><br/> | <span data-ttu-id="6a714-235">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6a714-235">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="6a714-236">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6a714-236">Namespace</span></span><br/>                | <span data-ttu-id="6a714-237">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="6a714-237">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6a714-238">MOF</span><span class="sxs-lookup"><span data-stu-id="6a714-238">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a714-239"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a714-239"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a714-240">DLL</span><span class="sxs-lookup"><span data-stu-id="6a714-240">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a714-241"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6a714-241"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6a714-242">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a714-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a714-243">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="6a714-243">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 


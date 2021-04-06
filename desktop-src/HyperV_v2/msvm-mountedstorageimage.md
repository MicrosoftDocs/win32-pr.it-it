---
description: Fornisce informazioni dettagliate su un'immagine di archiviazione montata manualmente.
ms.assetid: 40b94c5f-c277-40c8-a55d-ebc64cb231ca
title: Classe Msvm_MountedStorageImage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MountedStorageImage
- Msvm_MountedStorageImage.InstanceID
- Msvm_MountedStorageImage.Caption
- Msvm_MountedStorageImage.Description
- Msvm_MountedStorageImage.ElementName
- Msvm_MountedStorageImage.InstallDate
- Msvm_MountedStorageImage.Name
- Msvm_MountedStorageImage.OperationalStatus
- Msvm_MountedStorageImage.StatusDescriptions
- Msvm_MountedStorageImage.Status
- Msvm_MountedStorageImage.HealthState
- Msvm_MountedStorageImage.CommunicationStatus
- Msvm_MountedStorageImage.DetailedStatus
- Msvm_MountedStorageImage.OperatingStatus
- Msvm_MountedStorageImage.PrimaryStatus
- Msvm_MountedStorageImage.Type
- Msvm_MountedStorageImage.Access
- Msvm_MountedStorageImage.PortNumber
- Msvm_MountedStorageImage.PathId
- Msvm_MountedStorageImage.TargetId
- Msvm_MountedStorageImage.Lun
- Msvm_MountedStorageImage.PnpDevicePath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1b6f00b137fc73bcf8f79d39e6f7bfb5a6d7c944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759650"
---
# <a name="msvm_mountedstorageimage-class"></a><span data-ttu-id="d68cd-103">\_Classe MSVM MountedStorageImage</span><span class="sxs-lookup"><span data-stu-id="d68cd-103">Msvm\_MountedStorageImage class</span></span>

<span data-ttu-id="d68cd-104">Fornisce informazioni dettagliate su un'immagine di archiviazione montata manualmente.</span><span class="sxs-lookup"><span data-stu-id="d68cd-104">Provides detailed information about a manually mounted storage image.</span></span>

<span data-ttu-id="d68cd-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d68cd-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d68cd-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d68cd-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MountedStorageImage : CIM_LogicalElement
{
  string   InstanceID;
  string   Caption = "Mounted Storage Image";
  string   Description = "Information about a mounted storage image.";
  string   ElementName = "Mounted Storage Image";
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[] = { "OK" };
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   Type;
  uint16   Access;
  UINT8    PortNumber;
  UINT8    PathId;
  UINT8    TargetId;
  UINT8    Lun;
  string   PnpDevicePath;
};
```

## <a name="members"></a><span data-ttu-id="d68cd-107">Members</span><span class="sxs-lookup"><span data-stu-id="d68cd-107">Members</span></span>

<span data-ttu-id="d68cd-108">La **classe \_ MountedStorageImage di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d68cd-108">The **Msvm\_MountedStorageImage** class has these types of members:</span></span>

-   [<span data-ttu-id="d68cd-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="d68cd-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="d68cd-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d68cd-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d68cd-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="d68cd-111">Methods</span></span>

<span data-ttu-id="d68cd-112">La **classe \_ MountedStorageImage di MSVM** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="d68cd-112">The **Msvm\_MountedStorageImage** class has these methods.</span></span>



| <span data-ttu-id="d68cd-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="d68cd-113">Method</span></span>                                                                          | <span data-ttu-id="d68cd-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d68cd-114">Description</span></span>                                    |
|:--------------------------------------------------------------------------------|:-----------------------------------------------|
| [<span data-ttu-id="d68cd-115">**DetachVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="d68cd-115">**DetachVirtualHardDisk**</span></span>](detachvirtualharddisk-msvm-mountedstorageimage.md) | <span data-ttu-id="d68cd-116">Scollega l'immagine di archiviazione montata.</span><span class="sxs-lookup"><span data-stu-id="d68cd-116">Detaches the mounted storage image.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d68cd-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d68cd-117">Properties</span></span>

<span data-ttu-id="d68cd-118">La **classe \_ MountedStorageImage di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d68cd-118">The **Msvm\_MountedStorageImage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d68cd-119">**Accesso**</span><span class="sxs-lookup"><span data-stu-id="d68cd-119">**Access**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d68cd-120">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d68cd-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d68cd-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d68cd-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d68cd-122">Accesso in cui viene montata l'immagine di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d68cd-122">The access under which the storage image is mounted.</span></span>

<dt>

<span id="Read-only"></span><span id="read-only"></span><span id="READ-ONLY"></span>

<span data-ttu-id="d68cd-123">Sola **lettura** (1)</span><span class="sxs-lookup"><span data-stu-id="d68cd-123">**Read-only** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write"></span><span id="read_write"></span><span id="READ_WRITE"></span>

<span data-ttu-id="d68cd-124">**Lettura/scrittura** (2)</span><span class="sxs-lookup"><span data-stu-id="d68cd-124">**Read/Write** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d68cd-125">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="d68cd-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d68cd-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d68cd-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d68cd-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d68cd-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d68cd-128">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d68cd-128">A short description of the object.</span></span> <span data-ttu-id="d68cd-129">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e contiene sempre "mounted storage image".</span><span class="sxs-lookup"><span data-stu-id="d68cd-129">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it always contains "Mounted Storage Image".</span></span>

</dd> <dt>

<span data-ttu-id="d68cd-130">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="d68cd-130">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d68cd-131">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d68cd-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d68cd-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d68cd-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d68cd-133">Indica la capacità della strumentazione di comunicare con l'elemento gestito sottostante.</span><span class="sxs-lookup"><span data-stu-id="d68cd-133">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="d68cd-134">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="d68cd-134">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d68cd-135">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="d68cd-135">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d68cd-136">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d68cd-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d68cd-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d68cd-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d68cd-138">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="d68cd-138">A description of the object.</span></span> <span data-ttu-id="d68cd-139">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e contiene sempre "informazioni su un'immagine di archiviazione montata".</span><span class="sxs-lookup"><span data-stu-id="d68cd-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it always contains "Information about a mounted storage image.".</span></span>

</dd> <dt>

<span data-ttu-id="d68cd-140">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="d68cd-140">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d68cd-141">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d68cd-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d68cd-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d68cd-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d68cd-143">Aggiunge un complimento alla proprietà **PrimaryStatus** con ulteriori dettagli sullo stato.</span><span class="sxs-lookup"><span data-stu-id="d68cd-143">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="d68cd-144">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="d68cd-144">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d68cd-145">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d68cd-145">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d68cd-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d68cd-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d68cd-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d68cd-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d68cd-148">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d68cd-148">A display name for the object.</span></span> <span data-ttu-id="d68cd-149">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e contiene sempre "mounted storage image".</span><span class="sxs-lookup"><span data-stu-id="d68cd-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it always contains "Mounted Storage Image".</span></span>

</dd> <dt>

<span data-ttu-id="d68cd-150">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="d68cd-150">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d68cd-151">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d68cd-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d68cd-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d68cd-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d68cd-153">Stato corrente dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="d68cd-153">The current health of the element.</span></span> <span data-ttu-id="d68cd-154">Questo attributo esprime lo stato di integrità di questo elemento ma non necessariamente dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="d68cd-154">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="d68cd-155">I valori possibili sono compresi tra 0 e 30, dove 5 indica che l'elemento è completamente integro e 30 indica che l'elemento è completamente non funzionale.</span><span class="sxs-lookup"><span data-stu-id="d68cd-155">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="d68cd-156">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su 5.</span><span class="sxs-lookup"><span data-stu-id="d68cd-156">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5.</span></span>

</dd> <dt>

<span data-ttu-id="d68cd-157">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d68cd-157">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d68cd-158">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="d68cd-158">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d68cd-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d68cd-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d68cd-160">Data e ora di creazione della configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d68cd-160">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="d68cd-161">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d68cd-161">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d68cd-162">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d68cd-162">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d68cd-163">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d68cd-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d68cd-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d68cd-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d68cd-165">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="d68cd-165">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d68cd-166">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="d68cd-166">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d68cd-167">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre **null**.</span><span class="sxs-lookup"><span data-stu-id="d68cd-167">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d68cd-168">**Lun**</span><span class="sxs-lookup"><span data-stu-id="d68cd-168">**Lun**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d68cd-169">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="d68cd-169">Data type: **UINT8**</span></span>
</dt> <dt>

<span data-ttu-id="d68cd-170">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d68cd-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d68cd-171">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d68cd-171">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d68cd-172">ID LUN dell'indirizzo SCSI.</span><span class="sxs-lookup"><span data-stu-id="d68cd-172">The SCSI address LUN ID.</span></span>

</dd> <dt>

<span data-ttu-id="d68cd-173">**Nome**</span><span class="sxs-lookup"><span data-stu-id="d68cd-173">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d68cd-174">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d68cd-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d68cd-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d68cd-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d68cd-176">Percorso del disco rigido virtuale montato.</span><span class="sxs-lookup"><span data-stu-id="d68cd-176">The path to the VHD that is mounted.</span></span> <span data-ttu-id="d68cd-177">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="d68cd-177">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="d68cd-178">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="d68cd-178">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d68cd-179">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d68cd-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d68cd-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d68cd-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d68cd-181">Fornisce informazioni sullo stato corrente per la condizione operativa dell'elemento e può essere utilizzato per fornire maggiori dettagli rispetto al valore della proprietà **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="d68cd-181">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="d68cd-182">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="d68cd-182">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d68cd-183">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="d68cd-183">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d68cd-184">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d68cd-184">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="d68cd-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d68cd-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d68cd-186">Stato corrente dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d68cd-186">The current status of the object.</span></span> <span data-ttu-id="d68cd-187">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="d68cd-187">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d68cd-188">**PathId**</span><span class="sxs-lookup"><span data-stu-id="d68cd-188">**PathId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d68cd-189">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="d68cd-189">Data type: **UINT8**</span></span>
</dt> <dt>

<span data-ttu-id="d68cd-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d68cd-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d68cd-191">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d68cd-191">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d68cd-192">ID del percorso dell'indirizzo SCSI.</span><span class="sxs-lookup"><span data-stu-id="d68cd-192">The SCSI address path ID.</span></span>

</dd> <dt>

<span data-ttu-id="d68cd-193">**PnpDevicePath**</span><span class="sxs-lookup"><span data-stu-id="d68cd-193">**PnpDevicePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d68cd-194">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d68cd-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d68cd-195">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d68cd-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d68cd-196">Percorso del dispositivo PNP.</span><span class="sxs-lookup"><span data-stu-id="d68cd-196">The PNP device path.</span></span>

<span data-ttu-id="d68cd-197">**Windows 8.1:** Questo valore non è supportato fino a Windows 8.1 e Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="d68cd-197">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="d68cd-198">**NumeroPorta**</span><span class="sxs-lookup"><span data-stu-id="d68cd-198">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d68cd-199">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="d68cd-199">Data type: **UINT8**</span></span>
</dt> <dt>

<span data-ttu-id="d68cd-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d68cd-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d68cd-201">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d68cd-201">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d68cd-202">Numero di porta dell'indirizzo SCSI.</span><span class="sxs-lookup"><span data-stu-id="d68cd-202">The SCSI address port number.</span></span>

</dd> <dt>

<span data-ttu-id="d68cd-203">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="d68cd-203">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d68cd-204">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d68cd-204">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d68cd-205">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d68cd-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d68cd-206">Fornisce informazioni sullo stato di alto livello.</span><span class="sxs-lookup"><span data-stu-id="d68cd-206">Provides high level status information.</span></span> <span data-ttu-id="d68cd-207">Questa proprietà deve essere utilizzata in combinazione con la proprietà **DetailedStatus** per fornire lo stato di integrità di livello elevato e dettagliato dell'elemento e dei relativi sottocomponenti.</span><span class="sxs-lookup"><span data-stu-id="d68cd-207">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="d68cd-208">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su **null**.</span><span class="sxs-lookup"><span data-stu-id="d68cd-208">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="d68cd-209">**Status**</span><span class="sxs-lookup"><span data-stu-id="d68cd-209">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d68cd-210">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d68cd-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d68cd-211">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d68cd-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d68cd-212">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)ed è sempre impostata su "OK".</span><span class="sxs-lookup"><span data-stu-id="d68cd-212">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="d68cd-213">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="d68cd-213">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d68cd-214">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="d68cd-214">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d68cd-215">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d68cd-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d68cd-216">Stringhe che descrivono i vari valori della matrice **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="d68cd-216">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="d68cd-217">Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e ogni elemento della matrice è sempre impostato su "OK".</span><span class="sxs-lookup"><span data-stu-id="d68cd-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="d68cd-218">**TargetId**</span><span class="sxs-lookup"><span data-stu-id="d68cd-218">**TargetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d68cd-219">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="d68cd-219">Data type: **UINT8**</span></span>
</dt> <dt>

<span data-ttu-id="d68cd-220">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d68cd-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d68cd-221">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d68cd-221">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d68cd-222">ID di destinazione dell'indirizzo SCSI.</span><span class="sxs-lookup"><span data-stu-id="d68cd-222">The SCSI address target ID.</span></span>

</dd> <dt>

<span data-ttu-id="d68cd-223">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d68cd-223">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d68cd-224">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d68cd-224">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d68cd-225">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d68cd-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d68cd-226">Tipo di immagine di archiviazione montata.</span><span class="sxs-lookup"><span data-stu-id="d68cd-226">The type of storage image mounted.</span></span>

<dt>

<span id="Virtual_Hard_Disk"></span><span id="virtual_hard_disk"></span><span id="VIRTUAL_HARD_DISK"></span>

<span data-ttu-id="d68cd-227">**Disco rigido virtuale** (0)</span><span class="sxs-lookup"><span data-stu-id="d68cd-227">**Virtual Hard Disk** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_Image"></span><span id="iso_image"></span><span id="ISO_IMAGE"></span>

<span data-ttu-id="d68cd-228">**Immagine ISO** (1)</span><span class="sxs-lookup"><span data-stu-id="d68cd-228">**ISO Image** (1)</span></span>


<span data-ttu-id="d68cd-229"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d68cd-229"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="d68cd-230">Commenti</span><span class="sxs-lookup"><span data-stu-id="d68cd-230">Remarks</span></span>

<span data-ttu-id="d68cd-231">L'accesso alla **classe \_ MountedStorageImage di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="d68cd-231">Access to the **Msvm\_MountedStorageImage** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d68cd-232">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d68cd-232">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="d68cd-233">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d68cd-233">Requirements</span></span>



| <span data-ttu-id="d68cd-234">Requisito</span><span class="sxs-lookup"><span data-stu-id="d68cd-234">Requirement</span></span> | <span data-ttu-id="d68cd-235">Valore</span><span class="sxs-lookup"><span data-stu-id="d68cd-235">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d68cd-236">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d68cd-236">Minimum supported client</span></span><br/> | <span data-ttu-id="d68cd-237">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d68cd-237">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d68cd-238">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d68cd-238">Minimum supported server</span></span><br/> | <span data-ttu-id="d68cd-239">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d68cd-239">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d68cd-240">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d68cd-240">Namespace</span></span><br/>                | <span data-ttu-id="d68cd-241">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="d68cd-241">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d68cd-242">MOF</span><span class="sxs-lookup"><span data-stu-id="d68cd-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d68cd-243"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d68cd-243"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d68cd-244">DLL</span><span class="sxs-lookup"><span data-stu-id="d68cd-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d68cd-245"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d68cd-245"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d68cd-246">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d68cd-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d68cd-247">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="d68cd-247">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="d68cd-248">**\_LogicalElement CIM**</span><span class="sxs-lookup"><span data-stu-id="d68cd-248">**CIM\_LogicalElement**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicalelement)
</dt> <dt>

[<span data-ttu-id="d68cd-249">Classi di archiviazione</span><span class="sxs-lookup"><span data-stu-id="d68cd-249">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 


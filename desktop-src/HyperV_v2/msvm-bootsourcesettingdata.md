---
description: Rappresenta i parametri per impostare l'origine di avvio di una macchina virtuale.
ms.assetid: 21CD4B71-3D05-469E-89BB-DC2C65F5AB10
title: Classe Msvm_BootSourceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BootSourceSettingData
- Msvm_BootSourceSettingData.Description
- Msvm_BootSourceSettingData.Caption
- Msvm_BootSourceSettingData.InstanceID
- Msvm_BootSourceSettingData.ElementName
- Msvm_BootSourceSettingData.BootSourceType
- Msvm_BootSourceSettingData.OtherLocation
- Msvm_BootSourceSettingData.FirmwareDevicePath
- Msvm_BootSourceSettingData.BootSourceDescription
- Msvm_BootSourceSettingData.OptionalData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0403846e10df4c9bd54146eea44e8e91c06d01c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308340"
---
# <a name="msvm_bootsourcesettingdata-class"></a><span data-ttu-id="7bce1-103">\_Classe MSVM BootSourceSettingData</span><span class="sxs-lookup"><span data-stu-id="7bce1-103">Msvm\_BootSourceSettingData class</span></span>

<span data-ttu-id="7bce1-104">Rappresenta i parametri per impostare l'origine di avvio di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7bce1-104">Represents the parameters to set the boot source of a virtual machine.</span></span> <span data-ttu-id="7bce1-105">Questa classe deriva da [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7bce1-105">This class derives from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

<span data-ttu-id="7bce1-106">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="7bce1-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bce1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7bce1-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BootSourceSettingData : CIM_SettingData
{
  string Description;
  string Caption;
  string InstanceID;
  string ElementName;
  uint32 BootSourceType;
  string OtherLocation;
  string FirmwareDevicePath;
  string BootSourceDescription;
  uint8  OptionalData[];
};
```

## <a name="members"></a><span data-ttu-id="7bce1-108">Members</span><span class="sxs-lookup"><span data-stu-id="7bce1-108">Members</span></span>

<span data-ttu-id="7bce1-109">La **classe \_ BootSourceSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7bce1-109">The **Msvm\_BootSourceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="7bce1-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7bce1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7bce1-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7bce1-111">Properties</span></span>

<span data-ttu-id="7bce1-112">La **classe \_ BootSourceSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7bce1-112">The **Msvm\_BootSourceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7bce1-113">**BootSourceDescription**</span><span class="sxs-lookup"><span data-stu-id="7bce1-113">**BootSourceDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bce1-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7bce1-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bce1-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7bce1-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7bce1-116">Descrizione dell'origine di avvio fornita dal firmware.</span><span class="sxs-lookup"><span data-stu-id="7bce1-116">The description of the boot source provided by the firmware.</span></span>

</dd> <dt>

<span data-ttu-id="7bce1-117">**BootSourceType**</span><span class="sxs-lookup"><span data-stu-id="7bce1-117">**BootSourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bce1-118">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7bce1-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7bce1-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7bce1-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7bce1-120">Valore di enumerazione che specifica il tipo di origine di avvio.</span><span class="sxs-lookup"><span data-stu-id="7bce1-120">An enumeration value that specifies the type of the boot source.</span></span>

<span data-ttu-id="7bce1-121">Valori validi:</span><span class="sxs-lookup"><span data-stu-id="7bce1-121">These are valid values:</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7bce1-122">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="7bce1-122">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Drive"></span><span id="drive"></span><span id="DRIVE"></span>

<span data-ttu-id="7bce1-123">**Unità** (1)</span><span class="sxs-lookup"><span data-stu-id="7bce1-123">**Drive** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Network"></span><span id="network"></span><span id="NETWORK"></span>

<span data-ttu-id="7bce1-124">**Rete** (2)</span><span class="sxs-lookup"><span data-stu-id="7bce1-124">**Network** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="File"></span><span id="file"></span><span id="FILE"></span>

<span data-ttu-id="7bce1-125">**File** (3)</span><span class="sxs-lookup"><span data-stu-id="7bce1-125">**File** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7bce1-126">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="7bce1-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bce1-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7bce1-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bce1-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7bce1-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bce1-129">Qualificatori: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="7bce1-129">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="7bce1-130">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7bce1-130">A short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="7bce1-131">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="7bce1-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bce1-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7bce1-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bce1-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7bce1-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7bce1-134">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7bce1-134">A textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="7bce1-135">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="7bce1-135">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bce1-136">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7bce1-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bce1-137">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7bce1-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7bce1-138">Nome visualizzato per questa istanza di SettingData.</span><span class="sxs-lookup"><span data-stu-id="7bce1-138">The display name for this instance of SettingData.</span></span> <span data-ttu-id="7bce1-139">Inoltre, il nome visualizzato può essere utilizzato come proprietà di indice per una ricerca o una query.</span><span class="sxs-lookup"><span data-stu-id="7bce1-139">In addition, the display name can be used as an index property for a search or query.</span></span> <span data-ttu-id="7bce1-140">Nota: non è necessario che il nome sia univoco all'interno di uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="7bce1-140">(Note: The name does not have to be unique within a namespace.)</span></span>

</dd> <dt>

<span data-ttu-id="7bce1-141">**FirmwareDevicePath**</span><span class="sxs-lookup"><span data-stu-id="7bce1-141">**FirmwareDevicePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bce1-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7bce1-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bce1-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7bce1-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7bce1-144">Percorso nativo usato dal firmware per descrivere il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7bce1-144">The native path that the firmware uses to describe the device.</span></span>

</dd> <dt>

<span data-ttu-id="7bce1-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7bce1-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bce1-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7bce1-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bce1-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7bce1-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bce1-148">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="7bce1-148">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7bce1-149">All'interno dell'ambito dello spazio dei nomi di creazione di istanze, InstanceID indica in modo opaco e univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="7bce1-149">Within the scope of the instantiating Namespace, InstanceID opaquely and uniquely identifies an instance of this class.</span></span> <span data-ttu-id="7bce1-150">Per garantire l'univocità all'interno dello spazio dei nomi, il valore di InstanceID deve essere costruito usando l'algoritmo "preferito" seguente: *OrgID*:*localizzato* in cui *OrgID* e *LocalId* sono separati da due punti (:) e dove *OrgID* deve includere un nome con copyright, un marchio o in altro modo univoco di proprietà dell'entità di business che crea o definisce InstanceID o che è un ID registrato assegnato all'entità di business da un'autorità globale riconosciuta.</span><span class="sxs-lookup"><span data-stu-id="7bce1-150">To ensure uniqueness within the NameSpace, the value of InstanceID should be constructed using the following "preferred" algorithm: *OrgID*:*LocalID* Where *OrgID* and *LocalID* are separated by a colon (:), and where *OrgID* must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity that is creating or defining the InstanceID or that is a registered ID assigned to the business entity by a recognized global authority.</span></span> <span data-ttu-id="7bce1-151">(Questo requisito è simile a *SchemaName* \_ Struttura *ClassName* dei nomi delle classi dello schema. Inoltre, per garantire l'univocità, *OrgID* non deve contenere i due punti (:).</span><span class="sxs-lookup"><span data-stu-id="7bce1-151">(This requirement is similar to the *SchemaName*\_*ClassName* structure of Schema class names.) In addition, to ensure uniqueness, *OrgID* must not contain a colon (:).</span></span> <span data-ttu-id="7bce1-152">Quando si utilizza questo algoritmo, i primi due punti da visualizzare in InstanceID devono comparire tra *OrgID* e *localizzato*.</span><span class="sxs-lookup"><span data-stu-id="7bce1-152">When using this algorithm, the first colon to appear in InstanceID must appear between *OrgID* and *LocalID*.</span></span> <span data-ttu-id="7bce1-153">*Localizzato* viene scelto dall'entità business e non deve essere riutilizzato per identificare elementi diversi (reali) sottostanti.</span><span class="sxs-lookup"><span data-stu-id="7bce1-153">*LocalID* is chosen by the business entity and should not be reused to identify different underlying (real-world) elements.</span></span> <span data-ttu-id="7bce1-154">Se non viene utilizzato l'algoritmo preferenziale precedente, l'entità di definizione deve garantire che il InstanceID risultante non venga riutilizzato in alcun InstanceID prodotto da questo o da altri provider per lo spazio dei nomi di questa istanza.</span><span class="sxs-lookup"><span data-stu-id="7bce1-154">If the above preferred algorithm is not used, the defining entity must assure that the resulting InstanceID is not reused across any InstanceIDs produced by this or other providers for the NameSpace of this instance.</span></span> <span data-ttu-id="7bce1-155">Per le istanze definite da DMTF, è necessario usare l'algoritmo "preferenziale" con *OrgID* impostato su CIM.</span><span class="sxs-lookup"><span data-stu-id="7bce1-155">For DMTF-defined instances, the "preferred" algorithm must be used with the *OrgID* set to CIM.</span></span>

</dd> <dt>

<span data-ttu-id="7bce1-156">**OptionalData**</span><span class="sxs-lookup"><span data-stu-id="7bce1-156">**OptionalData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bce1-157">Tipo di dati: matrice **Uint8**</span><span class="sxs-lookup"><span data-stu-id="7bce1-157">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="7bce1-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7bce1-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bce1-159">Qualificatori: **OctetString**, [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="7bce1-159">Qualifiers: **OctetString**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="7bce1-160">Dati facoltativi forniti dal firmware.</span><span class="sxs-lookup"><span data-stu-id="7bce1-160">Optional data provided by the firmware.</span></span>

> [!Note]  
> <span data-ttu-id="7bce1-161">Proprietà aggiunta in Windows 10.</span><span class="sxs-lookup"><span data-stu-id="7bce1-161">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="7bce1-162">**OtherLocation**</span><span class="sxs-lookup"><span data-stu-id="7bce1-162">**OtherLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bce1-163">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7bce1-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bce1-164">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7bce1-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7bce1-165">Altre informazioni sulla posizione, se presenti, utilizzate dal firmware per identificare in modo univoco l'origine di avvio.</span><span class="sxs-lookup"><span data-stu-id="7bce1-165">The other location info, if any, that the firmware uses to further uniquely identify the boot source.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7bce1-166">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7bce1-166">Requirements</span></span>



| <span data-ttu-id="7bce1-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bce1-167">Requirement</span></span> | <span data-ttu-id="7bce1-168">Valore</span><span class="sxs-lookup"><span data-stu-id="7bce1-168">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bce1-169">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7bce1-169">Minimum supported client</span></span><br/> | <span data-ttu-id="7bce1-170">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7bce1-170">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="7bce1-171">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7bce1-171">Minimum supported server</span></span><br/> | <span data-ttu-id="7bce1-172">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7bce1-172">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7bce1-173">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7bce1-173">Namespace</span></span><br/>                | <span data-ttu-id="7bce1-174">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="7bce1-174">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7bce1-175">MOF</span><span class="sxs-lookup"><span data-stu-id="7bce1-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7bce1-176"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7bce1-176"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7bce1-177">DLL</span><span class="sxs-lookup"><span data-stu-id="7bce1-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7bce1-178"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7bce1-178"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7bce1-179">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7bce1-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bce1-180">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="7bce1-180">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

<span data-ttu-id="7bce1-181">[**\_SETTINGDATA CIM**](/previous-versions//cc136911(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7bce1-181">[**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85))</span></span>
</dt> </dl>

 


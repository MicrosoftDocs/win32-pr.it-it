---
description: Descrive un dispositivo Trusted Platform Module (TPM).
ms.assetid: c923106f-126e-4e7e-822a-2fb715bbbc26
title: Classe CIM_TPM
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM
- CIM_TPM.TPMSpecMajorVersion
- CIM_TPM.TPMSpecMinorVersion
- CIM_TPM.TPMManafucturerMajorRevision
- CIM_TPM.TPMManufacturerMinorRevision
- CIM_TPM.TPMManufacturerInfo
- CIM_TPM.TPMManufacturerId
- CIM_TPM.TPMState
- CIM_TPM.TransitioningToTPMState
- CIM_TPM.AvailableRequestedTPMStates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0f2d35d42e864a247ca042ec81813ff7d1ac5c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049830"
---
# <a name="cim_tpm-class"></a><span data-ttu-id="400f8-103">\_Classe TPM CIM</span><span class="sxs-lookup"><span data-stu-id="400f8-103">CIM\_TPM class</span></span>

<span data-ttu-id="400f8-104">Descrive un dispositivo Trusted Platform Module (TPM).</span><span class="sxs-lookup"><span data-stu-id="400f8-104">Describes a Trusted Platform Module (TPM) device.</span></span>

## <a name="syntax"></a><span data-ttu-id="400f8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="400f8-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.21.0"), UMLPackagePath("CIM::Device::TPM"), AMENDMENT]
class CIM_TPM : CIM_LogicalDevice
{
  uint32 TPMSpecMajorVersion;
  uint32 TPMSpecMinorVersion;
  uint32 TPMManafucturerMajorRevision;
  uint32 TPMManufacturerMinorRevision;
  string TPMManufacturerInfo;
  uint32 TPMManufacturerId;
  uint16 TPMState;
  uint16 TransitioningToTPMState = 12;
  uint16 AvailableRequestedTPMStates[];
};
```

## <a name="members"></a><span data-ttu-id="400f8-106">Members</span><span class="sxs-lookup"><span data-stu-id="400f8-106">Members</span></span>

<span data-ttu-id="400f8-107">La classe **CIM \_ TPM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="400f8-107">The **CIM\_TPM** class has these types of members:</span></span>

-   [<span data-ttu-id="400f8-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="400f8-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="400f8-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="400f8-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="400f8-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="400f8-110">Methods</span></span>

<span data-ttu-id="400f8-111">La classe del **\_ TPM CIM** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="400f8-111">The **CIM\_TPM** class has these methods.</span></span>



| <span data-ttu-id="400f8-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="400f8-112">Method</span></span>                                                         | <span data-ttu-id="400f8-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="400f8-113">Description</span></span>                                                                                                             |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="400f8-114">**ChangeOwnerAuth**</span><span class="sxs-lookup"><span data-stu-id="400f8-114">**ChangeOwnerAuth**</span></span>](cim-tpm-changeownerauth.md)             | <span data-ttu-id="400f8-115">Modifica le credenziali di autorizzazione del proprietario di un dispositivo TPM.</span><span class="sxs-lookup"><span data-stu-id="400f8-115">Changes the owner authorization credential of a TPM device.</span></span><br/>                                                  |
| [<span data-ttu-id="400f8-116">**RequestTPMStateChange**</span><span class="sxs-lookup"><span data-stu-id="400f8-116">**RequestTPMStateChange**</span></span>](cim-tpm-requesttpmstatechange.md) | <span data-ttu-id="400f8-117">Richiede che lo stato del TPM venga modificato in un valore specificato nel parametro **RequestedTPMState** .</span><span class="sxs-lookup"><span data-stu-id="400f8-117">Requests that the state of the TPM be changed to the value specified in the **RequestedTPMState** parameter.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="400f8-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="400f8-118">Properties</span></span>

<span data-ttu-id="400f8-119">La classe del **\_ TPM CIM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="400f8-119">The **CIM\_TPM** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="400f8-120">**AvailableRequestedTPMStates**</span><span class="sxs-lookup"><span data-stu-id="400f8-120">**AvailableRequestedTPMStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="400f8-121">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="400f8-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="400f8-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="400f8-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="400f8-123">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ TPM**.**RequestTPMStateChange**, CIM \_ TPMCapabilities. RequestedTPMStatesSupported ")</span><span class="sxs-lookup"><span data-stu-id="400f8-123">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_TPM**.**RequestTPMStateChange**, CIM\_TPMCapabilities.RequestedTPMStatesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="400f8-124">Valori possibili per il parametro *RequestedTPMState* del metodo [**RequestTPMStateChange**](cim-tpm-requesttpmstatechange.md) .</span><span class="sxs-lookup"><span data-stu-id="400f8-124">The possible values for the *RequestedTPMState* parameter of the [**RequestTPMStateChange**](cim-tpm-requesttpmstatechange.md) method.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="400f8-125">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="400f8-125">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="400f8-126">**S1 abilitato-di proprietà di Active** (2)</span><span class="sxs-lookup"><span data-stu-id="400f8-126">**S1 Enabled-Active-Owned** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="400f8-127">**S2 disabilitato-di proprietà di Active** (3)</span><span class="sxs-lookup"><span data-stu-id="400f8-127">**S2 Disabled-Active-Owned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="400f8-128">**S3 abilitato-inattivo-di proprietà** (4)</span><span class="sxs-lookup"><span data-stu-id="400f8-128">**S3 Enabled-Inactive-Owned** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="400f8-129">**S4 disabilitato-proprietà inattiva** (5)</span><span class="sxs-lookup"><span data-stu-id="400f8-129">**S4 Disabled-Inactive-Owned** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="400f8-130">**S5 abilitato-attivo-senza proprietario** (6)</span><span class="sxs-lookup"><span data-stu-id="400f8-130">**S5 Enabled-Active-Unowned** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="400f8-131">**S6 disabilitato-attivo-senza proprietario** (7)</span><span class="sxs-lookup"><span data-stu-id="400f8-131">**S6 Disabled-Active-Unowned** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="400f8-132">**S7 abilitato-inattivo-senza proprietario** (8)</span><span class="sxs-lookup"><span data-stu-id="400f8-132">**S7 Enabled-Inactive-Unowned** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="400f8-133">**S8 disabilitato-inattivo-non di proprietà** (9)</span><span class="sxs-lookup"><span data-stu-id="400f8-133">**S8 Disabled-Inactive-Unowned** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="400f8-134">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="400f8-134">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="400f8-135">**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="400f8-135">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="400f8-136">**TPMManafucturerMajorRevision**</span><span class="sxs-lookup"><span data-stu-id="400f8-136">**TPMManafucturerMajorRevision**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="400f8-137">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="400f8-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="400f8-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="400f8-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="400f8-139">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| part 2 v1dot2 \| Section 5,3 \| versione \| revMajor ")</span><span class="sxs-lookup"><span data-stu-id="400f8-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 5.3\|version\|revMajor")</span></span>
</dt> </dl>

<span data-ttu-id="400f8-140">Revisione principale del produttore del TPM.</span><span class="sxs-lookup"><span data-stu-id="400f8-140">The manufacturer major revision of the TPM.</span></span>

</dd> <dt>

<span data-ttu-id="400f8-141">**TPMManufacturerId**</span><span class="sxs-lookup"><span data-stu-id="400f8-141">**TPMManufacturerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="400f8-142">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="400f8-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="400f8-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="400f8-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="400f8-144">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| part 2 v1dot2 \| section 21,6 \| TPM \_ Cap \_ version \_ info \| tpmVendorID ")</span><span class="sxs-lookup"><span data-stu-id="400f8-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 21.6\|TPM\_CAP\_VERSION\_INFO\|tpmVendorID")</span></span>
</dt> </dl>

<span data-ttu-id="400f8-145">ID del produttore del TPM.</span><span class="sxs-lookup"><span data-stu-id="400f8-145">The TPM manufacturer ID.</span></span>

</dd> <dt>

<span data-ttu-id="400f8-146">**TPMManufacturerInfo**</span><span class="sxs-lookup"><span data-stu-id="400f8-146">**TPMManufacturerInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="400f8-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="400f8-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="400f8-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="400f8-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="400f8-149">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| part 2 v 1.2. TCG \| section 21,6 \| TPM \_ Cap \_ version \_ info \| vendorSpecific ")</span><span class="sxs-lookup"><span data-stu-id="400f8-149">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1.2.TCG\|Section 21.6\|TPM\_CAP\_VERSION\_INFO\|vendorSpecific")</span></span>
</dt> </dl>

<span data-ttu-id="400f8-150">Informazioni aggiuntive definite dal produttore del TPM.</span><span class="sxs-lookup"><span data-stu-id="400f8-150">The additional information defined by the TPM manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="400f8-151">**TPMManufacturerMinorRevision**</span><span class="sxs-lookup"><span data-stu-id="400f8-151">**TPMManufacturerMinorRevision**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="400f8-152">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="400f8-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="400f8-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="400f8-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="400f8-154">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| part 2 v1dot2 \| Section 5,3 \| versione \| revMinor ")</span><span class="sxs-lookup"><span data-stu-id="400f8-154">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 5.3\|version\|revMinor")</span></span>
</dt> </dl>

<span data-ttu-id="400f8-155">Revisione secondaria del produttore del TPM.</span><span class="sxs-lookup"><span data-stu-id="400f8-155">The manufacturer minor revision of the TPM.</span></span>

</dd> <dt>

<span data-ttu-id="400f8-156">**TPMSpecMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="400f8-156">**TPMSpecMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="400f8-157">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="400f8-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="400f8-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="400f8-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="400f8-159">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| part 2 v1dot2 \| Section 5,3 \| versione \| principale "," TSS. \|Sezione 2.3.2.18 di TCG Level 1 v 1.2 \| ")</span><span class="sxs-lookup"><span data-stu-id="400f8-159">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 5.3\|version\|major", "TSS.TCG\|Level 1 v1.2\|Section 2.3.2.18")</span></span>
</dt> </dl>

<span data-ttu-id="400f8-160">Versione principale del TPM.</span><span class="sxs-lookup"><span data-stu-id="400f8-160">The major version of the TPM.</span></span>

</dd> <dt>

<span data-ttu-id="400f8-161">**TPMSpecMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="400f8-161">**TPMSpecMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="400f8-162">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="400f8-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="400f8-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="400f8-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="400f8-164">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| part 2 v1dot2 \| sezione 5,3 \| versione \| secondaria "," TSS. \|Sezione 2.3.2.18 di TCG Level 1 v 1.2 \| ")</span><span class="sxs-lookup"><span data-stu-id="400f8-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 5.3\|version\|minor", "TSS.TCG\|Level 1 v1.2\|Section 2.3.2.18")</span></span>
</dt> </dl>

<span data-ttu-id="400f8-165">Versione secondaria del TPM.</span><span class="sxs-lookup"><span data-stu-id="400f8-165">The minor version of the TPM.</span></span>

</dd> <dt>

<span data-ttu-id="400f8-166">**TPMState**</span><span class="sxs-lookup"><span data-stu-id="400f8-166">**TPMState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="400f8-167">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="400f8-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="400f8-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="400f8-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="400f8-169">Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| Part 1 v1dot2 \| section 9,4 "," TPM. TCG \| part 2 v1dot2 \| Section 7,1 \| \_ flag permanenti TPM \_ "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ TPM**.**RequestTPMStateChange**","**CIM \_ TPM**.**TransitioningToTPMState**")</span><span class="sxs-lookup"><span data-stu-id="400f8-169">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 1 v1dot2\|Section 9.4", "TPM.TCG\|Part 2 v1dot2\|Section 7.1\|TPM\_PERMANENT\_FLAGS"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_TPM**.**RequestTPMStateChange**", "**CIM\_TPM**.**TransitioningToTPMState**")</span></span>
</dt> </dl>

<span data-ttu-id="400f8-170">Stato operativo del TPM.</span><span class="sxs-lookup"><span data-stu-id="400f8-170">The operational state of the TPM.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="400f8-171">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="400f8-171">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="400f8-172">**S1 abilitato-di proprietà di Active** (2)</span><span class="sxs-lookup"><span data-stu-id="400f8-172">**S1 Enabled-Active-Owned** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="400f8-173">**S2 disabilitato-di proprietà di Active** (3)</span><span class="sxs-lookup"><span data-stu-id="400f8-173">**S2 Disabled-Active-Owned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="400f8-174">**S3 abilitato-inattivo-di proprietà** (4)</span><span class="sxs-lookup"><span data-stu-id="400f8-174">**S3 Enabled-Inactive-Owned** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="400f8-175">**S4 disabilitato-proprietà inattiva** (5)</span><span class="sxs-lookup"><span data-stu-id="400f8-175">**S4 Disabled-Inactive-Owned** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="400f8-176">**S5 abilitato-attivo-senza proprietario** (6)</span><span class="sxs-lookup"><span data-stu-id="400f8-176">**S5 Enabled-Active-Unowned** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="400f8-177">**S6 disabilitato-attivo-senza proprietario** (7)</span><span class="sxs-lookup"><span data-stu-id="400f8-177">**S6 Disabled-Active-Unowned** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="400f8-178">**S7 abilitato-inattivo-senza proprietario** (8)</span><span class="sxs-lookup"><span data-stu-id="400f8-178">**S7 Enabled-Inactive-Unowned** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="400f8-179">**S8 disabilitato-inattivo-non di proprietà** (9)</span><span class="sxs-lookup"><span data-stu-id="400f8-179">**S8 Disabled-Inactive-Unowned** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="400f8-180">**Non applicabile** (10)</span><span class="sxs-lookup"><span data-stu-id="400f8-180">**Not Applicable** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="400f8-181">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="400f8-181">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="400f8-182">**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="400f8-182">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="400f8-183">**TransitioningToTPMState**</span><span class="sxs-lookup"><span data-stu-id="400f8-183">**TransitioningToTPMState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="400f8-184">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="400f8-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="400f8-185">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="400f8-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="400f8-186">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ TPM**.**RequestTPMStateChange**","**CIM \_ TPM**.**TPMState**")</span><span class="sxs-lookup"><span data-stu-id="400f8-186">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_TPM**.**RequestTPMStateChange**", "**CIM\_TPM**.**TPMState**")</span></span>
</dt> </dl>

<span data-ttu-id="400f8-187">Stato di destinazione a cui è in corso la transizione del TPM.</span><span class="sxs-lookup"><span data-stu-id="400f8-187">The target state to which the TPM is transitioning.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="400f8-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="400f8-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="400f8-189"><span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>**S1 abilitato-di proprietà di Active** (2)</span><span class="sxs-lookup"><span data-stu-id="400f8-189"><span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>**S1 Enabled-Active-Owned** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="400f8-190"><span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>**S2 disabilitato-di proprietà di Active** (3)</span><span class="sxs-lookup"><span data-stu-id="400f8-190"><span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>**S2 Disabled-Active-Owned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="400f8-191"><span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>**S3 abilitato-inattivo-di proprietà** (4)</span><span class="sxs-lookup"><span data-stu-id="400f8-191"><span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>**S3 Enabled-Inactive-Owned** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="400f8-192"><span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>**S4 disabilitato-proprietà inattiva** (5)</span><span class="sxs-lookup"><span data-stu-id="400f8-192"><span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>**S4 Disabled-Inactive-Owned** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="400f8-193"><span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>**S5 abilitato-attivo-senza proprietario** (6)</span><span class="sxs-lookup"><span data-stu-id="400f8-193"><span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>**S5 Enabled-Active-Unowned** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="400f8-194"><span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>**S6 disabilitato-attivo-senza proprietario** (7)</span><span class="sxs-lookup"><span data-stu-id="400f8-194"><span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>**S6 Disabled-Active-Unowned** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="400f8-195"><span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>**S7 abilitato-inattivo-senza proprietario** (8)</span><span class="sxs-lookup"><span data-stu-id="400f8-195"><span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>**S7 Enabled-Inactive-Unowned** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="400f8-196"><span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>**S8 disabilitato-inattivo-non di proprietà** (9)</span><span class="sxs-lookup"><span data-stu-id="400f8-196"><span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>**S8 Disabled-Inactive-Unowned** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="400f8-197"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Non applicabile** (10)</span><span class="sxs-lookup"><span data-stu-id="400f8-197"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

<span data-ttu-id="400f8-198"><span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>**Nessuna modifica** (11)</span><span class="sxs-lookup"><span data-stu-id="400f8-198"><span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>**No Change** (11)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="400f8-199">12</span><span class="sxs-lookup"><span data-stu-id="400f8-199">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="400f8-200"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="400f8-200"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="400f8-201"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="400f8-201"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="400f8-202"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="400f8-202"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="400f8-203">Requisiti</span><span class="sxs-lookup"><span data-stu-id="400f8-203">Requirements</span></span>



| <span data-ttu-id="400f8-204">Requisito</span><span class="sxs-lookup"><span data-stu-id="400f8-204">Requirement</span></span> | <span data-ttu-id="400f8-205">Valore</span><span class="sxs-lookup"><span data-stu-id="400f8-205">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="400f8-206">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="400f8-206">Minimum supported client</span></span><br/> | <span data-ttu-id="400f8-207">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="400f8-207">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="400f8-208">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="400f8-208">Minimum supported server</span></span><br/> | <span data-ttu-id="400f8-209">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="400f8-209">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="400f8-210">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="400f8-210">Namespace</span></span><br/>                | <span data-ttu-id="400f8-211">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="400f8-211">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="400f8-212">MOF</span><span class="sxs-lookup"><span data-stu-id="400f8-212">MOF</span></span><br/>                      | <dl> <span data-ttu-id="400f8-213"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="400f8-213"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="400f8-214">DLL</span><span class="sxs-lookup"><span data-stu-id="400f8-214">DLL</span></span><br/>                      | <dl> <span data-ttu-id="400f8-215"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="400f8-215"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="400f8-216">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="400f8-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="400f8-217">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="400f8-217">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 


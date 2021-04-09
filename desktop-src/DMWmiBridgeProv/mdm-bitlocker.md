---
title: Classe MDM_BitLocker
description: La \_ classe BITLOCKER MDM viene usata dall'azienda per gestire la crittografia di PC e dispositivi.
ms.assetid: e8bea6dc-8d3d-46d2-b2e3-9a4c547a639f
keywords:
- Classe MDM_BitLocker
- Classe MDM_BitLocker, descritta
topic_type:
- apiref
api_name:
- MDM_BitLocker
- MDM_BitLocker.InstanceID
- MDM_BitLocker.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b94db491333cada64b6287dc87ec233b420bf0f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121410"
---
# <a name="mdm_bitlocker-class"></a><span data-ttu-id="64b6a-105">\_Classe BITLOCKER MDM</span><span class="sxs-lookup"><span data-stu-id="64b6a-105">MDM\_BitLocker class</span></span>

<span data-ttu-id="64b6a-106">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="64b6a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="64b6a-107">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="64b6a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="64b6a-108">La \_ classe BITLOCKER MDM viene usata dall'azienda per gestire la crittografia di PC e dispositivi.</span><span class="sxs-lookup"><span data-stu-id="64b6a-108">The MDM\_BitLocker class is used by the enterprise to manage encryption of PCs and devices.</span></span>

<span data-ttu-id="64b6a-109">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="64b6a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="64b6a-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="64b6a-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_BitLocker
{
  string InstanceID;
  string ParentID;
  sint32 RequireStorageCardEncryption;
  sint32 RequireDeviceEncryption;
  string EncryptionMethodByDriveType;
  string SystemDrivesRequireStartupAuthentication;
  string SystemDrivesMinimumPINLength;
  string SystemDrivesRecoveryMessage;
  string SystemDrivesRecoveryOptions;
  string FixedDrivesRecoveryOptions;
  string FixedDrivesRequireEncryption;
  string RemovableDrivesRequireEncryption;
  sint32 AllowWarningForOtherDiskEncryption;
};
```

## <a name="members"></a><span data-ttu-id="64b6a-111">Members</span><span class="sxs-lookup"><span data-stu-id="64b6a-111">Members</span></span>

<span data-ttu-id="64b6a-112">La **classe \_ BitLocker di MDM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="64b6a-112">The **MDM\_BitLocker** class has these types of members:</span></span>

-   [<span data-ttu-id="64b6a-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="64b6a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="64b6a-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="64b6a-114">Properties</span></span>

<span data-ttu-id="64b6a-115">La **classe \_ BitLocker di MDM** presenta queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="64b6a-115">The **MDM\_BitLocker** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="64b6a-116">AllowWarningForOtherDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="64b6a-116">AllowWarningForOtherDiskEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#allowwarningforotherdiskencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="64b6a-117">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="64b6a-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="64b6a-118">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="64b6a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="64b6a-119">EncryptionMethodByDriveType</span><span class="sxs-lookup"><span data-stu-id="64b6a-119">EncryptionMethodByDriveType</span></span>](/windows/client-management/mdm/bitlocker-csp#encryptionmethodbydrivetype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="64b6a-120">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="64b6a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64b6a-121">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="64b6a-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="64b6a-122">FixedDrivesRecoveryOptions</span><span class="sxs-lookup"><span data-stu-id="64b6a-122">FixedDrivesRecoveryOptions</span></span>](/windows/client-management/mdm/bitlocker-csp#fixeddrivesrecoveryoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="64b6a-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="64b6a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64b6a-124">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="64b6a-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="64b6a-125">FixedDrivesRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="64b6a-125">FixedDrivesRequireEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#fixeddrivesrequireencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="64b6a-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="64b6a-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64b6a-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="64b6a-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="64b6a-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="64b6a-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64b6a-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="64b6a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64b6a-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64b6a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64b6a-131">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="64b6a-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="64b6a-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="64b6a-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="64b6a-133">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="64b6a-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64b6a-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="64b6a-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="64b6a-135">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="64b6a-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="64b6a-136">RemovableDrivesRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="64b6a-136">RemovableDrivesRequireEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#removabledrivesrequireencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="64b6a-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="64b6a-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64b6a-138">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="64b6a-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="64b6a-139">RequireDeviceEncryption</span><span class="sxs-lookup"><span data-stu-id="64b6a-139">RequireDeviceEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#requiredeviceencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="64b6a-140">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="64b6a-140">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="64b6a-141">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="64b6a-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="64b6a-142">RequireStorageCardEncryption</span><span class="sxs-lookup"><span data-stu-id="64b6a-142">RequireStorageCardEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#requirestoragecardencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="64b6a-143">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="64b6a-143">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="64b6a-144">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="64b6a-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="64b6a-145">SystemDrivesMinimumPINLength</span><span class="sxs-lookup"><span data-stu-id="64b6a-145">SystemDrivesMinimumPINLength</span></span>](/windows/client-management/mdm/bitlocker-csp#systemdrivesminimumpinlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="64b6a-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="64b6a-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64b6a-147">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="64b6a-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="64b6a-148">SystemDrivesRecoveryMessage</span><span class="sxs-lookup"><span data-stu-id="64b6a-148">SystemDrivesRecoveryMessage</span></span>](/windows/client-management/mdm/bitlocker-csp#systemdrivesrecoverymessage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="64b6a-149">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="64b6a-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64b6a-150">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="64b6a-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="64b6a-151">SystemDrivesRecoveryOptions</span><span class="sxs-lookup"><span data-stu-id="64b6a-151">SystemDrivesRecoveryOptions</span></span>](/windows/client-management/mdm/bitlocker-csp#systemdrivesrecoveryoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="64b6a-152">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="64b6a-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64b6a-153">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="64b6a-153">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="64b6a-154">SystemDrivesRequireStartupAuthentication</span><span class="sxs-lookup"><span data-stu-id="64b6a-154">SystemDrivesRequireStartupAuthentication</span></span>](/windows/client-management/mdm/bitlocker-csp#systemdrivesrequirestartupauthentication)
</dt> <dd> <dl> <dt>

<span data-ttu-id="64b6a-155">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="64b6a-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="64b6a-156">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="64b6a-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="64b6a-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64b6a-157">Requirements</span></span>



| <span data-ttu-id="64b6a-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="64b6a-158">Requirement</span></span> | <span data-ttu-id="64b6a-159">Valore</span><span class="sxs-lookup"><span data-stu-id="64b6a-159">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64b6a-160">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64b6a-160">Minimum supported client</span></span><br/> | <span data-ttu-id="64b6a-161">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="64b6a-161">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="64b6a-162">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64b6a-162">Minimum supported server</span></span><br/> | <span data-ttu-id="64b6a-163">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="64b6a-163">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="64b6a-164">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="64b6a-164">Namespace</span></span><br/>                | <span data-ttu-id="64b6a-165">\\ \\ Dmmap MDM CIMV2 \\ radice</span><span class="sxs-lookup"><span data-stu-id="64b6a-165">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="64b6a-166">MOF</span><span class="sxs-lookup"><span data-stu-id="64b6a-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64b6a-167"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="64b6a-167"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="64b6a-168">DLL</span><span class="sxs-lookup"><span data-stu-id="64b6a-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64b6a-169"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64b6a-169"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 


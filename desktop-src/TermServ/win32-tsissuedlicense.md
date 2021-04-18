---
title: Classe Win32_TSIssuedLicense
description: Descrive le istanze di Servizi Desktop remoto licenze di accesso client per dispositivo (RDS \ 160; Licenze CAL per dispositivo rilasciate da un server licenze Desktop remoto.
ms.assetid: 15825dc5-9ada-4c11-ac77-beb681e9b33c
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSIssuedLicense Servizi Desktop remoto
- Classe Win32_TSIssuedLicense Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSIssuedLicense
- Win32_TSIssuedLicense.LicenseId
- Win32_TSIssuedLicense.KeyPackId
- Win32_TSIssuedLicense.sIssuedToUser
- Win32_TSIssuedLicense.sIssuedToComputer
- Win32_TSIssuedLicense.LicenseStatus
- Win32_TSIssuedLicense.IssueDate
- Win32_TSIssuedLicense.ExpirationDate
- Win32_TSIssuedLicense.sHardwareId
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c3d08a68ddcc15a912de4c674403928211a297e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301740"
---
# <a name="win32_tsissuedlicense-class"></a><span data-ttu-id="b3100-105">Win32 \_ TSIssuedLicense (classe)</span><span class="sxs-lookup"><span data-stu-id="b3100-105">Win32\_TSIssuedLicense class</span></span>

<span data-ttu-id="b3100-106">Vengono descritte le istanze delle licenze CAL per dispositivo Servizi Desktop remoto per dispositivo che vengono rilasciate da un server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="b3100-106">Describes instances of Remote Desktop Services Per Device client access licenses (RDS Per Device CALs) that are issued from a Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3100-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3100-107">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSIssuedLicense
{
  uint32   LicenseId;
  uint32   KeyPackId;
  string   sIssuedToUser;
  string   sIssuedToComputer;
  uint32   LicenseStatus;
  DATETIME IssueDate;
  DATETIME ExpirationDate;
  string   sHardwareId;
};
```

## <a name="members"></a><span data-ttu-id="b3100-108">Members</span><span class="sxs-lookup"><span data-stu-id="b3100-108">Members</span></span>

<span data-ttu-id="b3100-109">La classe **Win32 \_ TSIssuedLicense** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b3100-109">The **Win32\_TSIssuedLicense** class has these types of members:</span></span>

-   [<span data-ttu-id="b3100-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="b3100-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="b3100-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b3100-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b3100-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="b3100-112">Methods</span></span>

<span data-ttu-id="b3100-113">La classe **Win32 \_ TSIssuedLicense** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b3100-113">The **Win32\_TSIssuedLicense** class has these methods.</span></span>



| <span data-ttu-id="b3100-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="b3100-114">Method</span></span>                                         | <span data-ttu-id="b3100-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3100-115">Description</span></span>                                                                                               |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b3100-116">**Revoke**</span><span class="sxs-lookup"><span data-stu-id="b3100-116">**Revoke**</span></span>](revoke-win32-tsissuedlicense.md) | <span data-ttu-id="b3100-117">Revoca le licenze CAL per dispositivo di Servizi Desktop remoto rappresentate dall'oggetto **Win32 \_ TSIssuedLicense** .</span><span class="sxs-lookup"><span data-stu-id="b3100-117">Revokes the RDS Per Device CALs that are represented by the **Win32\_TSIssuedLicense** object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b3100-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b3100-118">Properties</span></span>

<span data-ttu-id="b3100-119">La classe **Win32 \_ TSIssuedLicense** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b3100-119">The **Win32\_TSIssuedLicense** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b3100-120">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="b3100-120">**ExpirationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3100-121">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b3100-121">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="b3100-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b3100-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b3100-123">Identifica la data di scadenza della licenza.</span><span class="sxs-lookup"><span data-stu-id="b3100-123">Identifies the date that the license will expire.</span></span>

</dd> <dt>

<span data-ttu-id="b3100-124">**IssueDate**</span><span class="sxs-lookup"><span data-stu-id="b3100-124">**IssueDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3100-125">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b3100-125">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="b3100-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b3100-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b3100-127">Identifica la data di rilascio della licenza.</span><span class="sxs-lookup"><span data-stu-id="b3100-127">Identifies the date that the license was issued.</span></span>

</dd> <dt>

<span data-ttu-id="b3100-128">**KeyPackId**</span><span class="sxs-lookup"><span data-stu-id="b3100-128">**KeyPackId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3100-129">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b3100-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3100-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b3100-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3100-131">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b3100-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b3100-132">Identifica il Key Pack di Servizi Desktop remoto License.</span><span class="sxs-lookup"><span data-stu-id="b3100-132">Identifies the Remote Desktop Services license key pack.</span></span>

</dd> <dt>

<span data-ttu-id="b3100-133">**LicenseId**</span><span class="sxs-lookup"><span data-stu-id="b3100-133">**LicenseId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3100-134">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b3100-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3100-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b3100-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3100-136">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b3100-136">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b3100-137">Identificatore univoco per questa licenza.</span><span class="sxs-lookup"><span data-stu-id="b3100-137">Unique identifier for this license.</span></span>

</dd> <dt>

<span data-ttu-id="b3100-138">**LicenseStatus**</span><span class="sxs-lookup"><span data-stu-id="b3100-138">**LicenseStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3100-139">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b3100-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b3100-140">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b3100-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b3100-141">Stato della licenza.</span><span class="sxs-lookup"><span data-stu-id="b3100-141">Status of the license.</span></span>

<dt>

<span data-ttu-id="b3100-142">0</span><span class="sxs-lookup"><span data-stu-id="b3100-142">0</span></span>
</dt> <dd>

<span data-ttu-id="b3100-143">Lo stato della licenza è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="b3100-143">The license status is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="b3100-144">1</span><span class="sxs-lookup"><span data-stu-id="b3100-144">1</span></span>
</dt> <dd>

<span data-ttu-id="b3100-145">La licenza è una licenza temporanea.</span><span class="sxs-lookup"><span data-stu-id="b3100-145">The license is a temporary license.</span></span>

</dd> <dt>

<span data-ttu-id="b3100-146">2</span><span class="sxs-lookup"><span data-stu-id="b3100-146">2</span></span>
</dt> <dd>

<span data-ttu-id="b3100-147">La licenza è attiva.</span><span class="sxs-lookup"><span data-stu-id="b3100-147">The license is active.</span></span>

</dd> <dt>

<span data-ttu-id="b3100-148">3</span><span class="sxs-lookup"><span data-stu-id="b3100-148">3</span></span>
</dt> <dd>

<span data-ttu-id="b3100-149">La licenza è una licenza per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="b3100-149">The license is an upgrade license.</span></span>

</dd> <dt>

<span data-ttu-id="b3100-150">4</span><span class="sxs-lookup"><span data-stu-id="b3100-150">4</span></span>
</dt> <dd>

<span data-ttu-id="b3100-151">La licenza è stata revocata.</span><span class="sxs-lookup"><span data-stu-id="b3100-151">The license has been revoked.</span></span>

</dd> <dt>

<span data-ttu-id="b3100-152">5</span><span class="sxs-lookup"><span data-stu-id="b3100-152">5</span></span>
</dt> <dd>

<span data-ttu-id="b3100-153">Lo stato della licenza è in sospeso.</span><span class="sxs-lookup"><span data-stu-id="b3100-153">The license status is pending.</span></span>

</dd> <dt>

<span data-ttu-id="b3100-154">6</span><span class="sxs-lookup"><span data-stu-id="b3100-154">6</span></span>
</dt> <dd>

<span data-ttu-id="b3100-155">La licenza è una licenza simultanea.</span><span class="sxs-lookup"><span data-stu-id="b3100-155">The license is a concurrent license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b3100-156">**sHardwareId**</span><span class="sxs-lookup"><span data-stu-id="b3100-156">**sHardwareId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3100-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b3100-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3100-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b3100-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b3100-159">Identificatore hardware per il quale è stata emessa la licenza.</span><span class="sxs-lookup"><span data-stu-id="b3100-159">Hardware identifier for which the license was issued.</span></span>

</dd> <dt>

<span data-ttu-id="b3100-160">**sIssuedToComputer**</span><span class="sxs-lookup"><span data-stu-id="b3100-160">**sIssuedToComputer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3100-161">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b3100-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3100-162">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b3100-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b3100-163">Nome del computer per cui è stata emessa la licenza.</span><span class="sxs-lookup"><span data-stu-id="b3100-163">Computer name for which the license was issued.</span></span>

</dd> <dt>

<span data-ttu-id="b3100-164">**sIssuedToUser**</span><span class="sxs-lookup"><span data-stu-id="b3100-164">**sIssuedToUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3100-165">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b3100-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3100-166">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b3100-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b3100-167">Nome utente per cui è stata emessa la licenza.</span><span class="sxs-lookup"><span data-stu-id="b3100-167">User name for which the license was issued.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3100-168">Commenti</span><span class="sxs-lookup"><span data-stu-id="b3100-168">Remarks</span></span>

<span data-ttu-id="b3100-169">Per utilizzare questa classe, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="b3100-169">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="b3100-170">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b3100-170">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b3100-171">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="b3100-171">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b3100-172">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="b3100-172">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b3100-173">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b3100-173">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3100-174">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3100-174">Requirements</span></span>



| <span data-ttu-id="b3100-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3100-175">Requirement</span></span> | <span data-ttu-id="b3100-176">Valore</span><span class="sxs-lookup"><span data-stu-id="b3100-176">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3100-177">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3100-177">Minimum supported client</span></span><br/> | <span data-ttu-id="b3100-178">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b3100-178">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="b3100-179">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3100-179">Minimum supported server</span></span><br/> | <span data-ttu-id="b3100-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b3100-180">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="b3100-181">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b3100-181">Namespace</span></span><br/>                | <span data-ttu-id="b3100-182">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="b3100-182">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="b3100-183">MOF</span><span class="sxs-lookup"><span data-stu-id="b3100-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3100-184"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b3100-184"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3100-185">DLL</span><span class="sxs-lookup"><span data-stu-id="b3100-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3100-186"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3100-186"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3100-187">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3100-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3100-188">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="b3100-188">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> <dt>

[<span data-ttu-id="b3100-189">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="b3100-189">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="b3100-190">**\_TSLicenseReportEntry Win32**</span><span class="sxs-lookup"><span data-stu-id="b3100-190">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> <dt>

[<span data-ttu-id="b3100-191">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="b3100-191">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 


---
title: Classe Win32_TSLicenseReport
description: Fornisce istanze di Servizi Desktop remoto licenza di accesso client per utente (RDS \ 160; Report sull'utilizzo di licenze CAL per utente) generate nel server licenze Desktop remoto e metodi per le operazioni di generazione, recupero ed eliminazione dei report delle licenze.
ms.assetid: 8d67f158-cda3-4cf4-a766-09d08c21c49e
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSLicenseReport Servizi Desktop remoto
- Classe Win32_TSLicenseReport Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport
- Win32_TSLicenseReport.FileName
- Win32_TSLicenseReport.LicenseUsageCount
- Win32_TSLicenseReport.InstalledLicenses
- Win32_TSLicenseReport.GenerationDateTime
- Win32_TSLicenseReport.ScopeType
- Win32_TSLicenseReport.ScopeValue
- Win32_TSLicenseReport.Version
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de997056222c1b525253f320f6fe191f017614f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873405"
---
# <a name="win32_tslicensereport-class"></a><span data-ttu-id="87a0f-105">Win32 \_ TSLicenseReport (classe)</span><span class="sxs-lookup"><span data-stu-id="87a0f-105">Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="87a0f-106">Fornisce istanze di Servizi Desktop remoto report sull'utilizzo della licenza di accesso client per utente (RDS per utente CAL) generati nel server licenze Desktop remoto, nonché i metodi per le operazioni di generazione, recupero ed eliminazione dei report delle licenze.</span><span class="sxs-lookup"><span data-stu-id="87a0f-106">Provides instances of Remote Desktop Services Per User client access license (RDS Per User CAL) usage reports that are generated on the Remote Desktop license server, and methods for license report generation, fetch, and delete operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="87a0f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87a0f-107">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseReport
{
  string   FileName;
  uint32   LicenseUsageCount;
  uint32   InstalledLicenses;
  DATETIME GenerationDateTime;
  uint32   ScopeType;
  string   ScopeValue;
  uint32   Version;
};
```

## <a name="members"></a><span data-ttu-id="87a0f-108">Members</span><span class="sxs-lookup"><span data-stu-id="87a0f-108">Members</span></span>

<span data-ttu-id="87a0f-109">La classe **Win32 \_ TSLicenseReport** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="87a0f-109">The **Win32\_TSLicenseReport** class has these types of members:</span></span>

-   [<span data-ttu-id="87a0f-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="87a0f-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="87a0f-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="87a0f-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="87a0f-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="87a0f-112">Methods</span></span>

<span data-ttu-id="87a0f-113">La classe **Win32 \_ TSLicenseReport** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="87a0f-113">The **Win32\_TSLicenseReport** class has these methods.</span></span>



| <span data-ttu-id="87a0f-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="87a0f-114">Method</span></span>                                                                                                         | <span data-ttu-id="87a0f-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87a0f-115">Description</span></span>                                                                                                                                                                                     |
|:---------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="87a0f-116">**DeleteReport**</span><span class="sxs-lookup"><span data-stu-id="87a0f-116">**DeleteReport**</span></span>](deletereport-win32-tslicensereport.md)                                                     | <span data-ttu-id="87a0f-117">Elimina un oggetto report nel server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="87a0f-117">Deletes a report object on the Remote Desktop license server.</span></span> <span data-ttu-id="87a0f-118">Non si tratta di un metodo statico.</span><span class="sxs-lookup"><span data-stu-id="87a0f-118">This is not a static method.</span></span><br/>                                                                                           |
| [<span data-ttu-id="87a0f-119">**FetchReportEntries**</span><span class="sxs-lookup"><span data-stu-id="87a0f-119">**FetchReportEntries**</span></span>](fetchreportentries-win32-tslicensereport.md)                                         | <span data-ttu-id="87a0f-120">Recupera le voci nell'oggetto report.</span><span class="sxs-lookup"><span data-stu-id="87a0f-120">Retrieves entries in the report object.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="87a0f-121">**FetchReportFailedPerUserEntries**</span><span class="sxs-lookup"><span data-stu-id="87a0f-121">**FetchReportFailedPerUserEntries**</span></span>](fetchreportfailedperuserentries-win32-tslicensereport.md)               | <span data-ttu-id="87a0f-122">Recupera i dettagli relativi alle licenze CAL per utente non riuscite Servizi Desktop remoto per utente dal report.</span><span class="sxs-lookup"><span data-stu-id="87a0f-122">Retrieves details of failed Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span><br/>                                                             |
| [<span data-ttu-id="87a0f-123">**FetchReportFailedPerUserSummaryEntries**</span><span class="sxs-lookup"><span data-stu-id="87a0f-123">**FetchReportFailedPerUserSummaryEntries**</span></span>](fetchreportfailedperusersummaryentries-win32-tslicensereport.md) | <span data-ttu-id="87a0f-124">Recupera le informazioni di riepilogo di Servizi Desktop remoto non riuscite per licenze CAL per utente per utente dal report.</span><span class="sxs-lookup"><span data-stu-id="87a0f-124">Retrieves summary information of failed Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span><br/>                                                 |
| [<span data-ttu-id="87a0f-125">**FetchReportPerDeviceEntries**</span><span class="sxs-lookup"><span data-stu-id="87a0f-125">**FetchReportPerDeviceEntries**</span></span>](fetchreportperdeviceentries-win32-tslicensereport.md)                       | <span data-ttu-id="87a0f-126">Recupera le informazioni sulle licenze di accesso client per dispositivo di Servizi Desktop remoto emesse dal report.</span><span class="sxs-lookup"><span data-stu-id="87a0f-126">Retrieves information of issued Remote Desktop Services Per Device client access licenses (RDS Per Device CALs) from the report.</span></span><br/>                                                     |
| [<span data-ttu-id="87a0f-127">**FetchReportSummaryEntries**</span><span class="sxs-lookup"><span data-stu-id="87a0f-127">**FetchReportSummaryEntries**</span></span>](win32-tslicensereport-fetchreportsummaryentries.md)                           | <span data-ttu-id="87a0f-128">Recupera i riepiloghi delle licenze dall'oggetto report.</span><span class="sxs-lookup"><span data-stu-id="87a0f-128">Retrieves license summaries from the report object.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="87a0f-129">**GenerateReport**</span><span class="sxs-lookup"><span data-stu-id="87a0f-129">**GenerateReport**</span></span>](generatereport-win32-tslicensereport.md)                                                 | <span data-ttu-id="87a0f-130">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="87a0f-130">This method is not supported.</span></span><br/> <span data-ttu-id="87a0f-131">**Windows server 2008 R2 e Windows server 2008:** Genera un report di utilizzo delle licenze per utente corrente nel server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="87a0f-131">**Windows Server 2008 R2 and Windows Server 2008:** Generates a current per user license usage report on the Remote Desktop license server.</span></span><br/> |
| [<span data-ttu-id="87a0f-132">**GenerateReportEx**</span><span class="sxs-lookup"><span data-stu-id="87a0f-132">**GenerateReportEx**</span></span>](generatereportex-win32-tslicensereport.md)                                             | <span data-ttu-id="87a0f-133">Genera un report di utilizzo delle licenze per utente corrente nel server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="87a0f-133">Generates a current per user license usage report on the Remote Desktop license server.</span></span><br/>                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="87a0f-134">Proprietà</span><span class="sxs-lookup"><span data-stu-id="87a0f-134">Properties</span></span>

<span data-ttu-id="87a0f-135">La classe **Win32 \_ TSLicenseReport** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="87a0f-135">The **Win32\_TSLicenseReport** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="87a0f-136">**FileName**</span><span class="sxs-lookup"><span data-stu-id="87a0f-136">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87a0f-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="87a0f-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87a0f-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="87a0f-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87a0f-139">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="87a0f-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="87a0f-140">Nome del report.</span><span class="sxs-lookup"><span data-stu-id="87a0f-140">The report name.</span></span>

</dd> <dt>

<span data-ttu-id="87a0f-141">**GenerationDateTime**</span><span class="sxs-lookup"><span data-stu-id="87a0f-141">**GenerationDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87a0f-142">Tipo di dati: **[DateTime](/windows/desktop/WmiSdk/datetime)**</span><span class="sxs-lookup"><span data-stu-id="87a0f-142">Data type: **[DATETIME](/windows/desktop/WmiSdk/datetime)**</span></span>
</dt> <dt>

<span data-ttu-id="87a0f-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="87a0f-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87a0f-144">Data e ora di generazione del report di licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="87a0f-144">RD Licensing report generation date and time.</span></span>

</dd> <dt>

<span data-ttu-id="87a0f-145">**InstalledLicenses**</span><span class="sxs-lookup"><span data-stu-id="87a0f-145">**InstalledLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87a0f-146">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="87a0f-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="87a0f-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="87a0f-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87a0f-148">Qualificatori: [ **deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="87a0f-148">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="87a0f-149">Questa proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="87a0f-149">This property is not supported.</span></span>

<span data-ttu-id="87a0f-150">**Windows server 2008 R2 e Windows server 2008:** Numero di licenze CAL per utente di Servizi Desktop remoto installate.</span><span class="sxs-lookup"><span data-stu-id="87a0f-150">**Windows Server 2008 R2 and Windows Server 2008:** Number of RDS Per User CALs that are installed.</span></span>

</dd> <dt>

<span data-ttu-id="87a0f-151">**LicenseUsageCount**</span><span class="sxs-lookup"><span data-stu-id="87a0f-151">**LicenseUsageCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87a0f-152">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="87a0f-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="87a0f-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="87a0f-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87a0f-154">Qualificatori: [ **deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="87a0f-154">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="87a0f-155">Questa proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="87a0f-155">This property is not supported.</span></span>

<span data-ttu-id="87a0f-156">**Windows server 2008 R2 e Windows server 2008:** Numero di licenze CAL per utente per utente attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="87a0f-156">**Windows Server 2008 R2 and Windows Server 2008:** Number of RDS Per User CALs that are currently in use.</span></span>

</dd> <dt>

<span data-ttu-id="87a0f-157">**ScopeType**</span><span class="sxs-lookup"><span data-stu-id="87a0f-157">**ScopeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87a0f-158">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="87a0f-158">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="87a0f-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="87a0f-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87a0f-160">Qualificatori: [ **deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="87a0f-160">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="87a0f-161">Questa proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="87a0f-161">This property is not supported.</span></span>

<span data-ttu-id="87a0f-162">**Windows server 2008 R2 e Windows server 2008:** Tipo di ambito del report di licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="87a0f-162">**Windows Server 2008 R2 and Windows Server 2008:** RD Licensing report scope type.</span></span>

</dd> <dt>

<span data-ttu-id="87a0f-163">**ScopeValue**</span><span class="sxs-lookup"><span data-stu-id="87a0f-163">**ScopeValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87a0f-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="87a0f-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87a0f-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="87a0f-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87a0f-166">Qualificatori: [ **deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="87a0f-166">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="87a0f-167">Questa proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="87a0f-167">This property is not supported.</span></span>

<span data-ttu-id="87a0f-168">**Windows server 2008 R2 e Windows server 2008:** Valore dell'ambito del report di licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="87a0f-168">**Windows Server 2008 R2 and Windows Server 2008:** RD Licensing report scope value.</span></span>

</dd> <dt>

<span data-ttu-id="87a0f-169">**Versione**</span><span class="sxs-lookup"><span data-stu-id="87a0f-169">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87a0f-170">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="87a0f-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="87a0f-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="87a0f-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87a0f-172">Versione del report di licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="87a0f-172">RD Licensing report version.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87a0f-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="87a0f-173">Remarks</span></span>

<span data-ttu-id="87a0f-174">I report generati tramite WMI vengono visualizzati in gestione licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="87a0f-174">Reports that are generated by using WMI are displayed in RD Licensing Manager.</span></span> <span data-ttu-id="87a0f-175">Anche i report eliminati tramite WMI vengono eliminati da gestione licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="87a0f-175">Reports that are deleted by using WMI are also deleted from RD Licensing Manager.</span></span>

<span data-ttu-id="87a0f-176">Per utilizzare questa classe, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="87a0f-176">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="87a0f-177">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="87a0f-177">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="87a0f-178">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="87a0f-178">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="87a0f-179">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="87a0f-179">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="87a0f-180">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="87a0f-180">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="87a0f-181">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87a0f-181">Requirements</span></span>



| <span data-ttu-id="87a0f-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="87a0f-182">Requirement</span></span> | <span data-ttu-id="87a0f-183">Valore</span><span class="sxs-lookup"><span data-stu-id="87a0f-183">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="87a0f-184">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87a0f-184">Minimum supported client</span></span><br/> | <span data-ttu-id="87a0f-185">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="87a0f-185">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="87a0f-186">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87a0f-186">Minimum supported server</span></span><br/> | <span data-ttu-id="87a0f-187">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="87a0f-187">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="87a0f-188">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="87a0f-188">Namespace</span></span><br/>                | <span data-ttu-id="87a0f-189">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="87a0f-189">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="87a0f-190">MOF</span><span class="sxs-lookup"><span data-stu-id="87a0f-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87a0f-191"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="87a0f-191"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="87a0f-192">DLL</span><span class="sxs-lookup"><span data-stu-id="87a0f-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87a0f-193"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87a0f-193"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87a0f-194">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87a0f-194">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87a0f-195">**\_TSIssuedLicense Win32**</span><span class="sxs-lookup"><span data-stu-id="87a0f-195">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> <dt>

[<span data-ttu-id="87a0f-196">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="87a0f-196">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> <dt>

[<span data-ttu-id="87a0f-197">**\_TSLicenseReportEntry Win32**</span><span class="sxs-lookup"><span data-stu-id="87a0f-197">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> <dt>

[<span data-ttu-id="87a0f-198">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="87a0f-198">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 


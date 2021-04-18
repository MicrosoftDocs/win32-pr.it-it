---
title: Classe Win32_TSLicenseReportEntry
description: Fornisce i dettagli della licenza di accesso client per utente Servizi Desktop remoto pubblicata (RDS \ 160; CAL per utente).
ms.assetid: 75fa7f39-af5b-45a0-ba2b-5c667edfec16
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSLicenseReportEntry Servizi Desktop remoto
- Classe Win32_TSLicenseReportEntry Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportEntry
- Win32_TSLicenseReportEntry.User
- Win32_TSLicenseReportEntry.ExpirationDate
- Win32_TSLicenseReportEntry.CALType
- Win32_TSLicenseReportEntry.ProductVersion
- Win32_TSLicenseReportEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44fa97a91561a9d4cf3fd571c773288796754858
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400271"
---
# <a name="win32_tslicensereportentry-class"></a><span data-ttu-id="5ffb1-105">Win32 \_ TSLicenseReportEntry (classe)</span><span class="sxs-lookup"><span data-stu-id="5ffb1-105">Win32\_TSLicenseReportEntry class</span></span>

<span data-ttu-id="5ffb1-106">Fornisce i dettagli della licenza di accesso client per utente (CAL per utente) del Servizi Desktop remoto emesso.</span><span class="sxs-lookup"><span data-stu-id="5ffb1-106">Provides details of the issued Remote Desktop Services Per User client access license (RDS Per User CAL).</span></span>

## <a name="syntax"></a><span data-ttu-id="5ffb1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ffb1-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportEntry
{
  string   User;
  DATETIME ExpirationDate;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a><span data-ttu-id="5ffb1-108">Members</span><span class="sxs-lookup"><span data-stu-id="5ffb1-108">Members</span></span>

<span data-ttu-id="5ffb1-109">La classe **Win32 \_ TSLicenseReportEntry** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5ffb1-109">The **Win32\_TSLicenseReportEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="5ffb1-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5ffb1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5ffb1-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5ffb1-111">Properties</span></span>

<span data-ttu-id="5ffb1-112">La classe **Win32 \_ TSLicenseReportEntry** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5ffb1-112">The **Win32\_TSLicenseReportEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5ffb1-113">**CALType**</span><span class="sxs-lookup"><span data-stu-id="5ffb1-113">**CALType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ffb1-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ffb1-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ffb1-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ffb1-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ffb1-116">Specifica il tipo di licenza CAL rilasciata.</span><span class="sxs-lookup"><span data-stu-id="5ffb1-116">Specifies the type of CAL issued.</span></span> <span data-ttu-id="5ffb1-117">Si tratta di uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="5ffb1-117">This will be one of the following values.</span></span>

<span data-ttu-id="5ffb1-118">**Windows server 2008 R2 e Windows server 2008:** Questa proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="5ffb1-118">**Windows Server 2008 R2 and Windows Server 2008:** This property is not supported.</span></span>

<span data-ttu-id="5ffb1-119">"Licenze CAL per dispositivo predefinite"</span><span class="sxs-lookup"><span data-stu-id="5ffb1-119">"Built-in TS Per Device CAL"</span></span>

<span data-ttu-id="5ffb1-120">"Licenze CAL per dispositivo"</span><span class="sxs-lookup"><span data-stu-id="5ffb1-120">"TS Per Device CAL"</span></span>

<span data-ttu-id="5ffb1-121">"CAL Internet Connector CAL"</span><span class="sxs-lookup"><span data-stu-id="5ffb1-121">"TS Internet Connector CAL"</span></span>

<span data-ttu-id="5ffb1-122">"Licenza CAL per utente di servizi Terminal"</span><span class="sxs-lookup"><span data-stu-id="5ffb1-122">"TS Per User CAL"</span></span>

<span data-ttu-id="5ffb1-123">Licenza CAL per dispositivo di Servizi terminal o RDS</span><span class="sxs-lookup"><span data-stu-id="5ffb1-123">"TS or RDS Per Device CAL"</span></span>

<span data-ttu-id="5ffb1-124">Licenza CAL per utente di Servizi terminal o RDS</span><span class="sxs-lookup"><span data-stu-id="5ffb1-124">"TS or RDS Per User CAL"</span></span>

<span data-ttu-id="5ffb1-125">"Licenza abbonamento VDI Standard Suite per dispositivo"</span><span class="sxs-lookup"><span data-stu-id="5ffb1-125">"VDI Standard Suite Per Device subscription license"</span></span>

<span data-ttu-id="5ffb1-126">"Licenza di sottoscrizione di VDI Premium Suite per dispositivo"</span><span class="sxs-lookup"><span data-stu-id="5ffb1-126">"VDI Premium Suite Per Device subscription license"</span></span>

<span data-ttu-id="5ffb1-127">"RDS per dispositivo CAL"</span><span class="sxs-lookup"><span data-stu-id="5ffb1-127">"RDS Per Device CAL"</span></span>

<span data-ttu-id="5ffb1-128">"CAL per utente per utente"</span><span class="sxs-lookup"><span data-stu-id="5ffb1-128">"RDS Per User CAL"</span></span>

</dd> <dt>

<span data-ttu-id="5ffb1-129">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="5ffb1-129">**ExpirationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ffb1-130">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5ffb1-130">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="5ffb1-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ffb1-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ffb1-132">Data di scadenza della licenza rilasciata all'utente.</span><span class="sxs-lookup"><span data-stu-id="5ffb1-132">Expiration date of the license that was issued to the user.</span></span>

</dd> <dt>

<span data-ttu-id="5ffb1-133">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="5ffb1-133">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ffb1-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ffb1-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ffb1-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ffb1-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ffb1-136">Versione di Servizi Desktop remoto per cui è stata rilasciata la licenza CAL per utente.</span><span class="sxs-lookup"><span data-stu-id="5ffb1-136">Version of Remote Desktop Services for which the RDS Per User CAL was issued.</span></span>

<dt>

<span data-ttu-id="5ffb1-137">"Windows Server 2012"</span><span class="sxs-lookup"><span data-stu-id="5ffb1-137">"Windows Server 2012"</span></span>
</dt> <dd>

<span data-ttu-id="5ffb1-138">Con questa licenza sono supportati solo i server che eseguono Windows Server 2012, Windows Server 2008 R2 o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="5ffb1-138">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="5ffb1-139">"Windows Server 7"</span><span class="sxs-lookup"><span data-stu-id="5ffb1-139">"Windows Server 7"</span></span>
</dt> <dd>

<span data-ttu-id="5ffb1-140">Con questa licenza sono supportati solo i server che eseguono Windows Server 2008 R2 o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="5ffb1-140">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="5ffb1-141">"Windows Server 2008"</span><span class="sxs-lookup"><span data-stu-id="5ffb1-141">"Windows Server 2008"</span></span>
</dt> <dd>

<span data-ttu-id="5ffb1-142">Con questa licenza sono supportati solo i server che eseguono Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="5ffb1-142">Only servers running Windows Server 2008 are supported with this license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5ffb1-143">**ProductVersionID**</span><span class="sxs-lookup"><span data-stu-id="5ffb1-143">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ffb1-144">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5ffb1-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ffb1-145">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ffb1-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ffb1-146">Identificatore della versione del prodotto per il Key Pack di Servizi Desktop remoto License.</span><span class="sxs-lookup"><span data-stu-id="5ffb1-146">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="5ffb1-147">4</span><span class="sxs-lookup"><span data-stu-id="5ffb1-147">4</span></span>
</dt> <dd>

<span data-ttu-id="5ffb1-148">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5ffb1-148">Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="5ffb1-149">3</span><span class="sxs-lookup"><span data-stu-id="5ffb1-149">3</span></span>
</dt> <dd>

<span data-ttu-id="5ffb1-150">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5ffb1-150">Windows Server 2008 R2</span></span>

</dd> <dt>

<span data-ttu-id="5ffb1-151">2</span><span class="sxs-lookup"><span data-stu-id="5ffb1-151">2</span></span>
</dt> <dd>

<span data-ttu-id="5ffb1-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ffb1-152">Windows Server 2008</span></span>

</dd> <dt>

<span data-ttu-id="5ffb1-153">1</span><span class="sxs-lookup"><span data-stu-id="5ffb1-153">1</span></span>
</dt> <dd>

<span data-ttu-id="5ffb1-154">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="5ffb1-154">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="5ffb1-155">0</span><span class="sxs-lookup"><span data-stu-id="5ffb1-155">0</span></span>
</dt> <dd>

<span data-ttu-id="5ffb1-156">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="5ffb1-156">Not supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5ffb1-157">**Utente**</span><span class="sxs-lookup"><span data-stu-id="5ffb1-157">**User**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ffb1-158">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5ffb1-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ffb1-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ffb1-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ffb1-160">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5ffb1-160">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5ffb1-161">Nome dell'utente a cui è stata emessa la licenza.</span><span class="sxs-lookup"><span data-stu-id="5ffb1-161">Name of the user to whom the license was issued.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ffb1-162">Commenti</span><span class="sxs-lookup"><span data-stu-id="5ffb1-162">Remarks</span></span>

<span data-ttu-id="5ffb1-163">Per utilizzare questa classe, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="5ffb1-163">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="5ffb1-164">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="5ffb1-164">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5ffb1-165">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="5ffb1-165">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="5ffb1-166">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="5ffb1-166">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5ffb1-167">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="5ffb1-167">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="5ffb1-168">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ffb1-168">Requirements</span></span>



| <span data-ttu-id="5ffb1-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ffb1-169">Requirement</span></span> | <span data-ttu-id="5ffb1-170">Valore</span><span class="sxs-lookup"><span data-stu-id="5ffb1-170">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ffb1-171">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ffb1-171">Minimum supported client</span></span><br/> | <span data-ttu-id="5ffb1-172">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5ffb1-172">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="5ffb1-173">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ffb1-173">Minimum supported server</span></span><br/> | <span data-ttu-id="5ffb1-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ffb1-174">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="5ffb1-175">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5ffb1-175">Namespace</span></span><br/>                | <span data-ttu-id="5ffb1-176">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="5ffb1-176">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="5ffb1-177">MOF</span><span class="sxs-lookup"><span data-stu-id="5ffb1-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ffb1-178"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ffb1-178"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ffb1-179">DLL</span><span class="sxs-lookup"><span data-stu-id="5ffb1-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ffb1-180"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ffb1-180"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ffb1-181">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ffb1-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ffb1-182">**FetchReportEntries**</span><span class="sxs-lookup"><span data-stu-id="5ffb1-182">**FetchReportEntries**</span></span>](fetchreportentries-win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="5ffb1-183">**\_TSIssuedLicense Win32**</span><span class="sxs-lookup"><span data-stu-id="5ffb1-183">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> <dt>

[<span data-ttu-id="5ffb1-184">**\_TSLicenseKeyPack Win32**</span><span class="sxs-lookup"><span data-stu-id="5ffb1-184">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> <dt>

[<span data-ttu-id="5ffb1-185">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="5ffb1-185">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="5ffb1-186">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="5ffb1-186">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 


---
title: Classe Win32_TSLicenseReportPerDeviceEntry
description: Fornisce informazioni dettagliate sulla licenza di accesso client per dispositivo Servizi Desktop remoto non riuscita (RDS \ 160; Per ogni dispositivo CAL).
ms.assetid: b26f2518-439c-4562-9492-a0cfa60c457a
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSLicenseReportPerDeviceEntry Servizi Desktop remoto
- Classe Win32_TSLicenseReportPerDeviceEntry Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportPerDeviceEntry
- Win32_TSLicenseReportPerDeviceEntry.sIssuedToComputer
- Win32_TSLicenseReportPerDeviceEntry.sHardwareId
- Win32_TSLicenseReportPerDeviceEntry.ExpirationDate
- Win32_TSLicenseReportPerDeviceEntry.CALType
- Win32_TSLicenseReportPerDeviceEntry.ProductVersion
- Win32_TSLicenseReportPerDeviceEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a120d477ff03675f160d94f1506f59cdf1462fa1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475461"
---
# <a name="win32_tslicensereportperdeviceentry-class"></a><span data-ttu-id="1d8cb-105">Win32 \_ TSLicenseReportPerDeviceEntry (classe)</span><span class="sxs-lookup"><span data-stu-id="1d8cb-105">Win32\_TSLicenseReportPerDeviceEntry class</span></span>

<span data-ttu-id="1d8cb-106">Fornisce informazioni dettagliate sul Servizi Desktop remoto non riuscito per ogni dispositivo CAL per dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d8cb-106">Provides details about the failed Remote Desktop Services Per Device client access license (RDS Per Device CAL).</span></span>

<span data-ttu-id="1d8cb-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="1d8cb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d8cb-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1d8cb-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportPerDeviceEntry
{
  string   sIssuedToComputer;
  string   sHardwareId;
  DATETIME ExpirationDate;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a><span data-ttu-id="1d8cb-109">Members</span><span class="sxs-lookup"><span data-stu-id="1d8cb-109">Members</span></span>

<span data-ttu-id="1d8cb-110">La classe **Win32 \_ TSLicenseReportPerDeviceEntry** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1d8cb-110">The **Win32\_TSLicenseReportPerDeviceEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="1d8cb-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1d8cb-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1d8cb-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1d8cb-112">Properties</span></span>

<span data-ttu-id="1d8cb-113">La classe **Win32 \_ TSLicenseReportPerDeviceEntry** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1d8cb-113">The **Win32\_TSLicenseReportPerDeviceEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1d8cb-114">**CALType**</span><span class="sxs-lookup"><span data-stu-id="1d8cb-114">**CALType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d8cb-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d8cb-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d8cb-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d8cb-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d8cb-117">Specifica il tipo di licenza CAL rilasciata.</span><span class="sxs-lookup"><span data-stu-id="1d8cb-117">Specifies the type of CAL issued.</span></span> <span data-ttu-id="1d8cb-118">Si tratta di uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="1d8cb-118">This will be one of the following values.</span></span>

<span data-ttu-id="1d8cb-119">"Licenze CAL per dispositivo predefinite"</span><span class="sxs-lookup"><span data-stu-id="1d8cb-119">"Built-in TS Per Device CAL"</span></span>

<span data-ttu-id="1d8cb-120">"Licenze CAL per dispositivo"</span><span class="sxs-lookup"><span data-stu-id="1d8cb-120">"TS Per Device CAL"</span></span>

<span data-ttu-id="1d8cb-121">"CAL Internet Connector CAL"</span><span class="sxs-lookup"><span data-stu-id="1d8cb-121">"TS Internet Connector CAL"</span></span>

<span data-ttu-id="1d8cb-122">"Licenza CAL per utente di servizi Terminal"</span><span class="sxs-lookup"><span data-stu-id="1d8cb-122">"TS Per User CAL"</span></span>

<span data-ttu-id="1d8cb-123">Licenza CAL per dispositivo di Servizi terminal o RDS</span><span class="sxs-lookup"><span data-stu-id="1d8cb-123">"TS or RDS Per Device CAL"</span></span>

<span data-ttu-id="1d8cb-124">Licenza CAL per utente di Servizi terminal o RDS</span><span class="sxs-lookup"><span data-stu-id="1d8cb-124">"TS or RDS Per User CAL"</span></span>

<span data-ttu-id="1d8cb-125">"Licenza abbonamento VDI Standard Suite per dispositivo"</span><span class="sxs-lookup"><span data-stu-id="1d8cb-125">"VDI Standard Suite Per Device subscription license"</span></span>

<span data-ttu-id="1d8cb-126">"Licenza di sottoscrizione di VDI Premium Suite per dispositivo"</span><span class="sxs-lookup"><span data-stu-id="1d8cb-126">"VDI Premium Suite Per Device subscription license"</span></span>

<span data-ttu-id="1d8cb-127">"RDS per dispositivo CAL"</span><span class="sxs-lookup"><span data-stu-id="1d8cb-127">"RDS Per Device CAL"</span></span>

<span data-ttu-id="1d8cb-128">"CAL per utente per utente"</span><span class="sxs-lookup"><span data-stu-id="1d8cb-128">"RDS Per User CAL"</span></span>

</dd> <dt>

<span data-ttu-id="1d8cb-129">**ExpirationDate**</span><span class="sxs-lookup"><span data-stu-id="1d8cb-129">**ExpirationDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d8cb-130">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1d8cb-130">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="1d8cb-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d8cb-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d8cb-132">Data di scadenza della licenza.</span><span class="sxs-lookup"><span data-stu-id="1d8cb-132">The expiration date of the license.</span></span>

</dd> <dt>

<span data-ttu-id="1d8cb-133">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="1d8cb-133">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d8cb-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d8cb-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d8cb-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d8cb-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d8cb-136">Versione di Servizi Desktop remoto per cui è stata rilasciata la licenza CAL per utente.</span><span class="sxs-lookup"><span data-stu-id="1d8cb-136">The version of Remote Desktop Services for which the RDS Per User CAL was issued.</span></span> <span data-ttu-id="1d8cb-137">Si tratta di uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="1d8cb-137">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="1d8cb-138">"Windows Server 2012"</span><span class="sxs-lookup"><span data-stu-id="1d8cb-138">"Windows Server 2012"</span></span>
</dt> <dd>

<span data-ttu-id="1d8cb-139">Con questa licenza sono supportati solo i server che eseguono Windows Server 2012, Windows Server 2008 R2 o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="1d8cb-139">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="1d8cb-140">"Windows Server 7"</span><span class="sxs-lookup"><span data-stu-id="1d8cb-140">"Windows Server 7"</span></span>
</dt> <dd>

<span data-ttu-id="1d8cb-141">Con questa licenza sono supportati solo i server che eseguono Windows Server 2008 R2 o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="1d8cb-141">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="1d8cb-142">"Windows Server 2008"</span><span class="sxs-lookup"><span data-stu-id="1d8cb-142">"Windows Server 2008"</span></span>
</dt> <dd>

<span data-ttu-id="1d8cb-143">Con questa licenza sono supportati solo i server che eseguono Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="1d8cb-143">Only servers running Windows Server 2008 are supported with this license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1d8cb-144">**ProductVersionID**</span><span class="sxs-lookup"><span data-stu-id="1d8cb-144">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d8cb-145">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d8cb-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d8cb-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d8cb-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d8cb-147">Identificatore della versione del prodotto per il Key Pack di Servizi Desktop remoto License.</span><span class="sxs-lookup"><span data-stu-id="1d8cb-147">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="1d8cb-148">4</span><span class="sxs-lookup"><span data-stu-id="1d8cb-148">4</span></span>
</dt> <dd>

<span data-ttu-id="1d8cb-149">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1d8cb-149">Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="1d8cb-150">3</span><span class="sxs-lookup"><span data-stu-id="1d8cb-150">3</span></span>
</dt> <dd>

<span data-ttu-id="1d8cb-151">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1d8cb-151">Windows Server 2008 R2</span></span>

</dd> <dt>

<span data-ttu-id="1d8cb-152">2</span><span class="sxs-lookup"><span data-stu-id="1d8cb-152">2</span></span>
</dt> <dd>

<span data-ttu-id="1d8cb-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d8cb-153">Windows Server 2008</span></span>

</dd> <dt>

<span data-ttu-id="1d8cb-154">1</span><span class="sxs-lookup"><span data-stu-id="1d8cb-154">1</span></span>
</dt> <dd>

<span data-ttu-id="1d8cb-155">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="1d8cb-155">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="1d8cb-156">0</span><span class="sxs-lookup"><span data-stu-id="1d8cb-156">0</span></span>
</dt> <dd>

<span data-ttu-id="1d8cb-157">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="1d8cb-157">Not supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1d8cb-158">**sHardwareId**</span><span class="sxs-lookup"><span data-stu-id="1d8cb-158">**sHardwareId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d8cb-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d8cb-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d8cb-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d8cb-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d8cb-161">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1d8cb-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1d8cb-162">Identificatore hardware del computer.</span><span class="sxs-lookup"><span data-stu-id="1d8cb-162">The hardware identifier of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="1d8cb-163">**sIssuedToComputer**</span><span class="sxs-lookup"><span data-stu-id="1d8cb-163">**sIssuedToComputer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d8cb-164">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="1d8cb-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d8cb-165">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1d8cb-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d8cb-166">Nome del computer per cui è stato effettuato il tentativo di rilascio della licenza.</span><span class="sxs-lookup"><span data-stu-id="1d8cb-166">The name of the computer that the license issuance was attempted for.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d8cb-167">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d8cb-167">Requirements</span></span>



| <span data-ttu-id="1d8cb-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d8cb-168">Requirement</span></span> | <span data-ttu-id="1d8cb-169">Valore</span><span class="sxs-lookup"><span data-stu-id="1d8cb-169">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d8cb-170">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d8cb-170">Minimum supported client</span></span><br/> | <span data-ttu-id="1d8cb-171">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1d8cb-171">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="1d8cb-172">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d8cb-172">Minimum supported server</span></span><br/> | <span data-ttu-id="1d8cb-173">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1d8cb-173">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="1d8cb-174">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1d8cb-174">Namespace</span></span><br/>                | <span data-ttu-id="1d8cb-175">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="1d8cb-175">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="1d8cb-176">MOF</span><span class="sxs-lookup"><span data-stu-id="1d8cb-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d8cb-177"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d8cb-177"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d8cb-178">DLL</span><span class="sxs-lookup"><span data-stu-id="1d8cb-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d8cb-179"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d8cb-179"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d8cb-180">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d8cb-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d8cb-181">**FetchReportPerDeviceEntries**</span><span class="sxs-lookup"><span data-stu-id="1d8cb-181">**FetchReportPerDeviceEntries**</span></span>](fetchreportperdeviceentries-win32-tslicensereport.md)
</dt> </dl>

 


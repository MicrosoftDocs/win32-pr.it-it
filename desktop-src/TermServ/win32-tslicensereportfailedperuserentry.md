---
title: Classe Win32_TSLicenseReportFailedPerUserEntry
description: Fornisce informazioni dettagliate sulla licenza di accesso client Servizi Desktop remoto per utente non riuscita (RDS \ 160; CAL per utente).
ms.assetid: 27d155a4-938e-4bca-8d15-03c44740e506
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSLicenseReportFailedPerUserEntry Servizi Desktop remoto
- Classe Win32_TSLicenseReportFailedPerUserEntry Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportFailedPerUserEntry
- Win32_TSLicenseReportFailedPerUserEntry.User
- Win32_TSLicenseReportFailedPerUserEntry.TriedIssuanceOn
- Win32_TSLicenseReportFailedPerUserEntry.CALType
- Win32_TSLicenseReportFailedPerUserEntry.ProductVersion
- Win32_TSLicenseReportFailedPerUserEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18098ce0510a39f6083edcf688a18c10a3e20278
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400270"
---
# <a name="win32_tslicensereportfailedperuserentry-class"></a><span data-ttu-id="089a7-105">Win32 \_ TSLicenseReportFailedPerUserEntry (classe)</span><span class="sxs-lookup"><span data-stu-id="089a7-105">Win32\_TSLicenseReportFailedPerUserEntry class</span></span>

<span data-ttu-id="089a7-106">Fornisce informazioni dettagliate sulla licenza CAL per utente Servizi Desktop remoto per utente non riuscita.</span><span class="sxs-lookup"><span data-stu-id="089a7-106">Provides details about the failed Remote Desktop Services Per User client access license (RDS Per User CAL).</span></span>

<span data-ttu-id="089a7-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="089a7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="089a7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="089a7-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportFailedPerUserEntry
{
  string   User;
  DATETIME TriedIssuanceOn;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a><span data-ttu-id="089a7-109">Members</span><span class="sxs-lookup"><span data-stu-id="089a7-109">Members</span></span>

<span data-ttu-id="089a7-110">La classe **Win32 \_ TSLicenseReportFailedPerUserEntry** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="089a7-110">The **Win32\_TSLicenseReportFailedPerUserEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="089a7-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="089a7-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="089a7-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="089a7-112">Properties</span></span>

<span data-ttu-id="089a7-113">La classe **Win32 \_ TSLicenseReportFailedPerUserEntry** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="089a7-113">The **Win32\_TSLicenseReportFailedPerUserEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="089a7-114">**CALType**</span><span class="sxs-lookup"><span data-stu-id="089a7-114">**CALType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="089a7-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="089a7-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="089a7-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="089a7-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="089a7-117">Specifica il tipo di licenza CAL rilasciata.</span><span class="sxs-lookup"><span data-stu-id="089a7-117">Specifies the type of CAL issued.</span></span> <span data-ttu-id="089a7-118">Si tratta di uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="089a7-118">This will be one of the following values.</span></span>

<span data-ttu-id="089a7-119">"Licenze CAL per dispositivo predefinite"</span><span class="sxs-lookup"><span data-stu-id="089a7-119">"Built-in TS Per Device CAL"</span></span>

<span data-ttu-id="089a7-120">"Licenze CAL per dispositivo"</span><span class="sxs-lookup"><span data-stu-id="089a7-120">"TS Per Device CAL"</span></span>

<span data-ttu-id="089a7-121">"CAL Internet Connector CAL"</span><span class="sxs-lookup"><span data-stu-id="089a7-121">"TS Internet Connector CAL"</span></span>

<span data-ttu-id="089a7-122">"Licenza CAL per utente di servizi Terminal"</span><span class="sxs-lookup"><span data-stu-id="089a7-122">"TS Per User CAL"</span></span>

<span data-ttu-id="089a7-123">Licenza CAL per dispositivo di Servizi terminal o RDS</span><span class="sxs-lookup"><span data-stu-id="089a7-123">"TS or RDS Per Device CAL"</span></span>

<span data-ttu-id="089a7-124">Licenza CAL per utente di Servizi terminal o RDS</span><span class="sxs-lookup"><span data-stu-id="089a7-124">"TS or RDS Per User CAL"</span></span>

<span data-ttu-id="089a7-125">"Licenza abbonamento VDI Standard Suite per dispositivo"</span><span class="sxs-lookup"><span data-stu-id="089a7-125">"VDI Standard Suite Per Device subscription license"</span></span>

<span data-ttu-id="089a7-126">"Licenza di sottoscrizione di VDI Premium Suite per dispositivo"</span><span class="sxs-lookup"><span data-stu-id="089a7-126">"VDI Premium Suite Per Device subscription license"</span></span>

<span data-ttu-id="089a7-127">"RDS per dispositivo CAL"</span><span class="sxs-lookup"><span data-stu-id="089a7-127">"RDS Per Device CAL"</span></span>

<span data-ttu-id="089a7-128">"CAL per utente per utente"</span><span class="sxs-lookup"><span data-stu-id="089a7-128">"RDS Per User CAL"</span></span>

</dd> <dt>

<span data-ttu-id="089a7-129">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="089a7-129">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="089a7-130">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="089a7-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="089a7-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="089a7-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="089a7-132">Versione di Servizi Desktop remoto per cui è stata rilasciata la licenza CAL per utente.</span><span class="sxs-lookup"><span data-stu-id="089a7-132">The version of Remote Desktop Services for which the RDS Per User CAL was issued.</span></span> <span data-ttu-id="089a7-133">Si tratta di uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="089a7-133">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="089a7-134">"Windows Server 2012"</span><span class="sxs-lookup"><span data-stu-id="089a7-134">"Windows Server 2012"</span></span>
</dt> <dd>

<span data-ttu-id="089a7-135">Con questa licenza sono supportati solo i server che eseguono Windows Server 2012, Windows Server 2008 R2 o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="089a7-135">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="089a7-136">"Windows Server 7"</span><span class="sxs-lookup"><span data-stu-id="089a7-136">"Windows Server 7"</span></span>
</dt> <dd>

<span data-ttu-id="089a7-137">Con questa licenza sono supportati solo i server che eseguono Windows Server 2008 R2 o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="089a7-137">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="089a7-138">"Windows Server 2008"</span><span class="sxs-lookup"><span data-stu-id="089a7-138">"Windows Server 2008"</span></span>
</dt> <dd>

<span data-ttu-id="089a7-139">Con questa licenza sono supportati solo i server che eseguono Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="089a7-139">Only servers running Windows Server 2008 are supported with this license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="089a7-140">**ProductVersionID**</span><span class="sxs-lookup"><span data-stu-id="089a7-140">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="089a7-141">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="089a7-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="089a7-142">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="089a7-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="089a7-143">Identificatore della versione del prodotto per il Key Pack di Servizi Desktop remoto License.</span><span class="sxs-lookup"><span data-stu-id="089a7-143">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="089a7-144">4</span><span class="sxs-lookup"><span data-stu-id="089a7-144">4</span></span>
</dt> <dd>

<span data-ttu-id="089a7-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="089a7-145">Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="089a7-146">3</span><span class="sxs-lookup"><span data-stu-id="089a7-146">3</span></span>
</dt> <dd>

<span data-ttu-id="089a7-147">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="089a7-147">Windows Server 2008 R2</span></span>

</dd> <dt>

<span data-ttu-id="089a7-148">2</span><span class="sxs-lookup"><span data-stu-id="089a7-148">2</span></span>
</dt> <dd>

<span data-ttu-id="089a7-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="089a7-149">Windows Server 2008</span></span>

</dd> <dt>

<span data-ttu-id="089a7-150">1</span><span class="sxs-lookup"><span data-stu-id="089a7-150">1</span></span>
</dt> <dd>

<span data-ttu-id="089a7-151">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="089a7-151">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="089a7-152">0</span><span class="sxs-lookup"><span data-stu-id="089a7-152">0</span></span>
</dt> <dd>

<span data-ttu-id="089a7-153">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="089a7-153">Not supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="089a7-154">**TriedIssuanceOn**</span><span class="sxs-lookup"><span data-stu-id="089a7-154">**TriedIssuanceOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="089a7-155">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="089a7-155">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="089a7-156">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="089a7-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="089a7-157">Data in cui è stato effettuato il tentativo di rilascio della licenza.</span><span class="sxs-lookup"><span data-stu-id="089a7-157">The date on which license issuance was attempted.</span></span>

</dd> <dt>

<span data-ttu-id="089a7-158">**Utente**</span><span class="sxs-lookup"><span data-stu-id="089a7-158">**User**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="089a7-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="089a7-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="089a7-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="089a7-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="089a7-161">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="089a7-161">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="089a7-162">Nome dell'utente a cui è stato effettuato il tentativo di rilascio della licenza.</span><span class="sxs-lookup"><span data-stu-id="089a7-162">The name of the user to whom the license issuance was attempted.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="089a7-163">Requisiti</span><span class="sxs-lookup"><span data-stu-id="089a7-163">Requirements</span></span>



| <span data-ttu-id="089a7-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="089a7-164">Requirement</span></span> | <span data-ttu-id="089a7-165">Valore</span><span class="sxs-lookup"><span data-stu-id="089a7-165">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="089a7-166">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="089a7-166">Minimum supported client</span></span><br/> | <span data-ttu-id="089a7-167">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="089a7-167">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="089a7-168">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="089a7-168">Minimum supported server</span></span><br/> | <span data-ttu-id="089a7-169">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="089a7-169">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="089a7-170">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="089a7-170">Namespace</span></span><br/>                | <span data-ttu-id="089a7-171">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="089a7-171">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="089a7-172">MOF</span><span class="sxs-lookup"><span data-stu-id="089a7-172">MOF</span></span><br/>                      | <dl> <span data-ttu-id="089a7-173"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="089a7-173"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="089a7-174">DLL</span><span class="sxs-lookup"><span data-stu-id="089a7-174">DLL</span></span><br/>                      | <dl> <span data-ttu-id="089a7-175"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="089a7-175"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="089a7-176">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="089a7-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="089a7-177">**FetchReportFailedPerUserEntries**</span><span class="sxs-lookup"><span data-stu-id="089a7-177">**FetchReportFailedPerUserEntries**</span></span>](fetchreportfailedperuserentries-win32-tslicensereport.md)
</dt> </dl>

 


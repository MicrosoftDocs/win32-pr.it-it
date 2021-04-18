---
title: Classe Win32_TSLicenseReportSummaryEntry
description: Fornisce un riepilogo delle licenze di accesso client (RDS \ 160) installate e rilasciate Servizi Desktop remoto per utente. Licenze CAL per utente).
ms.assetid: 0FD3BFFE-58B9-4037-969F-8C2323136C9D
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSLicenseReportSummaryEntry Servizi Desktop remoto
- Classe Win32_TSLicenseReportSummaryEntry Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportSummaryEntry
- Win32_TSLicenseReportSummaryEntry.ProductVersion
- Win32_TSLicenseReportSummaryEntry.ProductVersionID
- Win32_TSLicenseReportSummaryEntry.TSCALType
- Win32_TSLicenseReportSummaryEntry.InstalledLicenses
- Win32_TSLicenseReportSummaryEntry.IssuedLicenses
- Win32_TSLicenseReportSummaryEntry.TSCALAvailability
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f34482e9c6199ef6586024d43d586421a54071ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301057"
---
# <a name="win32_tslicensereportsummaryentry-class"></a><span data-ttu-id="3534c-105">Win32 \_ TSLicenseReportSummaryEntry (classe)</span><span class="sxs-lookup"><span data-stu-id="3534c-105">Win32\_TSLicenseReportSummaryEntry class</span></span>

<span data-ttu-id="3534c-106">Fornisce un riepilogo delle licenze di accesso client (RDS per utente) installate e riServizi Desktop remoto lasciate per ogni utente.</span><span class="sxs-lookup"><span data-stu-id="3534c-106">Provides a summary of the installed and issued Remote Desktop Services Per User client access licenses (RDS Per User CALs).</span></span>

## <a name="syntax"></a><span data-ttu-id="3534c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3534c-107">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportSummaryEntry
{
  string ProductVersion;
  uint32 ProductVersionID;
  string TSCALType;
  uint32 InstalledLicenses;
  uint32 IssuedLicenses;
  string TSCALAvailability;
};
```

## <a name="members"></a><span data-ttu-id="3534c-108">Members</span><span class="sxs-lookup"><span data-stu-id="3534c-108">Members</span></span>

<span data-ttu-id="3534c-109">La classe **Win32 \_ TSLicenseReportSummaryEntry** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3534c-109">The **Win32\_TSLicenseReportSummaryEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="3534c-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3534c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3534c-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3534c-111">Properties</span></span>

<span data-ttu-id="3534c-112">La classe **Win32 \_ TSLicenseReportSummaryEntry** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3534c-112">The **Win32\_TSLicenseReportSummaryEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3534c-113">**InstalledLicenses**</span><span class="sxs-lookup"><span data-stu-id="3534c-113">**InstalledLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3534c-114">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3534c-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3534c-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3534c-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3534c-116">Numero di licenze CAL per utente di Servizi Desktop remoto installate.</span><span class="sxs-lookup"><span data-stu-id="3534c-116">Number of RDS Per User CALs that are installed.</span></span>

</dd> <dt>

<span data-ttu-id="3534c-117">**IssuedLicenses**</span><span class="sxs-lookup"><span data-stu-id="3534c-117">**IssuedLicenses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3534c-118">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3534c-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3534c-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3534c-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3534c-120">Numero di licenze CAL per utente per ogni utente rilasciate.</span><span class="sxs-lookup"><span data-stu-id="3534c-120">Number of RDS Per User CALs that are issued.</span></span>

</dd> <dt>

<span data-ttu-id="3534c-121">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="3534c-121">**ProductVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3534c-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3534c-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3534c-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3534c-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3534c-124">Versione di Servizi Desktop remoto per cui è stata rilasciata la licenza CAL per utente.</span><span class="sxs-lookup"><span data-stu-id="3534c-124">Version of Remote Desktop Services for which the RDS Per User CAL was issued.</span></span>

<dt>

<span data-ttu-id="3534c-125">"Windows Server 2012"</span><span class="sxs-lookup"><span data-stu-id="3534c-125">"Windows Server 2012"</span></span>
</dt> <dd>

<span data-ttu-id="3534c-126">Con questa licenza sono supportati solo i server che eseguono Windows Server 2012, Windows Server 2008 R2 o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="3534c-126">Only servers running Windows Server 2012, Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="3534c-127">"Windows Server 7"</span><span class="sxs-lookup"><span data-stu-id="3534c-127">"Windows Server 7"</span></span>
</dt> <dd>

<span data-ttu-id="3534c-128">Con questa licenza sono supportati solo i server che eseguono Windows Server 2008 R2 o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="3534c-128">Only servers running Windows Server 2008 R2, or Windows Server 2008 are supported with this license.</span></span>

</dd> <dt>

<span data-ttu-id="3534c-129">"Windows Server 2008"</span><span class="sxs-lookup"><span data-stu-id="3534c-129">"Windows Server 2008"</span></span>
</dt> <dd>

<span data-ttu-id="3534c-130">Con questa licenza sono supportati solo i server che eseguono Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="3534c-130">Only servers running Windows Server 2008 are supported with this license.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3534c-131">**ProductVersionID**</span><span class="sxs-lookup"><span data-stu-id="3534c-131">**ProductVersionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3534c-132">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3534c-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3534c-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3534c-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3534c-134">Identificatore della versione del prodotto per il Key Pack di Servizi Desktop remoto License.</span><span class="sxs-lookup"><span data-stu-id="3534c-134">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="3534c-135">4</span><span class="sxs-lookup"><span data-stu-id="3534c-135">4</span></span>
</dt> <dd>

<span data-ttu-id="3534c-136">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3534c-136">Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="3534c-137">3</span><span class="sxs-lookup"><span data-stu-id="3534c-137">3</span></span>
</dt> <dd>

<span data-ttu-id="3534c-138">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3534c-138">Windows Server 2008 R2</span></span>

</dd> <dt>

<span data-ttu-id="3534c-139">2</span><span class="sxs-lookup"><span data-stu-id="3534c-139">2</span></span>
</dt> <dd>

<span data-ttu-id="3534c-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3534c-140">Windows Server 2008</span></span>

</dd> <dt>

<span data-ttu-id="3534c-141">1</span><span class="sxs-lookup"><span data-stu-id="3534c-141">1</span></span>
</dt> <dd>

<span data-ttu-id="3534c-142">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="3534c-142">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="3534c-143">0</span><span class="sxs-lookup"><span data-stu-id="3534c-143">0</span></span>
</dt> <dd>

<span data-ttu-id="3534c-144">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="3534c-144">Not supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3534c-145">**TSCALAvailability**</span><span class="sxs-lookup"><span data-stu-id="3534c-145">**TSCALAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3534c-146">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3534c-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3534c-147">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3534c-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3534c-148">Disponibilità delle licenze CAL per utente per utente.</span><span class="sxs-lookup"><span data-stu-id="3534c-148">The availability of the RDS Per User CALs.</span></span> <span data-ttu-id="3534c-149">Si tratta di uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3534c-149">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="3534c-150">Disponibile</span><span class="sxs-lookup"><span data-stu-id="3534c-150">"Available"</span></span>
</dt> <dd>

<span data-ttu-id="3534c-151">Le licenze CAL per utente per utente sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="3534c-151">The RDS Per User CALs are available.</span></span>

</dd> <dt>

<span data-ttu-id="3534c-152">Limitato</span><span class="sxs-lookup"><span data-stu-id="3534c-152">"Limited"</span></span>
</dt> <dd>

<span data-ttu-id="3534c-153">La disponibilità delle licenze CAL per utente per utente è limitata.</span><span class="sxs-lookup"><span data-stu-id="3534c-153">The availability of the RDS Per User CALs is limited.</span></span>

</dd> <dt>

<span data-ttu-id="3534c-154">"None"</span><span class="sxs-lookup"><span data-stu-id="3534c-154">"None"</span></span>
</dt> <dd>

<span data-ttu-id="3534c-155">Le licenze CAL per utente per utente non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="3534c-155">The RDS Per User CALs are not available.</span></span>

</dd> <dt>

<span data-ttu-id="3534c-156">"Non rilevamento"</span><span class="sxs-lookup"><span data-stu-id="3534c-156">"Not Tracking"</span></span>
</dt> <dd>

<span data-ttu-id="3534c-157">Non è stata rilevata la disponibilità delle licenze CAL per utente per utente.</span><span class="sxs-lookup"><span data-stu-id="3534c-157">The availability of the RDS Per User CALs is not being tracked.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3534c-158">**TSCALType**</span><span class="sxs-lookup"><span data-stu-id="3534c-158">**TSCALType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3534c-159">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3534c-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3534c-160">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3534c-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3534c-161">Tipo di licenze CAL per utente per utente.</span><span class="sxs-lookup"><span data-stu-id="3534c-161">The type of RDS Per User CALs.</span></span> <span data-ttu-id="3534c-162">Si tratta di uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3534c-162">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="3534c-163">"Per dispositivo"</span><span class="sxs-lookup"><span data-stu-id="3534c-163">"Per Device"</span></span>
</dt> <dd>

<span data-ttu-id="3534c-164">Le licenze CAL per utente per utente vengono rilasciate per ogni dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3534c-164">The RDS Per User CALs are issued per device.</span></span>

</dd> <dt>

<span data-ttu-id="3534c-165">"Per utente"</span><span class="sxs-lookup"><span data-stu-id="3534c-165">"Per User"</span></span>
</dt> <dd>

<span data-ttu-id="3534c-166">Le licenze CAL per utente per utente vengono rilasciate per utente.</span><span class="sxs-lookup"><span data-stu-id="3534c-166">The RDS Per User CALs are issued per user.</span></span>

</dd> <dt>

<span data-ttu-id="3534c-167">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="3534c-167">"Unknown"</span></span>
</dt> <dd>

<span data-ttu-id="3534c-168">Il tipo di licenze CAL per utente per utente è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="3534c-168">The type of RDS Per User CALs is unknown.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3534c-169">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3534c-169">Requirements</span></span>



| <span data-ttu-id="3534c-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="3534c-170">Requirement</span></span> | <span data-ttu-id="3534c-171">Valore</span><span class="sxs-lookup"><span data-stu-id="3534c-171">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3534c-172">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3534c-172">Minimum supported client</span></span><br/> | <span data-ttu-id="3534c-173">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3534c-173">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="3534c-174">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3534c-174">Minimum supported server</span></span><br/> | <span data-ttu-id="3534c-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3534c-175">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="3534c-176">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3534c-176">Namespace</span></span><br/>                | <span data-ttu-id="3534c-177">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="3534c-177">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="3534c-178">MOF</span><span class="sxs-lookup"><span data-stu-id="3534c-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3534c-179"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3534c-179"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3534c-180">DLL</span><span class="sxs-lookup"><span data-stu-id="3534c-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3534c-181"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3534c-181"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



 

 






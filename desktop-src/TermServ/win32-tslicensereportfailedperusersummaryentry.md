---
title: Classe Win32_TSLicenseReportFailedPerUserSummaryEntry
description: Fornisce informazioni dettagliate sui domini per i quali il rilascio per utente non è riuscito.
ms.assetid: f7265734-ac4d-439f-ae8b-3694e6f81f2a
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSLicenseReportFailedPerUserSummaryEntry Servizi Desktop remoto
- Classe Win32_TSLicenseReportFailedPerUserSummaryEntry Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportFailedPerUserSummaryEntry
- Win32_TSLicenseReportFailedPerUserSummaryEntry.DomainName
- Win32_TSLicenseReportFailedPerUserSummaryEntry.FailedIssuanceCount
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f086d275c064f5df18ee01a3a38639a40913f3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963819"
---
# <a name="win32_tslicensereportfailedperusersummaryentry-class"></a><span data-ttu-id="07b46-105">Win32 \_ TSLicenseReportFailedPerUserSummaryEntry (classe)</span><span class="sxs-lookup"><span data-stu-id="07b46-105">Win32\_TSLicenseReportFailedPerUserSummaryEntry class</span></span>

<span data-ttu-id="07b46-106">Fornisce informazioni dettagliate sui domini per i quali il rilascio per utente non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="07b46-106">Provides details of the domains to which Per User Issuance was failed.</span></span>

<span data-ttu-id="07b46-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="07b46-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="07b46-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07b46-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportFailedPerUserSummaryEntry
{
  string DomainName;
  uint32 FailedIssuanceCount;
};
```

## <a name="members"></a><span data-ttu-id="07b46-109">Members</span><span class="sxs-lookup"><span data-stu-id="07b46-109">Members</span></span>

<span data-ttu-id="07b46-110">La classe **Win32 \_ TSLicenseReportFailedPerUserSummaryEntry** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="07b46-110">The **Win32\_TSLicenseReportFailedPerUserSummaryEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="07b46-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="07b46-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="07b46-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="07b46-112">Properties</span></span>

<span data-ttu-id="07b46-113">La classe **Win32 \_ TSLicenseReportFailedPerUserSummaryEntry** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="07b46-113">The **Win32\_TSLicenseReportFailedPerUserSummaryEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="07b46-114">**NomeDominio**</span><span class="sxs-lookup"><span data-stu-id="07b46-114">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b46-115">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="07b46-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="07b46-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b46-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="07b46-117">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="07b46-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="07b46-118">Specifica il nome di dominio in cui il rilascio della licenza non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="07b46-118">Specifies the domain name to which the license issuance failed.</span></span>

</dd> <dt>

<span data-ttu-id="07b46-119">**FailedIssuanceCount**</span><span class="sxs-lookup"><span data-stu-id="07b46-119">**FailedIssuanceCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="07b46-120">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="07b46-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="07b46-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="07b46-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="07b46-122">Numero di emissioni non riuscite.</span><span class="sxs-lookup"><span data-stu-id="07b46-122">The number of failed issuances.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="07b46-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07b46-123">Requirements</span></span>



| <span data-ttu-id="07b46-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="07b46-124">Requirement</span></span> | <span data-ttu-id="07b46-125">Valore</span><span class="sxs-lookup"><span data-stu-id="07b46-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="07b46-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07b46-126">Minimum supported client</span></span><br/> | <span data-ttu-id="07b46-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="07b46-127">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="07b46-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07b46-128">Minimum supported server</span></span><br/> | <span data-ttu-id="07b46-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="07b46-129">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="07b46-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="07b46-130">Namespace</span></span><br/>                | <span data-ttu-id="07b46-131">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="07b46-131">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="07b46-132">MOF</span><span class="sxs-lookup"><span data-stu-id="07b46-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07b46-133"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="07b46-133"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="07b46-134">DLL</span><span class="sxs-lookup"><span data-stu-id="07b46-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07b46-135"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07b46-135"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07b46-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07b46-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07b46-137">**FetchReportFailedPerUserSummaryEntries**</span><span class="sxs-lookup"><span data-stu-id="07b46-137">**FetchReportFailedPerUserSummaryEntries**</span></span>](fetchreportfailedperusersummaryentries-win32-tslicensereport.md)
</dt> </dl>

 


---
title: Metodo FetchReportFailedPerUserSummaryEntries della classe Win32_TSLicenseReport
description: Recupera le informazioni di riepilogo di Servizi Desktop remoto non riuscite per licenze client Access (RDS \ 160; Licenze CAL per utente) dal report.
ms.assetid: dc9c4a36-b2a8-407e-b902-ee9d51227909
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo FetchReportFailedPerUserSummaryEntries
- Metodo FetchReportFailedPerUserSummaryEntries Servizi Desktop remoto, classe Win32_TSLicenseReport
- Classe Win32_TSLicenseReport Servizi Desktop remoto, metodo FetchReportFailedPerUserSummaryEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportFailedPerUserSummaryEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5219c2c854e04dabf8b5bfe0b5b70a07bbc3c57e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302478"
---
# <a name="fetchreportfailedperusersummaryentries-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="6e494-106">Metodo FetchReportFailedPerUserSummaryEntries della \_ classe TSLicenseReport Win32</span><span class="sxs-lookup"><span data-stu-id="6e494-106">FetchReportFailedPerUserSummaryEntries method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="6e494-107">Recupera le informazioni di riepilogo di Servizi Desktop remoto non riuscite per licenze CAL per utente per utente dal report.</span><span class="sxs-lookup"><span data-stu-id="6e494-107">Retrieves summary information of failed Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e494-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6e494-108">Syntax</span></span>


```mof
uint32 FetchReportFailedPerUserSummaryEntries(
  [in]      uint32                                         StartIndex,
  [in, out] uint32                                         Count,
  [out]     Win32_TSLicenseReportFailedPerUserSummaryEntry ReportFailedPerUserSummaryEntries[]
);
```



## <a name="parameters"></a><span data-ttu-id="6e494-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6e494-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e494-110">*StartIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e494-110">*StartIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e494-111">Indice della prima voce del report da recuperare.</span><span class="sxs-lookup"><span data-stu-id="6e494-111">The index of the first report entry to be retrieved.</span></span> <span data-ttu-id="6e494-112">La prima voce del report ha un indice pari a zero.</span><span class="sxs-lookup"><span data-stu-id="6e494-112">The first report entry has an index of zero.</span></span>

</dd> <dt>

<span data-ttu-id="6e494-113">*Numero* \[ di in uscita\]</span><span class="sxs-lookup"><span data-stu-id="6e494-113">*Count* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e494-114">Numero di voci del report da recuperare dall'oggetto report.</span><span class="sxs-lookup"><span data-stu-id="6e494-114">The number of report entries to retrieve from the report object.</span></span> <span data-ttu-id="6e494-115">Un valore pari a zero indica che devono essere recuperate tutte le voci del report a partire da *startIndex* .</span><span class="sxs-lookup"><span data-stu-id="6e494-115">A value of zero indicates that all of the report entries starting at *StartIndex* are to be retrieved.</span></span> <span data-ttu-id="6e494-116">Nell'output restituito è contenuto il numero di voci nella matrice *ReportFailedPerUserSummaryEntries* .</span><span class="sxs-lookup"><span data-stu-id="6e494-116">On return, contains the number of entries in the *ReportFailedPerUserSummaryEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="6e494-117">*ReportFailedPerUserSummaryEntries* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6e494-117">*ReportFailedPerUserSummaryEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e494-118">Matrice di classi [**\_ TSLicenseReportFailedPerUserSummaryEntry Win32**](win32-tslicensereportfailedperusersummaryentry.md) che rappresentano le voci di licenza recuperate.</span><span class="sxs-lookup"><span data-stu-id="6e494-118">An array of [**Win32\_TSLicenseReportFailedPerUserSummaryEntry**](win32-tslicensereportfailedperusersummaryentry.md) classes that represent the license entries retrieved.</span></span> <span data-ttu-id="6e494-119">Il parametro *count* contiene il numero di elementi in questa matrice.</span><span class="sxs-lookup"><span data-stu-id="6e494-119">The *Count* parameter contains the number of elements in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e494-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6e494-120">Return value</span></span>

<span data-ttu-id="6e494-121">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="6e494-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="6e494-122">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="6e494-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="6e494-123">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6e494-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e494-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e494-124">Requirements</span></span>



| <span data-ttu-id="6e494-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e494-125">Requirement</span></span> | <span data-ttu-id="6e494-126">Valore</span><span class="sxs-lookup"><span data-stu-id="6e494-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e494-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e494-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6e494-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6e494-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="6e494-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e494-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6e494-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6e494-130">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="6e494-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6e494-131">Namespace</span></span><br/>                | <span data-ttu-id="6e494-132">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="6e494-132">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="6e494-133">MOF</span><span class="sxs-lookup"><span data-stu-id="6e494-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e494-134"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6e494-134"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e494-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6e494-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e494-136"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e494-136"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e494-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e494-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e494-138">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="6e494-138">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

 






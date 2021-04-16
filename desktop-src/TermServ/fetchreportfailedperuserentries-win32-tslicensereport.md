---
title: Metodo FetchReportFailedPerUserEntries della classe Win32_TSLicenseReport
description: Recupera i dettagli delle licenze di accesso client non riuscite Servizi Desktop remoto per utente (RDS \ 160; Licenze CAL per utente) dal report.
ms.assetid: 2c16723c-1755-4ec1-a6db-55d769f8b6fd
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo FetchReportFailedPerUserEntries
- Metodo FetchReportFailedPerUserEntries Servizi Desktop remoto, classe Win32_TSLicenseReport
- Classe Win32_TSLicenseReport Servizi Desktop remoto, metodo FetchReportFailedPerUserEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportFailedPerUserEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 159f980944c70dbad4c6948a614d0c9964a5f0cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518844"
---
# <a name="fetchreportfailedperuserentries-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="1ae94-106">Metodo FetchReportFailedPerUserEntries della \_ classe TSLicenseReport Win32</span><span class="sxs-lookup"><span data-stu-id="1ae94-106">FetchReportFailedPerUserEntries method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="1ae94-107">Recupera i dettagli relativi alle licenze CAL per utente non riuscite Servizi Desktop remoto per utente dal report.</span><span class="sxs-lookup"><span data-stu-id="1ae94-107">Retrieves details of failed Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ae94-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ae94-108">Syntax</span></span>


```mof
uint32 FetchReportFailedPerUserEntries(
  [in]      uint32                                  StartIndex,
  [in, out] uint32                                  Count,
  [out]     Win32_TSLicenseReportFailedPerUserEntry ReportFailedPerUserEntries[]
);
```



## <a name="parameters"></a><span data-ttu-id="1ae94-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1ae94-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ae94-110">*StartIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ae94-110">*StartIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae94-111">Indice della prima voce del report da recuperare.</span><span class="sxs-lookup"><span data-stu-id="1ae94-111">The index of the first report entry to be retrieved.</span></span> <span data-ttu-id="1ae94-112">La prima voce del report ha un indice pari a zero.</span><span class="sxs-lookup"><span data-stu-id="1ae94-112">The first report entry has an index of zero.</span></span>

</dd> <dt>

<span data-ttu-id="1ae94-113">*Numero* \[ di in uscita\]</span><span class="sxs-lookup"><span data-stu-id="1ae94-113">*Count* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae94-114">Numero di voci del report da recuperare dall'oggetto report.</span><span class="sxs-lookup"><span data-stu-id="1ae94-114">The number of report entries to retrieve from the report object.</span></span> <span data-ttu-id="1ae94-115">Un valore pari a zero indica che devono essere recuperate tutte le voci del report a partire da *startIndex* .</span><span class="sxs-lookup"><span data-stu-id="1ae94-115">A value of zero indicates that all of the report entries starting at *StartIndex* are to be retrieved.</span></span> <span data-ttu-id="1ae94-116">Nell'output restituito è contenuto il numero di voci nella matrice *ReportFailedPerUserEntries* .</span><span class="sxs-lookup"><span data-stu-id="1ae94-116">On return, contains the number of entries in the *ReportFailedPerUserEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="1ae94-117">*ReportFailedPerUserEntries* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1ae94-117">*ReportFailedPerUserEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae94-118">Matrice di classi [**\_ TSLicenseReportFailedPerUserEntry Win32**](win32-tslicensereportfailedperuserentry.md) che rappresentano le voci di licenza recuperate.</span><span class="sxs-lookup"><span data-stu-id="1ae94-118">An array of [**Win32\_TSLicenseReportFailedPerUserEntry**](win32-tslicensereportfailedperuserentry.md) classes that represent the license entries retrieved.</span></span> <span data-ttu-id="1ae94-119">Il parametro *count* contiene il numero di elementi in questa matrice.</span><span class="sxs-lookup"><span data-stu-id="1ae94-119">The *Count* parameter contains the number of elements in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ae94-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1ae94-120">Return value</span></span>

<span data-ttu-id="1ae94-121">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="1ae94-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="1ae94-122">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="1ae94-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="1ae94-123">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="1ae94-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1ae94-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ae94-124">Requirements</span></span>



| <span data-ttu-id="1ae94-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ae94-125">Requirement</span></span> | <span data-ttu-id="1ae94-126">Valore</span><span class="sxs-lookup"><span data-stu-id="1ae94-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ae94-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ae94-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1ae94-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1ae94-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="1ae94-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ae94-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1ae94-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1ae94-130">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="1ae94-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1ae94-131">Namespace</span></span><br/>                | <span data-ttu-id="1ae94-132">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="1ae94-132">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="1ae94-133">MOF</span><span class="sxs-lookup"><span data-stu-id="1ae94-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ae94-134"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1ae94-134"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ae94-135">DLL</span><span class="sxs-lookup"><span data-stu-id="1ae94-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ae94-136"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ae94-136"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ae94-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ae94-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ae94-138">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="1ae94-138">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

 






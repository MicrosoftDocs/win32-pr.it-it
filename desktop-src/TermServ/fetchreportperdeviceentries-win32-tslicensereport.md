---
title: Metodo FetchReportPerDeviceEntries della classe Win32_TSLicenseReport
description: Recupera le informazioni sulle licenze di accesso client per dispositivo Servizi Desktop remoto emesse (RDS \ 160; Per dispositivo CAL) dal report.
ms.assetid: 3f632a65-d6e0-4efd-9498-d04a05f9ddec
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo FetchReportPerDeviceEntries
- Metodo FetchReportPerDeviceEntries Servizi Desktop remoto, classe Win32_TSLicenseReport
- Classe Win32_TSLicenseReport Servizi Desktop remoto, metodo FetchReportPerDeviceEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportPerDeviceEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce77fce941dd0a24fb6ee17e0aeb67b4e78bdae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302477"
---
# <a name="fetchreportperdeviceentries-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="f3272-106">Metodo FetchReportPerDeviceEntries della \_ classe TSLicenseReport Win32</span><span class="sxs-lookup"><span data-stu-id="f3272-106">FetchReportPerDeviceEntries method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="f3272-107">Recupera le informazioni sulle licenze di accesso client per dispositivo di Servizi Desktop remoto emesse dal report.</span><span class="sxs-lookup"><span data-stu-id="f3272-107">Retrieves information of issued Remote Desktop Services Per Device client access licenses (RDS Per Device CALs) from the report.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3272-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3272-108">Syntax</span></span>


```mof
uint32 FetchReportPerDeviceEntries(
  [in]      uint32                              StartIndex,
  [in, out] uint32                              Count,
  [out]     Win32_TSLicenseReportPerDeviceEntry ReportPerDeviceEntries[]
);
```



## <a name="parameters"></a><span data-ttu-id="f3272-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f3272-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3272-110">*StartIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f3272-110">*StartIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3272-111">Indice della prima voce del report da recuperare.</span><span class="sxs-lookup"><span data-stu-id="f3272-111">The index of the first report entry to be retrieved.</span></span> <span data-ttu-id="f3272-112">La prima voce del report ha un indice pari a zero.</span><span class="sxs-lookup"><span data-stu-id="f3272-112">The first report entry has an index of zero.</span></span>

</dd> <dt>

<span data-ttu-id="f3272-113">*Numero* \[ di in uscita\]</span><span class="sxs-lookup"><span data-stu-id="f3272-113">*Count* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3272-114">Numero di voci del report da recuperare dall'oggetto report.</span><span class="sxs-lookup"><span data-stu-id="f3272-114">The number of report entries to retrieve from the report object.</span></span> <span data-ttu-id="f3272-115">Un valore pari a zero indica che devono essere recuperate tutte le voci del report a partire da *startIndex* .</span><span class="sxs-lookup"><span data-stu-id="f3272-115">A value of zero indicates that all of the report entries starting at *StartIndex* are to be retrieved.</span></span> <span data-ttu-id="f3272-116">Nell'output restituito è contenuto il numero di voci nella matrice *ReportPerDeviceEntries* .</span><span class="sxs-lookup"><span data-stu-id="f3272-116">On return, contains the number of entries in the *ReportPerDeviceEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="f3272-117">*ReportPerDeviceEntries* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f3272-117">*ReportPerDeviceEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3272-118">Matrice di classi [**\_ TSLicenseReportPerDeviceEntry Win32**](win32-tslicensereportperdeviceentry.md) che rappresentano le voci di licenza recuperate.</span><span class="sxs-lookup"><span data-stu-id="f3272-118">An array of [**Win32\_TSLicenseReportPerDeviceEntry**](win32-tslicensereportperdeviceentry.md) classes the represent the license entries retrieved.</span></span> <span data-ttu-id="f3272-119">Il parametro *count* contiene il numero di elementi in questa matrice.</span><span class="sxs-lookup"><span data-stu-id="f3272-119">The *Count* parameter contains the number of elements in this array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3272-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f3272-120">Return value</span></span>

<span data-ttu-id="f3272-121">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="f3272-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="f3272-122">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="f3272-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="f3272-123">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f3272-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f3272-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3272-124">Requirements</span></span>



| <span data-ttu-id="f3272-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3272-125">Requirement</span></span> | <span data-ttu-id="f3272-126">Valore</span><span class="sxs-lookup"><span data-stu-id="f3272-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3272-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3272-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f3272-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f3272-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="f3272-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3272-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f3272-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f3272-130">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="f3272-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f3272-131">Namespace</span></span><br/>                | <span data-ttu-id="f3272-132">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="f3272-132">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="f3272-133">MOF</span><span class="sxs-lookup"><span data-stu-id="f3272-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3272-134"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3272-134"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3272-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f3272-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3272-136"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3272-136"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3272-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3272-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3272-138">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="f3272-138">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 

 






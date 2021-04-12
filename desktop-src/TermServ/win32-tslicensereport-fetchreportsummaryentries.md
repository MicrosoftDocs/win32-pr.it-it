---
title: Metodo FetchReportSummaryEntries della classe Win32_TSLicenseReport
description: Recupera i riepiloghi delle licenze di accesso client di Servizi Desktop remoto per utente (RDS \ 160; Licenze CAL per utente) dal report.
ms.assetid: 0312B787-83E9-42FC-B21B-904B804C5C94
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo FetchReportSummaryEntries
- Metodo FetchReportSummaryEntries Servizi Desktop remoto, classe Win32_TSLicenseReport
- Classe Win32_TSLicenseReport Servizi Desktop remoto, metodo FetchReportSummaryEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportSummaryEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e47100c71e195cacb6a1004975955eae778765a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119115"
---
# <a name="fetchreportsummaryentries-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="30a8f-106">Metodo FetchReportSummaryEntries della \_ classe TSLicenseReport Win32</span><span class="sxs-lookup"><span data-stu-id="30a8f-106">FetchReportSummaryEntries method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="30a8f-107">Recupera i riepiloghi delle licenze CAL per utente Servizi Desktop remoto per utente dal report.</span><span class="sxs-lookup"><span data-stu-id="30a8f-107">Retrieves summaries of Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span>

## <a name="syntax"></a><span data-ttu-id="30a8f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="30a8f-108">Syntax</span></span>


```mof
uint32 FetchReportSummaryEntries(
  [in]      uint32                            StartIndex,
  [in, out] uint32                            Count,
  [out]     Win32_TSLicenseReportSummaryEntry ReportSummaryEntries[]
);
```



## <a name="parameters"></a><span data-ttu-id="30a8f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="30a8f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30a8f-110">*StartIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30a8f-110">*StartIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30a8f-111">Indice della prima voce del report da ricevere.</span><span class="sxs-lookup"><span data-stu-id="30a8f-111">Index of the first report entry to be received.</span></span> <span data-ttu-id="30a8f-112">La prima voce del report ha un indice pari a zero.</span><span class="sxs-lookup"><span data-stu-id="30a8f-112">The first report entry has an index of zero.</span></span>

</dd> <dt>

<span data-ttu-id="30a8f-113">*Numero* \[ di in uscita\]</span><span class="sxs-lookup"><span data-stu-id="30a8f-113">*Count* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="30a8f-114">Numero di voci del report da recuperare dall'oggetto report.</span><span class="sxs-lookup"><span data-stu-id="30a8f-114">Number of report entries to retrieve from the report object.</span></span> <span data-ttu-id="30a8f-115">Un valore pari a zero indica che devono essere recuperate tutte le voci del report a partire da *startIndex* .</span><span class="sxs-lookup"><span data-stu-id="30a8f-115">A value of zero indicates that all of the report entries starting at *StartIndex* are to be retrieved.</span></span> <span data-ttu-id="30a8f-116">Nell'output restituito è contenuto il numero di voci nella matrice *ReportSummaryEntries* .</span><span class="sxs-lookup"><span data-stu-id="30a8f-116">On return, contains the number of entries in the *ReportSummaryEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="30a8f-117">*ReportSummaryEntries* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="30a8f-117">*ReportSummaryEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30a8f-118">Restituisce una matrice di [**classi \_ TSLicenseReportSummaryEntry Win32**](win32-tslicensereportsummaryentry.md) .</span><span class="sxs-lookup"><span data-stu-id="30a8f-118">Returns an array of [**Win32\_TSLicenseReportSummaryEntry**](win32-tslicensereportsummaryentry.md) classes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30a8f-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="30a8f-119">Return value</span></span>

<span data-ttu-id="30a8f-120">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="30a8f-120">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="30a8f-121">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="30a8f-121">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="30a8f-122">Il valore **LSERVER non \_ \_ \_ più \_ dati** (0x4001) indica che non sono presenti altre voci del report.</span><span class="sxs-lookup"><span data-stu-id="30a8f-122">A value of **LSERVER\_I\_NO\_MORE\_DATA** (0x4001) indicates that there are no more report entries.</span></span>

## <a name="remarks"></a><span data-ttu-id="30a8f-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="30a8f-123">Remarks</span></span>

<span data-ttu-id="30a8f-124">Non si tratta di un metodo statico.</span><span class="sxs-lookup"><span data-stu-id="30a8f-124">This is not a static method.</span></span> <span data-ttu-id="30a8f-125">Questo metodo deve essere chiamato da un oggetto report utilizzo licenze per utente.</span><span class="sxs-lookup"><span data-stu-id="30a8f-125">This method must be called from a per user license usage report object.</span></span>

<span data-ttu-id="30a8f-126">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="30a8f-126">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="30a8f-127">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="30a8f-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="30a8f-128">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="30a8f-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="30a8f-129">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="30a8f-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="30a8f-130">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="30a8f-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="30a8f-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30a8f-131">Requirements</span></span>



| <span data-ttu-id="30a8f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="30a8f-132">Requirement</span></span> | <span data-ttu-id="30a8f-133">Valore</span><span class="sxs-lookup"><span data-stu-id="30a8f-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="30a8f-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30a8f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="30a8f-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="30a8f-135">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="30a8f-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30a8f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="30a8f-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30a8f-137">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="30a8f-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="30a8f-138">Namespace</span></span><br/>                | <span data-ttu-id="30a8f-139">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="30a8f-139">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="30a8f-140">MOF</span><span class="sxs-lookup"><span data-stu-id="30a8f-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="30a8f-141"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="30a8f-141"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="30a8f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="30a8f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30a8f-143"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30a8f-143"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30a8f-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30a8f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30a8f-145">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="30a8f-145">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="30a8f-146">**\_TSLicenseReportSummaryEntry Win32**</span><span class="sxs-lookup"><span data-stu-id="30a8f-146">**Win32\_TSLicenseReportSummaryEntry**</span></span>](win32-tslicensereportsummaryentry.md)
</dt> </dl>

 


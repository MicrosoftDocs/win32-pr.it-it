---
title: Metodo FetchReportEntries della classe Win32_TSLicenseReport
description: Recupera i dettagli delle licenze di accesso client di Servizi Desktop remoto per utente (RDS \ 160; Licenze CAL per utente) dal report. Ogni voce rappresenta un RDS \ 160; Licenza CAL per utente attualmente in uso.
ms.assetid: 151ff95c-4ad3-4d19-936d-1cb08b4d5056
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo FetchReportEntries
- Metodo FetchReportEntries Servizi Desktop remoto, classe Win32_TSLicenseReport
- Classe Win32_TSLicenseReport Servizi Desktop remoto, metodo FetchReportEntries
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.FetchReportEntries
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc64c9591444307ba0519da02cf9c6f13d20252e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518849"
---
# <a name="fetchreportentries-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="e9f82-107">Metodo FetchReportEntries della \_ classe TSLicenseReport Win32</span><span class="sxs-lookup"><span data-stu-id="e9f82-107">FetchReportEntries method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="e9f82-108">Recupera i dettagli di Servizi Desktop remoto licenze CAL per utente per utente dal report.</span><span class="sxs-lookup"><span data-stu-id="e9f82-108">Retrieves details of Remote Desktop Services Per User client access licenses (RDS Per User CALs) from the report.</span></span> <span data-ttu-id="e9f82-109">Ogni voce rappresenta una licenza CAL per utente per utente attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="e9f82-109">Each entry represents a RDS Per User CAL that is currently in use.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9f82-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9f82-110">Syntax</span></span>


```mof
uint32 FetchReportEntries(
  [in]      uint32                     StartIndex,
  [in, out] uint32                     Count,
  [out]     Win32_TSLicenseReportEntry ReportEntries[]
);
```



## <a name="parameters"></a><span data-ttu-id="e9f82-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9f82-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9f82-112">*StartIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e9f82-112">*StartIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9f82-113">Indice della prima voce del report da ricevere.</span><span class="sxs-lookup"><span data-stu-id="e9f82-113">Index of the first report entry to be received.</span></span> <span data-ttu-id="e9f82-114">La prima voce del report ha un indice pari a zero.</span><span class="sxs-lookup"><span data-stu-id="e9f82-114">The first report entry has an index of zero.</span></span>

</dd> <dt>

<span data-ttu-id="e9f82-115">*Numero* \[ di in uscita\]</span><span class="sxs-lookup"><span data-stu-id="e9f82-115">*Count* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9f82-116">Numero di voci del report da recuperare dall'oggetto report.</span><span class="sxs-lookup"><span data-stu-id="e9f82-116">Number of report entries to retrieve from the report object.</span></span> <span data-ttu-id="e9f82-117">Un valore pari a zero indica che devono essere recuperate tutte le voci del report a partire da *startIndex* .</span><span class="sxs-lookup"><span data-stu-id="e9f82-117">A value of zero indicates that all of the report entries starting at *StartIndex* are to be retrieved.</span></span> <span data-ttu-id="e9f82-118">Nell'output restituito è contenuto il numero di voci nella matrice *ReportEntries* .</span><span class="sxs-lookup"><span data-stu-id="e9f82-118">On return, contains the number of entries in the *ReportEntries* array.</span></span>

</dd> <dt>

<span data-ttu-id="e9f82-119">*ReportEntries* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e9f82-119">*ReportEntries* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9f82-120">Restituisce una matrice di [**classi \_ TSLicenseReportEntry Win32**](win32-tslicensereportentry.md) .</span><span class="sxs-lookup"><span data-stu-id="e9f82-120">Returns an array of [**Win32\_TSLicenseReportEntry**](win32-tslicensereportentry.md) classes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9f82-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9f82-121">Return value</span></span>

<span data-ttu-id="e9f82-122">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="e9f82-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e9f82-123">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="e9f82-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e9f82-124">Il valore **LSERVER non \_ \_ \_ più \_ dati** (0x4001) indica che non sono presenti altre voci del report.</span><span class="sxs-lookup"><span data-stu-id="e9f82-124">A value of **LSERVER\_I\_NO\_MORE\_DATA** (0x4001) indicates that there are no more report entries.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9f82-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9f82-125">Remarks</span></span>

<span data-ttu-id="e9f82-126">Non si tratta di un metodo statico.</span><span class="sxs-lookup"><span data-stu-id="e9f82-126">This is not a static method.</span></span> <span data-ttu-id="e9f82-127">Questo metodo deve essere chiamato da un oggetto report utilizzo licenze per utente.</span><span class="sxs-lookup"><span data-stu-id="e9f82-127">This method must be called from a per user license usage report object.</span></span>

<span data-ttu-id="e9f82-128">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="e9f82-128">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="e9f82-129">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="e9f82-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e9f82-130">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="e9f82-130">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e9f82-131">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="e9f82-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e9f82-132">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e9f82-132">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e9f82-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9f82-133">Requirements</span></span>



| <span data-ttu-id="e9f82-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9f82-134">Requirement</span></span> | <span data-ttu-id="e9f82-135">Valore</span><span class="sxs-lookup"><span data-stu-id="e9f82-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9f82-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9f82-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e9f82-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e9f82-137">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="e9f82-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9f82-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e9f82-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9f82-139">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="e9f82-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e9f82-140">Namespace</span></span><br/>                | <span data-ttu-id="e9f82-141">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="e9f82-141">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="e9f82-142">MOF</span><span class="sxs-lookup"><span data-stu-id="e9f82-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9f82-143"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9f82-143"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9f82-144">DLL</span><span class="sxs-lookup"><span data-stu-id="e9f82-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9f82-145"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9f82-145"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9f82-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9f82-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9f82-147">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="e9f82-147">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="e9f82-148">**\_TSLicenseReportEntry Win32**</span><span class="sxs-lookup"><span data-stu-id="e9f82-148">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> </dl>

 


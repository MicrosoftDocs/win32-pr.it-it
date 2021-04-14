---
title: Metodo GenerateReport della classe Win32_TSLicenseReport (gpmgmt. h)
description: GenerateReport non è più disponibile per l'uso a partire da Windows Server 2012.
ms.assetid: 2d3b16d6-52e8-491f-b6e5-419e9a21013b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GenerateReport
- Metodo GenerateReport Servizi Desktop remoto, classe Win32_TSLicenseReport
- Classe Win32_TSLicenseReport Servizi Desktop remoto, metodo GenerateReport
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.GenerateReport
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a5231c87d379decac8d4f6491042bff735c1ba2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400791"
---
# <a name="generatereport-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="4794d-106">Metodo GenerateReport della \_ classe TSLicenseReport Win32</span><span class="sxs-lookup"><span data-stu-id="4794d-106">GenerateReport method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="4794d-107">\[**GenerateReport** non è più disponibile per l'uso a partire da Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="4794d-107">\[**GenerateReport** is no longer available for use as of Windows Server 2012.</span></span> <span data-ttu-id="4794d-108">Usare invece [**GenerateReportEx**](generatereportex-win32-tslicensereport.md).\]</span><span class="sxs-lookup"><span data-stu-id="4794d-108">Instead, use [**GenerateReportEx**](generatereportex-win32-tslicensereport.md).\]</span></span>

<span data-ttu-id="4794d-109">Questo metodo non è supportato.</span><span class="sxs-lookup"><span data-stu-id="4794d-109">This method is not supported.</span></span>

<span data-ttu-id="4794d-110">**Windows server 2008 R2 e Windows server 2008:** Genera un report di utilizzo delle licenze per utente corrente nel server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="4794d-110">**Windows Server 2008 R2 and Windows Server 2008:** Generates a current per user license usage report on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="4794d-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4794d-111">Syntax</span></span>


```mof
uint32 GenerateReport(
  [in]  uint32 ScopeType,
  [in]  string ScopeValue,
  [out] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="4794d-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="4794d-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4794d-113">*ScopeType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4794d-113">*ScopeType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4794d-114">Ambito del report utilizzo licenze.</span><span class="sxs-lookup"><span data-stu-id="4794d-114">Scope of the license usage report.</span></span> <span data-ttu-id="4794d-115">Può contenere i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="4794d-115">It can have the following values.</span></span>

<dt>

<span data-ttu-id="4794d-116">1</span><span class="sxs-lookup"><span data-stu-id="4794d-116">1</span></span>
</dt> <dd>

<span data-ttu-id="4794d-117">Il report verrà generato per l'intero dominio.</span><span class="sxs-lookup"><span data-stu-id="4794d-117">The report will be generated for the entire domain.</span></span>

</dd> <dt>

<span data-ttu-id="4794d-118">2</span><span class="sxs-lookup"><span data-stu-id="4794d-118">2</span></span>
</dt> <dd>

<span data-ttu-id="4794d-119">Il report verrà generato per l'unità organizzativa (OU) specificata nel parametro *ScopeValue* .</span><span class="sxs-lookup"><span data-stu-id="4794d-119">The report will be generated for the organizational unit (OU) that is specified in the *ScopeValue* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4794d-120">3</span><span class="sxs-lookup"><span data-stu-id="4794d-120">3</span></span>
</dt> <dd>

<span data-ttu-id="4794d-121">Il report verrà generato per tutti i domini trusted.</span><span class="sxs-lookup"><span data-stu-id="4794d-121">The report will be generated for all trusted domains.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4794d-122">*ScopeValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4794d-122">*ScopeValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4794d-123">Se il parametro *ScopeType* è 2, *ScopeType* specifica l'unità organizzativa per la quale verrà generato il report.</span><span class="sxs-lookup"><span data-stu-id="4794d-123">If the *ScopeType* parameter is 2, *ScopeType* specifies the OU for which the report will be generated.</span></span> <span data-ttu-id="4794d-124">È necessario specificare *ScopeValue* usando il formato **ou =**_OUName1_*_, ou =_*_OUName2_*_..._*.</span><span class="sxs-lookup"><span data-stu-id="4794d-124">You must specify *ScopeValue* by using the format **OU=**_OUName1_*_,OU=_*_OUName2_*_..._*.</span></span>

</dd> <dt>

<span data-ttu-id="4794d-125">*Nome file* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4794d-125">*FileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4794d-126">Nome file del report generato.</span><span class="sxs-lookup"><span data-stu-id="4794d-126">The file name of the generated report.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4794d-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4794d-127">Return value</span></span>

<span data-ttu-id="4794d-128">Restituisce **WBEM \_ E \_ non \_ supportato**.</span><span class="sxs-lookup"><span data-stu-id="4794d-128">Returns **WBEM\_E\_NOT\_SUPPORTED**.</span></span>

<span data-ttu-id="4794d-129">**Windows server 2008 R2 e Windows server 2008:** Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="4794d-129">**Windows Server 2008 R2 and Windows Server 2008:** If the method succeeds, it returns zero.</span></span> <span data-ttu-id="4794d-130">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="4794d-130">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="4794d-131">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="4794d-131">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4794d-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="4794d-132">Remarks</span></span>

<span data-ttu-id="4794d-133">Si tratta di un metodo statico.</span><span class="sxs-lookup"><span data-stu-id="4794d-133">This is a static method.</span></span>

<span data-ttu-id="4794d-134">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="4794d-134">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="4794d-135">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="4794d-135">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4794d-136">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="4794d-136">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4794d-137">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="4794d-137">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4794d-138">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="4794d-138">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4794d-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4794d-139">Requirements</span></span>



| <span data-ttu-id="4794d-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="4794d-140">Requirement</span></span> | <span data-ttu-id="4794d-141">Valore</span><span class="sxs-lookup"><span data-stu-id="4794d-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4794d-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4794d-142">Minimum supported client</span></span><br/> | <span data-ttu-id="4794d-143">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4794d-143">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="4794d-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4794d-144">Minimum supported server</span></span><br/> | <span data-ttu-id="4794d-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4794d-145">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="4794d-146">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="4794d-146">End of client support</span></span><br/>    | <span data-ttu-id="4794d-147">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4794d-147">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="4794d-148">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="4794d-148">End of server support</span></span><br/>    | <span data-ttu-id="4794d-149">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4794d-149">Windows Server 2008 R2</span></span><br/>                                                         |
| <span data-ttu-id="4794d-150">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4794d-150">Namespace</span></span><br/>                | <span data-ttu-id="4794d-151">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="4794d-151">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="4794d-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4794d-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="4794d-153"><dt>Gpmgmt. h</dt></span><span class="sxs-lookup"><span data-stu-id="4794d-153"><dt>Gpmgmt.h</dt></span></span> </dl>       |
| <span data-ttu-id="4794d-154">MOF</span><span class="sxs-lookup"><span data-stu-id="4794d-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4794d-155"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4794d-155"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="4794d-156">DLL</span><span class="sxs-lookup"><span data-stu-id="4794d-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4794d-157"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4794d-157"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4794d-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4794d-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4794d-159">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="4794d-159">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 


---
title: Metodo GenerateReportEx della classe Win32_TSLicenseReport
description: Genera un report sull'utilizzo delle licenze corrente per le licenze per utente e per dispositivo.
ms.assetid: c454e0c5-ca1c-41c7-86b2-1e52c414aeb5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GenerateReportEx
- Metodo GenerateReportEx Servizi Desktop remoto, classe Win32_TSLicenseReport
- Classe Win32_TSLicenseReport Servizi Desktop remoto, metodo GenerateReportEx
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.GenerateReportEx
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 893e6e29d1e4716560b0f0f6b41e6109c89e2f5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400323"
---
# <a name="generatereportex-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="07606-106">Metodo GenerateReportEx della \_ classe TSLicenseReport Win32</span><span class="sxs-lookup"><span data-stu-id="07606-106">GenerateReportEx method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="07606-107">Genera un report sull'utilizzo delle licenze corrente per le licenze per utente e per dispositivo.</span><span class="sxs-lookup"><span data-stu-id="07606-107">Generates a current license usage report for both Per User and Per Device licenses.</span></span>

## <a name="syntax"></a><span data-ttu-id="07606-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07606-108">Syntax</span></span>


```mof
uint32 GenerateReportEx(
  [out] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="07606-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="07606-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07606-110">*Nome file* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="07606-110">*FileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="07606-111">Nome file del report generato.</span><span class="sxs-lookup"><span data-stu-id="07606-111">The file name of the generated report.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07606-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="07606-112">Return value</span></span>

<span data-ttu-id="07606-113">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="07606-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="07606-114">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="07606-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="07606-115">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="07606-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="07606-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="07606-116">Remarks</span></span>

<span data-ttu-id="07606-117">Si tratta di un metodo statico.</span><span class="sxs-lookup"><span data-stu-id="07606-117">This is a static method.</span></span>

<span data-ttu-id="07606-118">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="07606-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="07606-119">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="07606-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="07606-120">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="07606-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="07606-121">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="07606-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="07606-122">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="07606-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="07606-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07606-123">Requirements</span></span>



| <span data-ttu-id="07606-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="07606-124">Requirement</span></span> | <span data-ttu-id="07606-125">Valore</span><span class="sxs-lookup"><span data-stu-id="07606-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="07606-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07606-126">Minimum supported client</span></span><br/> | <span data-ttu-id="07606-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="07606-127">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="07606-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07606-128">Minimum supported server</span></span><br/> | <span data-ttu-id="07606-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="07606-129">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="07606-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="07606-130">Namespace</span></span><br/>                | <span data-ttu-id="07606-131">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="07606-131">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="07606-132">MOF</span><span class="sxs-lookup"><span data-stu-id="07606-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07606-133"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="07606-133"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="07606-134">DLL</span><span class="sxs-lookup"><span data-stu-id="07606-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07606-135"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07606-135"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07606-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07606-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07606-137">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="07606-137">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 


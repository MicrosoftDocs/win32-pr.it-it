---
title: Metodo DeleteReport della classe Win32_TSLicenseReport
description: Elimina un oggetto report nel server licenze Desktop remoto. Non si tratta di un metodo statico.
ms.assetid: cc70526c-7ce5-4d55-b72e-8a5e8799b1d8
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo DeleteReport
- Metodo DeleteReport Servizi Desktop remoto, classe Win32_TSLicenseReport
- Classe Win32_TSLicenseReport Servizi Desktop remoto, metodo DeleteReport
topic_type:
- apiref
api_name:
- Win32_TSLicenseReport.DeleteReport
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5a96c8626e4ecc1f89d0f2fcefa69845fec4df8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517451"
---
# <a name="deletereport-method-of-the-win32_tslicensereport-class"></a><span data-ttu-id="224ce-107">Metodo DeleteReport della \_ classe TSLicenseReport Win32</span><span class="sxs-lookup"><span data-stu-id="224ce-107">DeleteReport method of the Win32\_TSLicenseReport class</span></span>

<span data-ttu-id="224ce-108">Elimina un oggetto report nel server licenze Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="224ce-108">Deletes a report object on the Remote Desktop license server.</span></span> <span data-ttu-id="224ce-109">Non si tratta di un metodo statico.</span><span class="sxs-lookup"><span data-stu-id="224ce-109">This is not a static method.</span></span>

## <a name="syntax"></a><span data-ttu-id="224ce-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="224ce-110">Syntax</span></span>


```mof
uint32 DeleteReport();
```



## <a name="parameters"></a><span data-ttu-id="224ce-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="224ce-111">Parameters</span></span>

<span data-ttu-id="224ce-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="224ce-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="224ce-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="224ce-113">Return value</span></span>

<span data-ttu-id="224ce-114">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="224ce-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="224ce-115">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="224ce-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="224ce-116">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="224ce-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="224ce-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="224ce-117">Remarks</span></span>

<span data-ttu-id="224ce-118">Non si tratta di un metodo statico.</span><span class="sxs-lookup"><span data-stu-id="224ce-118">This is not a static method.</span></span> <span data-ttu-id="224ce-119">Questo metodo deve essere chiamato da un oggetto report utilizzo licenze per utente.</span><span class="sxs-lookup"><span data-stu-id="224ce-119">This method must be called from a per user license usage report object.</span></span>

<span data-ttu-id="224ce-120">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="224ce-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="224ce-121">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="224ce-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="224ce-122">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="224ce-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="224ce-123">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="224ce-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="224ce-124">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="224ce-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="224ce-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="224ce-125">Requirements</span></span>



| <span data-ttu-id="224ce-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="224ce-126">Requirement</span></span> | <span data-ttu-id="224ce-127">Valore</span><span class="sxs-lookup"><span data-stu-id="224ce-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="224ce-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="224ce-128">Minimum supported client</span></span><br/> | <span data-ttu-id="224ce-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="224ce-129">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="224ce-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="224ce-130">Minimum supported server</span></span><br/> | <span data-ttu-id="224ce-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="224ce-131">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="224ce-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="224ce-132">Namespace</span></span><br/>                | <span data-ttu-id="224ce-133">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="224ce-133">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="224ce-134">MOF</span><span class="sxs-lookup"><span data-stu-id="224ce-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="224ce-135"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="224ce-135"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="224ce-136">DLL</span><span class="sxs-lookup"><span data-stu-id="224ce-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="224ce-137"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="224ce-137"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="224ce-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="224ce-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="224ce-139">**\_TSLicenseReport Win32**</span><span class="sxs-lookup"><span data-stu-id="224ce-139">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> </dl>

 


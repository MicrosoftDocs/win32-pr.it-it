---
title: Metodo IsLSPublished della classe Win32_TSLicenseServer
description: Recupera un valore che indica se il server licenze Desktop remoto è pubblicato in Active Directory Domain Services (AD \ 160; DS).
ms.assetid: 0e97c9df-5cb0-4e28-8436-08093a8667d9
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo IsLSPublished
- Metodo IsLSPublished Servizi Desktop remoto, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Servizi Desktop remoto, metodo IsLSPublished
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSPublished
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69add751497ed52a107ea7183bb4b7cce4ea88c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301866"
---
# <a name="islspublished-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="f09bc-106">Metodo IsLSPublished della \_ classe TSLicenseServer Win32</span><span class="sxs-lookup"><span data-stu-id="f09bc-106">IsLSPublished method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="f09bc-107">Recupera un valore che indica se il server licenze Desktop remoto è pubblicato in Active Directory Domain Services (AD DS).</span><span class="sxs-lookup"><span data-stu-id="f09bc-107">Retrieves whether the Remote Desktop license server is published in Active Directory Domain Services (AD DS).</span></span>

## <a name="syntax"></a><span data-ttu-id="f09bc-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f09bc-108">Syntax</span></span>


```mof
uint32 IsLSPublished(
  [out] boolean Published
);
```



## <a name="parameters"></a><span data-ttu-id="f09bc-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f09bc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f09bc-110">*Edizione pubblicata* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f09bc-110">*Published* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f09bc-111">Valore booleano che indica se il server licenze è pubblicato in servizi di dominio Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f09bc-111">Boolean value that indicates whether the license server is published in AD DS.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f09bc-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f09bc-112">Return value</span></span>

<span data-ttu-id="f09bc-113">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="f09bc-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="f09bc-114">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="f09bc-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="f09bc-115">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f09bc-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f09bc-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="f09bc-116">Remarks</span></span>

<span data-ttu-id="f09bc-117">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="f09bc-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="f09bc-118">Se il server licenze è pubblicato in servizi di dominio Active Directory, sarà individuabile automaticamente dai server host sessione Desktop remoto (host sessione Desktop remoto) nella stessa foresta.</span><span class="sxs-lookup"><span data-stu-id="f09bc-118">If the license server is published in AD DS, it will be automatically discoverable by Remote Desktop Session Host (RD Session Host) servers in the same forest.</span></span>

<span data-ttu-id="f09bc-119">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f09bc-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f09bc-120">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="f09bc-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f09bc-121">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="f09bc-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f09bc-122">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f09bc-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f09bc-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f09bc-123">Requirements</span></span>



| <span data-ttu-id="f09bc-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f09bc-124">Requirement</span></span> | <span data-ttu-id="f09bc-125">Valore</span><span class="sxs-lookup"><span data-stu-id="f09bc-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f09bc-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f09bc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f09bc-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f09bc-127">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="f09bc-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f09bc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f09bc-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f09bc-129">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="f09bc-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f09bc-130">Namespace</span></span><br/>                | <span data-ttu-id="f09bc-131">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="f09bc-131">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="f09bc-132">MOF</span><span class="sxs-lookup"><span data-stu-id="f09bc-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f09bc-133"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f09bc-133"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f09bc-134">DLL</span><span class="sxs-lookup"><span data-stu-id="f09bc-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f09bc-135"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f09bc-135"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f09bc-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f09bc-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f09bc-137">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="f09bc-137">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 


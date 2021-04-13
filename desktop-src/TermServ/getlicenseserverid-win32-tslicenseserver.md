---
title: Metodo GetLicenseServerId della classe Win32_TSLicenseServer
description: Recupera l'identificatore del server licenze Desktop remoto se il server è attualmente attivato.
ms.assetid: 0eb2cf82-3632-4693-97d2-0cfa814d8c94
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetLicenseServerId
- Metodo GetLicenseServerId Servizi Desktop remoto, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Servizi Desktop remoto, metodo GetLicenseServerId
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.GetLicenseServerId
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43a5883a5a52a0d111959e1f9fc1cbe9da5357d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400459"
---
# <a name="getlicenseserverid-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="c2628-106">Metodo GetLicenseServerId della \_ classe TSLicenseServer Win32</span><span class="sxs-lookup"><span data-stu-id="c2628-106">GetLicenseServerId method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="c2628-107">Recupera l'identificatore del server licenze Desktop remoto se il server è attualmente attivato.</span><span class="sxs-lookup"><span data-stu-id="c2628-107">Retrieves the Remote Desktop license server identifier if the server is currently activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2628-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c2628-108">Syntax</span></span>


```mof
uint32 GetLicenseServerId(
  [out] string sLicenseServerId
);
```



## <a name="parameters"></a><span data-ttu-id="c2628-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c2628-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2628-110">*sLicenseServerId* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c2628-110">*sLicenseServerId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2628-111">Desktop remoto identificatore del server licenze.</span><span class="sxs-lookup"><span data-stu-id="c2628-111">Remote Desktop license server identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2628-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c2628-112">Return value</span></span>

<span data-ttu-id="c2628-113">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="c2628-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="c2628-114">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="c2628-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="c2628-115">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c2628-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c2628-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="c2628-116">Remarks</span></span>

<span data-ttu-id="c2628-117">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="c2628-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="c2628-118">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="c2628-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c2628-119">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="c2628-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c2628-120">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="c2628-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c2628-121">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c2628-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c2628-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2628-122">Requirements</span></span>



| <span data-ttu-id="c2628-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2628-123">Requirement</span></span> | <span data-ttu-id="c2628-124">Valore</span><span class="sxs-lookup"><span data-stu-id="c2628-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2628-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2628-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c2628-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c2628-126">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="c2628-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2628-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c2628-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2628-128">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="c2628-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c2628-129">Namespace</span></span><br/>                | <span data-ttu-id="c2628-130">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="c2628-130">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="c2628-131">MOF</span><span class="sxs-lookup"><span data-stu-id="c2628-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2628-132"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c2628-132"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c2628-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c2628-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2628-134"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2628-134"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2628-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2628-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2628-136">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="c2628-136">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 


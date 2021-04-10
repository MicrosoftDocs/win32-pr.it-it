---
title: Metodo IsLSonDC della classe Win32_TSLicenseServer
description: Recupera un valore che indica se in un controller di dominio è installato Desktop remoto Licensing (licenze Desktop remoto).
ms.assetid: 43345dc8-c8b6-4c41-b26d-781293d07516
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo IsLSonDC
- Metodo IsLSonDC Servizi Desktop remoto, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Servizi Desktop remoto, metodo IsLSonDC
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSonDC
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03ddbf01615903150ffa8f97fca88cfcf7fda937
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964418"
---
# <a name="islsondc-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="b59a0-106">Metodo IsLSonDC della \_ classe TSLicenseServer Win32</span><span class="sxs-lookup"><span data-stu-id="b59a0-106">IsLSonDC method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="b59a0-107">Recupera un valore che indica se in un controller di dominio è installato Desktop remoto Licensing (licenze Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="b59a0-107">Retrieves whether Remote Desktop Licensing (RD Licensing) is installed on a domain controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="b59a0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b59a0-108">Syntax</span></span>


```mof
uint32 IsLSonDC(
  [out] boolean OnDC
);
```



## <a name="parameters"></a><span data-ttu-id="b59a0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b59a0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b59a0-110">*OnDC* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b59a0-110">*OnDC* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b59a0-111">Valore booleano che indica se il servizio licenze Desktop remoto è installato in un controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="b59a0-111">Boolean value that indicates whether RD Licensing is installed on a domain controller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b59a0-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b59a0-112">Return value</span></span>

<span data-ttu-id="b59a0-113">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="b59a0-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b59a0-114">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="b59a0-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b59a0-115">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b59a0-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b59a0-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="b59a0-116">Remarks</span></span>

<span data-ttu-id="b59a0-117">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="b59a0-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="b59a0-118">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b59a0-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b59a0-119">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="b59a0-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b59a0-120">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="b59a0-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b59a0-121">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b59a0-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b59a0-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b59a0-122">Requirements</span></span>



| <span data-ttu-id="b59a0-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b59a0-123">Requirement</span></span> | <span data-ttu-id="b59a0-124">Valore</span><span class="sxs-lookup"><span data-stu-id="b59a0-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b59a0-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b59a0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b59a0-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b59a0-126">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="b59a0-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b59a0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b59a0-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b59a0-128">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="b59a0-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b59a0-129">Namespace</span></span><br/>                | <span data-ttu-id="b59a0-130">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="b59a0-130">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="b59a0-131">MOF</span><span class="sxs-lookup"><span data-stu-id="b59a0-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b59a0-132"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b59a0-132"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b59a0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b59a0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b59a0-134"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b59a0-134"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b59a0-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b59a0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b59a0-136">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="b59a0-136">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 


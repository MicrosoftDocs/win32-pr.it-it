---
title: Metodo RemoveLSfromTSLSGroup della classe Win32_TSLicenseServer
description: Rimuove il server licenze Desktop remoto dal gruppo server licenze Servizi Desktop remoto in un controller di dominio nello stesso dominio del server licenze.
ms.assetid: 5ed4595b-0668-4dd8-953e-b6fc61088cfd
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RemoveLSfromTSLSGroup
- Metodo RemoveLSfromTSLSGroup Servizi Desktop remoto, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Servizi Desktop remoto, metodo RemoveLSfromTSLSGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.RemoveLSfromTSLSGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b60c7a0e6b836b8fcf268942ba5d8eae1304b818
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518028"
---
# <a name="removelsfromtslsgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="aaaad-106">Metodo RemoveLSfromTSLSGroup della \_ classe TSLicenseServer Win32</span><span class="sxs-lookup"><span data-stu-id="aaaad-106">RemoveLSfromTSLSGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="aaaad-107">Rimuove il server licenze Desktop remoto dal gruppo server licenze Servizi Desktop remoto in un controller di dominio nello stesso dominio del server licenze.</span><span class="sxs-lookup"><span data-stu-id="aaaad-107">Removes the Remote Desktop license server from the Remote Desktop Services License Servers group on a domain controller in the same domain as the license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaaad-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aaaad-108">Syntax</span></span>


```mof
uint32 RemoveLSfromTSLSGroup();
```



## <a name="parameters"></a><span data-ttu-id="aaaad-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="aaaad-109">Parameters</span></span>

<span data-ttu-id="aaaad-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="aaaad-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aaaad-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aaaad-111">Return value</span></span>

<span data-ttu-id="aaaad-112">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="aaaad-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="aaaad-113">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="aaaad-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="aaaad-114">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="aaaad-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="aaaad-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="aaaad-115">Remarks</span></span>

<span data-ttu-id="aaaad-116">Per chiamare questo metodo, è necessario essere un membro del gruppo Domain Admins.</span><span class="sxs-lookup"><span data-stu-id="aaaad-116">You must be a member of the Domain Admins group to call this method.</span></span>

<span data-ttu-id="aaaad-117">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="aaaad-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="aaaad-118">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="aaaad-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="aaaad-119">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="aaaad-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="aaaad-120">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="aaaad-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="aaaad-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aaaad-121">Requirements</span></span>



| <span data-ttu-id="aaaad-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="aaaad-122">Requirement</span></span> | <span data-ttu-id="aaaad-123">Valore</span><span class="sxs-lookup"><span data-stu-id="aaaad-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="aaaad-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aaaad-124">Minimum supported client</span></span><br/> | <span data-ttu-id="aaaad-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="aaaad-125">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="aaaad-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aaaad-126">Minimum supported server</span></span><br/> | <span data-ttu-id="aaaad-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aaaad-127">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="aaaad-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="aaaad-128">Namespace</span></span><br/>                | <span data-ttu-id="aaaad-129">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="aaaad-129">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="aaaad-130">MOF</span><span class="sxs-lookup"><span data-stu-id="aaaad-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aaaad-131"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aaaad-131"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="aaaad-132">DLL</span><span class="sxs-lookup"><span data-stu-id="aaaad-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aaaad-133"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aaaad-133"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aaaad-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aaaad-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaaad-135">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="aaaad-135">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 


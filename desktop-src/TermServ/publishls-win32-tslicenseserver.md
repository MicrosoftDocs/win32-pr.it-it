---
title: Metodo PublishLS della classe Win32_TSLicenseServer
description: Pubblica il server licenze Desktop remoto in Active Directory Domain Services.
ms.assetid: 726d5dec-e438-455e-adb8-56d646d65d13
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo PublishLS
- Metodo PublishLS Servizi Desktop remoto, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Servizi Desktop remoto, metodo PublishLS
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.PublishLS
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ad3d20efe8b61cd00e1986bb190500c93fd9473
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121219"
---
# <a name="publishls-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="17b79-106">Metodo PublishLS della \_ classe TSLicenseServer Win32</span><span class="sxs-lookup"><span data-stu-id="17b79-106">PublishLS method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="17b79-107">Pubblica il server licenze Desktop remoto in Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="17b79-107">Publishes the Remote Desktop license server in Active Directory Domain Services.</span></span>

## <a name="syntax"></a><span data-ttu-id="17b79-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="17b79-108">Syntax</span></span>


```mof
uint32 PublishLS();
```



## <a name="parameters"></a><span data-ttu-id="17b79-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="17b79-109">Parameters</span></span>

<span data-ttu-id="17b79-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="17b79-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="17b79-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="17b79-111">Return value</span></span>

<span data-ttu-id="17b79-112">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="17b79-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="17b79-113">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="17b79-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="17b79-114">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="17b79-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="17b79-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="17b79-115">Remarks</span></span>

<span data-ttu-id="17b79-116">Per chiamare questo metodo, è necessario effettuare l'accesso come amministratore dell'organizzazione alla foresta in cui è membro il server licenze.</span><span class="sxs-lookup"><span data-stu-id="17b79-116">To call this method, you must be logged on as an enterprise administrator to the forest in which the license server is a member.</span></span>

<span data-ttu-id="17b79-117">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="17b79-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="17b79-118">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="17b79-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="17b79-119">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="17b79-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="17b79-120">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="17b79-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="17b79-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17b79-121">Requirements</span></span>



| <span data-ttu-id="17b79-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="17b79-122">Requirement</span></span> | <span data-ttu-id="17b79-123">Valore</span><span class="sxs-lookup"><span data-stu-id="17b79-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="17b79-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17b79-124">Minimum supported client</span></span><br/> | <span data-ttu-id="17b79-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="17b79-125">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="17b79-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17b79-126">Minimum supported server</span></span><br/> | <span data-ttu-id="17b79-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17b79-127">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="17b79-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="17b79-128">Namespace</span></span><br/>                | <span data-ttu-id="17b79-129">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="17b79-129">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="17b79-130">MOF</span><span class="sxs-lookup"><span data-stu-id="17b79-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17b79-131"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17b79-131"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="17b79-132">DLL</span><span class="sxs-lookup"><span data-stu-id="17b79-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17b79-133"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17b79-133"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17b79-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="17b79-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17b79-135">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="17b79-135">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 


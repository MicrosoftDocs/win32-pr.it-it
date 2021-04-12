---
title: Metodo UnpublishLS della classe Win32_TSLicenseServer
description: Annulla la pubblicazione di un server licenze Desktop remoto da Active Directory Domain Services.
ms.assetid: 275854e2-85f6-4142-8bce-8d633bfcff7d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo UnpublishLS
- Metodo UnpublishLS Servizi Desktop remoto, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Servizi Desktop remoto, metodo UnpublishLS
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.UnpublishLS
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1ec183b5be8055dc30add5bc00a7eb537cd20f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518015"
---
# <a name="unpublishls-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="f3a36-106">Metodo UnpublishLS della \_ classe TSLicenseServer Win32</span><span class="sxs-lookup"><span data-stu-id="f3a36-106">UnpublishLS method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="f3a36-107">Annulla la pubblicazione di un server licenze Desktop remoto da Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="f3a36-107">Unpublishes a Remote Desktop license server from Active Directory Domain Services.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3a36-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3a36-108">Syntax</span></span>


```mof
uint32 UnpublishLS();
```



## <a name="parameters"></a><span data-ttu-id="f3a36-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f3a36-109">Parameters</span></span>

<span data-ttu-id="f3a36-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="f3a36-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f3a36-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f3a36-111">Return value</span></span>

<span data-ttu-id="f3a36-112">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="f3a36-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="f3a36-113">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="f3a36-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="f3a36-114">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f3a36-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f3a36-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3a36-115">Remarks</span></span>

<span data-ttu-id="f3a36-116">Per chiamare questo metodo, è necessario effettuare l'accesso come amministratore dell'organizzazione alla foresta in cui è membro il server licenze.</span><span class="sxs-lookup"><span data-stu-id="f3a36-116">To call this method, you must be logged on as an enterprise administrator to the forest in which the license server is a member.</span></span>

<span data-ttu-id="f3a36-117">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f3a36-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f3a36-118">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="f3a36-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f3a36-119">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="f3a36-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f3a36-120">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f3a36-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f3a36-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3a36-121">Requirements</span></span>



| <span data-ttu-id="f3a36-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3a36-122">Requirement</span></span> | <span data-ttu-id="f3a36-123">Valore</span><span class="sxs-lookup"><span data-stu-id="f3a36-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3a36-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3a36-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f3a36-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f3a36-125">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="f3a36-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3a36-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f3a36-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3a36-127">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="f3a36-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f3a36-128">Namespace</span></span><br/>                | <span data-ttu-id="f3a36-129">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="f3a36-129">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="f3a36-130">MOF</span><span class="sxs-lookup"><span data-stu-id="f3a36-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3a36-131"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3a36-131"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3a36-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f3a36-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3a36-133"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3a36-133"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3a36-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3a36-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3a36-135">**\_TSLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="f3a36-135">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 


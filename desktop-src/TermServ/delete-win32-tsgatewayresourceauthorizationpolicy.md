---
title: Metodo Delete della classe Win32_TSGatewayResourceAuthorizationPolicy
description: Elimina i criteri di autorizzazione delle risorse di Desktop remoto correnti (RD \ 160; RAP).
ms.assetid: cbabb997-63b8-4a4c-9e16-34f2638fca97
ms.tgt_platform: multiple
keywords:
- Elimina Servizi Desktop remoto del metodo
- Metodo Delete Servizi Desktop remoto, classe Win32_TSGatewayResourceAuthorizationPolicy
- Classe Win32_TSGatewayResourceAuthorizationPolicy Servizi Desktop remoto, metodo Delete
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.Delete
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 396a766fb307d1e8a912d614147a2bff2bd924c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400331"
---
# <a name="delete-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="047c9-106">Metodo Delete della classe Win32 \_ TSGatewayResourceAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="047c9-106">Delete method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="047c9-107">Elimina i criteri di autorizzazione delle risorse di Desktop remoto correnti.</span><span class="sxs-lookup"><span data-stu-id="047c9-107">Deletes the current Remote Desktop resource authorization policy (RD RAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="047c9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="047c9-108">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="047c9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="047c9-109">Parameters</span></span>

<span data-ttu-id="047c9-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="047c9-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="047c9-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="047c9-111">Return value</span></span>

<span data-ttu-id="047c9-112">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="047c9-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="047c9-113">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="047c9-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="047c9-114">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="047c9-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="047c9-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="047c9-115">Remarks</span></span>

<span data-ttu-id="047c9-116">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="047c9-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="047c9-117">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="047c9-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="047c9-118">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="047c9-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="047c9-119">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="047c9-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="047c9-120">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="047c9-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="047c9-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="047c9-121">Requirements</span></span>



| <span data-ttu-id="047c9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="047c9-122">Requirement</span></span> | <span data-ttu-id="047c9-123">Valore</span><span class="sxs-lookup"><span data-stu-id="047c9-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="047c9-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="047c9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="047c9-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="047c9-125">None supported</span></span><br/>                                                                |
| <span data-ttu-id="047c9-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="047c9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="047c9-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="047c9-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="047c9-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="047c9-128">Namespace</span></span><br/>                | <span data-ttu-id="047c9-129">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="047c9-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="047c9-130">MOF</span><span class="sxs-lookup"><span data-stu-id="047c9-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="047c9-131"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="047c9-131"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="047c9-132">DLL</span><span class="sxs-lookup"><span data-stu-id="047c9-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="047c9-133"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="047c9-133"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="047c9-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="047c9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="047c9-135">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="047c9-135">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 


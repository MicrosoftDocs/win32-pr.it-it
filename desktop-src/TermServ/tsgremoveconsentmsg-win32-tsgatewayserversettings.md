---
title: Metodo TSGRemoveConsentMsg della classe Win32_TSGatewayServerSettings
description: Rimuove il messaggio amministrativo per il server gateway. | Metodo TSGRemoveConsentMsg della classe Win32_TSGatewayServerSettings
ms.assetid: 626dc9ca-d6a1-48ab-84ec-cfccb8e720c2
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo TSGRemoveConsentMsg
- Metodo TSGRemoveConsentMsg Servizi Desktop remoto, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo TSGRemoveConsentMsg
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.TSGRemoveConsentMsg
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24cd002ebb1a953d25cf129b4e5f3b4174842199
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886204"
---
# <a name="tsgremoveconsentmsg-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="eac49-107">Metodo TSGRemoveConsentMsg della \_ classe TSGatewayServerSettings Win32</span><span class="sxs-lookup"><span data-stu-id="eac49-107">TSGRemoveConsentMsg method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="eac49-108">Rimuove il messaggio amministrativo per il server gateway.</span><span class="sxs-lookup"><span data-stu-id="eac49-108">Removes the administrative message for the gateway server.</span></span>

## <a name="syntax"></a><span data-ttu-id="eac49-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eac49-109">Syntax</span></span>


```mof
uint32 TSGRemoveConsentMsg();
```



## <a name="parameters"></a><span data-ttu-id="eac49-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="eac49-110">Parameters</span></span>

<span data-ttu-id="eac49-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="eac49-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eac49-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eac49-112">Return value</span></span>

<span data-ttu-id="eac49-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eac49-113">Type: **uint32**</span></span>

<span data-ttu-id="eac49-114">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="eac49-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="eac49-115">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="eac49-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="eac49-116">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="eac49-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="eac49-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="eac49-117">Remarks</span></span>

<span data-ttu-id="eac49-118">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="eac49-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="eac49-119">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="eac49-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="eac49-120">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="eac49-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="eac49-121">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="eac49-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="eac49-122">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="eac49-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="eac49-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eac49-123">Requirements</span></span>



| <span data-ttu-id="eac49-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="eac49-124">Requirement</span></span> | <span data-ttu-id="eac49-125">Valore</span><span class="sxs-lookup"><span data-stu-id="eac49-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="eac49-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eac49-126">Minimum supported client</span></span><br/> | <span data-ttu-id="eac49-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="eac49-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="eac49-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eac49-128">Minimum supported server</span></span><br/> | <span data-ttu-id="eac49-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="eac49-129">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="eac49-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="eac49-130">Namespace</span></span><br/>                | <span data-ttu-id="eac49-131">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="eac49-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="eac49-132">MOF</span><span class="sxs-lookup"><span data-stu-id="eac49-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eac49-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eac49-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="eac49-134">DLL</span><span class="sxs-lookup"><span data-stu-id="eac49-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eac49-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eac49-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="eac49-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eac49-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eac49-137">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="eac49-137">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 


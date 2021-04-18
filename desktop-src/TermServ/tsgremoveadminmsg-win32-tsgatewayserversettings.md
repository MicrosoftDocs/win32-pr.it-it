---
title: Metodo TSGRemoveAdminMsg della classe Win32_TSGatewayServerSettings
description: Rimuove il messaggio amministrativo per il server gateway. | Metodo TSGRemoveAdminMsg della classe Win32_TSGatewayServerSettings
ms.assetid: 36b157de-80ee-46f8-9803-5012cf1d6f5f
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo TSGRemoveAdminMsg
- Metodo TSGRemoveAdminMsg Servizi Desktop remoto, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo TSGRemoveAdminMsg
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.TSGRemoveAdminMsg
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba9877b9e8704c92eb482876ab69107e116207b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321788"
---
# <a name="tsgremoveadminmsg-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="66a03-107">Metodo TSGRemoveAdminMsg della \_ classe TSGatewayServerSettings Win32</span><span class="sxs-lookup"><span data-stu-id="66a03-107">TSGRemoveAdminMsg method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="66a03-108">Rimuove il messaggio amministrativo per il server gateway.</span><span class="sxs-lookup"><span data-stu-id="66a03-108">Removes the administrative message for the gateway server.</span></span>

## <a name="syntax"></a><span data-ttu-id="66a03-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="66a03-109">Syntax</span></span>


```mof
uint32 TSGRemoveAdminMsg();
```



## <a name="parameters"></a><span data-ttu-id="66a03-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="66a03-110">Parameters</span></span>

<span data-ttu-id="66a03-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="66a03-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="66a03-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="66a03-112">Return value</span></span>

<span data-ttu-id="66a03-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="66a03-113">Type: **uint32**</span></span>

<span data-ttu-id="66a03-114">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="66a03-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="66a03-115">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="66a03-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="66a03-116">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="66a03-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="66a03-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="66a03-117">Remarks</span></span>

<span data-ttu-id="66a03-118">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="66a03-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="66a03-119">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="66a03-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="66a03-120">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="66a03-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="66a03-121">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="66a03-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="66a03-122">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="66a03-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="66a03-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66a03-123">Requirements</span></span>



| <span data-ttu-id="66a03-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="66a03-124">Requirement</span></span> | <span data-ttu-id="66a03-125">Valore</span><span class="sxs-lookup"><span data-stu-id="66a03-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="66a03-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66a03-126">Minimum supported client</span></span><br/> | <span data-ttu-id="66a03-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="66a03-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="66a03-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66a03-128">Minimum supported server</span></span><br/> | <span data-ttu-id="66a03-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="66a03-129">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="66a03-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="66a03-130">Namespace</span></span><br/>                | <span data-ttu-id="66a03-131">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="66a03-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="66a03-132">MOF</span><span class="sxs-lookup"><span data-stu-id="66a03-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66a03-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="66a03-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="66a03-134">DLL</span><span class="sxs-lookup"><span data-stu-id="66a03-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66a03-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66a03-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="66a03-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="66a03-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66a03-137">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="66a03-137">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 


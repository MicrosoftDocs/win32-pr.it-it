---
title: Metodo RecycleRpcApplicationPools della classe Win32_TSGatewayServerSettings
description: Ricicla i pool di applicazioni RPC in IIS.
ms.assetid: c7b1b797-7792-4d97-97f4-bea3b2f2495b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RecycleRpcApplicationPools
- Metodo RecycleRpcApplicationPools Servizi Desktop remoto, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo RecycleRpcApplicationPools
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.RecycleRpcApplicationPools
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1963b8dec826c72a8a5128abdfa01d4a1e841a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476426"
---
# <a name="recyclerpcapplicationpools-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="bebef-106">Metodo RecycleRpcApplicationPools della \_ classe TSGatewayServerSettings Win32</span><span class="sxs-lookup"><span data-stu-id="bebef-106">RecycleRpcApplicationPools method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="bebef-107">Ricicla i pool di applicazioni RPC in IIS.</span><span class="sxs-lookup"><span data-stu-id="bebef-107">Recycles the RPC application pools in IIS.</span></span>

## <a name="syntax"></a><span data-ttu-id="bebef-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bebef-108">Syntax</span></span>


```mof
uint32 RecycleRpcApplicationPools();
```



## <a name="parameters"></a><span data-ttu-id="bebef-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bebef-109">Parameters</span></span>

<span data-ttu-id="bebef-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="bebef-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bebef-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bebef-111">Return value</span></span>

<span data-ttu-id="bebef-112">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bebef-112">Type: **uint32**</span></span>

<span data-ttu-id="bebef-113">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="bebef-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="bebef-114">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="bebef-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="bebef-115">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="bebef-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bebef-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="bebef-116">Remarks</span></span>

<span data-ttu-id="bebef-117">La chiamata a questo metodo comporta la disconnessione di tutte le connessioni esistenti.</span><span class="sxs-lookup"><span data-stu-id="bebef-117">Calling this method results in all existing connections being disconnected.</span></span>

<span data-ttu-id="bebef-118">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="bebef-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="bebef-119">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="bebef-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bebef-120">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="bebef-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bebef-121">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="bebef-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bebef-122">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="bebef-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="bebef-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bebef-123">Requirements</span></span>



| <span data-ttu-id="bebef-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bebef-124">Requirement</span></span> | <span data-ttu-id="bebef-125">Valore</span><span class="sxs-lookup"><span data-stu-id="bebef-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bebef-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bebef-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bebef-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="bebef-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="bebef-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bebef-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bebef-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bebef-129">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="bebef-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bebef-130">Namespace</span></span><br/>                | <span data-ttu-id="bebef-131">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="bebef-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="bebef-132">MOF</span><span class="sxs-lookup"><span data-stu-id="bebef-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bebef-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bebef-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="bebef-134">DLL</span><span class="sxs-lookup"><span data-stu-id="bebef-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bebef-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bebef-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="bebef-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bebef-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bebef-137">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="bebef-137">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="bebef-138">**SetAuthenticationPlugin**</span><span class="sxs-lookup"><span data-stu-id="bebef-138">**SetAuthenticationPlugin**</span></span>](setauthenticationplugin-win32-tsgatewayserversettings.md)
</dt> </dl>

 


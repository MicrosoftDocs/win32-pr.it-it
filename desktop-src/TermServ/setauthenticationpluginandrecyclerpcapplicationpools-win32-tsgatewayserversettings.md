---
title: Metodo SetAuthenticationPluginAndRecycleRpcApplicationPools della classe Win32_TSGatewayServerSettings
description: Imposta il plug-in di autenticazione corrente per il server Gateway Desktop remoto (Gateway Desktop remoto) e ricicla i pool di applicazioni RPC in IIS.
ms.assetid: cdceaf50-3d0a-4af0-9ad5-fb43760fcf7b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetAuthenticationPluginAndRecycleRpcApplicationPools
- Metodo SetAuthenticationPluginAndRecycleRpcApplicationPools Servizi Desktop remoto, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo SetAuthenticationPluginAndRecycleRpcApplicationPools
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetAuthenticationPluginAndRecycleRpcApplicationPools
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b234e04c349d20ea178de12f050190b30193d444
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740719"
---
# <a name="setauthenticationpluginandrecyclerpcapplicationpools-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="8a36f-106">Metodo SetAuthenticationPluginAndRecycleRpcApplicationPools della \_ classe TSGatewayServerSettings Win32</span><span class="sxs-lookup"><span data-stu-id="8a36f-106">SetAuthenticationPluginAndRecycleRpcApplicationPools method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="8a36f-107">Imposta il plug-in di autenticazione corrente per il server Gateway Desktop remoto (Gateway Desktop remoto) e ricicla i pool di applicazioni RPC in IIS.</span><span class="sxs-lookup"><span data-stu-id="8a36f-107">Sets the current authentication plug-in for the Remote Desktop Gateway (RD Gateway) server and recycles the RPC application pools in IIS.</span></span>

<span data-ttu-id="8a36f-108">Questo metodo equivale a chiamare i metodi [**SetAuthenticationPlugin**](setauthenticationplugin-win32-tsgatewayserversettings.md) e [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) in sequenza.</span><span class="sxs-lookup"><span data-stu-id="8a36f-108">This method is equivalent to calling the [**SetAuthenticationPlugin**](setauthenticationplugin-win32-tsgatewayserversettings.md) and [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) methods in sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a36f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a36f-109">Syntax</span></span>


```mof
uint32 SetAuthenticationPluginAndRecycleRpcApplicationPools(
  [in] string PluginName
);
```



## <a name="parameters"></a><span data-ttu-id="8a36f-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="8a36f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a36f-111">*Plug-in* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a36f-111">*PluginName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a36f-112">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="8a36f-112">Type: **string**</span></span>

<span data-ttu-id="8a36f-113">Nome del plug-in di autenticazione</span><span class="sxs-lookup"><span data-stu-id="8a36f-113">Name of the authentication plug-in</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a36f-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8a36f-114">Return value</span></span>

<span data-ttu-id="8a36f-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8a36f-115">Type: **uint32**</span></span>

<span data-ttu-id="8a36f-116">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="8a36f-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="8a36f-117">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="8a36f-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="8a36f-118">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8a36f-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8a36f-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a36f-119">Remarks</span></span>

<span data-ttu-id="8a36f-120">La chiamata a questo metodo comporta la disconnessione di tutte le connessioni esistenti.</span><span class="sxs-lookup"><span data-stu-id="8a36f-120">Calling this method results in all existing connections being disconnected.</span></span>

<span data-ttu-id="8a36f-121">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="8a36f-121">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="8a36f-122">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="8a36f-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8a36f-123">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="8a36f-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8a36f-124">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="8a36f-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8a36f-125">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8a36f-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8a36f-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a36f-126">Requirements</span></span>



| <span data-ttu-id="8a36f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a36f-127">Requirement</span></span> | <span data-ttu-id="8a36f-128">Valore</span><span class="sxs-lookup"><span data-stu-id="8a36f-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a36f-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a36f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8a36f-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8a36f-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="8a36f-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8a36f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8a36f-132">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8a36f-132">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="8a36f-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8a36f-133">Namespace</span></span><br/>                | <span data-ttu-id="8a36f-134">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="8a36f-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="8a36f-135">MOF</span><span class="sxs-lookup"><span data-stu-id="8a36f-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a36f-136"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8a36f-136"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a36f-137">DLL</span><span class="sxs-lookup"><span data-stu-id="8a36f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a36f-138"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a36f-138"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="8a36f-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a36f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a36f-140">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="8a36f-140">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="8a36f-141">**SetAuthenticationPlugin**</span><span class="sxs-lookup"><span data-stu-id="8a36f-141">**SetAuthenticationPlugin**</span></span>](setauthenticationplugin-win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="8a36f-142">**RecycleRpcApplicationPools**</span><span class="sxs-lookup"><span data-stu-id="8a36f-142">**RecycleRpcApplicationPools**</span></span>](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)
</dt> </dl>

 


---
title: Metodo SetAuthenticationPlugin della classe Win32_TSGatewayServerSettings
description: Imposta il plug-in di autenticazione corrente per il server Gateway Desktop remoto (Gateway Desktop remoto).
ms.assetid: b79a5e7c-bf55-48f6-a6c0-5338e7eee2a1
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetAuthenticationPlugin
- Metodo SetAuthenticationPlugin Servizi Desktop remoto, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo SetAuthenticationPlugin
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetAuthenticationPlugin
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2b5b332dd288a01f96b0eb0b3a99e7e45269cdf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743503"
---
# <a name="setauthenticationplugin-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="83505-106">Metodo SetAuthenticationPlugin della \_ classe TSGatewayServerSettings Win32</span><span class="sxs-lookup"><span data-stu-id="83505-106">SetAuthenticationPlugin method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="83505-107">Imposta il plug-in di autenticazione corrente per il server Gateway Desktop remoto (Gateway Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="83505-107">Sets the current authentication plug-in for the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="83505-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="83505-108">Syntax</span></span>


```mof
uint32 SetAuthenticationPlugin(
  [in] string PluginName
);
```



## <a name="parameters"></a><span data-ttu-id="83505-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="83505-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83505-110">*Plug-in* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83505-110">*PluginName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83505-111">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="83505-111">Type: **string**</span></span>

<span data-ttu-id="83505-112">Nome del nuovo plug-in di autenticazione corrente.</span><span class="sxs-lookup"><span data-stu-id="83505-112">The name of the new current authentication plug-in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83505-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="83505-113">Return value</span></span>

<span data-ttu-id="83505-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="83505-114">Type: **uint32**</span></span>

<span data-ttu-id="83505-115">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="83505-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="83505-116">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="83505-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="83505-117">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="83505-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="83505-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="83505-118">Remarks</span></span>

<span data-ttu-id="83505-119">È necessario chiamare il metodo [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) per consentire il funzionamento del plug-in di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="83505-119">You must call the [**RecycleRpcApplicationPools**](recyclerpcapplicationpools-win32-tsgatewayserversettings.md) method to allow the authentication plug-in to work.</span></span>

<span data-ttu-id="83505-120">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="83505-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="83505-121">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="83505-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="83505-122">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="83505-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="83505-123">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="83505-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="83505-124">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="83505-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="83505-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83505-125">Requirements</span></span>



| <span data-ttu-id="83505-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="83505-126">Requirement</span></span> | <span data-ttu-id="83505-127">Valore</span><span class="sxs-lookup"><span data-stu-id="83505-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="83505-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83505-128">Minimum supported client</span></span><br/> | <span data-ttu-id="83505-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="83505-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="83505-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83505-130">Minimum supported server</span></span><br/> | <span data-ttu-id="83505-131">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="83505-131">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="83505-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="83505-132">Namespace</span></span><br/>                | <span data-ttu-id="83505-133">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="83505-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="83505-134">MOF</span><span class="sxs-lookup"><span data-stu-id="83505-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="83505-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="83505-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="83505-136">DLL</span><span class="sxs-lookup"><span data-stu-id="83505-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83505-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83505-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="83505-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83505-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83505-139">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="83505-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="83505-140">**RecycleRpcApplicationPools**</span><span class="sxs-lookup"><span data-stu-id="83505-140">**RecycleRpcApplicationPools**</span></span>](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)
</dt> </dl>

 


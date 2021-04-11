---
title: Metodo SetDefaultPluginsAndRecycleRpcApplicationPools della classe Win32_TSGatewayServerSettings
description: Imposta i plug-in di autenticazione e autorizzazione correnti per il server Gateway Desktop remoto di Desktop remoto e ricicla i pool di applicazioni RPC in IIS.
ms.assetid: 1eac9e42-e533-4020-b2b6-571063f18c3c
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetDefaultPluginsAndRecycleRpcApplicationPools
- Metodo SetDefaultPluginsAndRecycleRpcApplicationPools Servizi Desktop remoto, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo SetDefaultPluginsAndRecycleRpcApplicationPools
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetDefaultPluginsAndRecycleRpcApplicationPools
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b9ead29e987b68ec3f041010be5dde64d8a2b54
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964809"
---
# <a name="setdefaultpluginsandrecyclerpcapplicationpools-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="10647-106">Metodo SetDefaultPluginsAndRecycleRpcApplicationPools della \_ classe TSGatewayServerSettings Win32</span><span class="sxs-lookup"><span data-stu-id="10647-106">SetDefaultPluginsAndRecycleRpcApplicationPools method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="10647-107">Imposta i plug-in di autenticazione e autorizzazione correnti per il server Gateway Desktop remoto di Desktop remoto e ricicla i pool di applicazioni RPC in IIS.</span><span class="sxs-lookup"><span data-stu-id="10647-107">Sets the current authentication and authorization plug-ins for the Remote Desktop Gateway (RD Gateway) server and recycles the RPC application pools in IIS.</span></span>

## <a name="syntax"></a><span data-ttu-id="10647-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="10647-108">Syntax</span></span>


```mof
uint32 SetDefaultPluginsAndRecycleRpcApplicationPools();
```



## <a name="parameters"></a><span data-ttu-id="10647-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="10647-109">Parameters</span></span>

<span data-ttu-id="10647-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="10647-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="10647-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="10647-111">Return value</span></span>

<span data-ttu-id="10647-112">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10647-112">Type: **uint32**</span></span>

<span data-ttu-id="10647-113">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="10647-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="10647-114">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="10647-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="10647-115">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="10647-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="10647-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="10647-116">Remarks</span></span>

<span data-ttu-id="10647-117">La chiamata a questo metodo comporta la disconnessione di tutte le connessioni esistenti.</span><span class="sxs-lookup"><span data-stu-id="10647-117">Calling this method results in all existing connections being disconnected.</span></span>

<span data-ttu-id="10647-118">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="10647-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="10647-119">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="10647-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="10647-120">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="10647-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="10647-121">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="10647-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="10647-122">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="10647-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="10647-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10647-123">Requirements</span></span>



| <span data-ttu-id="10647-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="10647-124">Requirement</span></span> | <span data-ttu-id="10647-125">Valore</span><span class="sxs-lookup"><span data-stu-id="10647-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="10647-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10647-126">Minimum supported client</span></span><br/> | <span data-ttu-id="10647-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="10647-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="10647-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10647-128">Minimum supported server</span></span><br/> | <span data-ttu-id="10647-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="10647-129">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="10647-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="10647-130">Namespace</span></span><br/>                | <span data-ttu-id="10647-131">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="10647-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="10647-132">MOF</span><span class="sxs-lookup"><span data-stu-id="10647-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10647-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="10647-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="10647-134">DLL</span><span class="sxs-lookup"><span data-stu-id="10647-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10647-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10647-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="10647-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="10647-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10647-137">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="10647-137">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 


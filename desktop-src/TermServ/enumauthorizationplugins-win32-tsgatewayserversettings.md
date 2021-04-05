---
title: Metodo EnumAuthorizationPlugins della classe Win32_TSGatewayServerSettings
description: Enumera tutti i plug-in di autorizzazione registrati.
ms.assetid: 525b4001-b89c-43cc-986a-00db47dd5518
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo EnumAuthorizationPlugins
- Metodo EnumAuthorizationPlugins Servizi Desktop remoto, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo EnumAuthorizationPlugins
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnumAuthorizationPlugins
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d955c08f5e4f91547751b0f177681ad2abd57c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874606"
---
# <a name="enumauthorizationplugins-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="a122d-106">Metodo EnumAuthorizationPlugins della \_ classe TSGatewayServerSettings Win32</span><span class="sxs-lookup"><span data-stu-id="a122d-106">EnumAuthorizationPlugins method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="a122d-107">Enumera tutti i plug-in di autorizzazione registrati.</span><span class="sxs-lookup"><span data-stu-id="a122d-107">Enumerates all registered authorization plug-ins.</span></span>

## <a name="syntax"></a><span data-ttu-id="a122d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a122d-108">Syntax</span></span>


```mof
uint32 EnumAuthorizationPlugins(
  [out] string PluginNames[],
  [out] string CLSIDs[],
  [out] string Descriptions[]
);
```



## <a name="parameters"></a><span data-ttu-id="a122d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a122d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a122d-110">*PluginNames* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a122d-110">*PluginNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a122d-111">Tipo: **stringa \[ \]**</span><span class="sxs-lookup"><span data-stu-id="a122d-111">Type: **string\[\]**</span></span>

<span data-ttu-id="a122d-112">Matrice di **stringhe** che riceve i nomi dei plug-in di autorizzazione registrati.</span><span class="sxs-lookup"><span data-stu-id="a122d-112">A **string** array that receives the names of the registered authorization plug-ins.</span></span>

</dd> <dt>

<span data-ttu-id="a122d-113">*CLSID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a122d-113">*CLSIDs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a122d-114">Tipo: **stringa \[ \]**</span><span class="sxs-lookup"><span data-stu-id="a122d-114">Type: **string\[\]**</span></span>

<span data-ttu-id="a122d-115">Matrice di **stringhe** che riceve i CLSID dei plug-in di autorizzazione registrati.</span><span class="sxs-lookup"><span data-stu-id="a122d-115">A **string** array that receives the CLSIDs of the registered authorization plug-ins.</span></span>

</dd> <dt>

<span data-ttu-id="a122d-116">*Descrizioni* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="a122d-116">*Descriptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a122d-117">Tipo: **stringa \[ \]**</span><span class="sxs-lookup"><span data-stu-id="a122d-117">Type: **string\[\]**</span></span>

<span data-ttu-id="a122d-118">Matrice di **stringhe** che riceve le descrizioni dei plug-in di autorizzazione registrati.</span><span class="sxs-lookup"><span data-stu-id="a122d-118">A **string** array that receives the descriptions of the registered authorization plug-ins.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a122d-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a122d-119">Return value</span></span>

<span data-ttu-id="a122d-120">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a122d-120">Type: **uint32**</span></span>

<span data-ttu-id="a122d-121">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="a122d-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="a122d-122">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="a122d-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="a122d-123">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a122d-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a122d-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="a122d-124">Remarks</span></span>

<span data-ttu-id="a122d-125">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="a122d-125">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="a122d-126">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="a122d-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a122d-127">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="a122d-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a122d-128">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="a122d-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a122d-129">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a122d-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a122d-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a122d-130">Requirements</span></span>



| <span data-ttu-id="a122d-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a122d-131">Requirement</span></span> | <span data-ttu-id="a122d-132">Valore</span><span class="sxs-lookup"><span data-stu-id="a122d-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a122d-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a122d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a122d-134">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a122d-134">None supported</span></span><br/>                                                                |
| <span data-ttu-id="a122d-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a122d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a122d-136">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a122d-136">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="a122d-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a122d-137">Namespace</span></span><br/>                | <span data-ttu-id="a122d-138">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="a122d-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="a122d-139">MOF</span><span class="sxs-lookup"><span data-stu-id="a122d-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a122d-140"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a122d-140"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="a122d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a122d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a122d-142"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a122d-142"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="a122d-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a122d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a122d-144">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="a122d-144">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 


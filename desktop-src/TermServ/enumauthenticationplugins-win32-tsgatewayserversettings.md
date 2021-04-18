---
title: Metodo EnumAuthenticationPlugins della classe Win32_TSGatewayServerSettings
description: Enumera tutti i plug-in di autenticazione registrati.
ms.assetid: a5c1859d-e20c-4c72-aef5-ef9941edf73e
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo EnumAuthenticationPlugins
- Metodo EnumAuthenticationPlugins Servizi Desktop remoto, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo EnumAuthenticationPlugins
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnumAuthenticationPlugins
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0cd9d059a79749f657c6191e68e7bcd08555cb5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301231"
---
# <a name="enumauthenticationplugins-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="fb4f8-106">Metodo EnumAuthenticationPlugins della \_ classe TSGatewayServerSettings Win32</span><span class="sxs-lookup"><span data-stu-id="fb4f8-106">EnumAuthenticationPlugins method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="fb4f8-107">Enumera tutti i plug-in di autenticazione registrati.</span><span class="sxs-lookup"><span data-stu-id="fb4f8-107">Enumerates all registered authentication plug-ins.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb4f8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb4f8-108">Syntax</span></span>


```mof
uint32 EnumAuthenticationPlugins(
  [out] string PluginNames[],
  [out] string CLSIDs[],
  [out] string Descriptions[]
);
```



## <a name="parameters"></a><span data-ttu-id="fb4f8-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="fb4f8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb4f8-110">*PluginNames* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fb4f8-110">*PluginNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb4f8-111">Tipo: **stringa \[ \]**</span><span class="sxs-lookup"><span data-stu-id="fb4f8-111">Type: **string\[\]**</span></span>

<span data-ttu-id="fb4f8-112">Matrice di **stringhe** che riceve i nomi dei plug-in di autenticazione registrati.</span><span class="sxs-lookup"><span data-stu-id="fb4f8-112">A **string** array that receives the names of the registered authentication plug-ins.</span></span>

</dd> <dt>

<span data-ttu-id="fb4f8-113">*CLSID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fb4f8-113">*CLSIDs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb4f8-114">Tipo: **stringa \[ \]**</span><span class="sxs-lookup"><span data-stu-id="fb4f8-114">Type: **string\[\]**</span></span>

<span data-ttu-id="fb4f8-115">Matrice di **stringhe** che riceve i CLSID dei plug-in di autenticazione registrati.</span><span class="sxs-lookup"><span data-stu-id="fb4f8-115">A **string** array that receives the CLSIDs of the registered authentication plug-ins.</span></span>

</dd> <dt>

<span data-ttu-id="fb4f8-116">*Descrizioni* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="fb4f8-116">*Descriptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb4f8-117">Tipo: **stringa \[ \]**</span><span class="sxs-lookup"><span data-stu-id="fb4f8-117">Type: **string\[\]**</span></span>

<span data-ttu-id="fb4f8-118">Matrice di **stringhe** che riceve le descrizioni dei plug-in di autenticazione registrati.</span><span class="sxs-lookup"><span data-stu-id="fb4f8-118">A **string** array that receives the descriptions of the registered authentication plug-ins.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb4f8-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fb4f8-119">Return value</span></span>

<span data-ttu-id="fb4f8-120">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fb4f8-120">Type: **uint32**</span></span>

<span data-ttu-id="fb4f8-121">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="fb4f8-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="fb4f8-122">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="fb4f8-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="fb4f8-123">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="fb4f8-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fb4f8-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="fb4f8-124">Remarks</span></span>

<span data-ttu-id="fb4f8-125">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="fb4f8-125">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="fb4f8-126">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="fb4f8-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fb4f8-127">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="fb4f8-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fb4f8-128">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="fb4f8-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fb4f8-129">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="fb4f8-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb4f8-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb4f8-130">Requirements</span></span>



| <span data-ttu-id="fb4f8-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb4f8-131">Requirement</span></span> | <span data-ttu-id="fb4f8-132">Valore</span><span class="sxs-lookup"><span data-stu-id="fb4f8-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb4f8-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb4f8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="fb4f8-134">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fb4f8-134">None supported</span></span><br/>                                                                |
| <span data-ttu-id="fb4f8-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb4f8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="fb4f8-136">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fb4f8-136">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="fb4f8-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fb4f8-137">Namespace</span></span><br/>                | <span data-ttu-id="fb4f8-138">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="fb4f8-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="fb4f8-139">MOF</span><span class="sxs-lookup"><span data-stu-id="fb4f8-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb4f8-140"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fb4f8-140"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="fb4f8-141">DLL</span><span class="sxs-lookup"><span data-stu-id="fb4f8-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb4f8-142"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb4f8-142"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="fb4f8-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb4f8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb4f8-144">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="fb4f8-144">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 


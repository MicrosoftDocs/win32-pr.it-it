---
title: Metodo seenabled della classe Win32_TSGatewayResourceAuthorizationPolicy
description: Abilita o Disabilita i criteri di autorizzazione delle risorse Desktop remoto (RD \ 160; RAP) impostando la proprietà Enabled.
ms.assetid: ee5830ba-36a1-4f28-a902-be5867439ada
ms.tgt_platform: multiple
keywords:
- Metodo seenabled Servizi Desktop remoto
- Metodo seenabled Servizi Desktop remoto, classe Win32_TSGatewayResourceAuthorizationPolicy
- Classe Win32_TSGatewayResourceAuthorizationPolicy Servizi Desktop remoto, metodo seenabled
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0de7c4e013690a5d5e8ffd6b235a42ea43c445ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478862"
---
# <a name="setenabled-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="4b8c3-106">Metodo seenabled della classe Win32 \_ TSGatewayResourceAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="4b8c3-106">SetEnabled method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="4b8c3-107">Abilita o Disabilita i criteri di autorizzazione delle risorse di Desktop remoto (RD RAP) impostando la proprietà **Enabled** .</span><span class="sxs-lookup"><span data-stu-id="4b8c3-107">Enables or disables the Remote Desktop resource authorization policy (RD RAP) by setting the **Enabled** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b8c3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b8c3-108">Syntax</span></span>


```mof
uint32 SetEnabled(
  [in] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="4b8c3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4b8c3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b8c3-110">*Abilitato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b8c3-110">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b8c3-111">Se **true**, il criterio di autorizzazione connessioni Desktop remoto sarà abilitato.</span><span class="sxs-lookup"><span data-stu-id="4b8c3-111">If **True**, the RD RAP will be enabled.</span></span> <span data-ttu-id="4b8c3-112">Se **false**, il criterio di autorizzazione connessioni Desktop remoto sarà disabilitato.</span><span class="sxs-lookup"><span data-stu-id="4b8c3-112">If **False**, the RD RAP will be disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b8c3-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4b8c3-113">Return value</span></span>

<span data-ttu-id="4b8c3-114">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="4b8c3-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="4b8c3-115">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="4b8c3-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="4b8c3-116">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="4b8c3-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4b8c3-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="4b8c3-117">Remarks</span></span>

<span data-ttu-id="4b8c3-118">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="4b8c3-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="4b8c3-119">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="4b8c3-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4b8c3-120">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="4b8c3-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4b8c3-121">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="4b8c3-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4b8c3-122">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="4b8c3-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4b8c3-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b8c3-123">Requirements</span></span>



| <span data-ttu-id="4b8c3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b8c3-124">Requirement</span></span> | <span data-ttu-id="4b8c3-125">Valore</span><span class="sxs-lookup"><span data-stu-id="4b8c3-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b8c3-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b8c3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4b8c3-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4b8c3-127">None supported</span></span><br/>                                                                |
| <span data-ttu-id="4b8c3-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b8c3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4b8c3-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b8c3-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="4b8c3-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4b8c3-130">Namespace</span></span><br/>                | <span data-ttu-id="4b8c3-131">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="4b8c3-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="4b8c3-132">MOF</span><span class="sxs-lookup"><span data-stu-id="4b8c3-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b8c3-133"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b8c3-133"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b8c3-134">DLL</span><span class="sxs-lookup"><span data-stu-id="4b8c3-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b8c3-135"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b8c3-135"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="4b8c3-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b8c3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b8c3-137">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="4b8c3-137">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 


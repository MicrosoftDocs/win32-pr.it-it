---
title: Metodo sedescription della classe Win32_TSGatewayResourceAuthorizationPolicy
description: Imposta la proprietà Description per i criteri di autorizzazione delle risorse Desktop remoto (RD \ 160; RAP).
ms.assetid: 5a0f4c4b-50a4-4bd2-960f-8af7f4686d07
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto metodo di descrizione
- Metodo sedescription Servizi Desktop remoto, classe Win32_TSGatewayResourceAuthorizationPolicy
- Classe Win32_TSGatewayResourceAuthorizationPolicy Servizi Desktop remoto, metodo sedescription
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetDescription
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5dfdbcf67096dacc694061b5ff7e704c788bd2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400576"
---
# <a name="setdescription-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="f2e69-106">Metodo sedescription della classe Win32 \_ TSGatewayResourceAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="f2e69-106">SetDescription method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="f2e69-107">Imposta la proprietà **Description** per i criteri di autorizzazione delle risorse Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="f2e69-107">Sets the **Description** property for the Remote Desktop resource authorization policy (RD RAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="f2e69-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f2e69-108">Syntax</span></span>


```mof
uint32 SetDescription(
  [in] string Description
);
```



## <a name="parameters"></a><span data-ttu-id="f2e69-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f2e69-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2e69-110">*Descrizione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="f2e69-110">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2e69-111">Descrizione del criterio di autorizzazione connessioni Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="f2e69-111">Description of the RD RAP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2e69-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f2e69-112">Return value</span></span>

<span data-ttu-id="f2e69-113">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="f2e69-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="f2e69-114">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="f2e69-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="f2e69-115">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f2e69-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f2e69-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="f2e69-116">Remarks</span></span>

<span data-ttu-id="f2e69-117">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="f2e69-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="f2e69-118">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f2e69-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f2e69-119">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="f2e69-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f2e69-120">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="f2e69-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f2e69-121">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f2e69-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2e69-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2e69-122">Requirements</span></span>



| <span data-ttu-id="f2e69-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2e69-123">Requirement</span></span> | <span data-ttu-id="f2e69-124">Valore</span><span class="sxs-lookup"><span data-stu-id="f2e69-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2e69-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2e69-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f2e69-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f2e69-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="f2e69-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2e69-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f2e69-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2e69-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="f2e69-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f2e69-129">Namespace</span></span><br/>                | <span data-ttu-id="f2e69-130">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f2e69-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="f2e69-131">MOF</span><span class="sxs-lookup"><span data-stu-id="f2e69-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2e69-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2e69-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2e69-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f2e69-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2e69-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2e69-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="f2e69-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f2e69-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2e69-136">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="f2e69-136">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 


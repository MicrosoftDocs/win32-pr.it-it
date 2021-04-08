---
title: Metodo Sename della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Imposta un nuovo nome per i criteri di autorizzazione della connessione Desktop remoto (RD \ 160; LIMITE).
ms.assetid: 4a3b71d4-9b1c-46ea-b14a-fcbe32af37b5
ms.tgt_platform: multiple
keywords:
- Metodo senamer Servizi Desktop remoto
- Metodo senamer Servizi Desktop remoto, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Servizi Desktop remoto, metodo SetValue
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15fa4c374f5686f8cddbe99b5a464e6f84b4a12a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741282"
---
# <a name="setname-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="317c8-106">Metodo Sename della classe Win32 \_ TSGatewayConnectionAuthorizationPolicy</span><span class="sxs-lookup"><span data-stu-id="317c8-106">SetName method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="317c8-107">Imposta un nuovo nome per il criterio di autorizzazione della connessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="317c8-107">Sets a new name for this Remote Desktop connection authorization policy (RD CAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="317c8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="317c8-108">Syntax</span></span>


```mof
uint32 SetName(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="317c8-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="317c8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="317c8-110">*Nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="317c8-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="317c8-111">Nome del CAP di desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="317c8-111">Name of the RD CAP.</span></span> <span data-ttu-id="317c8-112">Il nome deve essere composto da un massimo di 64 caratteri, univoco (caso ignorato) e non può contenere i caratteri riservati seguenti:</span><span class="sxs-lookup"><span data-stu-id="317c8-112">The name must be 64 characters or less, unique (case is ignored), and cannot contain the following reserved characters:</span></span>

<span data-ttu-id="317c8-113"><> :; " / \\ \| ?</span><span class="sxs-lookup"><span data-stu-id="317c8-113"><> : ; " / \\ \| ?</span></span> <span data-ttu-id="317c8-114">\*\[Scheda\]</span><span class="sxs-lookup"><span data-stu-id="317c8-114">\* \[TAB\]</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="317c8-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="317c8-115">Return value</span></span>

<span data-ttu-id="317c8-116">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="317c8-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="317c8-117">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="317c8-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="317c8-118">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="317c8-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="317c8-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="317c8-119">Remarks</span></span>

<span data-ttu-id="317c8-120">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="317c8-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="317c8-121">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="317c8-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="317c8-122">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="317c8-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="317c8-123">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="317c8-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="317c8-124">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="317c8-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="317c8-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="317c8-125">Requirements</span></span>



| <span data-ttu-id="317c8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="317c8-126">Requirement</span></span> | <span data-ttu-id="317c8-127">Valore</span><span class="sxs-lookup"><span data-stu-id="317c8-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="317c8-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="317c8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="317c8-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="317c8-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="317c8-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="317c8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="317c8-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="317c8-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="317c8-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="317c8-132">Namespace</span></span><br/>                | <span data-ttu-id="317c8-133">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="317c8-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="317c8-134">MOF</span><span class="sxs-lookup"><span data-stu-id="317c8-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="317c8-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="317c8-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="317c8-136">DLL</span><span class="sxs-lookup"><span data-stu-id="317c8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="317c8-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="317c8-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="317c8-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="317c8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="317c8-139">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="317c8-139">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


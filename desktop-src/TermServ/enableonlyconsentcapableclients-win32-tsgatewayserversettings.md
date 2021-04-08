---
title: Metodo EnableOnlyConsentCapableClients della classe Win32_TSGatewayServerSettings
description: Imposta la proprietà OnlyConsentCapableClients.
ms.assetid: abc91ea8-0f3c-4b7c-9091-3c8193e610da
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo EnableOnlyConsentCapableClients
- Metodo EnableOnlyConsentCapableClients Servizi Desktop remoto, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo EnableOnlyConsentCapableClients
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableOnlyConsentCapableClients
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb671ccefe98cdc1b569bcde155071ef7cc0d9ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048090"
---
# <a name="enableonlyconsentcapableclients-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="b30d7-106">Metodo EnableOnlyConsentCapableClients della \_ classe TSGatewayServerSettings Win32</span><span class="sxs-lookup"><span data-stu-id="b30d7-106">EnableOnlyConsentCapableClients method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="b30d7-107">Imposta la proprietà **OnlyConsentCapableClients** .</span><span class="sxs-lookup"><span data-stu-id="b30d7-107">Sets the **OnlyConsentCapableClients** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="b30d7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b30d7-108">Syntax</span></span>


```mof
uint32 EnableOnlyConsentCapableClients(
  [in] boolean OnlyConsentCapableClients
);
```



## <a name="parameters"></a><span data-ttu-id="b30d7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b30d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b30d7-110">*OnlyConsentCapableClients* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b30d7-110">*OnlyConsentCapableClients* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b30d7-111">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b30d7-111">Type: **boolean**</span></span>

<span data-ttu-id="b30d7-112">Specifica il nuovo valore per la proprietà **OnlyConsentCapableClients** .</span><span class="sxs-lookup"><span data-stu-id="b30d7-112">Specifies the new value for the **OnlyConsentCapableClients** property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b30d7-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b30d7-113">Return value</span></span>

<span data-ttu-id="b30d7-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b30d7-114">Type: **uint32**</span></span>

<span data-ttu-id="b30d7-115">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="b30d7-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b30d7-116">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="b30d7-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b30d7-117">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b30d7-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b30d7-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="b30d7-118">Remarks</span></span>

<span data-ttu-id="b30d7-119">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="b30d7-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="b30d7-120">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b30d7-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b30d7-121">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="b30d7-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b30d7-122">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="b30d7-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b30d7-123">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b30d7-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b30d7-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b30d7-124">Requirements</span></span>



| <span data-ttu-id="b30d7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b30d7-125">Requirement</span></span> | <span data-ttu-id="b30d7-126">Valore</span><span class="sxs-lookup"><span data-stu-id="b30d7-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b30d7-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b30d7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b30d7-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b30d7-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b30d7-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b30d7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b30d7-130">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b30d7-130">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="b30d7-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b30d7-131">Namespace</span></span><br/>                | <span data-ttu-id="b30d7-132">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b30d7-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="b30d7-133">MOF</span><span class="sxs-lookup"><span data-stu-id="b30d7-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b30d7-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b30d7-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="b30d7-135">DLL</span><span class="sxs-lookup"><span data-stu-id="b30d7-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b30d7-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b30d7-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="b30d7-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b30d7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b30d7-138">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="b30d7-138">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 


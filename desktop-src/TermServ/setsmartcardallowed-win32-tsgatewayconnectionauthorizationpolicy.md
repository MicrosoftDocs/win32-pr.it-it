---
title: Metodo SetSmartcardAllowed della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Imposta la proprietà SmartcardAllowed, che Abilita o Disabilita il supporto per l'utilizzo di una smart card per la connessione al server Gateway Gateway Desktop remoto di Desktop remoto.
ms.assetid: 9fe1c7a9-2bab-439f-8dc2-421ed876fcf7
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetSmartcardAllowed
- Metodo SetSmartcardAllowed Servizi Desktop remoto, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Servizi Desktop remoto, metodo SetSmartcardAllowed
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetSmartcardAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 022b5461086ae05f198cbce4faaee0e9c36bf77e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400777"
---
# <a name="setsmartcardallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="0ba34-106">Metodo SetSmartcardAllowed della \_ classe TSGatewayConnectionAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="0ba34-106">SetSmartcardAllowed method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="0ba34-107">Imposta la proprietà **SmartcardAllowed** , che Abilita o Disabilita il supporto per l'utilizzo di una smart card per la connessione al server Gateway Gateway Desktop remoto di desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="0ba34-107">Sets the **SmartcardAllowed** property, which enables or disables support for using a smart card to connect to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ba34-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ba34-108">Syntax</span></span>


```mof
uint32 SetSmartcardAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a><span data-ttu-id="0ba34-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0ba34-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ba34-110">*Consentito* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ba34-110">*Allowed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ba34-111">Nuovo valore di **SmartcardAllowed** .</span><span class="sxs-lookup"><span data-stu-id="0ba34-111">New **SmartcardAllowed** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ba34-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0ba34-112">Return value</span></span>

<span data-ttu-id="0ba34-113">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="0ba34-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="0ba34-114">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="0ba34-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="0ba34-115">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="0ba34-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0ba34-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="0ba34-116">Remarks</span></span>

<span data-ttu-id="0ba34-117">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="0ba34-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="0ba34-118">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="0ba34-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0ba34-119">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="0ba34-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0ba34-120">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="0ba34-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0ba34-121">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0ba34-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0ba34-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ba34-122">Requirements</span></span>



| <span data-ttu-id="0ba34-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ba34-123">Requirement</span></span> | <span data-ttu-id="0ba34-124">Valore</span><span class="sxs-lookup"><span data-stu-id="0ba34-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ba34-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ba34-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0ba34-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0ba34-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="0ba34-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ba34-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0ba34-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0ba34-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="0ba34-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0ba34-129">Namespace</span></span><br/>                | <span data-ttu-id="0ba34-130">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0ba34-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="0ba34-131">MOF</span><span class="sxs-lookup"><span data-stu-id="0ba34-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ba34-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0ba34-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="0ba34-133">DLL</span><span class="sxs-lookup"><span data-stu-id="0ba34-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ba34-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ba34-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="0ba34-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ba34-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ba34-136">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="0ba34-136">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


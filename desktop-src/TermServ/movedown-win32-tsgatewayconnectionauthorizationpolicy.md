---
title: Metodo MoveDown della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Sposta i criteri di autorizzazione della connessione di Desktop remoto correnti (RD \ 160; CAP) una posizione verso il basso nell'ordine in cui RD \ 160; I tappi vengono valutati.
ms.assetid: 57349e59-e200-4789-bbcb-d474eacde39d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo MoveDown
- Metodo MoveDown Servizi Desktop remoto, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Servizi Desktop remoto, metodo MoveDown
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.MoveDown
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92e5b2e2b56a60d78f827f8989c0317cb003e511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302601"
---
# <a name="movedown-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="fb2a4-106">Metodo MoveDown della \_ classe TSGatewayConnectionAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="fb2a4-106">MoveDown method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="fb2a4-107">Sposta i criteri di autorizzazione connessione del Desktop remoto corrente (RD CAP) in un punto inferiore nell'ordine in cui vengono valutati i tappi RD.</span><span class="sxs-lookup"><span data-stu-id="fb2a4-107">Moves the current Remote Desktop connection authorization policy (RD CAP) one position down in the order that RD CAPs are evaluated.</span></span> <span data-ttu-id="fb2a4-108">Questo metodo incrementa la proprietà **Order** del criterio di autorizzazione connessioni Desktop remoto corrente e decrementa la proprietà **Order** del CAP di desktop remoto che ha seguito il limite di Rd corrente.</span><span class="sxs-lookup"><span data-stu-id="fb2a4-108">This method increments the **Order** property of the current RD CAP and decrements the **Order** property of the RD CAP that followed the current RD CAP.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb2a4-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb2a4-109">Syntax</span></span>


```mof
uint32 MoveDown();
```



## <a name="parameters"></a><span data-ttu-id="fb2a4-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="fb2a4-110">Parameters</span></span>

<span data-ttu-id="fb2a4-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="fb2a4-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fb2a4-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fb2a4-112">Return value</span></span>

<span data-ttu-id="fb2a4-113">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="fb2a4-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="fb2a4-114">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="fb2a4-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="fb2a4-115">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="fb2a4-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fb2a4-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="fb2a4-116">Remarks</span></span>

<span data-ttu-id="fb2a4-117">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="fb2a4-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="fb2a4-118">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="fb2a4-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fb2a4-119">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="fb2a4-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fb2a4-120">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="fb2a4-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fb2a4-121">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="fb2a4-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb2a4-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb2a4-122">Requirements</span></span>



| <span data-ttu-id="fb2a4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb2a4-123">Requirement</span></span> | <span data-ttu-id="fb2a4-124">Valore</span><span class="sxs-lookup"><span data-stu-id="fb2a4-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb2a4-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb2a4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fb2a4-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fb2a4-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="fb2a4-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb2a4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fb2a4-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fb2a4-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="fb2a4-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fb2a4-129">Namespace</span></span><br/>                | <span data-ttu-id="fb2a4-130">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="fb2a4-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="fb2a4-131">MOF</span><span class="sxs-lookup"><span data-stu-id="fb2a4-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb2a4-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fb2a4-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="fb2a4-133">DLL</span><span class="sxs-lookup"><span data-stu-id="fb2a4-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb2a4-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb2a4-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="fb2a4-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb2a4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb2a4-136">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="fb2a4-136">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="fb2a4-137">**MoveUp**</span><span class="sxs-lookup"><span data-stu-id="fb2a4-137">**MoveUp**</span></span>](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


---
title: Metodo MoveUp della classe Win32_TSGatewayConnectionAuthorizationPolicy
description: Sposta i criteri di autorizzazione della connessione di Desktop remoto correnti (RD \ 160; CAP) una posizione verso l'alto nell'ordine in cui RD \ 160; I tappi vengono valutati.
ms.assetid: 5c9ff18d-e019-4a52-af0b-75fa61d77b7a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo MoveUp
- Metodo MoveUp Servizi Desktop remoto, classe Win32_TSGatewayConnectionAuthorizationPolicy
- Classe Win32_TSGatewayConnectionAuthorizationPolicy Servizi Desktop remoto, metodo MoveUp
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.MoveUp
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81973261d156328aa1f306c26dd8bd9bdd20511f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479096"
---
# <a name="moveup-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="07d11-106">Metodo MoveUp della \_ classe TSGatewayConnectionAuthorizationPolicy Win32</span><span class="sxs-lookup"><span data-stu-id="07d11-106">MoveUp method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="07d11-107">Sposta i criteri di autorizzazione della connessione del Desktop remoto corrente (RD CAP) in una posizione verso l'alto nell'ordine in cui vengono valutati i tappi RD.</span><span class="sxs-lookup"><span data-stu-id="07d11-107">Moves the current Remote Desktop connection authorization policy (RD CAP) one position up in the order that RD CAPs are evaluated.</span></span> <span data-ttu-id="07d11-108">Questo metodo decrementa la proprietà **Order** del criterio di autorizzazione connessioni Desktop remoto corrente e incrementa la proprietà **Order** del CAP di Rd che precedeva il CAP di Rd corrente.</span><span class="sxs-lookup"><span data-stu-id="07d11-108">This method decrements the **Order** property of the current RD CAP and increments the **Order** property of the RD CAP that preceded the current RD CAP.</span></span>

## <a name="syntax"></a><span data-ttu-id="07d11-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07d11-109">Syntax</span></span>


```mof
uint32 MoveUp();
```



## <a name="parameters"></a><span data-ttu-id="07d11-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="07d11-110">Parameters</span></span>

<span data-ttu-id="07d11-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="07d11-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="07d11-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="07d11-112">Return value</span></span>

<span data-ttu-id="07d11-113">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="07d11-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="07d11-114">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="07d11-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="07d11-115">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="07d11-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="07d11-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="07d11-116">Remarks</span></span>

<span data-ttu-id="07d11-117">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="07d11-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="07d11-118">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="07d11-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="07d11-119">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="07d11-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="07d11-120">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="07d11-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="07d11-121">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="07d11-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="07d11-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07d11-122">Requirements</span></span>



| <span data-ttu-id="07d11-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="07d11-123">Requirement</span></span> | <span data-ttu-id="07d11-124">Valore</span><span class="sxs-lookup"><span data-stu-id="07d11-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="07d11-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07d11-125">Minimum supported client</span></span><br/> | <span data-ttu-id="07d11-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="07d11-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="07d11-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07d11-127">Minimum supported server</span></span><br/> | <span data-ttu-id="07d11-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07d11-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="07d11-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="07d11-129">Namespace</span></span><br/>                | <span data-ttu-id="07d11-130">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="07d11-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="07d11-131">MOF</span><span class="sxs-lookup"><span data-stu-id="07d11-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07d11-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="07d11-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="07d11-133">DLL</span><span class="sxs-lookup"><span data-stu-id="07d11-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07d11-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07d11-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="07d11-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07d11-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07d11-136">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="07d11-136">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="07d11-137">**MoveDown**</span><span class="sxs-lookup"><span data-stu-id="07d11-137">**MoveDown**</span></span>](movedown-win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


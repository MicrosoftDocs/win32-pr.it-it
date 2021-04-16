---
title: Metodo MoveDown della classe Win32_TSGatewayRADIUSServer
description: Sposta questo server di Remote Authentication Dial-In User Service (RADIUS) una posizione verso il basso nell'ordine di priorità.
ms.assetid: 1b12d2a0-1463-4bd7-9b92-5df2ba799a8a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo MoveDown
- Metodo MoveDown Servizi Desktop remoto, classe Win32_TSGatewayRADIUSServer
- Classe Win32_TSGatewayRADIUSServer Servizi Desktop remoto, metodo MoveDown
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.MoveDown
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b652eb5e9cfc36f0d41e14d9953b295d35e660be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517698"
---
# <a name="movedown-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="55f20-106">Metodo MoveDown della \_ classe TSGatewayRADIUSServer Win32</span><span class="sxs-lookup"><span data-stu-id="55f20-106">MoveDown method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="55f20-107">Sposta questo server di Remote Authentication Dial-In User Service (RADIUS) una posizione verso il basso nell'ordine di priorità.</span><span class="sxs-lookup"><span data-stu-id="55f20-107">Moves this Remote Authentication Dial-In User Service (RADIUS) server one position down in the priority order.</span></span> <span data-ttu-id="55f20-108">Questo metodo incrementa la proprietà **Priority** del server RADIUS corrente e decrementa la proprietà **Priority** del server RADIUS che segue il server RADIUS corrente.</span><span class="sxs-lookup"><span data-stu-id="55f20-108">This method increments the **Priority** property of the current RADIUS server and decrements the **Priority** property of the RADIUS server that follows the current RADIUS server.</span></span>

## <a name="syntax"></a><span data-ttu-id="55f20-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55f20-109">Syntax</span></span>


```mof
uint32 MoveDown();
```



## <a name="parameters"></a><span data-ttu-id="55f20-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="55f20-110">Parameters</span></span>

<span data-ttu-id="55f20-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="55f20-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="55f20-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="55f20-112">Return value</span></span>

<span data-ttu-id="55f20-113">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="55f20-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="55f20-114">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="55f20-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="55f20-115">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="55f20-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="55f20-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="55f20-116">Remarks</span></span>

<span data-ttu-id="55f20-117">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="55f20-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="55f20-118">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="55f20-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="55f20-119">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="55f20-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="55f20-120">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="55f20-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="55f20-121">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="55f20-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="55f20-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55f20-122">Requirements</span></span>



| <span data-ttu-id="55f20-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="55f20-123">Requirement</span></span> | <span data-ttu-id="55f20-124">Valore</span><span class="sxs-lookup"><span data-stu-id="55f20-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="55f20-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55f20-125">Minimum supported client</span></span><br/> | <span data-ttu-id="55f20-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="55f20-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="55f20-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55f20-127">Minimum supported server</span></span><br/> | <span data-ttu-id="55f20-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55f20-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="55f20-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="55f20-129">Namespace</span></span><br/>                | <span data-ttu-id="55f20-130">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="55f20-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="55f20-131">MOF</span><span class="sxs-lookup"><span data-stu-id="55f20-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55f20-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="55f20-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="55f20-133">DLL</span><span class="sxs-lookup"><span data-stu-id="55f20-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55f20-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55f20-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="55f20-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55f20-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55f20-136">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="55f20-136">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 


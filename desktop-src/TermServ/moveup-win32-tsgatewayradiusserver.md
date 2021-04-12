---
title: Metodo MoveUp della classe Win32_TSGatewayRADIUSServer
description: Sposta questo server di Remote Authentication Dial-In User Service (RADIUS) una posizione verso l'alto nell'ordine di priorità.
ms.assetid: 060bb90d-72c0-4364-a44f-c6368434b174
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo MoveUp
- Metodo MoveUp Servizi Desktop remoto, classe Win32_TSGatewayRADIUSServer
- Classe Win32_TSGatewayRADIUSServer Servizi Desktop remoto, metodo MoveUp
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.MoveUp
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca93eee44abd147576c6e678dce871ae4d49d921
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518928"
---
# <a name="moveup-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="fface-106">Metodo MoveUp della \_ classe TSGatewayRADIUSServer Win32</span><span class="sxs-lookup"><span data-stu-id="fface-106">MoveUp method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="fface-107">Sposta questo server di Remote Authentication Dial-In User Service (RADIUS) una posizione verso l'alto nell'ordine di priorità.</span><span class="sxs-lookup"><span data-stu-id="fface-107">Moves this Remote Authentication Dial-In User Service (RADIUS) server one position up in the priority order.</span></span> <span data-ttu-id="fface-108">Questo metodo decrementa la proprietà **Priority** del server RADIUS corrente e incrementa la proprietà **Priority** del server RADIUS che precede il server RADIUS corrente.</span><span class="sxs-lookup"><span data-stu-id="fface-108">This method decrements the **Priority** property of the current RADIUS server and increments the **Priority** property of the RADIUS server that precedes the current RADIUS server.</span></span>

## <a name="syntax"></a><span data-ttu-id="fface-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fface-109">Syntax</span></span>


```mof
uint32 MoveUp();
```



## <a name="parameters"></a><span data-ttu-id="fface-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="fface-110">Parameters</span></span>

<span data-ttu-id="fface-111">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="fface-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fface-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fface-112">Return value</span></span>

<span data-ttu-id="fface-113">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="fface-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="fface-114">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="fface-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="fface-115">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="fface-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fface-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="fface-116">Remarks</span></span>

<span data-ttu-id="fface-117">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="fface-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="fface-118">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="fface-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fface-119">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="fface-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fface-120">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="fface-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fface-121">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="fface-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fface-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fface-122">Requirements</span></span>



| <span data-ttu-id="fface-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fface-123">Requirement</span></span> | <span data-ttu-id="fface-124">Valore</span><span class="sxs-lookup"><span data-stu-id="fface-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fface-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fface-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fface-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fface-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="fface-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fface-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fface-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fface-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="fface-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fface-129">Namespace</span></span><br/>                | <span data-ttu-id="fface-130">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="fface-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="fface-131">MOF</span><span class="sxs-lookup"><span data-stu-id="fface-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fface-132"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fface-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="fface-133">DLL</span><span class="sxs-lookup"><span data-stu-id="fface-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fface-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fface-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="fface-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fface-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fface-136">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="fface-136">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 


---
title: Metodo Disconnect della classe Win32_TSGatewayConnection
description: Disconnette la connessione dal server Gateway Desktop remoto (Gateway Desktop remoto).
ms.assetid: 8c424e58-aa89-4ec6-acea-5b571d3f4c21
ms.tgt_platform: multiple
keywords:
- Disconnetti metodo Servizi Desktop remoto
- Metodo Disconnect Servizi Desktop remoto, classe Win32_TSGatewayConnection
- Classe Win32_TSGatewayConnection Servizi Desktop remoto, metodo Disconnect
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.Disconnect
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53101e5ca3529c5033adc918f1f9ad11a3b45f7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740031"
---
# <a name="disconnect-method-of-the-win32_tsgatewayconnection-class"></a><span data-ttu-id="21ae1-106">Metodo Disconnect della \_ classe TSGatewayConnection di Win32</span><span class="sxs-lookup"><span data-stu-id="21ae1-106">Disconnect method of the Win32\_TSGatewayConnection class</span></span>

<span data-ttu-id="21ae1-107">Disconnette la connessione dal server Gateway Desktop remoto (Gateway Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="21ae1-107">Disconnects the connection from the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="21ae1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21ae1-108">Syntax</span></span>


```mof
uint32 Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="21ae1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="21ae1-109">Parameters</span></span>

<span data-ttu-id="21ae1-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="21ae1-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="21ae1-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21ae1-111">Return value</span></span>

<span data-ttu-id="21ae1-112">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="21ae1-112">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="21ae1-113">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="21ae1-113">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="21ae1-114">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="21ae1-114">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="21ae1-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="21ae1-115">Remarks</span></span>

<span data-ttu-id="21ae1-116">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="21ae1-116">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="21ae1-117">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="21ae1-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="21ae1-118">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="21ae1-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="21ae1-119">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="21ae1-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="21ae1-120">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="21ae1-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="21ae1-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21ae1-121">Requirements</span></span>



| <span data-ttu-id="21ae1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="21ae1-122">Requirement</span></span> | <span data-ttu-id="21ae1-123">Valore</span><span class="sxs-lookup"><span data-stu-id="21ae1-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="21ae1-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21ae1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="21ae1-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="21ae1-125">None supported</span></span><br/>                                                                |
| <span data-ttu-id="21ae1-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21ae1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="21ae1-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="21ae1-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="21ae1-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="21ae1-128">Namespace</span></span><br/>                | <span data-ttu-id="21ae1-129">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="21ae1-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="21ae1-130">MOF</span><span class="sxs-lookup"><span data-stu-id="21ae1-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="21ae1-131"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="21ae1-131"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="21ae1-132">DLL</span><span class="sxs-lookup"><span data-stu-id="21ae1-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21ae1-133"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21ae1-133"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="21ae1-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21ae1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21ae1-135">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="21ae1-135">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> </dl>

 


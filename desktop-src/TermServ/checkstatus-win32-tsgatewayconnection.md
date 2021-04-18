---
title: Metodo CheckStatus della classe Win32_TSGatewayConnection
description: Controlla lo stato di una connessione del server Gateway Desktop remoto (Gateway Desktop remoto) a un altro computer e determina se il computer di destinazione è configurato per il bilanciamento del carico.
ms.assetid: e8ee3d40-76eb-401f-b255-bccd7ba8c058
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo CheckStatus
- Metodo CheckStatus Servizi Desktop remoto, classe Win32_TSGatewayConnection
- Classe Win32_TSGatewayConnection Servizi Desktop remoto, metodo CheckStatus
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection.CheckStatus
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: babb083af5c0581abe27d442a466c3d6114b957a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301232"
---
# <a name="checkstatus-method-of-the-win32_tsgatewayconnection-class"></a><span data-ttu-id="73935-106">Metodo CheckStatus della \_ classe TSGatewayConnection Win32</span><span class="sxs-lookup"><span data-stu-id="73935-106">CheckStatus method of the Win32\_TSGatewayConnection class</span></span>

<span data-ttu-id="73935-107">Controlla lo stato di una connessione del server Gateway Desktop remoto (Gateway Desktop remoto) a un altro computer e determina se il computer di destinazione è configurato per il bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="73935-107">Checks the status of a Remote Desktop Gateway (RD Gateway) server connection to another computer, and determines whether the target computer is configured for load balancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="73935-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="73935-108">Syntax</span></span>


```mof
uint32 CheckStatus(
  [in] string ServerName,
  [in] string EndPointName
);
```



## <a name="parameters"></a><span data-ttu-id="73935-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="73935-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73935-110">*Nomeserver* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73935-110">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73935-111">Nome del server Gateway Desktop remoto di origine da cui viene verificata la connessione.</span><span class="sxs-lookup"><span data-stu-id="73935-111">The name of the source RD Gateway server from which the connection is checked.</span></span>

</dd> <dt>

<span data-ttu-id="73935-112">*EndpointName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73935-112">*EndPointName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73935-113">Nome del server di destinazione (l'endpoint) a cui viene effettuato il controllo dell'accesso dal server di origine.</span><span class="sxs-lookup"><span data-stu-id="73935-113">The name of the target server (the endpoint) to which access is checked from the source server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73935-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="73935-114">Return value</span></span>

<span data-ttu-id="73935-115">Questo metodo restituisce i valori restituiti possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="73935-115">This method returns the following possible return values.</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="73935-116">0</span><span class="sxs-lookup"><span data-stu-id="73935-116">0</span></span>

<span data-ttu-id="73935-117">Lo stato della connessione è OK.</span><span class="sxs-lookup"><span data-stu-id="73935-117">The connection status is OK.</span></span> <span data-ttu-id="73935-118">L'endpoint è raggiungibile ed è configurato per il bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="73935-118">The endpoint is reachable and is configured for load balancing.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="73935-119">1</span><span class="sxs-lookup"><span data-stu-id="73935-119">1</span></span>

<span data-ttu-id="73935-120">Lo stato della connessione è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="73935-120">The connection status is unknown.</span></span> <span data-ttu-id="73935-121">È probabile che si sia verificata un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="73935-121">Most likely, an exception occurred.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="73935-122">0x80075c34</span><span class="sxs-lookup"><span data-stu-id="73935-122">0x80075c34</span></span>

<span data-ttu-id="73935-123">L'endpoint non è raggiungibile o non è configurato per il bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="73935-123">The endpoint is either not reachable, or it is not configured for load balancing.</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="73935-124">0x80075c32</span><span class="sxs-lookup"><span data-stu-id="73935-124">0x80075c32</span></span>

<span data-ttu-id="73935-125">Si è verificato un errore di stato.</span><span class="sxs-lookup"><span data-stu-id="73935-125">A status error occurred.</span></span> <span data-ttu-id="73935-126">L'endpoint è raggiungibile, ma il servizio di bilanciamento del carico RPC/HTTP (RPCHTTPLBS) non è stato avviato nel computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="73935-126">The endpoint is reachable, but the RPC/HTTP Load Balancing Service (RPCHTTPLBS) service is not started on the target computer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="73935-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="73935-127">Remarks</span></span>

<span data-ttu-id="73935-128">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="73935-128">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="73935-129">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="73935-129">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="73935-130">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="73935-130">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="73935-131">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="73935-131">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="73935-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73935-132">Requirements</span></span>



| <span data-ttu-id="73935-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="73935-133">Requirement</span></span> | <span data-ttu-id="73935-134">Valore</span><span class="sxs-lookup"><span data-stu-id="73935-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="73935-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73935-135">Minimum supported client</span></span><br/> | <span data-ttu-id="73935-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="73935-136">None supported</span></span><br/>                                                                |
| <span data-ttu-id="73935-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73935-137">Minimum supported server</span></span><br/> | <span data-ttu-id="73935-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73935-138">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="73935-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="73935-139">Namespace</span></span><br/>                | <span data-ttu-id="73935-140">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="73935-140">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="73935-141">MOF</span><span class="sxs-lookup"><span data-stu-id="73935-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73935-142"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="73935-142"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="73935-143">DLL</span><span class="sxs-lookup"><span data-stu-id="73935-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73935-144"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73935-144"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="73935-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73935-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73935-146">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="73935-146">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> </dl>

 


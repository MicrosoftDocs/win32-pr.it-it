---
title: Metodo GetLogEventName della classe Win32_TSGatewayServerSettings
description: Restituisce il nome dell'evento di log per l'indice dell'evento di log specificato.
ms.assetid: ca31ef8e-ab84-4132-a6d2-232b1e69230a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetLogEventName
- Metodo GetLogEventName Servizi Desktop remoto, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo GetLogEventName
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetLogEventName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e9c608b7a12d3de48d75ecd5651df94d0267fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301900"
---
# <a name="getlogeventname-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="0748f-106">Metodo GetLogEventName della \_ classe TSGatewayServerSettings Win32</span><span class="sxs-lookup"><span data-stu-id="0748f-106">GetLogEventName method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="0748f-107">Restituisce il nome dell'evento di log per l'indice dell'evento di log specificato.</span><span class="sxs-lookup"><span data-stu-id="0748f-107">Returns the log event name for the specified log event index.</span></span>

## <a name="syntax"></a><span data-ttu-id="0748f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0748f-108">Syntax</span></span>


```mof
uint32 GetLogEventName(
  [in]  uint32 EventIndex,
  [out] string EventName
);
```



## <a name="parameters"></a><span data-ttu-id="0748f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0748f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0748f-110">*EventIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0748f-110">*EventIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0748f-111">Indice dell'evento del log.</span><span class="sxs-lookup"><span data-stu-id="0748f-111">Index of the log event.</span></span> <span data-ttu-id="0748f-112">Il valore deve essere compreso tra zero e il valore della proprietà **MaxLogEvents** .</span><span class="sxs-lookup"><span data-stu-id="0748f-112">The value must be between zero and the value of the **MaxLogEvents** property.</span></span>

</dd> <dt>

<span data-ttu-id="0748f-113">*EventName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0748f-113">*EventName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0748f-114">Nome dell'evento specificato.</span><span class="sxs-lookup"><span data-stu-id="0748f-114">Name of the specified event.</span></span> <span data-ttu-id="0748f-115">Nell'elenco seguente sono riportati i valori possibili.</span><span class="sxs-lookup"><span data-stu-id="0748f-115">The following list displays the possible values.</span></span>

<dt>

<span id="LogChannelDisconnect"></span><span id="logchanneldisconnect"></span><span id="LOGCHANNELDISCONNECT"></span>

<span data-ttu-id="0748f-116"><span id="LogChannelDisconnect"></span><span id="logchanneldisconnect"></span><span id="LOGCHANNELDISCONNECT"></span>**LogChannelDisconnect**</span><span class="sxs-lookup"><span data-stu-id="0748f-116"><span id="LogChannelDisconnect"></span><span id="logchanneldisconnect"></span><span id="LOGCHANNELDISCONNECT"></span>**LogChannelDisconnect**</span></span>


</dt> <dd>

<span data-ttu-id="0748f-117">L'utente è stato disconnesso dalla risorsa.</span><span class="sxs-lookup"><span data-stu-id="0748f-117">User successfully disconnected from the resource.</span></span>

</dd> <dt>

<span id="LogFailureChannelConnect"></span><span id="logfailurechannelconnect"></span><span id="LOGFAILURECHANNELCONNECT"></span>

<span data-ttu-id="0748f-118"><span id="LogFailureChannelConnect"></span><span id="logfailurechannelconnect"></span><span id="LOGFAILURECHANNELCONNECT"></span>**LogFailureChannelConnect**</span><span class="sxs-lookup"><span data-stu-id="0748f-118"><span id="LogFailureChannelConnect"></span><span id="logfailurechannelconnect"></span><span id="LOGFAILURECHANNELCONNECT"></span>**LogFailureChannelConnect**</span></span>


</dt> <dd>

<span data-ttu-id="0748f-119">L'utente non è riuscito a connettersi alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="0748f-119">User failed to connect to the resource.</span></span>

</dd> <dt>

<span id="LogFailureConnectionAuthorizationCheck"></span><span id="logfailureconnectionauthorizationcheck"></span><span id="LOGFAILURECONNECTIONAUTHORIZATIONCHECK"></span>

<span data-ttu-id="0748f-120"><span id="LogFailureConnectionAuthorizationCheck"></span><span id="logfailureconnectionauthorizationcheck"></span><span id="LOGFAILURECONNECTIONAUTHORIZATIONCHECK"></span>**LogFailureConnectionAuthorizationCheck**</span><span class="sxs-lookup"><span data-stu-id="0748f-120"><span id="LogFailureConnectionAuthorizationCheck"></span><span id="logfailureconnectionauthorizationcheck"></span><span id="LOGFAILURECONNECTIONAUTHORIZATIONCHECK"></span>**LogFailureConnectionAuthorizationCheck**</span></span>


</dt> <dd>

<span data-ttu-id="0748f-121">Autorizzazione connessione utente non riuscita.</span><span class="sxs-lookup"><span data-stu-id="0748f-121">User failed connection authorization.</span></span>

</dd> <dt>

<span id="LogFailureResourceAuthorizationCheck"></span><span id="logfailureresourceauthorizationcheck"></span><span id="LOGFAILURERESOURCEAUTHORIZATIONCHECK"></span>

<span data-ttu-id="0748f-122"><span id="LogFailureResourceAuthorizationCheck"></span><span id="logfailureresourceauthorizationcheck"></span><span id="LOGFAILURERESOURCEAUTHORIZATIONCHECK"></span>**LogFailureResourceAuthorizationCheck**</span><span class="sxs-lookup"><span data-stu-id="0748f-122"><span id="LogFailureResourceAuthorizationCheck"></span><span id="logfailureresourceauthorizationcheck"></span><span id="LOGFAILURERESOURCEAUTHORIZATIONCHECK"></span>**LogFailureResourceAuthorizationCheck**</span></span>


</dt> <dd>

<span data-ttu-id="0748f-123">Autorizzazione risorse utente non riuscita.</span><span class="sxs-lookup"><span data-stu-id="0748f-123">User failed resource authorization.</span></span>

</dd> <dt>

<span id="LogSuccessfulChannelConnect"></span><span id="logsuccessfulchannelconnect"></span><span id="LOGSUCCESSFULCHANNELCONNECT"></span>

<span data-ttu-id="0748f-124"><span id="LogSuccessfulChannelConnect"></span><span id="logsuccessfulchannelconnect"></span><span id="LOGSUCCESSFULCHANNELCONNECT"></span>**LogSuccessfulChannelConnect**</span><span class="sxs-lookup"><span data-stu-id="0748f-124"><span id="LogSuccessfulChannelConnect"></span><span id="logsuccessfulchannelconnect"></span><span id="LOGSUCCESSFULCHANNELCONNECT"></span>**LogSuccessfulChannelConnect**</span></span>


</dt> <dd>

<span data-ttu-id="0748f-125">L'utente ha eseguito la connessione alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="0748f-125">User successfully connected to the resource.</span></span>

</dd> <dt>

<span id="LogSuccessfulConnectionAuthorizationCheck"></span><span id="logsuccessfulconnectionauthorizationcheck"></span><span id="LOGSUCCESSFULCONNECTIONAUTHORIZATIONCHECK"></span>

<span data-ttu-id="0748f-126"><span id="LogSuccessfulConnectionAuthorizationCheck"></span><span id="logsuccessfulconnectionauthorizationcheck"></span><span id="LOGSUCCESSFULCONNECTIONAUTHORIZATIONCHECK"></span>**LogSuccessfulConnectionAuthorizationCheck**</span><span class="sxs-lookup"><span data-stu-id="0748f-126"><span id="LogSuccessfulConnectionAuthorizationCheck"></span><span id="logsuccessfulconnectionauthorizationcheck"></span><span id="LOGSUCCESSFULCONNECTIONAUTHORIZATIONCHECK"></span>**LogSuccessfulConnectionAuthorizationCheck**</span></span>


</dt> <dd>

<span data-ttu-id="0748f-127">L'utente ha superato l'autorizzazione di connessione.</span><span class="sxs-lookup"><span data-stu-id="0748f-127">User successfully passed connection authorization.</span></span>

</dd> <dt>

<span id="LogSuccessfulResourceAuthorizationCheck"></span><span id="logsuccessfulresourceauthorizationcheck"></span><span id="LOGSUCCESSFULRESOURCEAUTHORIZATIONCHECK"></span>

<span data-ttu-id="0748f-128"><span id="LogSuccessfulResourceAuthorizationCheck"></span><span id="logsuccessfulresourceauthorizationcheck"></span><span id="LOGSUCCESSFULRESOURCEAUTHORIZATIONCHECK"></span>**LogSuccessfulResourceAuthorizationCheck**</span><span class="sxs-lookup"><span data-stu-id="0748f-128"><span id="LogSuccessfulResourceAuthorizationCheck"></span><span id="logsuccessfulresourceauthorizationcheck"></span><span id="LOGSUCCESSFULRESOURCEAUTHORIZATIONCHECK"></span>**LogSuccessfulResourceAuthorizationCheck**</span></span>


</dt> <dd>

<span data-ttu-id="0748f-129">L'utente ha superato l'autorizzazione risorse.</span><span class="sxs-lookup"><span data-stu-id="0748f-129">User successfully passed resource authorization.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0748f-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0748f-130">Return value</span></span>

<span data-ttu-id="0748f-131">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="0748f-131">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="0748f-132">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="0748f-132">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="0748f-133">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="0748f-133">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0748f-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="0748f-134">Remarks</span></span>

<span data-ttu-id="0748f-135">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="0748f-135">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="0748f-136">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="0748f-136">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0748f-137">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="0748f-137">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0748f-138">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="0748f-138">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0748f-139">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0748f-139">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0748f-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0748f-140">Requirements</span></span>



| <span data-ttu-id="0748f-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="0748f-141">Requirement</span></span> | <span data-ttu-id="0748f-142">Valore</span><span class="sxs-lookup"><span data-stu-id="0748f-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0748f-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0748f-143">Minimum supported client</span></span><br/> | <span data-ttu-id="0748f-144">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0748f-144">None supported</span></span><br/>                                                                |
| <span data-ttu-id="0748f-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0748f-145">Minimum supported server</span></span><br/> | <span data-ttu-id="0748f-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0748f-146">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="0748f-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0748f-147">Namespace</span></span><br/>                | <span data-ttu-id="0748f-148">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0748f-148">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="0748f-149">MOF</span><span class="sxs-lookup"><span data-stu-id="0748f-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0748f-150"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0748f-150"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="0748f-151">DLL</span><span class="sxs-lookup"><span data-stu-id="0748f-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0748f-152"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0748f-152"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="0748f-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0748f-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0748f-154">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="0748f-154">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="0748f-155">**EnableLogEvent**</span><span class="sxs-lookup"><span data-stu-id="0748f-155">**EnableLogEvent**</span></span>](enablelogevent-win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="0748f-156">**IsLogEventEnabled**</span><span class="sxs-lookup"><span data-stu-id="0748f-156">**IsLogEventEnabled**</span></span>](islogeventenabled-win32-tsgatewayserversettings.md)
</dt> </dl>

 


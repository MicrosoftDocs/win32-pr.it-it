---
title: Metodo EnableLogEvent della classe Win32_TSGatewayServerSettings
description: Abilita o Disabilita la registrazione del tipo di evento specificato.
ms.assetid: e901ef51-2ae2-4123-902a-ac359f3eb959
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo EnableLogEvent
- Metodo EnableLogEvent Servizi Desktop remoto, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo EnableLogEvent
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableLogEvent
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e72f7cb8567c7f2d5c3ca79d241013e2bd64a5e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479318"
---
# <a name="enablelogevent-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="9c5d7-106">Metodo EnableLogEvent della \_ classe TSGatewayServerSettings Win32</span><span class="sxs-lookup"><span data-stu-id="9c5d7-106">EnableLogEvent method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="9c5d7-107">Abilita o Disabilita la registrazione del tipo di evento specificato.</span><span class="sxs-lookup"><span data-stu-id="9c5d7-107">Enables or disables logging of the specified event type.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c5d7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9c5d7-108">Syntax</span></span>


```mof
uint32 EnableLogEvent(
  [in] string  EventName,
  [in] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="9c5d7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9c5d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c5d7-110">*EventName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9c5d7-110">*EventName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c5d7-111">Nome dell'evento.</span><span class="sxs-lookup"><span data-stu-id="9c5d7-111">Name of the event.</span></span> <span data-ttu-id="9c5d7-112">Questo valore deve essere recuperato tramite il metodo [**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="9c5d7-112">This value should be retrieved by using the [**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md) method.</span></span>

<dt>

<span data-ttu-id="9c5d7-113">LogChannelDisconnect</span><span class="sxs-lookup"><span data-stu-id="9c5d7-113">LogChannelDisconnect</span></span>
</dt> <dd>

<span data-ttu-id="9c5d7-114">L'utente è stato disconnesso dalla risorsa.</span><span class="sxs-lookup"><span data-stu-id="9c5d7-114">User successfully disconnected from the resource.</span></span>

</dd> <dt>

<span data-ttu-id="9c5d7-115">LogFailedChannelConnect</span><span class="sxs-lookup"><span data-stu-id="9c5d7-115">LogFailedChannelConnect</span></span>
</dt> <dd>

<span data-ttu-id="9c5d7-116">L'utente non è riuscito a connettersi alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="9c5d7-116">User failed to connect to the resource.</span></span>

</dd> <dt>

<span data-ttu-id="9c5d7-117">LogFailureNetworkAccessCheck</span><span class="sxs-lookup"><span data-stu-id="9c5d7-117">LogFailureNetworkAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="9c5d7-118">Autorizzazione connessione utente non riuscita.</span><span class="sxs-lookup"><span data-stu-id="9c5d7-118">User failed connection authorization.</span></span>

</dd> <dt>

<span data-ttu-id="9c5d7-119">LogFailureResourceAccessCheck</span><span class="sxs-lookup"><span data-stu-id="9c5d7-119">LogFailureResourceAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="9c5d7-120">Autorizzazione risorse utente non riuscita.</span><span class="sxs-lookup"><span data-stu-id="9c5d7-120">User failed resource authorization.</span></span>

</dd> <dt>

<span data-ttu-id="9c5d7-121">LogSuccessChannelConnect</span><span class="sxs-lookup"><span data-stu-id="9c5d7-121">LogSuccessChannelConnect</span></span>
</dt> <dd>

<span data-ttu-id="9c5d7-122">L'utente ha eseguito la connessione alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="9c5d7-122">User successfully connected to the resource.</span></span>

</dd> <dt>

<span data-ttu-id="9c5d7-123">LogSuccessfulNetworkAccessCheck</span><span class="sxs-lookup"><span data-stu-id="9c5d7-123">LogSuccessfulNetworkAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="9c5d7-124">L'utente ha superato l'autorizzazione di connessione.</span><span class="sxs-lookup"><span data-stu-id="9c5d7-124">User successfully passed connection authorization.</span></span>

</dd> <dt>

<span data-ttu-id="9c5d7-125">LogSuccessfulResourceAccessCheck</span><span class="sxs-lookup"><span data-stu-id="9c5d7-125">LogSuccessfulResourceAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="9c5d7-126">L'utente ha superato l'autorizzazione risorse.</span><span class="sxs-lookup"><span data-stu-id="9c5d7-126">User successfully passed resource authorization.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9c5d7-127">*Abilitato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9c5d7-127">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c5d7-128">Specifica se l'evento deve essere abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="9c5d7-128">Specifies whether the event should be enabled or disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c5d7-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9c5d7-129">Return value</span></span>

<span data-ttu-id="9c5d7-130">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="9c5d7-130">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="9c5d7-131">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="9c5d7-131">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="9c5d7-132">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9c5d7-132">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9c5d7-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="9c5d7-133">Remarks</span></span>

<span data-ttu-id="9c5d7-134">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="9c5d7-134">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="9c5d7-135">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="9c5d7-135">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9c5d7-136">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="9c5d7-136">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9c5d7-137">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="9c5d7-137">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9c5d7-138">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9c5d7-138">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c5d7-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9c5d7-139">Requirements</span></span>



| <span data-ttu-id="9c5d7-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c5d7-140">Requirement</span></span> | <span data-ttu-id="9c5d7-141">Valore</span><span class="sxs-lookup"><span data-stu-id="9c5d7-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c5d7-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c5d7-142">Minimum supported client</span></span><br/> | <span data-ttu-id="9c5d7-143">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9c5d7-143">None supported</span></span><br/>                                                                |
| <span data-ttu-id="9c5d7-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9c5d7-144">Minimum supported server</span></span><br/> | <span data-ttu-id="9c5d7-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9c5d7-145">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="9c5d7-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9c5d7-146">Namespace</span></span><br/>                | <span data-ttu-id="9c5d7-147">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="9c5d7-147">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="9c5d7-148">MOF</span><span class="sxs-lookup"><span data-stu-id="9c5d7-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c5d7-149"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9c5d7-149"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="9c5d7-150">DLL</span><span class="sxs-lookup"><span data-stu-id="9c5d7-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c5d7-151"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c5d7-151"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="9c5d7-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9c5d7-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c5d7-153">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="9c5d7-153">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="9c5d7-154">**GetLogEventName**</span><span class="sxs-lookup"><span data-stu-id="9c5d7-154">**GetLogEventName**</span></span>](getlogeventname-win32-tsgatewayserversettings.md)
</dt> </dl>

 


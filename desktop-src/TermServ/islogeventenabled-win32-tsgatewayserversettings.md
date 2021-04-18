---
title: Metodo IsLogEventEnabled della classe Win32_TSGatewayServerSettings
description: Indica se il tipo di registro eventi specificato è abilitato.
ms.assetid: 4abfc56f-871a-44ef-9998-da88949a0a2d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo IsLogEventEnabled
- Metodo IsLogEventEnabled Servizi Desktop remoto, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo IsLogEventEnabled
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.IsLogEventEnabled
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9acefe60a9ba50c49146d25c7bccddf706f198c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301981"
---
# <a name="islogeventenabled-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="749b3-106">Metodo IsLogEventEnabled della \_ classe TSGatewayServerSettings Win32</span><span class="sxs-lookup"><span data-stu-id="749b3-106">IsLogEventEnabled method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="749b3-107">Indica se il tipo di registro eventi specificato è abilitato.</span><span class="sxs-lookup"><span data-stu-id="749b3-107">Indicates whether the specified event log type is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="749b3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="749b3-108">Syntax</span></span>


```mof
uint32 IsLogEventEnabled(
  [in]  string  EventName,
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="749b3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="749b3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="749b3-110">*EventName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="749b3-110">*EventName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="749b3-111">Nome del tipo di registro eventi.</span><span class="sxs-lookup"><span data-stu-id="749b3-111">Name of the event log type.</span></span> <span data-ttu-id="749b3-112">Questo valore deve essere recuperato tramite il metodo [**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="749b3-112">This value should be retrieved by using the [**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md) method.</span></span>

<dt>

<span data-ttu-id="749b3-113">LogChannelDisconnect</span><span class="sxs-lookup"><span data-stu-id="749b3-113">LogChannelDisconnect</span></span>
</dt> <dd>

<span data-ttu-id="749b3-114">L'utente è stato disconnesso dalla risorsa.</span><span class="sxs-lookup"><span data-stu-id="749b3-114">User successfully disconnected from the resource.</span></span>

</dd> <dt>

<span data-ttu-id="749b3-115">LogFailedChannelConnect</span><span class="sxs-lookup"><span data-stu-id="749b3-115">LogFailedChannelConnect</span></span>
</dt> <dd>

<span data-ttu-id="749b3-116">L'utente non è riuscito a connettersi alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="749b3-116">User failed to connect to the resource.</span></span>

</dd> <dt>

<span data-ttu-id="749b3-117">LogFailureNetworkAccessCheck</span><span class="sxs-lookup"><span data-stu-id="749b3-117">LogFailureNetworkAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="749b3-118">Autorizzazione connessione utente non riuscita.</span><span class="sxs-lookup"><span data-stu-id="749b3-118">User failed connection authorization.</span></span>

</dd> <dt>

<span data-ttu-id="749b3-119">LogFailureResourceAccessCheck</span><span class="sxs-lookup"><span data-stu-id="749b3-119">LogFailureResourceAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="749b3-120">Autorizzazione risorse utente non riuscita.</span><span class="sxs-lookup"><span data-stu-id="749b3-120">User failed resource authorization.</span></span>

</dd> <dt>

<span data-ttu-id="749b3-121">LogSuccessChannelConnect</span><span class="sxs-lookup"><span data-stu-id="749b3-121">LogSuccessChannelConnect</span></span>
</dt> <dd>

<span data-ttu-id="749b3-122">L'utente ha eseguito la connessione alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="749b3-122">User successfully connected to the resource.</span></span>

</dd> <dt>

<span data-ttu-id="749b3-123">LogSuccessfulNetworkAccessCheck</span><span class="sxs-lookup"><span data-stu-id="749b3-123">LogSuccessfulNetworkAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="749b3-124">L'utente ha superato l'autorizzazione di connessione.</span><span class="sxs-lookup"><span data-stu-id="749b3-124">User successfully passed connection authorization.</span></span>

</dd> <dt>

<span data-ttu-id="749b3-125">LogSuccessfulResourceAccessCheck</span><span class="sxs-lookup"><span data-stu-id="749b3-125">LogSuccessfulResourceAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="749b3-126">L'utente ha superato l'autorizzazione risorse.</span><span class="sxs-lookup"><span data-stu-id="749b3-126">User successfully passed resource authorization.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="749b3-127">*Abilitato* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="749b3-127">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="749b3-128">Indica se il tipo di registro eventi specificato è abilitato.</span><span class="sxs-lookup"><span data-stu-id="749b3-128">Indicates whether the specified event log type is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="749b3-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="749b3-129">Return value</span></span>

<span data-ttu-id="749b3-130">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="749b3-130">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="749b3-131">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="749b3-131">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="749b3-132">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="749b3-132">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="749b3-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="749b3-133">Remarks</span></span>

<span data-ttu-id="749b3-134">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="749b3-134">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="749b3-135">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="749b3-135">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="749b3-136">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="749b3-136">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="749b3-137">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="749b3-137">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="749b3-138">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="749b3-138">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="749b3-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="749b3-139">Requirements</span></span>



| <span data-ttu-id="749b3-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="749b3-140">Requirement</span></span> | <span data-ttu-id="749b3-141">Valore</span><span class="sxs-lookup"><span data-stu-id="749b3-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="749b3-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="749b3-142">Minimum supported client</span></span><br/> | <span data-ttu-id="749b3-143">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="749b3-143">None supported</span></span><br/>                                                                |
| <span data-ttu-id="749b3-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="749b3-144">Minimum supported server</span></span><br/> | <span data-ttu-id="749b3-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="749b3-145">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="749b3-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="749b3-146">Namespace</span></span><br/>                | <span data-ttu-id="749b3-147">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="749b3-147">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="749b3-148">MOF</span><span class="sxs-lookup"><span data-stu-id="749b3-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="749b3-149"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="749b3-149"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="749b3-150">DLL</span><span class="sxs-lookup"><span data-stu-id="749b3-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="749b3-151"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="749b3-151"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="749b3-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="749b3-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="749b3-153">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="749b3-153">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="749b3-154">**GetLogEventName**</span><span class="sxs-lookup"><span data-stu-id="749b3-154">**GetLogEventName**</span></span>](getlogeventname-win32-tsgatewayserversettings.md)
</dt> </dl>

 


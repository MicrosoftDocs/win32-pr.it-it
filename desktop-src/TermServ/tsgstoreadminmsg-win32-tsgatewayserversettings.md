---
title: Metodo TSGStoreAdminMsg della classe Win32_TSGatewayServerSettings
description: Aggiorna il messaggio amministrativo per il server gateway.
ms.assetid: 84e5b967-12fd-47a7-93e4-2550c15c4491
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo TSGStoreAdminMsg
- Metodo TSGStoreAdminMsg Servizi Desktop remoto, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Servizi Desktop remoto, metodo TSGStoreAdminMsg
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.TSGStoreAdminMsg
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 398a027d28970b28b4a1e7db37b5fbfee06e881e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873921"
---
# <a name="tsgstoreadminmsg-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="40646-106">Metodo TSGStoreAdminMsg della \_ classe TSGatewayServerSettings Win32</span><span class="sxs-lookup"><span data-stu-id="40646-106">TSGStoreAdminMsg method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="40646-107">Aggiorna il messaggio amministrativo per il server gateway.</span><span class="sxs-lookup"><span data-stu-id="40646-107">Updates the administrative message for the gateway server.</span></span>

## <a name="syntax"></a><span data-ttu-id="40646-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="40646-108">Syntax</span></span>


```mof
uint32 TSGStoreAdminMsg(
  [in] string TSGAdmMsg,
  [in] string MsgStartTime,
  [in] string MsgEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="40646-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="40646-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40646-110">*TSGAdmMsg* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40646-110">*TSGAdmMsg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40646-111">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="40646-111">Type: **string**</span></span>

<span data-ttu-id="40646-112">Testo del messaggio amministrativo.</span><span class="sxs-lookup"><span data-stu-id="40646-112">The administrative message text.</span></span>

</dd> <dt>

<span data-ttu-id="40646-113">*MsgStartTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40646-113">*MsgStartTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40646-114">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="40646-114">Type: **string**</span></span>

<span data-ttu-id="40646-115">Ora di inizio del messaggio amministrativo.</span><span class="sxs-lookup"><span data-stu-id="40646-115">The administrative message start time.</span></span>

</dd> <dt>

<span data-ttu-id="40646-116">*MsgEndTime* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40646-116">*MsgEndTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40646-117">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="40646-117">Type: **string**</span></span>

<span data-ttu-id="40646-118">Ora di fine del messaggio amministrativo.</span><span class="sxs-lookup"><span data-stu-id="40646-118">The administrative message end time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40646-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="40646-119">Return value</span></span>

<span data-ttu-id="40646-120">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="40646-120">Type: **uint32**</span></span>

<span data-ttu-id="40646-121">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="40646-121">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="40646-122">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="40646-122">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="40646-123">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="40646-123">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="40646-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="40646-124">Remarks</span></span>

<span data-ttu-id="40646-125">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="40646-125">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="40646-126">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="40646-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="40646-127">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="40646-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="40646-128">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="40646-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="40646-129">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="40646-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="40646-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40646-130">Requirements</span></span>



| <span data-ttu-id="40646-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="40646-131">Requirement</span></span> | <span data-ttu-id="40646-132">Valore</span><span class="sxs-lookup"><span data-stu-id="40646-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="40646-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40646-133">Minimum supported client</span></span><br/> | <span data-ttu-id="40646-134">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="40646-134">None supported</span></span><br/>                                                                |
| <span data-ttu-id="40646-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40646-135">Minimum supported server</span></span><br/> | <span data-ttu-id="40646-136">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="40646-136">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="40646-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="40646-137">Namespace</span></span><br/>                | <span data-ttu-id="40646-138">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="40646-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="40646-139">MOF</span><span class="sxs-lookup"><span data-stu-id="40646-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40646-140"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="40646-140"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="40646-141">DLL</span><span class="sxs-lookup"><span data-stu-id="40646-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40646-142"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40646-142"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="40646-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40646-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40646-144">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="40646-144">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 


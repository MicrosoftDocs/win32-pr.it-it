---
title: Metodo Update della classe Win32_TSGatewayRADIUSServer
description: Aggiorna il server Remote Authentication Dial-In User Service (RADIUS) corrente.
ms.assetid: 38a15768-66eb-40d6-a079-16555f2bf96a
ms.tgt_platform: multiple
keywords:
- Metodo di aggiornamento Servizi Desktop remoto
- Metodo Update Servizi Desktop remoto, classe Win32_TSGatewayRADIUSServer
- Classe Win32_TSGatewayRADIUSServer Servizi Desktop remoto, metodo Update
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer.Update
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be4faf0c87e49a507ac300d7e8b32f218ed006ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740706"
---
# <a name="update-method-of-the-win32_tsgatewayradiusserver-class"></a><span data-ttu-id="0b798-106">Metodo Update della classe Win32 \_ TSGatewayRADIUSServer</span><span class="sxs-lookup"><span data-stu-id="0b798-106">Update method of the Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="0b798-107">Aggiorna il server Remote Authentication Dial-In User Service (RADIUS) corrente.</span><span class="sxs-lookup"><span data-stu-id="0b798-107">Updates the current Remote Authentication Dial-In User Service (RADIUS) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b798-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b798-108">Syntax</span></span>


```mof
uint32 Update(
  [in] string Name,
  [in] string SharedSecret
);
```



## <a name="parameters"></a><span data-ttu-id="0b798-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0b798-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b798-110">*Nome* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b798-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b798-111">Nome del server RADIUS.</span><span class="sxs-lookup"><span data-stu-id="0b798-111">RADIUS server name.</span></span>

</dd> <dt>

<span data-ttu-id="0b798-112">*SharedSecret* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b798-112">*SharedSecret* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b798-113">Segreto condiviso per il server RADIUS.</span><span class="sxs-lookup"><span data-stu-id="0b798-113">Shared secret for the RADIUS server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b798-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0b798-114">Return value</span></span>

<span data-ttu-id="0b798-115">Se il metodo ha esito positivo, restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="0b798-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="0b798-116">Se il metodo ha esito negativo, restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="0b798-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="0b798-117">Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="0b798-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0b798-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b798-118">Remarks</span></span>

<span data-ttu-id="0b798-119">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="0b798-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="0b798-120">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="0b798-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0b798-121">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="0b798-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0b798-122">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="0b798-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0b798-123">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0b798-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b798-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b798-124">Requirements</span></span>



| <span data-ttu-id="0b798-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b798-125">Requirement</span></span> | <span data-ttu-id="0b798-126">Valore</span><span class="sxs-lookup"><span data-stu-id="0b798-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b798-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b798-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0b798-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0b798-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="0b798-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b798-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0b798-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b798-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="0b798-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0b798-131">Namespace</span></span><br/>                | <span data-ttu-id="0b798-132">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0b798-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="0b798-133">MOF</span><span class="sxs-lookup"><span data-stu-id="0b798-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b798-134"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b798-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b798-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0b798-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b798-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b798-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="0b798-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b798-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b798-138">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="0b798-138">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> </dl>

 


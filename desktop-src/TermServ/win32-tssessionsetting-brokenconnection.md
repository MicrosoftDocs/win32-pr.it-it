---
title: Metodo BrokenConnection della classe Win32_TSSessionSetting (Wtsprotocol. h)
description: Imposta la proprietà BrokenConnectionAction, ovvero l'azione eseguita dal server in caso di raggiungimento del limite di tempo della sessione o di interruzione della connessione.
ms.assetid: 2422e314-9e1c-4bed-a958-eedd2daeca66
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo BrokenConnection
- Metodo BrokenConnection Servizi Desktop remoto, classe Win32_TSSessionSetting
- Classe Win32_TSSessionSetting Servizi Desktop remoto, metodo BrokenConnection
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting.BrokenConnection
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a90b3f6bada75812b37df014cedadfb4e7ff2e83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301501"
---
# <a name="brokenconnection-method-of-the-win32_tssessionsetting-class"></a><span data-ttu-id="2fec4-106">Metodo BrokenConnection della \_ classe TSSessionSetting Win32</span><span class="sxs-lookup"><span data-stu-id="2fec4-106">BrokenConnection method of the Win32\_TSSessionSetting class</span></span>

<span data-ttu-id="2fec4-107">Imposta la proprietà **BrokenConnectionAction** , ovvero l'azione eseguita dal server in caso di raggiungimento del limite di tempo della sessione o di interruzione della connessione.</span><span class="sxs-lookup"><span data-stu-id="2fec4-107">Sets the **BrokenConnectionAction** property, which is the action the server takes if the session time-limit is reached or if the connection is broken.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fec4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2fec4-108">Syntax</span></span>


```mof
uint32 BrokenConnection(
  [in] uint32 BrokenConnectionAction
);
```



## <a name="parameters"></a><span data-ttu-id="2fec4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2fec4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fec4-110">*BrokenConnectionAction* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2fec4-110">*BrokenConnectionAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fec4-111">Azione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="2fec4-111">The action to take.</span></span>

<dt>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>

<span data-ttu-id="2fec4-112"><span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Disconnetti** (0)</span><span class="sxs-lookup"><span data-stu-id="2fec4-112"><span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Disconnect** (0)</span></span>


</dt> <dd>

<span data-ttu-id="2fec4-113">L'utente è disconnesso dalla sessione.</span><span class="sxs-lookup"><span data-stu-id="2fec4-113">The user is disconnected from the session.</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="2fec4-114"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Termina** (1)</span><span class="sxs-lookup"><span data-stu-id="2fec4-114"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2fec4-115">La sessione viene eliminata definitivamente dal server.</span><span class="sxs-lookup"><span data-stu-id="2fec4-115">The session is permanently deleted from the server.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fec4-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2fec4-116">Return value</span></span>

<span data-ttu-id="2fec4-117">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="2fec4-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="2fec4-118">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="2fec4-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="2fec4-119">Il metodo restituisce un errore se l'impostazione è sotto Criteri di gruppo controllo.</span><span class="sxs-lookup"><span data-stu-id="2fec4-119">The method returns an error if the setting is under Group Policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fec4-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="2fec4-120">Remarks</span></span>

<span data-ttu-id="2fec4-121">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="2fec4-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2fec4-122">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="2fec4-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2fec4-123">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="2fec4-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2fec4-124">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2fec4-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2fec4-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2fec4-125">Requirements</span></span>



| <span data-ttu-id="2fec4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fec4-126">Requirement</span></span> | <span data-ttu-id="2fec4-127">Valore</span><span class="sxs-lookup"><span data-stu-id="2fec4-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fec4-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2fec4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2fec4-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2fec4-129">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="2fec4-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2fec4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2fec4-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2fec4-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2fec4-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2fec4-132">Namespace</span></span><br/>                | <span data-ttu-id="2fec4-133">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="2fec4-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="2fec4-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2fec4-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fec4-135"><dt>Wtsprotocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fec4-135"><dt>Wtsprotocol.h</dt></span></span> </dl> |
| <span data-ttu-id="2fec4-136">MOF</span><span class="sxs-lookup"><span data-stu-id="2fec4-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2fec4-137"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2fec4-137"><dt>TSCfgWmi.mof</dt></span></span> </dl>  |
| <span data-ttu-id="2fec4-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2fec4-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fec4-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fec4-139"><dt>TSCfgWmi.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2fec4-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2fec4-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fec4-141">**\_TSSessionSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="2fec4-141">**Win32\_TSSessionSetting**</span></span>](win32-tssessionsetting.md)
</dt> </dl>

 


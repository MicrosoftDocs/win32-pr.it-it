---
title: Metodo RemoteControl della classe Win32_TSRemoteControlSetting
description: Il metodo RemoteControl imposta la proprietà LevelOfControl.
ms.assetid: 341f4f8d-17be-4482-834a-b771e041cfec
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RemoteControl
- Metodo RemoteControl Servizi Desktop remoto, classe Win32_TSRemoteControlSetting
- Classe Win32_TSRemoteControlSetting Servizi Desktop remoto, metodo RemoteControl
topic_type:
- apiref
api_name:
- Win32_TSRemoteControlSetting.RemoteControl
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9476269c2f619b7ea46bc6546f106d7ccd2a486e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340632"
---
# <a name="remotecontrol-method-of-the-win32_tsremotecontrolsetting-class"></a><span data-ttu-id="01acd-106">Metodo RemoteControl della \_ classe TSRemoteControlSetting Win32</span><span class="sxs-lookup"><span data-stu-id="01acd-106">RemoteControl method of the Win32\_TSRemoteControlSetting class</span></span>

<span data-ttu-id="01acd-107">Il metodo **RemoteControl** imposta la proprietà **LevelOfControl** .</span><span class="sxs-lookup"><span data-stu-id="01acd-107">The **RemoteControl** method sets the **LevelOfControl** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="01acd-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="01acd-108">Syntax</span></span>


```mof
uint32 RemoteControl(
  [in] uint32 LevelOfControl
);
```



## <a name="parameters"></a><span data-ttu-id="01acd-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="01acd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01acd-110">*LevelOfControl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="01acd-110">*LevelOfControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01acd-111">Nuovo valore per la proprietà **LevelOfControl** , che specifica se la sessione verrà visualizzata solo dall'utente remoto oppure visualizzata e controllata tramite una tastiera e un mouse.</span><span class="sxs-lookup"><span data-stu-id="01acd-111">New value for the **LevelOfControl** property, which specifies whether the session will only be viewed by the remote user, or viewed and controlled through a keyboard and mouse.</span></span> <span data-ttu-id="01acd-112">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="01acd-112">For more information, see the Remarks section.</span></span> <span data-ttu-id="01acd-113">Sono supportati i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="01acd-113">The following values are supported.</span></span>

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="01acd-114"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disabilita** (0)</span><span class="sxs-lookup"><span data-stu-id="01acd-114"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="01acd-115">Il controllo remoto è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="01acd-115">Remote control is disabled.</span></span>

</dd> <dt>

<span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>

<span data-ttu-id="01acd-116"><span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**EnableInputNotify** (1)</span><span class="sxs-lookup"><span data-stu-id="01acd-116"><span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**EnableInputNotify** (1)</span></span>


</dt> <dd>

<span data-ttu-id="01acd-117">L'utente del controllo remoto dispone del controllo completo della sessione dell'utente, con l'autorizzazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="01acd-117">The user of remote control has full control of the user's session, with the user's permission.</span></span>

</dd> <dt>

<span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>

<span data-ttu-id="01acd-118"><span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**EnableInputNoNotify** (2)</span><span class="sxs-lookup"><span data-stu-id="01acd-118"><span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**EnableInputNoNotify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="01acd-119">L'utente del controllo remoto ha il controllo completo della sessione dell'utente. l'autorizzazione dell'utente non è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="01acd-119">The user of remote control has full control of the user's session; the user's permission is not required.</span></span>

</dd> <dt>

<span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>

<span data-ttu-id="01acd-120"><span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**EnableNoInputNotify** (3)</span><span class="sxs-lookup"><span data-stu-id="01acd-120"><span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**EnableNoInputNotify** (3)</span></span>


</dt> <dd>

<span data-ttu-id="01acd-121">L'utente del controllo remoto può visualizzare la sessione in modalità remota con l'autorizzazione dell'utente. l'utente remoto non è in grado di controllare attivamente la sessione.</span><span class="sxs-lookup"><span data-stu-id="01acd-121">The user of remote control can view the session remotely, with the user's permission; the remote user cannot actively control the session.</span></span>

</dd> <dt>

<span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>

<span data-ttu-id="01acd-122"><span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**EnableNoInputNoNotify** (4)</span><span class="sxs-lookup"><span data-stu-id="01acd-122"><span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**EnableNoInputNoNotify** (4)</span></span>


</dt> <dd>

<span data-ttu-id="01acd-123">L'utente del controllo remoto può visualizzare la sessione in modalità remota, ma non controlla attivamente la sessione. l'autorizzazione dell'utente non è obbligatoria.</span><span class="sxs-lookup"><span data-stu-id="01acd-123">The user of remote control can view the session remotely, but not actively control the session; the user's permission is not required.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01acd-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="01acd-124">Return value</span></span>

<span data-ttu-id="01acd-125">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="01acd-125">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="01acd-126">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="01acd-126">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="01acd-127">Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="01acd-127">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="01acd-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="01acd-128">Remarks</span></span>

<span data-ttu-id="01acd-129">Il controllo completo di una sessione significa che l'utente remoto può controllare attivamente la sessione dell'utente con una tastiera e un mouse.</span><span class="sxs-lookup"><span data-stu-id="01acd-129">Full control of a session means that the remote user can actively control the user's session with a keyboard and mouse.</span></span>

<span data-ttu-id="01acd-130">Quando un utente tenta di stabilire una connessione di controllo remoto, il sistema Visualizza un messaggio nel client remoto, richiedendo l'autorizzazione per visualizzare o partecipare attivamente alla sessione remota.</span><span class="sxs-lookup"><span data-stu-id="01acd-130">When a user attempts to establish a remote-control connection, the system displays a message to the remote client, requesting permission to either view or participate actively in the remote session.</span></span>

<span data-ttu-id="01acd-131">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="01acd-131">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="01acd-132">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="01acd-132">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="01acd-133">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="01acd-133">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="01acd-134">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="01acd-134">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="01acd-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="01acd-135">Requirements</span></span>



| <span data-ttu-id="01acd-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="01acd-136">Requirement</span></span> | <span data-ttu-id="01acd-137">Valore</span><span class="sxs-lookup"><span data-stu-id="01acd-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01acd-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01acd-138">Minimum supported client</span></span><br/> | <span data-ttu-id="01acd-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01acd-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="01acd-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="01acd-140">Minimum supported server</span></span><br/> | <span data-ttu-id="01acd-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01acd-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="01acd-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="01acd-142">Namespace</span></span><br/>                | <span data-ttu-id="01acd-143">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="01acd-143">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="01acd-144">MOF</span><span class="sxs-lookup"><span data-stu-id="01acd-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01acd-145"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01acd-145"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="01acd-146">DLL</span><span class="sxs-lookup"><span data-stu-id="01acd-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01acd-147"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01acd-147"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01acd-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="01acd-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01acd-149">**\_TSRemoteControlSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="01acd-149">**Win32\_TSRemoteControlSetting**</span></span>](win32-tsremotecontrolsetting.md)
</dt> </dl>

 


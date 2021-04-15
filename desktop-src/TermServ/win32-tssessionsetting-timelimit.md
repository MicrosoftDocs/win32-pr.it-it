---
title: Metodo di scadenza della classe Win32_TSSessionSetting
description: Imposta il tempo massimo allocato al tipo di limite di sessione specificato.
ms.assetid: 55194197-ffb6-49ae-827a-478ced867ab0
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo di scadenza
- Servizi Desktop remoto del metodo di scadenza, classe Win32_TSSessionSetting
- Classe Win32_TSSessionSetting Servizi Desktop remoto, metodo di scadenza
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting.TimeLimit
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4016c28de50d31338d9bc6ec50ef1497c7a561da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517397"
---
# <a name="timelimit-method-of-the-win32_tssessionsetting-class"></a><span data-ttu-id="1376a-106">Metodo di scadenza della \_ classe Win32 TSSessionSetting</span><span class="sxs-lookup"><span data-stu-id="1376a-106">TimeLimit method of the Win32\_TSSessionSetting class</span></span>

<span data-ttu-id="1376a-107">Imposta il tempo massimo allocato al tipo di limite di sessione specificato.</span><span class="sxs-lookup"><span data-stu-id="1376a-107">Sets the maximum time allocated to the specified session-limit type.</span></span>

## <a name="syntax"></a><span data-ttu-id="1376a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1376a-108">Syntax</span></span>


```mof
uint32 TimeLimit(
  [in] string SessionLimitType,
  [in] uint32 ValueLimit
);
```



## <a name="parameters"></a><span data-ttu-id="1376a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1376a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1376a-110">*SessionLimitType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1376a-110">*SessionLimitType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1376a-111">Specifica il tipo di proprietà del limite di sessione che il metodo sta impostando.</span><span class="sxs-lookup"><span data-stu-id="1376a-111">Specifies the type of session-limit property that the method is setting.</span></span>

<dt>

<span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>

<span data-ttu-id="1376a-112"><span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>**ActiveSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="1376a-112"><span id="ActiveSessionLimit"></span><span id="activesessionlimit"></span><span id="ACTIVESESSIONLIMIT"></span>**ActiveSessionLimit**</span></span>


</dt> <dd>

<span data-ttu-id="1376a-113">Il metodo sta impostando la proprietà **ActiveSessionLimit** .</span><span class="sxs-lookup"><span data-stu-id="1376a-113">The method is setting the **ActiveSessionLimit** property.</span></span>

</dd> <dt>

<span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>

<span data-ttu-id="1376a-114"><span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>**DisconnectedSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="1376a-114"><span id="DisconnectedSessionLimit"></span><span id="disconnectedsessionlimit"></span><span id="DISCONNECTEDSESSIONLIMIT"></span>**DisconnectedSessionLimit**</span></span>


</dt> <dd>

<span data-ttu-id="1376a-115">Il metodo sta impostando la proprietà **DisconnectedSessionLimit** .</span><span class="sxs-lookup"><span data-stu-id="1376a-115">The method is setting the **DisconnectedSessionLimit** property.</span></span>

</dd> <dt>

<span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>

<span data-ttu-id="1376a-116"><span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>**IdleSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="1376a-116"><span id="IdleSessionLimit"></span><span id="idlesessionlimit"></span><span id="IDLESESSIONLIMIT"></span>**IdleSessionLimit**</span></span>


</dt> <dd>

<span data-ttu-id="1376a-117">Il metodo sta impostando la proprietà **IdleSessionLimit** .</span><span class="sxs-lookup"><span data-stu-id="1376a-117">The method is setting the **IdleSessionLimit** property.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1376a-118">*ValueLimit* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1376a-118">*ValueLimit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1376a-119">Il nuovo tempo massimo, in millisecondi, per la proprietà specificata dal parametro *SessionLimitType* .</span><span class="sxs-lookup"><span data-stu-id="1376a-119">The new maximum time, in milliseconds, for the property specified by the *SessionLimitType* parameter.</span></span> <span data-ttu-id="1376a-120">Il valore zero indica che non esiste alcun limite di sessione.</span><span class="sxs-lookup"><span data-stu-id="1376a-120">The value zero indicates that there is no session limit.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1376a-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1376a-121">Return value</span></span>

<span data-ttu-id="1376a-122">Restituisce l'esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="1376a-122">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="1376a-123">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="1376a-123">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="1376a-124">Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="1376a-124">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="1376a-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="1376a-125">Remarks</span></span>

<span data-ttu-id="1376a-126">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="1376a-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1376a-127">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="1376a-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1376a-128">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="1376a-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1376a-129">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1376a-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1376a-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1376a-130">Requirements</span></span>



| <span data-ttu-id="1376a-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="1376a-131">Requirement</span></span> | <span data-ttu-id="1376a-132">Valore</span><span class="sxs-lookup"><span data-stu-id="1376a-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1376a-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1376a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1376a-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1376a-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1376a-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1376a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1376a-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1376a-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1376a-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1376a-137">Namespace</span></span><br/>                | <span data-ttu-id="1376a-138">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="1376a-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="1376a-139">MOF</span><span class="sxs-lookup"><span data-stu-id="1376a-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1376a-140"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1376a-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="1376a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="1376a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1376a-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1376a-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1376a-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1376a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1376a-144">**\_TSSessionSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="1376a-144">**Win32\_TSSessionSetting**</span></span>](win32-tssessionsetting.md)
</dt> </dl>

 


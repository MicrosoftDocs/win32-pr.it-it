---
title: Metodo SetSingleSession della classe Win32_TerminalServiceSetting
description: Il metodo SetSingleSession imposta la proprietà SingleSession per la classe.
ms.assetid: 67ccfa9d-86a5-4501-9d61-c7f1677ec3d5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetSingleSession
- Metodo SetSingleSession Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo SetSingleSession
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetSingleSession
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a6ff702020b7682938b7174c65623eba30076a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302437"
---
# <a name="setsinglesession-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="1ef42-106">Metodo SetSingleSession della \_ classe TerminalServiceSetting Win32</span><span class="sxs-lookup"><span data-stu-id="1ef42-106">SetSingleSession method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="1ef42-107">Il metodo **SetSingleSession** imposta la proprietà **SingleSession** per la classe.</span><span class="sxs-lookup"><span data-stu-id="1ef42-107">The **SetSingleSession** method sets the **SingleSession** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ef42-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ef42-108">Syntax</span></span>


```mof
uint32 SetSingleSession(
  [in] uint32 SingleSession
);
```



## <a name="parameters"></a><span data-ttu-id="1ef42-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1ef42-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ef42-110">*SingleSession* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ef42-110">*SingleSession* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ef42-111">Flag che disabilita o Abilita la proprietà **SingleSession** , che determina se gli utenti sono limitati a una o più sessioni di Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="1ef42-111">Flag disabling or enabling the **SingleSession** property, which determines whether users are limited to one or more Remote Desktop Services sessions.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="1ef42-112"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="1ef42-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="1ef42-113">Disabilitare la proprietà.</span><span class="sxs-lookup"><span data-stu-id="1ef42-113">Disable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="1ef42-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="1ef42-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="1ef42-115">Abilitare la proprietà.</span><span class="sxs-lookup"><span data-stu-id="1ef42-115">Enable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ef42-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1ef42-116">Return value</span></span>

<span data-ttu-id="1ef42-117">Restituisce l'esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="1ef42-117">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="1ef42-118">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="1ef42-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ef42-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="1ef42-119">Remarks</span></span>

<span data-ttu-id="1ef42-120">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="1ef42-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1ef42-121">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="1ef42-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1ef42-122">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="1ef42-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1ef42-123">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1ef42-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1ef42-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ef42-124">Requirements</span></span>



| <span data-ttu-id="1ef42-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ef42-125">Requirement</span></span> | <span data-ttu-id="1ef42-126">Valore</span><span class="sxs-lookup"><span data-stu-id="1ef42-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ef42-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ef42-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1ef42-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1ef42-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1ef42-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ef42-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1ef42-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1ef42-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1ef42-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1ef42-131">Namespace</span></span><br/>                | <span data-ttu-id="1ef42-132">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="1ef42-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="1ef42-133">MOF</span><span class="sxs-lookup"><span data-stu-id="1ef42-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ef42-134"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1ef42-134"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ef42-135">DLL</span><span class="sxs-lookup"><span data-stu-id="1ef42-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ef42-136"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ef42-136"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ef42-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ef42-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ef42-138">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="1ef42-138">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 


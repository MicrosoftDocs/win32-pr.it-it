---
title: Metodo ChangeMode della classe Win32_TerminalServiceSetting
description: Il metodo ChangeMode imposta il tipo di licenza del server di host sessione Desktop remoto (host sessione Desktop remoto) corrente.
ms.assetid: 293483ee-51ce-4cd4-ba13-6c7c02bbdbbf
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ChangeMode
- Metodo ChangeMode Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo ChangeMode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.ChangeMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 880fcab8aa68e49c6b3c00278b90635686de6168
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400568"
---
# <a name="changemode-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="f87d7-106">Metodo ChangeMode della \_ classe TerminalServiceSetting Win32</span><span class="sxs-lookup"><span data-stu-id="f87d7-106">ChangeMode method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="f87d7-107">Il metodo **ChangeMode** imposta il tipo di licenza del server di host sessione Desktop remoto (host sessione Desktop remoto) corrente.</span><span class="sxs-lookup"><span data-stu-id="f87d7-107">The **ChangeMode** method sets the licensing type of the current Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="f87d7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f87d7-108">Syntax</span></span>


```mof
uint32 ChangeMode(
  [in] uint32 LicensingType
);
```



## <a name="parameters"></a><span data-ttu-id="f87d7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f87d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f87d7-110">*LicensingType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f87d7-110">*LicensingType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f87d7-111">Tipo di licenza da impostare in base alla modalità server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="f87d7-111">The licensing type to set based on the RD Session Host server mode.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="f87d7-112"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="f87d7-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="f87d7-113">Server Host sessione Desktop remoto personale.</span><span class="sxs-lookup"><span data-stu-id="f87d7-113">Personal RD Session Host server.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="f87d7-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="f87d7-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="f87d7-115">Desktop remoto per l'amministrazione.</span><span class="sxs-lookup"><span data-stu-id="f87d7-115">Remote desktop for administration.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="f87d7-116"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="f87d7-116"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="f87d7-117">Per dispositivo/per postazione.</span><span class="sxs-lookup"><span data-stu-id="f87d7-117">Per device/per seat.</span></span> <span data-ttu-id="f87d7-118">Valido per i server applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f87d7-118">Valid for application servers.</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="f87d7-119"><span id="4"></span>**4**</span><span class="sxs-lookup"><span data-stu-id="f87d7-119"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="f87d7-120">Per utente.</span><span class="sxs-lookup"><span data-stu-id="f87d7-120">Per User.</span></span> <span data-ttu-id="f87d7-121">Valido per i server applicazioni.</span><span class="sxs-lookup"><span data-stu-id="f87d7-121">Valid for application servers.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f87d7-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f87d7-122">Return value</span></span>

<span data-ttu-id="f87d7-123">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="f87d7-123">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="f87d7-124">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="f87d7-124">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="f87d7-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="f87d7-125">Remarks</span></span>

<span data-ttu-id="f87d7-126">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f87d7-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f87d7-127">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="f87d7-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f87d7-128">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="f87d7-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f87d7-129">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f87d7-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f87d7-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f87d7-130">Requirements</span></span>



| <span data-ttu-id="f87d7-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f87d7-131">Requirement</span></span> | <span data-ttu-id="f87d7-132">Valore</span><span class="sxs-lookup"><span data-stu-id="f87d7-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f87d7-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f87d7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f87d7-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f87d7-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f87d7-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f87d7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f87d7-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f87d7-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f87d7-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f87d7-137">Namespace</span></span><br/>                | <span data-ttu-id="f87d7-138">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f87d7-138">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f87d7-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f87d7-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f87d7-140"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f87d7-140"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f87d7-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f87d7-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f87d7-142"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f87d7-142"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f87d7-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f87d7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f87d7-144">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="f87d7-144">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 


---
title: Metodo SetSessionDirectoryActive della classe Win32_TSSessionDirectory
description: Il metodo SetSessionDirectoryActive imposta la proprietà SessionDirectoryActive.
ms.assetid: b2175d1a-b62f-4bdf-9122-76e85233fba4
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetSessionDirectoryActive
- Metodo SetSessionDirectoryActive Servizi Desktop remoto, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Servizi Desktop remoto, metodo SetSessionDirectoryActive
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryActive
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ca8709028ee90db549c7cdeb053b04dc88b52ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400515"
---
# <a name="setsessiondirectoryactive-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="43fb7-106">Metodo SetSessionDirectoryActive della \_ classe TSSessionDirectory Win32</span><span class="sxs-lookup"><span data-stu-id="43fb7-106">SetSessionDirectoryActive method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="43fb7-107">Il metodo **SetSessionDirectoryActive** imposta la proprietà **SessionDirectoryActive** .</span><span class="sxs-lookup"><span data-stu-id="43fb7-107">The **SetSessionDirectoryActive** method sets the **SessionDirectoryActive** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="43fb7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="43fb7-108">Syntax</span></span>


```mof
uint32 SetSessionDirectoryActive(
  [in] uint32 SessionDirectoryActive
);
```



## <a name="parameters"></a><span data-ttu-id="43fb7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="43fb7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43fb7-110">*SessionDirectoryActive* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43fb7-110">*SessionDirectoryActive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43fb7-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43fb7-111">Type: **uint32**</span></span>

<span data-ttu-id="43fb7-112">Flag che disabilita o Abilita il servizio directory di sessione.</span><span class="sxs-lookup"><span data-stu-id="43fb7-112">Flag disabling or enabling the Session Directory service.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="43fb7-113"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="43fb7-113"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="43fb7-114">Disabilitare il servizio directory di sessione.</span><span class="sxs-lookup"><span data-stu-id="43fb7-114">Disable the Session Directory service.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="43fb7-115"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="43fb7-115"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="43fb7-116">Abilitare il servizio directory di sessione.</span><span class="sxs-lookup"><span data-stu-id="43fb7-116">Enable the Session Directory service.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43fb7-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="43fb7-117">Return value</span></span>

<span data-ttu-id="43fb7-118">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="43fb7-118">Type: **uint32**</span></span>

<span data-ttu-id="43fb7-119">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="43fb7-119">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="43fb7-120">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="43fb7-120">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="43fb7-121">Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="43fb7-121">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="43fb7-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="43fb7-122">Remarks</span></span>

<span data-ttu-id="43fb7-123">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="43fb7-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="43fb7-124">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="43fb7-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="43fb7-125">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="43fb7-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="43fb7-126">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="43fb7-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="43fb7-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43fb7-127">Requirements</span></span>



| <span data-ttu-id="43fb7-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="43fb7-128">Requirement</span></span> | <span data-ttu-id="43fb7-129">Valore</span><span class="sxs-lookup"><span data-stu-id="43fb7-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43fb7-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43fb7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="43fb7-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="43fb7-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="43fb7-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43fb7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="43fb7-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43fb7-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="43fb7-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="43fb7-134">Namespace</span></span><br/>                | <span data-ttu-id="43fb7-135">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="43fb7-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="43fb7-136">MOF</span><span class="sxs-lookup"><span data-stu-id="43fb7-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43fb7-137"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="43fb7-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="43fb7-138">DLL</span><span class="sxs-lookup"><span data-stu-id="43fb7-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43fb7-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43fb7-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43fb7-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43fb7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43fb7-141">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="43fb7-141">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 


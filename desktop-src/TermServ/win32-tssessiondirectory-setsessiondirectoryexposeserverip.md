---
title: Metodo SetSessionDirectoryExposeServerIP della classe Win32_TSSessionDirectory
description: Imposta la proprietà SessionDirectoryExposeServerIP.
ms.assetid: ae9a0c72-0a0a-42a0-a233-13da1efe60ef
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetSessionDirectoryExposeServerIP
- Metodo SetSessionDirectoryExposeServerIP Servizi Desktop remoto, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Servizi Desktop remoto, metodo SetSessionDirectoryExposeServerIP
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetSessionDirectoryExposeServerIP
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc03f175e780d63eed3881b9146116702a30a02a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964074"
---
# <a name="setsessiondirectoryexposeserverip-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="48a77-106">Metodo SetSessionDirectoryExposeServerIP della \_ classe TSSessionDirectory Win32</span><span class="sxs-lookup"><span data-stu-id="48a77-106">SetSessionDirectoryExposeServerIP method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="48a77-107">Imposta la proprietà **SessionDirectoryExposeServerIP** .</span><span class="sxs-lookup"><span data-stu-id="48a77-107">Sets the **SessionDirectoryExposeServerIP** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="48a77-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="48a77-108">Syntax</span></span>


```mof
uint32 SetSessionDirectoryExposeServerIP(
  [in] uint32 SessionDirectoryExposeServerIP
);
```



## <a name="parameters"></a><span data-ttu-id="48a77-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="48a77-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48a77-110">*SessionDirectoryExposeServerIP* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="48a77-110">*SessionDirectoryExposeServerIP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48a77-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48a77-111">Type: **uint32**</span></span>

<span data-ttu-id="48a77-112">Flag che disabilita o Abilita la proprietà **SessionDirectoryExposeServerIP** che consente o nega il recupero dell'indirizzo IP per la directory di sessione.</span><span class="sxs-lookup"><span data-stu-id="48a77-112">Flag disabling or enabling the **SessionDirectoryExposeServerIP** property which allows or denies retrieval of the IP address for the session directory.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="48a77-113"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="48a77-113"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="48a77-114">Disabilitare la proprietà.</span><span class="sxs-lookup"><span data-stu-id="48a77-114">Disable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="48a77-115"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="48a77-115"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="48a77-116">Abilitare la proprietà.</span><span class="sxs-lookup"><span data-stu-id="48a77-116">Enable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48a77-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="48a77-117">Return value</span></span>

<span data-ttu-id="48a77-118">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="48a77-118">Type: **uint32**</span></span>

<span data-ttu-id="48a77-119">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="48a77-119">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="48a77-120">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="48a77-120">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="48a77-121">Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="48a77-121">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="48a77-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="48a77-122">Remarks</span></span>

<span data-ttu-id="48a77-123">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="48a77-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="48a77-124">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="48a77-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="48a77-125">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="48a77-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="48a77-126">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="48a77-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="48a77-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48a77-127">Requirements</span></span>



| <span data-ttu-id="48a77-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="48a77-128">Requirement</span></span> | <span data-ttu-id="48a77-129">Valore</span><span class="sxs-lookup"><span data-stu-id="48a77-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48a77-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48a77-130">Minimum supported client</span></span><br/> | <span data-ttu-id="48a77-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="48a77-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="48a77-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="48a77-132">Minimum supported server</span></span><br/> | <span data-ttu-id="48a77-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48a77-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="48a77-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="48a77-134">Namespace</span></span><br/>                | <span data-ttu-id="48a77-135">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="48a77-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="48a77-136">MOF</span><span class="sxs-lookup"><span data-stu-id="48a77-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48a77-137"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="48a77-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="48a77-138">DLL</span><span class="sxs-lookup"><span data-stu-id="48a77-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48a77-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48a77-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48a77-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="48a77-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48a77-141">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="48a77-141">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 


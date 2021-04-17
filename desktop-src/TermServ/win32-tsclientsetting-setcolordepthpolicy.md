---
title: Metodo SetColorDepthPolicy della classe Win32_TSClientSetting
description: Il metodo SetColorDepthPolicy imposta la proprietà ColorDepthPolicy per la classe.
ms.assetid: 7a8c2b51-5f7a-4188-aae0-0b2d47d043bd
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetColorDepthPolicy
- Metodo SetColorDepthPolicy Servizi Desktop remoto, classe Win32_TSClientSetting
- Classe Win32_TSClientSetting Servizi Desktop remoto, metodo SetColorDepthPolicy
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetColorDepthPolicy
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2d47280ce303e7eeba401e0eb34c7f7fa5a7bec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400563"
---
# <a name="setcolordepthpolicy-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="1c590-106">Metodo SetColorDepthPolicy della \_ classe TSClientSetting Win32</span><span class="sxs-lookup"><span data-stu-id="1c590-106">SetColorDepthPolicy method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="1c590-107">Il metodo **SetColorDepthPolicy** imposta la proprietà **ColorDepthPolicy** per la classe.</span><span class="sxs-lookup"><span data-stu-id="1c590-107">The **SetColorDepthPolicy** method sets the **ColorDepthPolicy** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c590-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c590-108">Syntax</span></span>


```mof
uint32 SetColorDepthPolicy(
  [in] uint32 ColorDepthPolicy
);
```



## <a name="parameters"></a><span data-ttu-id="1c590-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c590-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c590-110">*ColorDepthPolicy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c590-110">*ColorDepthPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c590-111">Flag che disabilita o Abilita la proprietà **SetColorDepthPolicy** , che specifica se eseguire l'override dell'impostazione di colore massima dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1c590-111">Flag disabling or enabling the **SetColorDepthPolicy** property, which specifies whether to override the user's maximum color setting.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="1c590-112"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="1c590-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="1c590-113">Abilitare la proprietà.</span><span class="sxs-lookup"><span data-stu-id="1c590-113">Enable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="1c590-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="1c590-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="1c590-115">Disabilitare la proprietà.</span><span class="sxs-lookup"><span data-stu-id="1c590-115">Disable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c590-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1c590-116">Return value</span></span>

<span data-ttu-id="1c590-117">Restituisce l'esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="1c590-117">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="1c590-118">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="1c590-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="1c590-119">Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="1c590-119">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c590-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c590-120">Remarks</span></span>

<span data-ttu-id="1c590-121">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="1c590-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1c590-122">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="1c590-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1c590-123">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="1c590-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1c590-124">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1c590-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c590-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c590-125">Requirements</span></span>



| <span data-ttu-id="1c590-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c590-126">Requirement</span></span> | <span data-ttu-id="1c590-127">Valore</span><span class="sxs-lookup"><span data-stu-id="1c590-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c590-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c590-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1c590-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c590-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1c590-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c590-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1c590-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c590-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1c590-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1c590-132">Namespace</span></span><br/>                | <span data-ttu-id="1c590-133">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="1c590-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="1c590-134">MOF</span><span class="sxs-lookup"><span data-stu-id="1c590-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c590-135"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c590-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c590-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1c590-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c590-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c590-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c590-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c590-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c590-139">**\_TSClientSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="1c590-139">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 


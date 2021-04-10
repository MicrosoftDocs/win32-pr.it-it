---
title: Metodo SetColorDepth della classe Win32_TSClientSetting
description: Il metodo SetColorDepth imposta la proprietà ColorDepth per la classe.
ms.assetid: 1ab8ac41-cbbf-4077-b91e-692856ccba42
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetColorDepth
- Metodo SetColorDepth Servizi Desktop remoto, classe Win32_TSClientSetting
- Classe Win32_TSClientSetting Servizi Desktop remoto, metodo SetColorDepth
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetColorDepth
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f2b05c6b8ff02b78f48ff45751bdc8e57ef46a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964807"
---
# <a name="setcolordepth-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="4d420-106">Metodo SetColorDepth della \_ classe TSClientSetting Win32</span><span class="sxs-lookup"><span data-stu-id="4d420-106">SetColorDepth method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="4d420-107">Il metodo **SetColorDepth** imposta la proprietà **ColorDepth** per la classe.</span><span class="sxs-lookup"><span data-stu-id="4d420-107">The **SetColorDepth** method sets the **ColorDepth** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d420-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d420-108">Syntax</span></span>


```mof
uint32 SetColorDepth(
  [in] uint32 ColorDepth
);
```



## <a name="parameters"></a><span data-ttu-id="4d420-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4d420-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d420-110">*ColorDepth* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d420-110">*ColorDepth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d420-111">Nuovo valore per la proprietà **ColorDepth** .</span><span class="sxs-lookup"><span data-stu-id="4d420-111">The new value for the **ColorDepth** property.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="4d420-112"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="4d420-112"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="4d420-113">8 bit per pixel</span><span class="sxs-lookup"><span data-stu-id="4d420-113">8 bits per pixel</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="4d420-114"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="4d420-114"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="4d420-115">15 bit per pixel</span><span class="sxs-lookup"><span data-stu-id="4d420-115">15 bits per pixel</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="4d420-116"><span id="3"></span>**3**</span><span class="sxs-lookup"><span data-stu-id="4d420-116"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="4d420-117">16 bit per pixel</span><span class="sxs-lookup"><span data-stu-id="4d420-117">16 bits per pixel</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="4d420-118"><span id="4"></span>**4**</span><span class="sxs-lookup"><span data-stu-id="4d420-118"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="4d420-119">24 bit per pixel</span><span class="sxs-lookup"><span data-stu-id="4d420-119">24 bits per pixel</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="4d420-120"><span id="5"></span>**5**</span><span class="sxs-lookup"><span data-stu-id="4d420-120"><span id="5"></span>**5**</span></span>


</dt> <dd>

<span data-ttu-id="4d420-121">32 bit per pixel</span><span class="sxs-lookup"><span data-stu-id="4d420-121">32 bits per pixel</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d420-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4d420-122">Return value</span></span>

<span data-ttu-id="4d420-123">Restituisce l'esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="4d420-123">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="4d420-124">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="4d420-124">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="4d420-125">Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="4d420-125">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d420-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="4d420-126">Remarks</span></span>

<span data-ttu-id="4d420-127">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="4d420-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4d420-128">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="4d420-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4d420-129">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="4d420-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4d420-130">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="4d420-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d420-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d420-131">Requirements</span></span>



| <span data-ttu-id="4d420-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d420-132">Requirement</span></span> | <span data-ttu-id="4d420-133">Valore</span><span class="sxs-lookup"><span data-stu-id="4d420-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d420-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d420-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4d420-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d420-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4d420-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d420-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4d420-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d420-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4d420-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4d420-138">Namespace</span></span><br/>                | <span data-ttu-id="4d420-139">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="4d420-139">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="4d420-140">MOF</span><span class="sxs-lookup"><span data-stu-id="4d420-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d420-141"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4d420-141"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d420-142">DLL</span><span class="sxs-lookup"><span data-stu-id="4d420-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d420-143"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d420-143"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d420-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d420-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d420-145">**\_TSClientSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="4d420-145">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 


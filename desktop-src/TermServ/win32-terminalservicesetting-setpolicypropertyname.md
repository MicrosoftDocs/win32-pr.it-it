---
title: Metodo SetPolicyPropertyName della classe Win32_TerminalServiceSetting
description: Il metodo SetPolicyPropertyName imposta la proprietà DeleteTempFolders, UseTempFolders o help per la classe.
ms.assetid: 18d9927a-b7db-46c7-90ee-00da6de06202
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetPolicyPropertyName
- Metodo SetPolicyPropertyName Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo SetPolicyPropertyName
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetPolicyPropertyName
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f49732fa916dd3c37539dc35d6cef7a4d920d81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478832"
---
# <a name="setpolicypropertyname-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="601d9-106">Metodo SetPolicyPropertyName della \_ classe TerminalServiceSetting Win32</span><span class="sxs-lookup"><span data-stu-id="601d9-106">SetPolicyPropertyName method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="601d9-107">Il metodo **SetPolicyPropertyName** imposta la proprietà **DeleteTempFolders**, **UseTempFolders** o **Help** per la classe.</span><span class="sxs-lookup"><span data-stu-id="601d9-107">The **SetPolicyPropertyName** method sets the **DeleteTempFolders**, **UseTempFolders** or **Help** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="601d9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="601d9-108">Syntax</span></span>


```mof
uint32 SetPolicyPropertyName(
  [in] string  PropertyName,
  [in] boolean Value
);
```



## <a name="parameters"></a><span data-ttu-id="601d9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="601d9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="601d9-110">*PropertyName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="601d9-110">*PropertyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="601d9-111">Specifica la proprietà dei criteri che il metodo sta impostando.</span><span class="sxs-lookup"><span data-stu-id="601d9-111">Specifies the policy property that the method is setting.</span></span>

<dt>

<span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>

<span data-ttu-id="601d9-112"><span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>**DeleteTempFolders**</span><span class="sxs-lookup"><span data-stu-id="601d9-112"><span id="DeleteTempFolders"></span><span id="deletetempfolders"></span><span id="DELETETEMPFOLDERS"></span>**DeleteTempFolders**</span></span>


</dt> <dd>

<span data-ttu-id="601d9-113">Il metodo sta impostando la proprietà **DeleteTempFolders** .</span><span class="sxs-lookup"><span data-stu-id="601d9-113">The method is setting the **DeleteTempFolders** property.</span></span>

</dd> <dt>

<span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>

<span data-ttu-id="601d9-114"><span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>**UseTempFolders**</span><span class="sxs-lookup"><span data-stu-id="601d9-114"><span id="UseTempFolders"></span><span id="usetempfolders"></span><span id="USETEMPFOLDERS"></span>**UseTempFolders**</span></span>


</dt> <dd>

<span data-ttu-id="601d9-115">Il metodo sta impostando la proprietà **UseTempFolders** .</span><span class="sxs-lookup"><span data-stu-id="601d9-115">The method is setting the **UseTempFolders** property.</span></span>

</dd> <dt>

<span id="Help"></span><span id="help"></span><span id="HELP"></span>

<span data-ttu-id="601d9-116"><span id="Help"></span><span id="help"></span><span id="HELP"></span>**Guida**</span><span class="sxs-lookup"><span data-stu-id="601d9-116"><span id="Help"></span><span id="help"></span><span id="HELP"></span>**Help**</span></span>


</dt> <dd>

<span data-ttu-id="601d9-117">Il metodo sta impostando la proprietà della **Guida** .</span><span class="sxs-lookup"><span data-stu-id="601d9-117">The method is setting the **Help** property.</span></span>

<span data-ttu-id="601d9-118">**Nota** la **Guida** non è supportata  </span><span class="sxs-lookup"><span data-stu-id="601d9-118">**Note**  **Help** is not supported</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="601d9-119">*Valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="601d9-119">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="601d9-120">Valore che indica se abilitare o disabilitare la proprietà specificata dal parametro *PropertyName* .</span><span class="sxs-lookup"><span data-stu-id="601d9-120">Value that indicates whether to enable or disable the property specified by the *PropertyName* parameter.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="601d9-121"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="601d9-121"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="601d9-122">Disabilitare la proprietà.</span><span class="sxs-lookup"><span data-stu-id="601d9-122">Disable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="601d9-123"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="601d9-123"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="601d9-124">Abilitare la proprietà.</span><span class="sxs-lookup"><span data-stu-id="601d9-124">Enable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="601d9-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="601d9-125">Return value</span></span>

<span data-ttu-id="601d9-126">Restituisce l'esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="601d9-126">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="601d9-127">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="601d9-127">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="601d9-128">Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="601d9-128">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="601d9-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="601d9-129">Remarks</span></span>

<span data-ttu-id="601d9-130">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="601d9-130">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="601d9-131">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="601d9-131">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="601d9-132">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="601d9-132">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="601d9-133">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="601d9-133">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="601d9-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="601d9-134">Requirements</span></span>



| <span data-ttu-id="601d9-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="601d9-135">Requirement</span></span> | <span data-ttu-id="601d9-136">Valore</span><span class="sxs-lookup"><span data-stu-id="601d9-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="601d9-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="601d9-137">Minimum supported client</span></span><br/> | <span data-ttu-id="601d9-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="601d9-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="601d9-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="601d9-139">Minimum supported server</span></span><br/> | <span data-ttu-id="601d9-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="601d9-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="601d9-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="601d9-141">Namespace</span></span><br/>                | <span data-ttu-id="601d9-142">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="601d9-142">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="601d9-143">MOF</span><span class="sxs-lookup"><span data-stu-id="601d9-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="601d9-144"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="601d9-144"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="601d9-145">DLL</span><span class="sxs-lookup"><span data-stu-id="601d9-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="601d9-146"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="601d9-146"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="601d9-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="601d9-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="601d9-148">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="601d9-148">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 


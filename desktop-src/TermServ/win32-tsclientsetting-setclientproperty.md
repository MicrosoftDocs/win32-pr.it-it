---
title: Metodo SetClientProperty della classe Win32_TSClientSetting
description: Il metodo SetClientProperty imposta la proprietà LPTPortMapping, COMPortMapping, AudioMapping, ClipboardMapping, DriveMapping o WindowsPrinterMapping per la classe.
ms.assetid: a8ad922f-d768-4708-9a67-c6b00580baed
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetClientProperty
- Metodo SetClientProperty Servizi Desktop remoto, classe Win32_TSClientSetting
- Classe Win32_TSClientSetting Servizi Desktop remoto, metodo SetClientProperty
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetClientProperty
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a89bfdfd7c7f2c4b23f76b50ab671d74541f9dbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301507"
---
# <a name="setclientproperty-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="ca754-106">Metodo SetClientProperty della \_ classe TSClientSetting Win32</span><span class="sxs-lookup"><span data-stu-id="ca754-106">SetClientProperty method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="ca754-107">Il metodo **SetClientProperty** imposta la **Proprietà LPTPortMapping**, **COMPortMapping**, **AudioMapping**, **ClipboardMapping**, **DriveMapping** o **WindowsPrinterMapping** per la classe.</span><span class="sxs-lookup"><span data-stu-id="ca754-107">The **SetClientProperty** method sets the **LPTPortMapping**, **COMPortMapping**, **AudioMapping**, **ClipboardMapping**, **DriveMapping**, or **WindowsPrinterMapping** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca754-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca754-108">Syntax</span></span>


```mof
uint32 SetClientProperty(
  [in] string  PropertyName,
  [in] boolean Value
);
```



## <a name="parameters"></a><span data-ttu-id="ca754-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ca754-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca754-110">*PropertyName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca754-110">*PropertyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca754-111">Specifica la proprietà client che il metodo sta impostando.</span><span class="sxs-lookup"><span data-stu-id="ca754-111">Specifies the client property that the method is setting.</span></span>

<dt>

<span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>

<span data-ttu-id="ca754-112"><span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>**AudioMapping**</span><span class="sxs-lookup"><span data-stu-id="ca754-112"><span id="AudioMapping"></span><span id="audiomapping"></span><span id="AUDIOMAPPING"></span>**AudioMapping**</span></span>


</dt> <dd>

<span data-ttu-id="ca754-113">Il metodo sta impostando la proprietà **AudioMapping** .</span><span class="sxs-lookup"><span data-stu-id="ca754-113">The method is setting the **AudioMapping** property.</span></span>

</dd> <dt>

<span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>

<span data-ttu-id="ca754-114"><span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>**ClipboardMapping**</span><span class="sxs-lookup"><span data-stu-id="ca754-114"><span id="ClipboardMapping"></span><span id="clipboardmapping"></span><span id="CLIPBOARDMAPPING"></span>**ClipboardMapping**</span></span>


</dt> <dd>

<span data-ttu-id="ca754-115">Il metodo sta impostando la proprietà **ClipboardMapping** .</span><span class="sxs-lookup"><span data-stu-id="ca754-115">The method is setting the **ClipboardMapping** property.</span></span>

</dd> <dt>

<span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>

<span data-ttu-id="ca754-116"><span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>**COMPortMapping**</span><span class="sxs-lookup"><span data-stu-id="ca754-116"><span id="COMPortMapping"></span><span id="comportmapping"></span><span id="COMPORTMAPPING"></span>**COMPortMapping**</span></span>


</dt> <dd>

<span data-ttu-id="ca754-117">Il metodo sta impostando la proprietà **COMPortMapping** .</span><span class="sxs-lookup"><span data-stu-id="ca754-117">The method is setting the **COMPortMapping** property.</span></span>

</dd> <dt>

<span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>

<span data-ttu-id="ca754-118"><span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>**DriveMapping**</span><span class="sxs-lookup"><span data-stu-id="ca754-118"><span id="DriveMapping"></span><span id="drivemapping"></span><span id="DRIVEMAPPING"></span>**DriveMapping**</span></span>


</dt> <dd>

<span data-ttu-id="ca754-119">Il metodo sta impostando la proprietà **DriveMapping** .</span><span class="sxs-lookup"><span data-stu-id="ca754-119">The method is setting the **DriveMapping** property.</span></span>

</dd> <dt>

<span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>

<span data-ttu-id="ca754-120"><span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>**LPTPortMapping**</span><span class="sxs-lookup"><span data-stu-id="ca754-120"><span id="LPTPortMapping"></span><span id="lptportmapping"></span><span id="LPTPORTMAPPING"></span>**LPTPortMapping**</span></span>


</dt> <dd>

<span data-ttu-id="ca754-121">Il metodo sta impostando la proprietà **LPTPortMapping** .</span><span class="sxs-lookup"><span data-stu-id="ca754-121">The method is setting the **LPTPortMapping** property.</span></span>

</dd> <dt>

<span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>

<span data-ttu-id="ca754-122"><span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>**PNPRedirection**</span><span class="sxs-lookup"><span data-stu-id="ca754-122"><span id="PNPRedirection"></span><span id="pnpredirection"></span><span id="PNPREDIRECTION"></span>**PNPRedirection**</span></span>


</dt> <dd>

<span data-ttu-id="ca754-123">Il metodo sta impostando la proprietà **PNPRedirection** .</span><span class="sxs-lookup"><span data-stu-id="ca754-123">The method is setting the **PNPRedirection** property.</span></span>

</dd> <dt>

<span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>

<span data-ttu-id="ca754-124"><span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>**WindowsPrinterMapping**</span><span class="sxs-lookup"><span data-stu-id="ca754-124"><span id="WindowsPrinterMapping"></span><span id="windowsprintermapping"></span><span id="WINDOWSPRINTERMAPPING"></span>**WindowsPrinterMapping**</span></span>


</dt> <dd>

<span data-ttu-id="ca754-125">Il metodo sta impostando la proprietà **WindowsPrinterMapping** .</span><span class="sxs-lookup"><span data-stu-id="ca754-125">The method is setting the **WindowsPrinterMapping** property.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="ca754-126">*Valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ca754-126">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca754-127">Valore che indica se abilitare o disabilitare la proprietà specificata dal parametro *PropertyName* .</span><span class="sxs-lookup"><span data-stu-id="ca754-127">Value that indicates whether to enable or disable the property specified by the *PropertyName* parameter.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="ca754-128"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="ca754-128"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="ca754-129">Disabilitare la proprietà.</span><span class="sxs-lookup"><span data-stu-id="ca754-129">Disable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="ca754-130"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="ca754-130"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="ca754-131">Abilitare la proprietà.</span><span class="sxs-lookup"><span data-stu-id="ca754-131">Enable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca754-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ca754-132">Return value</span></span>

<span data-ttu-id="ca754-133">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="ca754-133">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="ca754-134">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="ca754-134">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="ca754-135">Il metodo restituisce un errore se la proprietà client specificata non è sotto il controllo criteri di gruppo o se l'impostazione della proprietà non è idonea per l'override da parte del server.</span><span class="sxs-lookup"><span data-stu-id="ca754-135">The method returns an error if the specified client property is not under group policy control or if the property setting is not eligible for override by the server.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca754-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="ca754-136">Remarks</span></span>

<span data-ttu-id="ca754-137">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ca754-137">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ca754-138">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="ca754-138">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ca754-139">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="ca754-139">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ca754-140">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ca754-140">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca754-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca754-141">Requirements</span></span>



| <span data-ttu-id="ca754-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca754-142">Requirement</span></span> | <span data-ttu-id="ca754-143">Valore</span><span class="sxs-lookup"><span data-stu-id="ca754-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca754-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca754-144">Minimum supported client</span></span><br/> | <span data-ttu-id="ca754-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ca754-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ca754-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca754-146">Minimum supported server</span></span><br/> | <span data-ttu-id="ca754-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ca754-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ca754-148">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ca754-148">Namespace</span></span><br/>                | <span data-ttu-id="ca754-149">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="ca754-149">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="ca754-150">MOF</span><span class="sxs-lookup"><span data-stu-id="ca754-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca754-151"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca754-151"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca754-152">DLL</span><span class="sxs-lookup"><span data-stu-id="ca754-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca754-153"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca754-153"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca754-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca754-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca754-155">**\_TSClientSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="ca754-155">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 


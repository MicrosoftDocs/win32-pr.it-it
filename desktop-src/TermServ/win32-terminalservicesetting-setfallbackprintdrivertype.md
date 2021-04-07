---
title: Metodo SetFallbackPrintDriverType della classe Win32_TerminalServiceSetting
description: Il metodo SetFallbackPrintDriverType imposta la proprietà FallbackPrintDriverType per la classe.
ms.assetid: be738134-199a-41a6-b2f8-cccfa14fa02b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetFallbackPrintDriverType
- Metodo SetFallbackPrintDriverType Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo SetFallbackPrintDriverType
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetFallbackPrintDriverType
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e445fef86970e89d5b0f09abebecd40f49ab7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048686"
---
# <a name="setfallbackprintdrivertype-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="b4006-106">Metodo SetFallbackPrintDriverType della \_ classe TerminalServiceSetting Win32</span><span class="sxs-lookup"><span data-stu-id="b4006-106">SetFallbackPrintDriverType method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="b4006-107">Il metodo **SetFallbackPrintDriverType** imposta la proprietà **FallbackPrintDriverType** per la classe.</span><span class="sxs-lookup"><span data-stu-id="b4006-107">The **SetFallbackPrintDriverType** method sets the **FallbackPrintDriverType** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4006-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b4006-108">Syntax</span></span>


```mof
uint32 SetFallbackPrintDriverType(
  [in] uint32 FallbackPrintDriverType
);
```



## <a name="parameters"></a><span data-ttu-id="b4006-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b4006-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4006-110">*FallbackPrintDriverType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b4006-110">*FallbackPrintDriverType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4006-111">Imposta la proprietà **FallbackPrintDriverType** che consente o nega nuove connessioni di Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="b4006-111">Sets the **FallbackPrintDriverType** property which allows or denies new Remote Desktop Services connections.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="b4006-112"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="b4006-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="b4006-113">Nessun driver di fallback.</span><span class="sxs-lookup"><span data-stu-id="b4006-113">No fallback drivers.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="b4006-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="b4006-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="b4006-115">Migliore ipotesi.</span><span class="sxs-lookup"><span data-stu-id="b4006-115">Best guess.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="b4006-116"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="b4006-116"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="b4006-117">Migliore ipotesi.</span><span class="sxs-lookup"><span data-stu-id="b4006-117">Best guess.</span></span> <span data-ttu-id="b4006-118">Se non viene trovata alcuna corrispondenza, eseguire il fallback a Hewlett-Packard PCL (Printer Control Language).</span><span class="sxs-lookup"><span data-stu-id="b4006-118">If no match is found, fallback to Hewlett-Packard Printer Control Language (PCL).</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="b4006-119"><span id="3"></span>**3**</span><span class="sxs-lookup"><span data-stu-id="b4006-119"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="b4006-120">Migliore ipotesi.</span><span class="sxs-lookup"><span data-stu-id="b4006-120">Best guess.</span></span> <span data-ttu-id="b4006-121">Se non viene trovata alcuna corrispondenza, eseguire il fallback a PostScript (PS).</span><span class="sxs-lookup"><span data-stu-id="b4006-121">If no match is found, fallback to Postscript (PS).</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="b4006-122"><span id="4"></span>**4**</span><span class="sxs-lookup"><span data-stu-id="b4006-122"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="b4006-123">Migliore ipotesi.</span><span class="sxs-lookup"><span data-stu-id="b4006-123">Best guess.</span></span> <span data-ttu-id="b4006-124">Se non viene trovata alcuna corrispondenza, visualizzare i driver PS e PCL.</span><span class="sxs-lookup"><span data-stu-id="b4006-124">If no match is found, show both PS and PCL drivers.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4006-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b4006-125">Return value</span></span>

<span data-ttu-id="b4006-126">Restituisce l'esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="b4006-126">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="b4006-127">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="b4006-127">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="b4006-128">Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="b4006-128">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4006-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="b4006-129">Remarks</span></span>

<span data-ttu-id="b4006-130">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="b4006-130">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b4006-131">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="b4006-131">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b4006-132">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="b4006-132">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b4006-133">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b4006-133">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4006-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4006-134">Requirements</span></span>



| <span data-ttu-id="b4006-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4006-135">Requirement</span></span> | <span data-ttu-id="b4006-136">Valore</span><span class="sxs-lookup"><span data-stu-id="b4006-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4006-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4006-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b4006-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b4006-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b4006-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4006-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b4006-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b4006-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b4006-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b4006-141">Namespace</span></span><br/>                | <span data-ttu-id="b4006-142">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b4006-142">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="b4006-143">MOF</span><span class="sxs-lookup"><span data-stu-id="b4006-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b4006-144"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b4006-144"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b4006-145">DLL</span><span class="sxs-lookup"><span data-stu-id="b4006-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4006-146"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4006-146"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4006-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b4006-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4006-148">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="b4006-148">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 


---
title: Metodo SetProfilePath della classe Win32_TerminalServiceSetting
description: Il metodo SetProfilePath imposta la proprietà propath per la classe.
ms.assetid: a0dfe6a4-929c-45ec-bd31-7e0ffb6ce5de
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetProfilePath
- Metodo SetProfilePath Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo SetProfilePath
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetProfilePath
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 434909471accc191e79c92287ab6e4ac427bf949
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400566"
---
# <a name="setprofilepath-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="09415-106">Metodo SetProfilePath della \_ classe TerminalServiceSetting Win32</span><span class="sxs-lookup"><span data-stu-id="09415-106">SetProfilePath method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="09415-107">Il metodo **SetProfilePath** imposta la proprietà **propath** per la classe.</span><span class="sxs-lookup"><span data-stu-id="09415-107">The **SetProfilePath** method sets the **ProfilePath** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="09415-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="09415-108">Syntax</span></span>


```mof
uint32 SetProfilePath(
  [in] string ProfilePath
);
```



## <a name="parameters"></a><span data-ttu-id="09415-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="09415-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09415-110">*Propath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="09415-110">*ProfilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09415-111">Nuovo valore per la proprietà **filePath** , che specifica il percorso del profilo per il computer.</span><span class="sxs-lookup"><span data-stu-id="09415-111">The new value for the **ProfilePath** property, which specifies the profile path for the computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09415-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="09415-112">Return value</span></span>

<span data-ttu-id="09415-113">Restituisce l'esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="09415-113">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="09415-114">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="09415-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="09415-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="09415-115">Remarks</span></span>

<span data-ttu-id="09415-116">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="09415-116">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="09415-117">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="09415-117">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="09415-118">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="09415-118">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="09415-119">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="09415-119">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="09415-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09415-120">Requirements</span></span>



| <span data-ttu-id="09415-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="09415-121">Requirement</span></span> | <span data-ttu-id="09415-122">Valore</span><span class="sxs-lookup"><span data-stu-id="09415-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="09415-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09415-123">Minimum supported client</span></span><br/> | <span data-ttu-id="09415-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="09415-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="09415-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="09415-125">Minimum supported server</span></span><br/> | <span data-ttu-id="09415-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09415-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="09415-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="09415-127">Namespace</span></span><br/>                | <span data-ttu-id="09415-128">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="09415-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="09415-129">MOF</span><span class="sxs-lookup"><span data-stu-id="09415-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09415-130"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="09415-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="09415-131">DLL</span><span class="sxs-lookup"><span data-stu-id="09415-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09415-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09415-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09415-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09415-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09415-134">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="09415-134">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 


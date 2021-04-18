---
title: Metodo SetAllowDwm della classe Win32_TSClientSetting
description: Imposta la proprietà AllowDwm.
ms.assetid: c70d3dc9-c109-4d77-be50-20a0352282d6
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetAllowDwm
- Metodo SetAllowDwm Servizi Desktop remoto, classe Win32_TSClientSetting
- Classe Win32_TSClientSetting Servizi Desktop remoto, metodo SetAllowDwm
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetAllowDwm
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39441ba3244f206b057ba47c3cb6f765b5e80604
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301518"
---
# <a name="setallowdwm-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="13e08-106">Metodo SetAllowDwm della \_ classe TSClientSetting Win32</span><span class="sxs-lookup"><span data-stu-id="13e08-106">SetAllowDwm method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="13e08-107">Imposta la proprietà **AllowDwm** .</span><span class="sxs-lookup"><span data-stu-id="13e08-107">Sets the **AllowDwm** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="13e08-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13e08-108">Syntax</span></span>


```mof
uint32 SetAllowDwm(
  [in] uint32 AllowDwm
);
```



## <a name="parameters"></a><span data-ttu-id="13e08-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="13e08-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13e08-110">*AllowDwm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13e08-110">*AllowDwm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13e08-111">Nuovo valore della proprietà **AllowDwm** .</span><span class="sxs-lookup"><span data-stu-id="13e08-111">The new **AllowDwm** property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13e08-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="13e08-112">Return value</span></span>

<span data-ttu-id="13e08-113">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="13e08-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="13e08-114">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="13e08-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="13e08-115">Il metodo restituisce un errore se le impostazioni di connessione dell'utente vengono sostituite dal server.</span><span class="sxs-lookup"><span data-stu-id="13e08-115">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="13e08-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13e08-116">Requirements</span></span>



| <span data-ttu-id="13e08-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="13e08-117">Requirement</span></span> | <span data-ttu-id="13e08-118">Valore</span><span class="sxs-lookup"><span data-stu-id="13e08-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13e08-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13e08-119">Minimum supported client</span></span><br/> | <span data-ttu-id="13e08-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="13e08-120">None supported</span></span><br/>                                                               |
| <span data-ttu-id="13e08-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13e08-121">Minimum supported server</span></span><br/> | <span data-ttu-id="13e08-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="13e08-122">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="13e08-123">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="13e08-123">End of client support</span></span><br/>    | <span data-ttu-id="13e08-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="13e08-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="13e08-125">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="13e08-125">End of server support</span></span><br/>    | <span data-ttu-id="13e08-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="13e08-126">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="13e08-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="13e08-127">Namespace</span></span><br/>                | <span data-ttu-id="13e08-128">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="13e08-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="13e08-129">MOF</span><span class="sxs-lookup"><span data-stu-id="13e08-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13e08-130"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13e08-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="13e08-131">DLL</span><span class="sxs-lookup"><span data-stu-id="13e08-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13e08-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13e08-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13e08-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13e08-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13e08-134">**\_TSClientSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="13e08-134">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

 






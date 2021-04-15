---
title: Metodo SetMaxXResolution della classe Win32_TSClientSetting
description: Imposta la proprietà MaxXResolution.
ms.assetid: c1e00bab-ab32-4cf6-8121-950184bd8a01
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetMaxXResolution
- Metodo SetMaxXResolution Servizi Desktop remoto, classe Win32_TSClientSetting
- Classe Win32_TSClientSetting Servizi Desktop remoto, metodo SetMaxXResolution
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxXResolution
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ab911fd66c7cf6b4f657d8f9e060eccee80675
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476414"
---
# <a name="setmaxxresolution-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="cfba1-106">Metodo SetMaxXResolution della \_ classe TSClientSetting Win32</span><span class="sxs-lookup"><span data-stu-id="cfba1-106">SetMaxXResolution method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="cfba1-107">Imposta la proprietà **MaxXResolution** .</span><span class="sxs-lookup"><span data-stu-id="cfba1-107">Sets the **MaxXResolution** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfba1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cfba1-108">Syntax</span></span>


```mof
uint32 SetMaxXResolution(
  [in] uint32 MaxXResolution
);
```



## <a name="parameters"></a><span data-ttu-id="cfba1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="cfba1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfba1-110">*MaxXResolution* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cfba1-110">*MaxXResolution* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfba1-111">Nuova risoluzione X massima supportata dal server.</span><span class="sxs-lookup"><span data-stu-id="cfba1-111">The new maximum X resolution supported by the server.</span></span> <span data-ttu-id="cfba1-112">Il valore minimo è 200 e il valore massimo è 4096.</span><span class="sxs-lookup"><span data-stu-id="cfba1-112">The minimum value is 200 and maximum value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfba1-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cfba1-113">Return value</span></span>

<span data-ttu-id="cfba1-114">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="cfba1-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="cfba1-115">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="cfba1-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="cfba1-116">Il metodo restituisce un errore se le impostazioni di connessione dell'utente vengono sostituite dal server.</span><span class="sxs-lookup"><span data-stu-id="cfba1-116">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfba1-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cfba1-117">Requirements</span></span>



| <span data-ttu-id="cfba1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfba1-118">Requirement</span></span> | <span data-ttu-id="cfba1-119">Valore</span><span class="sxs-lookup"><span data-stu-id="cfba1-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cfba1-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cfba1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cfba1-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="cfba1-121">None supported</span></span><br/>                                                               |
| <span data-ttu-id="cfba1-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cfba1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cfba1-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cfba1-123">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="cfba1-124">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cfba1-124">Namespace</span></span><br/>                | <span data-ttu-id="cfba1-125">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="cfba1-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="cfba1-126">MOF</span><span class="sxs-lookup"><span data-stu-id="cfba1-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cfba1-127"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cfba1-127"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="cfba1-128">DLL</span><span class="sxs-lookup"><span data-stu-id="cfba1-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfba1-129"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfba1-129"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfba1-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cfba1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfba1-131">**\_TSClientSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="cfba1-131">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

 






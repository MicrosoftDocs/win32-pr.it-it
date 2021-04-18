---
title: Metodo SetMaxYResolution della classe Win32_TSClientSetting
description: Imposta la proprietà MaxYResolution.
ms.assetid: a8399c7c-6b3a-464f-8112-8838257ccf06
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetMaxYResolution
- Metodo SetMaxYResolution Servizi Desktop remoto, classe Win32_TSClientSetting
- Classe Win32_TSClientSetting Servizi Desktop remoto, metodo SetMaxYResolution
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxYResolution
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c85564e075865d993552e831869979fc6227af29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301615"
---
# <a name="setmaxyresolution-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="a7fd3-106">Metodo SetMaxYResolution della \_ classe TSClientSetting Win32</span><span class="sxs-lookup"><span data-stu-id="a7fd3-106">SetMaxYResolution method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="a7fd3-107">Imposta la proprietà **MaxYResolution** .</span><span class="sxs-lookup"><span data-stu-id="a7fd3-107">Sets the **MaxYResolution** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7fd3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7fd3-108">Syntax</span></span>


```mof
uint32 SetMaxYResolution(
  [in] uint32 MaxYResolution
);
```



## <a name="parameters"></a><span data-ttu-id="a7fd3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a7fd3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7fd3-110">*MaxYResolution* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7fd3-110">*MaxYResolution* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7fd3-111">Nuova risoluzione Y massima supportata dal server.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-111">The new maximum Y resolution supported by the server.</span></span> <span data-ttu-id="a7fd3-112">Il valore minimo è 200 e il valore massimo è 2048.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-112">The minimum value is 200 and the maximum value is 2048.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7fd3-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a7fd3-113">Return value</span></span>

<span data-ttu-id="a7fd3-114">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="a7fd3-115">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="a7fd3-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="a7fd3-116">Il metodo restituisce un errore se le impostazioni di connessione dell'utente vengono sostituite dal server.</span><span class="sxs-lookup"><span data-stu-id="a7fd3-116">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7fd3-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7fd3-117">Requirements</span></span>



| <span data-ttu-id="a7fd3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7fd3-118">Requirement</span></span> | <span data-ttu-id="a7fd3-119">Valore</span><span class="sxs-lookup"><span data-stu-id="a7fd3-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7fd3-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7fd3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a7fd3-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a7fd3-121">None supported</span></span><br/>                                                               |
| <span data-ttu-id="a7fd3-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7fd3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a7fd3-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a7fd3-123">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="a7fd3-124">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a7fd3-124">Namespace</span></span><br/>                | <span data-ttu-id="a7fd3-125">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="a7fd3-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a7fd3-126">MOF</span><span class="sxs-lookup"><span data-stu-id="a7fd3-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a7fd3-127"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a7fd3-127"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a7fd3-128">DLL</span><span class="sxs-lookup"><span data-stu-id="a7fd3-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7fd3-129"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7fd3-129"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7fd3-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7fd3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7fd3-131">**\_TSClientSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="a7fd3-131">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

 






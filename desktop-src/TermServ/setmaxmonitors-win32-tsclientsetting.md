---
title: Metodo SetMaxMonitors della classe Win32_TSClientSetting
description: Imposta la proprietà MaxMonitors.
ms.assetid: 1c8266e1-ff2b-4fbc-af70-6f7b4499d88c
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetMaxMonitors
- Metodo SetMaxMonitors Servizi Desktop remoto, classe Win32_TSClientSetting
- Classe Win32_TSClientSetting Servizi Desktop remoto, metodo SetMaxMonitors
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxMonitors
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76cdbe29079f5006cbf596751bef73cda1e94e52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301857"
---
# <a name="setmaxmonitors-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="d37d4-106">Metodo SetMaxMonitors della \_ classe TSClientSetting Win32</span><span class="sxs-lookup"><span data-stu-id="d37d4-106">SetMaxMonitors method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="d37d4-107">Imposta la proprietà **MaxMonitors** .</span><span class="sxs-lookup"><span data-stu-id="d37d4-107">Sets the **MaxMonitors** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="d37d4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d37d4-108">Syntax</span></span>


```mof
uint32 SetMaxMonitors(
  [in] uint32 MaxMonitors
);
```



## <a name="parameters"></a><span data-ttu-id="d37d4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d37d4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d37d4-110">*MaxMonitors* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d37d4-110">*MaxMonitors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d37d4-111">Specifica il nuovo numero massimo di monitoraggi supportati dal server.</span><span class="sxs-lookup"><span data-stu-id="d37d4-111">Specifies the new maximum number of monitors supported by the server.</span></span> <span data-ttu-id="d37d4-112">Il valore minimo è 1 e il valore massimo è 10.</span><span class="sxs-lookup"><span data-stu-id="d37d4-112">The minimum value is 1 and the maximum value is 10.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d37d4-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d37d4-113">Return value</span></span>

<span data-ttu-id="d37d4-114">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="d37d4-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="d37d4-115">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="d37d4-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="d37d4-116">Il metodo restituisce un errore se le impostazioni di connessione dell'utente vengono sostituite dal server.</span><span class="sxs-lookup"><span data-stu-id="d37d4-116">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="d37d4-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d37d4-117">Requirements</span></span>



| <span data-ttu-id="d37d4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d37d4-118">Requirement</span></span> | <span data-ttu-id="d37d4-119">Valore</span><span class="sxs-lookup"><span data-stu-id="d37d4-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d37d4-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d37d4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d37d4-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d37d4-121">None supported</span></span><br/>                                                               |
| <span data-ttu-id="d37d4-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d37d4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d37d4-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d37d4-123">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="d37d4-124">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d37d4-124">Namespace</span></span><br/>                | <span data-ttu-id="d37d4-125">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="d37d4-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d37d4-126">MOF</span><span class="sxs-lookup"><span data-stu-id="d37d4-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d37d4-127"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d37d4-127"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d37d4-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d37d4-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d37d4-129"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d37d4-129"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d37d4-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d37d4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d37d4-131">**\_TSClientSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="d37d4-131">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

 






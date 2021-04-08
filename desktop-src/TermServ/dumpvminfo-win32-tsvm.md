---
title: Metodo DumpVmInfo della classe Win32_TSVm
description: Questo membro è a scopo di test interno e non deve essere utilizzato nel codice.
ms.assetid: 40cb4fdc-f657-47c6-8daa-684a12be30e4
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo DumpVmInfo
- Metodo DumpVmInfo Servizi Desktop remoto, classe Win32_TSVm
- Classe Win32_TSVm Servizi Desktop remoto, metodo DumpVmInfo
topic_type:
- apiref
api_name:
- Win32_TSVm.DumpVmInfo
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a2d02a1d4ea07bd045da2850a4d7ccb0069977a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743847"
---
# <a name="dumpvminfo-method-of-the-win32_tsvm-class"></a><span data-ttu-id="0b7b7-106">Metodo DumpVmInfo della \_ classe TSVm Win32</span><span class="sxs-lookup"><span data-stu-id="0b7b7-106">DumpVmInfo method of the Win32\_TSVm class</span></span>

<span data-ttu-id="0b7b7-107">Questo membro è a scopo di test interno e non deve essere utilizzato nel codice.</span><span class="sxs-lookup"><span data-stu-id="0b7b7-107">This member is for internal testing purposes, and should not be used in your code.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b7b7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b7b7-108">Syntax</span></span>


```mof
uint32 DumpVmInfo();
```



## <a name="parameters"></a><span data-ttu-id="0b7b7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0b7b7-109">Parameters</span></span>

<span data-ttu-id="0b7b7-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="0b7b7-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0b7b7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0b7b7-111">Return value</span></span>

<span data-ttu-id="0b7b7-112">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="0b7b7-112">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="0b7b7-113">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="0b7b7-113">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b7b7-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b7b7-114">Requirements</span></span>



| <span data-ttu-id="0b7b7-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b7b7-115">Requirement</span></span> | <span data-ttu-id="0b7b7-116">Valore</span><span class="sxs-lookup"><span data-stu-id="0b7b7-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b7b7-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b7b7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0b7b7-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0b7b7-118">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="0b7b7-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b7b7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0b7b7-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0b7b7-120">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="0b7b7-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0b7b7-121">Namespace</span></span><br/>                | <span data-ttu-id="0b7b7-122">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0b7b7-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="0b7b7-123">MOF</span><span class="sxs-lookup"><span data-stu-id="0b7b7-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b7b7-124"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b7b7-124"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="0b7b7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0b7b7-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b7b7-126"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b7b7-126"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b7b7-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b7b7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b7b7-128">**\_TSVm Win32**</span><span class="sxs-lookup"><span data-stu-id="0b7b7-128">**Win32\_TSVm**</span></span>](win32-tsvm.md)
</dt> </dl>

 

 






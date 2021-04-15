---
title: Metodo EmptySpecifiedLicenseServerList della classe Win32_TerminalServiceSetting
description: Rimuove tutti i server licenze dall'elenco dei server licenze specificati.
ms.assetid: de1633ca-3f0b-4540-8b45-44303a4e72fe
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo EmptySpecifiedLicenseServerList
- Metodo EmptySpecifiedLicenseServerList Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo EmptySpecifiedLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.EmptySpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1392c05618860f742a13140167e423b312e49b0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479319"
---
# <a name="emptyspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="47748-106">Metodo EmptySpecifiedLicenseServerList della \_ classe TerminalServiceSetting Win32</span><span class="sxs-lookup"><span data-stu-id="47748-106">EmptySpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="47748-107">Rimuove tutti i server licenze dall'elenco dei server licenze specificati.</span><span class="sxs-lookup"><span data-stu-id="47748-107">Removes all license servers from the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="47748-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="47748-108">Syntax</span></span>


```mof
uint32 EmptySpecifiedLicenseServerList();
```



## <a name="parameters"></a><span data-ttu-id="47748-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="47748-109">Parameters</span></span>

<span data-ttu-id="47748-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="47748-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="47748-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="47748-111">Return value</span></span>

<span data-ttu-id="47748-112">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="47748-112">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="47748-113">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="47748-113">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="47748-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="47748-114">Requirements</span></span>



| <span data-ttu-id="47748-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="47748-115">Requirement</span></span> | <span data-ttu-id="47748-116">Valore</span><span class="sxs-lookup"><span data-stu-id="47748-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47748-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="47748-117">Minimum supported client</span></span><br/> | <span data-ttu-id="47748-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="47748-118">None supported</span></span><br/>                                                               |
| <span data-ttu-id="47748-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="47748-119">Minimum supported server</span></span><br/> | <span data-ttu-id="47748-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="47748-120">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="47748-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="47748-121">Namespace</span></span><br/>                | <span data-ttu-id="47748-122">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="47748-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="47748-123">MOF</span><span class="sxs-lookup"><span data-stu-id="47748-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47748-124"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="47748-124"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="47748-125">DLL</span><span class="sxs-lookup"><span data-stu-id="47748-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47748-126"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47748-126"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47748-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="47748-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47748-128">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="47748-128">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="47748-129">**AddLSToSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="47748-129">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="47748-130">**GetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="47748-130">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="47748-131">**RemoveLSFromSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="47748-131">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="47748-132">**SetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="47748-132">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 






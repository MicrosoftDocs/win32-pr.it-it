---
title: Metodo RemoveLSFromSpecifiedLicenseServerList della classe Win32_TerminalServiceSetting
description: Rimuove il server licenze specificato dall'elenco dei server licenze specificati.
ms.assetid: c25eebf9-3a21-41a0-bb7d-c3f909cd8087
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RemoveLSFromSpecifiedLicenseServerList
- Metodo RemoveLSFromSpecifiedLicenseServerList Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo RemoveLSFromSpecifiedLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.RemoveLSFromSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 901c2676748e819290855df2de51e5d7936dc793
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873813"
---
# <a name="removelsfromspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="c8a6d-106">Metodo RemoveLSFromSpecifiedLicenseServerList della \_ classe TerminalServiceSetting Win32</span><span class="sxs-lookup"><span data-stu-id="c8a6d-106">RemoveLSFromSpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="c8a6d-107">Rimuove il server licenze specificato dall'elenco dei server licenze specificati.</span><span class="sxs-lookup"><span data-stu-id="c8a6d-107">Removes the given license server from the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8a6d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c8a6d-108">Syntax</span></span>


```mof
uint32 RemoveLSFromSpecifiedLicenseServerList(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a><span data-ttu-id="c8a6d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c8a6d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8a6d-110">*LicenseServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c8a6d-110">*LicenseServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8a6d-111">Nome del server licenze da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="c8a6d-111">The name of the license server to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8a6d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c8a6d-112">Return value</span></span>

<span data-ttu-id="c8a6d-113">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="c8a6d-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="c8a6d-114">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="c8a6d-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8a6d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8a6d-115">Requirements</span></span>



| <span data-ttu-id="c8a6d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8a6d-116">Requirement</span></span> | <span data-ttu-id="c8a6d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c8a6d-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8a6d-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8a6d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c8a6d-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c8a6d-119">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c8a6d-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8a6d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c8a6d-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c8a6d-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="c8a6d-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c8a6d-122">Namespace</span></span><br/>                | <span data-ttu-id="c8a6d-123">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="c8a6d-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c8a6d-124">MOF</span><span class="sxs-lookup"><span data-stu-id="c8a6d-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8a6d-125"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8a6d-125"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c8a6d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c8a6d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8a6d-127"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8a6d-127"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8a6d-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8a6d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8a6d-129">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="c8a6d-129">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="c8a6d-130">**AddLSToSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="c8a6d-130">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="c8a6d-131">**EmptySpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="c8a6d-131">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="c8a6d-132">**GetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="c8a6d-132">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="c8a6d-133">**SetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="c8a6d-133">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 






---
title: Metodo AddLSToSpecifiedLicenseServerList della classe Win32_TerminalServiceSetting
description: Aggiunge il server licenze specificato alla fine dell'elenco dei server licenze specificati.
ms.assetid: 2aebe7c0-5ec2-4c2d-9887-7ecd2d6ec02a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo AddLSToSpecifiedLicenseServerList
- Metodo AddLSToSpecifiedLicenseServerList Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo AddLSToSpecifiedLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.AddLSToSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c53a5279523405b760addabb03e381507775e6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963975"
---
# <a name="addlstospecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="85828-106">Metodo AddLSToSpecifiedLicenseServerList della \_ classe TerminalServiceSetting Win32</span><span class="sxs-lookup"><span data-stu-id="85828-106">AddLSToSpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="85828-107">Aggiunge il server licenze specificato alla fine dell'elenco dei server licenze specificati.</span><span class="sxs-lookup"><span data-stu-id="85828-107">Adds the given license server to the end of the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="85828-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="85828-108">Syntax</span></span>


```mof
uint32 AddLSToSpecifiedLicenseServerList(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a><span data-ttu-id="85828-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="85828-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85828-110">*LicenseServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85828-110">*LicenseServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85828-111">Nome del server licenze da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="85828-111">The name of the license server to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85828-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="85828-112">Return value</span></span>

<span data-ttu-id="85828-113">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="85828-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="85828-114">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="85828-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="85828-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85828-115">Requirements</span></span>



| <span data-ttu-id="85828-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="85828-116">Requirement</span></span> | <span data-ttu-id="85828-117">Valore</span><span class="sxs-lookup"><span data-stu-id="85828-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="85828-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85828-118">Minimum supported client</span></span><br/> | <span data-ttu-id="85828-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="85828-119">None supported</span></span><br/>                                                               |
| <span data-ttu-id="85828-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85828-120">Minimum supported server</span></span><br/> | <span data-ttu-id="85828-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="85828-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="85828-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="85828-122">Namespace</span></span><br/>                | <span data-ttu-id="85828-123">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="85828-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="85828-124">MOF</span><span class="sxs-lookup"><span data-stu-id="85828-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85828-125"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="85828-125"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="85828-126">DLL</span><span class="sxs-lookup"><span data-stu-id="85828-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85828-127"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85828-127"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85828-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="85828-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85828-129">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="85828-129">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="85828-130">**EmptySpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="85828-130">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="85828-131">**GetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="85828-131">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="85828-132">**RemoveLSFromSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="85828-132">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="85828-133">**SetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="85828-133">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 






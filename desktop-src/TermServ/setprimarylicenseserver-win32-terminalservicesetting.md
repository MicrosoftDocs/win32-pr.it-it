---
title: Metodo SetPrimaryLicenseServer della classe Win32_TerminalServiceSetting
description: Imposta il server licenze specificato come prima voce nell'elenco dei server licenze specificati.
ms.assetid: 8921e861-3b9a-49c5-a691-ded7be18ca0a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetPrimaryLicenseServer
- Metodo SetPrimaryLicenseServer Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo SetPrimaryLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetPrimaryLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61d73212230d1ca69e0a0809c48b8f2985920045
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873481"
---
# <a name="setprimarylicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="7c9ba-106">Metodo SetPrimaryLicenseServer della \_ classe TerminalServiceSetting Win32</span><span class="sxs-lookup"><span data-stu-id="7c9ba-106">SetPrimaryLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="7c9ba-107">Imposta il server licenze specificato come prima voce nell'elenco dei server licenze specificati.</span><span class="sxs-lookup"><span data-stu-id="7c9ba-107">Sets the given license server as the first entry in the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c9ba-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7c9ba-108">Syntax</span></span>


```mof
uint32 SetPrimaryLicenseServer(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a><span data-ttu-id="7c9ba-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c9ba-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c9ba-110">*LicenseServerName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c9ba-110">*LicenseServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c9ba-111">Nome del server licenze.</span><span class="sxs-lookup"><span data-stu-id="7c9ba-111">The name of the license server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c9ba-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c9ba-112">Return value</span></span>

<span data-ttu-id="7c9ba-113">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="7c9ba-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="7c9ba-114">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="7c9ba-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c9ba-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c9ba-115">Requirements</span></span>



| <span data-ttu-id="7c9ba-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c9ba-116">Requirement</span></span> | <span data-ttu-id="7c9ba-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7c9ba-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c9ba-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c9ba-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7c9ba-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7c9ba-119">None supported</span></span><br/>                                                               |
| <span data-ttu-id="7c9ba-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c9ba-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7c9ba-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7c9ba-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="7c9ba-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7c9ba-122">Namespace</span></span><br/>                | <span data-ttu-id="7c9ba-123">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="7c9ba-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="7c9ba-124">MOF</span><span class="sxs-lookup"><span data-stu-id="7c9ba-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c9ba-125"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7c9ba-125"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="7c9ba-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7c9ba-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c9ba-127"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c9ba-127"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c9ba-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c9ba-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c9ba-129">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="7c9ba-129">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 






---
title: Metodo GetRegisteredLicenseServerList della classe Win32_TerminalServiceSetting
description: Ottiene l'elenco dei server licenze registrati.
ms.assetid: 32e06b4b-652f-4977-be1f-6d52983d2605
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetRegisteredLicenseServerList
- Metodo GetRegisteredLicenseServerList Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo GetRegisteredLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetRegisteredLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5336910956a0d281fbfc8fbc65e1d3b8d5018cb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302472"
---
# <a name="getregisteredlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="2e3bc-106">Metodo GetRegisteredLicenseServerList della \_ classe TerminalServiceSetting Win32</span><span class="sxs-lookup"><span data-stu-id="2e3bc-106">GetRegisteredLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="2e3bc-107">Ottiene l'elenco dei server licenze registrati.</span><span class="sxs-lookup"><span data-stu-id="2e3bc-107">Gets the list of registered license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e3bc-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e3bc-108">Syntax</span></span>


```mof
uint32 GetRegisteredLicenseServerList(
  [out] string RegisteredLSList[]
);
```



## <a name="parameters"></a><span data-ttu-id="2e3bc-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2e3bc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e3bc-110">*RegisteredLSList* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2e3bc-110">*RegisteredLSList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e3bc-111">Matrice di stringhe che riceve l'elenco dei server licenze registrati.</span><span class="sxs-lookup"><span data-stu-id="2e3bc-111">A string array that receives the list of registered license servers.</span></span> <span data-ttu-id="2e3bc-112">Se non è presente alcun server licenze registrato, questa matrice sarà vuota.</span><span class="sxs-lookup"><span data-stu-id="2e3bc-112">If there are no registered license servers, this array will be empty.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e3bc-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2e3bc-113">Return value</span></span>

<span data-ttu-id="2e3bc-114">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="2e3bc-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="2e3bc-115">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="2e3bc-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e3bc-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e3bc-116">Requirements</span></span>



| <span data-ttu-id="2e3bc-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e3bc-117">Requirement</span></span> | <span data-ttu-id="2e3bc-118">Valore</span><span class="sxs-lookup"><span data-stu-id="2e3bc-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e3bc-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e3bc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2e3bc-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2e3bc-120">None supported</span></span><br/>                                                               |
| <span data-ttu-id="2e3bc-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2e3bc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2e3bc-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2e3bc-122">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="2e3bc-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2e3bc-123">Namespace</span></span><br/>                | <span data-ttu-id="2e3bc-124">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="2e3bc-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="2e3bc-125">MOF</span><span class="sxs-lookup"><span data-stu-id="2e3bc-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e3bc-126"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e3bc-126"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e3bc-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2e3bc-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e3bc-128"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e3bc-128"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e3bc-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e3bc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e3bc-130">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="2e3bc-130">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 






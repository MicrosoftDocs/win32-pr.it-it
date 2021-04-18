---
title: Metodo SetSpecifiedLicenseServerList della classe Win32_TerminalServiceSetting
description: Aggiorna l'elenco dei server licenze specificati, sostituendo i server licenze esistenti specificati.
ms.assetid: afd7ca11-9db5-4cf3-9706-3c6984789ecd
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetSpecifiedLicenseServerList
- Metodo SetSpecifiedLicenseServerList Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo SetSpecifiedLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d10fde34e490f26c287e63dcddae3c62761670bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301971"
---
# <a name="setspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="ded68-106">Metodo SetSpecifiedLicenseServerList della \_ classe TerminalServiceSetting Win32</span><span class="sxs-lookup"><span data-stu-id="ded68-106">SetSpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="ded68-107">Aggiorna l'elenco dei server licenze specificati, sostituendo i server licenze esistenti specificati.</span><span class="sxs-lookup"><span data-stu-id="ded68-107">Updates the list of specified license servers, replacing any existing specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="ded68-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ded68-108">Syntax</span></span>


```mof
uint32 SetSpecifiedLicenseServerList(
  [in] string SpecifiedLSList[]
);
```



## <a name="parameters"></a><span data-ttu-id="ded68-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ded68-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ded68-110">*SpecifiedLSList* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ded68-110">*SpecifiedLSList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ded68-111">Matrice di stringhe che contiene il nuovo elenco di server licenze specificati.</span><span class="sxs-lookup"><span data-stu-id="ded68-111">A string array that contains the new list of specified license servers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ded68-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ded68-112">Return value</span></span>

<span data-ttu-id="ded68-113">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="ded68-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="ded68-114">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="ded68-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="ded68-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ded68-115">Requirements</span></span>



| <span data-ttu-id="ded68-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ded68-116">Requirement</span></span> | <span data-ttu-id="ded68-117">Valore</span><span class="sxs-lookup"><span data-stu-id="ded68-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ded68-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ded68-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ded68-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ded68-119">None supported</span></span><br/>                                                               |
| <span data-ttu-id="ded68-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ded68-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ded68-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ded68-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="ded68-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ded68-122">Namespace</span></span><br/>                | <span data-ttu-id="ded68-123">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="ded68-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="ded68-124">MOF</span><span class="sxs-lookup"><span data-stu-id="ded68-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ded68-125"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ded68-125"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="ded68-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ded68-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ded68-127"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ded68-127"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ded68-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ded68-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ded68-129">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="ded68-129">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="ded68-130">**AddLSToSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="ded68-130">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="ded68-131">**GetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="ded68-131">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="ded68-132">**EmptySpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="ded68-132">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="ded68-133">**RemoveLSFromSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="ded68-133">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 






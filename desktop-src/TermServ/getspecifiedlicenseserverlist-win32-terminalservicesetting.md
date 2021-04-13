---
title: Metodo GetSpecifiedLicenseServerList della classe Win32_TerminalServiceSetting
description: Recupera l'elenco dei server licenze specificati.
ms.assetid: 800be0ce-1002-48e1-be4e-88db22590f12
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetSpecifiedLicenseServerList
- Metodo GetSpecifiedLicenseServerList Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo GetSpecifiedLicenseServerList
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f70c50281cad7072d420082db0e6916a631e2b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400319"
---
# <a name="getspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="d6d21-106">Metodo GetSpecifiedLicenseServerList della \_ classe TerminalServiceSetting Win32</span><span class="sxs-lookup"><span data-stu-id="d6d21-106">GetSpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="d6d21-107">Recupera l'elenco dei server licenze specificati.</span><span class="sxs-lookup"><span data-stu-id="d6d21-107">Retrieves the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6d21-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d6d21-108">Syntax</span></span>


```mof
uint32 GetSpecifiedLicenseServerList(
  [out] string SpecifiedLSList[]
);
```



## <a name="parameters"></a><span data-ttu-id="d6d21-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d6d21-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6d21-110">*SpecifiedLSList* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d6d21-110">*SpecifiedLSList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6d21-111">Matrice di stringhe che riceve l'elenco dei server licenze.</span><span class="sxs-lookup"><span data-stu-id="d6d21-111">A string array that receives the list of license servers.</span></span> <span data-ttu-id="d6d21-112">Se non sono presenti server licenze, questa matrice sarà vuota.</span><span class="sxs-lookup"><span data-stu-id="d6d21-112">If there are no license servers, this array will be empty.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6d21-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d6d21-113">Return value</span></span>

<span data-ttu-id="d6d21-114">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="d6d21-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="d6d21-115">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="d6d21-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6d21-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d6d21-116">Requirements</span></span>



| <span data-ttu-id="d6d21-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6d21-117">Requirement</span></span> | <span data-ttu-id="d6d21-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d6d21-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6d21-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6d21-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d6d21-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d6d21-120">None supported</span></span><br/>                                                               |
| <span data-ttu-id="d6d21-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6d21-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d6d21-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d6d21-122">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="d6d21-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d6d21-123">Namespace</span></span><br/>                | <span data-ttu-id="d6d21-124">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="d6d21-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d6d21-125">MOF</span><span class="sxs-lookup"><span data-stu-id="d6d21-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6d21-126"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d6d21-126"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d6d21-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d6d21-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6d21-128"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6d21-128"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6d21-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d6d21-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6d21-130">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="d6d21-130">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="d6d21-131">**AddLSToSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="d6d21-131">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="d6d21-132">**EmptySpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="d6d21-132">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="d6d21-133">**RemoveLSFromSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="d6d21-133">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="d6d21-134">**SetSpecifiedLicenseServerList**</span><span class="sxs-lookup"><span data-stu-id="d6d21-134">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 






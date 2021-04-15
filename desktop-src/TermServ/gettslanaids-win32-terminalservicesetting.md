---
title: Metodo GetTSLanaIds della classe Win32_TerminalServiceSetting
description: Ottiene gli ID della scheda di rete locale NetBIOS (LANA) e le descrizioni delle schede di rete Servizi Desktop remoto.
ms.assetid: 3f42e5da-c52b-4500-8cd0-52088dca544a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetTSLanaIds
- Metodo GetTSLanaIds Servizi Desktop remoto, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Servizi Desktop remoto, metodo GetTSLanaIds
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetTSLanaIds
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a66d2b2357df7e6d7ccc2cb8a774ba34c50cb46
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479307"
---
# <a name="gettslanaids-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="bab42-106">Metodo GetTSLanaIds della \_ classe TerminalServiceSetting Win32</span><span class="sxs-lookup"><span data-stu-id="bab42-106">GetTSLanaIds method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="bab42-107">Il metodo **GetTSLanaIds** ottiene gli ID della scheda di rete locale (lana) NetBIOS e le descrizioni delle schede di rete Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="bab42-107">The **GetTSLanaIds** method gets the NetBIOS Local Area Network Adapter (LANA) IDs and descriptions of Remote Desktop Services network adapters.</span></span>

## <a name="syntax"></a><span data-ttu-id="bab42-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bab42-108">Syntax</span></span>


```mof
uint32 GetTSLanaIds(
  [out] uint32 LanaIdList[],
  [out] string LanaIdDescriptions[]
);
```



## <a name="parameters"></a><span data-ttu-id="bab42-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bab42-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bab42-110">*LanaIdList* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bab42-110">*LanaIdList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bab42-111">Matrice di numeri di LANA.</span><span class="sxs-lookup"><span data-stu-id="bab42-111">Array of LANA numbers.</span></span>

</dd> <dt>

<span data-ttu-id="bab42-112">*LanaIdDescriptions* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bab42-112">*LanaIdDescriptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bab42-113">Matrice di descrizioni di LANA corrispondenti alla matrice *LanaIdList* .</span><span class="sxs-lookup"><span data-stu-id="bab42-113">Array of LANA descriptions corresponding to the *LanaIdList* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bab42-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bab42-114">Return value</span></span>

<span data-ttu-id="bab42-115">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="bab42-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="bab42-116">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="bab42-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="bab42-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="bab42-117">Remarks</span></span>

<span data-ttu-id="bab42-118">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="bab42-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bab42-119">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="bab42-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="bab42-120">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="bab42-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bab42-121">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="bab42-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="bab42-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bab42-122">Requirements</span></span>



| <span data-ttu-id="bab42-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="bab42-123">Requirement</span></span> | <span data-ttu-id="bab42-124">Valore</span><span class="sxs-lookup"><span data-stu-id="bab42-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bab42-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bab42-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bab42-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bab42-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bab42-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bab42-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bab42-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bab42-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bab42-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bab42-129">Namespace</span></span><br/>                | <span data-ttu-id="bab42-130">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="bab42-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="bab42-131">MOF</span><span class="sxs-lookup"><span data-stu-id="bab42-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bab42-132"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bab42-132"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="bab42-133">DLL</span><span class="sxs-lookup"><span data-stu-id="bab42-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bab42-134"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bab42-134"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bab42-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bab42-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bab42-136">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="bab42-136">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 


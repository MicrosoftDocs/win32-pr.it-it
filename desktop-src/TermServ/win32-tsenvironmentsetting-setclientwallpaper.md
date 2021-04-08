---
title: Metodo SetClientWallPaper della classe Win32_TSEnvironmentSetting
description: Il metodo SetClientWallPaper imposta la proprietà ClientWallPaper.
ms.assetid: 08c41df4-5a3c-4799-bb64-61f414814d0c
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetClientWallPaper
- Metodo SetClientWallPaper Servizi Desktop remoto, classe Win32_TSEnvironmentSetting
- Classe Win32_TSEnvironmentSetting Servizi Desktop remoto, metodo SetClientWallPaper
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting.SetClientWallPaper
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ae476134cf526602a059b4714cded6fd6c990e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741258"
---
# <a name="setclientwallpaper-method-of-the-win32_tsenvironmentsetting-class"></a><span data-ttu-id="12fdb-106">Metodo SetClientWallPaper della \_ classe TSEnvironmentSetting Win32</span><span class="sxs-lookup"><span data-stu-id="12fdb-106">SetClientWallPaper method of the Win32\_TSEnvironmentSetting class</span></span>

<span data-ttu-id="12fdb-107">Il metodo **SetClientWallPaper** imposta la proprietà **ClientWallPaper** .</span><span class="sxs-lookup"><span data-stu-id="12fdb-107">The **SetClientWallPaper** method sets the **ClientWallPaper** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="12fdb-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12fdb-108">Syntax</span></span>


```mof
uint32 SetClientWallPaper(
  [in] uint32 ClientWallPaper
);
```



## <a name="parameters"></a><span data-ttu-id="12fdb-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="12fdb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12fdb-110">*ClientWallPaper* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12fdb-110">*ClientWallPaper* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12fdb-111">Flag che disabilita o Abilita la proprietà **ClientWallPaper** , che specifica se nel client viene visualizzata l'immagine dello sfondo o dello sfondo.</span><span class="sxs-lookup"><span data-stu-id="12fdb-111">Flag disabling or enabling the **ClientWallPaper** property, which specifies whether the background (or wallpaper) image is displayed on the client.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="12fdb-112"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="12fdb-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="12fdb-113">L'immagine di sfondo (o sfondo) non viene visualizzata nel client.</span><span class="sxs-lookup"><span data-stu-id="12fdb-113">The background (or wallpaper) image is not displayed on the client.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="12fdb-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="12fdb-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="12fdb-115">L'immagine di sfondo (o sfondo) viene visualizzata nel client.</span><span class="sxs-lookup"><span data-stu-id="12fdb-115">The background (or wallpaper) image is displayed on the client.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12fdb-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="12fdb-116">Return value</span></span>

<span data-ttu-id="12fdb-117">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="12fdb-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="12fdb-118">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="12fdb-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="12fdb-119">Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="12fdb-119">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="12fdb-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="12fdb-120">Remarks</span></span>

<span data-ttu-id="12fdb-121">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="12fdb-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="12fdb-122">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="12fdb-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="12fdb-123">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="12fdb-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="12fdb-124">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="12fdb-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="12fdb-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12fdb-125">Requirements</span></span>



| <span data-ttu-id="12fdb-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="12fdb-126">Requirement</span></span> | <span data-ttu-id="12fdb-127">Valore</span><span class="sxs-lookup"><span data-stu-id="12fdb-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12fdb-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12fdb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="12fdb-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12fdb-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="12fdb-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12fdb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="12fdb-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12fdb-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="12fdb-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="12fdb-132">Namespace</span></span><br/>                | <span data-ttu-id="12fdb-133">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="12fdb-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="12fdb-134">MOF</span><span class="sxs-lookup"><span data-stu-id="12fdb-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12fdb-135"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12fdb-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="12fdb-136">DLL</span><span class="sxs-lookup"><span data-stu-id="12fdb-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12fdb-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12fdb-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12fdb-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12fdb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12fdb-139">**\_TSEnvironmentSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="12fdb-139">**Win32\_TSEnvironmentSetting**</span></span>](win32-tsenvironmentsetting.md)
</dt> </dl>

 


---
title: Metodo GetCurrentVMMPlugin della classe Win32_SessionDirectoryVMMPlugin
description: Ottiene il plug-in con priorità più elevata attivato.
ms.assetid: 7712573f-2252-4a3c-820c-b679be5dfd46
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetCurrentVMMPlugin
- Metodo GetCurrentVMMPlugin Servizi Desktop remoto, classe Win32_SessionDirectoryVMMPlugin
- Classe Win32_SessionDirectoryVMMPlugin Servizi Desktop remoto, metodo GetCurrentVMMPlugin
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.GetCurrentVMMPlugin
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7162322f4e5e3939309d64e27c93cf8d20da540c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874542"
---
# <a name="getcurrentvmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="77f38-106">Metodo GetCurrentVMMPlugin della \_ classe SessionDirectoryVMMPlugin Win32</span><span class="sxs-lookup"><span data-stu-id="77f38-106">GetCurrentVMMPlugin method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="77f38-107">Ottiene il plug-in con priorità più elevata attivato.</span><span class="sxs-lookup"><span data-stu-id="77f38-107">Gets the highest priority plug-in that is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="77f38-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="77f38-108">Syntax</span></span>


```mof
uint32 GetCurrentVMMPlugin(
  [out] string  sName,
  [out] string  sProvider,
  [out] string  sServiceLocation,
  [out] string  sClassID,
  [out] sint32  Priority,
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="77f38-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="77f38-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77f38-110">*sName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="77f38-110">*sName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77f38-111">Nome del plug-in.</span><span class="sxs-lookup"><span data-stu-id="77f38-111">The name of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="77f38-112">*sProvider* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="77f38-112">*sProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77f38-113">Nome del provider del plug-in.</span><span class="sxs-lookup"><span data-stu-id="77f38-113">The name of the plug-in provider.</span></span>

</dd> <dt>

<span data-ttu-id="77f38-114">*sServiceLocation* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="77f38-114">*sServiceLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77f38-115">Posizione del servizio che il plug-in deve contattare.</span><span class="sxs-lookup"><span data-stu-id="77f38-115">The service location that the plug-in should contact.</span></span>

</dd> <dt>

<span data-ttu-id="77f38-116">*sClassID* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="77f38-116">*sClassID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77f38-117">Identificatore di classe del plug-in.</span><span class="sxs-lookup"><span data-stu-id="77f38-117">The class identifier of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="77f38-118">*Priorità* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="77f38-118">*Priority* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77f38-119">Priorità del plug-in.</span><span class="sxs-lookup"><span data-stu-id="77f38-119">The priority of the plug-in.</span></span> <span data-ttu-id="77f38-120">Maggiore è il valore, maggiore è la priorità del plug-in.</span><span class="sxs-lookup"><span data-stu-id="77f38-120">The higher the value, the higher the priority of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="77f38-121">*Abilitato* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="77f38-121">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77f38-122">Indica se il plug-in è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="77f38-122">Indicates whether the plug-in is enabled or disabled.</span></span> <span data-ttu-id="77f38-123">**True** se il plug-in è abilitato o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="77f38-123">**True** if the plug-in is enabled or **false** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77f38-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="77f38-124">Return value</span></span>

<span data-ttu-id="77f38-125">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="77f38-125">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="77f38-126">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="77f38-126">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="77f38-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77f38-127">Requirements</span></span>



| <span data-ttu-id="77f38-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="77f38-128">Requirement</span></span> | <span data-ttu-id="77f38-129">Valore</span><span class="sxs-lookup"><span data-stu-id="77f38-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="77f38-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77f38-130">Minimum supported client</span></span><br/> | <span data-ttu-id="77f38-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="77f38-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="77f38-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="77f38-132">Minimum supported server</span></span><br/> | <span data-ttu-id="77f38-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="77f38-133">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="77f38-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="77f38-134">Namespace</span></span><br/>                | <span data-ttu-id="77f38-135">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="77f38-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="77f38-136">MOF</span><span class="sxs-lookup"><span data-stu-id="77f38-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77f38-137"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="77f38-137"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="77f38-138">DLL</span><span class="sxs-lookup"><span data-stu-id="77f38-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77f38-139"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77f38-139"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77f38-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="77f38-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77f38-141">**\_SessionDirectoryVMMPlugin Win32**</span><span class="sxs-lookup"><span data-stu-id="77f38-141">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 






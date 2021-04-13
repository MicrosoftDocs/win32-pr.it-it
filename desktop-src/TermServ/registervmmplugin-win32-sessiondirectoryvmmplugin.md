---
title: Metodo RegisterVMMPlugin della classe Win32_SessionDirectoryVMMPlugin
description: Registra un nuovo plug-in VMM.
ms.assetid: 8fa6109e-6320-4ad1-b313-f100d8383f85
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RegisterVMMPlugin
- Metodo RegisterVMMPlugin Servizi Desktop remoto, classe Win32_SessionDirectoryVMMPlugin
- Classe Win32_SessionDirectoryVMMPlugin Servizi Desktop remoto, metodo RegisterVMMPlugin
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.RegisterVMMPlugin
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381be34f9398147b323fa99093479da48adfd480
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400434"
---
# <a name="registervmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="0c87a-106">Metodo RegisterVMMPlugin della \_ classe SessionDirectoryVMMPlugin Win32</span><span class="sxs-lookup"><span data-stu-id="0c87a-106">RegisterVMMPlugin method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="0c87a-107">Registra un nuovo plug-in VMM.</span><span class="sxs-lookup"><span data-stu-id="0c87a-107">Registers a new VMM plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c87a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0c87a-108">Syntax</span></span>


```mof
uint32 RegisterVMMPlugin(
  [in] string  sName,
  [in] string  sProvider,
  [in] string  sServiceLocation,
  [in] string  sClassID,
  [in] sint32  Priority = ,
  [in] boolean Enabled = 
);
```



## <a name="parameters"></a><span data-ttu-id="0c87a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0c87a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c87a-110">*sName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c87a-110">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c87a-111">Nome del plug-in.</span><span class="sxs-lookup"><span data-stu-id="0c87a-111">The name of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="0c87a-112">*sProvider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c87a-112">*sProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c87a-113">Nome del provider del plug-in.</span><span class="sxs-lookup"><span data-stu-id="0c87a-113">The name of the plug-in provider.</span></span>

</dd> <dt>

<span data-ttu-id="0c87a-114">*sServiceLocation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c87a-114">*sServiceLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c87a-115">Posizione del servizio che il plug-in deve contattare.</span><span class="sxs-lookup"><span data-stu-id="0c87a-115">The service location that the plug-in should contact.</span></span>

</dd> <dt>

<span data-ttu-id="0c87a-116">*sClassID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c87a-116">*sClassID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c87a-117">Identificatore di classe del plug-in.</span><span class="sxs-lookup"><span data-stu-id="0c87a-117">The class identifier of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="0c87a-118">*Priorità* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="0c87a-118">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c87a-119">Priorità del plug-in.</span><span class="sxs-lookup"><span data-stu-id="0c87a-119">The priority of the plug-in.</span></span> <span data-ttu-id="0c87a-120">Maggiore è il valore, maggiore è la priorità del plug-in.</span><span class="sxs-lookup"><span data-stu-id="0c87a-120">The higher the value, the higher the priority of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="0c87a-121">*Abilitato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c87a-121">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c87a-122">Indica se il plug-in è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="0c87a-122">Indicates whether the plug-in is enabled or disabled.</span></span> <span data-ttu-id="0c87a-123">**True** se il plug-in è abilitato o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0c87a-123">**True** if the plug-in is enabled or **false** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c87a-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0c87a-124">Return value</span></span>

<span data-ttu-id="0c87a-125">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="0c87a-125">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="0c87a-126">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="0c87a-126">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c87a-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c87a-127">Requirements</span></span>



| <span data-ttu-id="0c87a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c87a-128">Requirement</span></span> | <span data-ttu-id="0c87a-129">Valore</span><span class="sxs-lookup"><span data-stu-id="0c87a-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c87a-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c87a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0c87a-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0c87a-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="0c87a-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c87a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0c87a-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0c87a-133">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="0c87a-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0c87a-134">Namespace</span></span><br/>                | <span data-ttu-id="0c87a-135">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0c87a-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="0c87a-136">MOF</span><span class="sxs-lookup"><span data-stu-id="0c87a-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c87a-137"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0c87a-137"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c87a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="0c87a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c87a-139"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c87a-139"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c87a-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c87a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c87a-141">**\_SessionDirectoryVMMPlugin Win32**</span><span class="sxs-lookup"><span data-stu-id="0c87a-141">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 






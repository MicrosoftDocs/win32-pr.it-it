---
title: Metodo di priorità della classe Win32_SessionDirectoryVMMPlugin
description: Imposta la priorità del plug-in.
ms.assetid: ddcf30cd-b87c-4869-80fc-ec92092e0df3
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto metodo di priorità
- Servizi Desktop remoto metodo di priorità, classe Win32_SessionDirectoryVMMPlugin
- Classe Win32_SessionDirectoryVMMPlugin Servizi Desktop remoto, metodo sepriority
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetPriority
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5d20dbc4af332d0c658f819f8e47f5b3eb4e95b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964903"
---
# <a name="setpriority-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="1db59-106">Metodo di priorità della classe Win32 \_ SessionDirectoryVMMPlugin</span><span class="sxs-lookup"><span data-stu-id="1db59-106">SetPriority method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="1db59-107">Imposta la priorità del plug-in.</span><span class="sxs-lookup"><span data-stu-id="1db59-107">Sets the priority of the plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="1db59-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1db59-108">Syntax</span></span>


```mof
uint32 SetPriority(
  [in] sint32 Priority
);
```



## <a name="parameters"></a><span data-ttu-id="1db59-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1db59-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1db59-110">*Priorità* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="1db59-110">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1db59-111">Priorità del plug-in.</span><span class="sxs-lookup"><span data-stu-id="1db59-111">The priority of the plug-in.</span></span> <span data-ttu-id="1db59-112">Maggiore è il valore, maggiore è la priorità del plug-in.</span><span class="sxs-lookup"><span data-stu-id="1db59-112">The higher the value, the higher the priority of the plug-in.</span></span> <span data-ttu-id="1db59-113">Per impostazione predefinita, la priorità è zero.</span><span class="sxs-lookup"><span data-stu-id="1db59-113">The priority is zero by default.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1db59-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1db59-114">Return value</span></span>

<span data-ttu-id="1db59-115">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="1db59-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="1db59-116">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="1db59-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="1db59-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1db59-117">Requirements</span></span>



| <span data-ttu-id="1db59-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1db59-118">Requirement</span></span> | <span data-ttu-id="1db59-119">Valore</span><span class="sxs-lookup"><span data-stu-id="1db59-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1db59-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1db59-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1db59-121">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1db59-121">None supported</span></span><br/>                                                              |
| <span data-ttu-id="1db59-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1db59-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1db59-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1db59-123">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="1db59-124">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1db59-124">Namespace</span></span><br/>                | <span data-ttu-id="1db59-125">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="1db59-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="1db59-126">MOF</span><span class="sxs-lookup"><span data-stu-id="1db59-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1db59-127"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1db59-127"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="1db59-128">DLL</span><span class="sxs-lookup"><span data-stu-id="1db59-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1db59-129"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1db59-129"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1db59-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1db59-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1db59-131">**\_SessionDirectoryVMMPlugin Win32**</span><span class="sxs-lookup"><span data-stu-id="1db59-131">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 






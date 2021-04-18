---
title: Metodo Sename della classe Win32_SessionDirectoryVMMPlugin
description: Imposta il nome del plug-in.
ms.assetid: 8af4abca-f147-4027-91fb-4d669b58caa4
ms.tgt_platform: multiple
keywords:
- Metodo senamer Servizi Desktop remoto
- Metodo senamer Servizi Desktop remoto, classe Win32_SessionDirectoryVMMPlugin
- Classe Win32_SessionDirectoryVMMPlugin Servizi Desktop remoto, metodo SetValue
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetName
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc9902e8d5931f0800dc6c62d36815f4f78db73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340663"
---
# <a name="setname-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="cdf15-106">Metodo Sename della classe Win32 \_ SessionDirectoryVMMPlugin</span><span class="sxs-lookup"><span data-stu-id="cdf15-106">SetName method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="cdf15-107">Imposta il nome del plug-in.</span><span class="sxs-lookup"><span data-stu-id="cdf15-107">Sets the name of the plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdf15-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cdf15-108">Syntax</span></span>


```mof
uint32 SetName(
  [in] string sName
);
```



## <a name="parameters"></a><span data-ttu-id="cdf15-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="cdf15-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdf15-110">*sName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdf15-110">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdf15-111">Nome del plug-in.</span><span class="sxs-lookup"><span data-stu-id="cdf15-111">The name of the plug-in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdf15-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cdf15-112">Return value</span></span>

<span data-ttu-id="cdf15-113">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="cdf15-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="cdf15-114">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="cdf15-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdf15-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cdf15-115">Requirements</span></span>



| <span data-ttu-id="cdf15-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdf15-116">Requirement</span></span> | <span data-ttu-id="cdf15-117">Valore</span><span class="sxs-lookup"><span data-stu-id="cdf15-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cdf15-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cdf15-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cdf15-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="cdf15-119">None supported</span></span><br/>                                                              |
| <span data-ttu-id="cdf15-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cdf15-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cdf15-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cdf15-121">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="cdf15-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cdf15-122">Namespace</span></span><br/>                | <span data-ttu-id="cdf15-123">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="cdf15-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="cdf15-124">MOF</span><span class="sxs-lookup"><span data-stu-id="cdf15-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cdf15-125"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cdf15-125"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="cdf15-126">DLL</span><span class="sxs-lookup"><span data-stu-id="cdf15-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdf15-127"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdf15-127"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdf15-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cdf15-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdf15-129">**\_SessionDirectoryVMMPlugin Win32**</span><span class="sxs-lookup"><span data-stu-id="cdf15-129">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 






---
title: Metodo seenabled della classe Win32_SessionDirectoryVMMPlugin
description: Abilita o Disabilita il plug-in.
ms.assetid: 25ce0614-5c3b-4a79-9174-1a9de1eb6c33
ms.tgt_platform: multiple
keywords:
- Metodo seenabled Servizi Desktop remoto
- Metodo seenabled Servizi Desktop remoto, classe Win32_SessionDirectoryVMMPlugin
- Classe Win32_SessionDirectoryVMMPlugin Servizi Desktop remoto, metodo seenabled
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetEnabled
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7089a21f143b6f3b27fe9fe58563e6777bf2f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743610"
---
# <a name="setenabled-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="2edb5-106">Metodo seenabled della classe Win32 \_ SessionDirectoryVMMPlugin</span><span class="sxs-lookup"><span data-stu-id="2edb5-106">SetEnabled method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="2edb5-107">Abilita o Disabilita il plug-in.</span><span class="sxs-lookup"><span data-stu-id="2edb5-107">Enables or disables the plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="2edb5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2edb5-108">Syntax</span></span>


```mof
uint32 SetEnabled(
  [in] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="2edb5-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2edb5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2edb5-110">*Abilitato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2edb5-110">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2edb5-111">Indica se il plug-in è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="2edb5-111">Indicates whether the plug-in is enabled or disabled.</span></span> <span data-ttu-id="2edb5-112">**True** se il plug-in è abilitato o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2edb5-112">**True** if the plug-in is enabled or **false** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2edb5-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2edb5-113">Return value</span></span>

<span data-ttu-id="2edb5-114">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="2edb5-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="2edb5-115">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="2edb5-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="2edb5-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2edb5-116">Requirements</span></span>



| <span data-ttu-id="2edb5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2edb5-117">Requirement</span></span> | <span data-ttu-id="2edb5-118">Valore</span><span class="sxs-lookup"><span data-stu-id="2edb5-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2edb5-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2edb5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2edb5-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2edb5-120">None supported</span></span><br/>                                                              |
| <span data-ttu-id="2edb5-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2edb5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2edb5-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2edb5-122">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="2edb5-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2edb5-123">Namespace</span></span><br/>                | <span data-ttu-id="2edb5-124">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="2edb5-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="2edb5-125">MOF</span><span class="sxs-lookup"><span data-stu-id="2edb5-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2edb5-126"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2edb5-126"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="2edb5-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2edb5-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2edb5-128"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2edb5-128"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2edb5-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2edb5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2edb5-130">**\_SessionDirectoryVMMPlugin Win32**</span><span class="sxs-lookup"><span data-stu-id="2edb5-130">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 






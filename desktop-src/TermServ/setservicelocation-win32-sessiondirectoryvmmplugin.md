---
title: Metodo SetServiceLocation della classe Win32_SessionDirectoryVMMPlugin
description: Imposta il percorso del servizio per il plug-in.
ms.assetid: e886a40b-9ea9-4159-a2ea-776160559410
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetServiceLocation
- Metodo SetServiceLocation Servizi Desktop remoto, classe Win32_SessionDirectoryVMMPlugin
- Classe Win32_SessionDirectoryVMMPlugin Servizi Desktop remoto, metodo SetServiceLocation
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetServiceLocation
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64c16a6bbe802052f53d28d4cd8cc2b9ab559b61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518165"
---
# <a name="setservicelocation-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="9ac62-106">Metodo SetServiceLocation della \_ classe SessionDirectoryVMMPlugin Win32</span><span class="sxs-lookup"><span data-stu-id="9ac62-106">SetServiceLocation method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="9ac62-107">Imposta il percorso del servizio per il plug-in.</span><span class="sxs-lookup"><span data-stu-id="9ac62-107">Sets the service location for the plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ac62-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9ac62-108">Syntax</span></span>


```mof
uint32 SetServiceLocation(
  [in] string sServiceLocation
);
```



## <a name="parameters"></a><span data-ttu-id="9ac62-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="9ac62-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ac62-110">*sServiceLocation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ac62-110">*sServiceLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ac62-111">Posizione del servizio che il plug-in deve contattare.</span><span class="sxs-lookup"><span data-stu-id="9ac62-111">The service location that the plug-in should contact.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ac62-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9ac62-112">Return value</span></span>

<span data-ttu-id="9ac62-113">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="9ac62-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="9ac62-114">Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="9ac62-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ac62-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ac62-115">Requirements</span></span>



| <span data-ttu-id="9ac62-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ac62-116">Requirement</span></span> | <span data-ttu-id="9ac62-117">Valore</span><span class="sxs-lookup"><span data-stu-id="9ac62-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ac62-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ac62-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9ac62-119">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9ac62-119">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9ac62-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ac62-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9ac62-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9ac62-121">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="9ac62-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9ac62-122">Namespace</span></span><br/>                | <span data-ttu-id="9ac62-123">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="9ac62-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="9ac62-124">MOF</span><span class="sxs-lookup"><span data-stu-id="9ac62-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ac62-125"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ac62-125"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ac62-126">DLL</span><span class="sxs-lookup"><span data-stu-id="9ac62-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ac62-127"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ac62-127"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ac62-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ac62-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ac62-129">**\_SessionDirectoryVMMPlugin Win32**</span><span class="sxs-lookup"><span data-stu-id="9ac62-129">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 






---
title: Metodo di disconnessione della classe Win32_VirtualDesktopSession (Sensevts. h)
description: Disconnette l'utente dalla sessione desktop virtuale.
ms.assetid: a9c90ace-324c-4eec-86e1-30ce35307e52
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto metodo di disconnessione
- Servizi Desktop remoto metodo di disconnessione, classe Win32_VirtualDesktopSession
- Classe Win32_VirtualDesktopSession Servizi Desktop remoto, metodo di disconnessione
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession.Logoff
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4582744f0d8ba9300bd620a45190ec1de4819ee1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400780"
---
# <a name="logoff-method-of-the-win32_virtualdesktopsession-class"></a><span data-ttu-id="4bc25-106">Metodo di disconnessione della \_ classe Win32 VirtualDesktopSession</span><span class="sxs-lookup"><span data-stu-id="4bc25-106">Logoff method of the Win32\_VirtualDesktopSession class</span></span>

<span data-ttu-id="4bc25-107">Disconnette l'utente dalla sessione desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="4bc25-107">Logs off the user from the virtual desktop session.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bc25-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4bc25-108">Syntax</span></span>


```mof
uint32 Logoff();
```



## <a name="parameters"></a><span data-ttu-id="4bc25-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4bc25-109">Parameters</span></span>

<span data-ttu-id="4bc25-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="4bc25-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4bc25-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4bc25-111">Return value</span></span>

<span data-ttu-id="4bc25-112">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="4bc25-112">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bc25-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4bc25-113">Requirements</span></span>



| <span data-ttu-id="4bc25-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bc25-114">Requirement</span></span> | <span data-ttu-id="4bc25-115">Valore</span><span class="sxs-lookup"><span data-stu-id="4bc25-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bc25-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4bc25-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4bc25-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4bc25-117">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="4bc25-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4bc25-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4bc25-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4bc25-119">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="4bc25-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4bc25-120">Namespace</span></span><br/>                | <span data-ttu-id="4bc25-121">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="4bc25-121">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="4bc25-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4bc25-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bc25-123"><dt>Sensevts. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bc25-123"><dt>Sensevts.h</dt></span></span> </dl>       |
| <span data-ttu-id="4bc25-124">MOF</span><span class="sxs-lookup"><span data-stu-id="4bc25-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4bc25-125"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4bc25-125"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="4bc25-126">DLL</span><span class="sxs-lookup"><span data-stu-id="4bc25-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bc25-127"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bc25-127"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="4bc25-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4bc25-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bc25-129">**\_VirtualDesktopSession Win32**</span><span class="sxs-lookup"><span data-stu-id="4bc25-129">**Win32\_VirtualDesktopSession**</span></span>](win32-virtualdesktopsession.md)
</dt> </dl>

 

 






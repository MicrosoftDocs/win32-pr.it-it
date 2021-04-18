---
title: Metodo CancelPatch della classe Win32_RDMSVirtualDesktopCollection
description: Annulla un processo di provisioning degli aggiornamenti software per le macchine virtuali in un insieme di desktop virtuali.
ms.assetid: fb0d6831-5c69-4017-b725-1a5038ad69f5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo CancelPatch
- Metodo CancelPatch Servizi Desktop remoto, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Servizi Desktop remoto, metodo CancelPatch
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.CancelPatch
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e56f33a819da976187fba823ac30fada9ff38730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301236"
---
# <a name="cancelpatch-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="2395a-106">Metodo CancelPatch della \_ classe RDMSVirtualDesktopCollection Win32</span><span class="sxs-lookup"><span data-stu-id="2395a-106">CancelPatch method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="2395a-107">Annulla un processo di provisioning degli aggiornamenti software per le macchine virtuali in un insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="2395a-107">Cancels a software update provisioning job for the virtual machines in a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2395a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2395a-108">Syntax</span></span>


```mof
uint32 CancelPatch();
```



## <a name="parameters"></a><span data-ttu-id="2395a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="2395a-109">Parameters</span></span>

<span data-ttu-id="2395a-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="2395a-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2395a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2395a-111">Return value</span></span>

<span data-ttu-id="2395a-112">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="2395a-112">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2395a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2395a-113">Requirements</span></span>



| <span data-ttu-id="2395a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2395a-114">Requirement</span></span> | <span data-ttu-id="2395a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2395a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2395a-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2395a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2395a-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2395a-117">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="2395a-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2395a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2395a-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2395a-119">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="2395a-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2395a-120">Namespace</span></span><br/>                | <span data-ttu-id="2395a-121">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="2395a-121">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="2395a-122">MOF</span><span class="sxs-lookup"><span data-stu-id="2395a-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2395a-123"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2395a-123"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="2395a-124">DLL</span><span class="sxs-lookup"><span data-stu-id="2395a-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2395a-125"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2395a-125"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="2395a-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2395a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2395a-127">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="2395a-127">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 






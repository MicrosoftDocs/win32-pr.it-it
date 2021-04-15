---
title: Metodo RemoveVirtualDesktop della classe Win32_RDMSVirtualDesktopCollection
description: Rimuove un desktop virtuale dall'insieme di desktop virtuali.
ms.assetid: 287ebbb2-86db-4b4a-8dbb-ac5472789e72
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RemoveVirtualDesktop
- Metodo RemoveVirtualDesktop Servizi Desktop remoto, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Servizi Desktop remoto, metodo RemoveVirtualDesktop
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.RemoveVirtualDesktop
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a468de22d571fa52d37c2ad51d40d492af35384a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517529"
---
# <a name="removevirtualdesktop-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="e0b7c-106">Metodo RemoveVirtualDesktop della \_ classe RDMSVirtualDesktopCollection Win32</span><span class="sxs-lookup"><span data-stu-id="e0b7c-106">RemoveVirtualDesktop method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="e0b7c-107">Rimuove un desktop virtuale dall'insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="e0b7c-107">Removes a virtual desktop from the virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0b7c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0b7c-108">Syntax</span></span>


```mof
uint32 RemoveVirtualDesktop(
  [in] string VMName
);
```



## <a name="parameters"></a><span data-ttu-id="e0b7c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0b7c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0b7c-110">*VMName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0b7c-110">*VMName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0b7c-111">Nome della macchina virtuale che ospita il desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="e0b7c-111">The name of the virtual machine that hosts the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0b7c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e0b7c-112">Return value</span></span>

<span data-ttu-id="e0b7c-113">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="e0b7c-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0b7c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0b7c-114">Requirements</span></span>



| <span data-ttu-id="e0b7c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0b7c-115">Requirement</span></span> | <span data-ttu-id="e0b7c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="e0b7c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0b7c-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0b7c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e0b7c-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e0b7c-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="e0b7c-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0b7c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e0b7c-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e0b7c-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="e0b7c-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e0b7c-121">Namespace</span></span><br/>                | <span data-ttu-id="e0b7c-122">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="e0b7c-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="e0b7c-123">MOF</span><span class="sxs-lookup"><span data-stu-id="e0b7c-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0b7c-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0b7c-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="e0b7c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e0b7c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0b7c-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0b7c-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="e0b7c-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0b7c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0b7c-128">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="e0b7c-128">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 






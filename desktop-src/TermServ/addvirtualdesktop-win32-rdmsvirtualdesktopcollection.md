---
title: Metodo AddVirtualDesktop della classe Win32_RDMSVirtualDesktopCollection
description: Aggiunge un desktop virtuale all'insieme di desktop virtuali.
ms.assetid: 31a3aa28-6e5d-4f8a-81ff-ab011f568b6a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo AddVirtualDesktop
- Metodo AddVirtualDesktop Servizi Desktop remoto, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Servizi Desktop remoto, metodo AddVirtualDesktop
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.AddVirtualDesktop
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4858f99f2ea4793fe0d83d06a0aaa429b7aa8f71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517499"
---
# <a name="addvirtualdesktop-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="343df-106">Metodo AddVirtualDesktop della \_ classe RDMSVirtualDesktopCollection Win32</span><span class="sxs-lookup"><span data-stu-id="343df-106">AddVirtualDesktop method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="343df-107">Aggiunge un desktop virtuale all'insieme di desktop virtuali.</span><span class="sxs-lookup"><span data-stu-id="343df-107">Adds a virtual desktop to the virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="343df-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="343df-108">Syntax</span></span>


```mof
uint32 AddVirtualDesktop(
  [in] string VMName
);
```



## <a name="parameters"></a><span data-ttu-id="343df-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="343df-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="343df-110">*VMName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="343df-110">*VMName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="343df-111">Nome della macchina virtuale che ospita il desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="343df-111">The name of the virtual machine that hosts the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="343df-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="343df-112">Return value</span></span>

<span data-ttu-id="343df-113">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="343df-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="343df-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="343df-114">Requirements</span></span>



| <span data-ttu-id="343df-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="343df-115">Requirement</span></span> | <span data-ttu-id="343df-116">Valore</span><span class="sxs-lookup"><span data-stu-id="343df-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="343df-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="343df-117">Minimum supported client</span></span><br/> | <span data-ttu-id="343df-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="343df-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="343df-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="343df-119">Minimum supported server</span></span><br/> | <span data-ttu-id="343df-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="343df-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="343df-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="343df-121">Namespace</span></span><br/>                | <span data-ttu-id="343df-122">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="343df-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="343df-123">MOF</span><span class="sxs-lookup"><span data-stu-id="343df-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="343df-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="343df-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="343df-125">DLL</span><span class="sxs-lookup"><span data-stu-id="343df-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="343df-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="343df-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="343df-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="343df-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="343df-128">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="343df-128">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 






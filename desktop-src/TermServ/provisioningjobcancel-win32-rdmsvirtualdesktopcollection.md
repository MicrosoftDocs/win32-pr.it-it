---
title: Metodo ProvisioningJobCancel della classe Win32_RDMSVirtualDesktopCollection
description: Annulla un processo di provisioning di un desktop virtuale.
ms.assetid: 933ea0f3-b916-4e70-89de-597f9eb23976
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ProvisioningJobCancel
- Metodo ProvisioningJobCancel Servizi Desktop remoto, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Servizi Desktop remoto, metodo ProvisioningJobCancel
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningJobCancel
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f414bcdc264d682817898bae98fcf60a716452
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301862"
---
# <a name="provisioningjobcancel-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="c81f1-106">Metodo ProvisioningJobCancel della \_ classe RDMSVirtualDesktopCollection Win32</span><span class="sxs-lookup"><span data-stu-id="c81f1-106">ProvisioningJobCancel method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="c81f1-107">Annulla un processo di provisioning di un desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="c81f1-107">Cancels a virtual desktop provisioning job.</span></span>

## <a name="syntax"></a><span data-ttu-id="c81f1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c81f1-108">Syntax</span></span>


```mof
uint32 ProvisioningJobCancel(
  [in] string JobGuid
);
```



## <a name="parameters"></a><span data-ttu-id="c81f1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c81f1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c81f1-110">*JobGuid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c81f1-110">*JobGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c81f1-111">**GUID** che identifica in modo univoco il processo di provisioning da annullare.</span><span class="sxs-lookup"><span data-stu-id="c81f1-111">The **GUID** that uniquely identifies the provisioning job to cancel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c81f1-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c81f1-112">Return value</span></span>

<span data-ttu-id="c81f1-113">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="c81f1-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c81f1-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c81f1-114">Requirements</span></span>



| <span data-ttu-id="c81f1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c81f1-115">Requirement</span></span> | <span data-ttu-id="c81f1-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c81f1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c81f1-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c81f1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c81f1-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c81f1-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="c81f1-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c81f1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c81f1-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c81f1-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="c81f1-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c81f1-121">Namespace</span></span><br/>                | <span data-ttu-id="c81f1-122">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="c81f1-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="c81f1-123">MOF</span><span class="sxs-lookup"><span data-stu-id="c81f1-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c81f1-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c81f1-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="c81f1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c81f1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c81f1-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c81f1-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="c81f1-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c81f1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c81f1-128">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="c81f1-128">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 






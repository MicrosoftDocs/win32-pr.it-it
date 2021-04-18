---
title: Metodo ProvisioningJobGetReport della classe Win32_RDMSVirtualDesktopCollection
description: Ottiene un report sullo stato di un processo di provisioning di un desktop virtuale.
ms.assetid: 8fc03fed-0838-4530-9b0f-0f561d76769d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ProvisioningJobGetReport
- Metodo ProvisioningJobGetReport Servizi Desktop remoto, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Servizi Desktop remoto, metodo ProvisioningJobGetReport
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningJobGetReport
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6605402c6ed6c0269b9971922bdefd48f265c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301861"
---
# <a name="provisioningjobgetreport-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="24b1a-106">Metodo ProvisioningJobGetReport della \_ classe RDMSVirtualDesktopCollection Win32</span><span class="sxs-lookup"><span data-stu-id="24b1a-106">ProvisioningJobGetReport method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="24b1a-107">Ottiene un report sullo stato di un processo di provisioning di un desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="24b1a-107">Gets a report about the status of a virtual desktop provisioning job.</span></span>

## <a name="syntax"></a><span data-ttu-id="24b1a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="24b1a-108">Syntax</span></span>


```mof
uint32 ProvisioningJobGetReport(
  [in]  string JobGuid,
  [out] string JobReportXml
);
```



## <a name="parameters"></a><span data-ttu-id="24b1a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="24b1a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24b1a-110">*JobGuid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24b1a-110">*JobGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24b1a-111">**GUID** che identifica in modo univoco il processo di provisioning.</span><span class="sxs-lookup"><span data-stu-id="24b1a-111">The **GUID** that uniquely identifies the provisioning job.</span></span>

</dd> <dt>

<span data-ttu-id="24b1a-112">*JobReportXml* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="24b1a-112">*JobReportXml* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="24b1a-113">Stringa che contiene il report in formato XML.</span><span class="sxs-lookup"><span data-stu-id="24b1a-113">A string that contains the report in XML format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24b1a-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="24b1a-114">Return value</span></span>

<span data-ttu-id="24b1a-115">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="24b1a-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="24b1a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24b1a-116">Requirements</span></span>



| <span data-ttu-id="24b1a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="24b1a-117">Requirement</span></span> | <span data-ttu-id="24b1a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="24b1a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="24b1a-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24b1a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="24b1a-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="24b1a-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="24b1a-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24b1a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="24b1a-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="24b1a-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="24b1a-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="24b1a-123">Namespace</span></span><br/>                | <span data-ttu-id="24b1a-124">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="24b1a-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="24b1a-125">MOF</span><span class="sxs-lookup"><span data-stu-id="24b1a-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24b1a-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="24b1a-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="24b1a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="24b1a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24b1a-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24b1a-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="24b1a-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24b1a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24b1a-130">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="24b1a-130">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 






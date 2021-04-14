---
title: Metodo ProvisioningJobExecute della classe Win32_RDMSVirtualDesktopCollection
description: Esegue un processo di provisioning di desktop virtuale.
ms.assetid: 69f0cc6a-7eef-4cd9-94ac-f0c7e52d02d8
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ProvisioningJobExecute
- Metodo ProvisioningJobExecute Servizi Desktop remoto, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Servizi Desktop remoto, metodo ProvisioningJobExecute
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningJobExecute
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c632a6bdc5fc5c4a128941d8a6c8b4379ddf9629
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478869"
---
# <a name="provisioningjobexecute-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="0cfbe-106">Metodo ProvisioningJobExecute della \_ classe RDMSVirtualDesktopCollection Win32</span><span class="sxs-lookup"><span data-stu-id="0cfbe-106">ProvisioningJobExecute method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="0cfbe-107">Esegue un processo di provisioning di desktop virtuale.</span><span class="sxs-lookup"><span data-stu-id="0cfbe-107">Runs a virtual desktop provisioning job.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cfbe-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0cfbe-108">Syntax</span></span>


```mof
uint32 ProvisioningJobExecute(
  [in]  string JobInputXml,
  [out] string JobGuid
);
```



## <a name="parameters"></a><span data-ttu-id="0cfbe-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="0cfbe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cfbe-110">*JobInputXml* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0cfbe-110">*JobInputXml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfbe-111">Stringa che contiene le informazioni di provisioning in formato XML.</span><span class="sxs-lookup"><span data-stu-id="0cfbe-111">A string that contains the provisioning information in XML format.</span></span>

</dd> <dt>

<span data-ttu-id="0cfbe-112">*JobGuid* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0cfbe-112">*JobGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfbe-113">**GUID** che identifica in modo univoco il processo di provisioning da eseguire.</span><span class="sxs-lookup"><span data-stu-id="0cfbe-113">The **GUID** that uniquely identifies the provisioning job to run.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cfbe-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0cfbe-114">Return value</span></span>

<span data-ttu-id="0cfbe-115">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="0cfbe-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cfbe-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0cfbe-116">Requirements</span></span>



| <span data-ttu-id="0cfbe-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cfbe-117">Requirement</span></span> | <span data-ttu-id="0cfbe-118">Valore</span><span class="sxs-lookup"><span data-stu-id="0cfbe-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cfbe-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0cfbe-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0cfbe-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0cfbe-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="0cfbe-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0cfbe-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0cfbe-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0cfbe-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="0cfbe-123">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0cfbe-123">Namespace</span></span><br/>                | <span data-ttu-id="0cfbe-124">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="0cfbe-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="0cfbe-125">MOF</span><span class="sxs-lookup"><span data-stu-id="0cfbe-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0cfbe-126"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0cfbe-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="0cfbe-127">DLL</span><span class="sxs-lookup"><span data-stu-id="0cfbe-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cfbe-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cfbe-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="0cfbe-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0cfbe-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cfbe-130">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="0cfbe-130">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 






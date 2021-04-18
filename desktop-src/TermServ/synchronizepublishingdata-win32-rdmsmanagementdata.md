---
title: Metodo SynchronizePublishingData della classe Win32_RDMSManagementData
description: Sincronizza il set specificato di dati di pubblicazione per Desktop remoto Management Services (RDBMS).
ms.assetid: 0476ce12-9b08-418c-83c2-208275574f5b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SynchronizePublishingData
- Metodo SynchronizePublishingData Servizi Desktop remoto, classe Win32_RDMSManagementData
- Classe Win32_RDMSManagementData Servizi Desktop remoto, metodo SynchronizePublishingData
topic_type:
- apiref
api_name:
- Win32_RDMSManagementData.SynchronizePublishingData
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d389ad08d81f39cab45502a42f4ebd95e16f36c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400573"
---
# <a name="synchronizepublishingdata-method-of-the-win32_rdmsmanagementdata-class"></a><span data-ttu-id="a9ac1-106">Metodo SynchronizePublishingData della \_ classe RDMSManagementData Win32</span><span class="sxs-lookup"><span data-stu-id="a9ac1-106">SynchronizePublishingData method of the Win32\_RDMSManagementData class</span></span>

<span data-ttu-id="a9ac1-107">Sincronizza il set specificato di dati di pubblicazione per Desktop remoto Management Services (RDBMS).</span><span class="sxs-lookup"><span data-stu-id="a9ac1-107">Synchronizes the specified set of publishing data for Remote Desktop Management Services (RDMS).</span></span>

## <a name="syntax"></a><span data-ttu-id="a9ac1-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a9ac1-108">Syntax</span></span>


```mof
uint32 SynchronizePublishingData(
  [in] string Context
);
```



## <a name="parameters"></a><span data-ttu-id="a9ac1-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a9ac1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9ac1-110">*Contesto* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9ac1-110">*Context* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9ac1-111">Informazioni di contesto dei dati di pubblicazione da sincronizzare.</span><span class="sxs-lookup"><span data-stu-id="a9ac1-111">The context information of the publishing data to synchronize.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9ac1-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a9ac1-112">Return value</span></span>

<span data-ttu-id="a9ac1-113">Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.</span><span class="sxs-lookup"><span data-stu-id="a9ac1-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9ac1-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9ac1-114">Requirements</span></span>



| <span data-ttu-id="a9ac1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9ac1-115">Requirement</span></span> | <span data-ttu-id="a9ac1-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a9ac1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9ac1-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9ac1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a9ac1-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a9ac1-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="a9ac1-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9ac1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a9ac1-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a9ac1-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="a9ac1-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a9ac1-121">Namespace</span></span><br/>                | <span data-ttu-id="a9ac1-122">Radice \\ CIMv2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="a9ac1-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="a9ac1-123">MOF</span><span class="sxs-lookup"><span data-stu-id="a9ac1-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a9ac1-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a9ac1-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="a9ac1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a9ac1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9ac1-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9ac1-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="a9ac1-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9ac1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9ac1-128">**\_RDMSManagementData Win32**</span><span class="sxs-lookup"><span data-stu-id="a9ac1-128">**Win32\_RDMSManagementData**</span></span>](win32-rdmsmanagementdata.md)
</dt> </dl>

 

 






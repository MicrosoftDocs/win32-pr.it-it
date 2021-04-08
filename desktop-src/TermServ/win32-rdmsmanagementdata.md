---
title: Classe Win32_RDMSManagementData
description: Sincronizza i dati di pubblicazione per Desktop remoto Management Services (RDBMS).
ms.assetid: 17f06294-6580-4297-9301-f88314db7775
ms.tgt_platform: multiple
keywords:
- Classe Win32_RDMSManagementData Servizi Desktop remoto
- Classe Win32_RDMSManagementData Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RDMSManagementData
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dddf2a73673e886456eb43bfbd2cefc72250cc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047956"
---
# <a name="win32_rdmsmanagementdata-class"></a><span data-ttu-id="ffbd9-105">Win32 \_ RDMSManagementData (classe)</span><span class="sxs-lookup"><span data-stu-id="ffbd9-105">Win32\_RDMSManagementData class</span></span>

<span data-ttu-id="ffbd9-106">Sincronizza i dati di pubblicazione per Desktop remoto Management Services (RDBMS).</span><span class="sxs-lookup"><span data-stu-id="ffbd9-106">Synchronizes publishing data for Remote Desktop Management Services (RDMS).</span></span>

<span data-ttu-id="ffbd9-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ffbd9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffbd9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ffbd9-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSManagementData
{
};
```

## <a name="members"></a><span data-ttu-id="ffbd9-109">Members</span><span class="sxs-lookup"><span data-stu-id="ffbd9-109">Members</span></span>

<span data-ttu-id="ffbd9-110">La classe **Win32 \_ RDMSManagementData** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ffbd9-110">The **Win32\_RDMSManagementData** class has these types of members:</span></span>

-   [<span data-ttu-id="ffbd9-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="ffbd9-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ffbd9-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="ffbd9-112">Methods</span></span>

<span data-ttu-id="ffbd9-113">La classe **Win32 \_ RDMSManagementData** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="ffbd9-113">The **Win32\_RDMSManagementData** class has these methods.</span></span>



| <span data-ttu-id="ffbd9-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="ffbd9-114">Method</span></span>                                                                                        | <span data-ttu-id="ffbd9-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ffbd9-115">Description</span></span>                                                            |
|:----------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="ffbd9-116">**SynchronizeAllPublishingData**</span><span class="sxs-lookup"><span data-stu-id="ffbd9-116">**SynchronizeAllPublishingData**</span></span>](synchronizeallpublishingdata-win32-rdmsmanagementdata.md) | <span data-ttu-id="ffbd9-117">Sincronizza tutti i dati di pubblicazione per RDBMS.</span><span class="sxs-lookup"><span data-stu-id="ffbd9-117">Synchronizes all publishing data for RDMS.</span></span><br/>                  |
| [<span data-ttu-id="ffbd9-118">**SynchronizePublishingData**</span><span class="sxs-lookup"><span data-stu-id="ffbd9-118">**SynchronizePublishingData**</span></span>](synchronizepublishingdata-win32-rdmsmanagementdata.md)       | <span data-ttu-id="ffbd9-119">Sincronizza il set specificato di dati di pubblicazione per RDBMS.</span><span class="sxs-lookup"><span data-stu-id="ffbd9-119">Synchronizes the specified set of publishing data for RDMS.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ffbd9-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ffbd9-120">Requirements</span></span>



| <span data-ttu-id="ffbd9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffbd9-121">Requirement</span></span> | <span data-ttu-id="ffbd9-122">Valore</span><span class="sxs-lookup"><span data-stu-id="ffbd9-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffbd9-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ffbd9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ffbd9-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ffbd9-124">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="ffbd9-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ffbd9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ffbd9-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ffbd9-126">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="ffbd9-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ffbd9-127">Namespace</span></span><br/>                | <span data-ttu-id="ffbd9-128">Radice \\ CIMV2 \\ RDBMS</span><span class="sxs-lookup"><span data-stu-id="ffbd9-128">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="ffbd9-129">MOF</span><span class="sxs-lookup"><span data-stu-id="ffbd9-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ffbd9-130"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ffbd9-130"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="ffbd9-131">DLL</span><span class="sxs-lookup"><span data-stu-id="ffbd9-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffbd9-132"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffbd9-132"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="ffbd9-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ffbd9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffbd9-134">Provider di Desktop remoto Management Services</span><span class="sxs-lookup"><span data-stu-id="ffbd9-134">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

 






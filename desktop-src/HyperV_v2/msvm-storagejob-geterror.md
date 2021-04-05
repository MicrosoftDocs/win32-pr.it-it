---
description: Recupera l'errore.
ms.assetid: 785b83c4-06f4-46b5-81f7-35c6fce16c92
title: Metodo GetError della classe Msvm_StorageJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a7d8ff9c2c01bb21343b4859e2db2dbed7ad643e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883041"
---
# <a name="geterror-method-of-the-msvm_storagejob-class"></a><span data-ttu-id="bc546-103">Metodo GetError della \_ classe StorageJob di MSVM</span><span class="sxs-lookup"><span data-stu-id="bc546-103">GetError method of the Msvm\_StorageJob class</span></span>

<span data-ttu-id="bc546-104">Recupera l'errore.</span><span class="sxs-lookup"><span data-stu-id="bc546-104">Retrieves the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc546-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bc546-105">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="bc546-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bc546-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc546-107">*Errore* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bc546-107">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc546-108">Errore recuperato.</span><span class="sxs-lookup"><span data-stu-id="bc546-108">The retrieved error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc546-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bc546-109">Return value</span></span>

<span data-ttu-id="bc546-110">Questo metodo restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="bc546-110">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="bc546-111">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="bc546-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bc546-112">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="bc546-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="bc546-113">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="bc546-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="bc546-114">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="bc546-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="bc546-115">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="bc546-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="bc546-116">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="bc546-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="bc546-117">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="bc546-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="bc546-118">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="bc546-118">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="bc546-119">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="bc546-119">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="bc546-120">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="bc546-120">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="bc546-121">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="bc546-121">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="bc546-122">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="bc546-122">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="bc546-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc546-123">Requirements</span></span>



| <span data-ttu-id="bc546-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc546-124">Requirement</span></span> | <span data-ttu-id="bc546-125">Valore</span><span class="sxs-lookup"><span data-stu-id="bc546-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc546-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc546-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bc546-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="bc546-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="bc546-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc546-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bc546-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bc546-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="bc546-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bc546-130">Namespace</span></span><br/>                | <span data-ttu-id="bc546-131">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="bc546-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bc546-132">MOF</span><span class="sxs-lookup"><span data-stu-id="bc546-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc546-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bc546-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc546-134">DLL</span><span class="sxs-lookup"><span data-stu-id="bc546-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc546-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bc546-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bc546-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc546-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc546-137">**\_StorageJob MSVM**</span><span class="sxs-lookup"><span data-stu-id="bc546-137">**Msvm\_StorageJob**</span></span>](msvm-storagejob.md)
</dt> </dl>

 

 





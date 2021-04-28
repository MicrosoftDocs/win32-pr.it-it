---
description: "Metodo GetError della classe Msvm_VirtualSystemReferencePointExportJob: recupera l'errore."
ms.assetid: a30cb74a-4e41-4981-b355-6f46b4b75ce6
title: Metodo GetError della classe Msvm_VirtualSystemReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d1311e4e56b6396266ece72277e8ddadcdb9d835
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109339"
---
# <a name="geterror-method-of-the-msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="aa7a2-103">Metodo GetError della classe Msvm \_ VirtualSystemReferencePointExportJob</span><span class="sxs-lookup"><span data-stu-id="aa7a2-103">GetError method of the Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="aa7a2-104">Recupera l'errore.</span><span class="sxs-lookup"><span data-stu-id="aa7a2-104">Retrieves the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa7a2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aa7a2-105">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="aa7a2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="aa7a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa7a2-107">*Errore* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="aa7a2-107">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa7a2-108">Errore recuperato.</span><span class="sxs-lookup"><span data-stu-id="aa7a2-108">The error retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa7a2-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aa7a2-109">Return value</span></span>

<span data-ttu-id="aa7a2-110">In caso di esito positivo, restituisce un valore 0. in caso contrario, contiene un errore.</span><span class="sxs-lookup"><span data-stu-id="aa7a2-110">On success, returns a 0; otherwise, contains an error.</span></span>

<dl> <dt>

<span data-ttu-id="aa7a2-111">**Completata senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="aa7a2-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="aa7a2-112">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="aa7a2-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="aa7a2-113">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="aa7a2-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="aa7a2-114">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="aa7a2-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="aa7a2-115">**Lo stato è sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="aa7a2-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="aa7a2-116">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="aa7a2-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="aa7a2-117">**Parametro non** valido (32773)</span><span class="sxs-lookup"><span data-stu-id="aa7a2-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="aa7a2-118">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="aa7a2-118">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="aa7a2-119">**Stato non valido per questa operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="aa7a2-119">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="aa7a2-120">**Tipo di dati non** corretto (32776)</span><span class="sxs-lookup"><span data-stu-id="aa7a2-120">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="aa7a2-121">**Il sistema non è disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="aa7a2-121">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="aa7a2-122">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="aa7a2-122">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="aa7a2-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa7a2-123">Requirements</span></span>



| <span data-ttu-id="aa7a2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa7a2-124">Requirement</span></span> | <span data-ttu-id="aa7a2-125">Valore</span><span class="sxs-lookup"><span data-stu-id="aa7a2-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa7a2-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa7a2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="aa7a2-127">Windows 10, solo app desktop versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="aa7a2-127">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="aa7a2-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa7a2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="aa7a2-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="aa7a2-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="aa7a2-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="aa7a2-130">Namespace</span></span><br/>                | <span data-ttu-id="aa7a2-131">Virtualizzazione \\ radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="aa7a2-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="aa7a2-132">MOF</span><span class="sxs-lookup"><span data-stu-id="aa7a2-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa7a2-133"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="aa7a2-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa7a2-134">DLL</span><span class="sxs-lookup"><span data-stu-id="aa7a2-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa7a2-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="aa7a2-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="aa7a2-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa7a2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa7a2-137">**Msvm \_ VirtualSystemReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="aa7a2-137">**Msvm\_VirtualSystemReferencePointExportJob**</span></span>](msvm-virtualsystemreferencepointexportjob.md)
</dt> </dl>

 

 





---
description: Richiede all'Servizi Desktop remoto dispositivo virtuale di avviare una connessione tramite pipe alla macchina virtuale.
ms.assetid: e53238ee-8264-416b-8855-193c28089cfa
title: Metodo EnableEndPoints della classe Msvm_RdvComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RdvComponent.EnableEndPoints
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a668e6a2605a52c7021f630145d6e4897e1c76ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226241"
---
# <a name="enableendpoints-method-of-the-msvm_rdvcomponent-class"></a><span data-ttu-id="7a810-103">Metodo EnableEndPoints della classe MSVM \_ RdvComponent</span><span class="sxs-lookup"><span data-stu-id="7a810-103">EnableEndPoints method of the Msvm\_RdvComponent class</span></span>

<span data-ttu-id="7a810-104">Richiede all'Servizi Desktop remoto dispositivo virtuale di avviare una connessione tramite pipe alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7a810-104">Requests the Remote Desktop Services virtual device to start a pipe connection with the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a810-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a810-105">Syntax</span></span>


```mof
uint32 EnableEndPoints();
```



## <a name="parameters"></a><span data-ttu-id="7a810-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7a810-106">Parameters</span></span>

<span data-ttu-id="7a810-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="7a810-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7a810-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7a810-108">Return value</span></span>

<span data-ttu-id="7a810-109">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="7a810-109">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7a810-110">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="7a810-110">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7a810-111">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="7a810-111">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7a810-112">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="7a810-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="7a810-113">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="7a810-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="7a810-114">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="7a810-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="7a810-115">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="7a810-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="7a810-116">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="7a810-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="7a810-117">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="7a810-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="7a810-118">**Memoria insufficiente** (32774)</span><span class="sxs-lookup"><span data-stu-id="7a810-118">**Out of memory** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="7a810-119">**File non trovato** (32775)</span><span class="sxs-lookup"><span data-stu-id="7a810-119">**File not found** (32775)</span></span>
</dt> <dt>

 <span data-ttu-id="7a810-120">(32776)</span><span class="sxs-lookup"><span data-stu-id="7a810-120">(32776)</span></span>
</dt> <dt>

 <span data-ttu-id="7a810-121">(32777)</span><span class="sxs-lookup"><span data-stu-id="7a810-121">(32777)</span></span>
</dt> <dt>

 <span data-ttu-id="7a810-122">(32778)</span><span class="sxs-lookup"><span data-stu-id="7a810-122">(32778)</span></span>
</dt> <dt>

 <span data-ttu-id="7a810-123">(32779)</span><span class="sxs-lookup"><span data-stu-id="7a810-123">(32779)</span></span>
</dt> <dt>

 <span data-ttu-id="7a810-124">(32780)</span><span class="sxs-lookup"><span data-stu-id="7a810-124">(32780)</span></span>
</dt> <dt>

 <span data-ttu-id="7a810-125">(32781)</span><span class="sxs-lookup"><span data-stu-id="7a810-125">(32781)</span></span>
</dt> <dt>

 <span data-ttu-id="7a810-126">(32782)</span><span class="sxs-lookup"><span data-stu-id="7a810-126">(32782)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7a810-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a810-127">Requirements</span></span>



| <span data-ttu-id="7a810-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a810-128">Requirement</span></span> | <span data-ttu-id="7a810-129">Valore</span><span class="sxs-lookup"><span data-stu-id="7a810-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a810-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a810-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7a810-131">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7a810-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7a810-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a810-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7a810-133">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7a810-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7a810-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7a810-134">Namespace</span></span><br/>                | <span data-ttu-id="7a810-135">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="7a810-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7a810-136">MOF</span><span class="sxs-lookup"><span data-stu-id="7a810-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a810-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7a810-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a810-138">DLL</span><span class="sxs-lookup"><span data-stu-id="7a810-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a810-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7a810-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7a810-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a810-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a810-141">**\_RdvComponent MSVM**</span><span class="sxs-lookup"><span data-stu-id="7a810-141">**Msvm\_RdvComponent**</span></span>](msvm-rdvcomponent.md)
</dt> </dl>

 

 





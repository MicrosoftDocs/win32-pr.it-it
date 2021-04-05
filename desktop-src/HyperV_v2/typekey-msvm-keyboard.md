---
description: Simula una sequenza di tasti stampa-rilascio.
ms.assetid: 4166BA71-315D-41BD-857C-48AFB702911E
title: Metodo TypeKey della classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1b978da48600cc52472ab8bdec011ddbaa5ff624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968324"
---
# <a name="typekey-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="02e02-103">Metodo TypeKey della classe della \_ tastiera MSVM</span><span class="sxs-lookup"><span data-stu-id="02e02-103">TypeKey method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="02e02-104">Simula una sequenza di tasti stampa-rilascio.</span><span class="sxs-lookup"><span data-stu-id="02e02-104">Simulates a press-release key sequence.</span></span> <span data-ttu-id="02e02-105">Equivale alla chiamata a [**pulsanteper**](presskey-msvm-keyboard.md) seguita da [**ReleaseKey**](releasekey-msvm-keyboard.md).</span><span class="sxs-lookup"><span data-stu-id="02e02-105">This is equivalent to calling [**PressKey**](presskey-msvm-keyboard.md) followed by [**ReleaseKey**](releasekey-msvm-keyboard.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="02e02-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02e02-106">Syntax</span></span>


```mof
uint32 TypeKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a><span data-ttu-id="02e02-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="02e02-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02e02-108">*codice* \[ di stato in\]</span><span class="sxs-lookup"><span data-stu-id="02e02-108">*keyCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02e02-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02e02-109">Type: **uint32**</span></span>

<span data-ttu-id="02e02-110">Codice chiave virtuale della chiave da premere.</span><span class="sxs-lookup"><span data-stu-id="02e02-110">The virtual key code of the key to press.</span></span> <span data-ttu-id="02e02-111">Per l'elenco dei codici delle chiavi virtuali, vedere [**codici a chiave virtuale**](../inputdev/virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="02e02-111">For the list for virtual-key codes, see [**Virtual-Key Codes**](../inputdev/virtual-key-codes.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02e02-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="02e02-112">Return value</span></span>

<span data-ttu-id="02e02-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02e02-113">Type: **uint32**</span></span>

<span data-ttu-id="02e02-114">Un valore restituito pari a zero indica esito positivo.</span><span class="sxs-lookup"><span data-stu-id="02e02-114">A return value of zero indicates success.</span></span> <span data-ttu-id="02e02-115">Un valore diverso da zero indica un errore di modifica dello stato della chiave.</span><span class="sxs-lookup"><span data-stu-id="02e02-115">A nonzero value indicates a failure to modify the key state.</span></span>

<dl> <dt>

<span data-ttu-id="02e02-116">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="02e02-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="02e02-117">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="02e02-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="02e02-118">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="02e02-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="02e02-119">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="02e02-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="02e02-120">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="02e02-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="02e02-121">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="02e02-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="02e02-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="02e02-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="02e02-123">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="02e02-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="02e02-124">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="02e02-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="02e02-125">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="02e02-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="02e02-126">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="02e02-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="02e02-127">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="02e02-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="02e02-128">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="02e02-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="02e02-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="02e02-129">Remarks</span></span>

<span data-ttu-id="02e02-130">L'accesso alla classe della [**\_ tastiera MSVM**](msvm-keyboard.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="02e02-130">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="02e02-131">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="02e02-131">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="02e02-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02e02-132">Requirements</span></span>



| <span data-ttu-id="02e02-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="02e02-133">Requirement</span></span> | <span data-ttu-id="02e02-134">Valore</span><span class="sxs-lookup"><span data-stu-id="02e02-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02e02-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02e02-135">Minimum supported client</span></span><br/> | <span data-ttu-id="02e02-136">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="02e02-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="02e02-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02e02-137">Minimum supported server</span></span><br/> | <span data-ttu-id="02e02-138">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="02e02-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="02e02-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="02e02-139">Namespace</span></span><br/>                | <span data-ttu-id="02e02-140">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="02e02-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="02e02-141">MOF</span><span class="sxs-lookup"><span data-stu-id="02e02-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02e02-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="02e02-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="02e02-143">DLL</span><span class="sxs-lookup"><span data-stu-id="02e02-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02e02-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="02e02-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="02e02-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02e02-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02e02-146">**\_Tastiera MSVM**</span><span class="sxs-lookup"><span data-stu-id="02e02-146">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> <dt>

[<span data-ttu-id="02e02-147">**Codici chiave virtuale**</span><span class="sxs-lookup"><span data-stu-id="02e02-147">**Virtual-Key Codes**</span></span>](../inputdev/virtual-key-codes.md)
</dt> </dl>

 


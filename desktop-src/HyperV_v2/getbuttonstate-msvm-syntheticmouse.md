---
description: 'Metodo GetButtonState della Msvm_SyntheticMouse classe : recupera lo stato corrente del pulsante del dispositivo specificato.'
ms.assetid: 66363AF1-E360-478D-8E62-513DE66EF130
title: Metodo GetButtonState della Msvm_SyntheticMouse classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.GetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 26839292cf2fb3099e740629b28c7de0fbe3f60f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119389"
---
# <a name="getbuttonstate-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="51a71-103">Metodo GetButtonState della classe SyntheticMouse Msvm \_</span><span class="sxs-lookup"><span data-stu-id="51a71-103">GetButtonState method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="51a71-104">Recupera lo stato corrente del pulsante del dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="51a71-104">Retrieves the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="51a71-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="51a71-105">Syntax</span></span>


```mof
uint32 GetButtonState(
  [in]  uint32  buttonIndex,
  [out] boolean isDown
);
```



## <a name="parameters"></a><span data-ttu-id="51a71-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="51a71-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51a71-107">*buttonIndex* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="51a71-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51a71-108">Tipo: **uint32**</span><span class="sxs-lookup"><span data-stu-id="51a71-108">Type: **uint32**</span></span>

<span data-ttu-id="51a71-109">Indice in base 1 del pulsante su cui eseguire la query.</span><span class="sxs-lookup"><span data-stu-id="51a71-109">The 1-based index of the button to query.</span></span>

</dd> <dt>

<span data-ttu-id="51a71-110">*isDown* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="51a71-110">*isDown* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="51a71-111">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="51a71-111">Type: **boolean**</span></span>

<span data-ttu-id="51a71-112">Stato corrente verso il basso del pulsante.</span><span class="sxs-lookup"><span data-stu-id="51a71-112">The current down state of the button.</span></span> <span data-ttu-id="51a71-113">Un **valore True** indica che il pulsante è in basso.</span><span class="sxs-lookup"><span data-stu-id="51a71-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51a71-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="51a71-114">Return value</span></span>

<span data-ttu-id="51a71-115">Tipo: **uint32**</span><span class="sxs-lookup"><span data-stu-id="51a71-115">Type: **uint32**</span></span>

<span data-ttu-id="51a71-116">Un valore restituito pari a zero indica l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="51a71-116">A return value of zero indicates success.</span></span> <span data-ttu-id="51a71-117">Un valore diverso da zero indica un errore di query.</span><span class="sxs-lookup"><span data-stu-id="51a71-117">A nonzero value indicates a query failure.</span></span>

<dl> <dt>

<span data-ttu-id="51a71-118">**Completata senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="51a71-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="51a71-119">**Parametri del metodo verificati - Processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="51a71-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="51a71-120">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="51a71-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="51a71-121">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="51a71-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="51a71-122">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="51a71-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="51a71-123">**Lo stato è sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="51a71-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="51a71-124">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="51a71-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="51a71-125">**Parametro non** valido (32773)</span><span class="sxs-lookup"><span data-stu-id="51a71-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="51a71-126">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="51a71-126">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="51a71-127">**Stato non valido per questa operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="51a71-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="51a71-128">**Tipo di dati non** corretto (32776)</span><span class="sxs-lookup"><span data-stu-id="51a71-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="51a71-129">**Il sistema non è disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="51a71-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="51a71-130">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="51a71-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="51a71-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="51a71-131">Remarks</span></span>

<span data-ttu-id="51a71-132">L'accesso alla [**classe Msvm \_ SyntheticMouse**](msvm-syntheticmouse.md) potrebbe essere limitato dal filtro del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="51a71-132">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="51a71-133">Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)</span><span class="sxs-lookup"><span data-stu-id="51a71-133">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="51a71-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51a71-134">Requirements</span></span>



| <span data-ttu-id="51a71-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="51a71-135">Requirement</span></span> | <span data-ttu-id="51a71-136">Valore</span><span class="sxs-lookup"><span data-stu-id="51a71-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51a71-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51a71-137">Minimum supported client</span></span><br/> | <span data-ttu-id="51a71-138">Windows 8 solo \[ app desktop\]</span><span class="sxs-lookup"><span data-stu-id="51a71-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="51a71-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51a71-139">Minimum supported server</span></span><br/> | <span data-ttu-id="51a71-140">Solo app desktop di Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="51a71-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="51a71-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="51a71-141">Namespace</span></span><br/>                | <span data-ttu-id="51a71-142">Virtualizzazione \\ radice \\ V2</span><span class="sxs-lookup"><span data-stu-id="51a71-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="51a71-143">MOF</span><span class="sxs-lookup"><span data-stu-id="51a71-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51a71-144"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="51a71-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="51a71-145">DLL</span><span class="sxs-lookup"><span data-stu-id="51a71-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51a71-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="51a71-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="51a71-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="51a71-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51a71-148">**Msvm \_ SyntheticMouse**</span><span class="sxs-lookup"><span data-stu-id="51a71-148">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 


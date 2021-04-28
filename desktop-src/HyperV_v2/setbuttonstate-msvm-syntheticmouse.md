---
description: 'Metodo SetButtonState della classe Msvm_SyntheticMouse : imposta lo stato corrente del pulsante del dispositivo specificato.'
ms.assetid: 942DB31C-09A2-43B6-A666-267AF6A84E0E
title: Metodo SetButtonState della Msvm_SyntheticMouse classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.SetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 161520ac1b7e9dba1a084a8fb3c623155aa135fe
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109209"
---
# <a name="setbuttonstate-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="97de0-103">Metodo SetButtonState della classe SyntheticMouse Msvm \_</span><span class="sxs-lookup"><span data-stu-id="97de0-103">SetButtonState method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="97de0-104">Imposta lo stato corrente del pulsante del dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="97de0-104">Sets the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="97de0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="97de0-105">Syntax</span></span>


```mof
uint32 SetButtonState(
  [in] uint32  buttonIndex,
  [in] boolean isDown
);
```



## <a name="parameters"></a><span data-ttu-id="97de0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="97de0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97de0-107">*buttonIndex* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="97de0-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97de0-108">Tipo: **uint32**</span><span class="sxs-lookup"><span data-stu-id="97de0-108">Type: **uint32**</span></span>

<span data-ttu-id="97de0-109">Indice in base 1 del pulsante da modificare.</span><span class="sxs-lookup"><span data-stu-id="97de0-109">The 1-based index of the button to modify.</span></span>

</dd> <dt>

<span data-ttu-id="97de0-110">*isDown* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="97de0-110">*isDown* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97de0-111">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="97de0-111">Type: **boolean**</span></span>

<span data-ttu-id="97de0-112">Nuovo stato verso il basso del pulsante.</span><span class="sxs-lookup"><span data-stu-id="97de0-112">The new down state of the button.</span></span> <span data-ttu-id="97de0-113">Un **valore True** indica che il pulsante è in basso.</span><span class="sxs-lookup"><span data-stu-id="97de0-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97de0-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="97de0-114">Return value</span></span>

<span data-ttu-id="97de0-115">Tipo: **uint32**</span><span class="sxs-lookup"><span data-stu-id="97de0-115">Type: **uint32**</span></span>

<span data-ttu-id="97de0-116">I valori diversi da zero indicano un errore di modifica dello stato del pulsante.</span><span class="sxs-lookup"><span data-stu-id="97de0-116">Non zero values indicate a failure to modify the button state.</span></span>

<dl> <dt>

<span data-ttu-id="97de0-117">**Completata senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="97de0-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="97de0-118">**Parametri del metodo verificati - Processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="97de0-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="97de0-119">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="97de0-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="97de0-120">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="97de0-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="97de0-121">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="97de0-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="97de0-122">**Lo stato è sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="97de0-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="97de0-123">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="97de0-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="97de0-124">**Parametro non** valido (32773)</span><span class="sxs-lookup"><span data-stu-id="97de0-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="97de0-125">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="97de0-125">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="97de0-126">**Stato non valido per questa operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="97de0-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="97de0-127">**Tipo di dati non** corretto (32776)</span><span class="sxs-lookup"><span data-stu-id="97de0-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="97de0-128">**Il sistema non è disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="97de0-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="97de0-129">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="97de0-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="97de0-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="97de0-130">Remarks</span></span>

<span data-ttu-id="97de0-131">L'accesso alla [**classe Msvm \_ SyntheticMouse**](msvm-syntheticmouse.md) potrebbe essere limitato dal filtro del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="97de0-131">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="97de0-132">Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)</span><span class="sxs-lookup"><span data-stu-id="97de0-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="97de0-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97de0-133">Requirements</span></span>



| <span data-ttu-id="97de0-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="97de0-134">Requirement</span></span> | <span data-ttu-id="97de0-135">Valore</span><span class="sxs-lookup"><span data-stu-id="97de0-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97de0-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97de0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="97de0-137">Windows 8 solo \[ app desktop\]</span><span class="sxs-lookup"><span data-stu-id="97de0-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="97de0-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97de0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="97de0-139">Solo app desktop di Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="97de0-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="97de0-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="97de0-140">Namespace</span></span><br/>                | <span data-ttu-id="97de0-141">Virtualizzazione \\ radice \\ V2</span><span class="sxs-lookup"><span data-stu-id="97de0-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="97de0-142">MOF</span><span class="sxs-lookup"><span data-stu-id="97de0-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97de0-143"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="97de0-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="97de0-144">DLL</span><span class="sxs-lookup"><span data-stu-id="97de0-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97de0-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="97de0-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="97de0-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97de0-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97de0-147">**Msvm \_ SyntheticMouse**</span><span class="sxs-lookup"><span data-stu-id="97de0-147">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 


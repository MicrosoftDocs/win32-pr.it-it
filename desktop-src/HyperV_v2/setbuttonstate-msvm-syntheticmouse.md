---
description: Imposta lo stato corrente del pulsante del dispositivo specificato.
ms.assetid: 942DB31C-09A2-43B6-A666-267AF6A84E0E
title: Metodo SetButtonState della classe Msvm_SyntheticMouse
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
ms.openlocfilehash: c99915fa8ede9cbb405f4483ac10ca9ff8efaf71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227418"
---
# <a name="setbuttonstate-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="1eba2-103">Metodo SetButtonState della classe MSVM \_ SyntheticMouse</span><span class="sxs-lookup"><span data-stu-id="1eba2-103">SetButtonState method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="1eba2-104">Imposta lo stato corrente del pulsante del dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="1eba2-104">Sets the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eba2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1eba2-105">Syntax</span></span>


```mof
uint32 SetButtonState(
  [in] uint32  buttonIndex,
  [in] boolean isDown
);
```



## <a name="parameters"></a><span data-ttu-id="1eba2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1eba2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1eba2-107">*ButtonIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1eba2-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eba2-108">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1eba2-108">Type: **uint32**</span></span>

<span data-ttu-id="1eba2-109">Indice in base 1 del pulsante da modificare.</span><span class="sxs-lookup"><span data-stu-id="1eba2-109">The 1-based index of the button to modify.</span></span>

</dd> <dt>

<span data-ttu-id="1eba2-110">in *basso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1eba2-110">*isDown* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1eba2-111">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="1eba2-111">Type: **boolean**</span></span>

<span data-ttu-id="1eba2-112">Nuovo stato di inattività del pulsante.</span><span class="sxs-lookup"><span data-stu-id="1eba2-112">The new down state of the button.</span></span> <span data-ttu-id="1eba2-113">Un valore **true** indica che il pulsante è inattivo.</span><span class="sxs-lookup"><span data-stu-id="1eba2-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1eba2-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1eba2-114">Return value</span></span>

<span data-ttu-id="1eba2-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1eba2-115">Type: **uint32**</span></span>

<span data-ttu-id="1eba2-116">I valori diversi da zero indicano un errore di modifica dello stato del pulsante.</span><span class="sxs-lookup"><span data-stu-id="1eba2-116">Non zero values indicate a failure to modify the button state.</span></span>

<dl> <dt>

<span data-ttu-id="1eba2-117">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="1eba2-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1eba2-118">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="1eba2-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="1eba2-119">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="1eba2-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="1eba2-120">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="1eba2-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="1eba2-121">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="1eba2-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="1eba2-122">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="1eba2-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="1eba2-123">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="1eba2-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="1eba2-124">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="1eba2-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="1eba2-125">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="1eba2-125">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="1eba2-126">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="1eba2-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="1eba2-127">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="1eba2-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="1eba2-128">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="1eba2-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="1eba2-129">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="1eba2-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="1eba2-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="1eba2-130">Remarks</span></span>

<span data-ttu-id="1eba2-131">L'accesso alla [**classe \_ SyntheticMouse di MSVM**](msvm-syntheticmouse.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="1eba2-131">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="1eba2-132">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="1eba2-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="1eba2-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1eba2-133">Requirements</span></span>



| <span data-ttu-id="1eba2-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="1eba2-134">Requirement</span></span> | <span data-ttu-id="1eba2-135">Valore</span><span class="sxs-lookup"><span data-stu-id="1eba2-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1eba2-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1eba2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1eba2-137">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1eba2-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1eba2-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1eba2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1eba2-139">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1eba2-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1eba2-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1eba2-140">Namespace</span></span><br/>                | <span data-ttu-id="1eba2-141">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="1eba2-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1eba2-142">MOF</span><span class="sxs-lookup"><span data-stu-id="1eba2-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1eba2-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1eba2-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1eba2-144">DLL</span><span class="sxs-lookup"><span data-stu-id="1eba2-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1eba2-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1eba2-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1eba2-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1eba2-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eba2-147">**\_SyntheticMouse MSVM**</span><span class="sxs-lookup"><span data-stu-id="1eba2-147">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 


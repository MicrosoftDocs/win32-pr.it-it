---
description: Imposta lo stato corrente del pulsante del dispositivo specificato.
ms.assetid: 312A2B8B-D518-4797-9B50-F12493598CD6
title: Metodo SetButtonState della classe Msvm_Ps2Mouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.SetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 34475edfa27d08cbe9de488502686a84e4391eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311771"
---
# <a name="setbuttonstate-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="061cf-103">Metodo SetButtonState della classe MSVM \_ Ps2mouse</span><span class="sxs-lookup"><span data-stu-id="061cf-103">SetButtonState method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="061cf-104">Imposta lo stato corrente del pulsante del dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="061cf-104">Sets the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="061cf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="061cf-105">Syntax</span></span>


```mof
uint32 SetButtonState(
  [in] uint32  buttonIndex,
  [in] boolean buttonState
);
```



## <a name="parameters"></a><span data-ttu-id="061cf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="061cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="061cf-107">*ButtonIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="061cf-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="061cf-108">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="061cf-108">Type: **uint32**</span></span>

<span data-ttu-id="061cf-109">Indice in base 1 del pulsante da modificare.</span><span class="sxs-lookup"><span data-stu-id="061cf-109">The 1-based index of the button to modify.</span></span>

</dd> <dt>

<span data-ttu-id="061cf-110">*ButtonState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="061cf-110">*buttonState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="061cf-111">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="061cf-111">Type: **boolean**</span></span>

<span data-ttu-id="061cf-112">Nuovo stato di inattività del pulsante.</span><span class="sxs-lookup"><span data-stu-id="061cf-112">The new down state of the button.</span></span> <span data-ttu-id="061cf-113">Un valore **true** indica che il pulsante è inattivo.</span><span class="sxs-lookup"><span data-stu-id="061cf-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="061cf-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="061cf-114">Return value</span></span>

<span data-ttu-id="061cf-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="061cf-115">Type: **uint32**</span></span>

<span data-ttu-id="061cf-116">Un valore restituito pari a zero indica esito positivo.</span><span class="sxs-lookup"><span data-stu-id="061cf-116">A return value of zero indicates success.</span></span> <span data-ttu-id="061cf-117">Un valore diverso da zero indica un errore di modifica dello stato del pulsante.</span><span class="sxs-lookup"><span data-stu-id="061cf-117">A nonzero value indicates a failure to modify the button state.</span></span>

<dl> <dt>

<span data-ttu-id="061cf-118">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="061cf-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="061cf-119">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="061cf-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="061cf-120">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="061cf-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="061cf-121">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="061cf-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="061cf-122">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="061cf-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="061cf-123">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="061cf-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="061cf-124">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="061cf-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="061cf-125">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="061cf-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="061cf-126">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="061cf-126">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="061cf-127">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="061cf-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="061cf-128">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="061cf-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="061cf-129">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="061cf-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="061cf-130">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="061cf-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="061cf-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="061cf-131">Remarks</span></span>

<span data-ttu-id="061cf-132">L'accesso alla [**classe \_ Ps2Mouse di MSVM**](msvm-ps2mouse.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="061cf-132">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="061cf-133">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="061cf-133">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="061cf-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="061cf-134">Requirements</span></span>



| <span data-ttu-id="061cf-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="061cf-135">Requirement</span></span> | <span data-ttu-id="061cf-136">Valore</span><span class="sxs-lookup"><span data-stu-id="061cf-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="061cf-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="061cf-137">Minimum supported client</span></span><br/> | <span data-ttu-id="061cf-138">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="061cf-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="061cf-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="061cf-139">Minimum supported server</span></span><br/> | <span data-ttu-id="061cf-140">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="061cf-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="061cf-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="061cf-141">Namespace</span></span><br/>                | <span data-ttu-id="061cf-142">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="061cf-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="061cf-143">MOF</span><span class="sxs-lookup"><span data-stu-id="061cf-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="061cf-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="061cf-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="061cf-145">DLL</span><span class="sxs-lookup"><span data-stu-id="061cf-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="061cf-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="061cf-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="061cf-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="061cf-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="061cf-148">**\_Ps2Mouse MSVM**</span><span class="sxs-lookup"><span data-stu-id="061cf-148">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 


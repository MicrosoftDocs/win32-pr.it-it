---
description: 'Metodo SetButtonState della classe Msvm_Ps2Mouse : imposta lo stato corrente del pulsante del dispositivo specificato.'
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
ms.openlocfilehash: ea6a984b84c7ee17436a7fb4738433edce6d68d8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118529"
---
# <a name="setbuttonstate-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="dfb9c-103">Metodo SetButtonState della classe Msvm \_ Ps2Mouse</span><span class="sxs-lookup"><span data-stu-id="dfb9c-103">SetButtonState method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="dfb9c-104">Imposta lo stato corrente del pulsante del dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="dfb9c-104">Sets the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfb9c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dfb9c-105">Syntax</span></span>


```mof
uint32 SetButtonState(
  [in] uint32  buttonIndex,
  [in] boolean buttonState
);
```



## <a name="parameters"></a><span data-ttu-id="dfb9c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dfb9c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfb9c-107">*buttonIndex* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="dfb9c-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfb9c-108">Tipo: **uint32**</span><span class="sxs-lookup"><span data-stu-id="dfb9c-108">Type: **uint32**</span></span>

<span data-ttu-id="dfb9c-109">Indice in base 1 del pulsante da modificare.</span><span class="sxs-lookup"><span data-stu-id="dfb9c-109">The 1-based index of the button to modify.</span></span>

</dd> <dt>

<span data-ttu-id="dfb9c-110">*buttonState* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="dfb9c-110">*buttonState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfb9c-111">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="dfb9c-111">Type: **boolean**</span></span>

<span data-ttu-id="dfb9c-112">Nuovo stato verso il basso del pulsante.</span><span class="sxs-lookup"><span data-stu-id="dfb9c-112">The new down state of the button.</span></span> <span data-ttu-id="dfb9c-113">Il **valore True** indica che il pulsante è in basso.</span><span class="sxs-lookup"><span data-stu-id="dfb9c-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfb9c-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dfb9c-114">Return value</span></span>

<span data-ttu-id="dfb9c-115">Tipo: **uint32**</span><span class="sxs-lookup"><span data-stu-id="dfb9c-115">Type: **uint32**</span></span>

<span data-ttu-id="dfb9c-116">Un valore restituito pari a zero indica l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="dfb9c-116">A return value of zero indicates success.</span></span> <span data-ttu-id="dfb9c-117">Un valore diverso da zero indica un errore di modifica dello stato del pulsante.</span><span class="sxs-lookup"><span data-stu-id="dfb9c-117">A nonzero value indicates a failure to modify the button state.</span></span>

<dl> <dt>

<span data-ttu-id="dfb9c-118">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="dfb9c-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dfb9c-119">**Parametri del metodo controllati - Processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="dfb9c-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="dfb9c-120">**Operazione non** riuscita (32768)</span><span class="sxs-lookup"><span data-stu-id="dfb9c-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="dfb9c-121">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="dfb9c-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="dfb9c-122">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="dfb9c-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="dfb9c-123">**Lo stato è sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="dfb9c-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="dfb9c-124">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="dfb9c-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="dfb9c-125">**Parametro non** valido (32773)</span><span class="sxs-lookup"><span data-stu-id="dfb9c-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="dfb9c-126">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="dfb9c-126">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="dfb9c-127">**Stato non valido per questa operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="dfb9c-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="dfb9c-128">**Tipo di dati non** corretto (32776)</span><span class="sxs-lookup"><span data-stu-id="dfb9c-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="dfb9c-129">**Il sistema non è disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="dfb9c-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="dfb9c-130">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="dfb9c-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="dfb9c-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="dfb9c-131">Remarks</span></span>

<span data-ttu-id="dfb9c-132">L'accesso alla [**classe Msvm \_ Ps2Mouse**](msvm-ps2mouse.md) potrebbe essere limitato dal filtro di Controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="dfb9c-132">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="dfb9c-133">Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)</span><span class="sxs-lookup"><span data-stu-id="dfb9c-133">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="dfb9c-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dfb9c-134">Requirements</span></span>



| <span data-ttu-id="dfb9c-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfb9c-135">Requirement</span></span> | <span data-ttu-id="dfb9c-136">Valore</span><span class="sxs-lookup"><span data-stu-id="dfb9c-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfb9c-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dfb9c-137">Minimum supported client</span></span><br/> | <span data-ttu-id="dfb9c-138">Windows 8 solo \[ app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dfb9c-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dfb9c-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dfb9c-139">Minimum supported server</span></span><br/> | <span data-ttu-id="dfb9c-140">Solo app desktop di Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="dfb9c-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dfb9c-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dfb9c-141">Namespace</span></span><br/>                | <span data-ttu-id="dfb9c-142">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="dfb9c-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dfb9c-143">MOF</span><span class="sxs-lookup"><span data-stu-id="dfb9c-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dfb9c-144"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="dfb9c-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dfb9c-145">DLL</span><span class="sxs-lookup"><span data-stu-id="dfb9c-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfb9c-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dfb9c-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dfb9c-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dfb9c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfb9c-148">**Msvm \_ Ps2Mouse**</span><span class="sxs-lookup"><span data-stu-id="dfb9c-148">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 


---
description: Recupera lo stato corrente del pulsante del dispositivo specificato.
ms.assetid: 66363AF1-E360-478D-8E62-513DE66EF130
title: Metodo GetButtonState della classe Msvm_SyntheticMouse
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
ms.openlocfilehash: 3812d3e019a303656305471fc097fb1479fa1ada
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307753"
---
# <a name="getbuttonstate-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="bf1bd-103">Metodo GetButtonState della classe MSVM \_ SyntheticMouse</span><span class="sxs-lookup"><span data-stu-id="bf1bd-103">GetButtonState method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="bf1bd-104">Recupera lo stato corrente del pulsante del dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-104">Retrieves the current state of the specified device button.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf1bd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf1bd-105">Syntax</span></span>


```mof
uint32 GetButtonState(
  [in]  uint32  buttonIndex,
  [out] boolean isDown
);
```



## <a name="parameters"></a><span data-ttu-id="bf1bd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bf1bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf1bd-107">*ButtonIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bf1bd-107">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf1bd-108">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf1bd-108">Type: **uint32**</span></span>

<span data-ttu-id="bf1bd-109">Indice in base 1 del pulsante su cui eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-109">The 1-based index of the button to query.</span></span>

</dd> <dt>

<span data-ttu-id="bf1bd-110">in *basso* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="bf1bd-110">*isDown* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf1bd-111">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="bf1bd-111">Type: **boolean**</span></span>

<span data-ttu-id="bf1bd-112">Stato di inattività corrente del pulsante.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-112">The current down state of the button.</span></span> <span data-ttu-id="bf1bd-113">Un valore **true** indica che il pulsante è inattivo.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-113">A **True** value means the button is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf1bd-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf1bd-114">Return value</span></span>

<span data-ttu-id="bf1bd-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bf1bd-115">Type: **uint32**</span></span>

<span data-ttu-id="bf1bd-116">Un valore restituito pari a zero indica esito positivo.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-116">A return value of zero indicates success.</span></span> <span data-ttu-id="bf1bd-117">Un valore diverso da zero indica un errore di query.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-117">A nonzero value indicates a query failure.</span></span>

<dl> <dt>

<span data-ttu-id="bf1bd-118">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="bf1bd-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bf1bd-119">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="bf1bd-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="bf1bd-120">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="bf1bd-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="bf1bd-121">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="bf1bd-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="bf1bd-122">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="bf1bd-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="bf1bd-123">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="bf1bd-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="bf1bd-124">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="bf1bd-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="bf1bd-125">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="bf1bd-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="bf1bd-126">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="bf1bd-126">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="bf1bd-127">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="bf1bd-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="bf1bd-128">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="bf1bd-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="bf1bd-129">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="bf1bd-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="bf1bd-130">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="bf1bd-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="bf1bd-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf1bd-131">Remarks</span></span>

<span data-ttu-id="bf1bd-132">L'accesso alla [**classe \_ SyntheticMouse di MSVM**](msvm-syntheticmouse.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="bf1bd-132">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="bf1bd-133">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="bf1bd-133">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf1bd-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf1bd-134">Requirements</span></span>



| <span data-ttu-id="bf1bd-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf1bd-135">Requirement</span></span> | <span data-ttu-id="bf1bd-136">Valore</span><span class="sxs-lookup"><span data-stu-id="bf1bd-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf1bd-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf1bd-137">Minimum supported client</span></span><br/> | <span data-ttu-id="bf1bd-138">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="bf1bd-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bf1bd-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf1bd-139">Minimum supported server</span></span><br/> | <span data-ttu-id="bf1bd-140">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="bf1bd-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bf1bd-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bf1bd-141">Namespace</span></span><br/>                | <span data-ttu-id="bf1bd-142">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="bf1bd-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bf1bd-143">MOF</span><span class="sxs-lookup"><span data-stu-id="bf1bd-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf1bd-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bf1bd-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf1bd-145">DLL</span><span class="sxs-lookup"><span data-stu-id="bf1bd-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf1bd-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bf1bd-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bf1bd-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf1bd-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf1bd-148">**\_SyntheticMouse MSVM**</span><span class="sxs-lookup"><span data-stu-id="bf1bd-148">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 


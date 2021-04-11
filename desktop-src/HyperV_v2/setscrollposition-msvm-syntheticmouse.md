---
description: Imposta la coordinata z del controllo rotellina del dispositivo di puntamento.
ms.assetid: 02349957-6BAA-42E7-B3D4-F39E748615E6
title: Metodo SetScrollPosition della classe Msvm_SyntheticMouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.SetScrollPosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6d82ad2cd75b41ca914d0db49d5de4709790ea6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131878"
---
# <a name="setscrollposition-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="67de4-103">Metodo SetScrollPosition della classe MSVM \_ SyntheticMouse</span><span class="sxs-lookup"><span data-stu-id="67de4-103">SetScrollPosition method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="67de4-104">Imposta la coordinata z del controllo rotellina del dispositivo di puntamento.</span><span class="sxs-lookup"><span data-stu-id="67de4-104">Sets the z-coordinate of the wheel control of the pointing device.</span></span> <span data-ttu-id="67de4-105">I valori scritti in questa proprietà sono sempre offset delle coordinate relative.</span><span class="sxs-lookup"><span data-stu-id="67de4-105">Values written to this property are always relative coordinate offsets.</span></span>

## <a name="syntax"></a><span data-ttu-id="67de4-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="67de4-106">Syntax</span></span>


```mof
uint32 SetScrollPosition(
  [in] sint32 scrollPositionDelta
);
```



## <a name="parameters"></a><span data-ttu-id="67de4-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="67de4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67de4-108">*scrollPositionDelta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67de4-108">*scrollPositionDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67de4-109">Tipo: **sint32**</span><span class="sxs-lookup"><span data-stu-id="67de4-109">Type: **sint32**</span></span>

<span data-ttu-id="67de4-110">Delta della posizione di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="67de4-110">The delta of the scroll position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67de4-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="67de4-111">Return value</span></span>

<span data-ttu-id="67de4-112">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67de4-112">Type: **uint32**</span></span>

<span data-ttu-id="67de4-113">Un valore restituito pari a zero indica esito positivo.</span><span class="sxs-lookup"><span data-stu-id="67de4-113">A return value of zero indicates success.</span></span> <span data-ttu-id="67de4-114">Un valore diverso da zero indica un errore di modifica della posizione di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="67de4-114">A nonzero value indicates a failure to alter the scroll position.</span></span>

<dl> <dt>

<span data-ttu-id="67de4-115">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="67de4-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="67de4-116">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="67de4-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="67de4-117">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="67de4-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="67de4-118">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="67de4-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="67de4-119">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="67de4-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="67de4-120">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="67de4-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="67de4-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="67de4-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="67de4-122">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="67de4-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="67de4-123">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="67de4-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="67de4-124">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="67de4-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="67de4-125">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="67de4-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="67de4-126">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="67de4-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="67de4-127">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="67de4-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="67de4-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="67de4-128">Remarks</span></span>

<span data-ttu-id="67de4-129">L'accesso alla [**classe \_ SyntheticMouse di MSVM**](msvm-syntheticmouse.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="67de4-129">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="67de4-130">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="67de4-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="67de4-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67de4-131">Requirements</span></span>



| <span data-ttu-id="67de4-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="67de4-132">Requirement</span></span> | <span data-ttu-id="67de4-133">Valore</span><span class="sxs-lookup"><span data-stu-id="67de4-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67de4-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67de4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="67de4-135">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="67de4-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="67de4-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67de4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="67de4-137">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="67de4-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="67de4-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="67de4-138">Namespace</span></span><br/>                | <span data-ttu-id="67de4-139">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="67de4-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="67de4-140">MOF</span><span class="sxs-lookup"><span data-stu-id="67de4-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67de4-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="67de4-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="67de4-142">DLL</span><span class="sxs-lookup"><span data-stu-id="67de4-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67de4-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="67de4-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="67de4-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="67de4-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67de4-145">**\_SyntheticMouse MSVM**</span><span class="sxs-lookup"><span data-stu-id="67de4-145">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 


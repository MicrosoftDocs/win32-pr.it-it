---
description: Regola la coordinata z del controllo rotellina del dispositivo di puntamento.
ms.assetid: FF1929EE-4A2D-4761-8919-488369FAEE1F
title: Metodo SetScrollPosition della classe Msvm_Ps2Mouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.SetScrollPosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ffec8e05acf2210c55038edde5def8373e900ed7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883026"
---
# <a name="setscrollposition-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="d4f39-103">Metodo SetScrollPosition della classe MSVM \_ Ps2mouse</span><span class="sxs-lookup"><span data-stu-id="d4f39-103">SetScrollPosition method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="d4f39-104">Regola la coordinata z del controllo rotellina del dispositivo di puntamento.</span><span class="sxs-lookup"><span data-stu-id="d4f39-104">Adjusts the z-coordinate of the wheel control of the pointing device.</span></span> <span data-ttu-id="d4f39-105">I valori scritti in questa proprietà sono sempre offset delle coordinate relative.</span><span class="sxs-lookup"><span data-stu-id="d4f39-105">Values written to this property are always relative coordinate offsets.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4f39-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d4f39-106">Syntax</span></span>


```mof
uint32 SetScrollPosition(
  [in] sint8 scrollPositionDelta
);
```



## <a name="parameters"></a><span data-ttu-id="d4f39-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d4f39-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4f39-108">*scrollPositionDelta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d4f39-108">*scrollPositionDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4f39-109">Tipo: **sint8**</span><span class="sxs-lookup"><span data-stu-id="d4f39-109">Type: **sint8**</span></span>

<span data-ttu-id="d4f39-110">Delta della posizione di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="d4f39-110">The delta of the scroll position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4f39-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d4f39-111">Return value</span></span>

<span data-ttu-id="d4f39-112">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d4f39-112">Type: **uint32**</span></span>

<span data-ttu-id="d4f39-113">Un valore restituito pari a zero indica esito positivo.</span><span class="sxs-lookup"><span data-stu-id="d4f39-113">A return value of zero indicates success.</span></span> <span data-ttu-id="d4f39-114">Un valore diverso da zero indica un errore di modifica della posizione di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="d4f39-114">A nonzero value indicates a failure to alter the scroll position.</span></span>

<dl> <dt>

<span data-ttu-id="d4f39-115">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="d4f39-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d4f39-116">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="d4f39-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d4f39-117">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="d4f39-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="d4f39-118">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="d4f39-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d4f39-119">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="d4f39-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="d4f39-120">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="d4f39-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="d4f39-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="d4f39-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="d4f39-122">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="d4f39-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d4f39-123">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="d4f39-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="d4f39-124">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="d4f39-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d4f39-125">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="d4f39-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="d4f39-126">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="d4f39-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="d4f39-127">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="d4f39-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="d4f39-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="d4f39-128">Remarks</span></span>

<span data-ttu-id="d4f39-129">L'accesso alla [**classe \_ Ps2Mouse di MSVM**](msvm-ps2mouse.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="d4f39-129">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d4f39-130">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d4f39-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4f39-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4f39-131">Requirements</span></span>



| <span data-ttu-id="d4f39-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4f39-132">Requirement</span></span> | <span data-ttu-id="d4f39-133">Valore</span><span class="sxs-lookup"><span data-stu-id="d4f39-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4f39-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4f39-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d4f39-135">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d4f39-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d4f39-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d4f39-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d4f39-137">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d4f39-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d4f39-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d4f39-138">Namespace</span></span><br/>                | <span data-ttu-id="d4f39-139">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="d4f39-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d4f39-140">MOF</span><span class="sxs-lookup"><span data-stu-id="d4f39-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d4f39-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d4f39-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d4f39-142">DLL</span><span class="sxs-lookup"><span data-stu-id="d4f39-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4f39-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d4f39-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d4f39-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d4f39-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4f39-145">**\_Ps2Mouse MSVM**</span><span class="sxs-lookup"><span data-stu-id="d4f39-145">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 


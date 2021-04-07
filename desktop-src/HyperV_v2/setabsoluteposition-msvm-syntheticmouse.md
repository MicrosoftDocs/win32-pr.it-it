---
description: Imposta la posizione orizzontale e verticale del cursore del mouse.
ms.assetid: 7845E10A-7F61-4134-BF81-AED5483F36AD
title: Metodo SetAbsolutePosition della classe Msvm_SyntheticMouse (Dbdao. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.SetAbsolutePosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4b8ffb3a4d415f76dedf30acba5869b4cc585eb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881533"
---
# <a name="setabsoluteposition-method-of-the-msvm_syntheticmouse-class"></a><span data-ttu-id="089e8-103">Metodo SetAbsolutePosition della classe MSVM \_ SyntheticMouse</span><span class="sxs-lookup"><span data-stu-id="089e8-103">SetAbsolutePosition method of the Msvm\_SyntheticMouse class</span></span>

<span data-ttu-id="089e8-104">Imposta la posizione orizzontale e verticale del cursore del mouse.</span><span class="sxs-lookup"><span data-stu-id="089e8-104">Sets the horizontal and vertical position of the mouse cursor.</span></span>

## <a name="syntax"></a><span data-ttu-id="089e8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="089e8-105">Syntax</span></span>


```mof
uint32 SetAbsolutePosition(
  [in] sint32 horizontalPosition,
  [in] sint32 verticalPosition
);
```



## <a name="parameters"></a><span data-ttu-id="089e8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="089e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="089e8-107">*horizontalPosition* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="089e8-107">*horizontalPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="089e8-108">Tipo: **sint32**</span><span class="sxs-lookup"><span data-stu-id="089e8-108">Type: **sint32**</span></span>

<span data-ttu-id="089e8-109">Nuova posizione orizzontale del cursore del mouse, in pixel.</span><span class="sxs-lookup"><span data-stu-id="089e8-109">The new horizontal position of the mouse cursor, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="089e8-110">*verticalPosition* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="089e8-110">*verticalPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="089e8-111">Tipo: **sint32**</span><span class="sxs-lookup"><span data-stu-id="089e8-111">Type: **sint32**</span></span>

<span data-ttu-id="089e8-112">Nuova posizione verticale del cursore del mouse, in pixel.</span><span class="sxs-lookup"><span data-stu-id="089e8-112">The new vertical position of the mouse cursor, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="089e8-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="089e8-113">Return value</span></span>

<span data-ttu-id="089e8-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="089e8-114">Type: **uint32**</span></span>

<span data-ttu-id="089e8-115">Un valore restituito pari a zero indica esito positivo.</span><span class="sxs-lookup"><span data-stu-id="089e8-115">A return value of zero indicates success.</span></span> <span data-ttu-id="089e8-116">Un valore diverso da zero indica un errore di modifica della posizione di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="089e8-116">A nonzero value indicates a failure to alter the scroll position.</span></span>

<dl> <dt>

<span data-ttu-id="089e8-117">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="089e8-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="089e8-118">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="089e8-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="089e8-119">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="089e8-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="089e8-120">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="089e8-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="089e8-121">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="089e8-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="089e8-122">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="089e8-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="089e8-123">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="089e8-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="089e8-124">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="089e8-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="089e8-125">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="089e8-125">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="089e8-126">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="089e8-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="089e8-127">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="089e8-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="089e8-128">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="089e8-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="089e8-129">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="089e8-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="089e8-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="089e8-130">Remarks</span></span>

<span data-ttu-id="089e8-131">L'accesso alla [**classe \_ SyntheticMouse di MSVM**](msvm-syntheticmouse.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="089e8-131">Access to the [**Msvm\_SyntheticMouse**](msvm-syntheticmouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="089e8-132">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="089e8-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="089e8-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="089e8-133">Requirements</span></span>



| <span data-ttu-id="089e8-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="089e8-134">Requirement</span></span> | <span data-ttu-id="089e8-135">Valore</span><span class="sxs-lookup"><span data-stu-id="089e8-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="089e8-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="089e8-136">Minimum supported client</span></span><br/> | <span data-ttu-id="089e8-137">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="089e8-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="089e8-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="089e8-138">Minimum supported server</span></span><br/> | <span data-ttu-id="089e8-139">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="089e8-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="089e8-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="089e8-140">Namespace</span></span><br/>                | <span data-ttu-id="089e8-141">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="089e8-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="089e8-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="089e8-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="089e8-143"><dt>DbDao. h</dt></span><span class="sxs-lookup"><span data-stu-id="089e8-143"><dt>Dbdao.h</dt></span></span> </dl>                      |
| <span data-ttu-id="089e8-144">MOF</span><span class="sxs-lookup"><span data-stu-id="089e8-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="089e8-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="089e8-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="089e8-146">DLL</span><span class="sxs-lookup"><span data-stu-id="089e8-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="089e8-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="089e8-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="089e8-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="089e8-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="089e8-149">**\_SyntheticMouse MSVM**</span><span class="sxs-lookup"><span data-stu-id="089e8-149">**Msvm\_SyntheticMouse**</span></span>](msvm-syntheticmouse.md)
</dt> </dl>

 


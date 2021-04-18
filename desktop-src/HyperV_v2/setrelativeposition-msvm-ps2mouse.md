---
description: Compensa la posizione del puntatore del mouse in base ai Delta orizzontali e verticali specificati.
ms.assetid: C74E4BEA-C7E1-44C7-B4FC-8926F23DF1FE
title: Metodo SetRelativePosition della classe Msvm_Ps2Mouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.SetRelativePosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b7f4d10f48bce4b33cd4965f08633b85b5a738bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314320"
---
# <a name="setrelativeposition-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="de2eb-103">Metodo SetRelativePosition della classe MSVM \_ Ps2mouse</span><span class="sxs-lookup"><span data-stu-id="de2eb-103">SetRelativePosition method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="de2eb-104">Compensa la posizione del puntatore del mouse in base ai Delta orizzontali e verticali specificati.</span><span class="sxs-lookup"><span data-stu-id="de2eb-104">Offsets the position of the mouse pointer by the specified horizontal and vertical deltas.</span></span>

## <a name="syntax"></a><span data-ttu-id="de2eb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="de2eb-105">Syntax</span></span>


```mof
uint32 SetRelativePosition(
  [in] sint8 horizontalDelta,
  [in] sint8 verticalDelta
);
```



## <a name="parameters"></a><span data-ttu-id="de2eb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="de2eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de2eb-107">*horizontalDelta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de2eb-107">*horizontalDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de2eb-108">Tipo: **sint8**</span><span class="sxs-lookup"><span data-stu-id="de2eb-108">Type: **sint8**</span></span>

<span data-ttu-id="de2eb-109">Modifica orizzontale della posizione del mouse, in pixel.</span><span class="sxs-lookup"><span data-stu-id="de2eb-109">The horizontal change for the mouse position, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="de2eb-110">*verticalDelta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="de2eb-110">*verticalDelta* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de2eb-111">Tipo: **sint8**</span><span class="sxs-lookup"><span data-stu-id="de2eb-111">Type: **sint8**</span></span>

<span data-ttu-id="de2eb-112">Modifica verticale della posizione del mouse, in pixel.</span><span class="sxs-lookup"><span data-stu-id="de2eb-112">The vertical change for the mouse position, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de2eb-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="de2eb-113">Return value</span></span>

<span data-ttu-id="de2eb-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="de2eb-114">Type: **uint32**</span></span>

<span data-ttu-id="de2eb-115">Un valore restituito pari a zero indica esito positivo.</span><span class="sxs-lookup"><span data-stu-id="de2eb-115">A return value of zero indicates success.</span></span> <span data-ttu-id="de2eb-116">Un valore diverso da zero indica un errore di modifica della posizione del mouse.</span><span class="sxs-lookup"><span data-stu-id="de2eb-116">A nonzero value indicates a failure to alter the mouse position.</span></span>

<dl> <dt>

<span data-ttu-id="de2eb-117">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="de2eb-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="de2eb-118">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="de2eb-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="de2eb-119">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="de2eb-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="de2eb-120">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="de2eb-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="de2eb-121">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="de2eb-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="de2eb-122">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="de2eb-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="de2eb-123">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="de2eb-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="de2eb-124">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="de2eb-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="de2eb-125">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="de2eb-125">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="de2eb-126">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="de2eb-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="de2eb-127">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="de2eb-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="de2eb-128">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="de2eb-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="de2eb-129">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="de2eb-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="de2eb-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="de2eb-130">Remarks</span></span>

<span data-ttu-id="de2eb-131">L'accesso alla [**classe \_ Ps2Mouse di MSVM**](msvm-ps2mouse.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="de2eb-131">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="de2eb-132">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="de2eb-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="de2eb-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de2eb-133">Requirements</span></span>



| <span data-ttu-id="de2eb-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="de2eb-134">Requirement</span></span> | <span data-ttu-id="de2eb-135">Valore</span><span class="sxs-lookup"><span data-stu-id="de2eb-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de2eb-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de2eb-136">Minimum supported client</span></span><br/> | <span data-ttu-id="de2eb-137">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="de2eb-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="de2eb-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de2eb-138">Minimum supported server</span></span><br/> | <span data-ttu-id="de2eb-139">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="de2eb-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="de2eb-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="de2eb-140">Namespace</span></span><br/>                | <span data-ttu-id="de2eb-141">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="de2eb-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="de2eb-142">MOF</span><span class="sxs-lookup"><span data-stu-id="de2eb-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de2eb-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="de2eb-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="de2eb-144">DLL</span><span class="sxs-lookup"><span data-stu-id="de2eb-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de2eb-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="de2eb-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="de2eb-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de2eb-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de2eb-147">**\_Ps2Mouse MSVM**</span><span class="sxs-lookup"><span data-stu-id="de2eb-147">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 


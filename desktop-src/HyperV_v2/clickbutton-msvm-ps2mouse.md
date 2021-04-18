---
description: Simula un clic del pulsante del dispositivo specificato.
ms.assetid: 77CFA2E9-E422-464C-B124-6F7D3D56BA4C
title: Metodo ClickButton della classe Msvm_Ps2Mouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.ClickButton
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ffaded2a5e9a8e4e37a158e3aa91b27520dff2b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310545"
---
# <a name="clickbutton-method-of-the-msvm_ps2mouse-class"></a><span data-ttu-id="46245-103">Metodo ClickButton della classe MSVM \_ Ps2mouse</span><span class="sxs-lookup"><span data-stu-id="46245-103">ClickButton method of the Msvm\_Ps2Mouse class</span></span>

<span data-ttu-id="46245-104">Simula un clic del pulsante del dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="46245-104">Simulates a click of the specified device button.</span></span> <span data-ttu-id="46245-105">Questa operazione equivale a chiamare due volte [**SetButtonState**](setbuttonstate-msvm-syntheticmouse.md) , prima di tutto per premere il pulsante e di nuovo per rilasciarlo.</span><span class="sxs-lookup"><span data-stu-id="46245-105">This is equivalent to calling [**SetButtonState**](setbuttonstate-msvm-syntheticmouse.md) twice, first to press the button, and again to release it.</span></span>

## <a name="syntax"></a><span data-ttu-id="46245-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46245-106">Syntax</span></span>


```mof
uint32 ClickButton(
  [in] uint32 buttonIndex
);
```



## <a name="parameters"></a><span data-ttu-id="46245-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="46245-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46245-108">*ButtonIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46245-108">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46245-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46245-109">Type: **uint32**</span></span>

<span data-ttu-id="46245-110">Indice in base 1 del pulsante.</span><span class="sxs-lookup"><span data-stu-id="46245-110">The 1-based index of the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46245-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46245-111">Return value</span></span>

<span data-ttu-id="46245-112">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46245-112">Type: **uint32**</span></span>

<span data-ttu-id="46245-113">Un valore restituito pari a zero indica esito positivo.</span><span class="sxs-lookup"><span data-stu-id="46245-113">A return value of zero indicates success.</span></span> <span data-ttu-id="46245-114">Un valore diverso da zero indica un errore di modifica dello stato del pulsante.</span><span class="sxs-lookup"><span data-stu-id="46245-114">A nonzero value indicates a failure to modify the button state.</span></span>

<dl> <dt>

<span data-ttu-id="46245-115">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="46245-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="46245-116">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="46245-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="46245-117">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="46245-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="46245-118">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="46245-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="46245-119">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="46245-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="46245-120">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="46245-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="46245-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="46245-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="46245-122">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="46245-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="46245-123">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="46245-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="46245-124">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="46245-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="46245-125">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="46245-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="46245-126">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="46245-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="46245-127">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="46245-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="46245-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="46245-128">Remarks</span></span>

<span data-ttu-id="46245-129">L'accesso alla [**classe \_ Ps2Mouse di MSVM**](msvm-ps2mouse.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="46245-129">Access to the [**Msvm\_Ps2Mouse**](msvm-ps2mouse.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="46245-130">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="46245-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="46245-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46245-131">Requirements</span></span>



| <span data-ttu-id="46245-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="46245-132">Requirement</span></span> | <span data-ttu-id="46245-133">Valore</span><span class="sxs-lookup"><span data-stu-id="46245-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46245-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46245-134">Minimum supported client</span></span><br/> | <span data-ttu-id="46245-135">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="46245-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="46245-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46245-136">Minimum supported server</span></span><br/> | <span data-ttu-id="46245-137">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="46245-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="46245-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="46245-138">Namespace</span></span><br/>                | <span data-ttu-id="46245-139">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="46245-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="46245-140">MOF</span><span class="sxs-lookup"><span data-stu-id="46245-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46245-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="46245-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="46245-142">DLL</span><span class="sxs-lookup"><span data-stu-id="46245-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46245-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="46245-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="46245-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46245-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46245-145">**\_Ps2Mouse MSVM**</span><span class="sxs-lookup"><span data-stu-id="46245-145">**Msvm\_Ps2Mouse**</span></span>](msvm-ps2mouse.md)
</dt> </dl>

 


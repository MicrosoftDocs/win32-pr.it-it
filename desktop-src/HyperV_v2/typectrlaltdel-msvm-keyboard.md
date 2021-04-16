---
description: Simula una sequenza di tasti CTRL + ALT + CANC.
ms.assetid: C24C9C42-844F-4560-B8C1-0054F5E913D6
title: Metodo TypeCtrlAltDel della classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeCtrlAltDel
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 64ebc4bddf8adccd7098cafed1df43d1cf1cb4eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348171"
---
# <a name="typectrlaltdel-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="40098-103">Metodo TypeCtrlAltDel della classe della \_ tastiera MSVM</span><span class="sxs-lookup"><span data-stu-id="40098-103">TypeCtrlAltDel method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="40098-104">Simula una sequenza di tasti CTRL + ALT + CANC.</span><span class="sxs-lookup"><span data-stu-id="40098-104">Simulates a Ctrl+Alt+Del key sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="40098-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="40098-105">Syntax</span></span>


```mof
uint32 TypeCtrlAltDel();
```



## <a name="parameters"></a><span data-ttu-id="40098-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="40098-106">Parameters</span></span>

<span data-ttu-id="40098-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="40098-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="40098-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="40098-108">Return value</span></span>

<span data-ttu-id="40098-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="40098-109">Type: **uint32**</span></span>

<span data-ttu-id="40098-110">Un valore restituito pari a zero indica esito positivo.</span><span class="sxs-lookup"><span data-stu-id="40098-110">A return value of zero indicates success.</span></span> <span data-ttu-id="40098-111">Un valore diverso da zero indica un errore di invio.</span><span class="sxs-lookup"><span data-stu-id="40098-111">A nonzero value indicates a failure to send.</span></span>

<dl> <dt>

<span data-ttu-id="40098-112">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="40098-112">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="40098-113">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="40098-113">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="40098-114">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="40098-114">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="40098-115">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="40098-115">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="40098-116">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="40098-116">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="40098-117">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="40098-117">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="40098-118">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="40098-118">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="40098-119">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="40098-119">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="40098-120">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="40098-120">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="40098-121">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="40098-121">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="40098-122">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="40098-122">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="40098-123">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="40098-123">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="40098-124">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="40098-124">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="40098-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="40098-125">Remarks</span></span>

<span data-ttu-id="40098-126">L'accesso alla classe della [**\_ tastiera MSVM**](msvm-keyboard.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="40098-126">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="40098-127">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="40098-127">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="40098-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40098-128">Requirements</span></span>



| <span data-ttu-id="40098-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="40098-129">Requirement</span></span> | <span data-ttu-id="40098-130">Valore</span><span class="sxs-lookup"><span data-stu-id="40098-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40098-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40098-131">Minimum supported client</span></span><br/> | <span data-ttu-id="40098-132">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="40098-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="40098-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40098-133">Minimum supported server</span></span><br/> | <span data-ttu-id="40098-134">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="40098-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="40098-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="40098-135">Namespace</span></span><br/>                | <span data-ttu-id="40098-136">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="40098-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="40098-137">MOF</span><span class="sxs-lookup"><span data-stu-id="40098-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40098-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="40098-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="40098-139">DLL</span><span class="sxs-lookup"><span data-stu-id="40098-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40098-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="40098-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="40098-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40098-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40098-142">**\_Tastiera MSVM**</span><span class="sxs-lookup"><span data-stu-id="40098-142">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 


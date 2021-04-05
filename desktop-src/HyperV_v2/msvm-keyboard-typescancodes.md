---
description: Simula una sequenza di chiavi usando i codici di analisi.
ms.assetid: F67D2FBA-3CE0-4135-9043-FAB59381DE3C
title: Metodo TypeScancodes della classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeScancodes
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 97479a1a0926894f72472b7459f77cd9325ac6fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752359"
---
# <a name="typescancodes-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="d2d91-103">Metodo TypeScancodes della classe della \_ tastiera MSVM</span><span class="sxs-lookup"><span data-stu-id="d2d91-103">TypeScancodes method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="d2d91-104">Simula una sequenza di chiavi usando i codici di analisi.</span><span class="sxs-lookup"><span data-stu-id="d2d91-104">Simulates a key sequence using scan codes.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2d91-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2d91-105">Syntax</span></span>


```mof
uint32 TypeScancodes(
  [in] uint8 Scancodes[]
);
```



## <a name="parameters"></a><span data-ttu-id="d2d91-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d2d91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2d91-107">*Scancode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d2d91-107">*Scancodes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2d91-108">Tipo: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="d2d91-108">Type: **uint8\[\]**</span></span>

<span data-ttu-id="d2d91-109">Matrice che contiene i codici di analisi da digitare.</span><span class="sxs-lookup"><span data-stu-id="d2d91-109">An array that contains the scan codes to type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2d91-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d2d91-110">Return value</span></span>

<span data-ttu-id="d2d91-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d2d91-111">Type: **uint32**</span></span>

<span data-ttu-id="d2d91-112">Questo metodo restituisce 0 se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="d2d91-112">This method returns 0 if it succeeds.</span></span> <span data-ttu-id="d2d91-113">Qualsiasi altro valore restituito indica un errore.</span><span class="sxs-lookup"><span data-stu-id="d2d91-113">Any other return value indicates an error.</span></span> <span data-ttu-id="d2d91-114">Il valore restituito può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d2d91-114">The return value can be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d2d91-115">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="d2d91-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d2d91-116">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="d2d91-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d2d91-117">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="d2d91-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="d2d91-118">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="d2d91-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d2d91-119">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="d2d91-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="d2d91-120">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="d2d91-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="d2d91-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="d2d91-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="d2d91-122">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="d2d91-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d2d91-123">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="d2d91-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="d2d91-124">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="d2d91-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d2d91-125">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="d2d91-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="d2d91-126">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="d2d91-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="d2d91-127">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="d2d91-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="d2d91-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2d91-128">Remarks</span></span>

<span data-ttu-id="d2d91-129">L'accesso alla classe della [**\_ tastiera MSVM**](msvm-keyboard.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="d2d91-129">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d2d91-130">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d2d91-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="d2d91-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2d91-131">Requirements</span></span>



| <span data-ttu-id="d2d91-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2d91-132">Requirement</span></span> | <span data-ttu-id="d2d91-133">Valore</span><span class="sxs-lookup"><span data-stu-id="d2d91-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2d91-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2d91-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d2d91-135">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d2d91-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d2d91-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2d91-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d2d91-137">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d2d91-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d2d91-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d2d91-138">Namespace</span></span><br/>                | <span data-ttu-id="d2d91-139">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="d2d91-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d2d91-140">MOF</span><span class="sxs-lookup"><span data-stu-id="d2d91-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2d91-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2d91-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2d91-142">DLL</span><span class="sxs-lookup"><span data-stu-id="d2d91-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2d91-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d2d91-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d2d91-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2d91-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2d91-145">**\_Tastiera MSVM**</span><span class="sxs-lookup"><span data-stu-id="d2d91-145">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 


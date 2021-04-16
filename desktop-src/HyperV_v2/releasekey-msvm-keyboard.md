---
description: Simula una versione della chiave.
ms.assetid: EAE84BD5-ECEA-44E7-A7AB-CD18299DF2FE
title: Metodo ReleaseKey della classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.ReleaseKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2193a4b78128ff3f65e98b4425528a51f6cf5916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530102"
---
# <a name="releasekey-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="15d34-103">Metodo ReleaseKey della classe della \_ tastiera MSVM</span><span class="sxs-lookup"><span data-stu-id="15d34-103">ReleaseKey method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="15d34-104">Simula una versione della chiave.</span><span class="sxs-lookup"><span data-stu-id="15d34-104">Simulates a key release.</span></span> <span data-ttu-id="15d34-105">In caso di esito positivo, la chiave sarà nello stato attivo.</span><span class="sxs-lookup"><span data-stu-id="15d34-105">When successful, the key will be in the up state.</span></span>

## <a name="syntax"></a><span data-ttu-id="15d34-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15d34-106">Syntax</span></span>


```mof
uint32 ReleaseKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a><span data-ttu-id="15d34-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="15d34-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15d34-108">*codice* \[ di stato in\]</span><span class="sxs-lookup"><span data-stu-id="15d34-108">*keyCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15d34-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="15d34-109">Type: **uint32**</span></span>

<span data-ttu-id="15d34-110">Codice chiave virtuale della chiave da rilasciare.</span><span class="sxs-lookup"><span data-stu-id="15d34-110">The virtual key code of the key to release.</span></span> <span data-ttu-id="15d34-111">Per l'elenco dei codici delle chiavi virtuali, vedere [**codici a chiave virtuale**](../inputdev/virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="15d34-111">For the list for virtual-key codes, see [**Virtual-Key Codes**](../inputdev/virtual-key-codes.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15d34-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="15d34-112">Return value</span></span>

<span data-ttu-id="15d34-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="15d34-113">Type: **uint32**</span></span>

<span data-ttu-id="15d34-114">Un valore restituito pari a zero indica esito positivo.</span><span class="sxs-lookup"><span data-stu-id="15d34-114">A return value of zero indicates success.</span></span> <span data-ttu-id="15d34-115">Un valore diverso da zero indica un errore di modifica dello stato della chiave.</span><span class="sxs-lookup"><span data-stu-id="15d34-115">A nonzero value indicates a failure to modify the key state.</span></span>

<dl> <dt>

<span data-ttu-id="15d34-116">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="15d34-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="15d34-117">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="15d34-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="15d34-118">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="15d34-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="15d34-119">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="15d34-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="15d34-120">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="15d34-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="15d34-121">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="15d34-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="15d34-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="15d34-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="15d34-123">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="15d34-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="15d34-124">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="15d34-124">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="15d34-125">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="15d34-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="15d34-126">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="15d34-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="15d34-127">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="15d34-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="15d34-128">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="15d34-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="15d34-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="15d34-129">Remarks</span></span>

<span data-ttu-id="15d34-130">Il metodo **ReleaseKey** esegue il mapping dei riferimenti al **\_ menu VK** (18), al **\_ controllo VK** (17) e al **\_ passaggio VK** (16) a **VK \_ LMENU** (164), **VK \_ LCONTROL** (162) e **VK \_ LSHIFT** (160), rispettivamente, perché i codici della chiave virtuale del **\_ menu VK**, del **\_ controllo** VK e del **VK \_ Shift** non rappresentano chiavi reali su una tastiera.</span><span class="sxs-lookup"><span data-stu-id="15d34-130">The **ReleaseKey** method maps references to the **VK\_MENU** (18), **VK\_CONTROL** (17), and **VK\_SHIFT** (16) to **VK\_LMENU** (164), **VK\_LCONTROL** (162), and **VK\_LSHIFT** (160), respectively, because the **VK\_MENU**, **VK\_CONTROL**, and **VK\_SHIFT** virtual key codes do not represent real keys on a keyboard.</span></span>

<span data-ttu-id="15d34-131">L'accesso alla classe della [**\_ tastiera MSVM**](msvm-keyboard.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="15d34-131">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="15d34-132">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="15d34-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="15d34-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15d34-133">Requirements</span></span>



| <span data-ttu-id="15d34-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="15d34-134">Requirement</span></span> | <span data-ttu-id="15d34-135">Valore</span><span class="sxs-lookup"><span data-stu-id="15d34-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15d34-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15d34-136">Minimum supported client</span></span><br/> | <span data-ttu-id="15d34-137">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="15d34-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="15d34-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15d34-138">Minimum supported server</span></span><br/> | <span data-ttu-id="15d34-139">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="15d34-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="15d34-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="15d34-140">Namespace</span></span><br/>                | <span data-ttu-id="15d34-141">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="15d34-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="15d34-142">MOF</span><span class="sxs-lookup"><span data-stu-id="15d34-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15d34-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15d34-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="15d34-144">DLL</span><span class="sxs-lookup"><span data-stu-id="15d34-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15d34-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="15d34-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="15d34-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15d34-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15d34-147">**\_Tastiera MSVM**</span><span class="sxs-lookup"><span data-stu-id="15d34-147">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> <dt>

[<span data-ttu-id="15d34-148">**Codici chiave virtuale**</span><span class="sxs-lookup"><span data-stu-id="15d34-148">**Virtual-Key Codes**</span></span>](../inputdev/virtual-key-codes.md)
</dt> </dl>

 


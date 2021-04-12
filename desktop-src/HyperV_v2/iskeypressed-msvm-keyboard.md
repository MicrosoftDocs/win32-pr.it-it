---
description: Recupera lo stato della chiave di una chiave.
ms.assetid: 4AEB732D-274E-42BB-AA97-9E4D30B81338
title: Metodo KeyPressed della classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.IsKeyPressed
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 44af7a3dc82c0d4d20a2e4c6aff21f7a47837490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226625"
---
# <a name="iskeypressed-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="a50fb-103">Metodo KeyPressed della \_ classe della tastiera MSVM</span><span class="sxs-lookup"><span data-stu-id="a50fb-103">IsKeyPressed method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="a50fb-104">Recupera lo stato della chiave di una chiave.</span><span class="sxs-lookup"><span data-stu-id="a50fb-104">Retrieves the key state of a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="a50fb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a50fb-105">Syntax</span></span>


```mof
uint32 IsKeyPressed(
  [in]  uint32  keyCode,
  [out] boolean keyState
);
```



## <a name="parameters"></a><span data-ttu-id="a50fb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a50fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a50fb-107">*codice* \[ di stato in\]</span><span class="sxs-lookup"><span data-stu-id="a50fb-107">*keyCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a50fb-108">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a50fb-108">Type: **uint32**</span></span>

<span data-ttu-id="a50fb-109">Codice della chiave virtuale della chiave su cui eseguire la query.</span><span class="sxs-lookup"><span data-stu-id="a50fb-109">The virtual key code of the key to query.</span></span> <span data-ttu-id="a50fb-110">Per l'elenco dei codici delle chiavi virtuali, vedere [**codici a chiave virtuale**](../inputdev/virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a50fb-110">For the list for virtual-key codes, see [**Virtual-Key Codes**](../inputdev/virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="a50fb-111">*stato* \[ della pagina out\]</span><span class="sxs-lookup"><span data-stu-id="a50fb-111">*keyState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a50fb-112">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a50fb-112">Type: **boolean**</span></span>

<span data-ttu-id="a50fb-113">Stato di inattività corrente della chiave.</span><span class="sxs-lookup"><span data-stu-id="a50fb-113">The current down state of the key.</span></span> <span data-ttu-id="a50fb-114">Un valore **true** indica che la chiave è inattiva.</span><span class="sxs-lookup"><span data-stu-id="a50fb-114">A **True** value means the key is down.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a50fb-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a50fb-115">Return value</span></span>

<span data-ttu-id="a50fb-116">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a50fb-116">Type: **uint32**</span></span>

<span data-ttu-id="a50fb-117">Un valore restituito pari a zero indica esito positivo.</span><span class="sxs-lookup"><span data-stu-id="a50fb-117">A return value of zero indicates success.</span></span> <span data-ttu-id="a50fb-118">Un valore diverso da zero indica un errore di query sullo stato della chiave.</span><span class="sxs-lookup"><span data-stu-id="a50fb-118">A nonzero value indicates a failure to query the key state.</span></span>

<dl> <dt>

<span data-ttu-id="a50fb-119">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="a50fb-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a50fb-120">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="a50fb-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a50fb-121">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="a50fb-121">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a50fb-122">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="a50fb-122">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a50fb-123">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="a50fb-123">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a50fb-124">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="a50fb-124">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a50fb-125">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="a50fb-125">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a50fb-126">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="a50fb-126">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a50fb-127">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="a50fb-127">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a50fb-128">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="a50fb-128">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a50fb-129">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="a50fb-129">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a50fb-130">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="a50fb-130">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a50fb-131">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="a50fb-131">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="a50fb-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="a50fb-132">Remarks</span></span>

<span data-ttu-id="a50fb-133">Il metodo **keypressed** restituirà sempre **false** per il **\_ menu VK** (18), il **\_ controllo VK** (17) e lo **\_ spostamento VK** (16) perché non si tratta di chiavi reali su una tastiera.</span><span class="sxs-lookup"><span data-stu-id="a50fb-133">The **IsKeyPressed** method will always return **False** for the **VK\_MENU** (18), **VK\_CONTROL** (17), and **VK\_SHIFT** (16) because these are not real keys on a keyboard.</span></span> <span data-ttu-id="a50fb-134">A questi codici delle chiavi virtuali viene sempre eseguito il mapping a **VK \_ LMENU** (164), **VK \_ LCONTROL** (162) e **VK \_ LSHIFT** (160) rispettivamente dai metodi [**pulsanteper**](presskey-msvm-keyboard.md) e [**ReleaseKey**](releasekey-msvm-keyboard.md) .</span><span class="sxs-lookup"><span data-stu-id="a50fb-134">These virtual key codes are always mapped to **VK\_LMENU** (164), **VK\_LCONTROL** (162), and **VK\_LSHIFT** (160), respectively, by the [**PressKey**](presskey-msvm-keyboard.md) and [**ReleaseKey**](releasekey-msvm-keyboard.md) methods.</span></span>

<span data-ttu-id="a50fb-135">L'accesso alla classe della [**\_ tastiera MSVM**](msvm-keyboard.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="a50fb-135">Access to the [**Msvm\_Keyboard**](msvm-keyboard.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a50fb-136">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a50fb-136">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a50fb-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a50fb-137">Requirements</span></span>



| <span data-ttu-id="a50fb-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="a50fb-138">Requirement</span></span> | <span data-ttu-id="a50fb-139">Valore</span><span class="sxs-lookup"><span data-stu-id="a50fb-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a50fb-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a50fb-140">Minimum supported client</span></span><br/> | <span data-ttu-id="a50fb-141">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a50fb-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a50fb-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a50fb-142">Minimum supported server</span></span><br/> | <span data-ttu-id="a50fb-143">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a50fb-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a50fb-144">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a50fb-144">Namespace</span></span><br/>                | <span data-ttu-id="a50fb-145">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="a50fb-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a50fb-146">MOF</span><span class="sxs-lookup"><span data-stu-id="a50fb-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a50fb-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a50fb-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a50fb-148">DLL</span><span class="sxs-lookup"><span data-stu-id="a50fb-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a50fb-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a50fb-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a50fb-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a50fb-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a50fb-151">**\_Tastiera MSVM**</span><span class="sxs-lookup"><span data-stu-id="a50fb-151">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> <dt>

[<span data-ttu-id="a50fb-152">**Codici chiave virtuale**</span><span class="sxs-lookup"><span data-stu-id="a50fb-152">**Virtual-Key Codes**</span></span>](../inputdev/virtual-key-codes.md)
</dt> </dl>

 


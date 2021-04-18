---
description: Genera un set di nomi di porta universali (WWPNs).
ms.assetid: 36f393eb-6f34-4ae3-a976-c5da60211f3e
title: Metodo GenerateWwpn della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GenerateWwpn
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b0efba6a24a7e4f7e6826f91930cb69b4b54f3cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307757"
---
# <a name="generatewwpn-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="e69d7-103">Metodo GenerateWwpn della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="e69d7-103">GenerateWwpn method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="e69d7-104">Genera un set di nomi di porta universali (WWPNs).</span><span class="sxs-lookup"><span data-stu-id="e69d7-104">Generates a set of World Wide Port Names (WWPNs).</span></span> <span data-ttu-id="e69d7-105">I WWPNs vengono generati dall'interno dell'intervallo preconfigurato definito dalle proprietà **MinimumWWPNAddress** e **MaximumWWPNAddress** della classe [**MSVM \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="e69d7-105">The WWPNs are generated from within the pre-configured range defined by the **MinimumWWPNAddress** and **MaximumWWPNAddress** properties of the [**Msvm\_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) class.</span></span> <span data-ttu-id="e69d7-106">Se il numero valido di WWPNs che è possibile generare è inferiore al numero richiesto, le voci rimanenti nella matrice *GeneratedWwpn* avranno la voce non valida "0000000000000000" e il valore restituito indicherà l'esito positivo (0).</span><span class="sxs-lookup"><span data-stu-id="e69d7-106">If the valid number of WWPNs that can be generated is less than the requested number, then the remaining entries in the *GeneratedWwpn* array will have the invalid entry of "0000000000000000" and the return value will indicate success (0).</span></span>

## <a name="syntax"></a><span data-ttu-id="e69d7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e69d7-107">Syntax</span></span>


```mof
uint32 GenerateWwpn(
  [in]  uint32 NumberOfWwpns,
  [out] string GeneratedWwpn[]
);
```



## <a name="parameters"></a><span data-ttu-id="e69d7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e69d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e69d7-109">*NumberOfWwpns* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e69d7-109">*NumberOfWwpns* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e69d7-110">Numero di WWPNs da generare.</span><span class="sxs-lookup"><span data-stu-id="e69d7-110">The number of WWPNs to be generated.</span></span>

</dd> <dt>

<span data-ttu-id="e69d7-111">*GeneratedWwpn* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e69d7-111">*GeneratedWwpn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e69d7-112">Matrice di stringhe, ognuna delle quali conterrà un WWPN generato.</span><span class="sxs-lookup"><span data-stu-id="e69d7-112">An array of strings, each of which will contain a generated WWPN.</span></span> <span data-ttu-id="e69d7-113">Verrà formattato in formato stringa come "01:23:45:67:89: AB: CD: EF".</span><span class="sxs-lookup"><span data-stu-id="e69d7-113">It will be formatted in string form as "01:23:45:67:89:ab:cd:ef".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e69d7-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e69d7-114">Return value</span></span>

<span data-ttu-id="e69d7-115">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="e69d7-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e69d7-116">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="e69d7-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e69d7-117">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="e69d7-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e69d7-118">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="e69d7-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e69d7-119">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="e69d7-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e69d7-120">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="e69d7-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e69d7-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="e69d7-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e69d7-122">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="e69d7-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e69d7-123">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="e69d7-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e69d7-124">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="e69d7-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e69d7-125">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="e69d7-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e69d7-126">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="e69d7-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e69d7-127">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="e69d7-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e69d7-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e69d7-128">Requirements</span></span>



| <span data-ttu-id="e69d7-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e69d7-129">Requirement</span></span> | <span data-ttu-id="e69d7-130">Valore</span><span class="sxs-lookup"><span data-stu-id="e69d7-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e69d7-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e69d7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e69d7-132">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e69d7-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e69d7-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e69d7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e69d7-134">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e69d7-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e69d7-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e69d7-135">Namespace</span></span><br/>                | <span data-ttu-id="e69d7-136">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="e69d7-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e69d7-137">MOF</span><span class="sxs-lookup"><span data-stu-id="e69d7-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e69d7-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e69d7-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e69d7-139">DLL</span><span class="sxs-lookup"><span data-stu-id="e69d7-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e69d7-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e69d7-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e69d7-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e69d7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e69d7-142">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="e69d7-142">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 





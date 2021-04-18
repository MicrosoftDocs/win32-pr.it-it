---
description: Rimuove i parametri DH-CHAP (Diffie Hellman-Challenge Handshake Authentication Protocol) da una porta Fibre Channel sintetica in una macchina virtuale.
ms.assetid: f15673e2-287d-4e87-bee4-6c0f5f9178c8
title: Metodo RemoveFibreChannelChap della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveFibreChannelChap
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 06e944c3c592b0b61ace8a72b5d42a801ab0f5df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307872"
---
# <a name="removefibrechannelchap-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="c057e-103">Metodo RemoveFibreChannelChap della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="c057e-103">RemoveFibreChannelChap method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="c057e-104">Rimuove i parametri DH-CHAP (Diffie Hellman-Challenge Handshake Authentication Protocol) da una porta Fibre Channel sintetica in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="c057e-104">Removes DH-CHAP (Diffie Hellman - Challenge Handshake Authentication Protocol) parameters from a synthetic Fibre Channel port in a virtual machine.</span></span> <span data-ttu-id="c057e-105">Questo metodo avrà esito negativo se la macchina virtuale è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c057e-105">This method will fail if the virtual machine is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="c057e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c057e-106">Syntax</span></span>


```mof
uint32 RemoveFibreChannelChap(
  [in] string FcPortSettings[]
);
```



## <a name="parameters"></a><span data-ttu-id="c057e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c057e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c057e-108">*FcPortSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c057e-108">*FcPortSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c057e-109">Matrice di stringhe che contengono un'istanza incorporata della classe [**\_ SyntheticFcPortSettingData MSVM**](msvm-syntheticfcportsettingdata.md) che definiscono le porte sintetiche Fibre Channel per la rimozione dei parametri DH-CHAP da.</span><span class="sxs-lookup"><span data-stu-id="c057e-109">An array of strings that contain an embedded instance of the [**Msvm\_SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) class that define the synthetic Fibre Channel ports to remove the DH-CHAP parameters from.</span></span> <span data-ttu-id="c057e-110">La proprietà **InstanceID** di ognuna di queste istanze identifica gli elementi da modificare.</span><span class="sxs-lookup"><span data-stu-id="c057e-110">The **InstanceID** property of each of these instances identifies the elements to be modified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c057e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c057e-111">Return value</span></span>

<span data-ttu-id="c057e-112">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="c057e-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c057e-113">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="c057e-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c057e-114">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="c057e-114">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="c057e-115">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="c057e-115">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="c057e-116">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="c057e-116">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="c057e-117">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="c057e-117">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="c057e-118">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="c057e-118">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="c057e-119">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="c057e-119">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="c057e-120">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="c057e-120">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="c057e-121">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="c057e-121">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="c057e-122">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="c057e-122">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="c057e-123">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="c057e-123">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="c057e-124">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="c057e-124">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c057e-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c057e-125">Requirements</span></span>



| <span data-ttu-id="c057e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c057e-126">Requirement</span></span> | <span data-ttu-id="c057e-127">Valore</span><span class="sxs-lookup"><span data-stu-id="c057e-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c057e-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c057e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c057e-129">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c057e-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c057e-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c057e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c057e-131">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c057e-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c057e-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c057e-132">Namespace</span></span><br/>                | <span data-ttu-id="c057e-133">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c057e-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c057e-134">MOF</span><span class="sxs-lookup"><span data-stu-id="c057e-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c057e-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c057e-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c057e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c057e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c057e-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c057e-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c057e-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c057e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c057e-139">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="c057e-139">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 





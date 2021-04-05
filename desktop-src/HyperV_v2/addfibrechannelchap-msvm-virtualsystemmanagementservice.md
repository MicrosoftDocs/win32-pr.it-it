---
description: Aggiunge i parametri DH-CHAP (Diffie Hellman-Challenge Handshake Authentication Protocol) a una porta di Fibre Channel sintetica in una macchina virtuale.
ms.assetid: b9799ea4-f948-4b5c-bd18-1faa90213bb3
title: Metodo AddFibreChannelChap della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddFibreChannelChap
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 07151a902efa8f8077debc44bd732286c0a96a81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967558"
---
# <a name="addfibrechannelchap-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="dc224-103">Metodo AddFibreChannelChap della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="dc224-103">AddFibreChannelChap method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="dc224-104">Aggiunge i parametri DH-CHAP (Diffie Hellman-Challenge Handshake Authentication Protocol) a una porta di Fibre Channel sintetica in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dc224-104">Adds DH-CHAP (Diffie Hellman - Challenge Handshake Authentication Protocol) parameters to a synthetic Fibre Channel port on a virtual machine.</span></span> <span data-ttu-id="dc224-105">Questo metodo avrà esito negativo se la macchina virtuale è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="dc224-105">This method will fail if the virtual machine is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc224-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc224-106">Syntax</span></span>


```mof
uint32 AddFibreChannelChap(
  [in] string FcPortSettings[],
  [in] uint8  SecretEncoding,
  [in] uint8  SharedSecret[]
);
```



## <a name="parameters"></a><span data-ttu-id="dc224-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="dc224-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc224-108">*FcPortSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc224-108">*FcPortSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc224-109">Matrice di stringhe che contengono un'istanza incorporata della classe [**MSVM \_ SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) che descrive le impostazioni per le porte Fibre Channel sintetiche per le macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="dc224-109">An array of strings that contain an embedded instance of the [**Msvm\_SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) class that describes settings for synthetic Fibre Channel ports for virtual machines.</span></span> <span data-ttu-id="dc224-110">La proprietà **InstanceID** di ognuna di queste istanze identifica gli elementi da modificare.</span><span class="sxs-lookup"><span data-stu-id="dc224-110">The **InstanceID** property of each of these instances identifies the elements to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="dc224-111">*SecretEncoding* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc224-111">*SecretEncoding* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc224-112">Specifica il tipo di codifica per il segreto condiviso.</span><span class="sxs-lookup"><span data-stu-id="dc224-112">Specifies the type of encoding for the shared secret.</span></span>

<dt>

<span id="Printable_ASCII"></span><span id="printable_ascii"></span><span id="PRINTABLE_ASCII"></span>

<span data-ttu-id="dc224-113">**ASCII stampabile** (1)</span><span class="sxs-lookup"><span data-stu-id="dc224-113">**Printable ASCII** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Binary"></span><span id="binary"></span><span id="BINARY"></span>

<span data-ttu-id="dc224-114">**Binario** (2)</span><span class="sxs-lookup"><span data-stu-id="dc224-114">**Binary** (2)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="dc224-115">*SharedSecret* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc224-115">*SharedSecret* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc224-116">Specifica il segreto condiviso.</span><span class="sxs-lookup"><span data-stu-id="dc224-116">Specifies the shared secret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc224-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dc224-117">Return value</span></span>

<span data-ttu-id="dc224-118">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="dc224-118">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="dc224-119">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="dc224-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="dc224-120">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="dc224-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="dc224-121">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="dc224-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="dc224-122">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="dc224-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="dc224-123">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="dc224-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="dc224-124">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="dc224-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="dc224-125">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="dc224-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="dc224-126">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="dc224-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="dc224-127">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="dc224-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="dc224-128">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="dc224-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="dc224-129">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="dc224-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="dc224-130">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="dc224-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="dc224-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc224-131">Requirements</span></span>



| <span data-ttu-id="dc224-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc224-132">Requirement</span></span> | <span data-ttu-id="dc224-133">Valore</span><span class="sxs-lookup"><span data-stu-id="dc224-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc224-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc224-134">Minimum supported client</span></span><br/> | <span data-ttu-id="dc224-135">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="dc224-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dc224-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc224-136">Minimum supported server</span></span><br/> | <span data-ttu-id="dc224-137">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="dc224-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dc224-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dc224-138">Namespace</span></span><br/>                | <span data-ttu-id="dc224-139">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="dc224-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dc224-140">MOF</span><span class="sxs-lookup"><span data-stu-id="dc224-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc224-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc224-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc224-142">DLL</span><span class="sxs-lookup"><span data-stu-id="dc224-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc224-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dc224-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="dc224-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dc224-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc224-145">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="dc224-145">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 





---
description: Restituisce le informazioni di riepilogo della macchina virtuale per i file di definizione della macchina virtuale specificati.
ms.assetid: 5a3d7f2c-3b89-4dd6-909d-4452afc3705f
title: Metodo GetDefinitionFileSummaryInformation della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetDefinitionFileSummaryInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a46daedd282d07c2367931a9f20a7fbfa1849f9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307748"
---
# <a name="getdefinitionfilesummaryinformation-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="6aea4-103">Metodo GetDefinitionFileSummaryInformation della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="6aea4-103">GetDefinitionFileSummaryInformation method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="6aea4-104">Restituisce le informazioni di riepilogo della macchina virtuale per i file di definizione della macchina virtuale specificati.</span><span class="sxs-lookup"><span data-stu-id="6aea4-104">Returns virtual machine summary information for the specified virtual machine definition files.</span></span>

## <a name="syntax"></a><span data-ttu-id="6aea4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6aea4-105">Syntax</span></span>


```mof
uint32 GetDefinitionFileSummaryInformation(
  [in]  string                      DefinitionFiles[],
  [out] Msvm_SummaryInformationBase SummaryInformation[]
);
```



## <a name="parameters"></a><span data-ttu-id="6aea4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6aea4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6aea4-107">*DefinitionFiles* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6aea4-107">*DefinitionFiles* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6aea4-108">Matrice di percorsi dei file di configurazione XML per i quali restituire le informazioni di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="6aea4-108">An array of paths to XML configuration files for which to return summary information.</span></span>

</dd> <dt>

<span data-ttu-id="6aea4-109">*SummaryInformation* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6aea4-109">*SummaryInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6aea4-110">Matrice di istanze di [**MSVM \_ SummaryInformationBase**](msvm-summaryinformation.md) contenenti le informazioni richieste per le macchine virtuali e/o gli snapshot specificati nella matrice *DefinitionFiles* .</span><span class="sxs-lookup"><span data-stu-id="6aea4-110">An array of [**Msvm\_SummaryInformationBase**](msvm-summaryinformation.md) instances containing the requested information for the virtual machines and/or snapshots specified in the *DefinitionFiles* array.</span></span> <span data-ttu-id="6aea4-111">Vengono restituite solo le proprietà **Name**, **ElementName**, **creationTime** e **Notes** . tutte le altre proprietà saranno **null**.</span><span class="sxs-lookup"><span data-stu-id="6aea4-111">Only the **Name**, **ElementName**, **CreationTime**, and **Notes** properties are returned, all other properties will be **Null**.</span></span>

> [!Note]  

 

<span data-ttu-id="6aea4-112">Prima di Windows 10, versione 1703, DataType era [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md).</span><span class="sxs-lookup"><span data-stu-id="6aea4-112">Prior to Windows 10, version 1703, datatype was [**Msvm\_SummaryInformation**](msvm-summaryinformation.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6aea4-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6aea4-113">Return value</span></span>

<span data-ttu-id="6aea4-114">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="6aea4-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="6aea4-115">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="6aea4-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6aea4-116">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="6aea4-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6aea4-117">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="6aea4-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="6aea4-118">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="6aea4-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="6aea4-119">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="6aea4-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="6aea4-120">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="6aea4-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="6aea4-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="6aea4-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="6aea4-122">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="6aea4-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="6aea4-123">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="6aea4-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="6aea4-124">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="6aea4-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="6aea4-125">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="6aea4-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="6aea4-126">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="6aea4-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="6aea4-127">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="6aea4-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6aea4-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6aea4-128">Requirements</span></span>



| <span data-ttu-id="6aea4-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="6aea4-129">Requirement</span></span> | <span data-ttu-id="6aea4-130">Valore</span><span class="sxs-lookup"><span data-stu-id="6aea4-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6aea4-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6aea4-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6aea4-132">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6aea4-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6aea4-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6aea4-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6aea4-134">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6aea4-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6aea4-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6aea4-135">Namespace</span></span><br/>                | <span data-ttu-id="6aea4-136">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="6aea4-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6aea4-137">MOF</span><span class="sxs-lookup"><span data-stu-id="6aea4-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6aea4-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6aea4-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6aea4-139">DLL</span><span class="sxs-lookup"><span data-stu-id="6aea4-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6aea4-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6aea4-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6aea4-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6aea4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6aea4-142">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="6aea4-142">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 





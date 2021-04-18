---
description: Restituisce una stringa del messaggio di errore formattato per la matrice specificata di istanze di errore MSVM incorporate \_ .
ms.assetid: 477EF4AE-00A8-4F2D-A335-E41A2EF620BB
title: Metodo FormatError della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.FormatError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e768a6ea968d428d7809c7c322a80f3ad233aa2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307759"
---
# <a name="formaterror-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="12919-103">Metodo FormatError della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="12919-103">FormatError method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="12919-104">Restituisce una stringa del messaggio di errore formattato per la matrice specificata di istanze di [**\_ errore MSVM**](msvm-error.md) incorporate.</span><span class="sxs-lookup"><span data-stu-id="12919-104">Returns a formatted error message string for the specified array of embedded [**Msvm\_Error**](msvm-error.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="12919-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12919-105">Syntax</span></span>


```mof
uint32 FormatError(
  [in]  string Errors[],
  [out] string ErrorMessage
);
```



## <a name="parameters"></a><span data-ttu-id="12919-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="12919-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12919-107">*Errori* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="12919-107">*Errors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12919-108">Tipo: **stringa \[ \]**</span><span class="sxs-lookup"><span data-stu-id="12919-108">Type: **string\[\]**</span></span>

<span data-ttu-id="12919-109">Matrice di stringhe contenente le istanze di [**\_ errore MSVM**](msvm-error.md) utilizzate per generare il messaggio di errore di output.</span><span class="sxs-lookup"><span data-stu-id="12919-109">An array of strings containing [**Msvm\_Error**](msvm-error.md) instances used to generate the output error message.</span></span>

</dd> <dt>

<span data-ttu-id="12919-110">*ErrorMessage* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="12919-110">*ErrorMessage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12919-111">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="12919-111">Type: **string**</span></span>

<span data-ttu-id="12919-112">Nell'output, stringa che contiene i messaggi di errore concatenati rappresentati dalle istanze di [**\_ errore MSVM**](msvm-error.md) passate nel parametro *Errors* .</span><span class="sxs-lookup"><span data-stu-id="12919-112">On output, a string that contains the concatenated error messages represented by the [**Msvm\_Error**](msvm-error.md) instances passed in the *Errors* parameter.</span></span> <span data-ttu-id="12919-113">Ogni stringa di errore è separata da una coppia di caratteri di nuova riga (' \\ n').</span><span class="sxs-lookup"><span data-stu-id="12919-113">Each error string is separated by a pair of newline characters ('\\n').</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12919-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="12919-114">Return value</span></span>

<span data-ttu-id="12919-115">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="12919-115">Type: **uint32**</span></span>

<span data-ttu-id="12919-116">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="12919-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="12919-117">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="12919-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="12919-118">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="12919-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="12919-119">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="12919-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="12919-120">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="12919-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="12919-121">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="12919-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="12919-122">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="12919-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="12919-123">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="12919-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="12919-124">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="12919-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="12919-125">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="12919-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="12919-126">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="12919-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="12919-127">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="12919-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="12919-128">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="12919-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="12919-129">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="12919-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="12919-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="12919-130">Remarks</span></span>

<span data-ttu-id="12919-131">L'accesso alla [**classe \_ VirtualSystemManagementService di MSVM**](msvm-virtualsystemmanagementservice.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="12919-131">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="12919-132">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="12919-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="12919-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12919-133">Requirements</span></span>



| <span data-ttu-id="12919-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="12919-134">Requirement</span></span> | <span data-ttu-id="12919-135">Valore</span><span class="sxs-lookup"><span data-stu-id="12919-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12919-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12919-136">Minimum supported client</span></span><br/> | <span data-ttu-id="12919-137">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="12919-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="12919-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12919-138">Minimum supported server</span></span><br/> | <span data-ttu-id="12919-139">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="12919-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="12919-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="12919-140">Namespace</span></span><br/>                | <span data-ttu-id="12919-141">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="12919-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="12919-142">MOF</span><span class="sxs-lookup"><span data-stu-id="12919-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12919-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12919-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="12919-144">DLL</span><span class="sxs-lookup"><span data-stu-id="12919-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12919-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="12919-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="12919-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12919-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12919-147">**FormatError (V1)**</span><span class="sxs-lookup"><span data-stu-id="12919-147">**FormatError (V1)**</span></span>](/previous-versions/windows/desktop/virtual/formaterror-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="12919-148">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="12919-148">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 


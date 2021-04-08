---
description: Fornisce informazioni su uno snapshot in un file di set VHD.
ms.assetid: 922bf0b8-523d-488e-9a41-1a27594e2e44
title: Classe Msvm_VHDSnapshotInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VHDSnapshotInformation
- Msvm_VHDSnapshotInformation.FilePath
- Msvm_VHDSnapshotInformation.SnapshotId
- Msvm_VHDSnapshotInformation.SnapshotPath
- Msvm_VHDSnapshotInformation.ParentPathsList
- Msvm_VHDSnapshotInformation.CreationTime
- Msvm_VHDSnapshotInformation.ResilientChangeTrackingId
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1a1e2a573546d62d79170f15abddd8d5c17e30f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879930"
---
# <a name="msvm_vhdsnapshotinformation-class"></a><span data-ttu-id="7a501-103">\_Classe MSVM VHDSnapshotInformation</span><span class="sxs-lookup"><span data-stu-id="7a501-103">Msvm\_VHDSnapshotInformation class</span></span>

<span data-ttu-id="7a501-104">Fornisce informazioni su uno snapshot in un file di set VHD</span><span class="sxs-lookup"><span data-stu-id="7a501-104">Provides information about a snapshot within a VHD Set file</span></span>

<span data-ttu-id="7a501-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="7a501-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a501-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a501-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VHDSnapshotInformation
{
  string   FilePath;
  string   SnapshotId;
  string   SnapshotPath;
  string   ParentPathsList[];
  DATETIME CreationTime;
  string   ResilientChangeTrackingId;
};
```

## <a name="members"></a><span data-ttu-id="7a501-107">Members</span><span class="sxs-lookup"><span data-stu-id="7a501-107">Members</span></span>

<span data-ttu-id="7a501-108">La **classe \_ VHDSnapshotInformation di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7a501-108">The **Msvm\_VHDSnapshotInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="7a501-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7a501-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7a501-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7a501-110">Properties</span></span>

<span data-ttu-id="7a501-111">La **classe \_ VHDSnapshotInformation di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7a501-111">The **Msvm\_VHDSnapshotInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7a501-112">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="7a501-112">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a501-113">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7a501-113">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="7a501-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7a501-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a501-115">Data e ora della creazione dello snapshot.</span><span class="sxs-lookup"><span data-stu-id="7a501-115">The date and time of this snapshot's creation.</span></span>

</dd> <dt>

<span data-ttu-id="7a501-116">**FilePath**</span><span class="sxs-lookup"><span data-stu-id="7a501-116">**FilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a501-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7a501-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a501-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7a501-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a501-119">Percorso del file di set VHD.</span><span class="sxs-lookup"><span data-stu-id="7a501-119">The path of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="7a501-120">**ParentPathsList**</span><span class="sxs-lookup"><span data-stu-id="7a501-120">**ParentPathsList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a501-121">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="7a501-121">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="7a501-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7a501-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a501-123">Elenco di percorsi di file che rappresentano tutti i file da cui dipende questo snapshot.</span><span class="sxs-lookup"><span data-stu-id="7a501-123">A list of file paths representing all of the files on which this snapshot depends.</span></span> <span data-ttu-id="7a501-124">Questo campo sarà vuoto a meno che non sia richiesto in modo specifico.</span><span class="sxs-lookup"><span data-stu-id="7a501-124">This field will be empty unless specifically requested.</span></span> <span data-ttu-id="7a501-125">La prima voce è l'elemento padre diretto del file, con l'ultima voce che corrisponde alla radice.</span><span class="sxs-lookup"><span data-stu-id="7a501-125">The first entry is the file's immediate parent, with the last entry being the root.</span></span>

</dd> <dt>

<span data-ttu-id="7a501-126">**ResilientChangeTrackingId**</span><span class="sxs-lookup"><span data-stu-id="7a501-126">**ResilientChangeTrackingId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a501-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7a501-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a501-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7a501-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a501-129">ID di rilevamento delle modifiche resiliente, se presente, associato a questo snapshot.</span><span class="sxs-lookup"><span data-stu-id="7a501-129">The resilient change tracking ID, if any, associated with this snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="7a501-130">**SnapshotId**</span><span class="sxs-lookup"><span data-stu-id="7a501-130">**SnapshotId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a501-131">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7a501-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a501-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7a501-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a501-133">GUID che identifica in modo univoco questo snapshot all'interno del file di set VHD.</span><span class="sxs-lookup"><span data-stu-id="7a501-133">A GUID that uniquely identifies this snapshot within the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="7a501-134">**SnapshotPath**</span><span class="sxs-lookup"><span data-stu-id="7a501-134">**SnapshotPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a501-135">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="7a501-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a501-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7a501-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a501-137">Percorso del file rappresentato da questo snapshot.</span><span class="sxs-lookup"><span data-stu-id="7a501-137">The path of the file represented by this snapshot.</span></span> <span data-ttu-id="7a501-138">Questo campo può essere vuoto se non è presente alcun file associato a questo snapshot.</span><span class="sxs-lookup"><span data-stu-id="7a501-138">This field may be empty if there is no file associated with this snapshot.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7a501-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a501-139">Requirements</span></span>



| <span data-ttu-id="7a501-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a501-140">Requirement</span></span> | <span data-ttu-id="7a501-141">Valore</span><span class="sxs-lookup"><span data-stu-id="7a501-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a501-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a501-142">Minimum supported client</span></span><br/> | <span data-ttu-id="7a501-143">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="7a501-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="7a501-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a501-144">Minimum supported server</span></span><br/> | <span data-ttu-id="7a501-145">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7a501-145">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="7a501-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7a501-146">Namespace</span></span><br/>                | <span data-ttu-id="7a501-147">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="7a501-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7a501-148">MOF</span><span class="sxs-lookup"><span data-stu-id="7a501-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a501-149"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7a501-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a501-150">DLL</span><span class="sxs-lookup"><span data-stu-id="7a501-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a501-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7a501-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 





---
description: Fornisce informazioni su un file di set VHD.
ms.assetid: a975c131-d3f3-4be3-bc69-e277e3ce4d28
title: Classe Msvm_VHDSetInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VHDSetInformation
- Msvm_VHDSetInformation.Path
- Msvm_VHDSetInformation.SnapshotIdList
- Msvm_VHDSetInformation.AllPaths
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 51f1371baea902627160c2c7a1fb31d156be8951
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308730"
---
# <a name="msvm_vhdsetinformation-class"></a><span data-ttu-id="a19b5-103">\_Classe MSVM VHDSetInformation</span><span class="sxs-lookup"><span data-stu-id="a19b5-103">Msvm\_VHDSetInformation class</span></span>

<span data-ttu-id="a19b5-104">Fornisce informazioni su un file di set VHD.</span><span class="sxs-lookup"><span data-stu-id="a19b5-104">Provides information about a VHD Set file.</span></span>

<span data-ttu-id="a19b5-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a19b5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a19b5-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a19b5-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VHDSetInformation
{
  string Path;
  string SnapshotIdList[];
  string AllPaths[];
};
```

## <a name="members"></a><span data-ttu-id="a19b5-107">Members</span><span class="sxs-lookup"><span data-stu-id="a19b5-107">Members</span></span>

<span data-ttu-id="a19b5-108">La **classe \_ VHDSetInformation di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a19b5-108">The **Msvm\_VHDSetInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="a19b5-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a19b5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a19b5-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a19b5-110">Properties</span></span>

<span data-ttu-id="a19b5-111">La **classe \_ VHDSetInformation di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a19b5-111">The **Msvm\_VHDSetInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a19b5-112">**AllPaths**</span><span class="sxs-lookup"><span data-stu-id="a19b5-112">**AllPaths**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a19b5-113">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="a19b5-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a19b5-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a19b5-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a19b5-115">Elenco di tutti i file inclusi nel file di set VHD, inclusi tutti i file senza riferimenti e gli eventuali elementi padre del disco rigido virtuale radice.</span><span class="sxs-lookup"><span data-stu-id="a19b5-115">A list of all files encompassed by the VHD Set file, including any unreferenced files and any parents of the root virtual hard disk.</span></span> <span data-ttu-id="a19b5-116">Tutti i file elencati dopo il disco rigido virtuale radice non sono gestiti da questo file di set VHD.</span><span class="sxs-lookup"><span data-stu-id="a19b5-116">All files listed after the root virtual hard disk are unmanaged by this VHD Set file.</span></span> <span data-ttu-id="a19b5-117">Questo campo può essere vuoto se queste informazioni non sono state richieste in modo specifico.</span><span class="sxs-lookup"><span data-stu-id="a19b5-117">This field may be empty if this information was not specifically requested.</span></span>

</dd> <dt>

<span data-ttu-id="a19b5-118">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="a19b5-118">**Path**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a19b5-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="a19b5-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a19b5-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a19b5-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a19b5-121">Percorso del file di set VHD.</span><span class="sxs-lookup"><span data-stu-id="a19b5-121">The path of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="a19b5-122">**SnapshotIdList**</span><span class="sxs-lookup"><span data-stu-id="a19b5-122">**SnapshotIdList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a19b5-123">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="a19b5-123">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a19b5-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a19b5-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a19b5-125">Elenco di GUID che rappresentano tutti gli snapshot contenuti in questo file di set VHD.</span><span class="sxs-lookup"><span data-stu-id="a19b5-125">A list of GUIDs representing all of the snapshots contained by this VHD Set file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a19b5-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a19b5-126">Requirements</span></span>



| <span data-ttu-id="a19b5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a19b5-127">Requirement</span></span> | <span data-ttu-id="a19b5-128">Valore</span><span class="sxs-lookup"><span data-stu-id="a19b5-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a19b5-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a19b5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a19b5-130">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="a19b5-130">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="a19b5-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a19b5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a19b5-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a19b5-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="a19b5-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a19b5-133">Namespace</span></span><br/>                | <span data-ttu-id="a19b5-134">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="a19b5-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a19b5-135">MOF</span><span class="sxs-lookup"><span data-stu-id="a19b5-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a19b5-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a19b5-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a19b5-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a19b5-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a19b5-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a19b5-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 





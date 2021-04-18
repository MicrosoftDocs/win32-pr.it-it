---
title: Classe Win32_TSVmMetadataAssociation
description: Rappresenta un'associazione tra una macchina virtuale Desktop remoto e le relative proprietà dei metadati.
ms.assetid: 374b1a29-78de-45fd-97b3-c5a5b724e66b
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSVmMetadataAssociation Servizi Desktop remoto
- Classe Win32_TSVmMetadataAssociation Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSVmMetadataAssociation
- Win32_TSVmMetadataAssociation.TSVm
- Win32_TSVmMetadataAssociation.MetadataItem
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db3a68c20553eaf52903471d19df9df169ecde21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301051"
---
# <a name="win32_tsvmmetadataassociation-class"></a><span data-ttu-id="0721e-105">Win32 \_ TSVmMetadataAssociation (classe)</span><span class="sxs-lookup"><span data-stu-id="0721e-105">Win32\_TSVmMetadataAssociation class</span></span>

<span data-ttu-id="0721e-106">Rappresenta un'associazione tra una macchina virtuale Desktop remoto e le relative proprietà dei metadati.</span><span class="sxs-lookup"><span data-stu-id="0721e-106">Represents an association between a Remote Desktop virtual machine and its metadata properties.</span></span>

<span data-ttu-id="0721e-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="0721e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0721e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0721e-108">Syntax</span></span>

``` syntax
[dynamic, Association, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVmMetadataAssociation
{
  Win32_TSVm             REF TSVm;
  Win32_TSVmMetadataItem REF MetadataItem;
};
```

## <a name="members"></a><span data-ttu-id="0721e-109">Members</span><span class="sxs-lookup"><span data-stu-id="0721e-109">Members</span></span>

<span data-ttu-id="0721e-110">La classe **Win32 \_ TSVmMetadataAssociation** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0721e-110">The **Win32\_TSVmMetadataAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="0721e-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0721e-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0721e-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0721e-112">Properties</span></span>

<span data-ttu-id="0721e-113">La classe **Win32 \_ TSVmMetadataAssociation** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0721e-113">The **Win32\_TSVmMetadataAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0721e-114">**MetadataItem**</span><span class="sxs-lookup"><span data-stu-id="0721e-114">**MetadataItem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0721e-115">Tipo di dati: **[ **Win32 \_ TSVmMetadataItem**](win32-tsvmmetadataitem.md)**</span><span class="sxs-lookup"><span data-stu-id="0721e-115">Data type: **[**Win32\_TSVmMetadataItem**](win32-tsvmmetadataitem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="0721e-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0721e-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0721e-117">Istanza della classe [**Win32 \_ TSVmMetadataItem**](win32-tsvmmetadataitem.md) che rappresenta i metadati per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0721e-117">An instance of the [**Win32\_TSVmMetadataItem**](win32-tsvmmetadataitem.md) class that represents the metadata for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="0721e-118">**TSVm**</span><span class="sxs-lookup"><span data-stu-id="0721e-118">**TSVm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0721e-119">Tipo di dati: **[ **Win32 \_ TSVm**](win32-tsvm.md)**</span><span class="sxs-lookup"><span data-stu-id="0721e-119">Data type: **[**Win32\_TSVm**](win32-tsvm.md)**</span></span>
</dt> <dt>

<span data-ttu-id="0721e-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0721e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0721e-121">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0721e-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0721e-122">Istanza della classe [**Win32 \_ TSVm**](win32-tsvm.md) che rappresenta la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0721e-122">An instance of the [**Win32\_TSVm**](win32-tsvm.md) class that represents the virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0721e-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0721e-123">Requirements</span></span>



| <span data-ttu-id="0721e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0721e-124">Requirement</span></span> | <span data-ttu-id="0721e-125">Valore</span><span class="sxs-lookup"><span data-stu-id="0721e-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="0721e-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0721e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0721e-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0721e-127">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="0721e-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0721e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0721e-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0721e-129">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="0721e-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0721e-130">Namespace</span></span><br/>                | <span data-ttu-id="0721e-131">Radice \\ CIMV2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0721e-131">Root\\CIMV2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="0721e-132">MOF</span><span class="sxs-lookup"><span data-stu-id="0721e-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0721e-133"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0721e-133"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="0721e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0721e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0721e-135"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0721e-135"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 


---
title: Classe MSAD_NamingContext
description: Rappresenta un particolare contesto dei nomi (NC) nel controller di dominio.
ms.assetid: 67dd6c68-6c67-40b4-a20a-c6c312d23441
ms.tgt_platform: multiple
keywords:
- Classe MSAD_NamingContext Active Directory
- Classe MSAD_NamingContext Active Directory, descritta
topic_type:
- apiref
api_name:
- MSAD_NamingContext
- MSAD_NamingContext.DistinguishedName
- MSAD_NamingContext.IsFullReplica
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d68f70c6e40e823df0a6827e1114f40dae7937be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741586"
---
# <a name="msad_namingcontext-class"></a><span data-ttu-id="51a39-105">\_Classe MSAD NamingContext</span><span class="sxs-lookup"><span data-stu-id="51a39-105">MSAD\_NamingContext class</span></span>

<span data-ttu-id="51a39-106">Rappresenta un particolare contesto dei nomi (NC) nel controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="51a39-106">Represents a particular naming context (NC) on the domain controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="51a39-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="51a39-107">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_NamingContext
{
  String  DistinguishedName;
  boolean IsFullReplica = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="51a39-108">Members</span><span class="sxs-lookup"><span data-stu-id="51a39-108">Members</span></span>

<span data-ttu-id="51a39-109">La **classe \_ NamingContext di MSAD** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="51a39-109">The **MSAD\_NamingContext** class has these types of members:</span></span>

-   [<span data-ttu-id="51a39-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="51a39-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="51a39-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="51a39-111">Properties</span></span>

<span data-ttu-id="51a39-112">La **classe \_ NamingContext di MSAD** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="51a39-112">The **MSAD\_NamingContext** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="51a39-113">**DistinguishedName**</span><span class="sxs-lookup"><span data-stu-id="51a39-113">**DistinguishedName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51a39-114">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="51a39-114">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="51a39-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="51a39-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51a39-116">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="51a39-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="51a39-117">Ottiene il percorso X. 500 del NC.</span><span class="sxs-lookup"><span data-stu-id="51a39-117">Gets the X.500 path of the NC.</span></span>

</dd> <dt>

<span data-ttu-id="51a39-118">**IsFullReplica**</span><span class="sxs-lookup"><span data-stu-id="51a39-118">**IsFullReplica**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51a39-119">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="51a39-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="51a39-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="51a39-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51a39-121">Ottiene il valore che indica se il NC è di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="51a39-121">Gets the value that indicates whether the NC is read/write.</span></span> <span data-ttu-id="51a39-122">**True** se il NC è di lettura/scrittura; **False** se il NC è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="51a39-122">**TRUE** if the NC is read/write; **FALSE** if the NC is read-only.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="51a39-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51a39-123">Requirements</span></span>



| <span data-ttu-id="51a39-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="51a39-124">Requirement</span></span> | <span data-ttu-id="51a39-125">Valore</span><span class="sxs-lookup"><span data-stu-id="51a39-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51a39-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51a39-126">Minimum supported client</span></span><br/> | <span data-ttu-id="51a39-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="51a39-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="51a39-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51a39-128">Minimum supported server</span></span><br/> | <span data-ttu-id="51a39-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="51a39-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="51a39-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="51a39-130">Namespace</span></span><br/>                | <span data-ttu-id="51a39-131">\\MicrosoftActiveDirectory radice</span><span class="sxs-lookup"><span data-stu-id="51a39-131">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="51a39-132">MOF</span><span class="sxs-lookup"><span data-stu-id="51a39-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51a39-133"><dt>Replprov. mof</dt></span><span class="sxs-lookup"><span data-stu-id="51a39-133"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="51a39-134">DLL</span><span class="sxs-lookup"><span data-stu-id="51a39-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51a39-135"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51a39-135"><dt>Replprov.dll</dt></span></span> </dl> |



 


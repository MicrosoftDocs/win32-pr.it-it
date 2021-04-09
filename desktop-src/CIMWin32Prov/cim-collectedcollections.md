---
description: La \_ classe CIM CollectedCollections è un'associazione di aggregazione che rappresenta una raccolta di elementi di sistema gestiti (MSE) contenuti in una raccolta di mses.
ms.assetid: 7baaf429-1211-4545-ace2-c6312d53c0f6
ms.tgt_platform: multiple
title: Classe CIM_CollectedCollections
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedCollections
- CIM_CollectedCollections.Collection
- CIM_CollectedCollections.CollectionInCollection
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e592c7799efc8c280d4cd64c2b54ed8a3ea328f6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966205"
---
# <a name="cim_collectedcollections-class"></a><span data-ttu-id="5790a-103">CIM \_ CollectedCollections (classe)</span><span class="sxs-lookup"><span data-stu-id="5790a-103">CIM\_CollectedCollections class</span></span>

<span data-ttu-id="5790a-104">La classe **CIM \_ CollectedCollections** è un'associazione di aggregazione che rappresenta una raccolta di elementi di sistema gestiti (MSE) contenuti in una raccolta di mses.</span><span class="sxs-lookup"><span data-stu-id="5790a-104">The **CIM\_CollectedCollections** class is an aggregation association that represents a collection of Managed System Elements (MSE) contained in a collection of MSEs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5790a-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="5790a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5790a-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5790a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5790a-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5790a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5790a-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="5790a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5790a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5790a-109">Syntax</span></span>

``` syntax
class CIM_CollectedCollections
{
  CIM_CollectionOfMSEs REF Collection;
  CIM_CollectionOfMSEs REF CollectionInCollection;
};
```

## <a name="members"></a><span data-ttu-id="5790a-110">Members</span><span class="sxs-lookup"><span data-stu-id="5790a-110">Members</span></span>

<span data-ttu-id="5790a-111">La classe **CIM \_ CollectedCollections** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5790a-111">The **CIM\_CollectedCollections** class has these types of members:</span></span>

-   [<span data-ttu-id="5790a-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5790a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5790a-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5790a-113">Properties</span></span>

<span data-ttu-id="5790a-114">La classe **CIM \_ CollectedCollections** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5790a-114">The **CIM\_CollectedCollections** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5790a-115">**Raccolta**</span><span class="sxs-lookup"><span data-stu-id="5790a-115">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5790a-116">Tipo di dati: **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="5790a-116">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="5790a-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5790a-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5790a-118">Riferimento all'elemento di livello superiore o padre nell'aggregazione.</span><span class="sxs-lookup"><span data-stu-id="5790a-118">Reference to the "higher level" or parent element in the aggregation.</span></span>

</dd> <dt>

<span data-ttu-id="5790a-119">**CollectionInCollection**</span><span class="sxs-lookup"><span data-stu-id="5790a-119">**CollectionInCollection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5790a-120">Tipo di dati: **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="5790a-120">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="5790a-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5790a-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5790a-122">Riferimento alla **raccolta**"raccolta".</span><span class="sxs-lookup"><span data-stu-id="5790a-122">Reference to the "collected" **Collection**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5790a-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="5790a-123">Remarks</span></span>

<span data-ttu-id="5790a-124">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="5790a-124">WMI does not implement this class.</span></span>

<span data-ttu-id="5790a-125">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="5790a-125">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5790a-126">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="5790a-126">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5790a-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5790a-127">Requirements</span></span>



| <span data-ttu-id="5790a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5790a-128">Requirement</span></span> | <span data-ttu-id="5790a-129">Valore</span><span class="sxs-lookup"><span data-stu-id="5790a-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5790a-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5790a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5790a-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5790a-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5790a-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5790a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5790a-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5790a-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5790a-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5790a-134">Namespace</span></span><br/>                | <span data-ttu-id="5790a-135">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="5790a-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5790a-136">MOF</span><span class="sxs-lookup"><span data-stu-id="5790a-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5790a-137"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5790a-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5790a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="5790a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5790a-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5790a-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 





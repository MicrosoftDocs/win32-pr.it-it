---
description: Rappresenta la classe del tipo di evento per gli eventi del tipo di oggetto correlati all'inizio e alla fine della raccolta dei dati.
ms.assetid: 16b21f61-e734-4f51-9b11-e507b5957107
title: Classe ObTypeEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObTypeEvent
- ObTypeEvent.ObjectType
- ObTypeEvent.Reserved
- ObTypeEvent.TypeName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9d80d5fbe57565d64e9ea53587d7a2c3488e6cf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131882"
---
# <a name="obtypeevent-class"></a><span data-ttu-id="f086c-103">Classe ObTypeEvent</span><span class="sxs-lookup"><span data-stu-id="f086c-103">ObTypeEvent class</span></span>

<span data-ttu-id="f086c-104">Rappresenta la classe del tipo di evento per gli eventi del tipo di oggetto correlati all'inizio e alla fine della raccolta dei dati.</span><span class="sxs-lookup"><span data-stu-id="f086c-104">Represents the event type class for object type events related to the beginning and end of data collection.</span></span> <span data-ttu-id="f086c-105">Questo evento comporta il mapping dei valori di indice del tipo ai nomi dei tipi.</span><span class="sxs-lookup"><span data-stu-id="f086c-105">This event involves the mapping of the type index values to the type names.</span></span>

<span data-ttu-id="f086c-106">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f086c-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f086c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f086c-107">Syntax</span></span>

``` syntax
[Dynamic, EventType{36,37}, EventTypeName{TypeDCStart,TypeDCEnd}]
class ObTypeEvent : ObTrace
{
  uint16 ObjectType;
  uint16 Reserved;
  string TypeName;
};
```

## <a name="members"></a><span data-ttu-id="f086c-108">Members</span><span class="sxs-lookup"><span data-stu-id="f086c-108">Members</span></span>

<span data-ttu-id="f086c-109">La classe **ObTypeEvent** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f086c-109">The **ObTypeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="f086c-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f086c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f086c-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f086c-111">Properties</span></span>

<span data-ttu-id="f086c-112">La classe **ObTypeEvent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f086c-112">The **ObTypeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f086c-113">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="f086c-113">**ObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f086c-114">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f086c-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f086c-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f086c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f086c-116">Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="f086c-116">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="f086c-117">Tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="f086c-117">The object type.</span></span>

</dd> <dt>

<span data-ttu-id="f086c-118">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="f086c-118">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f086c-119">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f086c-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f086c-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f086c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f086c-121">Qualificatori: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span><span class="sxs-lookup"><span data-stu-id="f086c-121">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="f086c-122">Riservato.</span><span class="sxs-lookup"><span data-stu-id="f086c-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="f086c-123">**TypeName**</span><span class="sxs-lookup"><span data-stu-id="f086c-123">**TypeName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f086c-124">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="f086c-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f086c-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f086c-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f086c-126">Qualificatori: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="f086c-126">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="f086c-127">Nome del tipo.</span><span class="sxs-lookup"><span data-stu-id="f086c-127">The type name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f086c-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f086c-128">Requirements</span></span>



| <span data-ttu-id="f086c-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="f086c-129">Requirement</span></span> | <span data-ttu-id="f086c-130">Valore</span><span class="sxs-lookup"><span data-stu-id="f086c-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f086c-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f086c-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f086c-132">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f086c-132">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f086c-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f086c-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f086c-134">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f086c-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f086c-135">MOF</span><span class="sxs-lookup"><span data-stu-id="f086c-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f086c-136"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f086c-136"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 





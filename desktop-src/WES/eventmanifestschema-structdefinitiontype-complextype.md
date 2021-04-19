---
title: Tipo complesso StructDefinitionType
description: Definisce una struttura che include uno o più elementi di dati che si desidera includere nell'evento. | Tipo complesso StructDefinitionType
ms.assetid: eb6b3682-1035-472b-8027-583d43c31748
keywords:
- Log eventi di tipo complesso StructDefinitionType
topic_type:
- apiref
api_name:
- StructDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 01e739077d38dec94c0a407e5779bec90369ffb9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321470"
---
# <a name="structdefinitiontype-complex-type"></a><span data-ttu-id="c25c9-105">Tipo complesso StructDefinitionType</span><span class="sxs-lookup"><span data-stu-id="c25c9-105">StructDefinitionType Complex Type</span></span>

<span data-ttu-id="c25c9-106">Definisce una struttura che include uno o più elementi di dati che si desidera includere nell'evento.</span><span class="sxs-lookup"><span data-stu-id="c25c9-106">Defines a structure that includes one or more data items that you want to include with the event.</span></span>

``` syntax
<xs:complexType name="StructDefinitionType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="data"
            type="DataDefinitionType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
        use="required"
     />
    <xs:attribute name="length"
        type="LengthType"
        use="optional"
     />
    <xs:attribute name="count"
        type="CountType"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="c25c9-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="c25c9-107">Child elements</span></span>



| <span data-ttu-id="c25c9-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="c25c9-108">Element</span></span>                                                               | <span data-ttu-id="c25c9-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="c25c9-109">Type</span></span>                                                                             | <span data-ttu-id="c25c9-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c25c9-110">Description</span></span>                                                               |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="c25c9-111">**dati**</span><span class="sxs-lookup"><span data-stu-id="c25c9-111">**data**</span></span>](eventmanifestschema-data-structdefinitiontype-element.md) | [<span data-ttu-id="c25c9-112">**DataDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="c25c9-112">**DataDefinitionType**</span></span>](eventmanifestschema-datadefinitiontype-complextype.md) | <span data-ttu-id="c25c9-113">Definisce un elemento di dati che si desidera includere nella struttura.</span><span class="sxs-lookup"><span data-stu-id="c25c9-113">Defines a data item that you want to include in the structure.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="c25c9-114">Attributi</span><span class="sxs-lookup"><span data-stu-id="c25c9-114">Attributes</span></span>



| <span data-ttu-id="c25c9-115">Nome</span><span class="sxs-lookup"><span data-stu-id="c25c9-115">Name</span></span>   | <span data-ttu-id="c25c9-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="c25c9-116">Type</span></span>                                                            | <span data-ttu-id="c25c9-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c25c9-117">Description</span></span>                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c25c9-118">count</span><span class="sxs-lookup"><span data-stu-id="c25c9-118">count</span></span>  | [<span data-ttu-id="c25c9-119">**CountType**</span><span class="sxs-lookup"><span data-stu-id="c25c9-119">**CountType**</span></span>](eventmanifestschema-counttype-simpletype.md)   | <span data-ttu-id="c25c9-120">Numero di elementi in una matrice di strutture.</span><span class="sxs-lookup"><span data-stu-id="c25c9-120">The number of elements in an array of structures.</span></span> <span data-ttu-id="c25c9-121">Questo attributo indica che la struttura definisce una matrice di strutture.</span><span class="sxs-lookup"><span data-stu-id="c25c9-121">This attribute indicates that the structure is defining an array of structures.</span></span> <span data-ttu-id="c25c9-122">È possibile specificare il conteggio effettivo o il nome di un elemento di dati all'esterno della struttura che contiene il conteggio.</span><span class="sxs-lookup"><span data-stu-id="c25c9-122">You can specify the actual count or the name of a data item outside of the structure that contains the count.</span></span> <br/>                               |
| <span data-ttu-id="c25c9-123">length</span><span class="sxs-lookup"><span data-stu-id="c25c9-123">length</span></span> | [<span data-ttu-id="c25c9-124">**LengthType**</span><span class="sxs-lookup"><span data-stu-id="c25c9-124">**LengthType**</span></span>](eventmanifestschema-lengthtype-simpletype.md) | <span data-ttu-id="c25c9-125">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="c25c9-125">Not available.</span></span><br/> <span data-ttu-id="c25c9-126">**Windows Server 2008 e Windows Vista:** Lunghezza, in byte, della struttura.</span><span class="sxs-lookup"><span data-stu-id="c25c9-126">**Windows Server 2008 and Windows Vista:** The length of this structure, in bytes.</span></span> <span data-ttu-id="c25c9-127">Non disponibile a partire da Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c25c9-127">Not available starting with Windows 7.</span></span><br/>                                                                                                                            |
| <span data-ttu-id="c25c9-128">name</span><span class="sxs-lookup"><span data-stu-id="c25c9-128">name</span></span>   | <span data-ttu-id="c25c9-129">string</span><span class="sxs-lookup"><span data-stu-id="c25c9-129">string</span></span>                                                          | <span data-ttu-id="c25c9-130">Nome della struttura.</span><span class="sxs-lookup"><span data-stu-id="c25c9-130">The name to the structure.</span></span> <span data-ttu-id="c25c9-131">È possibile usare il nome per fare riferimento all'elemento dati nel frammento XML se si specifica una sezione [**UserData**](eventmanifestschema-userdata-templateitemtype-element.md) nel modello.</span><span class="sxs-lookup"><span data-stu-id="c25c9-131">You can use the name to reference the data item in your XML fragment if you specify a [**UserData**](eventmanifestschema-userdata-templateitemtype-element.md) section in your template.</span></span><br/> <span data-ttu-id="c25c9-132">**Windows Vista:** Questo attributo è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c25c9-132">**Windows Vista:** This attribute is optional.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c25c9-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="c25c9-133">Remarks</span></span>

<span data-ttu-id="c25c9-134">I provider scrivono la struttura come un BLOB e non come singoli membri della struttura.</span><span class="sxs-lookup"><span data-stu-id="c25c9-134">Providers write the structure as a blob and not as individual members of the structure.</span></span> <span data-ttu-id="c25c9-135">Se la struttura C che si sta scrivendo contiene puntatori, ad esempio un puntatore di tipo LPWSTR, i dati dell'evento conterranno il valore del puntatore, non i dati dereferenziati.</span><span class="sxs-lookup"><span data-stu-id="c25c9-135">If the C structure that you are writing contains pointers (for example, a pointer of type LPWSTR), the event data will contain the pointer value, not the dereferenced data.</span></span>

<span data-ttu-id="c25c9-136">È consigliabile non utilizzare le strutture ma definire gli elementi di dati per ogni membro e scriverli separatamente.</span><span class="sxs-lookup"><span data-stu-id="c25c9-136">You should not use structures but instead should define data items for each member and write them separately.</span></span> <span data-ttu-id="c25c9-137">Se si decide di utilizzare la struttura, la struttura deve contenere solo tipi integrali ed è necessario assicurarsi che i membri della struttura siano allineati a un limite di 8 byte.</span><span class="sxs-lookup"><span data-stu-id="c25c9-137">If you decide to use structure, the structure should contain only integral types and you must ensure that the members of the structure align to an 8-byte boundary.</span></span> <span data-ttu-id="c25c9-138">In caso contrario, è probabile che vengano restituiti errori di allineamento quando si tenta di accedere ai dati.</span><span class="sxs-lookup"><span data-stu-id="c25c9-138">If you do not, you will likely receive alignment errors when you try to access the data.</span></span> <span data-ttu-id="c25c9-139">Si consiglia di utilizzare la \# direttiva pragma pack () per forzare l'allineamento su un limite di 8 byte.</span><span class="sxs-lookup"><span data-stu-id="c25c9-139">Consider using the \#pragma pack() directive to force alignment on an 8-byte boundary.</span></span>

## <a name="requirements"></a><span data-ttu-id="c25c9-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c25c9-140">Requirements</span></span>



| <span data-ttu-id="c25c9-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="c25c9-141">Requirement</span></span> | <span data-ttu-id="c25c9-142">Valore</span><span class="sxs-lookup"><span data-stu-id="c25c9-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c25c9-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c25c9-143">Minimum supported client</span></span><br/> | <span data-ttu-id="c25c9-144">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c25c9-144">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c25c9-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c25c9-145">Minimum supported server</span></span><br/> | <span data-ttu-id="c25c9-146">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c25c9-146">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 






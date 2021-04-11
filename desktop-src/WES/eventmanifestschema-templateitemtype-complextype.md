---
title: Tipo complesso TemplateItemType
description: Modello che definisce i dati da includere in un evento. | Tipo complesso TemplateItemType
ms.assetid: 1681af7d-03ef-47bc-bc02-ce1a9903fb44
keywords:
- Log eventi di tipo complesso TemplateItemType
topic_type:
- apiref
api_name:
- TemplateItemType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 94ae108ceed3285fe7e57461611d94b1147d94e7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234774"
---
# <a name="templateitemtype-complex-type"></a><span data-ttu-id="0f843-105">Tipo complesso TemplateItemType</span><span class="sxs-lookup"><span data-stu-id="0f843-105">TemplateItemType Complex Type</span></span>

<span data-ttu-id="0f843-106">Modello che definisce i dati da includere in un evento.</span><span class="sxs-lookup"><span data-stu-id="0f843-106">A template that defines the data to include with an event.</span></span>

``` syntax
<xs:complexType name="TemplateItemType">
    <xs:sequence
        maxOccurs="unbounded"
    >
        <xs:choice
            maxOccurs="unbounded"
            minOccurs="0"
        >
            <xs:element name="data"
                type="DataDefinitionType"
             />
            <xs:element name="struct"
                type="StructDefinitionType"
             />
        </xs:choice>
        <xs:element name="binary"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="name"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="UserData"
            type="XmlType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="tid"
        type="token"
        use="required"
     />
    <xs:attribute name="name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="0f843-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="0f843-107">Child elements</span></span>



| <span data-ttu-id="0f843-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="0f843-108">Element</span></span>                                                                   | <span data-ttu-id="0f843-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="0f843-109">Type</span></span>                                                                                 | <span data-ttu-id="0f843-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f843-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0f843-111">**binario**</span><span class="sxs-lookup"><span data-stu-id="0f843-111">**binary**</span></span>](eventmanifestschema-binary-templateitemtype-element.md)     |                                                                                      | <span data-ttu-id="0f843-112">Riservato esclusivamente per uso interno.</span><span class="sxs-lookup"><span data-stu-id="0f843-112">Reserved for internal use only.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="0f843-113">**dati**</span><span class="sxs-lookup"><span data-stu-id="0f843-113">**data**</span></span>](eventmanifestschema-data-templateitemtype-element.md)         | [<span data-ttu-id="0f843-114">**DataDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="0f843-114">**DataDefinitionType**</span></span>](eventmanifestschema-datadefinitiontype-complextype.md)     | <span data-ttu-id="0f843-115">Definisce un elemento di dati che si desidera includere nell'evento.</span><span class="sxs-lookup"><span data-stu-id="0f843-115">Defines a data item that you want to include with the event.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="0f843-116">**struct**</span><span class="sxs-lookup"><span data-stu-id="0f843-116">**struct**</span></span>](eventmanifestschema-struct-templateitemtype-element.md)     | [<span data-ttu-id="0f843-117">**StructDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="0f843-117">**StructDefinitionType**</span></span>](eventmanifestschema-structdefinitiontype-complextype.md) | <span data-ttu-id="0f843-118">Definisce una struttura che include uno o più elementi di dati che si desidera includere nell'evento.</span><span class="sxs-lookup"><span data-stu-id="0f843-118">Defines a structure that includes one or more data items that you want to include with the event.</span></span> <span data-ttu-id="0f843-119">I provider scrivono la struttura come un BLOB e non come singoli membri della struttura.</span><span class="sxs-lookup"><span data-stu-id="0f843-119">Providers write the structure as a blob and not as individual members of the structure.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="0f843-120">**UserData**</span><span class="sxs-lookup"><span data-stu-id="0f843-120">**UserData**</span></span>](eventmanifestschema-userdata-templateitemtype-element.md) | [<span data-ttu-id="0f843-121">**XmlType**</span><span class="sxs-lookup"><span data-stu-id="0f843-121">**XmlType**</span></span>](eventmanifestschema-xmltype-complextype.md)                           | <span data-ttu-id="0f843-122">Frammento XML utilizzato per eseguire il rendering dei dati dell'evento.</span><span class="sxs-lookup"><span data-stu-id="0f843-122">An XML fragment that is used to render the event data.</span></span> <span data-ttu-id="0f843-123">Se non si include il frammento, i dati dell'evento vengono visualizzati nell'ordine in cui gli elementi di dati sono definiti nel modello.</span><span class="sxs-lookup"><span data-stu-id="0f843-123">If you do not include the fragment, the event data is rendered in the order that the data items are defined in the template.</span></span> <span data-ttu-id="0f843-124">Il contenuto di questo elemento è qualsiasi frammento XML valido.</span><span class="sxs-lookup"><span data-stu-id="0f843-124">The contents of this element is any valid XML fragment.</span></span> <span data-ttu-id="0f843-125">Il frammento deve contenere solo un nodo di primo livello e il nodo di primo livello deve specificare il proprio spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="0f843-125">The fragment must contain only one top-level node and the top-level node must specify its own namespace.</span></span> <br/> <span data-ttu-id="0f843-126">Per fare riferimento a un elemento dati nel frammento, impostare il corpo del testo per un nodo nel frammento su%*n*, dove *n* è l'indice in base uno degli elementi di dati di primo livello nell'elenco di elementi di dati (non è possibile fare riferimento ai membri di una struttura).</span><span class="sxs-lookup"><span data-stu-id="0f843-126">To reference a data item in the fragment, set the text body for a node in the fragment to %*n*, where *n* is the one-based index of the top-level data items in the list of data items (you cannot reference members of a structure).</span></span> <span data-ttu-id="0f843-127">Il valore di indice specificato non deve essere maggiore del numero di elementi di dati di primo livello nel modello.</span><span class="sxs-lookup"><span data-stu-id="0f843-127">The index value that you specify must not be greater than the number of top-level data items in the template.</span></span><br/> <span data-ttu-id="0f843-128">Questo elemento segue tutti i **dati** e gli elementi **struct** .</span><span class="sxs-lookup"><span data-stu-id="0f843-128">This element follows all **data** and **struct** elements.</span></span> <br/> |



## <a name="attributes"></a><span data-ttu-id="0f843-129">Attributi</span><span class="sxs-lookup"><span data-stu-id="0f843-129">Attributes</span></span>



| <span data-ttu-id="0f843-130">Nome</span><span class="sxs-lookup"><span data-stu-id="0f843-130">Name</span></span> | <span data-ttu-id="0f843-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="0f843-131">Type</span></span>   | <span data-ttu-id="0f843-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f843-132">Description</span></span>                                                                                                                                                                                           |
|------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f843-133">name</span><span class="sxs-lookup"><span data-stu-id="0f843-133">name</span></span> | <span data-ttu-id="0f843-134">string</span><span class="sxs-lookup"><span data-stu-id="0f843-134">string</span></span> | <span data-ttu-id="0f843-135">Riservato esclusivamente per uso interno.</span><span class="sxs-lookup"><span data-stu-id="0f843-135">Reserved for internal use only.</span></span><br/>                                                                                                                                                            |
| <span data-ttu-id="0f843-136">name</span><span class="sxs-lookup"><span data-stu-id="0f843-136">name</span></span> | <span data-ttu-id="0f843-137">string</span><span class="sxs-lookup"><span data-stu-id="0f843-137">string</span></span> | <span data-ttu-id="0f843-138">Nome del modello.</span><span class="sxs-lookup"><span data-stu-id="0f843-138">The name of the template.</span></span><br/>                                                                                                                                                                  |
| <span data-ttu-id="0f843-139">tid</span><span class="sxs-lookup"><span data-stu-id="0f843-139">tid</span></span>  | <span data-ttu-id="0f843-140">token</span><span class="sxs-lookup"><span data-stu-id="0f843-140">token</span></span>  | <span data-ttu-id="0f843-141">Identificatore che identifica in modo univoco il modello all'interno dell'elenco di modelli definiti dal provider.</span><span class="sxs-lookup"><span data-stu-id="0f843-141">An identifier that uniquely identifies the template within the list of templates that the provider defines.</span></span> <span data-ttu-id="0f843-142">Utilizzare questo nome per fare riferimento al modello quando si definisce la definizione dell'evento.</span><span class="sxs-lookup"><span data-stu-id="0f843-142">Use this name to reference the template when you define your event definition.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0f843-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f843-143">Remarks</span></span>

<span data-ttu-id="0f843-144">La definizione del modello deve contenere almeno un elemento figlio data o struct.</span><span class="sxs-lookup"><span data-stu-id="0f843-144">The template definition must have at least one data or struct child element.</span></span> <span data-ttu-id="0f843-145">Il provider deve scrivere i dati dell'evento nell'ordine degli elementi di dati definiti nel modello.</span><span class="sxs-lookup"><span data-stu-id="0f843-145">The provider must write the event data in the order of the data items defined in the template.</span></span>

<span data-ttu-id="0f843-146">La dimensione di tutti gli elementi di dati nel modello deve essere inferiore a 64 KB.</span><span class="sxs-lookup"><span data-stu-id="0f843-146">The size of all the data items in the template must be less than 64 KB.</span></span>

## <a name="examples"></a><span data-ttu-id="0f843-147">Esempio</span><span class="sxs-lookup"><span data-stu-id="0f843-147">Examples</span></span>

<span data-ttu-id="0f843-148">Nell'esempio seguente viene illustrato come creare una definizione di modello.</span><span class="sxs-lookup"><span data-stu-id="0f843-148">The following example shows how to create a template definition.</span></span>


```XML
<templates>
   <template tid="T1">
       <data name="PrinterName" intype="win:UnicodeString" />
       <UserData>
          <PrinterConnectionFailure 
              xmlns="schemas.microsoft.com/schemas/event/Microsoft.Windows.PrintSpooler/1.0.1.0/6382e26fc390d748">
              <PrinterName>%1</PrinterName>
          </PrinterConnectionFailure>
       </xml>
   </template>
</templates>
```



## <a name="requirements"></a><span data-ttu-id="0f843-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f843-149">Requirements</span></span>



| <span data-ttu-id="0f843-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f843-150">Requirement</span></span> | <span data-ttu-id="0f843-151">Valore</span><span class="sxs-lookup"><span data-stu-id="0f843-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0f843-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f843-152">Minimum supported client</span></span><br/> | <span data-ttu-id="0f843-153">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0f843-153">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0f843-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f843-154">Minimum supported server</span></span><br/> | <span data-ttu-id="0f843-155">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0f843-155">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 






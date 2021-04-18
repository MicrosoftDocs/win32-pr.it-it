---
title: Tipo complesso TaskType
description: Definisce un componente o un sottocomponente di un'applicazione. | Tipo complesso TaskType
ms.assetid: d117636d-6363-43b6-ac5a-52234ac7c729
keywords:
- Log eventi di tipo complesso TaskType
topic_type:
- apiref
api_name:
- TaskType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ccad6813624d0a27a093ff4baa7fc8b9a6aa8b14
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321874"
---
# <a name="tasktype-complex-type"></a><span data-ttu-id="93644-105">Tipo complesso TaskType</span><span class="sxs-lookup"><span data-stu-id="93644-105">TaskType Complex Type</span></span>

<span data-ttu-id="93644-106">Definisce un componente o un sottocomponente di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="93644-106">Defines a component or subcomponent of an application.</span></span>

``` syntax
<xs:complexType name="TaskType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="opcodes"
            type="OpcodeListType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="QName"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
    <xs:attribute name="value"
        type="UInt16Type"
        use="required"
     />
    <xs:attribute name="eventGUID"
        type="GUIDType"
        use="optional"
     />
    <xs:attribute name="message"
        type="strTableRef"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="93644-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="93644-107">Child elements</span></span>



| <span data-ttu-id="93644-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="93644-108">Element</span></span>                                                         | <span data-ttu-id="93644-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="93644-109">Type</span></span>                                                                     | <span data-ttu-id="93644-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93644-110">Description</span></span>                                                                                                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93644-111">**OpCodes**</span><span class="sxs-lookup"><span data-stu-id="93644-111">**opcodes**</span></span>](eventmanifestschema-opcodes-tasktype-element.md) | [<span data-ttu-id="93644-112">**OpcodeListType**</span><span class="sxs-lookup"><span data-stu-id="93644-112">**OpcodeListType**</span></span>](eventmanifestschema-opcodelisttype-complextype.md) | <span data-ttu-id="93644-113">Definisce un elenco di codici operativi specifici dell'attività.</span><span class="sxs-lookup"><span data-stu-id="93644-113">Defines a list of task-specific opcodes.</span></span> <span data-ttu-id="93644-114">Non è possibile usare i valori opcode definiti in Winmeta.xml per i codici operativi specifici dell'attività.</span><span class="sxs-lookup"><span data-stu-id="93644-114">You cannot use the opcode values defined in Winmeta.xml for task-specific opcodes.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="93644-115">Attributi</span><span class="sxs-lookup"><span data-stu-id="93644-115">Attributes</span></span>



| <span data-ttu-id="93644-116">Nome</span><span class="sxs-lookup"><span data-stu-id="93644-116">Name</span></span>      | <span data-ttu-id="93644-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="93644-117">Type</span></span>                                                              | <span data-ttu-id="93644-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93644-118">Description</span></span>                                                                                                                                                                                                                                                                                                      |
|-----------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93644-119">eventGUID</span><span class="sxs-lookup"><span data-stu-id="93644-119">eventGUID</span></span> | [<span data-ttu-id="93644-120">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="93644-120">**GUIDType**</span></span>](eventmanifestschema-guidtype-simpletype.md)       | <span data-ttu-id="93644-121">Identificatore univoco globale, nel formato del registro di sistema, che identifica l'attività.</span><span class="sxs-lookup"><span data-stu-id="93644-121">A globally unique identifier, in Registry format, that identifies the task.</span></span> <span data-ttu-id="93644-122">Questo attributo è obbligatorio se si usa l'argomento del compilatore del messaggio-MOF per generare una classe MOF per il supporto di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="93644-122">This attribute is required if you use the -mof message compiler argument to generate a MOF class for downlevel support.</span></span><br/>                                                                                                   |
| <span data-ttu-id="93644-123">message</span><span class="sxs-lookup"><span data-stu-id="93644-123">message</span></span>   | [<span data-ttu-id="93644-124">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="93644-124">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="93644-125">Nome visualizzato localizzato per l'attività.</span><span class="sxs-lookup"><span data-stu-id="93644-125">The localized display name for the task.</span></span> <span data-ttu-id="93644-126">La stringa di messaggio fa riferimento a una stringa localizzata nella sezione [**un'STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) del manifesto.</span><span class="sxs-lookup"><span data-stu-id="93644-126">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                                   |
| <span data-ttu-id="93644-127">name</span><span class="sxs-lookup"><span data-stu-id="93644-127">name</span></span>      | <span data-ttu-id="93644-128">**QName**</span><span class="sxs-lookup"><span data-stu-id="93644-128">**QName**</span></span>                                                         | <span data-ttu-id="93644-129">Nome dell'attività.</span><span class="sxs-lookup"><span data-stu-id="93644-129">The name of the task.</span></span><br/>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="93644-130">simbolo</span><span class="sxs-lookup"><span data-stu-id="93644-130">symbol</span></span>    | [<span data-ttu-id="93644-131">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="93644-131">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="93644-132">Simbolo da utilizzare per fare riferimento all'attività nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="93644-132">The symbol to use to reference the task in your application.</span></span> <span data-ttu-id="93644-133">Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per l'attività nel file di intestazione generato dal compilatore.</span><span class="sxs-lookup"><span data-stu-id="93644-133">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the task in the header file that the compiler generates.</span></span> <span data-ttu-id="93644-134">Se non si specifica un simbolo, il compilatore ne genera uno automaticamente.</span><span class="sxs-lookup"><span data-stu-id="93644-134">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="93644-135">Valore</span><span class="sxs-lookup"><span data-stu-id="93644-135">value</span></span>     | [<span data-ttu-id="93644-136">**UInt16Type**</span><span class="sxs-lookup"><span data-stu-id="93644-136">**UInt16Type**</span></span>](eventmanifestschema-hexint16type-simpletype.md) | <span data-ttu-id="93644-137">Valore numerico che identifica in modo univoco questa attività nell'elenco delle attività definite dal provider.</span><span class="sxs-lookup"><span data-stu-id="93644-137">A numeric value that uniquely identifies this task within the list of tasks that the provider defines.</span></span> <span data-ttu-id="93644-138">Il valore deve essere compreso tra 1 e 239.</span><span class="sxs-lookup"><span data-stu-id="93644-138">The value must be in the range from 1 through 239.</span></span><br/>                                                                                                                                             |



## <a name="examples"></a><span data-ttu-id="93644-139">Esempio</span><span class="sxs-lookup"><span data-stu-id="93644-139">Examples</span></span>

<span data-ttu-id="93644-140">Nell'esempio seguente viene illustrato come specificare un'attività.</span><span class="sxs-lookup"><span data-stu-id="93644-140">The following example shows how to specify a task.</span></span>


```XML
<tasks>
  <task name="printspool:Disconnect" 
         symbol="PRINTSPOOL_TASK_DISCONNECT"
         value="0" 
         message="$(string.disconnect)"/>
 
  <task name="printspool:Connect" 
         symbol="PRINTSPOOL_TASK_CONNECT"
         value="1" 
         message="$(string.connect)">
       <opcodes>
          <opcode name="ReadRegistry" 
                  symbol="MYOPCODE_READ_REGISTRY" value="11"
                  message="$(string.ReadRegistry)"/>
       </opcodes>
   </task>
</tasks>
```



## <a name="requirements"></a><span data-ttu-id="93644-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93644-141">Requirements</span></span>



| <span data-ttu-id="93644-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="93644-142">Requirement</span></span> | <span data-ttu-id="93644-143">Valore</span><span class="sxs-lookup"><span data-stu-id="93644-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="93644-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93644-144">Minimum supported client</span></span><br/> | <span data-ttu-id="93644-145">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="93644-145">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="93644-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93644-146">Minimum supported server</span></span><br/> | <span data-ttu-id="93644-147">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="93644-147">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 






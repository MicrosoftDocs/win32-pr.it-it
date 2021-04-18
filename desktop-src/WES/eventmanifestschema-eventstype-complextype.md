---
title: Tipo complesso EventsType
description: Contiene un elenco di provider definiti nel manifesto. | Tipo complesso EventsType
ms.assetid: 43f9f577-eae0-45c5-aaf0-5a6df28d3b79
keywords:
- Log eventi di tipo complesso EventsType
topic_type:
- apiref
api_name:
- EventsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 36500aa037c8e33a48b4f9dd6e38e46eaac58da2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321539"
---
# <a name="eventstype-complex-type"></a><span data-ttu-id="a8a28-105">Tipo complesso EventsType</span><span class="sxs-lookup"><span data-stu-id="a8a28-105">EventsType Complex Type</span></span>

<span data-ttu-id="a8a28-106">Contiene un elenco di provider definiti nel manifesto.</span><span class="sxs-lookup"><span data-stu-id="a8a28-106">Contains a list of providers that are defined in the manifest.</span></span>

``` syntax
<xs:complexType name="EventsType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="provider"
            type="ProviderType"
            maxOccurs="unbounded"
         />
        <xs:element name="messageTable"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="message"
                        minOccurs="0"
                        maxOccurs="unbounded"
                    >
                        <xs:complexType>
                            <xs:attribute name="value"
                                type="UInt32Type"
                                use="required"
                             />
                            <xs:attribute name="mid"
                                type="xs:string"
                                use="optional"
                             />
                            <xs:attribute name="message"
                                type="strTableRef"
                                use="required"
                             />
                            <xs:attribute name="symbol"
                                type="CSymbolType"
                                use="optional"
                             />
                        </xs:complexType>
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:choice>
    <xs:anyAttribute
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a8a28-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="a8a28-107">Child elements</span></span>

| <span data-ttu-id="a8a28-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="a8a28-108">Element</span></span> | <span data-ttu-id="a8a28-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a8a28-109">Type</span></span> | <span data-ttu-id="a8a28-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8a28-110">Description</span></span> |
|---------|------|-------------|
| <span data-ttu-id="a8a28-111">message</span><span class="sxs-lookup"><span data-stu-id="a8a28-111">message</span></span> |      | <span data-ttu-id="a8a28-112">Definisce una stringa di messaggio.</span><span class="sxs-lookup"><span data-stu-id="a8a28-112">Defines a message string.</span></span> |
| <span data-ttu-id="a8a28-113">messageTable</span><span class="sxs-lookup"><span data-stu-id="a8a28-113">messageTable</span></span> | | <span data-ttu-id="a8a28-114">Definisce un elenco di stringhe di messaggio.</span><span class="sxs-lookup"><span data-stu-id="a8a28-114">Defines a list of message strings.</span></span> <span data-ttu-id="a8a28-115">Non è necessario utilizzare una tabella messaggi tranne nei casi seguenti, in cui è necessario definire una tabella messaggi per assegnare in modo esplicito i numeri delle risorse alle stringhe di messaggio.</span><span class="sxs-lookup"><span data-stu-id="a8a28-115">You should not have to use a message table except in the following cases where you must define a message table to explicitly assign resource numbers to message strings.</span></span> <ul><li><span data-ttu-id="a8a28-116">Si esegue la migrazione da un file di testo del messaggio (. MC) a un manifesto, ma si stanno ancora scrivendo eventi ai canali dell'applicazione e di sistema, in modo che i consumer legacy continuino a utilizzarli.</span><span class="sxs-lookup"><span data-stu-id="a8a28-116">You are migrating from a message text (.mc) file to a manifest but are still writing events to the application and system channels, so that legacy consumers to continue consuming the events.</span></span> <span data-ttu-id="a8a28-117">Per eseguire questa operazione, gli identificatori di risorsa per le stringhe di messaggio definite nel manifesto devono corrispondere agli identificatori di evento.</span><span class="sxs-lookup"><span data-stu-id="a8a28-117">To make this work, the resource identifiers for the message strings defined in the manifest must be the same as the event identifiers.</span></span> <span data-ttu-id="a8a28-118">Tuttavia, il compilatore di messaggi assegna automaticamente gli identificatori di risorsa alle stringhe di messaggio.</span><span class="sxs-lookup"><span data-stu-id="a8a28-118">However, the message compiler automatically assigns resource identifiers to the message strings.</span></span> <span data-ttu-id="a8a28-119">Per eseguire l'override del compilatore, utilizzare la tabella Message e impostare l'attributo value sull'identificatore dell'evento e l'attributo Message per fare riferimento a una stringa nella tabella di stringhe nella sezione localizzazione del manifesto.</span><span class="sxs-lookup"><span data-stu-id="a8a28-119">To override the compiler, use the message table and set the value attribute to the event identifier and the message attribute to refer to a string in the string table in the localization section of the manifest.</span></span></li><li><span data-ttu-id="a8a28-120">Se si desidera identificare più di 16 provider, è necessario includere la tabella dei messaggi che i provider XVII e su devono utilizzare per assegnare i valori delle risorse per le stringhe di messaggio definite.</span><span class="sxs-lookup"><span data-stu-id="a8a28-120">If you want to identify more than 16 providers, you must include the message table that the seventeenth and on providers must use to assign resource values for the message strings that they define.</span></span> <span data-ttu-id="a8a28-121">Se il provider fa riferimento a stringhe di messaggio che sono definite da 1 a 16, le stringhe di messaggio non vengono incluse nella tabella messaggi.</span><span class="sxs-lookup"><span data-stu-id="a8a28-121">If the provider references message strings that providers 1 through 16 defined, you do not include those message strings in the message table.</span></span></li></ul>|
| [<span data-ttu-id="a8a28-122">**provider**</span><span class="sxs-lookup"><span data-stu-id="a8a28-122">**provider**</span></span>](eventmanifestschema-provider-eventstype-element.md) | [<span data-ttu-id="a8a28-123">**ProviderType**</span><span class="sxs-lookup"><span data-stu-id="a8a28-123">**ProviderType**</span></span>](eventmanifestschema-providertype-complextype.md) | <span data-ttu-id="a8a28-124">Elenco di provider che si desidera definire.</span><span class="sxs-lookup"><span data-stu-id="a8a28-124">A list of providers that you want to define.</span></span> |

## <a name="attributes"></a><span data-ttu-id="a8a28-125">Attributi</span><span class="sxs-lookup"><span data-stu-id="a8a28-125">Attributes</span></span>

| <span data-ttu-id="a8a28-126">Nome</span><span class="sxs-lookup"><span data-stu-id="a8a28-126">Name</span></span>    | <span data-ttu-id="a8a28-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="a8a28-127">Type</span></span>                                                             | <span data-ttu-id="a8a28-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8a28-128">Description</span></span>                                                                            |
|---------|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8a28-129">message</span><span class="sxs-lookup"><span data-stu-id="a8a28-129">message</span></span> | [<span data-ttu-id="a8a28-130">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="a8a28-130">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="a8a28-131">Riferimento alla stringa localizzata nella tabella di stringhe.</span><span class="sxs-lookup"><span data-stu-id="a8a28-131">A reference to the localized string in the string table.</span></span>                               |
| <span data-ttu-id="a8a28-132">mid</span><span class="sxs-lookup"><span data-stu-id="a8a28-132">mid</span></span>     | <span data-ttu-id="a8a28-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="a8a28-133">xs:string</span></span>                                                        | <span data-ttu-id="a8a28-134">Non usato.</span><span class="sxs-lookup"><span data-stu-id="a8a28-134">Not used.</span></span>                                                                              |
| <span data-ttu-id="a8a28-135">simbolo</span><span class="sxs-lookup"><span data-stu-id="a8a28-135">symbol</span></span>  | [<span data-ttu-id="a8a28-136">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="a8a28-136">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="a8a28-137">Nome simbolico che si desidera venga creato dal compilatore di messaggi per questa stringa di messaggio.</span><span class="sxs-lookup"><span data-stu-id="a8a28-137">The symbolic name that you want the message compiler to create for this message string.</span></span>|
| <span data-ttu-id="a8a28-138">Valore</span><span class="sxs-lookup"><span data-stu-id="a8a28-138">value</span></span>   | [<span data-ttu-id="a8a28-139">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="a8a28-139">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="a8a28-140">Numero da utilizzare come identificatore del messaggio per questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="a8a28-140">The number to use as the message identifier for this message.</span></span>                          |


## <a name="remarks"></a><span data-ttu-id="a8a28-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="a8a28-141">Remarks</span></span>

<span data-ttu-id="a8a28-142">Il limite pratico del numero di provider che è possibile definire in un manifesto è 16 provider.</span><span class="sxs-lookup"><span data-stu-id="a8a28-142">The practical limit of the number of providers that you can define in a manifest is 16 providers.</span></span> <span data-ttu-id="a8a28-143">Se si specificano più di 16 provider, è necessario utilizzare una tabella messaggi per assegnare in modo esplicito i numeri delle risorse alle stringhe di messaggio a cui fa riferimento il provider.</span><span class="sxs-lookup"><span data-stu-id="a8a28-143">If you specify more than 16 providers, you must use a message table to explicitly assign resource numbers to the message strings that the provider references.</span></span> <span data-ttu-id="a8a28-144">Per ulteriori informazioni, vedere l'elemento Message sopra riportato.</span><span class="sxs-lookup"><span data-stu-id="a8a28-144">For more details, see the message element above.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8a28-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8a28-145">Requirements</span></span>

| <span data-ttu-id="a8a28-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8a28-146">Requirement</span></span> | <span data-ttu-id="a8a28-147">Valore</span><span class="sxs-lookup"><span data-stu-id="a8a28-147">Value</span></span> |
|--------------------------|-------------------------------------------|
| <span data-ttu-id="a8a28-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8a28-148">Minimum supported client</span></span> | <span data-ttu-id="a8a28-149">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a8a28-149">Windows Vista \[desktop apps only\]</span></span>       |
| <span data-ttu-id="a8a28-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a8a28-150">Minimum supported server</span></span> | <span data-ttu-id="a8a28-151">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a8a28-151">Windows Server 2008 \[desktop apps only\]</span></span> |

---
title: Tipo complesso LevelType
description: Definisce un valore di gravità che determina il livello di dettaglio degli eventi registrati.
ms.assetid: c71aedef-7c43-4343-9d6d-94eb45da49b9
keywords:
- Log eventi di tipo complesso LevelType
topic_type:
- apiref
api_name:
- LevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 237b38890283769e9aac20c9b3a3703ff4b72d3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119039"
---
# <a name="leveltype-complex-type"></a><span data-ttu-id="7c4f8-104">Tipo complesso LevelType</span><span class="sxs-lookup"><span data-stu-id="7c4f8-104">LevelType Complex Type</span></span>

<span data-ttu-id="7c4f8-105">Definisce un valore di gravità che determina il livello di dettaglio degli eventi registrati.</span><span class="sxs-lookup"><span data-stu-id="7c4f8-105">Defines a severity value that determines the verbosity of the events being logged.</span></span>

``` syntax
<xs:complexType name="LevelType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
        >
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="value"
                type="UInt8Type"
                use="required"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="7c4f8-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="7c4f8-106">Attributes</span></span>



| <span data-ttu-id="7c4f8-107">Nome</span><span class="sxs-lookup"><span data-stu-id="7c4f8-107">Name</span></span>    | <span data-ttu-id="7c4f8-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="7c4f8-108">Type</span></span>                                                              | <span data-ttu-id="7c4f8-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c4f8-109">Description</span></span>                                                                                                                                                                                                                                                                                                        |
|---------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c4f8-110">message</span><span class="sxs-lookup"><span data-stu-id="7c4f8-110">message</span></span> | [<span data-ttu-id="7c4f8-111">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="7c4f8-111">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="7c4f8-112">Nome visualizzato localizzato per il livello.</span><span class="sxs-lookup"><span data-stu-id="7c4f8-112">The localized display name for the level.</span></span> <span data-ttu-id="7c4f8-113">La stringa di messaggio fa riferimento a una stringa localizzata nella sezione [**un'STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) del manifesto.</span><span class="sxs-lookup"><span data-stu-id="7c4f8-113">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                                    |
| <span data-ttu-id="7c4f8-114">name</span><span class="sxs-lookup"><span data-stu-id="7c4f8-114">name</span></span>    | <span data-ttu-id="7c4f8-115">**QName**</span><span class="sxs-lookup"><span data-stu-id="7c4f8-115">**QName**</span></span>                                                         | <span data-ttu-id="7c4f8-116">Nome da assegnare a questo livello.</span><span class="sxs-lookup"><span data-stu-id="7c4f8-116">The name to assign to this level.</span></span> <span data-ttu-id="7c4f8-117">Questo nome deve essere univoco all'interno dell'ambito del provider.</span><span class="sxs-lookup"><span data-stu-id="7c4f8-117">This name must be unique within the scope of the provider.</span></span><br/>                                                                                                                                                                                                            |
| <span data-ttu-id="7c4f8-118">simbolo</span><span class="sxs-lookup"><span data-stu-id="7c4f8-118">symbol</span></span>  | [<span data-ttu-id="7c4f8-119">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="7c4f8-119">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="7c4f8-120">Simbolo da usare per fare riferimento al livello nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7c4f8-120">The symbol to use to reference the level in your application.</span></span> <span data-ttu-id="7c4f8-121">Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per il livello nel file di intestazione generato dal compilatore.</span><span class="sxs-lookup"><span data-stu-id="7c4f8-121">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the level in the header file that the compiler generates.</span></span> <span data-ttu-id="7c4f8-122">Se non si specifica un simbolo, il compilatore ne genera uno automaticamente.</span><span class="sxs-lookup"><span data-stu-id="7c4f8-122">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="7c4f8-123">Valore</span><span class="sxs-lookup"><span data-stu-id="7c4f8-123">value</span></span>   | [<span data-ttu-id="7c4f8-124">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="7c4f8-124">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="7c4f8-125">Valore del livello.</span><span class="sxs-lookup"><span data-stu-id="7c4f8-125">The level value.</span></span> <span data-ttu-id="7c4f8-126">È possibile specificare valori compresi tra 16 e 255.</span><span class="sxs-lookup"><span data-stu-id="7c4f8-126">You can specify values in the range 16 to 255.</span></span> <span data-ttu-id="7c4f8-127">Per i valori di livello predefiniti, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="7c4f8-127">For predefined level values, see Remarks.</span></span><br/>                                                                                                                                                                                               |



## <a name="remarks"></a><span data-ttu-id="7c4f8-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="7c4f8-128">Remarks</span></span>

<span data-ttu-id="7c4f8-129">Di seguito sono riportati i valori di livello predefiniti che è possibile utilizzare.</span><span class="sxs-lookup"><span data-stu-id="7c4f8-129">The following are the predefined level values that you can use.</span></span> <span data-ttu-id="7c4f8-130">Questi valori vengono definiti nel file di Winmeta.xml incluso nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="7c4f8-130">These values are defined in the Winmeta.xml file that is included in the Windows SDK.</span></span>



| <span data-ttu-id="7c4f8-131">Nome</span><span class="sxs-lookup"><span data-stu-id="7c4f8-131">Name</span></span>              | <span data-ttu-id="7c4f8-132">Valore</span><span class="sxs-lookup"><span data-stu-id="7c4f8-132">Value</span></span> | <span data-ttu-id="7c4f8-133">Simbolo</span><span class="sxs-lookup"><span data-stu-id="7c4f8-133">Symbol</span></span>                    | <span data-ttu-id="7c4f8-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c4f8-134">Description</span></span>                                                             |
|-------------------|-------|---------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="7c4f8-135">win:Critical</span><span class="sxs-lookup"><span data-stu-id="7c4f8-135">win:Critical</span></span>      | <span data-ttu-id="7c4f8-136">1</span><span class="sxs-lookup"><span data-stu-id="7c4f8-136">1</span></span>     | <span data-ttu-id="7c4f8-137">livello di WINEVENT \_ \_ critico</span><span class="sxs-lookup"><span data-stu-id="7c4f8-137">WINEVENT\_LEVEL\_CRITICAL</span></span> | <span data-ttu-id="7c4f8-138">Identifica un evento di chiusura o chiusura anomalo.</span><span class="sxs-lookup"><span data-stu-id="7c4f8-138">Identifies an abnormal exit or termination event.</span></span><br/>            |
| <span data-ttu-id="7c4f8-139">win:Error</span><span class="sxs-lookup"><span data-stu-id="7c4f8-139">win:Error</span></span>         | <span data-ttu-id="7c4f8-140">2</span><span class="sxs-lookup"><span data-stu-id="7c4f8-140">2</span></span>     | <span data-ttu-id="7c4f8-141">\_errore a livello di WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="7c4f8-141">WINEVENT\_LEVEL\_ERROR</span></span>    | <span data-ttu-id="7c4f8-142">Identifica un evento di errore grave.</span><span class="sxs-lookup"><span data-stu-id="7c4f8-142">Identifies a severe error event.</span></span><br/>                             |
| <span data-ttu-id="7c4f8-143">win:Warning</span><span class="sxs-lookup"><span data-stu-id="7c4f8-143">win:Warning</span></span>       | <span data-ttu-id="7c4f8-144">3</span><span class="sxs-lookup"><span data-stu-id="7c4f8-144">3</span></span>     | <span data-ttu-id="7c4f8-145">\_avviso livello \_ WINEVENT</span><span class="sxs-lookup"><span data-stu-id="7c4f8-145">WINEVENT\_LEVEL\_WARNING</span></span>  | <span data-ttu-id="7c4f8-146">Identifica un evento di avviso, ad esempio un errore di allocazione.</span><span class="sxs-lookup"><span data-stu-id="7c4f8-146">Identifies a warning event such as an allocation failure.</span></span><br/>    |
| <span data-ttu-id="7c4f8-147">win:Informational</span><span class="sxs-lookup"><span data-stu-id="7c4f8-147">win:Informational</span></span> | <span data-ttu-id="7c4f8-148">4</span><span class="sxs-lookup"><span data-stu-id="7c4f8-148">4</span></span>     | <span data-ttu-id="7c4f8-149">\_informazioni sul livello di WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="7c4f8-149">WINEVENT\_LEVEL\_INFO</span></span>     | <span data-ttu-id="7c4f8-150">Identifica un evento non di errore, ad esempio un evento di ingresso o di uscita.</span><span class="sxs-lookup"><span data-stu-id="7c4f8-150">Identifies a non-error event such as an entry or exit event.</span></span><br/> |
| <span data-ttu-id="7c4f8-151">win:Verbose</span><span class="sxs-lookup"><span data-stu-id="7c4f8-151">win:Verbose</span></span>       | <span data-ttu-id="7c4f8-152">5</span><span class="sxs-lookup"><span data-stu-id="7c4f8-152">5</span></span>     | <span data-ttu-id="7c4f8-153">\_dettagliato livello \_ WINEVENT</span><span class="sxs-lookup"><span data-stu-id="7c4f8-153">WINEVENT\_LEVEL\_VERBOSE</span></span>  | <span data-ttu-id="7c4f8-154">Identifica un evento di traccia dettagliato.</span><span class="sxs-lookup"><span data-stu-id="7c4f8-154">Identifies a detailed trace event.</span></span><br/>                           |



 

<span data-ttu-id="7c4f8-155">I numeri più alti implicano che si ottengono anche livelli inferiori.</span><span class="sxs-lookup"><span data-stu-id="7c4f8-155">Higher numbers imply that you get lower levels as well.</span></span> <span data-ttu-id="7c4f8-156">Se ad esempio si specifica Win: Warning, vengono visualizzati tutti gli eventi di avviso, di errore e di importanza critica.</span><span class="sxs-lookup"><span data-stu-id="7c4f8-156">For example, if you specify win:Warning, you receive all warning, error, and critical events.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c4f8-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c4f8-157">Requirements</span></span>



| <span data-ttu-id="7c4f8-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c4f8-158">Requirement</span></span> | <span data-ttu-id="7c4f8-159">Valore</span><span class="sxs-lookup"><span data-stu-id="7c4f8-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7c4f8-160">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c4f8-160">Minimum supported client</span></span><br/> | <span data-ttu-id="7c4f8-161">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7c4f8-161">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7c4f8-162">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c4f8-162">Minimum supported server</span></span><br/> | <span data-ttu-id="7c4f8-163">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7c4f8-163">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 






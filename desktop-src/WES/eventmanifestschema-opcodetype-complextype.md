---
title: Tipo complesso OpcodeType
description: Definisce un'operazione all'interno di un componente dell'applicazione.
ms.assetid: d97953df-669b-4c55-b1a8-925022b339b7
keywords:
- Log eventi di tipo complesso OpcodeType
topic_type:
- apiref
api_name:
- OpcodeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e5abaa11373086fe7f1237e10daf3e0a3df1cdb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121334"
---
# <a name="opcodetype-complex-type"></a><span data-ttu-id="17557-104">Tipo complesso OpcodeType</span><span class="sxs-lookup"><span data-stu-id="17557-104">OpcodeType Complex Type</span></span>

<span data-ttu-id="17557-105">Definisce un'operazione all'interno di un componente dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="17557-105">Defines an operation within a component of the application.</span></span> <span data-ttu-id="17557-106">Utilizzato insieme a un'attività per identificare la sezione dell'applicazione che registra l'evento.</span><span class="sxs-lookup"><span data-stu-id="17557-106">Used in conjunction with a task to identify the section of the application that is logging the event.</span></span>

``` syntax
<xs:complexType name="OpcodeType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
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
            <xs:attribute name="mofValue"
                type="UInt8Type"
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
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="17557-107">Attributi</span><span class="sxs-lookup"><span data-stu-id="17557-107">Attributes</span></span>



| <span data-ttu-id="17557-108">Nome</span><span class="sxs-lookup"><span data-stu-id="17557-108">Name</span></span>     | <span data-ttu-id="17557-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="17557-109">Type</span></span>                                                              | <span data-ttu-id="17557-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="17557-110">Description</span></span>                                                                                                                                                                                                                                                                                                          |
|----------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17557-111">message</span><span class="sxs-lookup"><span data-stu-id="17557-111">message</span></span>  | [<span data-ttu-id="17557-112">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="17557-112">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="17557-113">Nome visualizzato localizzato per il codice operativo.</span><span class="sxs-lookup"><span data-stu-id="17557-113">The localized display name for the opcode.</span></span> <span data-ttu-id="17557-114">La stringa di messaggio fa riferimento a una stringa localizzata nella sezione [**un'STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) del manifesto.</span><span class="sxs-lookup"><span data-stu-id="17557-114">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                                     |
| <span data-ttu-id="17557-115">mofValue</span><span class="sxs-lookup"><span data-stu-id="17557-115">mofValue</span></span> | [<span data-ttu-id="17557-116">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="17557-116">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="17557-117">Riservato esclusivamente per uso interno.</span><span class="sxs-lookup"><span data-stu-id="17557-117">Reserved for internal use only.</span></span><br/>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="17557-118">name</span><span class="sxs-lookup"><span data-stu-id="17557-118">name</span></span>     | <span data-ttu-id="17557-119">**QName**</span><span class="sxs-lookup"><span data-stu-id="17557-119">**QName**</span></span>                                                         | <span data-ttu-id="17557-120">Nome del codice operativo.</span><span class="sxs-lookup"><span data-stu-id="17557-120">The name of the opcode.</span></span> <span data-ttu-id="17557-121">Questo nome deve essere univoco all'interno dell'ambito di questo provider.</span><span class="sxs-lookup"><span data-stu-id="17557-121">This name must be unique within the scope of this provider.</span></span> <br/>                                                                                                                                                                                                                      |
| <span data-ttu-id="17557-122">simbolo</span><span class="sxs-lookup"><span data-stu-id="17557-122">symbol</span></span>   | [<span data-ttu-id="17557-123">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="17557-123">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="17557-124">Simbolo da utilizzare per fare riferimento al codice operativo nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="17557-124">The symbol to use to reference the opcode in your application.</span></span> <span data-ttu-id="17557-125">Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per il codice operativo nel file di intestazione generato dal compilatore.</span><span class="sxs-lookup"><span data-stu-id="17557-125">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the opcode in the header file that the compiler generates.</span></span> <span data-ttu-id="17557-126">Se non si specifica un simbolo, il compilatore ne genera uno automaticamente.</span><span class="sxs-lookup"><span data-stu-id="17557-126">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="17557-127">Valore</span><span class="sxs-lookup"><span data-stu-id="17557-127">value</span></span>    | [<span data-ttu-id="17557-128">**UInt8Type**</span><span class="sxs-lookup"><span data-stu-id="17557-128">**UInt8Type**</span></span>](eventmanifestschema-hexint8type-simpletype.md)   | <span data-ttu-id="17557-129">Valore OpCode.</span><span class="sxs-lookup"><span data-stu-id="17557-129">The opcode value.</span></span> <span data-ttu-id="17557-130">È possibile specificare valori compresi tra 10 e 239.</span><span class="sxs-lookup"><span data-stu-id="17557-130">You can specify values in the range 10 and 239.</span></span> <span data-ttu-id="17557-131">Per un elenco di valori opcode predefiniti, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="17557-131">For a list of predefined opcode values, see Remarks.</span></span><br/>                                                                                                                                                                                    |



## <a name="remarks"></a><span data-ttu-id="17557-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="17557-132">Remarks</span></span>

<span data-ttu-id="17557-133">Di seguito sono riportati i valori opcode predefiniti che è possibile utilizzare.</span><span class="sxs-lookup"><span data-stu-id="17557-133">The following are the predefined opcode values that you can use.</span></span> <span data-ttu-id="17557-134">Questi valori vengono definiti nel file di Winmeta.xml incluso nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="17557-134">These values are defined in the Winmeta.xml file that is included in the Windows SDK.</span></span>



| <span data-ttu-id="17557-135">Nome</span><span class="sxs-lookup"><span data-stu-id="17557-135">Name</span></span>          | <span data-ttu-id="17557-136">Valore</span><span class="sxs-lookup"><span data-stu-id="17557-136">Value</span></span> | <span data-ttu-id="17557-137">Simbolo</span><span class="sxs-lookup"><span data-stu-id="17557-137">Symbol</span></span>                      | <span data-ttu-id="17557-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="17557-138">Description</span></span>                                                                                            |
|---------------|-------|-----------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17557-139">Win: info</span><span class="sxs-lookup"><span data-stu-id="17557-139">win:Info</span></span>      | <span data-ttu-id="17557-140">0</span><span class="sxs-lookup"><span data-stu-id="17557-140">0</span></span>     | <span data-ttu-id="17557-141">\_informazioni OPCODE \_ WINEVENT</span><span class="sxs-lookup"><span data-stu-id="17557-141">WINEVENT\_OPCODE\_INFO</span></span>      | <span data-ttu-id="17557-142">Evento informativo.</span><span class="sxs-lookup"><span data-stu-id="17557-142">An informational event.</span></span>                                                                                |
| <span data-ttu-id="17557-143">Win: avvio</span><span class="sxs-lookup"><span data-stu-id="17557-143">win:Start</span></span>     | <span data-ttu-id="17557-144">1</span><span class="sxs-lookup"><span data-stu-id="17557-144">1</span></span>     | <span data-ttu-id="17557-145">\_avvio OPCODE \_ WINEVENT</span><span class="sxs-lookup"><span data-stu-id="17557-145">WINEVENT\_OPCODE\_START</span></span>     | <span data-ttu-id="17557-146">Evento che rappresenta l'avvio di un'attività.</span><span class="sxs-lookup"><span data-stu-id="17557-146">An event that represents starting an activity.</span></span>                                                         |
| <span data-ttu-id="17557-147">Win: arresta</span><span class="sxs-lookup"><span data-stu-id="17557-147">win:Stop</span></span>      | <span data-ttu-id="17557-148">2</span><span class="sxs-lookup"><span data-stu-id="17557-148">2</span></span>     | <span data-ttu-id="17557-149">WINEVENT \_ OPCODE \_ Stop</span><span class="sxs-lookup"><span data-stu-id="17557-149">WINEVENT\_OPCODE\_STOP</span></span>      | <span data-ttu-id="17557-150">Evento che rappresenta l'arresto di un'attività.</span><span class="sxs-lookup"><span data-stu-id="17557-150">An event that represents stopping an activity.</span></span> <span data-ttu-id="17557-151">L'evento corrisponde all'ultimo evento di inizio non associato.</span><span class="sxs-lookup"><span data-stu-id="17557-151">The event corresponds to the last unpaired start event.</span></span> |
| <span data-ttu-id="17557-152">Win: avvio del controller di dominio \_</span><span class="sxs-lookup"><span data-stu-id="17557-152">win:DC\_Start</span></span> | <span data-ttu-id="17557-153">3</span><span class="sxs-lookup"><span data-stu-id="17557-153">3</span></span>     | <span data-ttu-id="17557-154">avvio del controller di dominio \_ OPCODE WINEVENT \_ \_</span><span class="sxs-lookup"><span data-stu-id="17557-154">WINEVENT\_OPCODE\_DC\_START</span></span> | <span data-ttu-id="17557-155">Evento che rappresenta l'avvio della raccolta dati.</span><span class="sxs-lookup"><span data-stu-id="17557-155">An event that represents data collection starting.</span></span> <span data-ttu-id="17557-156">Si tratta di tipi di evento rundown.</span><span class="sxs-lookup"><span data-stu-id="17557-156">These are rundown event types.</span></span>                      |
| <span data-ttu-id="17557-157">Win: arresto del controller di dominio \_</span><span class="sxs-lookup"><span data-stu-id="17557-157">win:DC\_Stop</span></span>  | <span data-ttu-id="17557-158">4</span><span class="sxs-lookup"><span data-stu-id="17557-158">4</span></span>     | <span data-ttu-id="17557-159">WINEVENT \_ OPCODE \_ DC \_ Stop</span><span class="sxs-lookup"><span data-stu-id="17557-159">WINEVENT\_OPCODE\_DC\_STOP</span></span>  | <span data-ttu-id="17557-160">Evento che rappresenta l'arresto della raccolta dati.</span><span class="sxs-lookup"><span data-stu-id="17557-160">An event that represents data collection stopping.</span></span> <span data-ttu-id="17557-161">Si tratta di tipi di evento rundown.</span><span class="sxs-lookup"><span data-stu-id="17557-161">These are rundown event types.</span></span>                      |
| <span data-ttu-id="17557-162">Win: estensione</span><span class="sxs-lookup"><span data-stu-id="17557-162">win:Extension</span></span> | <span data-ttu-id="17557-163">5</span><span class="sxs-lookup"><span data-stu-id="17557-163">5</span></span>     | <span data-ttu-id="17557-164">\_estensione OPCODE \_ WINEVENT</span><span class="sxs-lookup"><span data-stu-id="17557-164">WINEVENT\_OPCODE\_EXTENSION</span></span> | <span data-ttu-id="17557-165">Evento di estensione.</span><span class="sxs-lookup"><span data-stu-id="17557-165">An extension event.</span></span>                                                                                    |
| <span data-ttu-id="17557-166">Win: risposta</span><span class="sxs-lookup"><span data-stu-id="17557-166">win:Reply</span></span>     | <span data-ttu-id="17557-167">6</span><span class="sxs-lookup"><span data-stu-id="17557-167">6</span></span>     | <span data-ttu-id="17557-168">\_risposta OPCODE \_ WINEVENT</span><span class="sxs-lookup"><span data-stu-id="17557-168">WINEVENT\_OPCODE\_REPLY</span></span>     | <span data-ttu-id="17557-169">Un evento di risposta.</span><span class="sxs-lookup"><span data-stu-id="17557-169">A reply event.</span></span>                                                                                         |
| <span data-ttu-id="17557-170">Win: Resume</span><span class="sxs-lookup"><span data-stu-id="17557-170">win:Resume</span></span>    | <span data-ttu-id="17557-171">7</span><span class="sxs-lookup"><span data-stu-id="17557-171">7</span></span>     | <span data-ttu-id="17557-172">\_riavvio del codice operativo WINEVENT \_</span><span class="sxs-lookup"><span data-stu-id="17557-172">WINEVENT\_OPCODE\_RESUME</span></span>    | <span data-ttu-id="17557-173">Evento che rappresenta una ripresa dell'attività dopo la sospensione.</span><span class="sxs-lookup"><span data-stu-id="17557-173">An event that represents an activity resuming after being suspended.</span></span>                                   |
| <span data-ttu-id="17557-174">Win: sospensione</span><span class="sxs-lookup"><span data-stu-id="17557-174">win:Suspend</span></span>   | <span data-ttu-id="17557-175">8</span><span class="sxs-lookup"><span data-stu-id="17557-175">8</span></span>     | <span data-ttu-id="17557-176">\_sospensione OPCODE \_ WINEVENT</span><span class="sxs-lookup"><span data-stu-id="17557-176">WINEVENT\_OPCODE\_SUSPEND</span></span>   | <span data-ttu-id="17557-177">Evento che rappresenta l'attività sospesa in attesa del completamento di un'altra attività.</span><span class="sxs-lookup"><span data-stu-id="17557-177">An event that represents the activity being suspended pending another activity's completion.</span></span>           |
| <span data-ttu-id="17557-178">Win: invio</span><span class="sxs-lookup"><span data-stu-id="17557-178">win:Send</span></span>      | <span data-ttu-id="17557-179">9</span><span class="sxs-lookup"><span data-stu-id="17557-179">9</span></span>     | <span data-ttu-id="17557-180">\_invio OPCODE \_ WINEVENT</span><span class="sxs-lookup"><span data-stu-id="17557-180">WINEVENT\_OPCODE\_SEND</span></span>      | <span data-ttu-id="17557-181">Evento che rappresenta il trasferimento dell'attività a un altro componente.</span><span class="sxs-lookup"><span data-stu-id="17557-181">An event that represents transferring activity to another component.</span></span>                                   |
| <span data-ttu-id="17557-182">Win: ricezione</span><span class="sxs-lookup"><span data-stu-id="17557-182">win:Receive</span></span>   | <span data-ttu-id="17557-183">240</span><span class="sxs-lookup"><span data-stu-id="17557-183">240</span></span>   | <span data-ttu-id="17557-184">\_ricezione OPCODE \_ WINEVENT</span><span class="sxs-lookup"><span data-stu-id="17557-184">WINEVENT\_OPCODE\_RECEIVE</span></span>   | <span data-ttu-id="17557-185">Evento che rappresenta la ricezione di un trasferimento di attività da un altro componente.</span><span class="sxs-lookup"><span data-stu-id="17557-185">An event that represents receiving an activity transfer from another component.</span></span>                        |



 

## <a name="requirements"></a><span data-ttu-id="17557-186">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17557-186">Requirements</span></span>



| <span data-ttu-id="17557-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="17557-187">Requirement</span></span> | <span data-ttu-id="17557-188">Valore</span><span class="sxs-lookup"><span data-stu-id="17557-188">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="17557-189">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17557-189">Minimum supported client</span></span><br/> | <span data-ttu-id="17557-190">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="17557-190">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="17557-191">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17557-191">Minimum supported server</span></span><br/> | <span data-ttu-id="17557-192">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="17557-192">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 






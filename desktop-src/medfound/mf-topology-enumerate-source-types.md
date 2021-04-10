---
description: Specifica se il caricatore della topologia enumera i tipi di supporto forniti dall'origine multimediale.
ms.assetid: 2675ef16-2018-47e8-bb22-2fc0d62e6681
title: Attributo MF_TOPOLOGY_ENUMERATE_SOURCE_TYPES (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015042bbf9994f81058c621239224196e6ec9ac8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343311"
---
# <a name="mf_topology_enumerate_source_types-attribute"></a><span data-ttu-id="8c8d1-103">\_Attributo della topologia MF \_ enumerazione di \_ tipi di origine \_</span><span class="sxs-lookup"><span data-stu-id="8c8d1-103">MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute</span></span>

<span data-ttu-id="8c8d1-104">Specifica se il caricatore della topologia enumera i tipi di supporto forniti dall'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="8c8d1-104">Specifies whether the topology loader enumerates the media types provided by the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="8c8d1-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="8c8d1-105">Data type</span></span>

<span data-ttu-id="8c8d1-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="8c8d1-106">**UINT32**</span></span>

<span data-ttu-id="8c8d1-107">Usare uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="8c8d1-107">Use one of the following values.</span></span>



| <span data-ttu-id="8c8d1-108">Valore</span><span class="sxs-lookup"><span data-stu-id="8c8d1-108">Value</span></span>                                                                                                                                    | <span data-ttu-id="8c8d1-109">Significato</span><span class="sxs-lookup"><span data-stu-id="8c8d1-109">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="8c8d1-110"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="8c8d1-110"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="8c8d1-111">Non enumerare i tipi di supporto di origine.</span><span class="sxs-lookup"><span data-stu-id="8c8d1-111">Do not enumerate the source media types.</span></span><br/> |
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="8c8d1-112"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="8c8d1-112"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="8c8d1-113">Enumerare i tipi di supporto di origine.</span><span class="sxs-lookup"><span data-stu-id="8c8d1-113">Enumerate the source media types.</span></span><br/>        |



 

## <a name="getset"></a><span data-ttu-id="8c8d1-114">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="8c8d1-114">Get/set</span></span>

<span data-ttu-id="8c8d1-115">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="8c8d1-115">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="8c8d1-116">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="8c8d1-116">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="8c8d1-117">Si applica a</span><span class="sxs-lookup"><span data-stu-id="8c8d1-117">Applies to</span></span>

[<span data-ttu-id="8c8d1-118">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="8c8d1-118">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="8c8d1-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="8c8d1-119">Remarks</span></span>

<span data-ttu-id="8c8d1-120">Ogni flusso in un'origine multimediale può offrire più di un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="8c8d1-120">Each stream on a media source can offer more than one media type.</span></span> <span data-ttu-id="8c8d1-121">L'elenco dei tipi viene enumerato tramite l'interfaccia [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) sul descrittore del flusso.</span><span class="sxs-lookup"><span data-stu-id="8c8d1-121">The list of types is enumerated through the [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) interface on the stream descriptor.</span></span>

<span data-ttu-id="8c8d1-122">L'ordine in cui il caricatore della topologia Cerca i tipi di supporto di un'origine multimediale è controllato da due attributi:</span><span class="sxs-lookup"><span data-stu-id="8c8d1-122">The order in which the topology loader tries a media source's media types is controlled by two attributes:</span></span>

-   <span data-ttu-id="8c8d1-123">L' \_ attributo della topologia MF \_ enumera \_ \_ i tipi di origine nella topologia.</span><span class="sxs-lookup"><span data-stu-id="8c8d1-123">The MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute on the topology.</span></span>
-   <span data-ttu-id="8c8d1-124">Attributo [**del \_ \_ \_ Metodo MF TOPONODE Connect**](mf-toponode-connect-method-attribute.md) nel nodo di origine.</span><span class="sxs-lookup"><span data-stu-id="8c8d1-124">The [**MF\_TOPONODE\_CONNECT\_METHOD**](mf-toponode-connect-method-attribute.md) attribute on the source node.</span></span>

<span data-ttu-id="8c8d1-125">Se l' \_ attributo della topologia MF \_ enumerazione dei \_ \_ tipi di origine è **false** o non impostato, il caricatore della topologia usa il tipo di supporto corrente del flusso.</span><span class="sxs-lookup"><span data-stu-id="8c8d1-125">If the MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute is **FALSE** or not set, the topology loader uses the stream's current media type.</span></span> <span data-ttu-id="8c8d1-126">Non enumera l'elenco dei tipi possibili.</span><span class="sxs-lookup"><span data-stu-id="8c8d1-126">It does not enumerate the list of possible types.</span></span> <span data-ttu-id="8c8d1-127">Se il tipo di supporto corrente non è compatibile con il nodo della topologia downstream e non è possibile trovare una combinazione di decodificatori/convertitori, la risoluzione della topologia ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="8c8d1-127">If the current media type is incompatible with the downstream topology node, and no combination of decoders/converters can be found, topology resolution fails.</span></span>

<span data-ttu-id="8c8d1-128">Se l' \_ attributo della topologia MF \_ enumerazione dei tipi di \_ origine \_ è **true**, il caricatore della topologia enumera i tipi di supporto dell'origine finché non trova un tipo compatibile.</span><span class="sxs-lookup"><span data-stu-id="8c8d1-128">If the MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute is **TRUE**, the topology loader enumerates the source's media types until it finds a compatible type.</span></span> <span data-ttu-id="8c8d1-129">In tal caso, l'ordine esatto delle operazioni varia a seconda che l'attributo [**del \_ \_ \_ Metodo MF TOPONODE Connect**](mf-toponode-connect-method-attribute.md) nel nodo di origine includa il flag OutputType per la **\_ \_ risoluzione \_ \_ MF Connect** .</span><span class="sxs-lookup"><span data-stu-id="8c8d1-129">In that case, the exact order of operations depends on the whether the [**MF\_TOPONODE\_CONNECT\_METHOD**](mf-toponode-connect-method-attribute.md) attribute on the source node includes the **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag.</span></span>

<span data-ttu-id="8c8d1-130">Se la \_ topologia MF \_ enumera \_ \_ i tipi di origine è **true** e si imposta il flag **MF \_ Connect \_ Resolve \_ Independent \_ OutputType** , il caricatore della topologia esaurisce ogni tipo di supporto prima di procedere al passaggio successivo, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="8c8d1-130">If MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES is **TRUE** and the **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag is set, the topology loader exhausts each media type before moving to the next, as follows:</span></span>

``` syntax
foreach media type T
    connect directly using T
    if failed, connect with converters using T
    if failed, connect with decoders using T
```

<span data-ttu-id="8c8d1-131">Se \_ la topologia MF \_ enumera i \_ \_ tipi di origine è **true** , ma non è impostata la **\_ soluzione MF Connect \_ Resolve \_ Independent \_ OutputType** , il caricatore della topologia tenta una connessione diretta a ogni tipo di supporto, quindi tenta ogni tipo di supporto con i convertitori e infine Cerca ogni tipo di supporto con i decodificatori:</span><span class="sxs-lookup"><span data-stu-id="8c8d1-131">If MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES is **TRUE** but **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** is not set, the topology loader tries a direct connection with each media type, then tries each media type with converters, and finally tries each media type with decoders:</span></span>

``` syntax
foreach media type T
    connect directly using T
if failed,
    foreach media type T
        connect with converters using T
if failed
    foreach media type T
        connect with decoders using T
```

<span data-ttu-id="8c8d1-132">Se \_ la topologia MF per l' \_ enumerazione \_ \_ dei tipi di origine è **false**, il flag OutputType per la **\_ \_ risoluzione \_ \_ MF Connect** viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="8c8d1-132">If MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES is **FALSE**, the **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag is ignored.</span></span>

<span data-ttu-id="8c8d1-133">Il valore predefinito della \_ topologia MF \_ enumerazione dei tipi di \_ origine \_ è **false** per compatibilità con le applicazioni esistenti.</span><span class="sxs-lookup"><span data-stu-id="8c8d1-133">The default value of MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES is **FALSE**, for compatibility with existing applications.</span></span>

<span data-ttu-id="8c8d1-134">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="8c8d1-134">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

### <a name="example"></a><span data-ttu-id="8c8d1-135">Esempio</span><span class="sxs-lookup"><span data-stu-id="8c8d1-135">Example</span></span>

<span data-ttu-id="8c8d1-136">Di seguito è riportato un esempio in cui viene illustrato il flag **MF \_ Connect \_ Resolve \_ Independent \_ OutputType** .</span><span class="sxs-lookup"><span data-stu-id="8c8d1-136">Here is an example that illustrates the **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag.</span></span> <span data-ttu-id="8c8d1-137">Si supponga che la topologia includa l' \_ attributo della topologia MF \_ enumerazione dei \_ \_ tipi di origine impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="8c8d1-137">Assume the topology has the MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute set to **TRUE**.</span></span>

<span data-ttu-id="8c8d1-138">L'origine multimediale offre i tipi seguenti:</span><span class="sxs-lookup"><span data-stu-id="8c8d1-138">The media source offers the following types:</span></span>

-   <span data-ttu-id="8c8d1-139">T1, T2, T3</span><span class="sxs-lookup"><span data-stu-id="8c8d1-139">T1, T2, T3</span></span>

<span data-ttu-id="8c8d1-140">Il sink multimediale accetta i tipi seguenti:</span><span class="sxs-lookup"><span data-stu-id="8c8d1-140">The media sink accepts the following types:</span></span>

-   <span data-ttu-id="8c8d1-141">T3, T4</span><span class="sxs-lookup"><span data-stu-id="8c8d1-141">T3, T4</span></span>

<span data-ttu-id="8c8d1-142">Caso 1: è impostato il flag per la **\_ risoluzione dei \_ \_ \_ OutputType indipendenti MF Connect** .</span><span class="sxs-lookup"><span data-stu-id="8c8d1-142">Case 1: The **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag is set.</span></span>

1.  <span data-ttu-id="8c8d1-143">Il caricatore della topologia tenta una connessione diretta con T1.</span><span class="sxs-lookup"><span data-stu-id="8c8d1-143">The topology loader tries a direct connection with T1.</span></span> <span data-ttu-id="8c8d1-144">Il sink rifiuta T1.</span><span class="sxs-lookup"><span data-stu-id="8c8d1-144">The sink rejects T1.</span></span>
2.  <span data-ttu-id="8c8d1-145">Il caricatore della topologia inserisce un decodificatore che accetta T1 e output T4.</span><span class="sxs-lookup"><span data-stu-id="8c8d1-145">The topology loader inserts a decoder that accepts T1 and outputs T4.</span></span> <span data-ttu-id="8c8d1-146">Il sink accetta T4.</span><span class="sxs-lookup"><span data-stu-id="8c8d1-146">The sink accepts T4.</span></span>
3.  <span data-ttu-id="8c8d1-147">La topologia finale contiene: origine multimediale → decodificatore → sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="8c8d1-147">The final topology contains: media source → decoder → media sink.</span></span>

<span data-ttu-id="8c8d1-148">Caso 2: il flag non è impostato.</span><span class="sxs-lookup"><span data-stu-id="8c8d1-148">Case 2: The flag is not set.</span></span>

1.  <span data-ttu-id="8c8d1-149">Il caricatore della topologia tenta una connessione diretta con T1.</span><span class="sxs-lookup"><span data-stu-id="8c8d1-149">The topology loader tries a direct connection with T1.</span></span> <span data-ttu-id="8c8d1-150">Il sink rifiuta T1.</span><span class="sxs-lookup"><span data-stu-id="8c8d1-150">The sink rejects T1.</span></span>
2.  <span data-ttu-id="8c8d1-151">Il caricatore della topologia tenta una connessione diretta con T2.</span><span class="sxs-lookup"><span data-stu-id="8c8d1-151">The topology loader tries a direct connection with T2.</span></span> <span data-ttu-id="8c8d1-152">Il sink rifiuta T2.</span><span class="sxs-lookup"><span data-stu-id="8c8d1-152">The sink rejects T2.</span></span>
3.  <span data-ttu-id="8c8d1-153">Il caricatore della topologia tenta una connessione diretta con T3.</span><span class="sxs-lookup"><span data-stu-id="8c8d1-153">The topology loader tries a direct connection with T3.</span></span> <span data-ttu-id="8c8d1-154">Il sink accetta T3.</span><span class="sxs-lookup"><span data-stu-id="8c8d1-154">The sink accepts T3.</span></span>
4.  <span data-ttu-id="8c8d1-155">La topologia finale contiene: origine multimediale → sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="8c8d1-155">The final topology contains: media source → media sink.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c8d1-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c8d1-156">Requirements</span></span>



| <span data-ttu-id="8c8d1-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c8d1-157">Requirement</span></span> | <span data-ttu-id="8c8d1-158">Valore</span><span class="sxs-lookup"><span data-stu-id="8c8d1-158">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8c8d1-159">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c8d1-159">Minimum supported client</span></span><br/> | <span data-ttu-id="8c8d1-160">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8c8d1-160">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8c8d1-161">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c8d1-161">Minimum supported server</span></span><br/> | <span data-ttu-id="8c8d1-162">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="8c8d1-162">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="8c8d1-163">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8c8d1-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c8d1-164"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c8d1-164"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c8d1-165">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8c8d1-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c8d1-166">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8c8d1-166">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8c8d1-167">Attributi della topologia</span><span class="sxs-lookup"><span data-stu-id="8c8d1-167">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 





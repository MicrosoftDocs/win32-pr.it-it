---
description: Nella tabella seguente sono elencati tutti i valori HRESULT che possono essere restituiti dai metodi dell'API documento XPS.
ms.assetid: 9e6db1e3-7151-4538-8607-b7185ebc0110
title: Errori relativi ai documenti XPS (Xpsobjectmodel. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a221858e177172a0062185cbe1bcc127ccc728fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226899"
---
# <a name="xps-document-errors"></a><span data-ttu-id="26b0f-103">Errori del documento XPS</span><span class="sxs-lookup"><span data-stu-id="26b0f-103">XPS Document Errors</span></span>

<span data-ttu-id="26b0f-104">Nella tabella seguente sono elencati tutti i valori **HRESULT** che possono essere restituiti dai metodi dell'API documento XPS.</span><span class="sxs-lookup"><span data-stu-id="26b0f-104">The following table lists all the **HRESULT** values that can be returned by the methods of the XPS Document API.</span></span> <span data-ttu-id="26b0f-105">Si noti che non tutti i metodi restituiscono tutti i valori restituiti elencati in questa tabella.</span><span class="sxs-lookup"><span data-stu-id="26b0f-105">Note that not every method returns every return value that is listed in this table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="26b0f-106">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="26b0f-106">Return code/value</span></span></th>
<th><span data-ttu-id="26b0f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26b0f-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="XPS_E_ALREADY_OWNED"></span><span id="xps_e_already_owned"></span><dl> <span data-ttu-id="26b0f-108"><dt><strong>XPS_E_ALREADY_OWNED</strong></dt> <dt>0x80520503</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-108"><dt><strong>XPS_E_ALREADY_OWNED</strong></dt> <dt>0x80520503</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-109">L'interfaccia dispone già di un proprietario.</span><span class="sxs-lookup"><span data-stu-id="26b0f-109">The interface already has an owner.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_BLEED_BOX_PAGE_DIMENSIONS_NOT_IN_SYNC"></span><span id="xps_e_bleed_box_page_dimensions_not_in_sync"></span><dl> <span data-ttu-id="26b0f-110"><dt><strong>XPS_E_BLEED_BOX_PAGE_DIMENSIONS_NOT_IN_SYNC</strong></dt> <dt>0x80520509</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-110"><dt><strong>XPS_E_BLEED_BOX_PAGE_DIMENSIONS_NOT_IN_SYNC</strong></dt> <dt>0x80520509</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-111">Le dimensioni della casella di spurgo non sono compatibili con le dimensioni della pagina.</span><span class="sxs-lookup"><span data-stu-id="26b0f-111">The bleed box dimensions are not compatible with the page dimensions.</span></span><br/> <span data-ttu-id="26b0f-112">Il valore della larghezza della casella di spurgo deve essere maggiore o uguale alla larghezza della pagina, più il valore assoluto della coordinata x dell'origine della casella di spurgo.</span><span class="sxs-lookup"><span data-stu-id="26b0f-112">The bleed box width value must be greater than or equal to the page width plus the absolute value of the x-coordinate of the bleed box origin.</span></span> <span data-ttu-id="26b0f-113">Il valore di altezza della casella di spurgo deve essere maggiore o uguale all'altezza della pagina più il valore assoluto della coordinata y dell'origine della casella di spurgo.</span><span class="sxs-lookup"><span data-stu-id="26b0f-113">The bleed box height value must be greater than or equal to the page height plus the absolute value of the y-coordinate of the bleed box origin.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_BOTH_PATHFIGURE_AND_ABBR_SYNTAX_PRESENT"></span><span id="xps_e_both_pathfigure_and_abbr_syntax_present"></span><dl> <span data-ttu-id="26b0f-114"><dt><strong>XPS_E_BOTH_PATHFIGURE_AND_ABBR_SYNTAX_PRESENT</strong></dt> <dt>0x80520507</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-114"><dt><strong>XPS_E_BOTH_PATHFIGURE_AND_ABBR_SYNTAX_PRESENT</strong></dt> <dt>0x80520507</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-115">Un elemento <strong>PathGeometry</strong> contiene un set di figure di percorso specificate con l'attributo <strong>Figures</strong> o con un elemento <strong>PathFigure</strong> figlio.</span><span class="sxs-lookup"><span data-stu-id="26b0f-115">A <strong>PathGeometry</strong> element contains a set of path figures that are specified either with the <strong>Figures</strong> attribute or with a child <strong>PathFigure</strong> element.</span></span> <span data-ttu-id="26b0f-116">Le figure di percorso di una geometria non possono avere sia l'attributo <strong>figure</strong> che un elemento <strong>PathFigure</strong> figlio.</span><span class="sxs-lookup"><span data-stu-id="26b0f-116">The path figures of a geometry cannot have both the <strong>Figures</strong> attribute and a child <strong>PathFigure</strong> element.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_BOTH_RESOURCE_AND_SOURCEATTR_PRESENT"></span><span id="xps_e_both_resource_and_sourceattr_present"></span><dl> <span data-ttu-id="26b0f-117"><dt><strong>XPS_E_BOTH_RESOURCE_AND_SOURCEATTR_PRESENT</strong></dt> <dt>0x80520508</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-117"><dt><strong>XPS_E_BOTH_RESOURCE_AND_SOURCEATTR_PRESENT</strong></dt> <dt>0x80520508</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-118">Un elemento <strong>ResourceDictionary</strong> che specifica un dizionario risorse remoto nell'attributo di <strong>origine</strong> non deve contenere elementi figlio di definizione di risorsa.</span><span class="sxs-lookup"><span data-stu-id="26b0f-118">A <strong>ResourceDictionary</strong> element that specifies a remote resource dictionary in its <strong>Source</strong> attribute MUST NOT contain any resource definition children.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_CARET_OUT_OF_ORDER"></span><span id="xps_e_caret_out_of_order"></span><dl> <span data-ttu-id="26b0f-119"><dt><strong>XPS_E_CARET_OUT_OF_ORDER</strong></dt> <dt>0x80520306</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-119"><dt><strong>XPS_E_CARET_OUT_OF_ORDER</strong></dt> <dt>0x80520306</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-120">Il valore della posizione del cursore non è in ordine.</span><span class="sxs-lookup"><span data-stu-id="26b0f-120">A caret location value is out of order.</span></span> <span data-ttu-id="26b0f-121">I valori del percorso devono essere ordinati in ordine crescente.</span><span class="sxs-lookup"><span data-stu-id="26b0f-121">The location values must be sorted in ascending order.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_CARET_OUTSIDE_STRING"></span><span id="xps_e_caret_outside_string"></span><dl> <span data-ttu-id="26b0f-122"><dt><strong>XPS_E_CARET_OUTSIDE_STRING</strong></dt> <dt>0x80520305</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-122"><dt><strong>XPS_E_CARET_OUTSIDE_STRING</strong></dt> <dt>0x80520305</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-123">Le interruzioni del punto di inserimento sono state specificate per una stringa vuota. in alternativa, l'indice di salto del cursore ha superato la lunghezza della stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="26b0f-123">Caret stops were specified for an empty string; or, the caret jump index has exceeded the length of the Unicode string.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_COLOR_COMPONENT_OUT_OF_RANGE"></span><span id="xps_e_color_component_out_of_range"></span><dl> <span data-ttu-id="26b0f-124"><dt><strong>XPS_E_COLOR_COMPONENT_OUT_OF_RANGE</strong></dt> <dt>0x80520506</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-124"><dt><strong>XPS_E_COLOR_COMPONENT_OUT_OF_RANGE</strong></dt> <dt>0x80520506</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-125">Un valore di colore non è compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="26b0f-125">A color value is out of range.</span></span><br/> <span data-ttu-id="26b0f-126">Per <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_SCRGB</strong></a> tipi di colore, il valore del canale alfa deve essere maggiore o uguale a 0,0 e minore o uguale a + 1,0.</span><span class="sxs-lookup"><span data-stu-id="26b0f-126">For <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_SCRGB</strong></a> color types, the alpha channel value must be greater than or equal to 0.0 and less than or equal to +1.0.</span></span><br/> <span data-ttu-id="26b0f-127">Per <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_CONTEXT</strong></a> tipi di colore, <strong>channelValues [0]</strong> che rappresenta il valore del canale alfa deve essere maggiore o uguale a 0,0 e minore o uguale a + 1,0.</span><span class="sxs-lookup"><span data-stu-id="26b0f-127">For <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_CONTEXT</strong></a> color types, the <strong>channelValues[0]</strong> that represents the alpha channel value must be greater than or equal to 0.0 and less than or equal to +1.0.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_DICTIONARY_ITEM_NAMED"></span><span id="xps_e_dictionary_item_named"></span><dl> <span data-ttu-id="26b0f-128"><dt><strong>XPS_E_DICTIONARY_ITEM_NAMED</strong></dt> <dt>0x80520401</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-128"><dt><strong>XPS_E_DICTIONARY_ITEM_NAMED</strong></dt> <dt>0x80520401</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-129">Un oggetto visivo in un dizionario risorse ha l'attributo <strong>Name</strong> , che non può essere specificato negli elementi figlio di un elemento <strong>ResourceDictionary</strong> .</span><span class="sxs-lookup"><span data-stu-id="26b0f-129">A visual in a resource dictionary has the <strong>Name</strong> attribute, which may not be specified on any children of a <strong>ResourceDictionary</strong> element.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_DUPLICATE_NAMES"></span><span id="xps_e_duplicate_names"></span><dl> <span data-ttu-id="26b0f-130"><dt><strong>XPS_E_DUPLICATE_NAMES</strong></dt> <dt>0x80520209</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-130"><dt><strong>XPS_E_DUPLICATE_NAMES</strong></dt> <dt>0x80520209</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-131">Un oggetto con questo nome esiste già nel dizionario.</span><span class="sxs-lookup"><span data-stu-id="26b0f-131">An object with this name already exists in the dictionary.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_DUPLICATE_RESOURCE_KEYS"></span><span id="xps_e_duplicate_resource_keys"></span><dl> <span data-ttu-id="26b0f-132"><dt><strong>XPS_E_DUPLICATE_RESOURCE_KEYS</strong></dt> <dt>0x80520200</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-132"><dt><strong>XPS_E_DUPLICATE_RESOURCE_KEYS</strong></dt> <dt>0x80520200</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-133">Un oggetto con questo nome di chiave esiste già nel dizionario.</span><span class="sxs-lookup"><span data-stu-id="26b0f-133">An object with this key name already exists in the dictionary.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INDEX_OUT_OF_RANGE"></span><span id="xps_e_index_out_of_range"></span><dl> <span data-ttu-id="26b0f-134"><dt><strong>XPS_E_INDEX_OUT_OF_RANGE</strong></dt> <dt>0x80520500</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-134"><dt><strong>XPS_E_INDEX_OUT_OF_RANGE</strong></dt> <dt>0x80520500</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-135">Riservato.</span><span class="sxs-lookup"><span data-stu-id="26b0f-135">Reserved.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_BLEED_BOX"></span><span id="xps_e_invalid_bleed_box"></span><dl> <span data-ttu-id="26b0f-136"><dt><strong>XPS_E_INVALID_BLEED_BOX</strong></dt> <dt>0x80520004</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-136"><dt><strong>XPS_E_INVALID_BLEED_BOX</strong></dt> <dt>0x80520004</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-137">Il rettangolo della casella di sfiato contiene uno o più valori non validi.</span><span class="sxs-lookup"><span data-stu-id="26b0f-137">The bleed box rectangle contains one or more values that are not valid.</span></span> <span data-ttu-id="26b0f-138">Vedere la descrizione del parametro per i valori validi.</span><span class="sxs-lookup"><span data-stu-id="26b0f-138">See the parameter description for the valid values.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_CONTENT_BOX"></span><span id="xps_e_invalid_content_box"></span><dl> <span data-ttu-id="26b0f-139"><dt><strong>XPS_E_INVALID_CONTENT_BOX</strong></dt> <dt>0x8052000b</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-139"><dt><strong>XPS_E_INVALID_CONTENT_BOX</strong></dt> <dt>0x8052000b</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-140">Il rettangolo della casella di contenuto contiene uno o più valori non validi.</span><span class="sxs-lookup"><span data-stu-id="26b0f-140">The content box rectangle contains one or more values that are not valid.</span></span> <span data-ttu-id="26b0f-141">Vedere la descrizione del parametro per i valori validi.</span><span class="sxs-lookup"><span data-stu-id="26b0f-141">See the parameter description for the valid values.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_CONTENT_TYPE"></span><span id="xps_e_invalid_content_type"></span><dl> <span data-ttu-id="26b0f-142"><dt><strong>XPS_E_INVALID_CONTENT_TYPE</strong></dt> <dt>0x8052000e</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-142"><dt><strong>XPS_E_INVALID_CONTENT_TYPE</strong></dt> <dt>0x8052000e</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-143">La stringa del tipo di contenuto non è valida.</span><span class="sxs-lookup"><span data-stu-id="26b0f-143">The content type string is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_FLOAT"></span><span id="xps_e_invalid_float"></span><dl> <span data-ttu-id="26b0f-144"><dt><strong>XPS_E_INVALID_FLOAT</strong></dt> <dt>0x80520007</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-144"><dt><strong>XPS_E_INVALID_FLOAT</strong></dt> <dt>0x80520007</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-145">Valore <strong>float</strong> non valido.</span><span class="sxs-lookup"><span data-stu-id="26b0f-145">A <strong>FLOAT</strong> value is not valid.</span></span> <span data-ttu-id="26b0f-146">È un valore NAN (infinito).</span><span class="sxs-lookup"><span data-stu-id="26b0f-146">It is either an infinite or not a number (NAN).</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_FONT_URI"></span><span id="xps_e_invalid_font_uri"></span><dl> <span data-ttu-id="26b0f-147"><dt><strong>XPS_E_INVALID_FONT_URI</strong></dt> <dt>0x8052000a</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-147"><dt><strong>XPS_E_INVALID_FONT_URI</strong></dt> <dt>0x8052000a</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-148">L'URI del tipo di carattere non è valido, probabilmente perché contiene frammenti vuoti o caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="26b0f-148">The font URI is not valid, possibly because it contains an empty fragment or characters that are not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_LANGUAGE"></span><span id="xps_e_invalid_language"></span><dl> <span data-ttu-id="26b0f-149"><dt><strong>XPS_E_INVALID_LANGUAGE</strong></dt> <dt>0x80520000</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-149"><dt><strong>XPS_E_INVALID_LANGUAGE</strong></dt> <dt>0x80520000</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-150">La lingua specificata non è valida o non è formattata correttamente.</span><span class="sxs-lookup"><span data-stu-id="26b0f-150">The specified language is either not valid or not correctly formatted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_LOOKUP_TYPE"></span><span id="xps_e_invalid_lookup_type"></span><dl> <span data-ttu-id="26b0f-151"><dt><strong>XPS_E_INVALID_LOOKUP_TYPE</strong></dt> <dt>0x80520006</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-151"><dt><strong>XPS_E_INVALID_LOOKUP_TYPE</strong></dt> <dt>0x80520006</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-152">Il nome della chiave di ricerca fa riferimento a un oggetto che non è il tipo corretto per la chiamata; Se, ad esempio, il metodo restituisce un pennello ma il nome della chiave di ricerca fa riferimento a un oggetto Geometry.</span><span class="sxs-lookup"><span data-stu-id="26b0f-152">The lookup key name references an object that is not the correct type for the call; for example, if the method returns a brush but the lookup key name refers to a geometry object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_MARKUP"></span><span id="xps_e_invalid_markup"></span><dl> <span data-ttu-id="26b0f-153"><dt><strong>XPS_E_INVALID_MARKUP</strong></dt> <dt>0x8052000c</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-153"><dt><strong>XPS_E_INVALID_MARKUP</strong></dt> <dt>0x8052000c</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-154">Il markup letto contiene un elemento o un attributo che non è conforme alla <a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">specifica del documento XML</a>.</span><span class="sxs-lookup"><span data-stu-id="26b0f-154">The markup being read contains an element or an attribute that does not conform to the <a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="26b0f-155">Per rappresentare i valori a virgola mobile, XPS OM usa il tipo di dati <strong>float</strong> anziché <strong>Double</strong>.</span><span class="sxs-lookup"><span data-stu-id="26b0f-155">To represent floating-point values, the XPS OM uses the <strong>FLOAT</strong> data type instead of <strong>DOUBLE</strong>.</span></span> <span data-ttu-id="26b0f-156">Se un documento XPS dispone di un elemento con dati a virgola mobile che non rientra in un valore <strong>float</strong> , questo errore viene restituito quando tale valore viene rilevato durante la deserializzazione.</span><span class="sxs-lookup"><span data-stu-id="26b0f-156">If an XPS document has an element with floating-point data that does not fit into a <strong>FLOAT</strong> value, this error will be returned when that value is encountered during deserialization.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_NAME"></span><span id="xps_e_invalid_name"></span><dl> <span data-ttu-id="26b0f-157"><dt><strong>XPS_E_INVALID_NAME</strong></dt> <dt>0x80520001</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-157"><dt><strong>XPS_E_INVALID_NAME</strong></dt> <dt>0x80520001</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-158">La stringa passata non è un nome valido, in base alla specifica del documento XML.</span><span class="sxs-lookup"><span data-stu-id="26b0f-158">The string that was passed is not a valid name, according to the XML Paper Specification.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_OBFUSCATED_FONT_URI"></span><span id="xps_e_invalid_obfuscated_font_uri"></span><dl> <span data-ttu-id="26b0f-159"><dt><strong>XPS_E_INVALID_OBFUSCATED_FONT_URI</strong></dt> <dt>0x8052000f</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-159"><dt><strong>XPS_E_INVALID_OBFUSCATED_FONT_URI</strong></dt> <dt>0x8052000f</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-160">Riservato.</span><span class="sxs-lookup"><span data-stu-id="26b0f-160">Reserved.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_PAGE_SIZE"></span><span id="xps_e_invalid_page_size"></span><dl> <span data-ttu-id="26b0f-161"><dt><strong>XPS_E_INVALID_PAGE_SIZE</strong></dt> <dt>0x80520003</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-161"><dt><strong>XPS_E_INVALID_PAGE_SIZE</strong></dt> <dt>0x80520003</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-162">Le dimensioni della pagina contengono un valore di dimensione della pagina non valido.</span><span class="sxs-lookup"><span data-stu-id="26b0f-162">The page dimensions contain a page size value that is not valid.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_RESOURCE_KEY"></span><span id="xps_e_invalid_resource_key"></span><dl> <span data-ttu-id="26b0f-163"><dt><strong>XPS_E_INVALID_RESOURCE_KEY</strong></dt> <dt>0x80520002</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-163"><dt><strong>XPS_E_INVALID_RESOURCE_KEY</strong></dt> <dt>0x80520002</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-164">In base alla <a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">specifica del documento XML</a>, la stringa della chiave di ricerca non è valida.</span><span class="sxs-lookup"><span data-stu-id="26b0f-164">According to the <a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>, the lookup key string is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_THUMBNAIL_IMAGE_TYPE"></span><span id="xps_e_invalid_thumbnail_image_type"></span><dl> <span data-ttu-id="26b0f-165"><dt><strong>XPS_E_INVALID_THUMBNAIL_IMAGE_TYPE</strong></dt> <dt>0x80520005</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-165"><dt><strong>XPS_E_INVALID_THUMBNAIL_IMAGE_TYPE</strong></dt> <dt>0x80520005</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-166">Il tipo di immagine di anteprima non è supportato.</span><span class="sxs-lookup"><span data-stu-id="26b0f-166">The thumbnail image type is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_XML_ENCODING"></span><span id="xps_e_invalid_xml_encoding"></span><dl> <span data-ttu-id="26b0f-167"><dt><strong>XPS_E_INVALID_XML_ENCODING</strong></dt> <dt>0x8052000d</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-167"><dt><strong>XPS_E_INVALID_XML_ENCODING</strong></dt> <dt>0x8052000d</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-168">È stato trovato un markup XML non corretto o formattato in modo errato.</span><span class="sxs-lookup"><span data-stu-id="26b0f-168">Found improper or incorrectly formatted XML markup.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MAPPING_OUT_OF_ORDER"></span><span id="xps_e_mapping_out_of_order"></span><dl> <span data-ttu-id="26b0f-169"><dt><strong>XPS_E_MAPPING_OUT_OF_ORDER</strong></dt> <dt>0x80520302</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-169"><dt><strong>XPS_E_MAPPING_OUT_OF_ORDER</strong></dt> <dt>0x80520302</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-170">In una o più strutture <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_mapping"><strong>XPS_GLYPH_MAPPING</strong></a> un elemento è fuori sequenza.</span><span class="sxs-lookup"><span data-stu-id="26b0f-170">In one or more <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_mapping"><strong>XPS_GLYPH_MAPPING</strong></a> structures, an element is out of sequence.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MAPPING_OUTSIDE_INDICES"></span><span id="xps_e_mapping_outside_indices"></span><dl> <span data-ttu-id="26b0f-171"><dt><strong>XPS_E_MAPPING_OUTSIDE_INDICES</strong></dt> <dt>0x80520304</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-171"><dt><strong>XPS_E_MAPPING_OUTSIDE_INDICES</strong></dt> <dt>0x80520304</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-172">I mapping dei glifi superano il numero di indici di glifi.</span><span class="sxs-lookup"><span data-stu-id="26b0f-172">The glyph mappings exceed the number of glyph indices.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MAPPING_OUTSIDE_STRING"></span><span id="xps_e_mapping_outside_string"></span><dl> <span data-ttu-id="26b0f-173"><dt><strong>XPS_E_MAPPING_OUTSIDE_STRING</strong></dt> <dt>0x80520303</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-173"><dt><strong>XPS_E_MAPPING_OUTSIDE_STRING</strong></dt> <dt>0x80520303</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-174">Errore nei mapping dei glifi.</span><span class="sxs-lookup"><span data-stu-id="26b0f-174">Error in the glyph mappings.</span></span><br/> <span data-ttu-id="26b0f-175">Se la stringa Unicode è vuota, questo errore indica che è stato definito anche il mapping di un glifo.</span><span class="sxs-lookup"><span data-stu-id="26b0f-175">If the Unicode string is empty, this error means that a glyph mapping was also defined.</span></span> <span data-ttu-id="26b0f-176">I mapping dei glifi non devono essere definiti se la stringa Unicode è vuota.</span><span class="sxs-lookup"><span data-stu-id="26b0f-176">Glyph mappings must not be defined if the Unicode string is empty.</span></span><br/> <span data-ttu-id="26b0f-177">Se la stringa Unicode non è vuota, questo errore indica che è stato definito un mapping del glifo per i glifi al di fuori della stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="26b0f-177">If the Unicode string is not empty, this error means that a glyph mapping was defined for glyphs outside of the Unicode string.</span></span> <span data-ttu-id="26b0f-178">Non è possibile definire i mapping dei glifi per i glifi che non rientrano nella lunghezza della stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="26b0f-178">Glyph mappings cannot be defined for glyphs that fall outside the length of the Unicode string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_COLORPROFILE"></span><span id="xps_e_missing_colorprofile"></span><dl> <span data-ttu-id="26b0f-179"><dt><strong>XPS_E_MISSING_COLORPROFILE</strong></dt> <dt>0x80520104</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-179"><dt><strong>XPS_E_MISSING_COLORPROFILE</strong></dt> <dt>0x80520104</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-180">Il parametro del profilo colori è <strong>null</strong>, ma è previsto un profilo colori.</span><span class="sxs-lookup"><span data-stu-id="26b0f-180">The color profile parameter is <strong>NULL</strong>, but a color profile is expected.</span></span> <span data-ttu-id="26b0f-181">Quando il tipo di colore è XPS_COLOR_TYPE_CONTEXT, è necessario un profilo colori.</span><span class="sxs-lookup"><span data-stu-id="26b0f-181">A color profile is required when the color type is XPS_COLOR_TYPE_CONTEXT.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_DISCARDCONTROL"></span><span id="xps_e_missing_discardcontrol"></span><dl> <span data-ttu-id="26b0f-182"><dt><strong>XPS_E_MISSING_DISCARDCONTROL</strong></dt> <dt>0x80520112</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-182"><dt><strong>XPS_E_MISSING_DISCARDCONTROL</strong></dt> <dt>0x80520112</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-183">Una pagina si riferisce a risorse eliminabili, ma non specifica un nome di parte DiscardControl.</span><span class="sxs-lookup"><span data-stu-id="26b0f-183">A page refers to discardable resources but does not specify a DiscardControl part name.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_DOCUMENT"></span><span id="xps_e_missing_document"></span><dl> <span data-ttu-id="26b0f-184"><dt><strong>XPS_E_MISSING_DOCUMENT</strong></dt> <dt>0x80520109</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-184"><dt><strong>XPS_E_MISSING_DOCUMENT</strong></dt> <dt>0x80520109</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-185"><a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage"><strong>IXpsOMPackageWriter:: AddPage</strong></a> è stato chiamato prima di <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument"><strong>IXpsOMPackageWriter:: StartNewDocument</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="26b0f-185"><a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage"><strong>IXpsOMPackageWriter::AddPage</strong></a> was called before <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument"><strong>IXpsOMPackageWriter::StartNewDocument</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_DOCUMENTSEQUENCE_RELATIONSHIP"></span><span id="xps_e_missing_documentsequence_relationship"></span><dl> <span data-ttu-id="26b0f-186"><dt><strong>XPS_E_MISSING_DOCUMENTSEQUENCE_RELATIONSHIP</strong></dt> <dt>0x80520108</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-186"><dt><strong>XPS_E_MISSING_DOCUMENTSEQUENCE_RELATIONSHIP</strong></dt> <dt>0x80520108</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-187">Il pacchetto non contiene un FixedDocumentSequence.</span><span class="sxs-lookup"><span data-stu-id="26b0f-187">The package does not contain a FixedDocumentSequence.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_FONTURI"></span><span id="xps_e_missing_fonturi"></span><dl> <span data-ttu-id="26b0f-188"><dt><strong>XPS_E_MISSING_FONTURI</strong></dt> <dt>0x80520107</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-188"><dt><strong>XPS_E_MISSING_FONTURI</strong></dt> <dt>0x80520107</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-189">L'interfaccia <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs"><strong>IXpsOMGlyphs</strong></a> richiede un URI del tipo di carattere, ma non ne è stato specificato uno.</span><span class="sxs-lookup"><span data-stu-id="26b0f-189">The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs"><strong>IXpsOMGlyphs</strong></a> interface requires a font URI, but one is not specified.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_GLYPHS"></span><span id="xps_e_missing_glyphs"></span><dl> <span data-ttu-id="26b0f-190"><dt><strong>XPS_E_MISSING_GLYPHS</strong></dt> <dt>0x80520102</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-190"><dt><strong>XPS_E_MISSING_GLYPHS</strong></dt> <dt>0x80520102</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-191">L'interfaccia <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs"><strong>IXpsOMGlyphs</strong></a> senza una stringa Unicode non specifica alcun indici di glifi.</span><span class="sxs-lookup"><span data-stu-id="26b0f-191">The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs"><strong>IXpsOMGlyphs</strong></a> interface without a Unicode string does not specify any glyph indices.</span></span> <span data-ttu-id="26b0f-192">Un'interfaccia <strong>IXpsOMGlyphs</strong> deve specificare una stringa Unicode o una matrice di indici di glifi.</span><span class="sxs-lookup"><span data-stu-id="26b0f-192">An <strong>IXpsOMGlyphs</strong> interface must specify either a Unicode string or an array of glyph indices.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_IMAGE_IN_IMAGEBRUSH"></span><span id="xps_e_missing_image_in_imagebrush"></span><dl> <span data-ttu-id="26b0f-193"><dt><strong>XPS_E_MISSING_IMAGE_IN_IMAGEBRUSH</strong></dt> <dt>0x8052010e</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-193"><dt><strong>XPS_E_MISSING_IMAGE_IN_IMAGEBRUSH</strong></dt> <dt>0x8052010e</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-194">Non è stato possibile trovare una risorsa immagine per il pennello immagine.</span><span class="sxs-lookup"><span data-stu-id="26b0f-194">An image resource could not be located for the image brush.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_LOOKUP"></span><span id="xps_e_missing_lookup"></span><dl> <span data-ttu-id="26b0f-195"><dt><strong>XPS_E_MISSING_LOOKUP</strong></dt> <dt>0x80520101</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-195"><dt><strong>XPS_E_MISSING_LOOKUP</strong></dt> <dt>0x80520101</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-196">La risorsa remota ha un oggetto imprevisto.</span><span class="sxs-lookup"><span data-stu-id="26b0f-196">The remote resource has an unexpected object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_NAME"></span><span id="xps_e_missing_name"></span><dl> <span data-ttu-id="26b0f-197"><dt><strong>XPS_E_MISSING_NAME</strong></dt> <dt>0x80520100</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-197"><dt><strong>XPS_E_MISSING_NAME</strong></dt> <dt>0x80520100</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-198">La pagina non è stata denominata; lo stato della destinazione del collegamento ipertestuale può essere impostato solo se la pagina ha un nome.</span><span class="sxs-lookup"><span data-stu-id="26b0f-198">The page has not been named; the hyperlink target status can only be set if the page has a name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_PAGE_IN_DOCUMENT"></span><span id="xps_e_missing_page_in_document"></span><dl> <span data-ttu-id="26b0f-199"><dt><strong>XPS_E_MISSING_PAGE_IN_DOCUMENT</strong></dt> <dt>0x8052010c</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-199"><dt><strong>XPS_E_MISSING_PAGE_IN_DOCUMENT</strong></dt> <dt>0x8052010c</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-200">FixedDocument non contiene parti FixedPage.</span><span class="sxs-lookup"><span data-stu-id="26b0f-200">The FixedDocument does not contain any FixedPage parts.</span></span> <span data-ttu-id="26b0f-201">Un documento XPS deve contenere almeno una parte FixedPage.</span><span class="sxs-lookup"><span data-stu-id="26b0f-201">An XPS document must contain at least one FixedPage part.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_PAGE_IN_PAGEREFERENCE"></span><span id="xps_e_missing_page_in_pagereference"></span><dl> <span data-ttu-id="26b0f-202"><dt><strong>XPS_E_MISSING_PAGE_IN_PAGEREFERENCE</strong></dt> <dt>0x8052010d</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-202"><dt><strong>XPS_E_MISSING_PAGE_IN_PAGEREFERENCE</strong></dt> <dt>0x8052010d</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-203">Il riferimento alla pagina non dispone di una pagina corrispondente.</span><span class="sxs-lookup"><span data-stu-id="26b0f-203">The page reference does not have a corresponding page.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_PART_REFERENCE"></span><span id="xps_e_missing_part_reference"></span><dl> <span data-ttu-id="26b0f-204"><dt><strong>XPS_E_MISSING_PART_REFERENCE</strong></dt> <dt>0x80520110</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-204"><dt><strong>XPS_E_MISSING_PART_REFERENCE</strong></dt> <dt>0x80520110</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-205">Non è stato fatto riferimento A una parte di destinazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="26b0f-205">A required target part was not referenced.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_PART_STREAM"></span><span id="xps_e_missing_part_stream"></span><dl> <span data-ttu-id="26b0f-206"><dt><strong>XPS_E_MISSING_PART_STREAM</strong></dt> <dt>0x80520113</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-206"><dt><strong>XPS_E_MISSING_PART_STREAM</strong></dt> <dt>0x80520113</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-207">Non è stato specificato alcun flusso per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="26b0f-207">A stream was not specified for the resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_REFERRED_DOCUMENT"></span><span id="xps_e_missing_referred_document"></span><dl> <span data-ttu-id="26b0f-208"><dt><strong>XPS_E_MISSING_REFERRED_DOCUMENT</strong></dt> <dt>0x8052010a</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-208"><dt><strong>XPS_E_MISSING_REFERRED_DOCUMENT</strong></dt> <dt>0x8052010a</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-209">Impossibile trovare la parte FixedDocument a cui fa riferimento il FixedDocumentSequence.</span><span class="sxs-lookup"><span data-stu-id="26b0f-209">The FixedDocument part that is referenced by the FixedDocumentSequence could not be found.</span></span> <span data-ttu-id="26b0f-210">Un documento XPS deve contenere almeno un FixedDocument.</span><span class="sxs-lookup"><span data-stu-id="26b0f-210">An XPS document must contain at least one FixedDocument.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_REFERRED_PAGE"></span><span id="xps_e_missing_referred_page"></span><dl> <span data-ttu-id="26b0f-211"><dt><strong>XPS_E_MISSING_REFERRED_PAGE</strong></dt> <dt>0x8052010b</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-211"><dt><strong>XPS_E_MISSING_REFERRED_PAGE</strong></dt> <dt>0x8052010b</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-212">Impossibile trovare la parte FixedPage a cui fa riferimento FixedDocument.</span><span class="sxs-lookup"><span data-stu-id="26b0f-212">The FixedPage part that is referenced by the FixedDocument could not be found.</span></span> <span data-ttu-id="26b0f-213">Un documento XPS deve contenere almeno una parte FixedPage.</span><span class="sxs-lookup"><span data-stu-id="26b0f-213">An XPS document must contain at least one FixedPage part.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_RELATIONSHIP_TARGET"></span><span id="xps_e_missing_relationship_target"></span><dl> <span data-ttu-id="26b0f-214"><dt><strong>XPS_E_MISSING_RELATIONSHIP_TARGET</strong></dt> <dt>0x80520105</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-214"><dt><strong>XPS_E_MISSING_RELATIONSHIP_TARGET</strong></dt> <dt>0x80520105</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-215">La parte della destinazione della relazione non è presente nella relazione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="26b0f-215">The relationship target part is not present in the package relationship.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_RESOURCE_KEY"></span><span id="xps_e_missing_resource_key"></span><dl> <span data-ttu-id="26b0f-216"><dt><strong>XPS_E_MISSING_RESOURCE_KEY</strong></dt> <dt>0x8052010f</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-216"><dt><strong>XPS_E_MISSING_RESOURCE_KEY</strong></dt> <dt>0x8052010f</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-217">Nessun attributo <strong>x:Key</strong> specificato per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="26b0f-217">No <strong>x:Key</strong> attribute was specified for the resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_RESOURCE_RELATIONSHIP"></span><span id="xps_e_missing_resource_relationship"></span><dl> <span data-ttu-id="26b0f-218"><dt><strong>XPS_E_MISSING_RESOURCE_RELATIONSHIP</strong></dt> <dt>0x80520106</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-218"><dt><strong>XPS_E_MISSING_RESOURCE_RELATIONSHIP</strong></dt> <dt>0x80520106</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-219">La risorsa a cui fa riferimento la pagina o il contenuto del dizionario remoto non esiste come relazione di pagina.</span><span class="sxs-lookup"><span data-stu-id="26b0f-219">The resource referred to by the page or remote dictionary content does not exist as a page relationship.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_RESTRICTED_FONT_RELATIONSHIP"></span><span id="xps_e_missing_restricted_font_relationship"></span><dl> <span data-ttu-id="26b0f-220"><dt><strong>XPS_E_MISSING_RESTRICTED_FONT_RELATIONSHIP</strong></dt> <dt>0x80520111</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-220"><dt><strong>XPS_E_MISSING_RESTRICTED_FONT_RELATIONSHIP</strong></dt> <dt>0x80520111</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-221">Il tipo di carattere limitato a cui si fa riferimento non è stato specificato nella chiamata a <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument"><strong>IXpsOMPackageWriter:: StartNewDocument</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="26b0f-221">The referenced restricted font was not specified in the call to <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument"><strong>IXpsOMPackageWriter::StartNewDocument</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_SEGMENT_DATA"></span><span id="xps_e_missing_segment_data"></span><dl> <span data-ttu-id="26b0f-222"><dt><strong>XPS_E_MISSING_SEGMENT_DATA</strong></dt> <dt>0x80520103</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-222"><dt><strong>XPS_E_MISSING_SEGMENT_DATA</strong></dt> <dt>0x80520103</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-223">Il numero di voci della matrice di dati del segmento è inferiore a quello della matrice dei tipi di segmento.</span><span class="sxs-lookup"><span data-stu-id="26b0f-223">The segment data array has fewer entries than the segment types array.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MULTIPLE_DOCUMENTSEQUENCE_RELATIONSHIPS"></span><span id="xps_e_multiple_documentsequence_relationships"></span><dl> <span data-ttu-id="26b0f-224"><dt><strong>XPS_E_MULTIPLE_DOCUMENTSEQUENCE_RELATIONSHIPS</strong></dt> <dt>0x80520202</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-224"><dt><strong>XPS_E_MULTIPLE_DOCUMENTSEQUENCE_RELATIONSHIPS</strong></dt> <dt>0x80520202</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-225">È stato effettuato un tentativo di aggiungere un FixedDocumentSequence a un pacchetto che ne contiene già uno.</span><span class="sxs-lookup"><span data-stu-id="26b0f-225">An attempt was made to add a FixedDocumentSequence to a package that already has one.</span></span> <span data-ttu-id="26b0f-226">Un documento XPS deve contenere solo una parte FixedDocumentSequence.</span><span class="sxs-lookup"><span data-stu-id="26b0f-226">An XPS document must contain one and only one FixedDocumentSequence part.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENT"></span><span id="xps_e_multiple_printtickets_on_document"></span><dl> <span data-ttu-id="26b0f-227"><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENT</strong></dt> <dt>0x80520206</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-227"><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENT</strong></dt> <dt>0x80520206</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-228">È stato effettuato un tentativo di aggiungere un ticket di stampa a livello di documento a un FixedDocument che ne contiene già uno.</span><span class="sxs-lookup"><span data-stu-id="26b0f-228">An attempt was made to add a document-level print ticket to a FixedDocument that already has one.</span></span> <span data-ttu-id="26b0f-229">Un FixedDocument in un documento XPS può contenere un solo ticket di stampa a livello di documento.</span><span class="sxs-lookup"><span data-stu-id="26b0f-229">A FixedDocument in an XPS document can contain only one document-level print ticket.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENTSEQUENCE"></span><span id="xps_e_multiple_printtickets_on_documentsequence"></span><dl> <span data-ttu-id="26b0f-230"><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENTSEQUENCE</strong></dt> <dt>0x80520207</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-230"><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENTSEQUENCE</strong></dt> <dt>0x80520207</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-231">È stato effettuato un tentativo di aggiungere un ticket di stampa a livello di processo a un FixedDocumentSequence che ne contiene già uno.</span><span class="sxs-lookup"><span data-stu-id="26b0f-231">An attempt was made to add a job-level print ticket to a FixedDocumentSequence that already has one.</span></span> <span data-ttu-id="26b0f-232">FixedDocumentSequence in un documento XPS può contenere un solo ticket di stampa a livello di processo.</span><span class="sxs-lookup"><span data-stu-id="26b0f-232">The FixedDocumentSequence in an XPS document can contain only one job-level print ticket.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MULTIPLE_PRINTTICKETS_ON_PAGE"></span><span id="xps_e_multiple_printtickets_on_page"></span><dl> <span data-ttu-id="26b0f-233"><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_PAGE</strong></dt> <dt>0x80520205</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-233"><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_PAGE</strong></dt> <dt>0x80520205</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-234">È stato effettuato un tentativo di aggiungere un ticket di stampa a livello di pagina a un elemento FixedPage che ne contiene già uno.</span><span class="sxs-lookup"><span data-stu-id="26b0f-234">An attempt was made to add a page-level print ticket to a FixedPage that already has one.</span></span> <span data-ttu-id="26b0f-235">Un elemento FixedPage in un documento XPS può contenere un solo ticket di stampa a livello di pagina.</span><span class="sxs-lookup"><span data-stu-id="26b0f-235">A FixedPage in an XPS document can contain only one page-level print ticket.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MULTIPLE_REFERENCES_TO_PART"></span><span id="xps_e_multiple_references_to_part"></span><dl> <span data-ttu-id="26b0f-236"><dt><strong>XPS_E_MULTIPLE_REFERENCES_TO_PART</strong></dt> <dt>0x80520208</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-236"><dt><strong>XPS_E_MULTIPLE_REFERENCES_TO_PART</strong></dt> <dt>0x80520208</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-237">La raccolta di tipi di carattere con restrizioni contiene una voce di tipo carattere limitata ripetuta.</span><span class="sxs-lookup"><span data-stu-id="26b0f-237">The restricted font collection contained a restricted font entry that was repeated.</span></span> <span data-ttu-id="26b0f-238">Ogni voce del tipo di carattere può essere presente solo una volta nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="26b0f-238">Each font entry can occur in the collection only once.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MULTIPLE_RESOURCES"></span><span id="xps_e_multiple_resources"></span><dl> <span data-ttu-id="26b0f-239"><dt><strong>XPS_E_MULTIPLE_RESOURCES</strong></dt> <dt>0x80520201</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-239"><dt><strong>XPS_E_MULTIPLE_RESOURCES</strong></dt> <dt>0x80520201</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-240">Una risorsa con tale nome di parte esiste già.</span><span class="sxs-lookup"><span data-stu-id="26b0f-240">A resource by that part name already exists.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MULTIPLE_THUMBNAILS_ON_PACKAGE"></span><span id="xps_e_multiple_thumbnails_on_package"></span><dl> <span data-ttu-id="26b0f-241"><dt><strong>XPS_E_MULTIPLE_THUMBNAILS_ON_PACKAGE</strong></dt> <dt>0x80520204</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-241"><dt><strong>XPS_E_MULTIPLE_THUMBNAILS_ON_PACKAGE</strong></dt> <dt>0x80520204</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-242">È stato effettuato un tentativo di aggiungere un'immagine di anteprima a un pacchetto che ne contiene già uno.</span><span class="sxs-lookup"><span data-stu-id="26b0f-242">An attempt was made to add a thumbnail image to a package that already has one.</span></span> <span data-ttu-id="26b0f-243">Un documento XPS può contenere una sola immagine di anteprima a livello di pacchetto.</span><span class="sxs-lookup"><span data-stu-id="26b0f-243">An XPS document can contain only one package-level thumbnail image.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MULTIPLE_THUMBNAILS_ON_PAGE"></span><span id="xps_e_multiple_thumbnails_on_page"></span><dl> <span data-ttu-id="26b0f-244"><dt><strong>XPS_E_MULTIPLE_THUMBNAILS_ON_PAGE</strong></dt> <dt>0x80520203</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-244"><dt><strong>XPS_E_MULTIPLE_THUMBNAILS_ON_PAGE</strong></dt> <dt>0x80520203</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-245">È stato effettuato un tentativo di aggiungere un'immagine di anteprima a livello di pagina a un elemento FixedPage che ne contiene già uno.</span><span class="sxs-lookup"><span data-stu-id="26b0f-245">An attempt was made to add a page-level thumbnail image to a FixedPage that already has one.</span></span> <span data-ttu-id="26b0f-246">Un FixedPage in un documento XPS può contenere una sola immagine di anteprima a livello di pagina.</span><span class="sxs-lookup"><span data-stu-id="26b0f-246">A FixedPage in an XPS document can contain only one page-level thumbnail image.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_NEGATIVE_FLOAT"></span><span id="xps_e_negative_float"></span><dl> <span data-ttu-id="26b0f-247"><dt><strong>XPS_E_NEGATIVE_FLOAT</strong></dt> <dt>0x8052030a</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-247"><dt><strong>XPS_E_NEGATIVE_FLOAT</strong></dt> <dt>0x8052030a</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-248">Una voce contiene un valore negativo, ma deve contenere un valore non negativo.</span><span class="sxs-lookup"><span data-stu-id="26b0f-248">An entry contains a negative value, but it must contain a non-negative value.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_NESTED_REMOTE_DICTIONARY"></span><span id="xps_e_nested_remote_dictionary"></span><dl> <span data-ttu-id="26b0f-249"><dt><strong>XPS_E_NESTED_REMOTE_DICTIONARY</strong></dt> <dt>0x80520402</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-249"><dt><strong>XPS_E_NESTED_REMOTE_DICTIONARY</strong></dt> <dt>0x80520402</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-250">È stato effettuato un tentativo di aggiungere un riferimento a un dizionario remoto a un dizionario remoto.</span><span class="sxs-lookup"><span data-stu-id="26b0f-250">An attempt was made to add a remote dictionary reference to a remote dictionary.</span></span> <span data-ttu-id="26b0f-251">Un dizionario remoto non può fare riferimento A un altro dizionario remoto.</span><span class="sxs-lookup"><span data-stu-id="26b0f-251">A remote dictionary cannot reference another remote dictionary.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_NO_CUSTOM_OBJECTS"></span><span id="xps_e_no_custom_objects"></span><dl> <span data-ttu-id="26b0f-252"><dt><strong>XPS_E_NO_CUSTOM_OBJECTS</strong></dt> <dt>0x80520502</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-252"><dt><strong>XPS_E_NO_CUSTOM_OBJECTS</strong></dt> <dt>0x80520502</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-253">Un puntatore a interfaccia non punta a un'implementazione di interfaccia riconosciuta.</span><span class="sxs-lookup"><span data-stu-id="26b0f-253">An interface pointer does not point to a recognized interface implementation.</span></span> <span data-ttu-id="26b0f-254">L'implementazione personalizzata delle interfacce API per documenti XPS non è supportata.</span><span class="sxs-lookup"><span data-stu-id="26b0f-254">Custom implementation of XPS Document API interfaces is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_NOT_ENOUGH_GRADIENT_STOPS"></span><span id="xps_e_not_enough_gradient_stops"></span><dl> <span data-ttu-id="26b0f-255"><dt><strong>XPS_E_NOT_ENOUGH_GRADIENT_STOPS</strong></dt> <dt>0x8052050b</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-255"><dt><strong>XPS_E_NOT_ENOUGH_GRADIENT_STOPS</strong></dt> <dt>0x8052050b</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-256">La raccolta di arresti sfumatura ha meno di due arresti.</span><span class="sxs-lookup"><span data-stu-id="26b0f-256">The gradient stop collection has fewer than two stops.</span></span> <span data-ttu-id="26b0f-257">Una raccolta di arresti sfumati deve avere almeno due cursori sfumatura.</span><span class="sxs-lookup"><span data-stu-id="26b0f-257">A gradient stop collection must have at least two gradient stops.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_ODD_BIDILEVEL"></span><span id="xps_e_odd_bidilevel"></span><dl> <span data-ttu-id="26b0f-258"><dt><strong>XPS_E_ODD_BIDILEVEL</strong></dt> <dt>0x80520307</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-258"><dt><strong>XPS_E_ODD_BIDILEVEL</strong></dt> <dt>0x80520307</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-259">La stringa di testo è stata specificata come orientata lateralmente e da destra a sinistra.</span><span class="sxs-lookup"><span data-stu-id="26b0f-259">The text string was specified as being oriented sideways and right-to-left.</span></span> <span data-ttu-id="26b0f-260">Se il testo è orientato lateralmente, non può avere un livello BiDi che è un valore dispari (da destra a sinistra).</span><span class="sxs-lookup"><span data-stu-id="26b0f-260">If the text is oriented sideways, it cannot have a bidi level that is an odd value (right-to-left).</span></span> <span data-ttu-id="26b0f-261">Analogamente, se il livello BiDi è un valore dispari, il testo non può essere orientato lateralmente.</span><span class="sxs-lookup"><span data-stu-id="26b0f-261">Likewise, if the bidi level is an odd value, the text cannot be oriented sideways.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_ONE_TO_ONE_MAPPING_EXPECTED"></span><span id="xps_e_one_to_one_mapping_expected"></span><dl> <span data-ttu-id="26b0f-262"><dt><strong>XPS_E_ONE_TO_ONE_MAPPING_EXPECTED</strong></dt> <dt>0x80520308</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-262"><dt><strong>XPS_E_ONE_TO_ONE_MAPPING_EXPECTED</strong></dt> <dt>0x80520308</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-263">I mapping dei glifi non corrispondono al contenuto della stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="26b0f-263">The glyph mappings do not match the Unicode string contents.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_PACKAGE_WRITER_NOT_CLOSED"></span><span id="xps_e_package_writer_not_closed"></span><dl> <span data-ttu-id="26b0f-264"><dt><strong>XPS_E_PACKAGE_WRITER_NOT_CLOSED</strong></dt> <dt>0x8052050c</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-264"><dt><strong>XPS_E_PACKAGE_WRITER_NOT_CLOSED</strong></dt> <dt>0x8052050c</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-265">Il writer del pacchetto non è stato chiuso prima del rilascio.</span><span class="sxs-lookup"><span data-stu-id="26b0f-265">The package writer was not closed before it was released.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_RELATIONSHIP_EXTERNAL"></span><span id="xps_e_relationship_external"></span><dl> <span data-ttu-id="26b0f-266"><dt><strong>XPS_E_RELATIONSHIP_EXTERNAL</strong></dt> <dt>0x8052050a</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-266"><dt><strong>XPS_E_RELATIONSHIP_EXTERNAL</strong></dt> <dt>0x8052050a</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-267">Una relazione fa riferimento a una parte esterna al documento XPS.</span><span class="sxs-lookup"><span data-stu-id="26b0f-267">A relationship refers to a part that is outside of the XPS document.</span></span> <span data-ttu-id="26b0f-268">Tutto il contenuto di cui eseguire il rendering in un documento XPS deve essere contenuto nel documento XPS.</span><span class="sxs-lookup"><span data-stu-id="26b0f-268">All content to be rendered in an XPS document must be contained in the XPS document.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_RESOURCE_NOT_OWNED"></span><span id="xps_e_resource_not_owned"></span><dl> <span data-ttu-id="26b0f-269"><dt><strong>XPS_E_RESOURCE_NOT_OWNED</strong></dt> <dt>0x80520504</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-269"><dt><strong>XPS_E_RESOURCE_NOT_OWNED</strong></dt> <dt>0x80520504</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-270">Riservato.</span><span class="sxs-lookup"><span data-stu-id="26b0f-270">Reserved.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_RESTRICTED_FONT_NOT_OBFUSCATED"></span><span id="xps_e_restricted_font_not_obfuscated"></span><dl> <span data-ttu-id="26b0f-271"><dt><strong>XPS_E_RESTRICTED_FONT_NOT_OBFUSCATED</strong></dt> <dt>0x80520309</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-271"><dt><strong>XPS_E_RESTRICTED_FONT_NOT_OBFUSCATED</strong></dt> <dt>0x80520309</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-272"><em>Riservato</em>.</span><span class="sxs-lookup"><span data-stu-id="26b0f-272"><em>Reserved</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_STRING_TOO_LONG"></span><span id="xps_e_string_too_long"></span><dl> <span data-ttu-id="26b0f-273"><dt><strong>XPS_E_STRING_TOO_LONG</strong></dt> <dt>0x80520300</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-273"><dt><strong>XPS_E_STRING_TOO_LONG</strong></dt> <dt>0x80520300</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-274">Si è verificato un overflow <strong>size_t</strong> durante un tentativo di copia di una stringa in un nuovo buffer.</span><span class="sxs-lookup"><span data-stu-id="26b0f-274">A <strong>size_t</strong> overflow occurred during an attempt to copy a string into a new buffer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_TOO_MANY_INDICES"></span><span id="xps_e_too_many_indices"></span><dl> <span data-ttu-id="26b0f-275"><dt><strong>XPS_E_TOO_MANY_INDICES</strong></dt> <dt>0x80520301</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-275"><dt><strong>XPS_E_TOO_MANY_INDICES</strong></dt> <dt>0x80520301</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-276">Sono presenti più indici di glifo rispetto ai punti di codice Unicode.</span><span class="sxs-lookup"><span data-stu-id="26b0f-276">There were more glyph indices than Unicode code points.</span></span> <span data-ttu-id="26b0f-277">Se non sono presenti mapping di glifi, il numero di indici di glifi deve essere minore o uguale al numero di punti di codice Unicode.</span><span class="sxs-lookup"><span data-stu-id="26b0f-277">If there are no glyph mappings, the number of glyph indices must be less than or equal to the number of Unicode code points.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_UNAVAILABLE_PACKAGE"></span><span id="xps_e_unavailable_package"></span><dl> <span data-ttu-id="26b0f-278"><dt><strong>XPS_E_UNAVAILABLE_PACKAGE</strong></dt> <dt>0x80520114</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-278"><dt><strong>XPS_E_UNAVAILABLE_PACKAGE</strong></dt> <dt>0x80520114</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-279">Si è verificato un errore grave e il contenuto di XPS OM potrebbe non essere ripristinabile.</span><span class="sxs-lookup"><span data-stu-id="26b0f-279">A severe error occurred and the contents of the XPS OM might be unrecoverable.</span></span> <span data-ttu-id="26b0f-280">Alcuni componenti di XPS OM potrebbero ancora essere utilizzabili, ma sarà necessario verificarli prima di essere utilizzati ulteriormente.</span><span class="sxs-lookup"><span data-stu-id="26b0f-280">Some components of the XPS OM might still be usable, but they will need to be verified before being used further.</span></span> <span data-ttu-id="26b0f-281">Poiché lo stato di XPS OM non può essere stimato dopo la restituzione di questo errore, tutti i componenti di XPS OM devono essere rilasciati e rimossi.</span><span class="sxs-lookup"><span data-stu-id="26b0f-281">Because the state of the XPS OM cannot be predicted after this error is returned, all components of the XPS OM should be released and discarded.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_UNEXPECTED_COLORPROFILE"></span><span id="xps_e_unexpected_colorprofile"></span><dl> <span data-ttu-id="26b0f-282"><dt><strong>XPS_E_UNEXPECTED_COLORPROFILE</strong></dt> <dt>0x80520505</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-282"><dt><strong>XPS_E_UNEXPECTED_COLORPROFILE</strong></dt> <dt>0x80520505</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-283">Un profilo colori era presente quando non ne era previsto uno.</span><span class="sxs-lookup"><span data-stu-id="26b0f-283">A color profile was present when one was not expected.</span></span> <span data-ttu-id="26b0f-284">Un profilo colori è consentito solo quando il tipo di colore è <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_CONTEXT</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="26b0f-284">A color profile is only allowed when the color type is <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_CONTEXT</strong></a>.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_UNEXPECTED_CONTENT_TYPE"></span><span id="xps_e_unexpected_content_type"></span><dl> <span data-ttu-id="26b0f-285"><dt><strong>XPS_E_UNEXPECTED_CONTENT_TYPE</strong></dt> <dt>0x80520008</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-285"><dt><strong>XPS_E_UNEXPECTED_CONTENT_TYPE</strong></dt> <dt>0x80520008</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-286">La destinazione di una relazione non è il tipo previsto dal contesto della relazione.</span><span class="sxs-lookup"><span data-stu-id="26b0f-286">The target of a relationship is not the type expected by the context of the relationship.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_UNEXPECTED_RELATIONSHIP_TYPE"></span><span id="xps_e_unexpected_relationship_type"></span><dl> <span data-ttu-id="26b0f-287"><dt><strong>XPS_E_UNEXPECTED_RELATIONSHIP_TYPE</strong></dt> <dt>0x80520010</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-287"><dt><strong>XPS_E_UNEXPECTED_RELATIONSHIP_TYPE</strong></dt> <dt>0x80520010</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-288">Il tipo di relazione non è stato riconosciuto.</span><span class="sxs-lookup"><span data-stu-id="26b0f-288">The relationship type was not recognized.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_UNEXPECTED_RESTRICTED_FONT_RELATIONSHIP"></span><span id="xps_e_unexpected_restricted_font_relationship"></span><dl> <span data-ttu-id="26b0f-289"><dt><strong>XPS_E_UNEXPECTED_RESTRICTED_FONT_RELATIONSHIP</strong></dt> <dt>0x80520011</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-289"><dt><strong>XPS_E_UNEXPECTED_RESTRICTED_FONT_RELATIONSHIP</strong></dt> <dt>0x80520011</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-290">La raccolta di tipi di carattere con restrizioni contiene un tipo di carattere senza restrizioni.</span><span class="sxs-lookup"><span data-stu-id="26b0f-290">The restricted font collection contains an unrestricted font.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_VISUAL_CIRCULAR_REF"></span><span id="xps_e_visual_circular_ref"></span><dl> <span data-ttu-id="26b0f-291"><dt><strong>XPS_E_VISUAL_CIRCULAR_REF</strong></dt> <dt>0x80520501</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-291"><dt><strong>XPS_E_VISUAL_CIRCULAR_REF</strong></dt> <dt>0x80520501</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-292">Riservato.</span><span class="sxs-lookup"><span data-stu-id="26b0f-292">Reserved.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_XKEY_ATTR_PRESENT_OUTSIDE_RES_DICT"></span><span id="xps_e_xkey_attr_present_outside_res_dict"></span><dl> <span data-ttu-id="26b0f-293"><dt><strong>XPS_E_XKEY_ATTR_PRESENT_OUTSIDE_RES_DICT</strong></dt> <dt>0x80520400</dt> </span><span class="sxs-lookup"><span data-stu-id="26b0f-293"><dt><strong>XPS_E_XKEY_ATTR_PRESENT_OUTSIDE_RES_DICT</strong></dt> <dt>0x80520400</dt> </span></span></dl></td>
<td><span data-ttu-id="26b0f-294">Una geometria del percorso che non si trova in un dizionario risorse ha un attributo <strong>x:Key</strong> specificato.</span><span class="sxs-lookup"><span data-stu-id="26b0f-294">A path geometry that is not in a resource dictionary has an <strong>x:Key</strong> attribute specified.</span></span> <span data-ttu-id="26b0f-295">Le geometrie del percorso che non sono in un dizionario risorse non possono avere un attributo <strong>x:Key</strong> .</span><span class="sxs-lookup"><span data-stu-id="26b0f-295">Path geometries that are not in a resource dictionary cannot have an <strong>x:Key</strong> attribute.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="26b0f-296">Commenti</span><span class="sxs-lookup"><span data-stu-id="26b0f-296">Remarks</span></span>

<span data-ttu-id="26b0f-297">Alcuni metodi dell'API Document XPS effettuano chiamate all'API di creazione [pacchetti](/previous-versions/windows/desktop/opc/packaging) .</span><span class="sxs-lookup"><span data-stu-id="26b0f-297">Some XPS document API methods make calls to the [Packaging](/previous-versions/windows/desktop/opc/packaging) API.</span></span> <span data-ttu-id="26b0f-298">Per informazioni sui valori restituiti dell'API di creazione pacchetti, vedere errori di creazione [pacchetti](/previous-versions/windows/desktop/opc/packaging-errors).</span><span class="sxs-lookup"><span data-stu-id="26b0f-298">For information about the Packaging API return values, see [Packaging Errors](/previous-versions/windows/desktop/opc/packaging-errors).</span></span>

## <a name="requirements"></a><span data-ttu-id="26b0f-299">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26b0f-299">Requirements</span></span>



| <span data-ttu-id="26b0f-300">Requisito</span><span class="sxs-lookup"><span data-stu-id="26b0f-300">Requirement</span></span> | <span data-ttu-id="26b0f-301">Valore</span><span class="sxs-lookup"><span data-stu-id="26b0f-301">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26b0f-302">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26b0f-302">Minimum supported client</span></span><br/> | <span data-ttu-id="26b0f-303">Windows 7, Windows Vista con SP2 e aggiornamento della piattaforma solo per le applicazioni desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="26b0f-303">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="26b0f-304">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26b0f-304">Minimum supported server</span></span><br/> | <span data-ttu-id="26b0f-305">Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma solo per le \[ app desktop Windows server 2008\]</span><span class="sxs-lookup"><span data-stu-id="26b0f-305">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="26b0f-306">Intestazione</span><span class="sxs-lookup"><span data-stu-id="26b0f-306">Header</span></span><br/>                   | <dl> <span data-ttu-id="26b0f-307"><dt>Xpsobjectmodel. h</dt></span><span class="sxs-lookup"><span data-stu-id="26b0f-307"><dt>Xpsobjectmodel.h</dt></span></span> </dl>                                       |
| <span data-ttu-id="26b0f-308">IDL</span><span class="sxs-lookup"><span data-stu-id="26b0f-308">IDL</span></span><br/>                      | <dl> <span data-ttu-id="26b0f-309"><dt>XpsObjectModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="26b0f-309"><dt>XpsObjectModel.idl</dt></span></span> </dl>                                     |



## <a name="see-also"></a><span data-ttu-id="26b0f-310">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26b0f-310">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26b0f-311">Gestione degli errori in COM</span><span class="sxs-lookup"><span data-stu-id="26b0f-311">Error Handling in COM</span></span>](../com/error-handling-in-com.md)
</dt> </dl>

 


---
title: Elemento PARAM (WMP SDK)
description: L'elemento PARAM definisce un parametro personalizzato associato a una playlist o a un elemento di una playlist.
ms.assetid: d905a42a-ac89-4c99-94ca-b3b7060ebbdc
keywords:
- Finestra elementi PARAM Media Player
topic_type:
- apiref
api_name:
- PARAM Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7879f9dc9a8cf31afee5a3f1684af5cba33a9e0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332546"
---
# <a name="param-element"></a><span data-ttu-id="44a3d-104">PARAM (elemento)</span><span class="sxs-lookup"><span data-stu-id="44a3d-104">PARAM Element</span></span>

<span data-ttu-id="44a3d-105">L'elemento **param** definisce un parametro personalizzato associato a una playlist o a un elemento di una playlist.</span><span class="sxs-lookup"><span data-stu-id="44a3d-105">The **PARAM** element defines a custom parameter associated with a playlist or an element of a playlist.</span></span>

``` syntax
<PARAM
   NAME = "parameter name"
   VALUE = "parameter value"
/>
```

## <a name="parameters"></a><span data-ttu-id="44a3d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="44a3d-106">Parameters</span></span>

<span data-ttu-id="44a3d-107">Un parametro può essere associato anche alla visualizzazione anziché a un singolo clip, inserendo questo elemento direttamente dopo il tag **ASX** .</span><span class="sxs-lookup"><span data-stu-id="44a3d-107">A parameter can also be associated with the show rather than an individual clip, by placing this element directly after the **ASX** tag.</span></span> <span data-ttu-id="44a3d-108">A questi elementi viene fatto riferimento con i relativi nomi e un valore di indice che inizia con zero.</span><span class="sxs-lookup"><span data-stu-id="44a3d-108">These items are referenced by their names and an index value beginning with zero.</span></span>

> [!Note]  
> <span data-ttu-id="44a3d-109">Questo elemento **ASX** è disponibile solo per Windows Media Player versione 6,01 e successive.</span><span class="sxs-lookup"><span data-stu-id="44a3d-109">This **ASX** element is only available for Windows Media Player version 6.01 and later.</span></span> <span data-ttu-id="44a3d-110">L'installazione standard di Microsoft Internet Explorer 5 include una versione compatibile di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="44a3d-110">The standard installation of Microsoft Internet Explorer 5 includes a compatible version of Windows Media Player.</span></span>

 

## <a name="attributes"></a><span data-ttu-id="44a3d-111">Attributi</span><span class="sxs-lookup"><span data-stu-id="44a3d-111">Attributes</span></span>

<span data-ttu-id="44a3d-112">**NOME**</span><span class="sxs-lookup"><span data-stu-id="44a3d-112">**NAME**</span></span>

<span data-ttu-id="44a3d-113">Nome utilizzato per accedere al valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="44a3d-113">Name used to access the parameter value.</span></span> <span data-ttu-id="44a3d-114">Il nome può essere qualsiasi stringa valida.</span><span class="sxs-lookup"><span data-stu-id="44a3d-114">The name can be any valid string.</span></span> <span data-ttu-id="44a3d-115">Le stringhe seguenti sono già state definite.</span><span class="sxs-lookup"><span data-stu-id="44a3d-115">The following strings have already been defined.</span></span>



| <span data-ttu-id="44a3d-116">string</span><span class="sxs-lookup"><span data-stu-id="44a3d-116">String</span></span>                          | <span data-ttu-id="44a3d-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="44a3d-117">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44a3d-118">AllowShuffle</span><span class="sxs-lookup"><span data-stu-id="44a3d-118">AllowShuffle</span></span>                    | <span data-ttu-id="44a3d-119">L'attributo **value** specifica se la playlist del metafile consente alla funzionalità Windows Media Player shuffle di riprodurre le voci in ordine casuale.</span><span class="sxs-lookup"><span data-stu-id="44a3d-119">The **VALUE** attribute specifies whether the metafile playlist allows the Windows Media Player shuffle feature to play the entries in random order.</span></span> <span data-ttu-id="44a3d-120">L'attributo **value** può essere impostato su "Yes" o "No".</span><span class="sxs-lookup"><span data-stu-id="44a3d-120">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="44a3d-121">Il valore predefinito è "No".</span><span class="sxs-lookup"><span data-stu-id="44a3d-121">The default value is "No".</span></span>                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="44a3d-122">CanPause</span><span class="sxs-lookup"><span data-stu-id="44a3d-122">CanPause</span></span>                        | <span data-ttu-id="44a3d-123">L'attributo **value** specifica se l'utente può sospendere la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="44a3d-123">The **VALUE** attribute specifies whether the user can pause playback.</span></span> <span data-ttu-id="44a3d-124">L'attributo **value** può essere impostato su "Yes" o "No".</span><span class="sxs-lookup"><span data-stu-id="44a3d-124">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="44a3d-125">Il valore predefinito è "Yes".</span><span class="sxs-lookup"><span data-stu-id="44a3d-125">The default value is "Yes".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="44a3d-126">CanSeek</span><span class="sxs-lookup"><span data-stu-id="44a3d-126">CanSeek</span></span>                         | <span data-ttu-id="44a3d-127">L'attributo **value** specifica se l'utente può modificare la posizione di riproduzione corrente usando la barra di ricerca, l'avanzamento rapido o l'inversione veloce.</span><span class="sxs-lookup"><span data-stu-id="44a3d-127">The **VALUE** attribute specifies whether the user can change the current playback position by using the seek bar, fast forward, or fast reverse.</span></span> <span data-ttu-id="44a3d-128">L'attributo **value** può essere impostato su "Yes" o "No".</span><span class="sxs-lookup"><span data-stu-id="44a3d-128">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="44a3d-129">Il valore predefinito è "Yes".</span><span class="sxs-lookup"><span data-stu-id="44a3d-129">The default value is "Yes".</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="44a3d-130">CanSkipBack</span><span class="sxs-lookup"><span data-stu-id="44a3d-130">CanSkipBack</span></span>                     | <span data-ttu-id="44a3d-131">L'attributo **value** specifica se l'utente può passare all'elemento della playlist precedente **facendo clic su indietro.**</span><span class="sxs-lookup"><span data-stu-id="44a3d-131">The **VALUE** attribute specifies whether the user can skip backward to the previous playlist item by clicking **Previous**.</span></span> <span data-ttu-id="44a3d-132">L'attributo **value** può essere impostato su "Yes" o "No".</span><span class="sxs-lookup"><span data-stu-id="44a3d-132">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="44a3d-133">Il valore predefinito è "Yes".</span><span class="sxs-lookup"><span data-stu-id="44a3d-133">The default value is "Yes".</span></span>                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="44a3d-134">CanSkipForward</span><span class="sxs-lookup"><span data-stu-id="44a3d-134">CanSkipForward</span></span>                  | <span data-ttu-id="44a3d-135">L'attributo **value** specifica se l'utente può passare alla voce successiva della playlist facendo clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="44a3d-135">The **VALUE** attribute specifies whether the user can skip forward to the next playlist item by clicking **Next**.</span></span> <span data-ttu-id="44a3d-136">L'attributo **value** può essere impostato su "Yes" o "No".</span><span class="sxs-lookup"><span data-stu-id="44a3d-136">The **VALUE** attribute can be set to "Yes" or "No".</span></span> <span data-ttu-id="44a3d-137">Il valore predefinito è "Yes".</span><span class="sxs-lookup"><span data-stu-id="44a3d-137">The default value is "Yes".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="44a3d-138">CPRadioID</span><span class="sxs-lookup"><span data-stu-id="44a3d-138">CPRadioID</span></span>                       | <span data-ttu-id="44a3d-139">L'attributo **value** specifica l'ID di un feed di radio fornito da un archivio online di tipo 1.</span><span class="sxs-lookup"><span data-stu-id="44a3d-139">The **VALUE** attribute specifies the ID of a radio feed provided by a type 1 online store.</span></span> <span data-ttu-id="44a3d-140">Ovvero, l'attributo **value** deve essere uguale al campo RadioID di uno dei feed di radio nel catalogo del negozio online.</span><span class="sxs-lookup"><span data-stu-id="44a3d-140">That is, the **VALUE** attribute must be equal to the RadioID field of one of the radio feeds in the online store's catalog.</span></span> <span data-ttu-id="44a3d-141">L'elemento padre è l'elemento **ASX** .</span><span class="sxs-lookup"><span data-stu-id="44a3d-141">The parent element is the **ASX** element.</span></span>                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="44a3d-142">Codifica</span><span class="sxs-lookup"><span data-stu-id="44a3d-142">Encoding</span></span>                        | <span data-ttu-id="44a3d-143">L'attributo **value** è impostato su "UTF-8" per indicare che il metafile è un file con codifica Unicode (UTF-8).</span><span class="sxs-lookup"><span data-stu-id="44a3d-143">The **VALUE** attribute is set to "utf-8" to indicate that the metafile is a Unicode (UTF-8) encoded file.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="44a3d-144">HtmlFlink</span><span class="sxs-lookup"><span data-stu-id="44a3d-144">HtmlFlink</span></span>                       | <span data-ttu-id="44a3d-145">L'attributo **value** è una stringa fornita da un archivio online di tipo 1.</span><span class="sxs-lookup"><span data-stu-id="44a3d-145">The **VALUE** attribute is a string provided by a type 1 online store.</span></span> <span data-ttu-id="44a3d-146">Windows Media Player passa la stringa al metodo [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) , implementato dal plug-in Online Store.</span><span class="sxs-lookup"><span data-stu-id="44a3d-146">Windows Media Player passes the string to the [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) method, which is implemented by the online store's plug-in.</span></span> <span data-ttu-id="44a3d-147">Il metodo **GetItemInfo** restituisce l'URL della pagina Web da visualizzare nel riquadro **Now Playing** del lettore.</span><span class="sxs-lookup"><span data-stu-id="44a3d-147">The **GetItemInfo** method returns the URL of the webpage to display in the **Now Playing** pane of the Player.</span></span> <span data-ttu-id="44a3d-148">La pagina Web ha accesso a tutti i metodi esposti dall'oggetto **esterno** per il tipo 1.</span><span class="sxs-lookup"><span data-stu-id="44a3d-148">The webpage has access to all of the methods that the **External** object exposes to type 1 stores.</span></span> <span data-ttu-id="44a3d-149">Per un elenco di questi metodi, vedere [oggetto esterno per gli archivi online di tipo 1](external-object-for-type-1-online-stores.md).</span><span class="sxs-lookup"><span data-stu-id="44a3d-149">For a list of those methods, see [External Object for Type 1 Online Stores](external-object-for-type-1-online-stores.md).</span></span> |
| <span data-ttu-id="44a3d-150">HTMLView</span><span class="sxs-lookup"><span data-stu-id="44a3d-150">HTMLView</span></span>                        | <span data-ttu-id="44a3d-151">L'attributo **value** specifica un URL che viene visualizzato nel riquadro **ora di riproduzione** del lettore in modalità completa per la durata della playlist o della voce corrente a seconda che l'elemento padre sia l'elemento **ASX** o un elemento **entry** .</span><span class="sxs-lookup"><span data-stu-id="44a3d-151">The **VALUE** attribute specifies a URL that displays in the **Now Playing** pane of the full mode Player for the duration of the playlist or the current entry depending on whether the parent element is the **ASX** element or an **ENTRY** element.</span></span> <span data-ttu-id="44a3d-152">HTMLView non è supportato per il controllo Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="44a3d-152">HTMLView is not supported for the Windows Media Player control.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="44a3d-153">Log:*FieldName* \[ :*spazio dei nomi*\]</span><span class="sxs-lookup"><span data-stu-id="44a3d-153">Log:*FieldName*\[:*NameSpace*\]</span></span> | <span data-ttu-id="44a3d-154">L'attributo **value** specifica il valore a cui verrà impostato il campo di log indicato.</span><span class="sxs-lookup"><span data-stu-id="44a3d-154">The **VALUE** attribute specifies the value that the indicated log field will be set to.</span></span> <span data-ttu-id="44a3d-155">La parte:*namespace* dell'attributo **Name** è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="44a3d-155">The :*NameSpace* portion of the **NAME** attribute is optional.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="44a3d-156">PreBuffer</span><span class="sxs-lookup"><span data-stu-id="44a3d-156">Prebuffer</span></span>                       | <span data-ttu-id="44a3d-157">L'attributo **value** specifica se la voce della playlist successiva inizia a memorizzare il buffer prima della fine della voce corrente, che consente una transizione senza problemi.</span><span class="sxs-lookup"><span data-stu-id="44a3d-157">The **VALUE** attribute specifies whether the next playlist entry begins buffering before the end of the current entry, which enables a seamless transition.</span></span> <span data-ttu-id="44a3d-158">L'attributo **value** può essere impostato su "true" o "false".</span><span class="sxs-lookup"><span data-stu-id="44a3d-158">The **VALUE** attribute can be set to "true" or "false".</span></span>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="44a3d-159">ShowWhileBuffering</span><span class="sxs-lookup"><span data-stu-id="44a3d-159">ShowWhileBuffering</span></span>              | <span data-ttu-id="44a3d-160">L'attributo **value** specifica se un file di immagine a cui fa riferimento l'elemento **entry** corrente continua a essere visualizzato oltre la durata specificata, mentre la voce della playlist successiva viene memorizzata nel buffer.</span><span class="sxs-lookup"><span data-stu-id="44a3d-160">The **VALUE** attribute specifies whether an image file referenced by the current **ENTRY** element continues to display past its specified duration time while the next playlist entry is buffered.</span></span> <span data-ttu-id="44a3d-161">L'attributo **value** può essere impostato su "true" o "false".</span><span class="sxs-lookup"><span data-stu-id="44a3d-161">The **VALUE** attribute can be set to "true" or "false".</span></span>                                                                                                                                                                                                                                                                                                                                         |



 

<span data-ttu-id="44a3d-162">**VALUE**</span><span class="sxs-lookup"><span data-stu-id="44a3d-162">**VALUE**</span></span>

<span data-ttu-id="44a3d-163">Valore associato a questo parametro.</span><span class="sxs-lookup"><span data-stu-id="44a3d-163">Value associated with this parameter.</span></span> <span data-ttu-id="44a3d-164">Può essere un valore numerico o stringa.</span><span class="sxs-lookup"><span data-stu-id="44a3d-164">It can be either a numeric or string value.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="44a3d-165">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="44a3d-165">Parent/Child Elements</span></span>



| <span data-ttu-id="44a3d-166">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="44a3d-166">Hierarchy</span></span>       | <span data-ttu-id="44a3d-167">Elementi</span><span class="sxs-lookup"><span data-stu-id="44a3d-167">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="44a3d-168">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="44a3d-168">Parent elements</span></span> | <span data-ttu-id="44a3d-169">**ASX**, **voce**</span><span class="sxs-lookup"><span data-stu-id="44a3d-169">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="44a3d-170">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="44a3d-170">Child elements</span></span>  | <span data-ttu-id="44a3d-171">nessuno</span><span class="sxs-lookup"><span data-stu-id="44a3d-171">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="44a3d-172">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="44a3d-172">Remarks</span></span>

<span data-ttu-id="44a3d-173">Questo elemento consente agli utenti di inserire informazioni aggiuntive su ogni clip all'interno dell'elemento **entry** che la contiene.</span><span class="sxs-lookup"><span data-stu-id="44a3d-173">This element allows users to place additional information about each clip inside the **ENTRY** element that contains it.</span></span> <span data-ttu-id="44a3d-174">Per recuperare le informazioni sui metadati specificate nella **voce** della playlist, usare il *supporto*. metodo **GetItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="44a3d-174">To retrieve metadata information specified in the playlist **ENTRY**, use the *Media*.**getItemInfo** method.</span></span> <span data-ttu-id="44a3d-175">*Supporti*. il metodo **GetItemInfo** Recupera il valore dell'attributo **value** , dato il nome del parametro.</span><span class="sxs-lookup"><span data-stu-id="44a3d-175">The *Media*.**getItemInfo** method retrieves the value of the **VALUE** attribute, given the name of the parameter.</span></span> <span data-ttu-id="44a3d-176">Le versioni precedenti di Windows Media Player recuperare le informazioni sui metadati specificate nella **voce** della playlist, usando il metodo **GetMediaParameter** in base al nome del parametro e un numero di indice per la voce.</span><span class="sxs-lookup"><span data-stu-id="44a3d-176">Previous versions of Windows Media Player retrieve metadata information specified in the playlist **ENTRY**, using the **GetMediaParameter** method given the name of the parameter and an index number for the entry.</span></span>

<span data-ttu-id="44a3d-177">Un parametro può essere associato anche alla visualizzazione anziché a un singolo clip, inserendo questo elemento direttamente dopo il tag **ASX** .</span><span class="sxs-lookup"><span data-stu-id="44a3d-177">A parameter can also be associated with the show rather than an individual clip, by placing this element directly after the **ASX** tag.</span></span> <span data-ttu-id="44a3d-178">A questi elementi viene fatto riferimento con i relativi nomi e un valore di indice che inizia con zero.</span><span class="sxs-lookup"><span data-stu-id="44a3d-178">These items are referenced by their names and an index value beginning with zero.</span></span>

<span data-ttu-id="44a3d-179">**Nota**</span><span class="sxs-lookup"><span data-stu-id="44a3d-179">**Note**</span></span>

<span data-ttu-id="44a3d-180">Questo elemento **ASX** è disponibile solo per Windows Media Player versione 6,01 e successive.</span><span class="sxs-lookup"><span data-stu-id="44a3d-180">This **ASX** element is only available for Windows Media Player version 6.01 and later.</span></span> <span data-ttu-id="44a3d-181">L'installazione standard di Microsoft Internet Explorer 5 include una versione compatibile di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="44a3d-181">The standard installation of Microsoft Internet Explorer 5 includes a compatible version of Windows Media Player.</span></span>

## <a name="examples"></a><span data-ttu-id="44a3d-182">Esempio</span><span class="sxs-lookup"><span data-stu-id="44a3d-182">Examples</span></span>


```XML
<ASX VERSION="3.0">
   <TITLE>Example Media Player Show</TITLE>
   <PARAM NAME="Director" VALUE="Jane D." />
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <REF HREF="https://sample.microsoft.com/media.asf" />
      <PARAM NAME="Location" VALUE="North America" />
      <PARAM NAME="Release Date" VALUE="March 1998" />
   </ENTRY>
   
   <ENTRY>
      <TITLE>Another Clip</TITLE>
      <REF HREF="https://sample.microsoft.com/more_media.asf" />
      <PARAM NAME="Location" VALUE="Japan">
      <PARAM NAME="Release Date" VALUE="December 1996" />
   </ENTRY>
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="44a3d-183">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44a3d-183">Requirements</span></span>



| <span data-ttu-id="44a3d-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="44a3d-184">Requirement</span></span> | <span data-ttu-id="44a3d-185">Valore</span><span class="sxs-lookup"><span data-stu-id="44a3d-185">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44a3d-186">Versione</span><span class="sxs-lookup"><span data-stu-id="44a3d-186">Version</span></span><br/> | <span data-ttu-id="44a3d-187">Windows Media Player versione 7,0 o successiva, è necessario Windows Media Player 9 serie o versione successiva per gli attributi nome predefiniti, è necessario Windows Media Player 10 o versione successiva per i nomi predefiniti CanPause, CanSeek, CanSkipBack e CanSkipForward</span><span class="sxs-lookup"><span data-stu-id="44a3d-187">Windows Media Player version 7.0 or later, Windows Media Player 9 Series or later is required for the predefined NAME attributes, Windows Media Player 10 or later is required for the predefined names CanPause, CanSeek, CanSkipBack, and CanSkipForward</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="44a3d-188">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="44a3d-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44a3d-189">**Visualizzazione di pagine Web in Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="44a3d-189">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="44a3d-190">**Registrazione dei dati del flusso**</span><span class="sxs-lookup"><span data-stu-id="44a3d-190">**Logging Stream Data**</span></span>](logging-stream-data.md)
</dt> <dt>

[<span data-ttu-id="44a3d-191">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="44a3d-191">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="44a3d-192">**Informazioni di riferimento sui metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="44a3d-192">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 






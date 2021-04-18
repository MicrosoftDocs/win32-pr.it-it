---
title: Elemento MOREINFO
description: L'elemento MOREINFO specifica un URL di un sito Web, un indirizzo di posta elettronica o un comando script associato a una visualizzazione, una clip o un banner.
ms.assetid: b817ef1d-4ca0-45f4-942b-695eaf537110
keywords:
- Finestra elementi MOREINFO Media Player
topic_type:
- apiref
api_name:
- MOREINFO Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: efc54fe9745566ec7eaa87b7f0f4645b07a055f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325440"
---
# <a name="moreinfo-element"></a><span data-ttu-id="d71d3-104">Elemento MOREINFO</span><span class="sxs-lookup"><span data-stu-id="d71d3-104">MOREINFO Element</span></span>

<span data-ttu-id="d71d3-105">L'elemento **moreinfo** specifica un URL di un sito Web, un indirizzo di posta elettronica o un comando script associato a una visualizzazione, una clip o un banner.</span><span class="sxs-lookup"><span data-stu-id="d71d3-105">The **MOREINFO** element specifies a URL to a website, email address, or script command associated with a show, clip, or banner.</span></span>

``` syntax
<MOREINFO
   HREF = "URL"
   TARGET = "Frame"
/>
```

## <a name="attributes"></a><span data-ttu-id="d71d3-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="d71d3-106">Attributes</span></span>

<span data-ttu-id="d71d3-107">**Href** (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="d71d3-107">**HREF** (required)</span></span>

<span data-ttu-id="d71d3-108">URL di un sito Web, un indirizzo di posta elettronica o un comando di script.</span><span class="sxs-lookup"><span data-stu-id="d71d3-108">URL to a website, email address, or script command.</span></span>

<span data-ttu-id="d71d3-109">**DESTINAZIONE**</span><span class="sxs-lookup"><span data-stu-id="d71d3-109">**TARGET**</span></span>

<span data-ttu-id="d71d3-110">Valore che definisce il frame o la finestra in cui il browser aprirà la pagina definita dall'attributo **href** .</span><span class="sxs-lookup"><span data-stu-id="d71d3-110">Value defining the frame or window in which the browser will open the page defined by the **HREF** attribute.</span></span>

<span data-ttu-id="d71d3-111">Può trattarsi di una stringa contenente il nome di una finestra o di uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d71d3-111">This can be a string containing a window name, or one of the following values.</span></span>



| <span data-ttu-id="d71d3-112">Valore</span><span class="sxs-lookup"><span data-stu-id="d71d3-112">Value</span></span>    | <span data-ttu-id="d71d3-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d71d3-113">Description</span></span>                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d71d3-114">\_vuoto</span><span class="sxs-lookup"><span data-stu-id="d71d3-114">\_blank</span></span>  | <span data-ttu-id="d71d3-115">Il documento viene caricato in una nuova finestra del browser.</span><span class="sxs-lookup"><span data-stu-id="d71d3-115">The document loads in a new browser window.</span></span>                                                                              |
| <span data-ttu-id="d71d3-116">\_auto</span><span class="sxs-lookup"><span data-stu-id="d71d3-116">\_self</span></span>   | <span data-ttu-id="d71d3-117">Il documento viene caricato nello stesso frame del documento corrente contenente il controllo Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="d71d3-117">The document loads in the same frame as the current document containing the Windows Media Player control.</span></span>                |
| <span data-ttu-id="d71d3-118">\_padre</span><span class="sxs-lookup"><span data-stu-id="d71d3-118">\_parent</span></span> | <span data-ttu-id="d71d3-119">Il documento viene caricato nel frame padre immediato del frame corrente o nel frame corrente se non è presente alcun frame padre.</span><span class="sxs-lookup"><span data-stu-id="d71d3-119">The document loads in the immediate parent frame of the current frame, or the current frame if there is no parent frame.</span></span> |
| <span data-ttu-id="d71d3-120">\_In alto</span><span class="sxs-lookup"><span data-stu-id="d71d3-120">\_top</span></span>    | <span data-ttu-id="d71d3-121">Il documento viene caricato nella finestra del browser completo, sostituendo tutti gli altri frame o documenti.</span><span class="sxs-lookup"><span data-stu-id="d71d3-121">The document loads in the full browser window, replacing all other frames or documents.</span></span>                                  |



 

## <a name="parentchild-elements"></a><span data-ttu-id="d71d3-122">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="d71d3-122">Parent/Child Elements</span></span>



| <span data-ttu-id="d71d3-123">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="d71d3-123">Hierarchy</span></span>       | <span data-ttu-id="d71d3-124">Elementi</span><span class="sxs-lookup"><span data-stu-id="d71d3-124">Elements</span></span>                       |
|-----------------|--------------------------------|
| <span data-ttu-id="d71d3-125">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="d71d3-125">Parent elements</span></span> | <span data-ttu-id="d71d3-126">**ASX**, **voce**, **banner**</span><span class="sxs-lookup"><span data-stu-id="d71d3-126">**ASX**, **ENTRY**, **BANNER**</span></span> |
| <span data-ttu-id="d71d3-127">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="d71d3-127">Child elements</span></span>  | <span data-ttu-id="d71d3-128">nessuno</span><span class="sxs-lookup"><span data-stu-id="d71d3-128">None</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="d71d3-129">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="d71d3-129">Remarks</span></span>

<span data-ttu-id="d71d3-130">Questo elemento specifica un URL di un sito Web, un indirizzo di posta elettronica **o un comando di script. L'utente può accedere alla destinazione dell'URL facendo clic sul grafico o sul testo associato all'elemento MOREINFO** .</span><span class="sxs-lookup"><span data-stu-id="d71d3-130">This element specifies a URL to a website, email address, **or script command. The user can access the target of the URL by clicking on the graphic or text associated with the MOREINFO** element.</span></span> <span data-ttu-id="d71d3-131">I dettagli dipendono dall'elemento padre dell'elemento **moreinfo** :</span><span class="sxs-lookup"><span data-stu-id="d71d3-131">The details depend on the parent element of the **MOREINFO** element:</span></span>

-   <span data-ttu-id="d71d3-132">Se l'elemento **moreinfo** è figlio di un elemento **ASX** , l'utente può accedere all'URL facendo clic sul titolo show.</span><span class="sxs-lookup"><span data-stu-id="d71d3-132">If the **MOREINFO** element is the child of an **ASX** element, the user can access the URL by clicking the show title.</span></span>
-   <span data-ttu-id="d71d3-133">Se l'elemento **moreinfo** è figlio di un elemento **entry** , l'utente può accedere all'URL facendo clic sul titolo della clip.</span><span class="sxs-lookup"><span data-stu-id="d71d3-133">If the **MOREINFO** element is the child of an **ENTRY** element, the user can access the URL by clicking the clip title.</span></span>
-   <span data-ttu-id="d71d3-134">Se l'elemento **moreinfo** è figlio di un elemento **banner** , l'utente può accedere all'URL facendo clic sull'icona del banner.</span><span class="sxs-lookup"><span data-stu-id="d71d3-134">If the **MOREINFO** element is the child of a **BANNER** element, the user can access the URL by clicking the banner graphic.</span></span>

<span data-ttu-id="d71d3-135">Se l'attributo **href** specifica un URL di un sito Web, il browser si apre e passa all'URL.</span><span class="sxs-lookup"><span data-stu-id="d71d3-135">If the **HREF** attribute specifies a URL to a website, the browser opens and navigates to the URL.</span></span> <span data-ttu-id="d71d3-136">Se l'attributo **href** specifica un indirizzo di posta elettronica, viene avviata l'applicazione di posta elettronica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d71d3-136">If the **HREF** attribute specifies an email address, the user's email application starts.</span></span> <span data-ttu-id="d71d3-137">Se l'attributo **href** specifica un comando script, il comando script viene eseguito nel browser.</span><span class="sxs-lookup"><span data-stu-id="d71d3-137">If the **HREF** attribute specifies a script command, the script command executes in the browser.</span></span>

<span data-ttu-id="d71d3-138">**Nota**</span><span class="sxs-lookup"><span data-stu-id="d71d3-138">**Note**</span></span>

<span data-ttu-id="d71d3-139">Se l'elemento **moreinfo** viene visualizzato all'interno di un elemento **ASX** o **entry** , quando il cursore del mouse viene posizionato sul titolo della Mostra (per un elemento **ASX** ) o su una clip (per un elemento **entry** ), l'URL definito nell'attributo **href** può essere selezionato e accessibile da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="d71d3-139">If the **MOREINFO** element appears within an **ASX** or **ENTRY** element, when the mouse cursor is held over the title of the show (for an **ASX** element) or clip (for an **ENTRY** element), the URL defined in the **HREF** attribute can be selected and accessed by Windows Media Player.</span></span>

<span data-ttu-id="d71d3-140">L'attributo di **destinazione** consente di definire il frame o la finestra in cui il browser aprirà la pagina definita dall'attributo **href** .</span><span class="sxs-lookup"><span data-stu-id="d71d3-140">The **TARGET** attribute defines the frame or window in which the browser will open the page defined by the **HREF** attribute.</span></span> <span data-ttu-id="d71d3-141">I valori per questo attributo seguono la sintassi HTML standard e le definizioni.</span><span class="sxs-lookup"><span data-stu-id="d71d3-141">The values for this attribute follow standard HTML syntax and definitions.</span></span> <span data-ttu-id="d71d3-142">Nel caso di un controllo incorporato in una pagina Web, se non è stato definito alcun attributo di **destinazione** , l'URL caricherà la finestra del browser corrente e sostituirà la pagina esistente, il che significa che il contenuto smette di essere riprodotto.</span><span class="sxs-lookup"><span data-stu-id="d71d3-142">In the case of a control embedded in a webpage, if no **TARGET** attribute is defined, the URL loads the current browser window and replaces the existing page, which means the content stops playing.</span></span> <span data-ttu-id="d71d3-143">È pertanto consigliabile specificare sempre un attributo di **destinazione** quando si incorpora il controllo Media Player di Windows in una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="d71d3-143">Therefore, it is recommended that you always specify a **TARGET** attribute when embedding the Windows Media Player control in a webpage.</span></span>

<span data-ttu-id="d71d3-144">Se il metafile viene aperto nel Media Player Windows autonomo, l'attributo di **destinazione** viene ignorato e l'URL viene caricato in una finestra del browser esistente.</span><span class="sxs-lookup"><span data-stu-id="d71d3-144">If the metafile is opened in the stand-alone Windows Media Player, the **TARGET** attribute is ignored, and the URL loads in an existing browser window.</span></span> <span data-ttu-id="d71d3-145">Se non è presente alcuna finestra del browser attualmente aperta, l'URL viene caricato in una nuova finestra del browser.</span><span class="sxs-lookup"><span data-stu-id="d71d3-145">If there is no browser window currently open, the URL loads in a new browser window.</span></span>

## <a name="examples"></a><span data-ttu-id="d71d3-146">Esempio</span><span class="sxs-lookup"><span data-stu-id="d71d3-146">Examples</span></span>


```XML
<ASX VERSION="3.0">

   <TITLE>Example Media Player Show</TITLE>
   <MOREINFO HREF="https://example.microsoft.com/info/show_info.htm" />
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <MOREINFO HREF="https://example.microsoft.com/info/clip1_info.htm" />
      <REF HREF="mms://example.microsoft.com/media.asf" />
   </ENTRY>
   
</ASX>

```



## <a name="requirements"></a><span data-ttu-id="d71d3-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d71d3-147">Requirements</span></span>



| <span data-ttu-id="d71d3-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="d71d3-148">Requirement</span></span> | <span data-ttu-id="d71d3-149">Valore</span><span class="sxs-lookup"><span data-stu-id="d71d3-149">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="d71d3-150">Versione</span><span class="sxs-lookup"><span data-stu-id="d71d3-150">Version</span></span><br/> | <span data-ttu-id="d71d3-151">Windows Media Player versione 70 o successiva</span><span class="sxs-lookup"><span data-stu-id="d71d3-151">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d71d3-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d71d3-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d71d3-153">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="d71d3-153">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="d71d3-154">**Informazioni di riferimento sui metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="d71d3-154">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 






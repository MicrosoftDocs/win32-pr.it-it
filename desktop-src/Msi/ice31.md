---
description: ICE31 convalida tutti gli stili di carattere predefiniti usati nei controlli che visualizzano il testo. Consente inoltre di verificare che la proprietà DefaultUIFont faccia riferimento a uno stile del tipo di carattere valido.
ms.assetid: 07e60774-0e26-4a50-b818-a8f074512e3e
title: ICE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4797d577ceaa2a2b7838f1f03a8577d9a633fb65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232246"
---
# <a name="ice31"></a><span data-ttu-id="6cfb0-104">ICE31</span><span class="sxs-lookup"><span data-stu-id="6cfb0-104">ICE31</span></span>

<span data-ttu-id="6cfb0-105">ICE31 convalida tutti gli stili di carattere predefiniti usati nei [controlli](controls.md) che visualizzano il testo.</span><span class="sxs-lookup"><span data-stu-id="6cfb0-105">ICE31 validates any predefined font styles used in [controls](controls.md) that display text.</span></span> <span data-ttu-id="6cfb0-106">Consente inoltre di verificare che la proprietà [**DefaultUIFont**](defaultuifont.md) faccia riferimento a uno stile del tipo di carattere valido.</span><span class="sxs-lookup"><span data-stu-id="6cfb0-106">It also validates that the [**DefaultUIFont**](defaultuifont.md) property refers to a valid font style.</span></span>

<span data-ttu-id="6cfb0-107">I controlli possono avere uno stile del carattere predefinito, come descritto in [aggiunta di controlli e testo](adding-controls-and-text.md).</span><span class="sxs-lookup"><span data-stu-id="6cfb0-107">Controls can have a predefined font style as described in [Adding Controls and Text](adding-controls-and-text.md).</span></span> <span data-ttu-id="6cfb0-108">Per impostare il tipo di carattere e lo stile del carattere di una stringa di testo, anteporre alla stringa dei caratteri visualizzati lo stile { \\ Style} o {&*Style*}.</span><span class="sxs-lookup"><span data-stu-id="6cfb0-108">To set the font and font style of a text string, prefix the string of displayed characters with {\\style} or {&*style*}.</span></span> <span data-ttu-id="6cfb0-109">Dove Style è un identificatore elencato nella colonna TextStyle della [tabella TextStyle](textstyle-table.md).</span><span class="sxs-lookup"><span data-stu-id="6cfb0-109">Where style is an identifier listed in the TextStyle column of the [TextStyle table](textstyle-table.md).</span></span> <span data-ttu-id="6cfb0-110">Se nessuna di queste è presente, ma la proprietà [**DefaultUIFont**](defaultuifont.md) è definita come uno stile di testo valido, verrà usato tale tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="6cfb0-110">If neither of these are present, but the [**DefaultUIFont**](defaultuifont.md) property is defined as a valid text style, that font will be used.</span></span>

<span data-ttu-id="6cfb0-111">ICE31 controlla la colonna di testo per ogni controllo nella [tabella dei controlli](control-table.md) per verificare che sia presente una voce valida nella [tabella TextStyle](textstyle-table.md).</span><span class="sxs-lookup"><span data-stu-id="6cfb0-111">ICE31 checks the Text column for each control in the [Control Table](control-table.md) to verifies that a valid entry exist in the [TextStyle table](textstyle-table.md).</span></span>

<span data-ttu-id="6cfb0-112">ICE31 ignora il [controllo ScrollableText](scrollabletext-control.md).</span><span class="sxs-lookup"><span data-stu-id="6cfb0-112">ICE31 ignores the [ScrollableText Control](scrollabletext-control.md).</span></span>

## <a name="results"></a><span data-ttu-id="6cfb0-113">Risultati</span><span class="sxs-lookup"><span data-stu-id="6cfb0-113">Results</span></span>

<span data-ttu-id="6cfb0-114">ICE31 Invia un messaggio di errore per gli stili non definiti, i nomi di stile troppo lunghi, una tabella TextStyle mancante e i tag di stile senza parentesi graffa di chiusura.</span><span class="sxs-lookup"><span data-stu-id="6cfb0-114">ICE31 posts an error message for undefined styles, style names that are too long, a missing TextStyle table, and style tags with no closing brace.</span></span>

<span data-ttu-id="6cfb0-115">ICE31 pubblica un avviso se il tag di stile non si trova all'inizio della riga o se un controllo ha più tag di stile.</span><span class="sxs-lookup"><span data-stu-id="6cfb0-115">ICE31 posts a warning if the style tag is not at the beginning of the line, or if a control has multiple style tags.</span></span>

## <a name="example"></a><span data-ttu-id="6cfb0-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="6cfb0-116">Example</span></span>

<span data-ttu-id="6cfb0-117">ICE31 invia gli errori seguenti per l'esempio illustrato:</span><span class="sxs-lookup"><span data-stu-id="6cfb0-117">ICE31 posts the following errors for the example shown:</span></span>

-   <span data-ttu-id="6cfb0-118">Il controllo DialogB. Control1 USA undefined TextStyle BadStyle.</span><span class="sxs-lookup"><span data-stu-id="6cfb0-118">Control DialogB.Control1 uses undefined TextStyle BadStyle.</span></span>
-   <span data-ttu-id="6cfb0-119">Il controllo DialogB. Controllo2 USA undefined TextStyle BadStyle.</span><span class="sxs-lookup"><span data-stu-id="6cfb0-119">Control DialogB.Control2 uses undefined TextStyle BadStyle.</span></span>
-   <span data-ttu-id="6cfb0-120">Per il controllo DialogB. Control6 manca la parentesi graffa di chiusura nello stile del testo.</span><span class="sxs-lookup"><span data-stu-id="6cfb0-120">Control DialogB.Control6 is missing closing brace in text style.</span></span>
-   <span data-ttu-id="6cfb0-121">Il controllo DialogB. Control3 specifica uno stile del testo troppo lungo per essere valido.</span><span class="sxs-lookup"><span data-stu-id="6cfb0-121">Control DialogB.Control3 specifies a text style that is too long to be valid.</span></span>

<span data-ttu-id="6cfb0-122">ICE31 invia l'avviso seguente per l'esempio illustrato:</span><span class="sxs-lookup"><span data-stu-id="6cfb0-122">ICE31 posts the following warning for the example shown:</span></span>

-   <span data-ttu-id="6cfb0-123">Il tag di stile testo in DialogB. Control4 non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="6cfb0-123">Text Style tag in DialogB.Control4 has no effect.</span></span> <span data-ttu-id="6cfb0-124">Si vuole che venga visualizzato come testo?</span><span class="sxs-lookup"><span data-stu-id="6cfb0-124">Do you really want it to appear as text?</span></span>

<span data-ttu-id="6cfb0-125">[Tabella di controllo](control-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="6cfb0-125">[Control Table](control-table.md) (partial)</span></span>



| <span data-ttu-id="6cfb0-126">Finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="6cfb0-126">Dialog</span></span>  | <span data-ttu-id="6cfb0-127">Control</span><span class="sxs-lookup"><span data-stu-id="6cfb0-127">Control</span></span>  | <span data-ttu-id="6cfb0-128">Testo</span><span class="sxs-lookup"><span data-stu-id="6cfb0-128">Text</span></span>                                                                                                                                                                |
|---------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cfb0-129">Finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="6cfb0-129">DialogA</span></span> | <span data-ttu-id="6cfb0-130">Control0</span><span class="sxs-lookup"><span data-stu-id="6cfb0-130">Control0</span></span> | <span data-ttu-id="6cfb0-131">{ \\ OKStyle} questo è il testo da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="6cfb0-131">{\\OKStyle}This is the text to display.</span></span>                                                                                                                             |
| <span data-ttu-id="6cfb0-132">Finestra di dialogo</span><span class="sxs-lookup"><span data-stu-id="6cfb0-132">DialogA</span></span> | <span data-ttu-id="6cfb0-133">Control1</span><span class="sxs-lookup"><span data-stu-id="6cfb0-133">Control1</span></span> | <span data-ttu-id="6cfb0-134">{&OKStyle} Testo da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="6cfb0-134">{&OKStyle}This is the text to display.</span></span>                                                                                                                              |
| <span data-ttu-id="6cfb0-135">DialogB</span><span class="sxs-lookup"><span data-stu-id="6cfb0-135">DialogB</span></span> | <span data-ttu-id="6cfb0-136">Control1</span><span class="sxs-lookup"><span data-stu-id="6cfb0-136">Control1</span></span> | <span data-ttu-id="6cfb0-137">{&BadStyle} Testo da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="6cfb0-137">{&BadStyle}This is the text to display.</span></span>                                                                                                                             |
| <span data-ttu-id="6cfb0-138">DialogB</span><span class="sxs-lookup"><span data-stu-id="6cfb0-138">DialogB</span></span> | <span data-ttu-id="6cfb0-139">Controllo2</span><span class="sxs-lookup"><span data-stu-id="6cfb0-139">Control2</span></span> | <span data-ttu-id="6cfb0-140">{ \\ BadStyle} questo è il testo da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="6cfb0-140">{\\BadStyle}This is the text to display.</span></span>                                                                                                                            |
| <span data-ttu-id="6cfb0-141">DialogB</span><span class="sxs-lookup"><span data-stu-id="6cfb0-141">DialogB</span></span> | <span data-ttu-id="6cfb0-142">Control3</span><span class="sxs-lookup"><span data-stu-id="6cfb0-142">Control3</span></span> | <span data-ttu-id="6cfb0-143">{&stile costituito da più di 72 caratteri e pertanto non può essere uno stile anche se in qualche modo si è gestito per ottenerlo nella tabella TextStyle} Testo da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="6cfb0-143">{&Style that is over 72 chars and therefore cannot possibly be a style even if somehow you did manage to get it in the TextStyle table}This is the text to display.</span></span> |
| <span data-ttu-id="6cfb0-144">DialogB</span><span class="sxs-lookup"><span data-stu-id="6cfb0-144">DialogB</span></span> | <span data-ttu-id="6cfb0-145">Control4</span><span class="sxs-lookup"><span data-stu-id="6cfb0-145">Control4</span></span> | <span data-ttu-id="6cfb0-146">Avviso { \\ OKStyle} questo è il testo da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="6cfb0-146">Warning {\\OKStyle}This is the text to display.</span></span>                                                                                                                     |
| <span data-ttu-id="6cfb0-147">DialogB</span><span class="sxs-lookup"><span data-stu-id="6cfb0-147">DialogB</span></span> | <span data-ttu-id="6cfb0-148">Control5</span><span class="sxs-lookup"><span data-stu-id="6cfb0-148">Control5</span></span> | <span data-ttu-id="6cfb0-149">{ \\ OKStyle} {&OKStyle} questo è il testo da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="6cfb0-149">{\\OKStyle}{&OKStyle}This is the text to display.</span></span>                                                                                                                   |
| <span data-ttu-id="6cfb0-150">DialogB</span><span class="sxs-lookup"><span data-stu-id="6cfb0-150">DialogB</span></span> | <span data-ttu-id="6cfb0-151">Control6</span><span class="sxs-lookup"><span data-stu-id="6cfb0-151">Control6</span></span> | <span data-ttu-id="6cfb0-152">{ \\ OKStyle questo è il testo da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="6cfb0-152">{\\OKStyle This is the text to display.</span></span>                                                                                                                             |



 

<span data-ttu-id="6cfb0-153">[Tabella TextStyle](textstyle-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="6cfb0-153">[TextStyle table](textstyle-table.md) (partial)</span></span>



| <span data-ttu-id="6cfb0-154">TextStyle</span><span class="sxs-lookup"><span data-stu-id="6cfb0-154">TextStyle</span></span> |
|-----------|
| <span data-ttu-id="6cfb0-155">OkStyle</span><span class="sxs-lookup"><span data-stu-id="6cfb0-155">OkStyle</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="6cfb0-156">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6cfb0-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cfb0-157">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="6cfb0-157">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




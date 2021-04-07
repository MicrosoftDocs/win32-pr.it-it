---
title: Esempio di file SAMI
description: Esempio di file SAMI
ms.assetid: 52b566f1-0d87-4bf2-87b3-3821e69a5699
keywords:
- Windows Media Player, Media Interchange accessibile sincronizzato (SAMI)
- Modello a oggetti di Windows Media Player, Media Interchange accessibile sincronizzato (SAMI)
- modello a oggetti, interscambio multimediale accessibile sincronizzato (SAMI)
- Windows Media Player Mobile, Media Interchange accessibile sincronizzato (SAMI)
- Controllo ActiveX Windows Media Player, Media Interchange accessibile sincronizzato (SAMI)
- Windows Media Player Mobile ActiveX Control, Synchronized Accessible Media Interchange (SAMI)
- Controllo ActiveX, interscambio multimediale accessibile sincronizzato (SAMI)
- SAMI (Synchronized Accessible Media Interchange), file
- SAMI (interscambio multimediale accessibile sincronizzato), file
- SAMI (Synchronized Accessible Media Interchange), codice di esempio
- SAMI (interscambio multimediale accessibile sincronizzato), codice di esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9634de52f71b4ca1db151bdf9104c3891c8ce5d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "103885921"
---
# <a name="sami-file-example"></a><span data-ttu-id="81129-114">Esempio di file SAMI</span><span class="sxs-lookup"><span data-stu-id="81129-114">SAMI File Example</span></span>

<span data-ttu-id="81129-115">Il codice di esempio seguente è un file SAMI completo con un set di testo della didascalia chiuso e diverse dichiarazioni di classe per lo stile del testo e la lingua della didascalia.</span><span class="sxs-lookup"><span data-stu-id="81129-115">The following example code is a complete SAMI file with one set of closed caption text and several class declarations for text style and caption language.</span></span>


```C++
<SAMI>
<HEAD>
   <STYLE TYPE = "text/css">
   <!--
   /* P defines the basic style selector for closed caption paragraph text */
   P {font-family:sans-serif; color:white;}
   /* Source, Small, and Big define additional ID selectors for closed caption text */
   #Source {color: orange; font-family: arial; font-size: 12pt;}
   #Small {Name: SmallTxt; font-size: 8pt; color: yellow;}
   #Big {Name: BigTxt; font-size: 12pt; color: magenta;}
   /* ENUSCC and FRFRCC define language class selectors for closed caption text */
   .ENUSCC {Name: 'English Captions'; lang: en-US; SAMIType: CC;}
   .FRFRCC {Name: 'French Captions'; lang: fr-FR; SAMIType: CC;}
   -->
   </STYLE>
</HEAD>
<BODY>
   <!<entity type="mdash"/>- The closed caption text displays at 1000 milliseconds. -->
   <SYNC Start = 1000>
      <!-- English closed captions -->
      <P Class = ENUSCC ID = Source>Narrator
      <P Class = ENUSCC>Great reason to visit Seattle, brought to you by two out-of-staters.
      <!-- French closed captions -->
      <P Class = FRFRCC ID = Source>Narrateur
      <P Class = FRFRCC>Deux personnes ne venant la r&eacute;gion vous donnent de bonnes raisons de visiter Seattle.
</BODY>
</SAMI>

```



<span data-ttu-id="81129-116">Gli stili definiti in un file SAMI sono conformi alla sintassi standard del selettore CSS per gli elementi, le classi e gli ID.</span><span class="sxs-lookup"><span data-stu-id="81129-116">Styles defined within a SAMI file conform to standard CSS selector syntax for elements, classes, and IDs.</span></span> <span data-ttu-id="81129-117">Nell'elemento BODY tutti gli elementi P hanno lo stile definito per il selettore di elementi P nell'elemento STYLE.</span><span class="sxs-lookup"><span data-stu-id="81129-117">In the BODY element, all P elements have the style defined for the P element selector in the STYLE element.</span></span> <span data-ttu-id="81129-118">L'attributo Class di un elemento specifica la lingua dell'elemento in base a quanto definito dai selettori di classe nell'elemento STYLE (i selettori che iniziano con i punti).</span><span class="sxs-lookup"><span data-stu-id="81129-118">The class attribute of an element specifies the language of that element as defined by the class selectors in the STYLE element (the selectors beginning with periods).</span></span> <span data-ttu-id="81129-119">I nomi di linguaggio specificati dai selettori di classe possono essere qualsiasi stringa.</span><span class="sxs-lookup"><span data-stu-id="81129-119">The language names specified by the class selectors can be any string.</span></span> <span data-ttu-id="81129-120">Gli elementi con l'attributo ID specificati hanno uno stile aggiuntivo applicato come indicato dai selettori di ID nell'elemento STYLE, ovvero i selettori con prefisso \# Characters.</span><span class="sxs-lookup"><span data-stu-id="81129-120">Elements with the ID attribute specified have additional styling applied as indicated by the ID selectors in the STYLE element (the selectors prefixed with \# characters).</span></span>

<span data-ttu-id="81129-121">Se utilizzati insieme al modello a oggetti di Windows Media Player, i selettori di classe corrispondono a *ClosedCaption*. Proprietà **SAMILang** , che può essere usata per specificare la lingua delle didascalie.</span><span class="sxs-lookup"><span data-stu-id="81129-121">When used in conjunction with the Windows Media Player object model, the class selectors correspond to the *ClosedCaption*.**SAMILang** property, which can be used to specify the language of the captions.</span></span> <span data-ttu-id="81129-122">I selettori ID corrispondono a *ClosedCaption*. Proprietà **SAMIStyle** , che può essere usata per specificare lo stile in cui verranno visualizzate le didascalie.</span><span class="sxs-lookup"><span data-stu-id="81129-122">The ID selectors correspond to the *ClosedCaption*.**SAMIStyle** property, which can be used to specify the style the captions will appear in.</span></span>

<span data-ttu-id="81129-123">Per ulteriori informazioni sulla creazione di file SAMI, vedere informazioni su SAMI 1,0 sul [sito Web Microsoft](/documentation/).</span><span class="sxs-lookup"><span data-stu-id="81129-123">For more information about creating SAMI files, see Understanding SAMI 1.0 at the [Microsoft website](/documentation/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="81129-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="81129-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81129-125">**Aggiunta di didascalie chiuse a file multimediali digitali**</span><span class="sxs-lookup"><span data-stu-id="81129-125">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 
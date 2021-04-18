---
title: File di definizione dell'interfaccia
description: File di definizione dell'interfaccia
ms.assetid: ed5f7c61-c830-4075-a79f-d5539454bd3b
keywords:
- Interfacce di Media Player di Windows, file di definizione dell'interfaccia
- interfacce, file di definizione dell'interfaccia
- file per le interfacce, definizione dell'interfaccia
- file di definizione dell'interfaccia, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bd06708a99a15dc9a8266278850c0507007f058
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298585"
---
# <a name="skin-definition-file"></a><span data-ttu-id="f92a6-107">File di definizione dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="f92a6-107">Skin Definition File</span></span>

<span data-ttu-id="f92a6-108">I file di definizione dell'interfaccia contengono le istruzioni di base per l'utilizzo dell'interfaccia e la posizione in cui possono essere trovati altri file usati dall'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="f92a6-108">Skin definition files contain the basic instructions for what the skin does and where other files used by the skin can be found.</span></span> <span data-ttu-id="f92a6-109">Può essere presente un solo file di definizione di interfaccia per un'interfaccia e ha un'estensione del nome di file WMS.</span><span class="sxs-lookup"><span data-stu-id="f92a6-109">There can only be one skin definition file for a skin, and it has a .wms file name extension.</span></span>

<span data-ttu-id="f92a6-110">Le istruzioni nel file di definizione dell'interfaccia sono scritte in Extensible Markup Language (XML), che è simile a HTML.</span><span class="sxs-lookup"><span data-stu-id="f92a6-110">The instructions in the skin definition file are written in Extensible Markup Language (XML), which is similar to HTML.</span></span> <span data-ttu-id="f92a6-111">Se è stato usato HTML per creare pagine Web, si noterà che XML ha un aspetto familiare.</span><span class="sxs-lookup"><span data-stu-id="f92a6-111">If you have used HTML to create webpages, you will find that XML looks familiar.</span></span>

<span data-ttu-id="f92a6-112">Il codice XML nel file di definizione dell'interfaccia usa un set di tag di elemento speciali per definire le parti dell'interfaccia utente di skin.</span><span class="sxs-lookup"><span data-stu-id="f92a6-112">The XML in the skin definition file uses a set of special element tags to define parts of the skin user interface.</span></span> <span data-ttu-id="f92a6-113">Ad esempio, l'elemento [Button](button-element.md) definisce il comportamento di un pulsante, la posizione in cui verrà inserito e l'aspetto.</span><span class="sxs-lookup"><span data-stu-id="f92a6-113">For example, the [BUTTON](button-element.md) element defines how a button will behave, where it will go, and what it will look like.</span></span>

<span data-ttu-id="f92a6-114">Ogni tag di elemento ha attributi specifici.</span><span class="sxs-lookup"><span data-stu-id="f92a6-114">Each element tag has specific attributes.</span></span> <span data-ttu-id="f92a6-115">Ad esempio, l'elemento [Button](button-element.md) ha un attributo **Image** che definisce la posizione in cui è possibile trovare l'immagine per il pulsante.</span><span class="sxs-lookup"><span data-stu-id="f92a6-115">For example, the [BUTTON](button-element.md) element has an **image** attribute that defines where the picture for the button can be found.</span></span> <span data-ttu-id="f92a6-116">Questa operazione è simile a HTML, in cui l'elemento BODY avrà un attributo **bgcolor** che definisce il colore di sfondo della pagina HTML.</span><span class="sxs-lookup"><span data-stu-id="f92a6-116">This is similar to HTML, where the BODY element will have a **bgcolor** attribute that defines the background color of the HTML page.</span></span> <span data-ttu-id="f92a6-117">Informazioni dettagliate su tutti gli elementi Skin e sui relativi attributi sono incluse nella sezione riferimento per la [programmazione dell'interfaccia](skin-programming-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="f92a6-117">Detailed information about all skin elements and their attributes is included in the [Skin Programming Reference](skin-programming-reference.md) section.</span></span>

<span data-ttu-id="f92a6-118">XML include alcune semplici regole che è necessario tenere presente per creare le interfacce.</span><span class="sxs-lookup"><span data-stu-id="f92a6-118">XML has a few simple rules that you need to know to create skins.</span></span> <span data-ttu-id="f92a6-119">A differenza di HTML, XML richiede di seguire esattamente le regole.</span><span class="sxs-lookup"><span data-stu-id="f92a6-119">Unlike HTML, XML requires you to follow the rules exactly.</span></span>

## <a name="enclose-elements-with-angle-brackets"></a><span data-ttu-id="f92a6-120">Racchiudere gli elementi tra parentesi angolari</span><span class="sxs-lookup"><span data-stu-id="f92a6-120">Enclose Elements with Angle Brackets</span></span>

<span data-ttu-id="f92a6-121">Tutti gli elementi sono racchiusi tra parentesi angolari; ad esempio, l'elemento **Button** è tipizzato come segue:</span><span class="sxs-lookup"><span data-stu-id="f92a6-121">All elements are enclosed by angle brackets; for example, the **BUTTON** element is typed like this:</span></span>


```C++
<BUTTON>

```



<span data-ttu-id="f92a6-122">Non è necessario digitare la parola "BUTTON" in tutte le lettere maiuscole, ma la convenzione di digitare i nomi degli elementi in tutti i caratteri maiuscoli viene usata nel codice di esempio di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="f92a6-122">You do not need to type the word "BUTTON" in all uppercase letters, but the convention of typing element names in all uppercase is used in the example code of this SDK.</span></span>

## <a name="put-attributes-before-the-closing-bracket"></a><span data-ttu-id="f92a6-123">Inserire gli attributi prima della parentesi quadra di chiusura</span><span class="sxs-lookup"><span data-stu-id="f92a6-123">Put Attributes Before the Closing Bracket</span></span>

<span data-ttu-id="f92a6-124">Tutti gli attributi per un particolare elemento devono essere inclusi prima della parentesi angolare di chiusura.</span><span class="sxs-lookup"><span data-stu-id="f92a6-124">All attributes for a particular element must be included before the closing angle bracket.</span></span> <span data-ttu-id="f92a6-125">Un attributo è costituito dal nome dell'attributo seguito da un segno di uguale (=) e dal valore dell'attributo tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="f92a6-125">An attribute consists of the attribute name followed by an equal sign (=) and the value of the attribute in quotes.</span></span>


```C++
<BUTTON image="mypic.jpg">

```



<span data-ttu-id="f92a6-126">Non è necessario digitare la parola "image" in minuscolo, ma la convenzione di tipizzazione dei nomi degli attributi in minuscolo viene usata nel codice di esempio di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="f92a6-126">You do not need to type the word "image" in lowercase, but the convention of typing attribute names in lowercase is used in the example code of this SDK.</span></span> <span data-ttu-id="f92a6-127">Si noti inoltre che il valore dell'attributo è racchiuso tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="f92a6-127">Also note that the value of the attribute is enclosed in quotation marks.</span></span>

## <a name="opening-and-closing-elements"></a><span data-ttu-id="f92a6-128">Apertura e chiusura di elementi</span><span class="sxs-lookup"><span data-stu-id="f92a6-128">Opening and Closing Elements</span></span>

<span data-ttu-id="f92a6-129">Alcuni elementi vengono raggruppati all'interno di un altro elemento.</span><span class="sxs-lookup"><span data-stu-id="f92a6-129">Some elements are grouped together inside another element.</span></span> <span data-ttu-id="f92a6-130">Ad esempio, l'elemento **ButtonGroup** non ha molto senso, a meno che non si usino uno o più elementi **ButtonElement** .</span><span class="sxs-lookup"><span data-stu-id="f92a6-130">For example, the **BUTTONGROUP** element does not make a lot of sense unless you use one or more **BUTTONELEMENT** elements with it.</span></span> <span data-ttu-id="f92a6-131">Per chiarire il raggruppamento, è necessario disporre di un tag di apertura e di chiusura per ogni elemento.</span><span class="sxs-lookup"><span data-stu-id="f92a6-131">To make the grouping clear, you need to have an opening and closing tag for each element.</span></span> <span data-ttu-id="f92a6-132">Il tag di apertura è solo il nome dell'elemento e gli eventuali attributi correlati, racchiusi tra parentesi angolari.</span><span class="sxs-lookup"><span data-stu-id="f92a6-132">The opening tag is just the element name and any related attributes, surrounded by angle brackets.</span></span> <span data-ttu-id="f92a6-133">Il tag di chiusura è il nome dell'elemento, preceduto da una barra (/), quindi racchiuso tra parentesi angolari.</span><span class="sxs-lookup"><span data-stu-id="f92a6-133">The closing tag is the element name, preceded by a forward slash (/), and then enclosed by angle brackets.</span></span> <span data-ttu-id="f92a6-134">Ad esempio, il tag di apertura dell'elemento **ButtonGroup** è simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="f92a6-134">For example, the **BUTTONGROUP** element opening tag looks like this:</span></span>


```C++
<BUTTONGROUP>

```



<span data-ttu-id="f92a6-135">Il tag di chiusura **ButtonGroup** ha un aspetto simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="f92a6-135">The closing **BUTTONGROUP** tag looks like this:</span></span>


```C++
</BUTTONGROUP>

```



<span data-ttu-id="f92a6-136">Inserire i tag **ButtonElement** tra i tag dell'elemento **ButtonGroup** di apertura e di chiusura.</span><span class="sxs-lookup"><span data-stu-id="f92a6-136">You would put the **BUTTONELEMENT** tags between the opening and closing **BUTTONGROUP** element tags.</span></span> <span data-ttu-id="f92a6-137">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="f92a6-137">For example:</span></span>


```C++
<BUTTONGROUP>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



## <a name="closing-off-elements"></a><span data-ttu-id="f92a6-138">Chiusura di elementi</span><span class="sxs-lookup"><span data-stu-id="f92a6-138">Closing Off Elements</span></span>

<span data-ttu-id="f92a6-139">Se un elemento non contiene altri elementi, è necessario inserire una barra alla fine del nome dell'elemento immediatamente prima della parentesi angolare di chiusura.</span><span class="sxs-lookup"><span data-stu-id="f92a6-139">If an element has no other elements inside it, you must put a forward slash at the end of the element name just before the closing angle bracket.</span></span> <span data-ttu-id="f92a6-140">Nel codice precedente, ad esempio, ogni elemento **ButtonElement** ha una barra per indicare che non sono presenti altri elementi annidati al suo interno.</span><span class="sxs-lookup"><span data-stu-id="f92a6-140">For example, in the code above, each **BUTTONELEMENT** element has a forward slash to indicate that there are no other elements nested within it.</span></span>

<span data-ttu-id="f92a6-141">In altre parole, è necessario avere un tag di chiusura dell'elemento o chiudere l'elemento con una barra.</span><span class="sxs-lookup"><span data-stu-id="f92a6-141">In other words, you must either have a closing element tag or close off your element with a forward slash.</span></span>

<span data-ttu-id="f92a6-142">Questa operazione è corretta:</span><span class="sxs-lookup"><span data-stu-id="f92a6-142">This is correct:</span></span>


```C++
<BUTTONGROUP>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



<span data-ttu-id="f92a6-143">Questa operazione non è corretta:</span><span class="sxs-lookup"><span data-stu-id="f92a6-143">This is not correct:</span></span>


```C++
<BUTTONGROUP/>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



<span data-ttu-id="f92a6-144">Anche questo non è corretto:</span><span class="sxs-lookup"><span data-stu-id="f92a6-144">This is also not correct:</span></span>


```C++
<BUTTONGROUP>
    <BUTTONELEMENT>
    <BUTTONELEMENT>
</BUTTONGROUP>

```



<span data-ttu-id="f92a6-145">Nella sezione seguente vengono fornite ulteriori informazioni sui file di definizione dell'interfaccia:</span><span class="sxs-lookup"><span data-stu-id="f92a6-145">The following section provides more information about skin definition files:</span></span>

-   [<span data-ttu-id="f92a6-146">Struttura del file di definizione dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="f92a6-146">Skin Definition File Structure</span></span>](skin-definition-file-structure.md)

## <a name="related-topics"></a><span data-ttu-id="f92a6-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f92a6-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f92a6-148">**File di interfaccia**</span><span class="sxs-lookup"><span data-stu-id="f92a6-148">**Skin Files**</span></span>](skin-files.md)
</dt> </dl>

 

 





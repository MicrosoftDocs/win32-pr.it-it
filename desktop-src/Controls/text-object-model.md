---
title: Modello a oggetti testo
description: Questa sezione contiene informazioni sugli elementi di programmazione usati con il modello a oggetti di testo (TOM).
ms.assetid: vs|controls|~\controls\richedit\textobjectmodel.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7625ca7772da7f4e10aa7d64159971ee0e259d2a
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2020
ms.locfileid: "103873061"
---
# <a name="text-object-model"></a><span data-ttu-id="910a4-103">Modello a oggetti testo</span><span class="sxs-lookup"><span data-stu-id="910a4-103">Text Object Model</span></span>

<span data-ttu-id="910a4-104">Questa sezione contiene informazioni sugli elementi di programmazione usati con il modello a oggetti di testo (TOM).</span><span class="sxs-lookup"><span data-stu-id="910a4-104">This section contains information about the programming elements used with the Text Object Model (TOM).</span></span>

<span data-ttu-id="910a4-105">Il TOM definisce un set sostanziale di interfacce di manipolazione del testo.</span><span class="sxs-lookup"><span data-stu-id="910a4-105">The TOM defines a substantial set of text manipulation interfaces.</span></span> <span data-ttu-id="910a4-106">Le soluzioni di testo, ad esempio Microsoft Word e i controlli Rich Edit supportano il set di funzionalità di TOM.</span><span class="sxs-lookup"><span data-stu-id="910a4-106">Text solutions such as Microsoft Word and rich edit controls support the TOM feature set.</span></span> <span data-ttu-id="910a4-107">TOM è stato fortemente influenzato da WordBasic (il linguaggio di programmazione usato per Word) ed è facile da usare da Microsoft Visual Basic, Applications Edition (VBA).</span><span class="sxs-lookup"><span data-stu-id="910a4-107">TOM was greatly influenced by WordBasic (the programming language used for Word) and it is easy to use from Microsoft Visual Basic for Applications (VBA).</span></span> <span data-ttu-id="910a4-108">Questa compatibilità presenta diversi vantaggi:</span><span class="sxs-lookup"><span data-stu-id="910a4-108">This compatibility has several advantages:</span></span>

-   <span data-ttu-id="910a4-109">Il codice può essere migrato abbastanza facilmente da una soluzione a un'altra.</span><span class="sxs-lookup"><span data-stu-id="910a4-109">Code can migrate fairly easily from one solution to another.</span></span>
-   <span data-ttu-id="910a4-110">Una lingua può essere usata per condividere le informazioni di testo tra diversi motori di testo.</span><span class="sxs-lookup"><span data-stu-id="910a4-110">One language can be used to share text information between different text engines.</span></span>
-   <span data-ttu-id="910a4-111">Riduce la necessità di documentazione e codice rispetto alle interfacce COM (Component Object Model di basso livello) e VBA separate.</span><span class="sxs-lookup"><span data-stu-id="910a4-111">It reduces the need for documentation and code compared to the separate low-level Component Object Model (COM) and VBA interfaces.</span></span>

<span data-ttu-id="910a4-112">Tuttavia, può essere meno efficiente per gli scopi C/C++ rispetto all'uso di interfacce COM più generali di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="910a4-112">However, it can be less efficient for C/C++ purposes than the use of more general lower level COM interfaces.</span></span>

<span data-ttu-id="910a4-113">TOM è un set semplice di interfacce da implementare per le soluzioni di testo principale, i controlli Word e Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="910a4-113">TOM is a straightforward set of interfaces to implement for its primary text solutions, Word and rich edit controls.</span></span> <span data-ttu-id="910a4-114">Tuttavia, per le applicazioni che inseriscono un'enfasi secondaria sul testo, è preferibile fornire le interfacce TOM trasferendo il testo in un controllo di modifica che supporta TOM.</span><span class="sxs-lookup"><span data-stu-id="910a4-114">However, for applications that place minor emphasis on text, it is better to provide TOM interfaces by transferring the text to an edit control that supports TOM.</span></span> <span data-ttu-id="910a4-115">Poiché i controlli Rich Edit vengono forniti con i sistemi operativi Microsoft, sono i metodi standard per ottenere la funzionalità TOM.</span><span class="sxs-lookup"><span data-stu-id="910a4-115">Since rich edit controls ship with Microsoft operating systems, they are the standard means of obtaining TOM functionality.</span></span>

### <a name="overviews"></a><span data-ttu-id="910a4-116">Cenni preliminari</span><span class="sxs-lookup"><span data-stu-id="910a4-116">Overviews</span></span>



| <span data-ttu-id="910a4-117">Argomento</span><span class="sxs-lookup"><span data-stu-id="910a4-117">Topic</span></span>                                                          | <span data-ttu-id="910a4-118">Contenuto</span><span class="sxs-lookup"><span data-stu-id="910a4-118">Contents</span></span>                                                                                                                                                                                                         |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="910a4-119">Informazioni sul modello a oggetti di testo</span><span class="sxs-lookup"><span data-stu-id="910a4-119">About Text Object Model</span></span>](about-text-object-model.md)         | <span data-ttu-id="910a4-120">L'oggetto TOM (Text Object Model) di primo livello è definito dall'interfaccia [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) , che dispone di metodi per la creazione e il recupero di oggetti di livello inferiore nella gerarchia di oggetti.</span><span class="sxs-lookup"><span data-stu-id="910a4-120">The top-level Text Object Model (TOM) object is defined by the [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) interface, which has methods for creating and retrieving objects lower in the object hierarchy.</span></span><br/> |
| [<span data-ttu-id="910a4-121">Uso del modello a oggetti di testo</span><span class="sxs-lookup"><span data-stu-id="910a4-121">Using The Text Object Model</span></span>](using-the-text-object-model.md) | <span data-ttu-id="910a4-122">Negli esempi di codice di questo documento vengono illustrati i vari aspetti dell'utilizzo del modello a oggetti di testo (TOM).</span><span class="sxs-lookup"><span data-stu-id="910a4-122">The code samples in this document show various aspects of using the Text Object Model (TOM).</span></span><br/>                                                                                                          |



 

### <a name="interfaces"></a><span data-ttu-id="910a4-123">Interfacce</span><span class="sxs-lookup"><span data-stu-id="910a4-123">Interfaces</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="910a4-124">Argomento</span><span class="sxs-lookup"><span data-stu-id="910a4-124">Topic</span></span></th>
<th><span data-ttu-id="910a4-125">Contenuto</span><span class="sxs-lookup"><span data-stu-id="910a4-125">Contents</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="910a4-126"><a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a></span><span class="sxs-lookup"><span data-stu-id="910a4-126"><a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a></span></span></td>
<td><span data-ttu-id="910a4-127">L'interfaccia <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> è l'interfaccia di primo livello di Tom, che recupera gli oggetti selezione e intervallo attivi per qualsiasi storia del documento, indipendentemente dal fatto che sia attiva o meno.</span><span class="sxs-lookup"><span data-stu-id="910a4-127">The <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> interface is the TOM top-level interface, which retrieves the active selection and range objects for any story in the document whether active or not.</span></span> <span data-ttu-id="910a4-128">Consente all'applicazione di:</span><span class="sxs-lookup"><span data-stu-id="910a4-128">It enables the application to:</span></span>
<ul>
<li><span data-ttu-id="910a4-129">Aprire e salvare i documenti.</span><span class="sxs-lookup"><span data-stu-id="910a4-129">Open and save documents.</span></span></li>
<li><span data-ttu-id="910a4-130">Controllare il comportamento di annullamento e l'aggiornamento dello schermo.</span><span class="sxs-lookup"><span data-stu-id="910a4-130">Control undo behavior and screen updating.</span></span></li>
<li><span data-ttu-id="910a4-131">Trovare un intervallo da una posizione dello schermo.</span><span class="sxs-lookup"><span data-stu-id="910a4-131">Find a range from a screen position.</span></span></li>
<li><span data-ttu-id="910a4-132">Ottiene un enumeratore di <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> Story.</span><span class="sxs-lookup"><span data-stu-id="910a4-132">Get an <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> story enumerator.</span></span></li>
</ul>
<br/> <span data-ttu-id="910a4-133"><strong>Quando implementare</strong></span><span class="sxs-lookup"><span data-stu-id="910a4-133"><strong>When to Implement</strong></span></span><br/> <span data-ttu-id="910a4-134">Le applicazioni in genere non implementano l'interfaccia <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="910a4-134">Applications typically do not implement the <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> interface.</span></span> <span data-ttu-id="910a4-135">Le soluzioni Microsoft Text, ad esempio i controlli Rich Edit, implementano <strong>ITextDocument</strong> come parte dell'implementazione di Tom.</span><span class="sxs-lookup"><span data-stu-id="910a4-135">Microsoft text solutions, such as rich edit controls, implement <strong>ITextDocument</strong> as part of their TOM implementation.</span></span> <br/> <span data-ttu-id="910a4-136"><strong>Quando usare</strong></span><span class="sxs-lookup"><span data-stu-id="910a4-136"><strong>When to Use</strong></span></span><br/> <span data-ttu-id="910a4-137">Le applicazioni possono recuperare un puntatore <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> da un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="910a4-137">Applications can retrieve an <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a> pointer from a rich edit control.</span></span> <span data-ttu-id="910a4-138">A tale scopo, inviare un messaggio di <a href="em-getoleinterface.md"><strong>EM_GETOLEINTERFACE</strong></a> per recuperare un oggetto <a href="/windows/desktop/api/Richole/nn-richole-iricheditole"><strong>IRichEditOle</strong></a> da un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="910a4-138">To do this, send an <a href="em-getoleinterface.md"><strong>EM_GETOLEINTERFACE</strong></a> message to retrieve an <a href="/windows/desktop/api/Richole/nn-richole-iricheditole"><strong>IRichEditOle</strong></a> object from a rich edit control.</span></span> <span data-ttu-id="910a4-139">Chiamare quindi il metodo <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>IUnknown:: QueryInterface</strong></a> dell'oggetto per recuperare un puntatore <strong>ITextDocument</strong> .</span><span class="sxs-lookup"><span data-stu-id="910a4-139">Then, call the object's <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>IUnknown::QueryInterface</strong></a> method to retrieve an <strong>ITextDocument</strong> pointer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="910a4-140"><a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a></span><span class="sxs-lookup"><span data-stu-id="910a4-140"><a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a></span></span></td>
<td><span data-ttu-id="910a4-141">È possibile accedere agli attributi di intervallo RTF di TOM con una coppia di interfacce duali, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> e <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="910a4-141">TOM rich text-range attributes are accessed through a pair of dual interfaces, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> and <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="910a4-142"><a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a></span><span class="sxs-lookup"><span data-stu-id="910a4-142"><a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a></span></span></td>
<td><span data-ttu-id="910a4-143">È possibile accedere agli attributi di intervallo RTF di TOM con una coppia di interfacce duali, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> e <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="910a4-143">TOM rich text-range attributes are accessed through a pair of dual interfaces, <a href="/windows/desktop/api/Tom/nn-tom-itextfont"><strong>ITextFont</strong></a> and <a href="/windows/desktop/api/Tom/nn-tom-itextpara"><strong>ITextPara</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="910a4-144"><a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a></span><span class="sxs-lookup"><span data-stu-id="910a4-144"><a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a></span></span></td>
<td><span data-ttu-id="910a4-145">Gli oggetti <a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a> sono strumenti avanzati per la modifica e il data binding che consentono a un programma di selezionare il testo in una storia, quindi di esaminare o modificare il testo.</span><span class="sxs-lookup"><span data-stu-id="910a4-145">The <a href="/windows/desktop/api/Tom/nn-tom-itextrange"><strong>ITextRange</strong></a> objects are powerful editing and data-binding tools that allow a program to select text in a story and then examine or change that text.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="910a4-146"><a href="/windows/desktop/api/Tom/nn-tom-itextselection"><strong>ITextSelection</strong></a></span><span class="sxs-lookup"><span data-stu-id="910a4-146"><a href="/windows/desktop/api/Tom/nn-tom-itextselection"><strong>ITextSelection</strong></a></span></span></td>
<td><span data-ttu-id="910a4-147">Una selezione di testo è un intervallo di testo con evidenziazione della selezione.</span><span class="sxs-lookup"><span data-stu-id="910a4-147">A text selection is a text range with selection highlighting.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="910a4-148"><a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a></span><span class="sxs-lookup"><span data-stu-id="910a4-148"><a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a></span></span></td>
<td><span data-ttu-id="910a4-149">Lo scopo dell'interfaccia <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> è enumerare le storie in un <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="910a4-149">The purpose of the <a href="/windows/desktop/api/Tom/nn-tom-itextstoryranges"><strong>ITextStoryRanges</strong></a> interface is to enumerate the stories in an <a href="/windows/desktop/api/Tom/nn-tom-itextdocument"><strong>ITextDocument</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 


---
title: Riferimento al modello a oggetti la
description: In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.
ms.assetid: 68a84c68-3aac-4971-9611-45f52e057708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 889c977260548c26bbfd8196160e4537ccb8895d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047267"
---
# <a name="vml-object-model-reference"></a><span data-ttu-id="2473c-104">Riferimento al modello a oggetti la</span><span class="sxs-lookup"><span data-stu-id="2473c-104">VML Object Model Reference</span></span>

<span data-ttu-id="2473c-105">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="2473c-105">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2473c-106">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="2473c-106">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2473c-107">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="2473c-107">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2473c-108">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="2473c-108">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2473c-109">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="2473c-109">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2473c-110">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="2473c-110">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2473c-111">In questo argomento</span><span class="sxs-lookup"><span data-stu-id="2473c-111">In this topic:</span></span>

-   [<span data-ttu-id="2473c-112">Introduzione</span><span class="sxs-lookup"><span data-stu-id="2473c-112">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="2473c-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="2473c-113">Example</span></span>](#example)
-   [<span data-ttu-id="2473c-114">Configurazione di la</span><span class="sxs-lookup"><span data-stu-id="2473c-114">Setting up VML</span></span>](#setting-up-vml)
-   [<span data-ttu-id="2473c-115">Riferimento a la OM</span><span class="sxs-lookup"><span data-stu-id="2473c-115">VML OM Reference</span></span>](#vml-om-reference)
    -   [<span data-ttu-id="2473c-116">Shape-elemento</span><span class="sxs-lookup"><span data-stu-id="2473c-116">Shape element</span></span>](#shape-element)
-   [<span data-ttu-id="2473c-117">Sottoelementi dell'elemento Shape</span><span class="sxs-lookup"><span data-stu-id="2473c-117">Subelements of the Shape Element</span></span>](#subelements-of-the-shape-element)
    -   [<span data-ttu-id="2473c-118">Elemento background</span><span class="sxs-lookup"><span data-stu-id="2473c-118">Background element</span></span>](#background-element)
    -   [<span data-ttu-id="2473c-119">Elemento Extrusion</span><span class="sxs-lookup"><span data-stu-id="2473c-119">Extrusion element</span></span>](#extrusion-element)
    -   [<span data-ttu-id="2473c-120">Fill (elemento)</span><span class="sxs-lookup"><span data-stu-id="2473c-120">Fill element</span></span>](#fill-element)
    -   [<span data-ttu-id="2473c-121">Group - elemento</span><span class="sxs-lookup"><span data-stu-id="2473c-121">Group element</span></span>](#group-element)
    -   [<span data-ttu-id="2473c-122">Elemento ImageData</span><span class="sxs-lookup"><span data-stu-id="2473c-122">Imagedata element</span></span>](#imagedata-element)
    -   [<span data-ttu-id="2473c-123">Path-elemento</span><span class="sxs-lookup"><span data-stu-id="2473c-123">Path element</span></span>](#path-element)
    -   [<span data-ttu-id="2473c-124">Elemento Shadow</span><span class="sxs-lookup"><span data-stu-id="2473c-124">Shadow element</span></span>](#shadow-element)
    -   [<span data-ttu-id="2473c-125">Elemento asimmetria</span><span class="sxs-lookup"><span data-stu-id="2473c-125">Skew element</span></span>](#skew-element)
    -   [<span data-ttu-id="2473c-126">Stroke-elemento</span><span class="sxs-lookup"><span data-stu-id="2473c-126">Stroke element</span></span>](#stroke-element)
    -   [<span data-ttu-id="2473c-127">Elemento TextPath</span><span class="sxs-lookup"><span data-stu-id="2473c-127">TextPath element</span></span>](#textpath-element)
-   [<span data-ttu-id="2473c-128">Tipi di dati utilizzati nel modello a oggetti la</span><span class="sxs-lookup"><span data-stu-id="2473c-128">Data Types Used in the VML Object Model</span></span>](#data-types-used-in-the-vml-object-model)

## <a name="introduction"></a><span data-ttu-id="2473c-129">Introduzione</span><span class="sxs-lookup"><span data-stu-id="2473c-129">Introduction</span></span>

<span data-ttu-id="2473c-130">[Vector Markup Language (la)](https://www.w3.org/TR/NOTE-datetime.html) è un linguaggio basato su testo che usa [XML](https://www.w3.org/TR/REC-xml.mdl) per estendere il codice HTML allo scopo di visualizzare le informazioni grafiche vettoriali.</span><span class="sxs-lookup"><span data-stu-id="2473c-130">[Vector Markup Language (VML)](https://www.w3.org/TR/NOTE-datetime.html) is a text-based language that uses [XML](https://www.w3.org/TR/REC-xml.mdl) to extend HTML for the purpose of displaying vector graphic information.</span></span> <span data-ttu-id="2473c-131">Il Document Object Model la (DOM) definisce un'interfaccia a livello di codice per la manipolazione degli elementi del documento.</span><span class="sxs-lookup"><span data-stu-id="2473c-131">The VML Document Object Model (DOM) defines a programmatic interface for the manipulation of the document elements.</span></span> <span data-ttu-id="2473c-132">Ciò consente all'utente di creare e modificare dinamicamente la grafica vettoriale tramite un'interfaccia indipendente dalla piattaforma e dal linguaggio.</span><span class="sxs-lookup"><span data-stu-id="2473c-132">This enables the user to dynamically create and modify vector graphics through a platform- and language-neutral interface.</span></span> <span data-ttu-id="2473c-133">Il DOM la è conforme alla specifica [Document Object Model](https://www.w3.org/TR/REC-DOM-Level-1/) .</span><span class="sxs-lookup"><span data-stu-id="2473c-133">The VML DOM conforms to the [Document Object Model](https://www.w3.org/TR/REC-DOM-Level-1/) specification.</span></span>

<span data-ttu-id="2473c-134">LA usa l'elemento [Shape](#shape-element) come blocco predefinito di base per le immagini grafiche vettoriali.</span><span class="sxs-lookup"><span data-stu-id="2473c-134">VML uses the [Shape](#shape-element) element as the basic building block for vector graphic images.</span></span> <span data-ttu-id="2473c-135">Una volta creata una forma, è possibile modificare la forma tramite gli attributi o i sottoelementi collegati.</span><span class="sxs-lookup"><span data-stu-id="2473c-135">Once a shape is created, you can modify the shape through attributes or by attached subelements.</span></span> <span data-ttu-id="2473c-136">Per modificare, ad esempio, il colore di una forma, assegnare un valore di colore all'attributo **FillColor** .</span><span class="sxs-lookup"><span data-stu-id="2473c-136">For example, to change the color of a shape, assign a color value to the **FillColor** attribute.</span></span>


```HTML
myshape.fillcolor = "red"
```



<span data-ttu-id="2473c-137">Molti degli attributi di una forma sono anche [sottoelementi](/windows) e hanno attributi propri, inclusi i seguenti:</span><span class="sxs-lookup"><span data-stu-id="2473c-137">Several of the attributes of a shape are also [subelements](/windows) and have their own attributes, including the following:</span></span>

-   [<span data-ttu-id="2473c-138">Background</span><span class="sxs-lookup"><span data-stu-id="2473c-138">Background</span></span>](#background-element)
-   [<span data-ttu-id="2473c-139">Estrusione</span><span class="sxs-lookup"><span data-stu-id="2473c-139">Extrusion</span></span>](#extrusion-element)
-   [<span data-ttu-id="2473c-140">Fill</span><span class="sxs-lookup"><span data-stu-id="2473c-140">Fill</span></span>](#fill-element)
-   [<span data-ttu-id="2473c-141">Gruppo</span><span class="sxs-lookup"><span data-stu-id="2473c-141">Group</span></span>](#group-element)
-   [<span data-ttu-id="2473c-142">ImageData</span><span class="sxs-lookup"><span data-stu-id="2473c-142">Imagedata</span></span>](#imagedata-element)
-   [<span data-ttu-id="2473c-143">Percorso</span><span class="sxs-lookup"><span data-stu-id="2473c-143">Path</span></span>](#path-element)
-   [<span data-ttu-id="2473c-144">Shadow</span><span class="sxs-lookup"><span data-stu-id="2473c-144">Shadow</span></span>](#shadow-element)
-   [<span data-ttu-id="2473c-145">Sfasamento</span><span class="sxs-lookup"><span data-stu-id="2473c-145">Skew</span></span>](#skew-element)
-   [<span data-ttu-id="2473c-146">Stroke</span><span class="sxs-lookup"><span data-stu-id="2473c-146">Stroke</span></span>](#stroke-element)
-   [<span data-ttu-id="2473c-147">TextPath</span><span class="sxs-lookup"><span data-stu-id="2473c-147">TextPath</span></span>](#textpath-element)

<span data-ttu-id="2473c-148">LA OM usa diversi [tipi di dati](/windows) per definire i parametri.</span><span class="sxs-lookup"><span data-stu-id="2473c-148">The VML OM uses several [data types](/windows) to define parameters.</span></span> <span data-ttu-id="2473c-149">I tipi di DataType con prefisso "VG" sono enumerazioni e quelli con prefisso "IVg" sono oggetti.</span><span class="sxs-lookup"><span data-stu-id="2473c-149">Datatypes prefixed with "Vg" are enumerations and those prefixed with "IVg" are objects.</span></span> <span data-ttu-id="2473c-150">Per un elenco, fare clic qui.</span><span class="sxs-lookup"><span data-stu-id="2473c-150">Click here for a list.</span></span> <span data-ttu-id="2473c-151">I tipi di Data Type secondari sono elencati con parametri specifici.</span><span class="sxs-lookup"><span data-stu-id="2473c-151">Minor datatypes are listed with specific parameters.</span></span>

## <a name="example"></a><span data-ttu-id="2473c-152">Esempio</span><span class="sxs-lookup"><span data-stu-id="2473c-152">Example</span></span>

<span data-ttu-id="2473c-153">Nel codice VBScript seguente viene illustrato come creare una forma semplice:</span><span class="sxs-lookup"><span data-stu-id="2473c-153">The following VBScript code shows how to create a simple shape:</span></span>


```HTML
        Set MyRect = Document.CreateElement("v:Rect")
        Set R = MyDiv.AppendChild(MyRect)
        R.Style.Position = "absolute"
        R.Style.Width = 20
        R.Style.Height = 20
        R.Style.Top = 50
        R.Style.Left = 50
        R.FillColor = "red"
```



<span data-ttu-id="2473c-154">Nell'esempio precedente viene creata una forma usando il Document Object Model metodo **CreateElement**.</span><span class="sxs-lookup"><span data-stu-id="2473c-154">In the above example, a shape is created by using the Document Object Model method **CreateElement**.</span></span> <span data-ttu-id="2473c-155">La forma è una forma Rect predefinita di la.</span><span class="sxs-lookup"><span data-stu-id="2473c-155">The shape is a VML predefined Rect shape.</span></span> <span data-ttu-id="2473c-156">Anche se l'oggetto esiste, non può far parte del documento finché non viene collegato al documento.</span><span class="sxs-lookup"><span data-stu-id="2473c-156">Even though the object exists, it cannot be part of the document until it is attached to the document.</span></span> <span data-ttu-id="2473c-157">Utilizzando il metodo **AppendChild** , il Rect viene trasformato come figlio di un elemento **div** denominato MyDiv.</span><span class="sxs-lookup"><span data-stu-id="2473c-157">Using the **AppendChild** method, the Rect is made a child of a **DIV** element called MyDiv.</span></span> <span data-ttu-id="2473c-158">Alcuni attributi di stile minimo (**posizione**, **larghezza**, **altezza**, **superiore**, **sinistra**) sono impostati in modo da assegnare alla forma una dimensione specifica.</span><span class="sxs-lookup"><span data-stu-id="2473c-158">A few minimum style attributes (**Position**, **Width**, **Height**, **Top**, **Left**) are set to give the shape a specific size.</span></span> <span data-ttu-id="2473c-159">Infine, viene assegnato un colore con l'attributo **FillColor** .</span><span class="sxs-lookup"><span data-stu-id="2473c-159">Finally, a color is assigned with the **FillColor** attribute.</span></span> <span data-ttu-id="2473c-160">Si noti che è possibile usare qualsiasi linguaggio di scripting o qualsiasi linguaggio in grado di funzionare con Document Object Model interfacce.</span><span class="sxs-lookup"><span data-stu-id="2473c-160">Note that any scripting language or any language that can work with Document Object Model interfaces can be used.</span></span>

## <a name="setting-up-vml"></a><span data-ttu-id="2473c-161">Configurazione di la</span><span class="sxs-lookup"><span data-stu-id="2473c-161">Setting up VML</span></span>

<span data-ttu-id="2473c-162">Un'implementazione di la è tramite Microsoft Internet Explorer 5,0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="2473c-162">One implementation of VML is through Microsoft Internet Explorer 5.0 or greater.</span></span> <span data-ttu-id="2473c-163">Per configurare correttamente l'oggetto rendering in una pagina Web, è necessario effettuare le aggiunte seguenti:</span><span class="sxs-lookup"><span data-stu-id="2473c-163">To set up the rendering object correctly in a Web page, the following additions must be made:</span></span>

1.  <span data-ttu-id="2473c-164">È necessario configurare lo schema nella finestra iniziale</span><span class="sxs-lookup"><span data-stu-id="2473c-164">The schema must be set up in the initial</span></span> <HTML> <span data-ttu-id="2473c-165">Tag come segue:</span><span class="sxs-lookup"><span data-stu-id="2473c-165">tag as follows:</span></span>
    ```HTML
    <HTML xmlns:v="urn:schemas-microsoft-com:vml">
    ```

    

2.  <span data-ttu-id="2473c-166">Il comportamento di rendering deve far parte dello stile del documento:</span><span class="sxs-lookup"><span data-stu-id="2473c-166">The rendering behavior must be part of the document's style:</span></span>
    ```HTML
    <STYLE>
    v\:* { behavior: url(#default#VML); display:inline-block}
    </STYLE>
    ```

    

<span data-ttu-id="2473c-167">Di seguito viene illustrata una pagina Web HTML di esempio configurata correttamente per la che mostra la creazione dinamica di una forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-167">The following shows a sample HTML Web page set up correctly for VML showing the dynamic creation of a shape.</span></span>


```HTML
<HTML xmlns:v="urn:schemas-microsoft-com:vml">
<HEAD>
<STYLE>
v\:* { behavior: url(#default#VML); display:inline-block}
</STYLE>
<TITLE>VML Sample</TITLE>
</HEAD>
<BODY>
<DIV id="MyDiv"></DIV>
<SCRIPT ID="MYSCRIPT" LANGUAGE="VBScript">
<!--
Set MyRect = Document.CreateElement("v:Rect")
Set R = MyDiv.AppendChild(MyRect)
R.Style.Position = "absolute"
R.Style.Width = 20
R.Style.Height = 20
R.Style.Top = 50
R.Style.Left = 50
R.FillColor = "red"
-->
</SCRIPT>
</BODY>
</HTML>
```



<span data-ttu-id="2473c-168">Si noti che nelle versioni beta, era necessario un tag Object ActiveX e uno stile di comportamento diverso.</span><span class="sxs-lookup"><span data-stu-id="2473c-168">Note that in beta versions, an ActiveX object tag and a different behavior style was required.</span></span>

## <a name="vml-om-reference"></a><span data-ttu-id="2473c-169">Riferimento a la OM</span><span class="sxs-lookup"><span data-stu-id="2473c-169">VML OM Reference</span></span>

<span data-ttu-id="2473c-170">Questo riferimento definisce l'elemento della [forma](#shape-element) , i [sottoelementi](/windows)e i [tipi di dati](/windows) utilizzati dal modello a oggetti di la.</span><span class="sxs-lookup"><span data-stu-id="2473c-170">This reference defines the [Shape](#shape-element) element, [subelements](/windows), and [data types](/windows) that are used by the object model of VML.</span></span>

### <a name="shape-element"></a><span data-ttu-id="2473c-171">Shape-elemento</span><span class="sxs-lookup"><span data-stu-id="2473c-171">Shape element</span></span>

<span data-ttu-id="2473c-172">Le forme sono i blocchi predefiniti delle immagini grafiche definite da Vector Markup Language (la).</span><span class="sxs-lookup"><span data-stu-id="2473c-172">Shapes are the building blocks of graphical images defined by Vector Markup Language (VML).</span></span> <span data-ttu-id="2473c-173">La forma è l'elemento di primo livello e diversi sottoelementi consentono di definire la natura di ogni forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-173">The shape is the top-level element and several subelements help define the nature of each shape.</span></span>

<span data-ttu-id="2473c-174">LA fornisce forme predefinite:</span><span class="sxs-lookup"><span data-stu-id="2473c-174">VML provides predefined shapes:</span></span>

<span data-ttu-id="2473c-175">**Attributi di forma**</span><span class="sxs-lookup"><span data-stu-id="2473c-175">**Shape Attributes**</span></span>

-   <span data-ttu-id="2473c-176">**Arc**</span><span class="sxs-lookup"><span data-stu-id="2473c-176">**Arc**</span></span>
-   <span data-ttu-id="2473c-177">**Curva**</span><span class="sxs-lookup"><span data-stu-id="2473c-177">**Curve**</span></span>
-   <span data-ttu-id="2473c-178">**Linea**</span><span class="sxs-lookup"><span data-stu-id="2473c-178">**Line**</span></span>
-   <span data-ttu-id="2473c-179">**Polilinea**</span><span class="sxs-lookup"><span data-stu-id="2473c-179">**PolyLine**</span></span>
-   <span data-ttu-id="2473c-180">**Rect**</span><span class="sxs-lookup"><span data-stu-id="2473c-180">**Rect**</span></span>
-   <span data-ttu-id="2473c-181">**RoundRect**</span><span class="sxs-lookup"><span data-stu-id="2473c-181">**RoundRect**</span></span>



|              |                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2473c-182">ADJ</span><span class="sxs-lookup"><span data-stu-id="2473c-182">Adj</span></span>          | <span data-ttu-id="2473c-183">[IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-183">[IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md).</span></span> <span data-ttu-id="2473c-184">Elenco delimitato da virgole di numeri che rappresentano i parametri per le formule della guida che definiscono il percorso della forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-184">A comma-delimited list of numbers that are the parameters for the guide formulas that define the path of the shape.</span></span> <span data-ttu-id="2473c-185">È possibile omettere i valori per consentire l'utilizzo delle impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="2473c-185">Values may be omitted to allow for using defaults.</span></span> <span data-ttu-id="2473c-186">Possono essere presenti fino a 8 valori di regolazione.</span><span class="sxs-lookup"><span data-stu-id="2473c-186">There can be up to 8 adjustment values.</span></span>                                                                                                   |
| <span data-ttu-id="2473c-187">ALT</span><span class="sxs-lookup"><span data-stu-id="2473c-187">Alt</span></span>          | <span data-ttu-id="2473c-188">Stringa.</span><span class="sxs-lookup"><span data-stu-id="2473c-188">String.</span></span> <span data-ttu-id="2473c-189">Testo alternativo associato alla forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-189">Alternative text associated with shape.</span></span> <span data-ttu-id="2473c-190">Usato per l'esplorazione non grafica.</span><span class="sxs-lookup"><span data-stu-id="2473c-190">Used for non-graphical browsing.</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="2473c-191">Pulsante</span><span class="sxs-lookup"><span data-stu-id="2473c-191">Button</span></span>       | <span data-ttu-id="2473c-192">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-192">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="2473c-193">Visualizza il comportamento del pulsante sul clic.</span><span class="sxs-lookup"><span data-stu-id="2473c-193">Displays button behavior on click.</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="2473c-194">BWMode</span><span class="sxs-lookup"><span data-stu-id="2473c-194">BWMode</span></span>       | <span data-ttu-id="2473c-195">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-195">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="2473c-196">Determina la modalità di rendering della forma nella visualizzazione in bianco e nero nelle app o quando viene stampata su stampanti nere e bianche.</span><span class="sxs-lookup"><span data-stu-id="2473c-196">Determines how shape will render in black-and-white view in apps or when printed to black-and-white printers.</span></span> <span data-ttu-id="2473c-197">I valori includono: **color**, **auto**, **gradazioni di grigio**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **undisegnato**.</span><span class="sxs-lookup"><span data-stu-id="2473c-197">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="2473c-198">Impostazione predefinita: **auto**.</span><span class="sxs-lookup"><span data-stu-id="2473c-198">Default: **Auto**.</span></span> |
| <span data-ttu-id="2473c-199">BWNormal</span><span class="sxs-lookup"><span data-stu-id="2473c-199">BWNormal</span></span>     | <span data-ttu-id="2473c-200">VgBlackWhiteMode.</span><span class="sxs-lookup"><span data-stu-id="2473c-200">VgBlackWhiteMode.</span></span> <span data-ttu-id="2473c-201">Quando BWMode è auto, viene consultata questa proprietà per il rendering della forma in bianco e nero normale.</span><span class="sxs-lookup"><span data-stu-id="2473c-201">When BWMode is Auto, this property is consulted for how to render the shape in normal black and white.</span></span> <span data-ttu-id="2473c-202">I valori includono: **color**, **auto**, **gradazioni di grigio**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **undisegnato**.</span><span class="sxs-lookup"><span data-stu-id="2473c-202">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="2473c-203">Impostazione predefinita: **auto**.</span><span class="sxs-lookup"><span data-stu-id="2473c-203">Default: **Auto**.</span></span>                                                |
| <span data-ttu-id="2473c-204">BWPure</span><span class="sxs-lookup"><span data-stu-id="2473c-204">BWPure</span></span>       | <span data-ttu-id="2473c-205">VgBlackWhiteMode.</span><span class="sxs-lookup"><span data-stu-id="2473c-205">VgBlackWhiteMode.</span></span> <span data-ttu-id="2473c-206">Quando BWMode è auto, viene consultata questa proprietà per il rendering della forma in B/W pure.</span><span class="sxs-lookup"><span data-stu-id="2473c-206">When BWMode is Auto, this property is consulted for how to render the shape in pure B/W.</span></span> <span data-ttu-id="2473c-207">I valori includono: **color**, **auto**, **gradazioni di grigio**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **undisegnato**.</span><span class="sxs-lookup"><span data-stu-id="2473c-207">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="2473c-208">Impostazione predefinita: **auto**.</span><span class="sxs-lookup"><span data-stu-id="2473c-208">Default: **Auto**.</span></span>                                                              |
| <span data-ttu-id="2473c-209">ChildShapes</span><span class="sxs-lookup"><span data-stu-id="2473c-209">ChildShapes</span></span>  | <span data-ttu-id="2473c-210">IVgGroupShapes.</span><span class="sxs-lookup"><span data-stu-id="2473c-210">IVgGroupShapes.</span></span> <span data-ttu-id="2473c-211">Raccolta di altre forme in questo gruppo.</span><span class="sxs-lookup"><span data-stu-id="2473c-211">A collection of other shapes in this group.</span></span> <span data-ttu-id="2473c-212">Questa raccolta supporta i metodi di lunghezza ed elemento standard.</span><span class="sxs-lookup"><span data-stu-id="2473c-212">This collection supports the standard Length and Item methods.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="2473c-213">Chromakey</span><span class="sxs-lookup"><span data-stu-id="2473c-213">Chromakey</span></span>    | <span data-ttu-id="2473c-214">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-214">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="2473c-215">Valore di colore che sarà trasparente e visualizzerà qualsiasi elemento sottostante la forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-215">A color value that will be transparent and show anything behind the shape.</span></span>                                                                                                                                                                                                                                                             |
| <span data-ttu-id="2473c-216">Control1</span><span class="sxs-lookup"><span data-stu-id="2473c-216">Control1</span></span>     | <span data-ttu-id="2473c-217">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-217">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="2473c-218">Punto di controllo per la curva.</span><span class="sxs-lookup"><span data-stu-id="2473c-218">Control point for curve.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="2473c-219">Controllo2</span><span class="sxs-lookup"><span data-stu-id="2473c-219">Control2</span></span>     | <span data-ttu-id="2473c-220">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-220">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="2473c-221">Punto di controllo per la curva.</span><span class="sxs-lookup"><span data-stu-id="2473c-221">Control point for curve.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="2473c-222">CoordOrigin</span><span class="sxs-lookup"><span data-stu-id="2473c-222">CoordOrigin</span></span>  | <span data-ttu-id="2473c-223">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md) Coordinate nell'angolo superiore sinistro del rettangolo del contenitore.</span><span class="sxs-lookup"><span data-stu-id="2473c-223">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md) The coordinates at the top left corner of the container rectangle.</span></span> <span data-ttu-id="2473c-224">Intervallo compreso tra 0 e infinito.</span><span class="sxs-lookup"><span data-stu-id="2473c-224">Range from 0 to infinity.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="2473c-225">CoordSize</span><span class="sxs-lookup"><span data-stu-id="2473c-225">CoordSize</span></span>    | <span data-ttu-id="2473c-226">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-226">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="2473c-227">Larghezza e altezza dello spazio delle coordinate all'interno del rettangolo di riferimento di questa forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-227">The width and height of the coordinate space inside the reference rectangle of this shape.</span></span> <span data-ttu-id="2473c-228">Se non è specificato, è uguale alla larghezza e all'altezza del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="2473c-228">If it is not specified, it is the same as the width and height of the rectangle.</span></span> <span data-ttu-id="2473c-229">Intervallo compreso tra 0 e infinito.</span><span class="sxs-lookup"><span data-stu-id="2473c-229">Range from 0 to infinity.</span></span> <span data-ttu-id="2473c-230">Impostazione predefinita: "1000, 1000".</span><span class="sxs-lookup"><span data-stu-id="2473c-230">Default: "1000,1000".</span></span>                                                                                               |
| <span data-ttu-id="2473c-231">EndAngle</span><span class="sxs-lookup"><span data-stu-id="2473c-231">EndAngle</span></span>     | <span data-ttu-id="2473c-232">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-232">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="2473c-233">Angolo finale della forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-233">End angle of shape.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="2473c-234">Estrusione</span><span class="sxs-lookup"><span data-stu-id="2473c-234">Extrusion</span></span>    | <span data-ttu-id="2473c-235">IVgExtrusion.</span><span class="sxs-lookup"><span data-stu-id="2473c-235">IVgExtrusion.</span></span> <span data-ttu-id="2473c-236">Specifica il valore dell'oggetto estrusione per la forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-236">Specifies the Extrusion object value for this shape.</span></span> <span data-ttu-id="2473c-237">Per informazioni dettagliate, vedere l'elemento [estrusione](msdn-online-vml-extrusion-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2473c-237">See the [Extrusion](msdn-online-vml-extrusion-element.md) element for details.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="2473c-238">Fill</span><span class="sxs-lookup"><span data-stu-id="2473c-238">Fill</span></span>         | <span data-ttu-id="2473c-239">VgFillFormat.</span><span class="sxs-lookup"><span data-stu-id="2473c-239">VgFillFormat.</span></span> <span data-ttu-id="2473c-240">Specifica il valore di riempimento per questa forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-240">Specifies the fill value for this shape.</span></span> <span data-ttu-id="2473c-241">Per ulteriori informazioni, vedere l'elemento [Fill](msdn-online-vml-fill-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2473c-241">See the [Fill](msdn-online-vml-fill-element.md) element for more details.</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="2473c-242">FillColor</span><span class="sxs-lookup"><span data-stu-id="2473c-242">FillColor</span></span>    | <span data-ttu-id="2473c-243">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-243">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="2473c-244">Colore principale del pennello da utilizzare per riempire il percorso di questa forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-244">The primary color of the brush to use to fill the path of this shape.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="2473c-245">Compilato</span><span class="sxs-lookup"><span data-stu-id="2473c-245">Filled</span></span>       | <span data-ttu-id="2473c-246">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-246">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="2473c-247">Se true, verrà riempito il percorso che definisce la forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-247">If True, the path defining the shape will be filled.</span></span> <span data-ttu-id="2473c-248">Per impostazione predefinita, verrà riempito con un colore a tinta unita a meno che non esista un sottoelemento Fill che specifica proprietà di riempimento più complesse.</span><span class="sxs-lookup"><span data-stu-id="2473c-248">By default, it will be filled using a solid color unless there is a Fill subelement that specifies more complex fill properties.</span></span> <span data-ttu-id="2473c-249">Se false, il riempimento è trasparente.</span><span class="sxs-lookup"><span data-stu-id="2473c-249">If False, the fill is transparent.</span></span>                                                                                                           |
| <span data-ttu-id="2473c-250">Capovolgi</span><span class="sxs-lookup"><span data-stu-id="2473c-250">Flip</span></span>         | <span data-ttu-id="2473c-251">VgFlipOrientation.</span><span class="sxs-lookup"><span data-stu-id="2473c-251">VgFlipOrientation.</span></span> <span data-ttu-id="2473c-252">I valori sono: X Y XY YX</span><span class="sxs-lookup"><span data-stu-id="2473c-252">Values are: X Y XY YX</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="2473c-253">ForceDash</span><span class="sxs-lookup"><span data-stu-id="2473c-253">ForceDash</span></span>    | <span data-ttu-id="2473c-254">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-254">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="2473c-255">Indica che deve essere eseguito il rendering di un contorno tratteggiato quando non è presente alcuna riga e nessun riempimento per una forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-255">Indication that a dashed outline should be rendered when there is no line and no fill for a shape.</span></span> <span data-ttu-id="2473c-256">Questo comportamento è in genere utile per rendere visibili le forme invisibili nella modifica delle applicazioni in modo che possano essere selezionate e utilizzate, ad esempio in una mappa immagine.</span><span class="sxs-lookup"><span data-stu-id="2473c-256">This behavior is generally useful for making invisible shapes visible in editing applications so they can be selected and operated on, such as in an image map.</span></span>                                                                 |
| <span data-ttu-id="2473c-257">Formule</span><span class="sxs-lookup"><span data-stu-id="2473c-257">Formulas</span></span>     | <span data-ttu-id="2473c-258">IVgFormulas.</span><span class="sxs-lookup"><span data-stu-id="2473c-258">IVgFormulas.</span></span> <span data-ttu-id="2473c-259">Matrice di formule che definisce una forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-259">An array of formulas that defines a shape.</span></span>                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="2473c-260">Da</span><span class="sxs-lookup"><span data-stu-id="2473c-260">From</span></span>         | <span data-ttu-id="2473c-261">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-261">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="2473c-262">Punto iniziale della linea.</span><span class="sxs-lookup"><span data-stu-id="2473c-262">Starting point of line.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="2473c-263">HRef</span><span class="sxs-lookup"><span data-stu-id="2473c-263">HRef</span></span>         | <span data-ttu-id="2473c-264">[Stringa](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-264">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="2473c-265">URL a cui passare se si fa clic sulla forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-265">The URL to jump to if this shape is clicked.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="2473c-266">ImageData</span><span class="sxs-lookup"><span data-stu-id="2473c-266">ImageData</span></span>    | <span data-ttu-id="2473c-267">IVgImageData.</span><span class="sxs-lookup"><span data-stu-id="2473c-267">IVgImageData.</span></span> <span data-ttu-id="2473c-268">Informazioni sull'immagine se la forma è un'immagine.</span><span class="sxs-lookup"><span data-stu-id="2473c-268">Image information if the shape is a picture.</span></span> <span data-ttu-id="2473c-269">Per ulteriori informazioni, vedere l'elemento ImageData.</span><span class="sxs-lookup"><span data-stu-id="2473c-269">See the ImageData element for more information.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="2473c-270">OnEd</span><span class="sxs-lookup"><span data-stu-id="2473c-270">OnEd</span></span>         | <span data-ttu-id="2473c-271">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-271">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="2473c-272">Nasconde tutti gli handle ad eccezione della parte superiore sinistra e della parte inferiore destra, come negli handle per un segmento di linea retta.</span><span class="sxs-lookup"><span data-stu-id="2473c-272">Hides all handles except the top left and bottom right, as in the handles for a straight line segment.</span></span>                                                                                                                                                                                                                             |
| <span data-ttu-id="2473c-273">Opacità</span><span class="sxs-lookup"><span data-stu-id="2473c-273">Opacity</span></span>      | <span data-ttu-id="2473c-274">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-274">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="2473c-275">Opacità dell'intera forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-275">The opacity of the entire shape.</span></span> <span data-ttu-id="2473c-276">Numero compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="2473c-276">A number between 0.0 and 1.0.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="2473c-277">Percorso</span><span class="sxs-lookup"><span data-stu-id="2473c-277">Path</span></span>         | <span data-ttu-id="2473c-278">IVgPath.</span><span class="sxs-lookup"><span data-stu-id="2473c-278">IVgPath.</span></span> <span data-ttu-id="2473c-279">Stringa contenente i comandi che definiscono il percorso.</span><span class="sxs-lookup"><span data-stu-id="2473c-279">A string containing the commands that define the path.</span></span>                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="2473c-280">Punti</span><span class="sxs-lookup"><span data-stu-id="2473c-280">Points</span></span>       | <span data-ttu-id="2473c-281">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-281">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md).</span></span> <span data-ttu-id="2473c-282">Raccolta di punti che definiscono una forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-282">A collection of points defining a shape.</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="2473c-283">Stampa</span><span class="sxs-lookup"><span data-stu-id="2473c-283">Print</span></span>        | <span data-ttu-id="2473c-284">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-284">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="2473c-285">Se true, la forma deve essere stampata.</span><span class="sxs-lookup"><span data-stu-id="2473c-285">If True, this shape is meant to be printed.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="2473c-286">Rotazione</span><span class="sxs-lookup"><span data-stu-id="2473c-286">Rotation</span></span>     | <span data-ttu-id="2473c-287">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-287">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="2473c-288">Imposta la rotazione della forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-288">Sets rotation of shape.</span></span> <span data-ttu-id="2473c-289">Il valore viene propagato allo stile della forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-289">Value is propagated to the shape style.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="2473c-290">Scalabilità</span><span class="sxs-lookup"><span data-stu-id="2473c-290">Scale</span></span>        | <span data-ttu-id="2473c-291">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-291">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="2473c-292">Scala della forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-292">Scale of shape.</span></span>                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="2473c-293">Ombreggiatura</span><span class="sxs-lookup"><span data-stu-id="2473c-293">Shadow</span></span>       | <span data-ttu-id="2473c-294">IVgShadow.</span><span class="sxs-lookup"><span data-stu-id="2473c-294">IVgShadow.</span></span> <span data-ttu-id="2473c-295">Specifica l'ombreggiatura per questa forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-295">Specifies the shadow for this shape.</span></span> <span data-ttu-id="2473c-296">Per informazioni dettagliate, vedere l'elemento [shadow](msdn-online-vml-shadow-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2473c-296">See the [Shadow](msdn-online-vml-shadow-element.md) element for details.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="2473c-297">SPT</span><span class="sxs-lookup"><span data-stu-id="2473c-297">Spt</span></span>          | <span data-ttu-id="2473c-298">Riservato.</span><span class="sxs-lookup"><span data-stu-id="2473c-298">Reserved.</span></span>                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="2473c-299">StartAngle</span><span class="sxs-lookup"><span data-stu-id="2473c-299">StartAngle</span></span>   | <span data-ttu-id="2473c-300">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-300">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="2473c-301">Angolo iniziale della forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-301">Start angle of shape.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="2473c-302">Stroke</span><span class="sxs-lookup"><span data-stu-id="2473c-302">Stroke</span></span>       | <span data-ttu-id="2473c-303">VgStrokeFormat.</span><span class="sxs-lookup"><span data-stu-id="2473c-303">VgStrokeFormat.</span></span> <span data-ttu-id="2473c-304">Per informazioni dettagliate, vedere elemento Stroke.</span><span class="sxs-lookup"><span data-stu-id="2473c-304">See Stroke element for details.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="2473c-305">StrokeColor</span><span class="sxs-lookup"><span data-stu-id="2473c-305">StrokeColor</span></span>  | <span data-ttu-id="2473c-306">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-306">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="2473c-307">Colore principale del pennello da utilizzare per tracciare il percorso di questa forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-307">The primary color of the brush to use to stroke the path of this shape.</span></span>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="2473c-308">Tracciato</span><span class="sxs-lookup"><span data-stu-id="2473c-308">Stroked</span></span>      | <span data-ttu-id="2473c-309">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-309">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="2473c-310">Se true, verrà tracciato il percorso che definisce la forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-310">If True, the path defining the shape will be stroked.</span></span>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="2473c-311">StrokeWeight</span><span class="sxs-lookup"><span data-stu-id="2473c-311">StrokeWeight</span></span> | <span data-ttu-id="2473c-312">[VGLength](msdn-online-vml-vglength.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-312">[VGLength](msdn-online-vml-vglength.md).</span></span> <span data-ttu-id="2473c-313">Larghezza del pennello da utilizzare per tracciare il tracciato.</span><span class="sxs-lookup"><span data-stu-id="2473c-313">The width of the brush to use to stroke the path.</span></span> <span data-ttu-id="2473c-314">Intervallo compreso tra 0 e 1584.</span><span class="sxs-lookup"><span data-stu-id="2473c-314">Ranges between 0 and 1584.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="2473c-315">TextPath</span><span class="sxs-lookup"><span data-stu-id="2473c-315">TextPath</span></span>     | <span data-ttu-id="2473c-316">IVgTextPath.</span><span class="sxs-lookup"><span data-stu-id="2473c-316">IVgTextPath.</span></span> <span data-ttu-id="2473c-317">Specifica l'oggetto TextPath della forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-317">Specifies the TextPath object of the shape.</span></span> <span data-ttu-id="2473c-318">Per ulteriori informazioni, vedere l'elemento [TextPath](msdn-online-vml-textpath-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2473c-318">See the [TextPath](msdn-online-vml-textpath-element.md) element for more information.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="2473c-319">A</span><span class="sxs-lookup"><span data-stu-id="2473c-319">To</span></span>           | <span data-ttu-id="2473c-320">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-320">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="2473c-321">Punto finale della linea.</span><span class="sxs-lookup"><span data-stu-id="2473c-321">End point of line.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="2473c-322">Tipo</span><span class="sxs-lookup"><span data-stu-id="2473c-322">Type</span></span>         | <span data-ttu-id="2473c-323">Stringa.</span><span class="sxs-lookup"><span data-stu-id="2473c-323">String.</span></span> <span data-ttu-id="2473c-324">Tipo di forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-324">Type of shape.</span></span>                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="subelements-of-the-shape-element"></a><span data-ttu-id="2473c-325">Sottoelementi dell'elemento Shape</span><span class="sxs-lookup"><span data-stu-id="2473c-325">Subelements of the Shape Element</span></span>

<span data-ttu-id="2473c-326">I sottoelementi seguenti fanno parte del modello a oggetti la.</span><span class="sxs-lookup"><span data-stu-id="2473c-326">The following subelements are part of the VML object model.</span></span>

-   [<span data-ttu-id="2473c-327">Background</span><span class="sxs-lookup"><span data-stu-id="2473c-327">Background</span></span>](#background-element)
-   [<span data-ttu-id="2473c-328">Estrusione</span><span class="sxs-lookup"><span data-stu-id="2473c-328">Extrusion</span></span>](#extrusion-element)
-   [<span data-ttu-id="2473c-329">Fill</span><span class="sxs-lookup"><span data-stu-id="2473c-329">Fill</span></span>](#fill-element)
-   [<span data-ttu-id="2473c-330">Gruppo</span><span class="sxs-lookup"><span data-stu-id="2473c-330">Group</span></span>](#group-element)
-   [<span data-ttu-id="2473c-331">ImageData</span><span class="sxs-lookup"><span data-stu-id="2473c-331">Imagedata</span></span>](#imagedata-element)
-   [<span data-ttu-id="2473c-332">Percorso</span><span class="sxs-lookup"><span data-stu-id="2473c-332">Path</span></span>](#path-element)
-   [<span data-ttu-id="2473c-333">Shadow</span><span class="sxs-lookup"><span data-stu-id="2473c-333">Shadow</span></span>](#shadow-element)
-   [<span data-ttu-id="2473c-334">Sfasamento</span><span class="sxs-lookup"><span data-stu-id="2473c-334">Skew</span></span>](#skew-element)
-   [<span data-ttu-id="2473c-335">Stroke</span><span class="sxs-lookup"><span data-stu-id="2473c-335">Stroke</span></span>](#stroke-element)
-   [<span data-ttu-id="2473c-336">TextPath</span><span class="sxs-lookup"><span data-stu-id="2473c-336">TextPath</span></span>](#textpath-element)

### <a name="background-element"></a><span data-ttu-id="2473c-337">Elemento background</span><span class="sxs-lookup"><span data-stu-id="2473c-337">Background element</span></span>

<span data-ttu-id="2473c-338">Descrive il riempimento dello sfondo di una pagina usando Fill la.</span><span class="sxs-lookup"><span data-stu-id="2473c-338">Describes the fill of the background of a page using VML fills.</span></span>

<span data-ttu-id="2473c-339">**Attributes (Attributi)**</span><span class="sxs-lookup"><span data-stu-id="2473c-339">**Attributes**</span></span>



|           |                                                                                                                                                                                         |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2473c-340">BWMode</span><span class="sxs-lookup"><span data-stu-id="2473c-340">BWMode</span></span>    | <span data-ttu-id="2473c-341">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-341">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="2473c-342">Determina la modalità di rendering della forma nella visualizzazione in bianco e nero nelle applicazioni o quando viene stampata.</span><span class="sxs-lookup"><span data-stu-id="2473c-342">Determines how shape will render in black-and-white view in applications or when printed.</span></span>                                     |
| <span data-ttu-id="2473c-343">BWNormal</span><span class="sxs-lookup"><span data-stu-id="2473c-343">BWNormal</span></span>  | <span data-ttu-id="2473c-344">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-344">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="2473c-345">Quando BWMode è auto, viene consultata questa proprietà per il rendering della forma in bianco e nero normale.</span><span class="sxs-lookup"><span data-stu-id="2473c-345">When BWMode is Auto, this property is consulted for how to render the shape in normal black and white.</span></span>                        |
| <span data-ttu-id="2473c-346">BWPure</span><span class="sxs-lookup"><span data-stu-id="2473c-346">BWPure</span></span>    | <span data-ttu-id="2473c-347">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-347">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="2473c-348">Quando BWMode è auto, viene consultata questa proprietà per il rendering della forma in bianco e nero puro.</span><span class="sxs-lookup"><span data-stu-id="2473c-348">When BWMode is Auto, this property is consulted for how to render the shape in pure black and white.</span></span>                          |
| <span data-ttu-id="2473c-349">Fill</span><span class="sxs-lookup"><span data-stu-id="2473c-349">Fill</span></span>      | <span data-ttu-id="2473c-350">VgFillFormat.</span><span class="sxs-lookup"><span data-stu-id="2473c-350">VgFillFormat.</span></span> <span data-ttu-id="2473c-351">Specifica il riempimento per questa forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-351">Specifies the fill for this shape.</span></span> <span data-ttu-id="2473c-352">Per ulteriori informazioni, vedere elemento [Fill](msdn-online-vml-fill-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2473c-352">See [Fill](msdn-online-vml-fill-element.md) element for more information.</span></span>                                                             |
| <span data-ttu-id="2473c-353">FillColor</span><span class="sxs-lookup"><span data-stu-id="2473c-353">FillColor</span></span> | <span data-ttu-id="2473c-354">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-354">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="2473c-355">Colore principale del pennello da utilizzare per riempire il percorso di questa forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-355">The primary color of the brush to use to fill the path of this shape.</span></span> <span data-ttu-id="2473c-356">Duplicato del valore del colore nell'elemento Fill.</span><span class="sxs-lookup"><span data-stu-id="2473c-356">Duplicate of the Color value in the Fill element.</span></span> <span data-ttu-id="2473c-357">Il valore predefinito è bianco.</span><span class="sxs-lookup"><span data-stu-id="2473c-357">The default is white.</span></span> |



 

### <a name="extrusion-element"></a><span data-ttu-id="2473c-358">Elemento Extrusion</span><span class="sxs-lookup"><span data-stu-id="2473c-358">Extrusion element</span></span>

<span data-ttu-id="2473c-359">Descrive un'estrusione 3D della forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-359">Describes a 3-D extrusion of the shape.</span></span>

<span data-ttu-id="2473c-360">**Attributes (Attributi)**</span><span class="sxs-lookup"><span data-stu-id="2473c-360">**Attributes**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2473c-361">AutoRotationCenter</span><span class="sxs-lookup"><span data-stu-id="2473c-361">AutoRotationCenter</span></span></td>
<td><span data-ttu-id="2473c-362"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-362"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="2473c-363">Se true, il centro di rotazione del gruppo di oggetti 3D (in effetti esiste solo un oggetto nel gruppo) viene determinato automaticamente come il centro del gruppo. in caso contrario, viene determinato dai parametri RotationCenter, che sono una frazione della forma con 0, 0, 0 che corrisponde al centro.</span><span class="sxs-lookup"><span data-stu-id="2473c-363">If True, the center of rotation of the group of 3-D objects (in fact there is only ever one object in the group) is determined automatically to be the center of the group; otherwise it is determined by the RotationCenter parameters, which are a fraction of the shape with 0,0,0 being the center.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-364">Backdepth</span><span class="sxs-lookup"><span data-stu-id="2473c-364">BackDepth</span></span></td>
<td><span data-ttu-id="2473c-365"><a href="msdn-online-vml-vglength.md"><strong>VgLength</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-365"><a href="msdn-online-vml-vglength.md"><strong>VgLength</strong></a>.</span></span> <span data-ttu-id="2473c-366">Quantità di estrusione a ritroso.</span><span class="sxs-lookup"><span data-stu-id="2473c-366">Amount of backward extrusion.</span></span> <span data-ttu-id="2473c-367">È compreso tra 0 e 32767.</span><span class="sxs-lookup"><span data-stu-id="2473c-367">Ranges from 0 to 32767.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-368">Luminosità</span><span class="sxs-lookup"><span data-stu-id="2473c-368">Brightness</span></span></td>
<td><span data-ttu-id="2473c-369"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-369"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="2473c-370">Luminosità complessiva della scena.</span><span class="sxs-lookup"><span data-stu-id="2473c-370">Overall brightness of the scene.</span></span> <span data-ttu-id="2473c-371">Il valore predefinito è &quot; 20.000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="2473c-371">Default is &quot;20,000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-372">Colore</span><span class="sxs-lookup"><span data-stu-id="2473c-372">Color</span></span></td>
<td><span data-ttu-id="2473c-373"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-373"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="2473c-374">Colore dell'estrusione.</span><span class="sxs-lookup"><span data-stu-id="2473c-374">The color of the extrusion.</span></span> <span data-ttu-id="2473c-375">Usato solo se ColorMode è Custom.</span><span class="sxs-lookup"><span data-stu-id="2473c-375">Only used if ColorMode is Custom.</span></span> <span data-ttu-id="2473c-376">In caso contrario, imposta automaticamente il colore dell'effetto Estrusione sullo stesso FillColor.</span><span class="sxs-lookup"><span data-stu-id="2473c-376">Otherwise, Auto sets the extrusion effect color to the same as FillColor.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-377">ColorMode</span><span class="sxs-lookup"><span data-stu-id="2473c-377">ColorMode</span></span></td>
<td><span data-ttu-id="2473c-378">Vg3DColorMode.</span><span class="sxs-lookup"><span data-stu-id="2473c-378">Vg3DColorMode.</span></span> <span data-ttu-id="2473c-379">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="2473c-379">Values are:</span></span>
<ul>
<li><span data-ttu-id="2473c-380">Automatico (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2473c-380">Auto (default)</span></span></li>
<li><span data-ttu-id="2473c-381">Personalizzato</span><span class="sxs-lookup"><span data-stu-id="2473c-381">Custom</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-382">Diffusione</span><span class="sxs-lookup"><span data-stu-id="2473c-382">Diffusity</span></span></td>
<td><span data-ttu-id="2473c-383"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-383"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="2473c-384">Rapporto tra evento imprevisto e riflesso chiaro.</span><span class="sxs-lookup"><span data-stu-id="2473c-384">The ratio of incident to diffusely reflected light.</span></span> <span data-ttu-id="2473c-385">I valori minori di 1,0 sono normali, ma i valori superiori a uno possono generare effetti interessanti.</span><span class="sxs-lookup"><span data-stu-id="2473c-385">Values less than 1.0 are normal but values higher than one can generate interesting effects.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-386">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2473c-386">Edge</span></span></td>
<td><span data-ttu-id="2473c-387"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-387"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="2473c-388">Imposta la dimensione di un bordo smussato arrotondato simulato.</span><span class="sxs-lookup"><span data-stu-id="2473c-388">Sets the size of a simulated rounded beveled edge.</span></span> <span data-ttu-id="2473c-389">Varia da 0 a 32767 in PTS a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="2473c-389">Ranges from 0 to 32767 in floating point pts.</span></span> <span data-ttu-id="2473c-390">Il valore predefinito è &quot; 1Pt &quot; .</span><span class="sxs-lookup"><span data-stu-id="2473c-390">Default is &quot;1pt&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-391">Facet</span><span class="sxs-lookup"><span data-stu-id="2473c-391">Facet</span></span></td>
<td><span data-ttu-id="2473c-392"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-392"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="2473c-393">Imposta il facet della scena.</span><span class="sxs-lookup"><span data-stu-id="2473c-393">Sets the facet of the scene.</span></span> <span data-ttu-id="2473c-394">Il valore predefinito è &quot; 30.000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="2473c-394">Default is &quot;30,000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-395">ForeDepth</span><span class="sxs-lookup"><span data-stu-id="2473c-395">ForeDepth</span></span></td>
<td><span data-ttu-id="2473c-396"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-396"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="2473c-397">Quantità di estrusione di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="2473c-397">Amount of forward extrusion.</span></span> <span data-ttu-id="2473c-398">È compreso tra 0 e 32767.</span><span class="sxs-lookup"><span data-stu-id="2473c-398">Ranges from 0 to 32767.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-399">LightFace</span><span class="sxs-lookup"><span data-stu-id="2473c-399">LightFace</span></span></td>
<td><span data-ttu-id="2473c-400"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-400"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="2473c-401">Determimes se il front-end dell'oggetto risponderà alle modifiche nell'illuminazione 3D, ad esempio quando un oggetto viene ruotato.</span><span class="sxs-lookup"><span data-stu-id="2473c-401">Determimes whether the front face of the object will respond to changes in the 3-D lighting, e.g., when an object rotates.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-402">LightHarsh</span><span class="sxs-lookup"><span data-stu-id="2473c-402">LightHarsh</span></span></td>
<td><span data-ttu-id="2473c-403"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-403"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="2473c-404">Illuminazione rigida per la fonte di luce primaria.</span><span class="sxs-lookup"><span data-stu-id="2473c-404">Harsh lighting for the primary light source.</span></span> <span data-ttu-id="2473c-405">Il valore predefinito è False.</span><span class="sxs-lookup"><span data-stu-id="2473c-405">Default is False.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-406">LightHarsh2</span><span class="sxs-lookup"><span data-stu-id="2473c-406">LightHarsh2</span></span></td>
<td><span data-ttu-id="2473c-407"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-407"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="2473c-408">Illuminazione rigida per la sorgente di luce secondaria.</span><span class="sxs-lookup"><span data-stu-id="2473c-408">Harsh lighting for the secondary light source.</span></span> <span data-ttu-id="2473c-409">Il valore predefinito è False.</span><span class="sxs-lookup"><span data-stu-id="2473c-409">Default is False.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-410">LightLevel</span><span class="sxs-lookup"><span data-stu-id="2473c-410">LightLevel</span></span></td>
<td><span data-ttu-id="2473c-411"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-411"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span></span> <span data-ttu-id="2473c-412">Intensità della sorgente di luce primaria.</span><span class="sxs-lookup"><span data-stu-id="2473c-412">Intensity of the primary light source.</span></span> <span data-ttu-id="2473c-413">Il valore predefinito è &quot; 38000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="2473c-413">Default is &quot;38000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-414">LightLevel2</span><span class="sxs-lookup"><span data-stu-id="2473c-414">LightLevel2</span></span></td>
<td><span data-ttu-id="2473c-415"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-415"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span></span> <span data-ttu-id="2473c-416">Intensità della sorgente di luce secondaria.</span><span class="sxs-lookup"><span data-stu-id="2473c-416">Intensity of the secondary light source.</span></span> <span data-ttu-id="2473c-417">Il valore predefinito è &quot; 38000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="2473c-417">Default is &quot;38000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-418">Posizioneilluminazione</span><span class="sxs-lookup"><span data-stu-id="2473c-418">LightPosition</span></span></td>
<td><span data-ttu-id="2473c-419">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="2473c-419">Vector3D.</span></span> <span data-ttu-id="2473c-420">Posizione della sorgente di luce primaria.</span><span class="sxs-lookup"><span data-stu-id="2473c-420">Position of the primary light source.</span></span> <span data-ttu-id="2473c-421">Il valore predefinito è &quot; 50000, 0, 10000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="2473c-421">Default is &quot;50000,0,10000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-422">LightPosition2</span><span class="sxs-lookup"><span data-stu-id="2473c-422">LightPosition2</span></span></td>
<td><span data-ttu-id="2473c-423">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="2473c-423">Vector3D.</span></span> <span data-ttu-id="2473c-424">Posizione della sorgente di luce secondaria.</span><span class="sxs-lookup"><span data-stu-id="2473c-424">Position of the secondary light source.</span></span> <span data-ttu-id="2473c-425">Il valore predefinito è &quot; -50000, 0, 10000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="2473c-425">Default is &quot;-50000,0,10000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-426">LockRotationCenter</span><span class="sxs-lookup"><span data-stu-id="2473c-426">LockRotationCenter</span></span></td>
<td><span data-ttu-id="2473c-427"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-427"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="2473c-428">&quot;Lockrotationcenter &quot; significa che la rotazione del gruppo è definita in base all'angolo di rotazione [1] gradi sull'asse y della pagina, seguito da angolo di rotazione [0] gradi sull'asse x.</span><span class="sxs-lookup"><span data-stu-id="2473c-428">&quot;Lockrotationcenter&quot; means that the rotation of the group is defined to be by rotation-angle[1] degrees about the y-axis on the page followed by rotation-angle[0] degrees about the x-axis.</span></span> <span data-ttu-id="2473c-429">Quando LockRotationCenter è false, la rotazione viene definita in base ai gradi dell'angolo di orientamento del vettore definito dall'orientamento.</span><span class="sxs-lookup"><span data-stu-id="2473c-429">When LockRotationCenter is False, the rotation is defined to be by orientation-angle degrees about the vector defined by orientation.</span></span> <span data-ttu-id="2473c-430">Quindi, ad esempio, lockrotationcenter = false OrientationAngle = 45 Orientation = (0, 1, 0) equivale a lockrotationcenter = true RotationAngle = (0, 45).</span><span class="sxs-lookup"><span data-stu-id="2473c-430">So, for example, lockrotationcenter=false orientationangle=45 orientation=(0,1,0) is equivalent to lockrotationcenter=true rotationangle=(0,45).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-431">Metallico</span><span class="sxs-lookup"><span data-stu-id="2473c-431">Metal</span></span></td>
<td><span data-ttu-id="2473c-432"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-432"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="2473c-433">Fa in modo che la luce riflessa in modo speculare sia il colore del materiale anziché il colore della sorgente di luce, rendendo l'oggetto più metallico.</span><span class="sxs-lookup"><span data-stu-id="2473c-433">Causes specularly reflected light to be the material color instead of the light source color, making the object seem more metallic.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-434">Attivato</span><span class="sxs-lookup"><span data-stu-id="2473c-434">On</span></span></td>
<td><span data-ttu-id="2473c-435"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-435"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="2473c-436">Attiva e disattiva la visualizzazione dell'effetto estrusione.</span><span class="sxs-lookup"><span data-stu-id="2473c-436">Turns the display of the extrusion effect on and off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-437">Orientamento</span><span class="sxs-lookup"><span data-stu-id="2473c-437">Orientation</span></span></td>
<td><span data-ttu-id="2473c-438">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="2473c-438">Vector3D.</span></span> <span data-ttu-id="2473c-439">Orientamento della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="2473c-439">Orientation of the camera.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-440">OrientationAngle</span><span class="sxs-lookup"><span data-stu-id="2473c-440">OrientationAngle</span></span></td>
<td><span data-ttu-id="2473c-441"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-441"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="2473c-442">Angolo tra l'orientamento della fotocamera e il piano XY.</span><span class="sxs-lookup"><span data-stu-id="2473c-442">Angle between the orientation of the camera and the xy plane.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-443">Aereo</span><span class="sxs-lookup"><span data-stu-id="2473c-443">Plane</span></span></td>
<td><span data-ttu-id="2473c-444">Vg3DExtrudePlane.</span><span class="sxs-lookup"><span data-stu-id="2473c-444">Vg3DExtrudePlane.</span></span> <span data-ttu-id="2473c-445">Consente l'estrusione da piani ortogonali al piano dello schermo.</span><span class="sxs-lookup"><span data-stu-id="2473c-445">Allows extrusion from planes orthogonal to the screen plane.</span></span> <span data-ttu-id="2473c-446">È necessario specificare ForeDepth e backdepth nelle unità di disegno anziché in emù.</span><span class="sxs-lookup"><span data-stu-id="2473c-446">Requires ForeDepth and BackDepth to be specified in drawing units instead of emus.</span></span> <span data-ttu-id="2473c-447">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="2473c-447">Values are:</span></span>
<ul>
<li><span data-ttu-id="2473c-448">XY</span><span class="sxs-lookup"><span data-stu-id="2473c-448">XY</span></span></li>
<li><span data-ttu-id="2473c-449">ZX</span><span class="sxs-lookup"><span data-stu-id="2473c-449">ZX</span></span></li>
<li><span data-ttu-id="2473c-450">YZ</span><span class="sxs-lookup"><span data-stu-id="2473c-450">YZ</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-451">Rendering</span><span class="sxs-lookup"><span data-stu-id="2473c-451">Render</span></span></td>
<td><span data-ttu-id="2473c-452">Vg3DRenderMode.</span><span class="sxs-lookup"><span data-stu-id="2473c-452">Vg3DRenderMode.</span></span> <span data-ttu-id="2473c-453">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="2473c-453">Values are:</span></span>
<ul>
<li><span data-ttu-id="2473c-454">Solid (valore predefinito)</span><span class="sxs-lookup"><span data-stu-id="2473c-454">Solid (default)</span></span></li>
<li><span data-ttu-id="2473c-455">WireFrame</span><span class="sxs-lookup"><span data-stu-id="2473c-455">WireFrame</span></span></li>
<li><span data-ttu-id="2473c-456">BoundingCube</span><span class="sxs-lookup"><span data-stu-id="2473c-456">BoundingCube</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-457">RotationAngle</span><span class="sxs-lookup"><span data-stu-id="2473c-457">RotationAngle</span></span></td>
<td><span data-ttu-id="2473c-458"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-458"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="2473c-459">AngleX, AngleY o AngleZ è controllato dall'attributo ShapeRotation.</span><span class="sxs-lookup"><span data-stu-id="2473c-459">AngleX, AngleY, or AngleZ is controlled by the ShapeRotation attribute.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-460">RotationCenter</span><span class="sxs-lookup"><span data-stu-id="2473c-460">RotationCenter</span></span></td>
<td><span data-ttu-id="2473c-461">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="2473c-461">Vector3D.</span></span> <span data-ttu-id="2473c-462">Centro di rotazione.</span><span class="sxs-lookup"><span data-stu-id="2473c-462">Center of rotation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-463">Lucentezza</span><span class="sxs-lookup"><span data-stu-id="2473c-463">Shininess</span></span></td>
<td><span data-ttu-id="2473c-464"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-464"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="2473c-465">Determina il modo in cui la reflection speculare è concentrata o distribuita.</span><span class="sxs-lookup"><span data-stu-id="2473c-465">Determines how concentrated or spread out specular reflection is.</span></span> <span data-ttu-id="2473c-466">Un valore elevato è da 8 a 10 e si avvicinerà a un mirror e un valore basso sarebbe da 2 a 3 e avrebbe approssimato gli indumenti paillettes.</span><span class="sxs-lookup"><span data-stu-id="2473c-466">A high value would be 8 to 10 and would approximate a mirror, and a low value would be 2 to 3 and would approximate sequined clothing.</span></span> <span data-ttu-id="2473c-467">Sono consigliati i valori da 3 a 7.</span><span class="sxs-lookup"><span data-stu-id="2473c-467">Values of 3 to 7 are recommended.</span></span> <span data-ttu-id="2473c-468">I valori elevati riflettono le fonti di luce.</span><span class="sxs-lookup"><span data-stu-id="2473c-468">High values will reflect pinpoint light sources.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-469">SkewAmt</span><span class="sxs-lookup"><span data-stu-id="2473c-469">SkewAmt</span></span></td>
<td><span data-ttu-id="2473c-470"><a href="#data-types-used-in-the-vml-object-model">VgPercentage</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-470"><a href="#data-types-used-in-the-vml-object-model">VgPercentage</a>.</span></span> <span data-ttu-id="2473c-471">Se il tipo è parallelo, l'attributo determina la quantità di asimmetria.</span><span class="sxs-lookup"><span data-stu-id="2473c-471">If Type is Parallel, attribute determines the amount of skew.</span></span> <span data-ttu-id="2473c-472">È compreso tra 0 e 100.</span><span class="sxs-lookup"><span data-stu-id="2473c-472">Ranges from 0 to 100.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-473">SkewAngle</span><span class="sxs-lookup"><span data-stu-id="2473c-473">SkewAngle</span></span></td>
<td><span data-ttu-id="2473c-474"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-474"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="2473c-475">Se il tipo è parallelo, l'attributo determina il grado di asimmetria.</span><span class="sxs-lookup"><span data-stu-id="2473c-475">If Type is Parallel, attribute determines the degree of skew.</span></span> <span data-ttu-id="2473c-476">Il valore predefinito è &quot; -45 &quot; .</span><span class="sxs-lookup"><span data-stu-id="2473c-476">Default is &quot;-45&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-477">Specularità</span><span class="sxs-lookup"><span data-stu-id="2473c-477">Specularity</span></span></td>
<td><span data-ttu-id="2473c-478"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-478"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="2473c-479">Rapporto tra evento imprevisto e riflesso chiaro.</span><span class="sxs-lookup"><span data-stu-id="2473c-479">The ratio of incident to specularly reflected light.</span></span> <span data-ttu-id="2473c-480">I valori minori di 1,0 sono normali, ma i valori superiori a uno possono generare effetti interessanti.</span><span class="sxs-lookup"><span data-stu-id="2473c-480">Values less than 1.0 are normal but values higher than one can generate interesting effects.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-481">Tipo</span><span class="sxs-lookup"><span data-stu-id="2473c-481">Type</span></span></td>
<td><span data-ttu-id="2473c-482">VgExtrusionType.</span><span class="sxs-lookup"><span data-stu-id="2473c-482">VgExtrusionType.</span></span> <span data-ttu-id="2473c-483">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="2473c-483">Values are:</span></span>
<ul>
<li><span data-ttu-id="2473c-484">Parallel (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2473c-484">Parallel (default)</span></span></li>
<li><span data-ttu-id="2473c-485">Prospettiva</span><span class="sxs-lookup"><span data-stu-id="2473c-485">Perspective</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-486">Vista</span><span class="sxs-lookup"><span data-stu-id="2473c-486">Viewpoint</span></span></td>
<td><span data-ttu-id="2473c-487">Vector3D.</span><span class="sxs-lookup"><span data-stu-id="2473c-487">Vector3D.</span></span> <span data-ttu-id="2473c-488">Punto da cui viene visualizzata la scena.</span><span class="sxs-lookup"><span data-stu-id="2473c-488">The point where the scene is being viewed from.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-489">ViewpointOrigin</span><span class="sxs-lookup"><span data-stu-id="2473c-489">ViewpointOrigin</span></span></td>
<td><span data-ttu-id="2473c-490"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-490"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="2473c-491">Il valore di può essere compreso tra 0,5 e-0,5 per posizionare l'origine del punto di vista nel rettangolo di delimitazione della forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-491">Can have values from 0.5 to -0.5 to position the origin of the viewpoint within the shape bounding box.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="fill-element"></a><span data-ttu-id="2473c-492">Fill (elemento)</span><span class="sxs-lookup"><span data-stu-id="2473c-492">Fill element</span></span>

<span data-ttu-id="2473c-493">Descrive il modo in cui deve essere compilato un percorso per riempimenti più complessi rispetto a un colore a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="2473c-493">Describes how a path should be filled for fills more complex than a solid color.</span></span>

<span data-ttu-id="2473c-494">**Attributes (Attributi)**</span><span class="sxs-lookup"><span data-stu-id="2473c-494">**Attributes**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2473c-495">AlignShape</span><span class="sxs-lookup"><span data-stu-id="2473c-495">AlignShape</span></span></td>
<td><span data-ttu-id="2473c-496"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-496"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="2473c-497">Allineare l'immagine alla forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-497">Align the image with the shape.</span></span> <span data-ttu-id="2473c-498">Se false, allineare l'immagine con la finestra.</span><span class="sxs-lookup"><span data-stu-id="2473c-498">If False, align image with window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-499">Angle</span><span class="sxs-lookup"><span data-stu-id="2473c-499">Angle</span></span></td>
<td><span data-ttu-id="2473c-500"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-500"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="2473c-501">Angolo lungo il quale viene rilasciata la sfumatura.</span><span class="sxs-lookup"><span data-stu-id="2473c-501">The angle along which the gradient goes.</span></span> <span data-ttu-id="2473c-502">0 gradi si trova lungo l'asse orizzontale da sinistra a destra.</span><span class="sxs-lookup"><span data-stu-id="2473c-502">0 degrees is along the horizontal axis from left to right.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-503">Aspetto</span><span class="sxs-lookup"><span data-stu-id="2473c-503">Aspect</span></span></td>
<td><span data-ttu-id="2473c-504"><strong>VgAspectType</strong>.</span><span class="sxs-lookup"><span data-stu-id="2473c-504"><strong>VgAspectType</strong>.</span></span> <span data-ttu-id="2473c-505">L'attributo ImageSize verrà regolato in modo da mantenere l'aspetto dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="2473c-505">ImageSize attribute will be adjusted to preserve the aspect of the image.</span></span> <span data-ttu-id="2473c-506">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="2473c-506">Values include:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2473c-507">Valore</span><span class="sxs-lookup"><span data-stu-id="2473c-507">Value</span></span></th>
<th><span data-ttu-id="2473c-508">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2473c-508">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2473c-509">Ignora</span><span class="sxs-lookup"><span data-stu-id="2473c-509">Ignore</span></span></td>
<td><span data-ttu-id="2473c-510">Ignorare i problemi di aspetto.</span><span class="sxs-lookup"><span data-stu-id="2473c-510">Ignore aspect issues.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-511">AtLeast</span><span class="sxs-lookup"><span data-stu-id="2473c-511">AtLeast</span></span></td>
<td><span data-ttu-id="2473c-512">L'immagine è almeno uguale alla dimensione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="2473c-512">Image is at least as big as the image size.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-513">AtMost</span><span class="sxs-lookup"><span data-stu-id="2473c-513">AtMost</span></span></td>
<td><span data-ttu-id="2473c-514">L'immagine non è più grande delle dimensioni dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="2473c-514">Image is no bigger than image size.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-515">Colore</span><span class="sxs-lookup"><span data-stu-id="2473c-515">Color</span></span></td>
<td><span data-ttu-id="2473c-516"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> Colore di riempimento principale.</span><span class="sxs-lookup"><span data-stu-id="2473c-516"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> The main fill color.</span></span> <span data-ttu-id="2473c-517">Uguale all'attributo FillColor nella forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-517">Same as FillColor attribute in shape.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-518">Color2</span><span class="sxs-lookup"><span data-stu-id="2473c-518">Color2</span></span></td>
<td><span data-ttu-id="2473c-519"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-519"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="2473c-520">Colore secondario per un riempimento quando il tipo di immagine è motivo o riempimento sfumato.</span><span class="sxs-lookup"><span data-stu-id="2473c-520">The secondary color for a fill when image type is Pattern or a gradient fill.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-521">Colori</span><span class="sxs-lookup"><span data-stu-id="2473c-521">Colors</span></span></td>
<td><span data-ttu-id="2473c-522"><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-522"><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>.</span></span> <span data-ttu-id="2473c-523">Colori intermedi nella sfumatura e relative posizioni lungo la sfumatura, ad esempio &quot; 30% rosso, 70% blu, 90% verde &quot; .</span><span class="sxs-lookup"><span data-stu-id="2473c-523">Intermediate colors in the gradient and their relative positions along the gradient, e.g., &quot;30% red, 70% blue, 90% green&quot;.</span></span> <span data-ttu-id="2473c-524">Il colore primario (attributo color nella forma) è 0% e il colore secondario (attributo color2) è 100%.</span><span class="sxs-lookup"><span data-stu-id="2473c-524">Primary color (Color attribute in shape) is 0% and secondary color (Color2 attribute) is 100%.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-525">Focus</span><span class="sxs-lookup"><span data-stu-id="2473c-525">Focus</span></span></td>
<td><span data-ttu-id="2473c-526"><a href="#data-types-used-in-the-vml-object-model">VgSignedPercentage</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-526"><a href="#data-types-used-in-the-vml-object-model">VgSignedPercentage</a>.</span></span> <span data-ttu-id="2473c-527">Punto focale del riempimento lineare sfumato.</span><span class="sxs-lookup"><span data-stu-id="2473c-527">Focal point for linear gradient fill.</span></span> <span data-ttu-id="2473c-528">I valori vanno da-100 a + 100.</span><span class="sxs-lookup"><span data-stu-id="2473c-528">Values go from -100 to +100.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-529">FocusPosition</span><span class="sxs-lookup"><span data-stu-id="2473c-529">FocusPosition</span></span></td>
<td><span data-ttu-id="2473c-530"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-530"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="2473c-531">Posizione del rettangolo più interno per le sfumature radiali.</span><span class="sxs-lookup"><span data-stu-id="2473c-531">Position of the innermost rectangle for radial gradients.</span></span> <span data-ttu-id="2473c-532">Il vettore è una frazione (0,0-1,0) della larghezza e dell'altezza della forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-532">The vector is a fraction (0.0 - 1.0) of the shape's width and height.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-533">FocusSize</span><span class="sxs-lookup"><span data-stu-id="2473c-533">FocusSize</span></span></td>
<td><span data-ttu-id="2473c-534"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Dimensioni del rettangolo più interno per le sfumature radiali.</span><span class="sxs-lookup"><span data-stu-id="2473c-534"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Size of the innermost rectangle for radial gradients.</span></span> <span data-ttu-id="2473c-535">Il vettore è una frazione (da 0,0 a 1,0) della larghezza e dell'altezza della forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-535">The vector is a fraction (0.0 to 1.0) of the shape's width and height.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-536">Metodo</span><span class="sxs-lookup"><span data-stu-id="2473c-536">Method</span></span></td>
<td><span data-ttu-id="2473c-537">VgSigmaType.</span><span class="sxs-lookup"><span data-stu-id="2473c-537">VgSigmaType.</span></span> <span data-ttu-id="2473c-538">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="2473c-538">Values include:</span></span>
<ul>
<li><span data-ttu-id="2473c-539">nessuno</span><span class="sxs-lookup"><span data-stu-id="2473c-539">None</span></span></li>
<li><span data-ttu-id="2473c-540">Lineari</span><span class="sxs-lookup"><span data-stu-id="2473c-540">Linear</span></span></li>
<li><span data-ttu-id="2473c-541">Sigma</span><span class="sxs-lookup"><span data-stu-id="2473c-541">Sigma</span></span></li>
<li><span data-ttu-id="2473c-542">Qualsiasi</span><span class="sxs-lookup"><span data-stu-id="2473c-542">Any</span></span></li>
</ul>
<p><span data-ttu-id="2473c-543">Il valore predefinito è Sigma.</span><span class="sxs-lookup"><span data-stu-id="2473c-543">Default is Sigma.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-544">Attivato</span><span class="sxs-lookup"><span data-stu-id="2473c-544">On</span></span></td>
<td><span data-ttu-id="2473c-545"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-545"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="2473c-546">Attiva la visualizzazione del riempimento.</span><span class="sxs-lookup"><span data-stu-id="2473c-546">Turns fill display on.</span></span> <span data-ttu-id="2473c-547">Uguale all'attributo Fill nella forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-547">Same as Fill attribute in shape.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-548">Opacità</span><span class="sxs-lookup"><span data-stu-id="2473c-548">Opacity</span></span></td>
<td><span data-ttu-id="2473c-549"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-549"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="2473c-550">Opacità del riempimento.</span><span class="sxs-lookup"><span data-stu-id="2473c-550">Opacity of the fill.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-551">Opacity2</span><span class="sxs-lookup"><span data-stu-id="2473c-551">Opacity2</span></span></td>
<td><span data-ttu-id="2473c-552"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-552"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="2473c-553">Opacità secondaria per le sfumature.</span><span class="sxs-lookup"><span data-stu-id="2473c-553">The secondary opacity for gradients.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-554">Origine</span><span class="sxs-lookup"><span data-stu-id="2473c-554">Origin</span></span></td>
<td><span data-ttu-id="2473c-555"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-555"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="2473c-556">Punto relativo all'angolo superiore sinistro dell'immagine trattata come origine dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="2473c-556">Point relative to upper left corner of the image that is treated as the origin of the image.</span></span> <span data-ttu-id="2473c-557">Il valore predefinito è il centro dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="2473c-557">Default is the center of the image.</span></span> <span data-ttu-id="2473c-558">Il vettore è una frazione (da 0,0 a 1,0) della larghezza e dell'altezza dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="2473c-558">The vector is a fraction (from 0.0 to 1.0) of the image's width and height.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-559">Posizione</span><span class="sxs-lookup"><span data-stu-id="2473c-559">Position</span></span></td>
<td><span data-ttu-id="2473c-560"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-560"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="2473c-561">Puntare il rettangolo di riferimento della forma per posizionare l'origine dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="2473c-561">Point in the reference rectangle of the shape to position the origin of the image.</span></span> <span data-ttu-id="2473c-562">Il valore predefinito è il centro del rettangolo del contenitore.</span><span class="sxs-lookup"><span data-stu-id="2473c-562">Default is the center of the container rectangle.</span></span> <span data-ttu-id="2473c-563">Il vettore è una frazione (0,0-1,0) della larghezza e dell'altezza dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="2473c-563">The vector is a fraction (0.0 - 1.0) of the image's width and height.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-564">Dimensione</span><span class="sxs-lookup"><span data-stu-id="2473c-564">Size</span></span></td>
<td><span data-ttu-id="2473c-565"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-565"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="2473c-566">Dimensione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="2473c-566">The size of the image.</span></span> <span data-ttu-id="2473c-567">Il valore predefinito è la dimensione in pixel dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="2473c-567">Default is pixel size of the image.</span></span> <span data-ttu-id="2473c-568">Può essere specificato in coordinate assolute o in percentuale.</span><span class="sxs-lookup"><span data-stu-id="2473c-568">May be specified in absolute coordinates or percentage.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-569">Src</span><span class="sxs-lookup"><span data-stu-id="2473c-569">Src</span></span></td>
<td><span data-ttu-id="2473c-570"><a href="#data-types-used-in-the-vml-object-model">Stringa</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-570"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="2473c-571">URL di un'immagine da caricare per le compilazioni di immagini e modelli.</span><span class="sxs-lookup"><span data-stu-id="2473c-571">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="2473c-572">Questo attributo deve essere sempre presente e puntare a dati di immagine validi affinché venga visualizzata un'immagine.</span><span class="sxs-lookup"><span data-stu-id="2473c-572">This attribute must always be present and point to valid image data for a picture to appear.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-573">Tipo</span><span class="sxs-lookup"><span data-stu-id="2473c-573">Type</span></span></td>
<td><span data-ttu-id="2473c-574">VgFillType.</span><span class="sxs-lookup"><span data-stu-id="2473c-574">VgFillType.</span></span> <span data-ttu-id="2473c-575">indicati di seguito.</span><span class="sxs-lookup"><span data-stu-id="2473c-575">May be one of the following types:</span></span>
<ul>
<li><span data-ttu-id="2473c-576">Sfondo</span><span class="sxs-lookup"><span data-stu-id="2473c-576">Background</span></span></li>
<li><span data-ttu-id="2473c-577">Frame</span><span class="sxs-lookup"><span data-stu-id="2473c-577">Frame</span></span></li>
<li><span data-ttu-id="2473c-578">Sfumatura</span><span class="sxs-lookup"><span data-stu-id="2473c-578">Gradient</span></span></li>
<li><span data-ttu-id="2473c-579">GradientCenter</span><span class="sxs-lookup"><span data-stu-id="2473c-579">GradientCenter</span></span></li>
<li><span data-ttu-id="2473c-580">GradientRadial</span><span class="sxs-lookup"><span data-stu-id="2473c-580">GradientRadial</span></span></li>
<li><span data-ttu-id="2473c-581">GradientTitle</span><span class="sxs-lookup"><span data-stu-id="2473c-581">GradientTitle</span></span></li>
<li><span data-ttu-id="2473c-582">GradientUnscaled</span><span class="sxs-lookup"><span data-stu-id="2473c-582">GradientUnscaled</span></span></li>
<li><span data-ttu-id="2473c-583">Modello</span><span class="sxs-lookup"><span data-stu-id="2473c-583">Pattern</span></span></li>
<li><span data-ttu-id="2473c-584">Tinta unita</span><span class="sxs-lookup"><span data-stu-id="2473c-584">Solid</span></span></li>
<li><span data-ttu-id="2473c-585">Tile</span><span class="sxs-lookup"><span data-stu-id="2473c-585">Tile</span></span></li>
</ul>
<span data-ttu-id="2473c-586">Il riquadro, il pattern e il frame richiedono gli attributi di immagine da fornire.</span><span class="sxs-lookup"><span data-stu-id="2473c-586">Tile, Pattern, and Frame require the image attributes to be supplied.</span></span> <span data-ttu-id="2473c-587">Gradient e GradientRadial richiedono che vengano forniti gli attributi di sfumatura.</span><span class="sxs-lookup"><span data-stu-id="2473c-587">Gradient and GradientRadial require the gradient attributes to be supplied.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="group-element"></a><span data-ttu-id="2473c-588">Group - elemento</span><span class="sxs-lookup"><span data-stu-id="2473c-588">Group element</span></span>

<span data-ttu-id="2473c-589">Un gruppo è una raccolta di forme singole che possono essere posizionate e trasformate come unità.</span><span class="sxs-lookup"><span data-stu-id="2473c-589">A group is a collection of individual shapes that can be positioned and transformed as a unit.</span></span>



|        |                                                                                              |
|--------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2473c-590">Elemento</span><span class="sxs-lookup"><span data-stu-id="2473c-590">Item</span></span>   | <span data-ttu-id="2473c-591">[IVgShape](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-591">[IVgShape](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="2473c-592">Elemento specificato nella matrice di forme.</span><span class="sxs-lookup"><span data-stu-id="2473c-592">Specified item in the array of shapes.</span></span> |
| <span data-ttu-id="2473c-593">Length</span><span class="sxs-lookup"><span data-stu-id="2473c-593">Length</span></span> | <span data-ttu-id="2473c-594">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-594">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="2473c-595">Numero di forme in questo gruppo.</span><span class="sxs-lookup"><span data-stu-id="2473c-595">Number of shapes in this group.</span></span>         |



 

### <a name="imagedata-element"></a><span data-ttu-id="2473c-596">Elemento ImageData</span><span class="sxs-lookup"><span data-stu-id="2473c-596">Imagedata element</span></span>

<span data-ttu-id="2473c-597">Descrive un'immagine di cui eseguire il rendering su una forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-597">Describes a picture to be rendered on top of a shape.</span></span>



|             |                                                                                                                                                                                                                                                                                                                                                                 |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2473c-598">Bilivello</span><span class="sxs-lookup"><span data-stu-id="2473c-598">BiLevel</span></span>     | <span data-ttu-id="2473c-599">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-599">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="2473c-600">Visualizza l'immagine solo in due colori, in genere nero e bianco.</span><span class="sxs-lookup"><span data-stu-id="2473c-600">Display picture in only two colors (usually black and white).</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="2473c-601">BlackLevel</span><span class="sxs-lookup"><span data-stu-id="2473c-601">BlackLevel</span></span>  | <span data-ttu-id="2473c-602">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-602">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="2473c-603">Consente la regolazione per impostare il livello in modo che i neri appaiano come veri neri e tutti gli altri colori siano visibili come ombreggiatura sopra il nero.</span><span class="sxs-lookup"><span data-stu-id="2473c-603">Allows adjustment to set the level so that blacks appear as true blacks, and all other colors are visible as shades above black.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="2473c-604">Chromakey</span><span class="sxs-lookup"><span data-stu-id="2473c-604">Chromakey</span></span>   | <span data-ttu-id="2473c-605">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-605">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="2473c-606">Colore trasparente dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="2473c-606">Transparent color of picture.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="2473c-607">CropBottom</span><span class="sxs-lookup"><span data-stu-id="2473c-607">CropBottom</span></span>  | <span data-ttu-id="2473c-608">[VgNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-608">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="2473c-609">Distanza di ritaglio dalla parte inferiore dell'immagine espressa come percentuale delle dimensioni dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="2473c-609">Crop distance from bottom of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="2473c-610">CropLeft</span><span class="sxs-lookup"><span data-stu-id="2473c-610">CropLeft</span></span>    | <span data-ttu-id="2473c-611">[VgNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-611">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="2473c-612">Distanza di ritaglio dal bordo sinistro dell'immagine espressa come frazione delle dimensioni dell'immagine (da 0,0 a 1,0).</span><span class="sxs-lookup"><span data-stu-id="2473c-612">Crop distance from left edge of picture expressed as a fraction of picture size (from 0.0 to 1.0).</span></span> <span data-ttu-id="2473c-613">Tuttavia, il "out-ritaglio" è supportato e pertanto sono supportati i valori minori di 0 e maggiori di 1. ad esempio,-5, 20 dovrebbe ritagliare i limiti 25X le dimensioni dell'immagine con 4/5 su un lato dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="2473c-613">However, "out-cropping" is supported and thus values of less than 0 and greater than 1 are supported; e.g., -5, 20 would out-crop the bounds 25X the picture size with 4/5 on one side of the picture.</span></span> |
| <span data-ttu-id="2473c-614">CropRight</span><span class="sxs-lookup"><span data-stu-id="2473c-614">CropRight</span></span>   | <span data-ttu-id="2473c-615">[VgNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-615">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="2473c-616">Distanza di ritaglio rispetto a destra dell'immagine espressa come percentuale delle dimensioni dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="2473c-616">Crop distance from right of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="2473c-617">CropTop</span><span class="sxs-lookup"><span data-stu-id="2473c-617">CropTop</span></span>     | <span data-ttu-id="2473c-618">[VgNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-618">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="2473c-619">Distanza di ritaglio dalla parte superiore dell'immagine espressa come percentuale delle dimensioni dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="2473c-619">Crop distance from top of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="2473c-620">EmbossColor</span><span class="sxs-lookup"><span data-stu-id="2473c-620">EmbossColor</span></span> | <span data-ttu-id="2473c-621">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-621">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="2473c-622">Questa proprietà è impostata su una percentuale del colore di ombreggiatura per creare un effetto immagine in rilievo.</span><span class="sxs-lookup"><span data-stu-id="2473c-622">This is set to a percentage of the shadow color to create an embossed picture effect.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="2473c-623">Ottenere</span><span class="sxs-lookup"><span data-stu-id="2473c-623">Gain</span></span>        | <span data-ttu-id="2473c-624">[VgPositiveNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-624">[VgPositiveNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="2473c-625">Regola l'intensità di tutti i colori.</span><span class="sxs-lookup"><span data-stu-id="2473c-625">Adjusts the intensity of all colors.</span></span> <span data-ttu-id="2473c-626">In sostanza, imposta la luminosità del bianco.</span><span class="sxs-lookup"><span data-stu-id="2473c-626">Essentially sets how bright white will be.</span></span> <span data-ttu-id="2473c-627">È compreso tra 0 e 32767.</span><span class="sxs-lookup"><span data-stu-id="2473c-627">Ranges from 0 to 32767.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="2473c-628">Gamma</span><span class="sxs-lookup"><span data-stu-id="2473c-628">Gamma</span></span>       | <span data-ttu-id="2473c-629">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-629">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="2473c-630">Correzione gamma.</span><span class="sxs-lookup"><span data-stu-id="2473c-630">Gamma correction.</span></span> <span data-ttu-id="2473c-631">Aumentando il numero di immagini, si ottiene un contrasto maggiore.</span><span class="sxs-lookup"><span data-stu-id="2473c-631">Increasing it gives an image more contrast.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="2473c-632">GrayScale</span><span class="sxs-lookup"><span data-stu-id="2473c-632">GrayScale</span></span>   | <span data-ttu-id="2473c-633">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-633">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="2473c-634">Visualizza l'immagine nei colori in scala di grigi.</span><span class="sxs-lookup"><span data-stu-id="2473c-634">Display picture in grayscale colors.</span></span>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="2473c-635">Src</span><span class="sxs-lookup"><span data-stu-id="2473c-635">Src</span></span>         | <span data-ttu-id="2473c-636">[Stringa](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-636">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="2473c-637">URL di un'immagine da caricare per le compilazioni di immagini e modelli.</span><span class="sxs-lookup"><span data-stu-id="2473c-637">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="2473c-638">Questo attributo deve essere sempre presente e puntare a dati di immagine validi affinché venga visualizzata un'immagine.</span><span class="sxs-lookup"><span data-stu-id="2473c-638">This attribute must always be present and point to valid image data for a picture to appear.</span></span>                                                                                                                                                           |



 

### <a name="path-element"></a><span data-ttu-id="2473c-639">Path - elemento</span><span class="sxs-lookup"><span data-stu-id="2473c-639">Path element</span></span>

<span data-ttu-id="2473c-640">Definisce il percorso che costituisce la forma, usando una stringa che contiene un set completo di comandi "movimento penna".</span><span class="sxs-lookup"><span data-stu-id="2473c-640">Defines the path that makes up the shape, using a string that contains a rich set of "pen movement" commands.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2473c-641">Limousine</span><span class="sxs-lookup"><span data-stu-id="2473c-641">Limo</span></span></td>
<td><span data-ttu-id="2473c-642"><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-642"><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>.</span></span> <span data-ttu-id="2473c-643">Definisce il punto in cui la forma è allungata. ad esempio, per una forma giraffa, il punto di limo si trova sul collo in modo che quando la forma viene ridimensionata, il collo si estenderà e il resto della forma manterrà le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="2473c-643">Defines the point where the shape is stretched; e.g., for a giraffe shape, the limo point would be on the neck so when the shape is resized, the neck will stretch and the rest of the shape will maintain its dimensions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-644">TextBoxRect</span><span class="sxs-lookup"><span data-stu-id="2473c-644">TextBoxRect</span></span></td>
<td><span data-ttu-id="2473c-645"><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-645"><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>.</span></span> <span data-ttu-id="2473c-646">Matrice contenente i rettangoli che definiscono la posizione in cui deve essere inserito il testo.</span><span class="sxs-lookup"><span data-stu-id="2473c-646">Array containing the rectangles that define where text should go.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-647">V</span><span class="sxs-lookup"><span data-stu-id="2473c-647">V</span></span></td>
<td><span data-ttu-id="2473c-648"><a href="#data-types-used-in-the-vml-object-model">Stringa</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-648"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="2473c-649">Corrisponde all'attributo v nel tag Path.</span><span class="sxs-lookup"><span data-stu-id="2473c-649">Matches the v attribute on the Path tag.</span></span> <span data-ttu-id="2473c-650">Si noti che il percorso può corrispondere all'attributo o all'elemento Path.</span><span class="sxs-lookup"><span data-stu-id="2473c-650">Note that path may correspond to Path attribute or element.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-651">Valore</span><span class="sxs-lookup"><span data-stu-id="2473c-651">Value</span></span></td>
<td><span data-ttu-id="2473c-652"><a href="#data-types-used-in-the-vml-object-model">Stringa</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-652"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="2473c-653">Rappresentazione testuale dei comandi che definiscono il percorso.</span><span class="sxs-lookup"><span data-stu-id="2473c-653">A text representation of the commands that define the path.</span></span> <span data-ttu-id="2473c-654">I valori delle coordinate X o y possono essere un riferimento a una formula nel formato &quot; @# &quot; dove # è il numero ordinale della formula, ad esempio &quot; . @2 &quot;</span><span class="sxs-lookup"><span data-stu-id="2473c-654">X or y-coordinate values can be a reference to a formula in the form &quot;@#&quot; where # is the formula's ordinal number, e.g., &quot;@2&quot;.</span></span> <span data-ttu-id="2473c-655">Questa stringa di attributo è costituita da un set completo di comandi, inclusi i seguenti:</span><span class="sxs-lookup"><span data-stu-id="2473c-655">This attribute string is made up of a rich set of commands including the following:</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2473c-656">Comando</span><span class="sxs-lookup"><span data-stu-id="2473c-656">Command</span></span></th>
<th><span data-ttu-id="2473c-657">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2473c-657">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2473c-658">AE (angleellipseto)</span><span class="sxs-lookup"><span data-stu-id="2473c-658">ae (angleellipseto)</span></span></td>
<td><span data-ttu-id="2473c-659"><strong>dimensioni</strong> <strong>centrali</strong>(x, y) (w, h) <strong>Inizio-angolo</strong>, <strong>angolo finale</strong></span><span class="sxs-lookup"><span data-stu-id="2473c-659"><strong>center</strong>(x,y) <strong>size</strong>(w,h) <strong>start-angle</strong>, <strong>end-angle</strong></span></span><br/> <span data-ttu-id="2473c-660">Creare un segmento di un'ellisse.</span><span class="sxs-lookup"><span data-stu-id="2473c-660">Draw a segment of an ellipse.</span></span> <span data-ttu-id="2473c-661">Viene disegnata una linea retta dal punto corrente al punto iniziale del segmento.</span><span class="sxs-lookup"><span data-stu-id="2473c-661">A straight line is drawn from the current point to the start point of the segment.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-662">al (angleelipse)</span><span class="sxs-lookup"><span data-stu-id="2473c-662">al (angleelipse)</span></span></td>
<td><span data-ttu-id="2473c-663">Uguale a AE ad eccezione del fatto che esiste un m implicito al punto iniziale del segmento.</span><span class="sxs-lookup"><span data-stu-id="2473c-663">Same as ae except that there is an implied m to the starting point of the segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-664">AR (Arc)</span><span class="sxs-lookup"><span data-stu-id="2473c-664">ar (arc)</span></span></td>
<td><span data-ttu-id="2473c-665">Uguale a.</span><span class="sxs-lookup"><span data-stu-id="2473c-665">Same as at.</span></span> <span data-ttu-id="2473c-666">Tuttavia, un nuovo sottopercorso viene avviato da un m implicito al punto iniziale dell'arco.</span><span class="sxs-lookup"><span data-stu-id="2473c-666">However, a new subpath is started by an implied m to the start point of the arc.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-667">all'indirizzo (ArcTo)</span><span class="sxs-lookup"><span data-stu-id="2473c-667">at (arcto)</span></span></td>
<td><span data-ttu-id="2473c-668"><strong>Left</strong>, <strong>Top</strong>, <strong>right</strong>, <strong>Bottom</strong>, <strong>Start</strong>(x, y) <strong>end</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="2473c-668"><strong>left</strong>, <strong>top</strong>, <strong>right</strong>, <strong>bottom</strong>, <strong>start</strong>(x,y) <strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="2473c-669">I primi quattro valori definiscono il rettangolo di delimitazione di un'ellisse.</span><span class="sxs-lookup"><span data-stu-id="2473c-669">The first four values define the bounding box of an ellipse.</span></span> <span data-ttu-id="2473c-670">Le ultime quattro definiscono due vettori radiali.</span><span class="sxs-lookup"><span data-stu-id="2473c-670">The last four define two radial vectors.</span></span> <span data-ttu-id="2473c-671">Viene disegnato un segmento dell'ellisse che inizia in corrispondenza dell'angolo definito dal vettore RADIUS iniziale e termina in corrispondenza dell'angolo definito dal vettore finale.</span><span class="sxs-lookup"><span data-stu-id="2473c-671">A segment of the ellipse is drawn that starts at the angle defined by the start radius vector and ends at the angle defined by the end vector.</span></span> <span data-ttu-id="2473c-672">Viene disegnata una linea retta dal punto corrente all'inizio dell'arco. L'arco viene sempre disegnato in senso antiorario.</span><span class="sxs-lookup"><span data-stu-id="2473c-672">A straight line is drawn from the current point to the start of the arc. The arc is always drawn in a counterclockwise direction.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-673">c (curveTo)</span><span class="sxs-lookup"><span data-stu-id="2473c-673">c (curveto)</span></span></td>
<td><span data-ttu-id="2473c-674"><strong>Control1</strong>(x, y) <strong>controllo2</strong>(x, y) <strong>a</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="2473c-674"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>to</strong>(x,y)</span></span> <br/> <span data-ttu-id="2473c-675">Consente di creare una curva di Bezier cubica dal punto corrente alla coordinata fornita dai due parametri finali, ovvero i punti di controllo forniti dai primi quattro parametri.</span><span class="sxs-lookup"><span data-stu-id="2473c-675">Draw a cubic bezier curve from the current point to the coordinate given by the final two parameters, the control points given by the first four parameters.</span></span> <span data-ttu-id="2473c-676">Il punto corrente diventa l'endpoint di Bezier.</span><span class="sxs-lookup"><span data-stu-id="2473c-676">The current point becomes the endpoint of the bezier.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-677">e (fine)</span><span class="sxs-lookup"><span data-stu-id="2473c-677">e (end)</span></span></td>
<td><span data-ttu-id="2473c-678">Termina il set corrente di sottopercorsi.</span><span class="sxs-lookup"><span data-stu-id="2473c-678">End the current set of subpaths.</span></span> <span data-ttu-id="2473c-679">Un set specificato di sottopercorsi (delimitati da end) viene riempito usando eofill.</span><span class="sxs-lookup"><span data-stu-id="2473c-679">A given set of subpaths (as delimited by end) are filled using eofill.</span></span> <span data-ttu-id="2473c-680">I set successivi di sottopercorsi vengono compilati in modo indipendente e sovrapposti a quelli esistenti.</span><span class="sxs-lookup"><span data-stu-id="2473c-680">Subsequent sets of subpaths are filled independently and superimposed on existing ones.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-681">l (LineTo)</span><span class="sxs-lookup"><span data-stu-id="2473c-681">l (lineto)</span></span></td>
<td><span data-ttu-id="2473c-682">x, y</span><span class="sxs-lookup"><span data-stu-id="2473c-682">x,y</span></span><br/> <span data-ttu-id="2473c-683">Consente di creare una linea dal punto corrente alla coordinata x, y specificata, che diventa il nuovo punto corrente.</span><span class="sxs-lookup"><span data-stu-id="2473c-683">Draw a line from the current point to the given x,y-coordinate, which becomes the new current point.</span></span> <span data-ttu-id="2473c-684">È possibile specificare coppie di coordinate aggiuntive per formare una polilinea, ad esempio &quot; l 10, 13, 45, 27, 89,-12 &quot; .</span><span class="sxs-lookup"><span data-stu-id="2473c-684">Additional coordinate pairs may be specified to form a polyline, e.g., &quot;l 10,13,45,27,89,-12&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-685">m (MoveTo)</span><span class="sxs-lookup"><span data-stu-id="2473c-685">m (moveto)</span></span></td>
<td><span data-ttu-id="2473c-686">x, y</span><span class="sxs-lookup"><span data-stu-id="2473c-686">x,y</span></span><br/> <span data-ttu-id="2473c-687">Avvia un nuovo sottopercorso in corrispondenza della coordinata x, y specificata.</span><span class="sxs-lookup"><span data-stu-id="2473c-687">Start a new subpath at the given x,y-coordinate.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-688">NF (NoFill)</span><span class="sxs-lookup"><span data-stu-id="2473c-688">nf (nofill)</span></span></td>
<td><span data-ttu-id="2473c-689">Il set corrente di sottopercorsi (delimitati da end) non verrà compilato.</span><span class="sxs-lookup"><span data-stu-id="2473c-689">The current set of subpaths (delimited by end) will not be filled.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-690">NS (noStroke)</span><span class="sxs-lookup"><span data-stu-id="2473c-690">ns (nostroke)</span></span></td>
<td><span data-ttu-id="2473c-691">Il set corrente di sottopercorsi (delimitati da end) non verrà tracciato.</span><span class="sxs-lookup"><span data-stu-id="2473c-691">The current set of subpaths (delimited by end) will not be stroked.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-692">QB (quadraticbezier)</span><span class="sxs-lookup"><span data-stu-id="2473c-692">qb (quadraticbezier)</span></span></td>
<td><span data-ttu-id="2473c-693">(<strong>ControlPoint</strong>(x, y)) \*,<strong>end</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="2473c-693">(<strong>controlpoint</strong>(x, y))\*,<strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="2473c-694">Definisce una o più curve di Bézier quadratiche per mezzo di punti di controllo e un endpoint.</span><span class="sxs-lookup"><span data-stu-id="2473c-694">Defines one or more quadratic bezier curves by means of control points and an endpoint.</span></span> <span data-ttu-id="2473c-695">I punti intermedi (su curva) sono ottenuti dall'interpolazione tra punti di controllo successivi simili a tipi di carattere TrueType.</span><span class="sxs-lookup"><span data-stu-id="2473c-695">Intermediate (on-curve) points are obtained by interpolation between successive control points similar to TrueType fonts.</span></span> <span data-ttu-id="2473c-696">Il sottopercorso non deve essere un inizio, nel qual caso il sottopercorso viene chiuso e l'ultimo punto definisce il punto iniziale.</span><span class="sxs-lookup"><span data-stu-id="2473c-696">The subpath need not be a start, in which case the subpath is closed and the last point defines the start point.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-697">QX (ellipticalquadrantx)</span><span class="sxs-lookup"><span data-stu-id="2473c-697">qx (ellipticalquadrantx)</span></span></td>
<td><span data-ttu-id="2473c-698"><strong>fine</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="2473c-698"><strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="2473c-699">Viene disegnato un ellisse del trimestre dal punto corrente all'endpoint specificato.</span><span class="sxs-lookup"><span data-stu-id="2473c-699">A quarter ellipse is drawn from the current point to the given endpoint.</span></span> <span data-ttu-id="2473c-700">Il segmento ellittico è inizialmente tangente a una linea parallela all'asse x. ovvero, il segmento inizia orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="2473c-700">The elliptical segment is initially tangential to a line parallel to the x-axis; i.e., the segment starts out horizontal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-701">QY (ellipticalquadranty)</span><span class="sxs-lookup"><span data-stu-id="2473c-701">qy (ellipticalquadranty)</span></span></td>
<td><span data-ttu-id="2473c-702"><strong>fine</strong>(x, y)</span><span class="sxs-lookup"><span data-stu-id="2473c-702"><strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="2473c-703">Uguale a QX, ad eccezione del fatto che il segmento ellittico è inizialmente tangente a una linea parallela all'asse y. ovvero, il segmento inizia verticalmente.</span><span class="sxs-lookup"><span data-stu-id="2473c-703">Same as qx except that the elliptical segment is initially tangential to a line parallel to the y-axis; i.e., the segment starts out vertical.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-704">r (rlineto)</span><span class="sxs-lookup"><span data-stu-id="2473c-704">r (rlineto)</span></span></td>
<td><span data-ttu-id="2473c-705">x, y</span><span class="sxs-lookup"><span data-stu-id="2473c-705">x,y</span></span> <br/> <span data-ttu-id="2473c-706">Consente di creare una linea dal punto corrente alla coordinata relativa (CPX + x, CPY + y).</span><span class="sxs-lookup"><span data-stu-id="2473c-706">Draw a line from the current point to the relative coordinate (cpx + x, cpy + y).</span></span> <span data-ttu-id="2473c-707">Se vengono fornite coppie di coordinate aggiuntive, ogni nuovo punto viene calcolato in relazione all'ultima.</span><span class="sxs-lookup"><span data-stu-id="2473c-707">If additional coordinate pairs are given, each new point is computed relative to the last one.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-708">t (rmoveto)</span><span class="sxs-lookup"><span data-stu-id="2473c-708">t (rmoveto)</span></span></td>
<td><span data-ttu-id="2473c-709">x, y</span><span class="sxs-lookup"><span data-stu-id="2473c-709">x,y</span></span><br/> <span data-ttu-id="2473c-710">Avviare un nuovo sottopercorso in corrispondenza delle coordinate relative (CPX + x, CPY + y) dove CPX, CPY è la posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="2473c-710">Start a new subpath at the relative coordinates ( cpx + x, cpy + y) where cpx, cpy is the current position.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-711">v (curveTo)</span><span class="sxs-lookup"><span data-stu-id="2473c-711">v (curveto)</span></span></td>
<td><span data-ttu-id="2473c-712"><strong>Control1</strong>(x, y) <strong>controllo2</strong>(x, y) <strong>a</strong> (x, y)</span><span class="sxs-lookup"><span data-stu-id="2473c-712"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>to</strong> (x,y)</span></span> <br/> <span data-ttu-id="2473c-713">Curva di Bezier cubica usando le coordinate specificate rispetto al punto corrente.</span><span class="sxs-lookup"><span data-stu-id="2473c-713">Cubic bezier curve using the given coordinates relative to the current point.</span></span> <span data-ttu-id="2473c-714">Tutti i punti vengono calcolati in relazione allo stesso punto di partenza.</span><span class="sxs-lookup"><span data-stu-id="2473c-714">All the points are computed relative to the same starting point.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-715">WA (clockwisearcto)</span><span class="sxs-lookup"><span data-stu-id="2473c-715">wa (clockwisearcto)</span></span></td>
<td><span data-ttu-id="2473c-716">Uguale a, ma l'arco viene disegnato in senso orario.</span><span class="sxs-lookup"><span data-stu-id="2473c-716">Same as at but the arc is drawn in a clockwise direction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-717">WR (clockwisearc)</span><span class="sxs-lookup"><span data-stu-id="2473c-717">wr (clockwisearc)</span></span></td>
<td><span data-ttu-id="2473c-718">Uguale a AR ma viene disegnato in senso orario.</span><span class="sxs-lookup"><span data-stu-id="2473c-718">Same as ar but is drawn in a clockwise direction.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-719">x (Chiudi)</span><span class="sxs-lookup"><span data-stu-id="2473c-719">x (close)</span></span></td>
<td><span data-ttu-id="2473c-720">Chiudere il sottopercorso corrente disegnando una linea retta dal punto corrente al punto MoveTo originale.</span><span class="sxs-lookup"><span data-stu-id="2473c-720">Close the current subpath by drawing a straight line from the current point to the original moveto point.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="shadow-element"></a><span data-ttu-id="2473c-721">Elemento Shadow</span><span class="sxs-lookup"><span data-stu-id="2473c-721">Shadow element</span></span>

<span data-ttu-id="2473c-722">Descrive un effetto ombreggiatura su una forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-722">Describes a shadow effect on a shape.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2473c-723">Colore</span><span class="sxs-lookup"><span data-stu-id="2473c-723">Color</span></span></td>
<td><span data-ttu-id="2473c-724"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-724"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="2473c-725">Colore dell'ombreggiatura primaria.</span><span class="sxs-lookup"><span data-stu-id="2473c-725">Color of the primary shadow.</span></span> <span data-ttu-id="2473c-726">Il valore predefinito è RGB (128128128)</span><span class="sxs-lookup"><span data-stu-id="2473c-726">Default is RGB(128,128,128)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-727">Color2</span><span class="sxs-lookup"><span data-stu-id="2473c-727">Color2</span></span></td>
<td><span data-ttu-id="2473c-728"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-728"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="2473c-729">Colore della seconda ombreggiatura o evidenziazione in un'ombreggiatura goffrata o incisa.</span><span class="sxs-lookup"><span data-stu-id="2473c-729">Color of the second shadow, or highlight in an embossed or engraved shadow.</span></span> <span data-ttu-id="2473c-730">Il valore predefinito è RGB (203203203).</span><span class="sxs-lookup"><span data-stu-id="2473c-730">Default is RGB(203,203,203).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-731">Matrice</span><span class="sxs-lookup"><span data-stu-id="2473c-731">Matrix</span></span></td>
<td><span data-ttu-id="2473c-732"><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-732"><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix</a>.</span></span> <span data-ttu-id="2473c-733">Una matrice di trasformazione prospettica nel formato &quot; SXX, SXY, SYX, SYY, px, py &quot; [s = scale, p = Perspective].</span><span class="sxs-lookup"><span data-stu-id="2473c-733">A perspective transform matrix in the form, &quot;sxx,sxy,syx,syy,px,py&quot; [s=scale, p=perspective].</span></span> <span data-ttu-id="2473c-734">Gli elementi s specificano il modo in cui deve essere ridimensionata l'ombreggiatura rispetto alla forma e gli elementi p specificano come deve essere inclinata l'ombreggiatura rispetto alla forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-734">The s items specify how the shadow should scale with respect to the shape, and the p items specify how the shadow should skew with respect to the shape.</span></span> <span data-ttu-id="2473c-735">Ad esempio, la matrice seguente ridimensiona la forma in base a un fattore 2 e la inclina per un fattore di 4 in tutte le direzioni:</span><span class="sxs-lookup"><span data-stu-id="2473c-735">For example, the following matrix resizes the shape by a factor of 2 and skews it by a factor of 4 in all directions:</span></span> <br/> <span data-ttu-id="2473c-736">&quot;2, 2, 2, 2, 4, 4&quot;</span><span class="sxs-lookup"><span data-stu-id="2473c-736">&quot;2,2,2,2,4,4&quot;</span></span><br/> <span data-ttu-id="2473c-737">Questa matrice viene utilizzata solo se il tipo dell'ombreggiatura è impostato sulla prospettiva.</span><span class="sxs-lookup"><span data-stu-id="2473c-737">This matrix is only used if the type of the shadow is set to perspective.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-738">Nascosto</span><span class="sxs-lookup"><span data-stu-id="2473c-738">Obscured</span></span></td>
<td><span data-ttu-id="2473c-739"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-739"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="2473c-740">L'ombreggiatura può essere visualizzata se non è presente alcun riempimento della forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-740">The shadow can be seen through if there is no fill on the shape.</span></span> <span data-ttu-id="2473c-741">Il valore predefinito è False.</span><span class="sxs-lookup"><span data-stu-id="2473c-741">Default is False.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-742">Offset</span><span class="sxs-lookup"><span data-stu-id="2473c-742">Offset</span></span></td>
<td><span data-ttu-id="2473c-743"><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-743"><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset</a>.</span></span> <span data-ttu-id="2473c-744">Quantità di offset x, y dalla posizione della forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-744">Amount of x,y offset from the shape's location.</span></span> <span data-ttu-id="2473c-745">Il valore predefinito è &quot; 2PT, 2PT &quot; .</span><span class="sxs-lookup"><span data-stu-id="2473c-745">Default is &quot;2pt,2pt&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-746">Offset2</span><span class="sxs-lookup"><span data-stu-id="2473c-746">Offset2</span></span></td>
<td><span data-ttu-id="2473c-747"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-747"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="2473c-748">Quantità di offset x, y secondo rispetto alla posizione della forma? s.</span><span class="sxs-lookup"><span data-stu-id="2473c-748">Amount of x,y second offset from the shape?s location.</span></span> <span data-ttu-id="2473c-749">I valori sono una misura assoluta o un valore frazionario della forma (da-0,5 a + 0,5).</span><span class="sxs-lookup"><span data-stu-id="2473c-749">Values are either an absolute measurement, or a fractional value of shape (-0.5 to +0.5).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-750">Attivato</span><span class="sxs-lookup"><span data-stu-id="2473c-750">On</span></span></td>
<td><span data-ttu-id="2473c-751"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-751"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="2473c-752">Attiva e disattiva la visualizzazione dell'ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="2473c-752">Turns the display of the shadow on and off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-753">Opacità</span><span class="sxs-lookup"><span data-stu-id="2473c-753">Opacity</span></span></td>
<td><span data-ttu-id="2473c-754"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-754"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="2473c-755">Opacità dell'effetto di ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="2473c-755">Opacity of the shadow effect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-756">Origine</span><span class="sxs-lookup"><span data-stu-id="2473c-756">Origin</span></span></td>
<td><span data-ttu-id="2473c-757"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Coppia di valori frazionari della forma da-0,5 a + 0,5.</span><span class="sxs-lookup"><span data-stu-id="2473c-757"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> A pair of fractional values of shape from -0.5 to +0.5.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-758">Tipo</span><span class="sxs-lookup"><span data-stu-id="2473c-758">Type</span></span></td>
<td><span data-ttu-id="2473c-759"><a href="#data-types-used-in-the-vml-object-model">VgShadowType</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-759"><a href="#data-types-used-in-the-vml-object-model">VgShadowType</a>.</span></span> <span data-ttu-id="2473c-760">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="2473c-760">Values are:</span></span>
<ul>
<li><span data-ttu-id="2473c-761">Single (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2473c-761">Single (default)</span></span></li>
<li><span data-ttu-id="2473c-762">Double</span><span class="sxs-lookup"><span data-stu-id="2473c-762">Double</span></span></li>
<li><span data-ttu-id="2473c-763">Prospettiva</span><span class="sxs-lookup"><span data-stu-id="2473c-763">Perspective</span></span></li>
<li><span data-ttu-id="2473c-764">ShapeRelative</span><span class="sxs-lookup"><span data-stu-id="2473c-764">ShapeRelative</span></span></li>
<li><span data-ttu-id="2473c-765">DrawingRelative</span><span class="sxs-lookup"><span data-stu-id="2473c-765">DrawingRelative</span></span></li>
<li><span data-ttu-id="2473c-766">Rilievo</span><span class="sxs-lookup"><span data-stu-id="2473c-766">Emboss</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="skew-element"></a><span data-ttu-id="2473c-767">Elemento asimmetria</span><span class="sxs-lookup"><span data-stu-id="2473c-767">Skew element</span></span>

<span data-ttu-id="2473c-768">Descrive un effetto di inclinazione della prospettiva su una forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-768">Describes a perspective skew effect on a shape.</span></span> <span data-ttu-id="2473c-769">L'inclinazione viene applicata ai dati grafici vettoriali, non ai dati di immagine.</span><span class="sxs-lookup"><span data-stu-id="2473c-769">The skew is applied to vector graphic data, not image data.</span></span>



|        |                                                                                                                                                                                                                                                                                    |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2473c-770">Matrice</span><span class="sxs-lookup"><span data-stu-id="2473c-770">Matrix</span></span> | <span data-ttu-id="2473c-771">[IVgSkewMatrix](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-771">[IVgSkewMatrix](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="2473c-772">Una matrice di trasformazione della prospettiva nel formato "SXX, SXY, SYX, SYY, px, py" \[ s = scale, p = Perspective \] .</span><span class="sxs-lookup"><span data-stu-id="2473c-772">A perspective transform matrix in the form, "sxx,sxy,syx,syy,px,py" \[ s=scale, p=perspective\].</span></span> <span data-ttu-id="2473c-773">Se l'offset è in unità assolute, il px, py si trovano in unità Emu ^-1; in caso contrario, si tratta di una frazione inversa della dimensione della forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-773">If offset is in absolute units then px,py are in emu ^ -1 units; otherwise they are an inverse fraction of shape size.</span></span> |
| <span data-ttu-id="2473c-774">Offset</span><span class="sxs-lookup"><span data-stu-id="2473c-774">Offset</span></span> | <span data-ttu-id="2473c-775">[IvgSkewOffset](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-775">[IvgSkewOffset](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="2473c-776">Quantità di offset x, y dalla posizione della forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-776">Amount of x,y offset from the shape's location.</span></span> <span data-ttu-id="2473c-777">Il valore predefinito è "2PT, 2PT".</span><span class="sxs-lookup"><span data-stu-id="2473c-777">Default is "2pt,2pt".</span></span>                                                                                                                                                   |
| <span data-ttu-id="2473c-778">Attivato</span><span class="sxs-lookup"><span data-stu-id="2473c-778">On</span></span>     | <span data-ttu-id="2473c-779">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-779">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="2473c-780">Attiva o disattiva la visualizzazione della distorsione.</span><span class="sxs-lookup"><span data-stu-id="2473c-780">Turns the display of the skew on or off.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="2473c-781">Origine</span><span class="sxs-lookup"><span data-stu-id="2473c-781">Origin</span></span> | <span data-ttu-id="2473c-782">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-782">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="2473c-783">Coppia di valori frazionari della forma da-0,5 a + 0,5.</span><span class="sxs-lookup"><span data-stu-id="2473c-783">A pair of fractional values of shape from -0.5 to +0.5.</span></span>                                                                                                                                                                     |



 

### <a name="stroke-element"></a><span data-ttu-id="2473c-784">Stroke-elemento</span><span class="sxs-lookup"><span data-stu-id="2473c-784">Stroke element</span></span>

<span data-ttu-id="2473c-785">Viene descritto come tracciare il percorso se si desidera un elemento che supera una linea continua con un colore a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="2473c-785">Describes how to draw the path if something beyond a solid line with a solid color is desired.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2473c-786">Colore</span><span class="sxs-lookup"><span data-stu-id="2473c-786">Color</span></span></td>
<td><span data-ttu-id="2473c-787"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-787"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="2473c-788">Colore della linea.</span><span class="sxs-lookup"><span data-stu-id="2473c-788">The color of the line.</span></span> <span data-ttu-id="2473c-789">Uguale all'attributo StrokeColor nella forma, ma ne esegue l'override.</span><span class="sxs-lookup"><span data-stu-id="2473c-789">Same as StrokeColor attribute in Shape but overrides it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-790">Color2</span><span class="sxs-lookup"><span data-stu-id="2473c-790">Color2</span></span></td>
<td><span data-ttu-id="2473c-791"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-791"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="2473c-792">Colore secondario.</span><span class="sxs-lookup"><span data-stu-id="2473c-792">Secondary color.</span></span> <span data-ttu-id="2473c-793">Utilizzato quando elemento FillType è pattern.</span><span class="sxs-lookup"><span data-stu-id="2473c-793">Used when FillType is Pattern.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-794">DashStyle</span><span class="sxs-lookup"><span data-stu-id="2473c-794">DashStyle</span></span></td>
<td><span data-ttu-id="2473c-795"><strong>VgLineDashStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="2473c-795"><strong>VgLineDashStyle</strong>.</span></span> <span data-ttu-id="2473c-796">Formato di stile Dash.</span><span class="sxs-lookup"><span data-stu-id="2473c-796">Dash style format.</span></span> <span data-ttu-id="2473c-797">Può essere un valore specifico o una sequenza di numeri con un modello Dash definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="2473c-797">May be a specific value or a sequence of numbers with a user-defined dash pattern.</span></span> <span data-ttu-id="2473c-798">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="2473c-798">Values are:</span></span>
<ul>
<li><span data-ttu-id="2473c-799">Solid (valore predefinito)</span><span class="sxs-lookup"><span data-stu-id="2473c-799">Solid (default)</span></span></li>
<li><span data-ttu-id="2473c-800">ShortDash</span><span class="sxs-lookup"><span data-stu-id="2473c-800">ShortDash</span></span></li>
<li><span data-ttu-id="2473c-801">ShortDot</span><span class="sxs-lookup"><span data-stu-id="2473c-801">ShortDot</span></span></li>
<li><span data-ttu-id="2473c-802">ShortDashDot</span><span class="sxs-lookup"><span data-stu-id="2473c-802">ShortDashDot</span></span></li>
<li><span data-ttu-id="2473c-803">ShortDashDotDot</span><span class="sxs-lookup"><span data-stu-id="2473c-803">ShortDashDotDot</span></span></li>
<li><span data-ttu-id="2473c-804">Punto</span><span class="sxs-lookup"><span data-stu-id="2473c-804">Dot</span></span></li>
<li><span data-ttu-id="2473c-805">Trattino</span><span class="sxs-lookup"><span data-stu-id="2473c-805">Dash</span></span></li>
<li><span data-ttu-id="2473c-806">DashDot</span><span class="sxs-lookup"><span data-stu-id="2473c-806">DashDot</span></span></li>
<li><span data-ttu-id="2473c-807">LongDash</span><span class="sxs-lookup"><span data-stu-id="2473c-807">LongDash</span></span></li>
<li><span data-ttu-id="2473c-808">LongDashDot</span><span class="sxs-lookup"><span data-stu-id="2473c-808">LongDashDot</span></span></li>
<li><span data-ttu-id="2473c-809">LongDashDotDot</span><span class="sxs-lookup"><span data-stu-id="2473c-809">LongDashDotDot</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-810">EndArrow</span><span class="sxs-lookup"><span data-stu-id="2473c-810">EndArrow</span></span></td>
<td><span data-ttu-id="2473c-811"><strong>VgArrowheadStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="2473c-811"><strong>VgArrowheadStyle</strong>.</span></span> <span data-ttu-id="2473c-812">Freccia per la fine della riga.</span><span class="sxs-lookup"><span data-stu-id="2473c-812">Arrowhead for the end of the line.</span></span> <span data-ttu-id="2473c-813">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="2473c-813">Values are:</span></span>
<ul>
<li><span data-ttu-id="2473c-814">Nessuno (valore predefinito)</span><span class="sxs-lookup"><span data-stu-id="2473c-814">None (default)</span></span></li>
<li><span data-ttu-id="2473c-815">Blocca</span><span class="sxs-lookup"><span data-stu-id="2473c-815">Block</span></span></li>
<li><span data-ttu-id="2473c-816">Classic</span><span class="sxs-lookup"><span data-stu-id="2473c-816">Classic</span></span></li>
<li><span data-ttu-id="2473c-817">Diamond</span><span class="sxs-lookup"><span data-stu-id="2473c-817">Diamond</span></span></li>
<li><span data-ttu-id="2473c-818">Ovale</span><span class="sxs-lookup"><span data-stu-id="2473c-818">Oval</span></span></li>
<li><span data-ttu-id="2473c-819">Apri</span><span class="sxs-lookup"><span data-stu-id="2473c-819">Open</span></span></li>
<li><span data-ttu-id="2473c-820">Frecce di espansione</span><span class="sxs-lookup"><span data-stu-id="2473c-820">Chevron</span></span></li>
<li><span data-ttu-id="2473c-821">DoubleChevron</span><span class="sxs-lookup"><span data-stu-id="2473c-821">DoubleChevron</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-822">EndArrowLength</span><span class="sxs-lookup"><span data-stu-id="2473c-822">EndArrowLength</span></span></td>
<td><span data-ttu-id="2473c-823"><strong>VgArrowHeadLength</strong>.</span><span class="sxs-lookup"><span data-stu-id="2473c-823"><strong>VgArrowHeadLength</strong>.</span></span> <span data-ttu-id="2473c-824">Lunghezza della freccia per la fine della riga.</span><span class="sxs-lookup"><span data-stu-id="2473c-824">Arrowhead length for the end of the line.</span></span> <span data-ttu-id="2473c-825">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="2473c-825">Values are:</span></span>
<ul>
<li><span data-ttu-id="2473c-826">Short</span><span class="sxs-lookup"><span data-stu-id="2473c-826">Short</span></span></li>
<li><span data-ttu-id="2473c-827">Media (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2473c-827">Medium (default)</span></span></li>
<li><span data-ttu-id="2473c-828">long</span><span class="sxs-lookup"><span data-stu-id="2473c-828">Long</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-829">EndArrowWidth</span><span class="sxs-lookup"><span data-stu-id="2473c-829">EndArrowWidth</span></span></td>
<td><span data-ttu-id="2473c-830"><strong>VgArrowheadWidth</strong>.</span><span class="sxs-lookup"><span data-stu-id="2473c-830"><strong>VgArrowheadWidth</strong>.</span></span> <span data-ttu-id="2473c-831">Larghezza della freccia per la fine della riga.</span><span class="sxs-lookup"><span data-stu-id="2473c-831">Arrowhead width for the end of the line.</span></span> <span data-ttu-id="2473c-832">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="2473c-832">Values are:</span></span>
<ul>
<li><span data-ttu-id="2473c-833">Limitare</span><span class="sxs-lookup"><span data-stu-id="2473c-833">Narrow</span></span></li>
<li><span data-ttu-id="2473c-834">Media (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2473c-834">Medium (default)</span></span></li>
<li><span data-ttu-id="2473c-835">Largo</span><span class="sxs-lookup"><span data-stu-id="2473c-835">Wide</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-836">EndCap</span><span class="sxs-lookup"><span data-stu-id="2473c-836">EndCap</span></span></td>
<td><span data-ttu-id="2473c-837"><strong>VgLineEndCapStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="2473c-837"><strong>VgLineEndCapStyle</strong>.</span></span> <span data-ttu-id="2473c-838">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="2473c-838">Values are:</span></span>
<ul>
<li><span data-ttu-id="2473c-839">Semplice</span><span class="sxs-lookup"><span data-stu-id="2473c-839">Flat</span></span></li>
<li><span data-ttu-id="2473c-840">Square</span><span class="sxs-lookup"><span data-stu-id="2473c-840">Square</span></span></li>
<li><span data-ttu-id="2473c-841">Round</span><span class="sxs-lookup"><span data-stu-id="2473c-841">Round</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-842">Elemento FillType</span><span class="sxs-lookup"><span data-stu-id="2473c-842">FillType</span></span></td>
<td><span data-ttu-id="2473c-843"><strong>VgLineFillType</strong>.</span><span class="sxs-lookup"><span data-stu-id="2473c-843"><strong>VgLineFillType</strong>.</span></span> <span data-ttu-id="2473c-844">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="2473c-844">Values are:</span></span>
<ul>
<li><span data-ttu-id="2473c-845">Solid (valore predefinito)</span><span class="sxs-lookup"><span data-stu-id="2473c-845">Solid (default)</span></span></li>
<li><span data-ttu-id="2473c-846">Tile</span><span class="sxs-lookup"><span data-stu-id="2473c-846">Tile</span></span></li>
<li><span data-ttu-id="2473c-847">Modello</span><span class="sxs-lookup"><span data-stu-id="2473c-847">Pattern</span></span></li>
<li><span data-ttu-id="2473c-848">Frame</span><span class="sxs-lookup"><span data-stu-id="2473c-848">Frame</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-849">ImageAlignShape</span><span class="sxs-lookup"><span data-stu-id="2473c-849">ImageAlignShape</span></span></td>
<td><span data-ttu-id="2473c-850"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-850"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="2473c-851">Allineare l'immagine alla forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-851">Align the image with the shape.</span></span> <span data-ttu-id="2473c-852">Se false, allineare l'immagine con la finestra.</span><span class="sxs-lookup"><span data-stu-id="2473c-852">If False, align image with window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-853">ImageAspect</span><span class="sxs-lookup"><span data-stu-id="2473c-853">ImageAspect</span></span></td>
<td><span data-ttu-id="2473c-854"><strong>VgAspectType</strong>.</span><span class="sxs-lookup"><span data-stu-id="2473c-854"><strong>VgAspectType</strong>.</span></span> <span data-ttu-id="2473c-855">L'attributo ImageSize verrà regolato in modo da mantenere l'aspetto dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="2473c-855">ImageSize attribute will be adjusted to preserve the aspect of the image.</span></span> <span data-ttu-id="2473c-856">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="2473c-856">Values include:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2473c-857">Valore</span><span class="sxs-lookup"><span data-stu-id="2473c-857">Value</span></span></th>
<th><span data-ttu-id="2473c-858">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2473c-858">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2473c-859">Ignora</span><span class="sxs-lookup"><span data-stu-id="2473c-859">Ignore</span></span></td>
<td><span data-ttu-id="2473c-860">Ignorare i problemi di aspetto.</span><span class="sxs-lookup"><span data-stu-id="2473c-860">Ignore aspect issues.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-861">AtLeast</span><span class="sxs-lookup"><span data-stu-id="2473c-861">AtLeast</span></span></td>
<td><span data-ttu-id="2473c-862">L'immagine è almeno uguale alla dimensione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="2473c-862">Image is at least as big as the image size.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-863">AtMost</span><span class="sxs-lookup"><span data-stu-id="2473c-863">AtMost</span></span></td>
<td><span data-ttu-id="2473c-864">L'immagine non è più grande delle dimensioni dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="2473c-864">Image is no bigger than image size.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-865">ImageSize</span><span class="sxs-lookup"><span data-stu-id="2473c-865">ImageSize</span></span></td>
<td><span data-ttu-id="2473c-866"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-866"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="2473c-867">Dimensione dell'immagine con cui formare il pennello.</span><span class="sxs-lookup"><span data-stu-id="2473c-867">Size of the image to form the brush with.</span></span> <span data-ttu-id="2473c-868">Il valore predefinito corrisponde alla dimensione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="2473c-868">Default is the size of the image.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-869">JoinStyle</span><span class="sxs-lookup"><span data-stu-id="2473c-869">JoinStyle</span></span></td>
<td><span data-ttu-id="2473c-870"><strong>VgLineJoinStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="2473c-870"><strong>VgLineJoinStyle</strong>.</span></span> <span data-ttu-id="2473c-871">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="2473c-871">Values are:</span></span>
<ul>
<li><span data-ttu-id="2473c-872">Round (misto arrotondato)</span><span class="sxs-lookup"><span data-stu-id="2473c-872">Round (rounded joint)</span></span></li>
<li><span data-ttu-id="2473c-873">Smussato (misto smussato)</span><span class="sxs-lookup"><span data-stu-id="2473c-873">Bevel (beveled joint)</span></span></li>
<li><span data-ttu-id="2473c-874">Miter (misto smussato)</span><span class="sxs-lookup"><span data-stu-id="2473c-874">Miter (miter joint)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-875">LineStyle</span><span class="sxs-lookup"><span data-stu-id="2473c-875">LineStyle</span></span></td>
<td><span data-ttu-id="2473c-876"><strong>VgLineStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="2473c-876"><strong>VgLineStyle</strong>.</span></span> <span data-ttu-id="2473c-877">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="2473c-877">Values are:</span></span>
<ul>
<li><span data-ttu-id="2473c-878">Single</span><span class="sxs-lookup"><span data-stu-id="2473c-878">Single</span></span></li>
<li><span data-ttu-id="2473c-879">ThinThin (1:1:1)</span><span class="sxs-lookup"><span data-stu-id="2473c-879">ThinThin (1:1:1)</span></span></li>
<li><span data-ttu-id="2473c-880">ThinThick (1:1:2)</span><span class="sxs-lookup"><span data-stu-id="2473c-880">ThinThick (1:1:2)</span></span></li>
<li><span data-ttu-id="2473c-881">ThickThin (2:1:1)</span><span class="sxs-lookup"><span data-stu-id="2473c-881">ThickThin (2:1:1)</span></span></li>
<li><span data-ttu-id="2473c-882">ThickBetweenThin (1:1:2:1:1)</span><span class="sxs-lookup"><span data-stu-id="2473c-882">ThickBetweenThin (1:1:2:1:1)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-883">MiterLimit</span><span class="sxs-lookup"><span data-stu-id="2473c-883">MiterLimit</span></span></td>
<td><span data-ttu-id="2473c-884"><a href="msdn-online-vml-vglength.md">Lunghezza</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-884"><a href="msdn-online-vml-vglength.md">Length</a>.</span></span> <span data-ttu-id="2473c-885">Distanza massima tra il punto interno e il punto esterno di una giunzione.</span><span class="sxs-lookup"><span data-stu-id="2473c-885">The maximum distance between the inner point and outer point of a joint.</span></span> <span data-ttu-id="2473c-886">Questo numero è un multiplo dello spessore della linea.</span><span class="sxs-lookup"><span data-stu-id="2473c-886">This number is a multiple of the thickness of the line.</span></span> <span data-ttu-id="2473c-887">È compreso tra 0 e 32.767.</span><span class="sxs-lookup"><span data-stu-id="2473c-887">Ranges from 0 to 32,767.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-888">Attivato</span><span class="sxs-lookup"><span data-stu-id="2473c-888">On</span></span></td>
<td><span data-ttu-id="2473c-889"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-889"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="2473c-890">Attiva e disattiva la visualizzazione della riga.</span><span class="sxs-lookup"><span data-stu-id="2473c-890">Turns the display of the line on and off.</span></span> <span data-ttu-id="2473c-891">Uguale all'attributo Stroke nella forma, ma ne esegue l'override.</span><span class="sxs-lookup"><span data-stu-id="2473c-891">Same as Stroke attribute in Shape but overrides it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-892">Opacità</span><span class="sxs-lookup"><span data-stu-id="2473c-892">Opacity</span></span></td>
<td><span data-ttu-id="2473c-893"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-893"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="2473c-894">Opacità del tratto.</span><span class="sxs-lookup"><span data-stu-id="2473c-894">Opacity of the stroke.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-895">Src</span><span class="sxs-lookup"><span data-stu-id="2473c-895">Src</span></span></td>
<td><span data-ttu-id="2473c-896">Stringa.</span><span class="sxs-lookup"><span data-stu-id="2473c-896">String.</span></span> <span data-ttu-id="2473c-897">URL di un'immagine da caricare per le compilazioni di immagini e modelli.</span><span class="sxs-lookup"><span data-stu-id="2473c-897">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="2473c-898">Questo attributo deve essere sempre presente e puntare a dati di immagine validi affinché venga visualizzata un'immagine.</span><span class="sxs-lookup"><span data-stu-id="2473c-898">This attribute must always be present and point to valid image data for a picture to appear.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-899">StartArrow</span><span class="sxs-lookup"><span data-stu-id="2473c-899">StartArrow</span></span></td>
<td><span data-ttu-id="2473c-900"><strong>VgArrowheadStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="2473c-900"><strong>VgArrowheadStyle</strong>.</span></span> <span data-ttu-id="2473c-901">Freccia per l'inizio della riga.</span><span class="sxs-lookup"><span data-stu-id="2473c-901">Arrowhead for the start of the line.</span></span> <span data-ttu-id="2473c-902">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="2473c-902">Values are:</span></span>
<ul>
<li><span data-ttu-id="2473c-903">Nessuno (valore predefinito)</span><span class="sxs-lookup"><span data-stu-id="2473c-903">None (default)</span></span></li>
<li><span data-ttu-id="2473c-904">Blocca</span><span class="sxs-lookup"><span data-stu-id="2473c-904">Block</span></span></li>
<li><span data-ttu-id="2473c-905">Classic</span><span class="sxs-lookup"><span data-stu-id="2473c-905">Classic</span></span></li>
<li><span data-ttu-id="2473c-906">Diamond</span><span class="sxs-lookup"><span data-stu-id="2473c-906">Diamond</span></span></li>
<li><span data-ttu-id="2473c-907">Ovale</span><span class="sxs-lookup"><span data-stu-id="2473c-907">Oval</span></span></li>
<li><span data-ttu-id="2473c-908">Apri</span><span class="sxs-lookup"><span data-stu-id="2473c-908">Open</span></span></li>
<li><span data-ttu-id="2473c-909">Frecce di espansione</span><span class="sxs-lookup"><span data-stu-id="2473c-909">Chevron</span></span></li>
<li><span data-ttu-id="2473c-910">DoubleChevron</span><span class="sxs-lookup"><span data-stu-id="2473c-910">DoubleChevron</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-911">StartArrowLength</span><span class="sxs-lookup"><span data-stu-id="2473c-911">StartArrowLength</span></span></td>
<td><span data-ttu-id="2473c-912">VgArrowHeadLength.</span><span class="sxs-lookup"><span data-stu-id="2473c-912">VgArrowHeadLength.</span></span> <span data-ttu-id="2473c-913">Lunghezza della freccia per l'inizio della riga.</span><span class="sxs-lookup"><span data-stu-id="2473c-913">Arrowhead length for the start of the line.</span></span> <span data-ttu-id="2473c-914">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="2473c-914">Values are:</span></span>
<ul>
<li><span data-ttu-id="2473c-915">Short</span><span class="sxs-lookup"><span data-stu-id="2473c-915">Short</span></span></li>
<li><span data-ttu-id="2473c-916">Media (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2473c-916">Medium (default)</span></span></li>
<li><span data-ttu-id="2473c-917">long</span><span class="sxs-lookup"><span data-stu-id="2473c-917">Long</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-918">StartArrowWidth</span><span class="sxs-lookup"><span data-stu-id="2473c-918">StartArrowWidth</span></span></td>
<td><span data-ttu-id="2473c-919">VgArrowheadWidth.</span><span class="sxs-lookup"><span data-stu-id="2473c-919">VgArrowheadWidth.</span></span> <span data-ttu-id="2473c-920">Larghezza della freccia per l'inizio della riga.</span><span class="sxs-lookup"><span data-stu-id="2473c-920">Arrowhead width for the start of the line.</span></span> <span data-ttu-id="2473c-921">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="2473c-921">Values are:</span></span>
<ul>
<li><span data-ttu-id="2473c-922">Larghezza media ristretta (predefinita)</span><span class="sxs-lookup"><span data-stu-id="2473c-922">Narrow Medium (default) Wide</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-923">Peso</span><span class="sxs-lookup"><span data-stu-id="2473c-923">Weight</span></span></td>
<td><span data-ttu-id="2473c-924"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-924"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="2473c-925">Larghezza della linea.</span><span class="sxs-lookup"><span data-stu-id="2473c-925">Width of line.</span></span> <span data-ttu-id="2473c-926">È compreso tra 0 e 1584.</span><span class="sxs-lookup"><span data-stu-id="2473c-926">Ranges from 0 to 1584.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="2473c-927">L'attributo DashStyle consente all'utente di specificare un modello Dash definito in modo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="2473c-927">The DashStyle attribute allows the user to specify a custom-defined dash pattern.</span></span> <span data-ttu-id="2473c-928">Questa operazione viene eseguita usando una serie di numeri.</span><span class="sxs-lookup"><span data-stu-id="2473c-928">This is done using a series of numbers.</span></span> <span data-ttu-id="2473c-929">Gli stili Dash sono definiti in termini di lunghezza del trattino (la parte disegnata del tratto) e della lunghezza dello spazio tra i trattini.</span><span class="sxs-lookup"><span data-stu-id="2473c-929">Dash styles are defined in terms of the length of the dash (the drawn part of the stroke) and the length of the space between the dashes.</span></span> <span data-ttu-id="2473c-930">Le lunghezze sono relative alla lunghezza riga; la lunghezza di &quot; 1 &quot; è uguale alla lunghezza della linea.</span><span class="sxs-lookup"><span data-stu-id="2473c-930">The lengths are relative to the line width; a length of &quot;1&quot; is equal to the line width.</span></span> <span data-ttu-id="2473c-931">Lo stile di estremità viene applicato a ogni trattino, mentre gli stili delle frecce non lo sono.</span><span class="sxs-lookup"><span data-stu-id="2473c-931">The EndCap style is applied to each dash, arrow styles are not.</span></span> <span data-ttu-id="2473c-932">La stringa definisce prima di tutto la lunghezza del trattino, quindi la lunghezza dello spazio.</span><span class="sxs-lookup"><span data-stu-id="2473c-932">The string first defines the length of the dash then the length of the space.</span></span> <span data-ttu-id="2473c-933">Questa operazione può essere ripetuta per formare stili trattini complessi.</span><span class="sxs-lookup"><span data-stu-id="2473c-933">This may be repeated to form complex dash styles.</span></span> <span data-ttu-id="2473c-934">La stringa deve sempre contenere una coppia di numeri; Se contiene un numero dispari di numeri, l'ultimo può essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="2473c-934">The string should always contain a pair of numbers; if it contains an odd number of numbers the last may be disregarded.</span></span> <span data-ttu-id="2473c-935">Nella tabella seguente sono elencati alcuni valori tipici e una descrizione dell'effetto desiderato.</span><span class="sxs-lookup"><span data-stu-id="2473c-935">The following table lists some typical values and a description of the intended effect.</span></span> <span data-ttu-id="2473c-936">&quot;0 indica &quot; un punto che dovrebbe essere quadruplo simmetrico (con round estremità deve essere un cerchio).</span><span class="sxs-lookup"><span data-stu-id="2473c-936">&quot;0&quot; implies a dot that should be fourfold symmetrical (with round endcaps it should be a circle).</span></span> <span data-ttu-id="2473c-937">Se il limite di riga è Flat, un visualizzatore deve scegliere un trattino del sistema operativo predefinito, laddove possibile (ad esempio, un elemento che è veloce da creare).</span><span class="sxs-lookup"><span data-stu-id="2473c-937">If the line endcap is Flat, a viewer should choose a built-in operating system dash where possible (i.e., something that is fast to draw).</span></span> <span data-ttu-id="2473c-938">Di seguito sono riportati alcuni esempi.</span><span class="sxs-lookup"><span data-stu-id="2473c-938">The following shows some examples.</span></span>
</blockquote>
</div>
<div>
 
</div>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2473c-939">&quot;2 2&quot;</span><span class="sxs-lookup"><span data-stu-id="2473c-939">&quot;2 2&quot;</span></span></td>
<td><span data-ttu-id="2473c-940">brevi trattini (ogni trattino e lo spazio tra due corrisponde al doppio della larghezza della linea)</span><span class="sxs-lookup"><span data-stu-id="2473c-940">short-dashes (each dash and the space in between is twice the width of the line)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-941">&quot;1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="2473c-941">&quot;1 2&quot;</span></span></td>
<td><span data-ttu-id="2473c-942">punto (ogni trattino è la larghezza della linea mentre ogni spazio è il doppio della larghezza della linea)</span><span class="sxs-lookup"><span data-stu-id="2473c-942">dot (each dash is the width of the line while each space is twice the width of the line)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-943">&quot;4 2&quot;</span><span class="sxs-lookup"><span data-stu-id="2473c-943">&quot;4 2&quot;</span></span></td>
<td><span data-ttu-id="2473c-944">Dash (ogni trattino è quattro volte la larghezza della linea mentre ogni spazio è il doppio della larghezza della linea)</span><span class="sxs-lookup"><span data-stu-id="2473c-944">dash (each dash is four times the width of the line while each space is twice the width of the line)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-945">&quot;8 2&quot;</span><span class="sxs-lookup"><span data-stu-id="2473c-945">&quot;8 2&quot;</span></span></td>
<td><span data-ttu-id="2473c-946">trattino lungo</span><span class="sxs-lookup"><span data-stu-id="2473c-946">long-dash</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-947">&quot;4 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="2473c-947">&quot;4 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="2473c-948">punto tratteggiato</span><span class="sxs-lookup"><span data-stu-id="2473c-948">dash dot</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-949">&quot;8 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="2473c-949">&quot;8 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="2473c-950">punto lungo trattino</span><span class="sxs-lookup"><span data-stu-id="2473c-950">long-dash dot</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-951">&quot;8 2 1 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="2473c-951">&quot;8 2 1 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="2473c-952">punto a trattino lungo</span><span class="sxs-lookup"><span data-stu-id="2473c-952">long-dash dot dot</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="textpath-element"></a><span data-ttu-id="2473c-953">Elemento TextPath</span><span class="sxs-lookup"><span data-stu-id="2473c-953">TextPath element</span></span>

<span data-ttu-id="2473c-954">Descrive un percorso vettoriale basato sui dati di testo, il tipo di carattere e gli stili forniti.</span><span class="sxs-lookup"><span data-stu-id="2473c-954">Describes a vector path based on the text data, font, and styles supplied.</span></span> <span data-ttu-id="2473c-955">Il percorso di testo è decurvato per essere conforme a un elemento **path** , se specificato.</span><span class="sxs-lookup"><span data-stu-id="2473c-955">The text path is warped to conform to a **Path** element if supplied.</span></span>



|          |                                                                                                                               |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2473c-956">FitPath</span><span class="sxs-lookup"><span data-stu-id="2473c-956">FitPath</span></span>  | <span data-ttu-id="2473c-957">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-957">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="2473c-958">Ridimensiona il testo per riempire il percorso su cui si trova.</span><span class="sxs-lookup"><span data-stu-id="2473c-958">Sizes the text to fill the path it lies out on.</span></span>                                 |
| <span data-ttu-id="2473c-959">FitShape</span><span class="sxs-lookup"><span data-stu-id="2473c-959">FitShape</span></span> | <span data-ttu-id="2473c-960">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-960">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="2473c-961">Estende il percorso del testo ai bordi della casella della forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-961">Stretches the text path out to the edges of the shape box.</span></span>                      |
| <span data-ttu-id="2473c-962">Attivato</span><span class="sxs-lookup"><span data-stu-id="2473c-962">On</span></span>       | <span data-ttu-id="2473c-963">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-963">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="2473c-964">Determina se i percorsi dei caratteri sono visualizzati o meno.</span><span class="sxs-lookup"><span data-stu-id="2473c-964">Determines whether the character paths are displayed or not.</span></span>                    |
| <span data-ttu-id="2473c-965">string</span><span class="sxs-lookup"><span data-stu-id="2473c-965">String</span></span>   | <span data-ttu-id="2473c-966">Stringa.</span><span class="sxs-lookup"><span data-stu-id="2473c-966">String.</span></span> <span data-ttu-id="2473c-967">Testo di cui eseguire il rendering come percorso di testo.</span><span class="sxs-lookup"><span data-stu-id="2473c-967">The text to render as a text path.</span></span>                                                                                    |
| <span data-ttu-id="2473c-968">Taglio</span><span class="sxs-lookup"><span data-stu-id="2473c-968">Trim</span></span>     | <span data-ttu-id="2473c-969">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-969">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="2473c-970">Rimuove qualsiasi spazio aggiuntivo riservato per gli ascendenti e i discendenti se non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="2473c-970">Removes any additional space reserved for ascenders and descenders if not used.</span></span> |
| <span data-ttu-id="2473c-971">XScale</span><span class="sxs-lookup"><span data-stu-id="2473c-971">XScale</span></span>   | <span data-ttu-id="2473c-972">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-972">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="2473c-973">Utilizzare la misurazione x dritto anziché misurare lungo il percorso.</span><span class="sxs-lookup"><span data-stu-id="2473c-973">Use straight x measurement instead of measuring along the path.</span></span>                 |



 

## <a name="data-types-used-in-the-vml-object-model"></a><span data-ttu-id="2473c-974">Tipi di dati utilizzati nel modello a oggetti la</span><span class="sxs-lookup"><span data-stu-id="2473c-974">Data Types Used in the VML Object Model</span></span>

<span data-ttu-id="2473c-975">I tipi di dati seguenti vengono utilizzati dal modello a oggetti la.</span><span class="sxs-lookup"><span data-stu-id="2473c-975">The following data types are used by the VML Object Model.</span></span>

-   [<span data-ttu-id="2473c-976">Double</span><span class="sxs-lookup"><span data-stu-id="2473c-976">Double</span></span>](/windows)
-   [<span data-ttu-id="2473c-977">Fisso</span><span class="sxs-lookup"><span data-stu-id="2473c-977">Fixed</span></span>](/windows)
-   [<span data-ttu-id="2473c-978">Integer</span><span class="sxs-lookup"><span data-stu-id="2473c-978">Integer</span></span>](/windows)
-   [<span data-ttu-id="2473c-979">IVgAdjustments</span><span class="sxs-lookup"><span data-stu-id="2473c-979">IVgAdjustments</span></span>](/windows)
-   [<span data-ttu-id="2473c-980">IVgColor</span><span class="sxs-lookup"><span data-stu-id="2473c-980">IVgColor</span></span>](/windows)
-   [<span data-ttu-id="2473c-981">IVgEquation</span><span class="sxs-lookup"><span data-stu-id="2473c-981">IVgEquation</span></span>](/windows)
-   [<span data-ttu-id="2473c-982">IVgFixedRectangle</span><span class="sxs-lookup"><span data-stu-id="2473c-982">IVgFixedRectangle</span></span>](/windows)
-   [<span data-ttu-id="2473c-983">IVgFixedRectangleArray</span><span class="sxs-lookup"><span data-stu-id="2473c-983">IVgFixedRectangleArray</span></span>](/windows)
-   [<span data-ttu-id="2473c-984">IVgFormula</span><span class="sxs-lookup"><span data-stu-id="2473c-984">IVgFormula</span></span>](/windows)
-   [<span data-ttu-id="2473c-985">IVgFormulas</span><span class="sxs-lookup"><span data-stu-id="2473c-985">IVgFormulas</span></span>](/windows)
-   [<span data-ttu-id="2473c-986">IVgGradientColorArray</span><span class="sxs-lookup"><span data-stu-id="2473c-986">IVgGradientColorArray</span></span>](/windows)
-   [<span data-ttu-id="2473c-987">IVgPoints</span><span class="sxs-lookup"><span data-stu-id="2473c-987">IVgPoints</span></span>](/windows)
-   [<span data-ttu-id="2473c-988">IVgSkewMatrix</span><span class="sxs-lookup"><span data-stu-id="2473c-988">IVgSkewMatrix</span></span>](/windows)
-   [<span data-ttu-id="2473c-989">IVgSkewOffset</span><span class="sxs-lookup"><span data-stu-id="2473c-989">IVgSkewOffset</span></span>](/windows)
-   [<span data-ttu-id="2473c-990">IVgVector2D</span><span class="sxs-lookup"><span data-stu-id="2473c-990">IVgVector2D</span></span>](/windows)
-   [<span data-ttu-id="2473c-991">IVgVector3D</span><span class="sxs-lookup"><span data-stu-id="2473c-991">IVgVector3D</span></span>](/windows)
-   [<span data-ttu-id="2473c-992">Length</span><span class="sxs-lookup"><span data-stu-id="2473c-992">Length</span></span>](/windows)
-   [<span data-ttu-id="2473c-993">Measure</span><span class="sxs-lookup"><span data-stu-id="2473c-993">Measure</span></span>](/windows)
-   [<span data-ttu-id="2473c-994">Stringa</span><span class="sxs-lookup"><span data-stu-id="2473c-994">String</span></span>](/windows)
-   [<span data-ttu-id="2473c-995">VgBlackWhiteMode</span><span class="sxs-lookup"><span data-stu-id="2473c-995">VgBlackWhiteMode</span></span>](/windows)
-   [<span data-ttu-id="2473c-996">VgFraction</span><span class="sxs-lookup"><span data-stu-id="2473c-996">VgFraction</span></span>](/windows)
-   [<span data-ttu-id="2473c-997">VgTriState</span><span class="sxs-lookup"><span data-stu-id="2473c-997">VgTriState</span></span>](/windows)

<span data-ttu-id="2473c-998">**Tipo di dati Double**</span><span class="sxs-lookup"><span data-stu-id="2473c-998">**Double data type**</span></span>

<span data-ttu-id="2473c-999">Intero a precisione doppia con intervallo compreso tra-infinito e infinito.</span><span class="sxs-lookup"><span data-stu-id="2473c-999">A double precision integer with range from -infinity to infinity.</span></span>

<span data-ttu-id="2473c-1000">**Tipo di dati Fixed**</span><span class="sxs-lookup"><span data-stu-id="2473c-1000">**Fixed data type**</span></span>

<span data-ttu-id="2473c-1001">Numero a virgola mobile con intervallo compreso tra-32.766,0 e 32.766,0.</span><span class="sxs-lookup"><span data-stu-id="2473c-1001">Floating point number with range from -32,766.0 to 32,766.0.</span></span>

<span data-ttu-id="2473c-1002">**Tipo di dati Integer**</span><span class="sxs-lookup"><span data-stu-id="2473c-1002">**Integer data type**</span></span>

<span data-ttu-id="2473c-1003">Intero con un intervallo compreso tra-infinito e infinito.</span><span class="sxs-lookup"><span data-stu-id="2473c-1003">An integer with a range from -infinity to infinity.</span></span>

<span data-ttu-id="2473c-1004">**Tipo di dati IVgAdjustments**</span><span class="sxs-lookup"><span data-stu-id="2473c-1004">**IVgAdjustments data type**</span></span>

<span data-ttu-id="2473c-1005">Raccolta di modifiche apportate a una forma che può essere utilizzata per modificare le dimensioni di una forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-1005">Collection of adjustments to a shape that can be used to change the dimensions of a shape.</span></span> <span data-ttu-id="2473c-1006">Le regolazioni possono essere utilizzate come segnaposti temporanei o per qualsiasi motivo per cui si utilizzano le variabili.</span><span class="sxs-lookup"><span data-stu-id="2473c-1006">Adjustments can be used as temporary placeholders or for any reason you would use variables.</span></span> <span data-ttu-id="2473c-1007">Sono presenti solo 8 modifiche nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="2473c-1007">There are only 8 adjustments in the collection.</span></span>



| <span data-ttu-id="2473c-1008">Attributi</span><span class="sxs-lookup"><span data-stu-id="2473c-1008">Attributes</span></span> | <span data-ttu-id="2473c-1009">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2473c-1009">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2473c-1010">Exists</span><span class="sxs-lookup"><span data-stu-id="2473c-1010">Exists</span></span>     | <span data-ttu-id="2473c-1011">[IVgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-1011">[IVgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="2473c-1012">Determina se esiste una rettifica specificata.</span><span class="sxs-lookup"><span data-stu-id="2473c-1012">Determines whether a specified adjustment exists.</span></span> <span data-ttu-id="2473c-1013">Si noti che è necessario utilizzare un indice. ovvero è necessario utilizzare EXISTS (item) per recuperare l'esistenza di un elemento.</span><span class="sxs-lookup"><span data-stu-id="2473c-1013">Note that an index must be used; that is, exists( item ) must be used to retrieve the existence of an item.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="2473c-1014">Elemento</span><span class="sxs-lookup"><span data-stu-id="2473c-1014">Item</span></span>       | <span data-ttu-id="2473c-1015">[Long](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-1015">[Long](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="2473c-1016">Matrice di regolazioni indicizzate da 0 a 7.</span><span class="sxs-lookup"><span data-stu-id="2473c-1016">Array of adjustments indexed from 0 to 7.</span></span> <span data-ttu-id="2473c-1017">Si noti che le regolazioni possono essere specificate in SPARC; ovvero i valori della matrice intermedia potrebbero non essere sempre compilati.</span><span class="sxs-lookup"><span data-stu-id="2473c-1017">Note that adjustments may be sparcely specified; that is, intermediate array values may not always be filled.</span></span> <span data-ttu-id="2473c-1018">Ad esempio, Item 1, 3 e 5 possono avere valori per una lunghezza di 3, con Item (0), Item (2) e Item (4) specificati.</span><span class="sxs-lookup"><span data-stu-id="2473c-1018">For example, item 1, 3, and 5 could have values for a length of 3, with item(0), item(2), and item(4) specified.</span></span> <span data-ttu-id="2473c-1019">Per verificare se esiste un elemento, usare l'attributo exists.</span><span class="sxs-lookup"><span data-stu-id="2473c-1019">To see if an item exists, use the Exists attribute.</span></span> |
| <span data-ttu-id="2473c-1020">Length</span><span class="sxs-lookup"><span data-stu-id="2473c-1020">Length</span></span>     | <span data-ttu-id="2473c-1021">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-1021">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="2473c-1022">Numero di rettifiche.</span><span class="sxs-lookup"><span data-stu-id="2473c-1022">Number of adjustments.</span></span> <span data-ttu-id="2473c-1023">Non può essere maggiore di 8.</span><span class="sxs-lookup"><span data-stu-id="2473c-1023">Can be no greater than 8.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="2473c-1024">Valore</span><span class="sxs-lookup"><span data-stu-id="2473c-1024">Value</span></span>      | <span data-ttu-id="2473c-1025">[Stringa](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-1025">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="2473c-1026">Rappresentazione testuale dei valori numerici, con virgole tra ogni numero.</span><span class="sxs-lookup"><span data-stu-id="2473c-1026">Text representation of numeric values, with commas between each number.</span></span>                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="2473c-1027">**IVgColor**</span><span class="sxs-lookup"><span data-stu-id="2473c-1027">**IVgColor**</span></span>

<span data-ttu-id="2473c-1028">Specifica un colore.</span><span class="sxs-lookup"><span data-stu-id="2473c-1028">Specifies a color.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2473c-1029">Attributi</span><span class="sxs-lookup"><span data-stu-id="2473c-1029">Attributes</span></span></th>
<th><span data-ttu-id="2473c-1030">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2473c-1030">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2473c-1031">RGB</span><span class="sxs-lookup"><span data-stu-id="2473c-1031">RGB</span></span></td>
<td><span data-ttu-id="2473c-1032"><strong>VgRGBType</strong>.</span><span class="sxs-lookup"><span data-stu-id="2473c-1032"><strong>VgRGBType</strong>.</span></span> <span data-ttu-id="2473c-1033">Valore RGB (Long) del colore.</span><span class="sxs-lookup"><span data-stu-id="2473c-1033">RGB value (Long) of the color.</span></span> <span data-ttu-id="2473c-1034">Valido solo se il tipo è RGB.</span><span class="sxs-lookup"><span data-stu-id="2473c-1034">Only valid if Type is RGB.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-1035">R</span><span class="sxs-lookup"><span data-stu-id="2473c-1035">R</span></span></td>
<td><span data-ttu-id="2473c-1036"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-1036"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="2473c-1037">Componente rosso del colore.</span><span class="sxs-lookup"><span data-stu-id="2473c-1037">Red component of the color.</span></span> <span data-ttu-id="2473c-1038">Può variare da 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="2473c-1038">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-1039">G</span><span class="sxs-lookup"><span data-stu-id="2473c-1039">G</span></span></td>
<td><span data-ttu-id="2473c-1040"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-1040"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="2473c-1041">Componente verde del colore.</span><span class="sxs-lookup"><span data-stu-id="2473c-1041">Green component of the color.</span></span> <span data-ttu-id="2473c-1042">Può variare da 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="2473c-1042">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-1043">B</span><span class="sxs-lookup"><span data-stu-id="2473c-1043">B</span></span></td>
<td><span data-ttu-id="2473c-1044"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-1044"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="2473c-1045">Componente blu del colore.</span><span class="sxs-lookup"><span data-stu-id="2473c-1045">Blue component of the color.</span></span> <span data-ttu-id="2473c-1046">Può variare da 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="2473c-1046">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-1047">string</span><span class="sxs-lookup"><span data-stu-id="2473c-1047">String</span></span></td>
<td><span data-ttu-id="2473c-1048"><a href="#data-types-used-in-the-vml-object-model">Stringa</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-1048"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="2473c-1049">Rappresentazione testuale del colore.</span><span class="sxs-lookup"><span data-stu-id="2473c-1049">Text representation of the color.</span></span> <span data-ttu-id="2473c-1050">Sono supportati i seguenti tipi di colori denominati:</span><span class="sxs-lookup"><span data-stu-id="2473c-1050">The following named color types are supported:</span></span>
<ul>
<li><span data-ttu-id="2473c-1051">Nero (#000000)</span><span class="sxs-lookup"><span data-stu-id="2473c-1051">Black (#000000)</span></span></li>
<li><span data-ttu-id="2473c-1052">Argento (#C0C0C0)</span><span class="sxs-lookup"><span data-stu-id="2473c-1052">Silver (#C0C0C0)</span></span></li>
<li><span data-ttu-id="2473c-1053">Grigio (#808080)</span><span class="sxs-lookup"><span data-stu-id="2473c-1053">Gray (#808080)</span></span></li>
<li><span data-ttu-id="2473c-1054">Bianco (#FFFFFF)</span><span class="sxs-lookup"><span data-stu-id="2473c-1054">White (#FFFFFF)</span></span></li>
<li><span data-ttu-id="2473c-1055">Marrone (#800000)</span><span class="sxs-lookup"><span data-stu-id="2473c-1055">Maroon (#800000)</span></span></li>
<li><span data-ttu-id="2473c-1056">Rosso (#FF0000)</span><span class="sxs-lookup"><span data-stu-id="2473c-1056">Red (#FF0000)</span></span></li>
<li><span data-ttu-id="2473c-1057">Viola (#800080)</span><span class="sxs-lookup"><span data-stu-id="2473c-1057">Purple (#800080)</span></span></li>
<li><span data-ttu-id="2473c-1058">Fucsia (#FF00FF)</span><span class="sxs-lookup"><span data-stu-id="2473c-1058">Fuchsia (#FF00FF)</span></span></li>
<li><span data-ttu-id="2473c-1059">Verde (#008000)</span><span class="sxs-lookup"><span data-stu-id="2473c-1059">Green (#008000)</span></span></li>
<li><span data-ttu-id="2473c-1060">Lime (#00FF00)</span><span class="sxs-lookup"><span data-stu-id="2473c-1060">Lime (#00FF00)</span></span></li>
<li><span data-ttu-id="2473c-1061">Olive (#808000)</span><span class="sxs-lookup"><span data-stu-id="2473c-1061">Olive (#808000)</span></span></li>
<li><span data-ttu-id="2473c-1062">Giallo (#FFFF00)</span><span class="sxs-lookup"><span data-stu-id="2473c-1062">Yellow (#FFFF00)</span></span></li>
<li><span data-ttu-id="2473c-1063">Navy (#000080)</span><span class="sxs-lookup"><span data-stu-id="2473c-1063">Navy (#000080)</span></span></li>
<li><span data-ttu-id="2473c-1064">Blu (#0000FF)</span><span class="sxs-lookup"><span data-stu-id="2473c-1064">Blue (#0000FF)</span></span></li>
<li><span data-ttu-id="2473c-1065">Verde acqua (#008080)</span><span class="sxs-lookup"><span data-stu-id="2473c-1065">Teal (#008080)</span></span></li>
<li><span data-ttu-id="2473c-1066">Aqua (#00FFFF)</span><span class="sxs-lookup"><span data-stu-id="2473c-1066">Aqua (#00FFFF)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-1067">Tipo</span><span class="sxs-lookup"><span data-stu-id="2473c-1067">Type</span></span></td>
<td><span data-ttu-id="2473c-1068"><strong>VgColorType</strong>.</span><span class="sxs-lookup"><span data-stu-id="2473c-1068"><strong>VgColorType</strong>.</span></span> <span data-ttu-id="2473c-1069">Tipo di colore.</span><span class="sxs-lookup"><span data-stu-id="2473c-1069">Type of color.</span></span> <span data-ttu-id="2473c-1070">Uno dei tipi seguenti:</span><span class="sxs-lookup"><span data-stu-id="2473c-1070">One of the following types:</span></span>
<ul>
<li><span data-ttu-id="2473c-1071">Mixed</span><span class="sxs-lookup"><span data-stu-id="2473c-1071">Mixed</span></span></li>
<li><span data-ttu-id="2473c-1072">denominata</span><span class="sxs-lookup"><span data-stu-id="2473c-1072">Named</span></span></li>
<li><span data-ttu-id="2473c-1073">RGB</span><span class="sxs-lookup"><span data-stu-id="2473c-1073">RGB</span></span></li>
<li><span data-ttu-id="2473c-1074">Schema</span><span class="sxs-lookup"><span data-stu-id="2473c-1074">Scheme</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2473c-1075">**IVgEquation**</span><span class="sxs-lookup"><span data-stu-id="2473c-1075">**IVgEquation**</span></span>

<span data-ttu-id="2473c-1076">Equazioni utilizzate per le formule.</span><span class="sxs-lookup"><span data-stu-id="2473c-1076">Equations used for formulas.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2473c-1077">Operazione</span><span class="sxs-lookup"><span data-stu-id="2473c-1077">Operation</span></span></td>
<td><span data-ttu-id="2473c-1078"><strong>VgEquationOperationType</strong> Nome dell'operazione da eseguire sui parametri.</span><span class="sxs-lookup"><span data-stu-id="2473c-1078"><strong>VgEquationOperationType</strong> Name of operation to perform on the parameters.</span></span> <span data-ttu-id="2473c-1079">In un'equazione è possibile usare le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="2473c-1079">The following operations can be used in an equation:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2473c-1080">Operazione</span><span class="sxs-lookup"><span data-stu-id="2473c-1080">Operation</span></span></th>
<th><span data-ttu-id="2473c-1081">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2473c-1081">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2473c-1082">Abs</span><span class="sxs-lookup"><span data-stu-id="2473c-1082">Abs</span></span></td>
<td><span data-ttu-id="2473c-1083">Valore assoluto.</span><span class="sxs-lookup"><span data-stu-id="2473c-1083">Absolute value.</span></span> <br/> <span data-ttu-id="2473c-1084"><strong>ABS</strong>(v)</span><span class="sxs-lookup"><span data-stu-id="2473c-1084"><strong>abs</strong>(v)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-1085">Atan2</span><span class="sxs-lookup"><span data-stu-id="2473c-1085">Atan2</span></span></td>
<td><span data-ttu-id="2473c-1086">Aritmetica polare: restituisce unità FD (gradi moltiplicate per 65536).</span><span class="sxs-lookup"><span data-stu-id="2473c-1086">Polar arithmetic--results in fd units (degrees multiplied by 65536).</span></span><br/> <span data-ttu-id="2473c-1087"><strong>Atan2</strong>(P1, v)</span><span class="sxs-lookup"><span data-stu-id="2473c-1087"><strong>atan2</strong>(p1,v)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-1088">Cos</span><span class="sxs-lookup"><span data-stu-id="2473c-1088">Cos</span></span></td>
<td><span data-ttu-id="2473c-1089">Coseno, argomento in unità FD (gradi moltiplicato per 65536).</span><span class="sxs-lookup"><span data-stu-id="2473c-1089">Cosine, argument in fd units (degrees multiplied by 65536).</span></span><br/> <span data-ttu-id="2473c-1090">v \* <strong>cos</strong>(P1)</span><span class="sxs-lookup"><span data-stu-id="2473c-1090">v \* <strong>cos</strong>(p1)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-1091">Cosatan2</span><span class="sxs-lookup"><span data-stu-id="2473c-1091">Cosatan2</span></span></td>
<td><span data-ttu-id="2473c-1092">Conserva la precisione completa nel calcolo intermedio.</span><span class="sxs-lookup"><span data-stu-id="2473c-1092">Preserves full accuracy in intermediate calculation.</span></span><br/> <span data-ttu-id="2473c-1093">v \* <strong>cos (atan2 (</strong> P2, P1 <strong>))</strong></span><span class="sxs-lookup"><span data-stu-id="2473c-1093">v \* <strong>cos(atan2(</strong> p2,p1 <strong>))</strong></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-1094">Ellisse</span><span class="sxs-lookup"><span data-stu-id="2473c-1094">Ellipse</span></span></td>
<td><span data-ttu-id="2473c-1095">Ellisse</span><span class="sxs-lookup"><span data-stu-id="2473c-1095">Ellipse</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-1096">Se</span><span class="sxs-lookup"><span data-stu-id="2473c-1096">If</span></span></td>
<td><span data-ttu-id="2473c-1097">Se il test della condizione.</span><span class="sxs-lookup"><span data-stu-id="2473c-1097">If Condition test.</span></span> <span data-ttu-id="2473c-1098">v > 0 <strong>?</strong></span><span class="sxs-lookup"><span data-stu-id="2473c-1098">v > 0 <strong>?</strong></span></span> <span data-ttu-id="2473c-1099">P1: P2</span><span class="sxs-lookup"><span data-stu-id="2473c-1099">p1 : p2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-1100">Max</span><span class="sxs-lookup"><span data-stu-id="2473c-1100">Max</span></span></td>
<td><span data-ttu-id="2473c-1101">Maggiore di due valori.</span><span class="sxs-lookup"><span data-stu-id="2473c-1101">The greater of two values.</span></span> <br/> <span data-ttu-id="2473c-1102"><strong>Max</strong>(v, P1)</span><span class="sxs-lookup"><span data-stu-id="2473c-1102"><strong>max</strong>(v,p1)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-1103">Mid</span><span class="sxs-lookup"><span data-stu-id="2473c-1103">Mid</span></span></td>
<td><span data-ttu-id="2473c-1104">Media (v + P1)/2</span><span class="sxs-lookup"><span data-stu-id="2473c-1104">Average ( v + p1)/2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-1105">Min</span><span class="sxs-lookup"><span data-stu-id="2473c-1105">Min</span></span></td>
<td><span data-ttu-id="2473c-1106">Minore di due valori.</span><span class="sxs-lookup"><span data-stu-id="2473c-1106">The lesser of two values.</span></span> <span data-ttu-id="2473c-1107"><strong>min</strong>(v, P1)</span><span class="sxs-lookup"><span data-stu-id="2473c-1107"><strong>min</strong>(v,p1)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-1108">Mod</span><span class="sxs-lookup"><span data-stu-id="2473c-1108">Mod</span></span></td>
<td><span data-ttu-id="2473c-1109">Modulo.</span><span class="sxs-lookup"><span data-stu-id="2473c-1109">Modulus.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-1110">Prodotto</span><span class="sxs-lookup"><span data-stu-id="2473c-1110">Product</span></span></td>
<td><span data-ttu-id="2473c-1111">Usato per la moltiplicazione e la divisione.</span><span class="sxs-lookup"><span data-stu-id="2473c-1111">Used for multiplication and division.</span></span> <span data-ttu-id="2473c-1112">v \* P1/P2</span><span class="sxs-lookup"><span data-stu-id="2473c-1112">v \* p1 / p2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-1113">Sin</span><span class="sxs-lookup"><span data-stu-id="2473c-1113">Sin</span></span></td>
<td><span data-ttu-id="2473c-1114">Seno, argomento in unità FD (gradi moltiplicato per 65536).</span><span class="sxs-lookup"><span data-stu-id="2473c-1114">Sine, argument in fd units (degrees multiplied by 65536).</span></span> <br/> <span data-ttu-id="2473c-1115">v \* <strong>sin</strong>(P1)</span><span class="sxs-lookup"><span data-stu-id="2473c-1115">v \* <strong>sin</strong>(p1)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-1116">Sinatan2</span><span class="sxs-lookup"><span data-stu-id="2473c-1116">Sinatan2</span></span></td>
<td><span data-ttu-id="2473c-1117">Conserva la precisione completa nel calcolo intermedio.</span><span class="sxs-lookup"><span data-stu-id="2473c-1117">Preserves full accuracy in intermediate calculation.</span></span> <span data-ttu-id="2473c-1118">v \* <strong>sin</strong>(<strong>Atan2</strong>(P2, P1))</span><span class="sxs-lookup"><span data-stu-id="2473c-1118">v \* <strong>sin</strong>(<strong>atan2</strong>(p2,p1))</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-1119">Sqrt</span><span class="sxs-lookup"><span data-stu-id="2473c-1119">Sqrt</span></span></td>
<td><span data-ttu-id="2473c-1120">Il risultato è positivo e viene arrotondato per difetto.</span><span class="sxs-lookup"><span data-stu-id="2473c-1120">Result is positive and rounds down.</span></span> <br/> <span data-ttu-id="2473c-1121"><strong>Sqrt</strong>(v)</span><span class="sxs-lookup"><span data-stu-id="2473c-1121"><strong>sqrt</strong>(v)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-1122">Sum</span><span class="sxs-lookup"><span data-stu-id="2473c-1122">Sum</span></span></td>
<td><span data-ttu-id="2473c-1123">Utilizzato per l'addizione e la sottrazione.</span><span class="sxs-lookup"><span data-stu-id="2473c-1123">Used for addition and subtraction.</span></span><br/> <span data-ttu-id="2473c-1124">v + P1 P2</span><span class="sxs-lookup"><span data-stu-id="2473c-1124">v + p1 p2</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-1125">Sumangle</span><span class="sxs-lookup"><span data-stu-id="2473c-1125">Sumangle</span></span></td>
<td><span data-ttu-id="2473c-1126">Angolo esistente (ridimensionato di 65536), dove P1 e P2 sono in gradi.</span><span class="sxs-lookup"><span data-stu-id="2473c-1126">Existing angle (scaled by 65536), where p1 and p2 are in degrees.</span></span><br/> <span data-ttu-id="2473c-1127">v + P1 \* 65536 + P2 \* 65536</span><span class="sxs-lookup"><span data-stu-id="2473c-1127">v + p1 \* 65536 + p2 \* 65536</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-1128">Tan</span><span class="sxs-lookup"><span data-stu-id="2473c-1128">Tan</span></span></td>
<td><span data-ttu-id="2473c-1129">Tangente, argomento in unità FD (gradi moltiplicato per 65536).</span><span class="sxs-lookup"><span data-stu-id="2473c-1129">Tangent, argument is in fd units (degrees multiplied by 65536).</span></span> <br/> <span data-ttu-id="2473c-1130">v \* Tan (P1)</span><span class="sxs-lookup"><span data-stu-id="2473c-1130">v \* tan( p1 )</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-1131">Val</span><span class="sxs-lookup"><span data-stu-id="2473c-1131">Val</span></span></td>
<td><span data-ttu-id="2473c-1132">Definisce un valore di guida da un altro valore.</span><span class="sxs-lookup"><span data-stu-id="2473c-1132">Defines a guide value from some other value.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-1133">Param1</span><span class="sxs-lookup"><span data-stu-id="2473c-1133">Param1</span></span></td>
<td><span data-ttu-id="2473c-1134"><strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="2473c-1134"><strong>Integer</strong>.</span></span> <span data-ttu-id="2473c-1135">Primo parametro.</span><span class="sxs-lookup"><span data-stu-id="2473c-1135">The first parameter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-1136">Paramtype1</span><span class="sxs-lookup"><span data-stu-id="2473c-1136">Paramtype1</span></span></td>
<td><span data-ttu-id="2473c-1137"><strong>VgFormulaParamType</strong>.</span><span class="sxs-lookup"><span data-stu-id="2473c-1137"><strong>VgFormulaParamType</strong>.</span></span> <span data-ttu-id="2473c-1138">Tipo del primo parametro.</span><span class="sxs-lookup"><span data-stu-id="2473c-1138">The type of the first parameter.</span></span> <span data-ttu-id="2473c-1139">Sono supportati i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="2473c-1139">The following values are supported:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2473c-1140">Tipo</span><span class="sxs-lookup"><span data-stu-id="2473c-1140">Type</span></span></th>
<th><span data-ttu-id="2473c-1141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2473c-1141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2473c-1142">Valore</span><span class="sxs-lookup"><span data-stu-id="2473c-1142">Value</span></span></td>
<td><span data-ttu-id="2473c-1143">Il parametro è un valore semplice.</span><span class="sxs-lookup"><span data-stu-id="2473c-1143">Parameter is simple value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-1144">AdjustmentReference</span><span class="sxs-lookup"><span data-stu-id="2473c-1144">AdjustmentReference</span></span></td>
<td><span data-ttu-id="2473c-1145">Il parametro è un riferimento a una rettifica.</span><span class="sxs-lookup"><span data-stu-id="2473c-1145">Parameter is a reference to an adjustment.</span></span> <span data-ttu-id="2473c-1146">Se, ad esempio, il primo parametro è 1, verrà utilizzato il valore della prima regolazione.</span><span class="sxs-lookup"><span data-stu-id="2473c-1146">For example, if the first parameter is 1, then the value of the first adjustment will be used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-1147">FormulaReference</span><span class="sxs-lookup"><span data-stu-id="2473c-1147">FormulaReference</span></span></td>
<td><span data-ttu-id="2473c-1148">Il parametro è il risultato di un riferimento al risultato di una formula precedente.</span><span class="sxs-lookup"><span data-stu-id="2473c-1148">Parameter is the result of a reference to the result of a previous formula.</span></span> <span data-ttu-id="2473c-1149">Se, ad esempio, il primo parametro è 2, verrà utilizzato il risultato della formula 2.</span><span class="sxs-lookup"><span data-stu-id="2473c-1149">For example, if the first parameter is 2, then the result of formula 2 will be used.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-1150">Param2</span><span class="sxs-lookup"><span data-stu-id="2473c-1150">Param2</span></span></td>
<td><span data-ttu-id="2473c-1151"><strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="2473c-1151"><strong>Integer</strong>.</span></span> <span data-ttu-id="2473c-1152">Secondo parametro.</span><span class="sxs-lookup"><span data-stu-id="2473c-1152">The second parameter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-1153">Paramtype2</span><span class="sxs-lookup"><span data-stu-id="2473c-1153">Paramtype2</span></span></td>
<td><span data-ttu-id="2473c-1154"><strong>VgFormulaParamType</strong> Tipo di parametro 2.</span><span class="sxs-lookup"><span data-stu-id="2473c-1154"><strong>VgFormulaParamType</strong> The type of parameter 2.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-1155">Val</span><span class="sxs-lookup"><span data-stu-id="2473c-1155">Val</span></span></td>
<td><span data-ttu-id="2473c-1156"><strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="2473c-1156"><strong>Integer</strong>.</span></span> <span data-ttu-id="2473c-1157">Risultato.</span><span class="sxs-lookup"><span data-stu-id="2473c-1157">The result.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-1158">Valtype2</span><span class="sxs-lookup"><span data-stu-id="2473c-1158">Valtype2</span></span></td>
<td><span data-ttu-id="2473c-1159"><strong>VgFormulaParamType</strong>.</span><span class="sxs-lookup"><span data-stu-id="2473c-1159"><strong>VgFormulaParamType</strong>.</span></span> <span data-ttu-id="2473c-1160">Tipo del risultato.</span><span class="sxs-lookup"><span data-stu-id="2473c-1160">The type of the result.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2473c-1161">**IVgFixedRectangle**</span><span class="sxs-lookup"><span data-stu-id="2473c-1161">**IVgFixedRectangle**</span></span>

<span data-ttu-id="2473c-1162">Specifica un rettangolo fisso.</span><span class="sxs-lookup"><span data-stu-id="2473c-1162">Specifies a fixed rectangle.</span></span>



| <span data-ttu-id="2473c-1163">Attributi</span><span class="sxs-lookup"><span data-stu-id="2473c-1163">Attributes</span></span> | <span data-ttu-id="2473c-1164">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2473c-1164">Description</span></span>                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2473c-1165">Valore</span><span class="sxs-lookup"><span data-stu-id="2473c-1165">Value</span></span>      | <span data-ttu-id="2473c-1166">[Stringa](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-1166">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="2473c-1167">Valore di testo che specifica il percorso.</span><span class="sxs-lookup"><span data-stu-id="2473c-1167">Text value specifying the path.</span></span>         |
| <span data-ttu-id="2473c-1168">Sinistra</span><span class="sxs-lookup"><span data-stu-id="2473c-1168">Left</span></span>       | <span data-ttu-id="2473c-1169">[Valore Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-1169">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="2473c-1170">Coordinata più a sinistra del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="2473c-1170">Leftmost coordinate of the rectangle.</span></span>   |
| <span data-ttu-id="2473c-1171">Inizio</span><span class="sxs-lookup"><span data-stu-id="2473c-1171">Top</span></span>        | <span data-ttu-id="2473c-1172">[Valore Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-1172">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="2473c-1173">Coordinata superiore del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="2473c-1173">Topmost coordinate of the rectangle.</span></span>    |
| <span data-ttu-id="2473c-1174">Destra</span><span class="sxs-lookup"><span data-stu-id="2473c-1174">Right</span></span>      | <span data-ttu-id="2473c-1175">[Valore Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-1175">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="2473c-1176">Coordinata più a destra del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="2473c-1176">Rightmost coordinate of the rectangle.</span></span>  |
| <span data-ttu-id="2473c-1177">Ultimo</span><span class="sxs-lookup"><span data-stu-id="2473c-1177">Bottom</span></span>     | <span data-ttu-id="2473c-1178">[Valore Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-1178">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="2473c-1179">Coordinata inferiori del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="2473c-1179">Bottommost coordinate of the rectangle.</span></span> |



 

<span data-ttu-id="2473c-1180">**IVgFixedRectangleArray**</span><span class="sxs-lookup"><span data-stu-id="2473c-1180">**IVgFixedRectangleArray**</span></span>

<span data-ttu-id="2473c-1181">Matrice di rettangoli fissi.</span><span class="sxs-lookup"><span data-stu-id="2473c-1181">Array of fixed rectangles.</span></span>



| <span data-ttu-id="2473c-1182">Attributi</span><span class="sxs-lookup"><span data-stu-id="2473c-1182">Attributes</span></span> | <span data-ttu-id="2473c-1183">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2473c-1183">Description</span></span>                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2473c-1184">Valore</span><span class="sxs-lookup"><span data-stu-id="2473c-1184">Value</span></span>      | <span data-ttu-id="2473c-1185">[Stringa](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-1185">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="2473c-1186">Rappresentazione testuale della matrice.</span><span class="sxs-lookup"><span data-stu-id="2473c-1186">Text representation of array.</span></span>                           |
| <span data-ttu-id="2473c-1187">Length</span><span class="sxs-lookup"><span data-stu-id="2473c-1187">Length</span></span>     | <span data-ttu-id="2473c-1188">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-1188">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="2473c-1189">Numero di rettangoli in questa matrice.</span><span class="sxs-lookup"><span data-stu-id="2473c-1189">Number of rectangles in this array.</span></span>                    |
| <span data-ttu-id="2473c-1190">Elemento</span><span class="sxs-lookup"><span data-stu-id="2473c-1190">Item</span></span>       | <span data-ttu-id="2473c-1191">[IVgFixedRectangle](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-1191">[IVgFixedRectangle](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="2473c-1192">Oggetto rettangolo in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="2473c-1192">The rectangle object at the specified index.</span></span> |



 

<span data-ttu-id="2473c-1193">Tipo di dati **IVgFormula**</span><span class="sxs-lookup"><span data-stu-id="2473c-1193">**IVgFormula** data type</span></span>

<span data-ttu-id="2473c-1194">Definizioni per le formule che possono variare il percorso di una forma o essere utilizzate per altri scopi di calcolo.</span><span class="sxs-lookup"><span data-stu-id="2473c-1194">Definitions for formulas that can vary the path of a shape or be used for other calculation purposes.</span></span> <span data-ttu-id="2473c-1195">Le formule possono essere basate sull'attributo **ADJ** di una forma, che può cambiare.</span><span class="sxs-lookup"><span data-stu-id="2473c-1195">Formulas can be based on the **Adj** attribute of a shape, which can change.</span></span> <span data-ttu-id="2473c-1196">Le formule possono anche fare riferimento ad altre formule.</span><span class="sxs-lookup"><span data-stu-id="2473c-1196">Formulas can reference other formulas as well.</span></span>



| <span data-ttu-id="2473c-1197">Attributi</span><span class="sxs-lookup"><span data-stu-id="2473c-1197">Attributes</span></span> | <span data-ttu-id="2473c-1198">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2473c-1198">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2473c-1199">EQN</span><span class="sxs-lookup"><span data-stu-id="2473c-1199">Eqn</span></span>        | <span data-ttu-id="2473c-1200">[IVgEquation](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-1200">[IVgEquation](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="2473c-1201">Ogni formula definisce un singolo valore come risultato della valutazione dell'espressione.</span><span class="sxs-lookup"><span data-stu-id="2473c-1201">Each formula defines a single value as the result of the evaluation of the expression.</span></span> <span data-ttu-id="2473c-1202">L'espressione è definita da questo attributo e ha il formato generale di un'operazione seguita da un massimo di tre argomenti, che possono essere valori di rettifica (ad esempio, \# 2), i risultati delle formule precedenti (ad esempio, @2 ), i numeri fissi o i valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="2473c-1202">The expression is defined by this attribute and has the general form of an operation followed by up to three arguments, which may be adjustment values (e.g., \#2), the results of earlier formulas (e.g., @2), fixed numbers, or predefined values.</span></span> |



 

<span data-ttu-id="2473c-1203">**Tipo di dati IVgFormulas**</span><span class="sxs-lookup"><span data-stu-id="2473c-1203">**IVgFormulas data type**</span></span>

<span data-ttu-id="2473c-1204">Raccolta di oggetti formula.</span><span class="sxs-lookup"><span data-stu-id="2473c-1204">A collection of formula objects.</span></span>



| <span data-ttu-id="2473c-1205">Attributi</span><span class="sxs-lookup"><span data-stu-id="2473c-1205">Attributes</span></span> | <span data-ttu-id="2473c-1206">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2473c-1206">Description</span></span>                                                                                                                                  |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2473c-1207">Length</span><span class="sxs-lookup"><span data-stu-id="2473c-1207">Length</span></span>     | <span data-ttu-id="2473c-1208">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-1208">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="2473c-1209">Numero di oggetti formula nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="2473c-1209">Number of formula objects in collection.</span></span>                                                |
| <span data-ttu-id="2473c-1210">Elemento</span><span class="sxs-lookup"><span data-stu-id="2473c-1210">Item</span></span>       | <span data-ttu-id="2473c-1211">[IVgFormula](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-1211">[IVgFormula](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="2473c-1212">Formula specifica.</span><span class="sxs-lookup"><span data-stu-id="2473c-1212">A specific formula.</span></span> <span data-ttu-id="2473c-1213">Si noti che la matrice di formule può essere ereditata dal tipo di forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-1213">Note that the formula array may be inherited fom the shape type.</span></span> |



 

<span data-ttu-id="2473c-1214">**IVgGradientColorArray**</span><span class="sxs-lookup"><span data-stu-id="2473c-1214">**IVgGradientColorArray**</span></span>

<span data-ttu-id="2473c-1215">Matrice di colori che definiscono una sfumatura (intervallo di colori misto).</span><span class="sxs-lookup"><span data-stu-id="2473c-1215">An array of colors that define a gradient (blended range of colors).</span></span>



| <span data-ttu-id="2473c-1216">Attributi</span><span class="sxs-lookup"><span data-stu-id="2473c-1216">Attributes</span></span> | <span data-ttu-id="2473c-1217">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2473c-1217">Description</span></span>                                                                                                                  |
|------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2473c-1218">Valore</span><span class="sxs-lookup"><span data-stu-id="2473c-1218">Value</span></span>      | <span data-ttu-id="2473c-1219">[Stringa](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-1219">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="2473c-1220">Specifica la matrice di colori; ad esempio, "rosso. 2; verde. 4; nero. 7 "</span><span class="sxs-lookup"><span data-stu-id="2473c-1220">Specifies the array of colors; for example, "red .2; green .4; black .7"</span></span> |
| <span data-ttu-id="2473c-1221">Length</span><span class="sxs-lookup"><span data-stu-id="2473c-1221">Length</span></span>     | <span data-ttu-id="2473c-1222">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-1222">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="2473c-1223">Numero di colori nella matrice.</span><span class="sxs-lookup"><span data-stu-id="2473c-1223">Number of colors in the array.</span></span>                                          |



 



| <span data-ttu-id="2473c-1224">Metodi</span><span class="sxs-lookup"><span data-stu-id="2473c-1224">Methods</span></span>     | <span data-ttu-id="2473c-1225">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2473c-1225">Description</span></span>                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2473c-1226">AddColor</span><span class="sxs-lookup"><span data-stu-id="2473c-1226">AddColor</span></span>    | <span data-ttu-id="2473c-1227">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-1227">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="2473c-1228">Aggiunge nuovo colore all'endpoint specificato dalla frazione.</span><span class="sxs-lookup"><span data-stu-id="2473c-1228">Adds new color at endpoint specified by fraction.</span></span> <span data-ttu-id="2473c-1229">Per impostazione predefinita, il nuovo colore è bianco e il valore restituito è.</span><span class="sxs-lookup"><span data-stu-id="2473c-1229">The new color is white by default and is the return value.</span></span> <span data-ttu-id="2473c-1230">Il colore può quindi essere modificato per riferimento.</span><span class="sxs-lookup"><span data-stu-id="2473c-1230">The color can then be changed by reference.</span></span> |
| <span data-ttu-id="2473c-1231">RemoveColor</span><span class="sxs-lookup"><span data-stu-id="2473c-1231">RemoveColor</span></span> | <span data-ttu-id="2473c-1232">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-1232">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="2473c-1233">Rimuove un colore in corrispondenza dell'endpoint specificato dalla frazione.</span><span class="sxs-lookup"><span data-stu-id="2473c-1233">Removes a color at endpoint specified by fraction.</span></span> <span data-ttu-id="2473c-1234">Nota: se 0,0 o 1,0 non esiste, è implicito e il colore bianco viene usato in quel punto.</span><span class="sxs-lookup"><span data-stu-id="2473c-1234">Note: if 0.0 or 1.0 does not exist, it is implied and the color white is used at that point.</span></span>          |



 

<span data-ttu-id="2473c-1235">**Tipo di dati IVgPoints**</span><span class="sxs-lookup"><span data-stu-id="2473c-1235">**IVgPoints datatype**</span></span>

<span data-ttu-id="2473c-1236">Matrice di punti che definiscono una forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-1236">Array of points that define a shape.</span></span>



| <span data-ttu-id="2473c-1237">Attributi</span><span class="sxs-lookup"><span data-stu-id="2473c-1237">Attributes</span></span> | <span data-ttu-id="2473c-1238">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2473c-1238">Description</span></span>                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2473c-1239">Valore</span><span class="sxs-lookup"><span data-stu-id="2473c-1239">Value</span></span>      | <span data-ttu-id="2473c-1240">[Stringa](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-1240">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="2473c-1241">Rappresentazione testuale della matrice.</span><span class="sxs-lookup"><span data-stu-id="2473c-1241">Text representation of array.</span></span>           |
| <span data-ttu-id="2473c-1242">Length</span><span class="sxs-lookup"><span data-stu-id="2473c-1242">Length</span></span>     | <span data-ttu-id="2473c-1243">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-1243">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="2473c-1244">Numero di punti in questa matrice.</span><span class="sxs-lookup"><span data-stu-id="2473c-1244">Number of points in this array.</span></span>        |
| <span data-ttu-id="2473c-1245">Elemento</span><span class="sxs-lookup"><span data-stu-id="2473c-1245">Item</span></span>       | <span data-ttu-id="2473c-1246">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="2473c-1246">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="2473c-1247">Punto in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="2473c-1247">The point at the specified index.</span></span> |



 

<span data-ttu-id="2473c-1248">**Tipo di dati IVgSkewMatrix**</span><span class="sxs-lookup"><span data-stu-id="2473c-1248">**IVgSkewMatrix datatype**</span></span>

<span data-ttu-id="2473c-1249">Matrice utilizzata per le forme inclinate, una matrice di trasformazione prospettica nel formato "*SXX, SXY, SYX, SYY, px, py* " \[ *s* = scale, *p* = Perspective \] .</span><span class="sxs-lookup"><span data-stu-id="2473c-1249">A matrix used for skewing shapes, a perspective transform matrix in the form, "*sxx,sxy,syx,syy,px,py* " \[*s* =scale, *p* =perspective\].</span></span> <span data-ttu-id="2473c-1250">Se l'offset è espresso in unità assolute, *px, py* si trovano in unità Emu ^-1; in caso contrario, si tratta di una frazione inversa della dimensione della forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-1250">If offset is in absolute units, then *px,py* are in emu ^-1 units; otherwise they are an inverse fraction of shape size.</span></span>



| <span data-ttu-id="2473c-1251">Attributi</span><span class="sxs-lookup"><span data-stu-id="2473c-1251">Attributes</span></span>   | <span data-ttu-id="2473c-1252">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2473c-1252">Description</span></span>                                         |
|--------------|-----------------------------------------------------|
| <span data-ttu-id="2473c-1253">XtoX</span><span class="sxs-lookup"><span data-stu-id="2473c-1253">XtoX</span></span>         | <span data-ttu-id="2473c-1254">[Valore Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-1254">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="2473c-1255">YtoX</span><span class="sxs-lookup"><span data-stu-id="2473c-1255">YtoX</span></span>         | <span data-ttu-id="2473c-1256">[Valore Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-1256">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="2473c-1257">XtoY</span><span class="sxs-lookup"><span data-stu-id="2473c-1257">XtoY</span></span>         | <span data-ttu-id="2473c-1258">[Valore Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-1258">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="2473c-1259">YtoY</span><span class="sxs-lookup"><span data-stu-id="2473c-1259">YtoY</span></span>         | <span data-ttu-id="2473c-1260">[Valore Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-1260">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="2473c-1261">PerspectiveX</span><span class="sxs-lookup"><span data-stu-id="2473c-1261">PerspectiveX</span></span> | <span data-ttu-id="2473c-1262">[Valore Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-1262">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="2473c-1263">Prospettiva</span><span class="sxs-lookup"><span data-stu-id="2473c-1263">PerspectiveY</span></span> | <span data-ttu-id="2473c-1264">[Valore Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="2473c-1264">[Double](#data-types-used-in-the-vml-object-model).</span></span> |



 

<span data-ttu-id="2473c-1265">**IVgSkewOffset**</span><span class="sxs-lookup"><span data-stu-id="2473c-1265">**IVgSkewOffset**</span></span>

<span data-ttu-id="2473c-1266">Specifica l'offset dell'asimmetria.</span><span class="sxs-lookup"><span data-stu-id="2473c-1266">Specifies the offset of the skew.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2473c-1267">Attributi</span><span class="sxs-lookup"><span data-stu-id="2473c-1267">Attributes</span></span></th>
<th><span data-ttu-id="2473c-1268">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2473c-1268">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2473c-1269">Valore</span><span class="sxs-lookup"><span data-stu-id="2473c-1269">Value</span></span></td>
<td><span data-ttu-id="2473c-1270"><a href="#data-types-used-in-the-vml-object-model">Stringa</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-1270"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="2473c-1271">Rappresentazione testuale dell'offset.</span><span class="sxs-lookup"><span data-stu-id="2473c-1271">Text representation of offset.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-1272">X</span><span class="sxs-lookup"><span data-stu-id="2473c-1272">X</span></span></td>
<td><span data-ttu-id="2473c-1273"><a href="#data-types-used-in-the-vml-object-model">Valore Double</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-1273"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="2473c-1274">Componente X.</span><span class="sxs-lookup"><span data-stu-id="2473c-1274">X component.</span></span> <span data-ttu-id="2473c-1275">Percentuale o misura.</span><span class="sxs-lookup"><span data-stu-id="2473c-1275">Percentage or measure.</span></span> <span data-ttu-id="2473c-1276">Se non sono presenti unità, il tipo ShapeRelative è implicito; in caso contrario, il tipo assoluto è implicito.</span><span class="sxs-lookup"><span data-stu-id="2473c-1276">If no units, then ShapeRelative type is implied; otherwise Absolute type is implied.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-1277">S</span><span class="sxs-lookup"><span data-stu-id="2473c-1277">Y</span></span></td>
<td><span data-ttu-id="2473c-1278"><a href="#data-types-used-in-the-vml-object-model">Valore Double</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-1278"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="2473c-1279">Componente Y.</span><span class="sxs-lookup"><span data-stu-id="2473c-1279">Y component.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-1280">Tipo</span><span class="sxs-lookup"><span data-stu-id="2473c-1280">Type</span></span></td>
<td><span data-ttu-id="2473c-1281"><strong>VgSkewTransformType</strong>.</span><span class="sxs-lookup"><span data-stu-id="2473c-1281"><strong>VgSkewTransformType</strong>.</span></span> <span data-ttu-id="2473c-1282">Specifica il tipo di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="2473c-1282">Specifies the type of transformation.</span></span> <span data-ttu-id="2473c-1283">I valori validi sono punti interi compresi tra-infinito e infinito.</span><span class="sxs-lookup"><span data-stu-id="2473c-1283">Valid values are integer points ranging between -infinity and infinity.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2473c-1284">Tipo</span><span class="sxs-lookup"><span data-stu-id="2473c-1284">Type</span></span></th>
<th><span data-ttu-id="2473c-1285">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2473c-1285">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2473c-1286">ShapeRelative</span><span class="sxs-lookup"><span data-stu-id="2473c-1286">ShapeRelative</span></span></td>
<td><span data-ttu-id="2473c-1287">I valori dell'offset sono percentuali (rapporti) delle dimensioni della forma originale; ad esempio, il valore 0,5 indica un offset metà della dimensione della forma.</span><span class="sxs-lookup"><span data-stu-id="2473c-1287">The values of the offset are percentages (ratios) of the original shape's size; e.g., a value of 0.5 means an offset half the size of the shape.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-1288">Assoluto</span><span class="sxs-lookup"><span data-stu-id="2473c-1288">Absolute</span></span></td>
<td><span data-ttu-id="2473c-1289">I valori sono unità assolute.</span><span class="sxs-lookup"><span data-stu-id="2473c-1289">The values are absolute units.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2473c-1290">**Tipo di dati IVgVector2D**</span><span class="sxs-lookup"><span data-stu-id="2473c-1290">**IVgVector2D data type**</span></span>

<span data-ttu-id="2473c-1291">Specifica un vettore bidimensionale costituito da due numeri **doppi** .</span><span class="sxs-lookup"><span data-stu-id="2473c-1291">Specifies a two-dimensional vector consisting of two **Double** numbers.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2473c-1292">Attributi</span><span class="sxs-lookup"><span data-stu-id="2473c-1292">Attributes</span></span></th>
<th><span data-ttu-id="2473c-1293">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2473c-1293">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2473c-1294">Valore</span><span class="sxs-lookup"><span data-stu-id="2473c-1294">Value</span></span></td>
<td><span data-ttu-id="2473c-1295"><strong>Stringa</strong>.</span><span class="sxs-lookup"><span data-stu-id="2473c-1295"><strong>String</strong>.</span></span> <span data-ttu-id="2473c-1296">Rappresentazione testuale di entrambi i numeri di vettore separati da uno spazio.</span><span class="sxs-lookup"><span data-stu-id="2473c-1296">Text representation of both vector numbers separated by a space.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-1297">X</span><span class="sxs-lookup"><span data-stu-id="2473c-1297">X</span></span></td>
<td><span data-ttu-id="2473c-1298"><a href="#data-types-used-in-the-vml-object-model">Valore Double</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-1298"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="2473c-1299">Componente X di questo vettore.</span><span class="sxs-lookup"><span data-stu-id="2473c-1299">X component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-1300">S</span><span class="sxs-lookup"><span data-stu-id="2473c-1300">Y</span></span></td>
<td><span data-ttu-id="2473c-1301"><a href="#data-types-used-in-the-vml-object-model">Valore Double</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-1301"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="2473c-1302">Componente Y di questo vettore.</span><span class="sxs-lookup"><span data-stu-id="2473c-1302">Y component of this vector.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-1303">Tipo</span><span class="sxs-lookup"><span data-stu-id="2473c-1303">Type</span></span></td>
<td><span data-ttu-id="2473c-1304"><strong>VgVectorType</strong>.</span><span class="sxs-lookup"><span data-stu-id="2473c-1304"><strong>VgVectorType</strong>.</span></span> <span data-ttu-id="2473c-1305">Unità previste per questo vettore.</span><span class="sxs-lookup"><span data-stu-id="2473c-1305">Expected units for this vector.</span></span> <span data-ttu-id="2473c-1306">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="2473c-1306">Values are:</span></span>
<ul>
<li><span data-ttu-id="2473c-1307">Measure</span><span class="sxs-lookup"><span data-stu-id="2473c-1307">Measure</span></span></li>
<li><span data-ttu-id="2473c-1308">Length</span><span class="sxs-lookup"><span data-stu-id="2473c-1308">Length</span></span></li>
<li><span data-ttu-id="2473c-1309">AngoloInGradi</span><span class="sxs-lookup"><span data-stu-id="2473c-1309">AngleInDegrees</span></span></li>
<li><span data-ttu-id="2473c-1310">Fraction</span><span class="sxs-lookup"><span data-stu-id="2473c-1310">Fraction</span></span></li>
<li><span data-ttu-id="2473c-1311">Numero intero percentuale</span><span class="sxs-lookup"><span data-stu-id="2473c-1311">Number Percentage Integer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2473c-1312">**Tipo di dati IVgVector3D**</span><span class="sxs-lookup"><span data-stu-id="2473c-1312">**IVgVector3D data type**</span></span>

<span data-ttu-id="2473c-1313">Specifica un vettore tridimensionale costituito da tre numeri **doppi** .</span><span class="sxs-lookup"><span data-stu-id="2473c-1313">Specifies a three-dimensional vector consisting of three **Double** numbers.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2473c-1314">Valore</span><span class="sxs-lookup"><span data-stu-id="2473c-1314">Value</span></span></td>
<td><span data-ttu-id="2473c-1315"><strong>Stringa</strong>.</span><span class="sxs-lookup"><span data-stu-id="2473c-1315"><strong>String</strong>.</span></span> <span data-ttu-id="2473c-1316">Rappresentazione testuale di tre numeri di vettore separati da uno spazio.</span><span class="sxs-lookup"><span data-stu-id="2473c-1316">Text representation of three vector numbers separated by a space.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-1317">X</span><span class="sxs-lookup"><span data-stu-id="2473c-1317">X</span></span></td>
<td><span data-ttu-id="2473c-1318"><a href="#data-types-used-in-the-vml-object-model">Valore Double</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-1318"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="2473c-1319">Componente X di questo vettore.</span><span class="sxs-lookup"><span data-stu-id="2473c-1319">X component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-1320">S</span><span class="sxs-lookup"><span data-stu-id="2473c-1320">Y</span></span></td>
<td><span data-ttu-id="2473c-1321"><a href="#data-types-used-in-the-vml-object-model">Valore Double</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-1321"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="2473c-1322">Componente Y di questo vettore.</span><span class="sxs-lookup"><span data-stu-id="2473c-1322">Y component of this vector.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2473c-1323">Z</span><span class="sxs-lookup"><span data-stu-id="2473c-1323">Z</span></span></td>
<td><span data-ttu-id="2473c-1324"><a href="#data-types-used-in-the-vml-object-model">Valore Double</a>.</span><span class="sxs-lookup"><span data-stu-id="2473c-1324"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="2473c-1325">Componente Z di questo vettore.</span><span class="sxs-lookup"><span data-stu-id="2473c-1325">Z component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2473c-1326">Tipo</span><span class="sxs-lookup"><span data-stu-id="2473c-1326">Type</span></span></td>
<td><span data-ttu-id="2473c-1327"><strong>VgVectorType</strong>.</span><span class="sxs-lookup"><span data-stu-id="2473c-1327"><strong>VgVectorType</strong>.</span></span> <span data-ttu-id="2473c-1328">Unità previste per questo vettore.</span><span class="sxs-lookup"><span data-stu-id="2473c-1328">Expected units for this vector.</span></span> <span data-ttu-id="2473c-1329">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="2473c-1329">Values are:</span></span>
<ul>
<li><span data-ttu-id="2473c-1330">Measure</span><span class="sxs-lookup"><span data-stu-id="2473c-1330">Measure</span></span></li>
<li><span data-ttu-id="2473c-1331">Length</span><span class="sxs-lookup"><span data-stu-id="2473c-1331">Length</span></span></li>
<li><span data-ttu-id="2473c-1332">AngoloInGradi</span><span class="sxs-lookup"><span data-stu-id="2473c-1332">AngleInDegrees</span></span></li>
<li><span data-ttu-id="2473c-1333">Fraction</span><span class="sxs-lookup"><span data-stu-id="2473c-1333">Fraction</span></span></li>
<li><span data-ttu-id="2473c-1334">Numero</span><span class="sxs-lookup"><span data-stu-id="2473c-1334">Number</span></span></li>
<li><span data-ttu-id="2473c-1335">Percentuale</span><span class="sxs-lookup"><span data-stu-id="2473c-1335">Percentage</span></span></li>
<li><span data-ttu-id="2473c-1336">Integer</span><span class="sxs-lookup"><span data-stu-id="2473c-1336">Integer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2473c-1337">**Tipo di dati length**</span><span class="sxs-lookup"><span data-stu-id="2473c-1337">**Length data type**</span></span>

<span data-ttu-id="2473c-1338">Numero a virgola mobile con un intervallo compreso tra 0 e infinito.</span><span class="sxs-lookup"><span data-stu-id="2473c-1338">A floating point number with a range from 0 to infinity.</span></span>

<span data-ttu-id="2473c-1339">**Tipo di dati Measure**</span><span class="sxs-lookup"><span data-stu-id="2473c-1339">**Measure data type**</span></span>

<span data-ttu-id="2473c-1340">Numero a virgola mobile da-infinito a infinito.</span><span class="sxs-lookup"><span data-stu-id="2473c-1340">A floating point number from -infinity to infinity.</span></span>

<span data-ttu-id="2473c-1341">**Tipo di dati String**</span><span class="sxs-lookup"><span data-stu-id="2473c-1341">**String data type**</span></span>

<span data-ttu-id="2473c-1342">Dati di tipo carattere di qualsiasi lunghezza.</span><span class="sxs-lookup"><span data-stu-id="2473c-1342">Character data of any length.</span></span>

<span data-ttu-id="2473c-1343">**VgBlackWhiteMode**</span><span class="sxs-lookup"><span data-stu-id="2473c-1343">**VgBlackWhiteMode**</span></span>

<span data-ttu-id="2473c-1344">Modalità di rendering per il bianco e il nero.</span><span class="sxs-lookup"><span data-stu-id="2473c-1344">Rendering mode for black and white.</span></span> <span data-ttu-id="2473c-1345">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="2473c-1345">Possible values are:</span></span>

-   <span data-ttu-id="2473c-1346">**Colore**</span><span class="sxs-lookup"><span data-stu-id="2473c-1346">**Color**</span></span>
-   <span data-ttu-id="2473c-1347">**Auto**</span><span class="sxs-lookup"><span data-stu-id="2473c-1347">**Auto**</span></span>
-   <span data-ttu-id="2473c-1348">**Grigi**</span><span class="sxs-lookup"><span data-stu-id="2473c-1348">**GrayScale**</span></span>
-   <span data-ttu-id="2473c-1349">**LightGrayScale**</span><span class="sxs-lookup"><span data-stu-id="2473c-1349">**LightGrayScale**</span></span>
-   <span data-ttu-id="2473c-1350">**InverseGray**</span><span class="sxs-lookup"><span data-stu-id="2473c-1350">**InverseGray**</span></span>
-   <span data-ttu-id="2473c-1351">**GrayOutline**</span><span class="sxs-lookup"><span data-stu-id="2473c-1351">**GrayOutline**</span></span>
-   <span data-ttu-id="2473c-1352">**BlackTextAndLines**</span><span class="sxs-lookup"><span data-stu-id="2473c-1352">**BlackTextAndLines**</span></span>
-   <span data-ttu-id="2473c-1353">**HighContrast**</span><span class="sxs-lookup"><span data-stu-id="2473c-1353">**HighContrast**</span></span>
-   <span data-ttu-id="2473c-1354">**Nero**</span><span class="sxs-lookup"><span data-stu-id="2473c-1354">**Black**</span></span>
-   <span data-ttu-id="2473c-1355">**White**</span><span class="sxs-lookup"><span data-stu-id="2473c-1355">**White**</span></span>
-   <span data-ttu-id="2473c-1356">**Non disegnato**</span><span class="sxs-lookup"><span data-stu-id="2473c-1356">**Undrawn**</span></span>

<span data-ttu-id="2473c-1357">**Tipo di dati VgFraction**</span><span class="sxs-lookup"><span data-stu-id="2473c-1357">**VgFraction data type**</span></span>

<span data-ttu-id="2473c-1358">Numero a virgola mobile con intervallo compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="2473c-1358">Floating point number with range from 0.0 to 1.0.</span></span> <span data-ttu-id="2473c-1359">È inoltre possibile specificare frazioni come percentuale; ad esempio, "50%".</span><span class="sxs-lookup"><span data-stu-id="2473c-1359">Fractions can also be specified as a percentage; e.g., "50%".</span></span>

<span data-ttu-id="2473c-1360">**Tipo di dati VgTriState**</span><span class="sxs-lookup"><span data-stu-id="2473c-1360">**VgTriState datatype**</span></span>

<span data-ttu-id="2473c-1361">Enumerazione utilizzata per i valori che possono essere uno dei tre stati seguenti:</span><span class="sxs-lookup"><span data-stu-id="2473c-1361">Enumeration used for values that can be one of three states:</span></span>

-   <span data-ttu-id="2473c-1362">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="2473c-1362">**TRUE**</span></span>
-   <span data-ttu-id="2473c-1363">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="2473c-1363">**FALSE**</span></span>
-   <span data-ttu-id="2473c-1364">**MIXED**</span><span class="sxs-lookup"><span data-stu-id="2473c-1364">**MIXED**</span></span>
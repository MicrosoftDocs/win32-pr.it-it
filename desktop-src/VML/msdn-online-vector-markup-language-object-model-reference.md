---
title: Informazioni di riferimento sul modello a oggetti VML
description: Questo argomento descrive VML, una funzionalità deprecata a Internet Explorer Windows 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.
ms.assetid: 68a84c68-3aac-4971-9611-45f52e057708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c387935119babc73442e9b8f307672925bdf71d3
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444822"
---
# <a name="vml-object-model-reference"></a><span data-ttu-id="1b539-104">Informazioni di riferimento sul modello a oggetti VML</span><span class="sxs-lookup"><span data-stu-id="1b539-104">VML Object Model Reference</span></span>

<span data-ttu-id="1b539-105">Questo argomento descrive VML, una funzionalità deprecata a Internet Explorer Windows 9.</span><span class="sxs-lookup"><span data-stu-id="1b539-105">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1b539-106">Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="1b539-106">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1b539-107">A partire da dicembre 2011, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="1b539-107">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1b539-108">Di conseguenza, non viene più gestito attivamente.</span><span class="sxs-lookup"><span data-stu-id="1b539-108">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1b539-109">Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/)</span><span class="sxs-lookup"><span data-stu-id="1b539-109">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1b539-110">Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)</span><span class="sxs-lookup"><span data-stu-id="1b539-110">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1b539-111">In questo argomento</span><span class="sxs-lookup"><span data-stu-id="1b539-111">In this topic:</span></span>

-   [<span data-ttu-id="1b539-112">Introduzione</span><span class="sxs-lookup"><span data-stu-id="1b539-112">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="1b539-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="1b539-113">Example</span></span>](#example)
-   [<span data-ttu-id="1b539-114">Configurazione di VML</span><span class="sxs-lookup"><span data-stu-id="1b539-114">Setting up VML</span></span>](#setting-up-vml)
-   [<span data-ttu-id="1b539-115">Informazioni di riferimento su VML OM</span><span class="sxs-lookup"><span data-stu-id="1b539-115">VML OM Reference</span></span>](#vml-om-reference)
    -   [<span data-ttu-id="1b539-116">Elemento Shape</span><span class="sxs-lookup"><span data-stu-id="1b539-116">Shape element</span></span>](#shape-element)
-   [<span data-ttu-id="1b539-117">Sottoelementi dell'elemento Shape</span><span class="sxs-lookup"><span data-stu-id="1b539-117">Subelements of the Shape Element</span></span>](#subelements-of-the-shape-element)
    -   [<span data-ttu-id="1b539-118">Elemento Background</span><span class="sxs-lookup"><span data-stu-id="1b539-118">Background element</span></span>](#background-element)
    -   [<span data-ttu-id="1b539-119">Elemento Extrusion</span><span class="sxs-lookup"><span data-stu-id="1b539-119">Extrusion element</span></span>](#extrusion-element)
    -   [<span data-ttu-id="1b539-120">Fill - elemento</span><span class="sxs-lookup"><span data-stu-id="1b539-120">Fill element</span></span>](#fill-element)
    -   [<span data-ttu-id="1b539-121">Group - elemento</span><span class="sxs-lookup"><span data-stu-id="1b539-121">Group element</span></span>](#group-element)
    -   [<span data-ttu-id="1b539-122">Elemento Imagedata</span><span class="sxs-lookup"><span data-stu-id="1b539-122">Imagedata element</span></span>](#imagedata-element)
    -   [<span data-ttu-id="1b539-123">Elemento Path</span><span class="sxs-lookup"><span data-stu-id="1b539-123">Path element</span></span>](#path-element)
    -   [<span data-ttu-id="1b539-124">Elemento Shadow</span><span class="sxs-lookup"><span data-stu-id="1b539-124">Shadow element</span></span>](#shadow-element)
    -   [<span data-ttu-id="1b539-125">Elemento Skew</span><span class="sxs-lookup"><span data-stu-id="1b539-125">Skew element</span></span>](#skew-element)
    -   [<span data-ttu-id="1b539-126">Elemento Stroke</span><span class="sxs-lookup"><span data-stu-id="1b539-126">Stroke element</span></span>](#stroke-element)
    -   [<span data-ttu-id="1b539-127">Elemento TextPath</span><span class="sxs-lookup"><span data-stu-id="1b539-127">TextPath element</span></span>](#textpath-element)
-   [<span data-ttu-id="1b539-128">Tipi di dati usati nel modello a oggetti VML</span><span class="sxs-lookup"><span data-stu-id="1b539-128">Data Types Used in the VML Object Model</span></span>](#data-types-used-in-the-vml-object-model)

## <a name="introduction"></a><span data-ttu-id="1b539-129">Introduzione</span><span class="sxs-lookup"><span data-stu-id="1b539-129">Introduction</span></span>

<span data-ttu-id="1b539-130">[Vector Markup Language (VML)](https://www.w3.org/TR/NOTE-datetime.html) è un linguaggio basato su testo che usa [XML](https://www.w3.org/TR/REC-xml.mdl) per estendere il codice HTML allo scopo di visualizzare informazioni grafiche vettoriali.</span><span class="sxs-lookup"><span data-stu-id="1b539-130">[Vector Markup Language (VML)](https://www.w3.org/TR/NOTE-datetime.html) is a text-based language that uses [XML](https://www.w3.org/TR/REC-xml.mdl) to extend HTML for the purpose of displaying vector graphic information.</span></span> <span data-ttu-id="1b539-131">Il modello DOCUMENT OBJECT MODEL (DOM) definisce un'interfaccia a livello di codice per la modifica degli elementi del documento.</span><span class="sxs-lookup"><span data-stu-id="1b539-131">The VML Document Object Model (DOM) defines a programmatic interface for the manipulation of the document elements.</span></span> <span data-ttu-id="1b539-132">In questo modo l'utente può creare e modificare dinamicamente la grafica vettoriale tramite un'interfaccia indipendente dalla piattaforma e dalla lingua.</span><span class="sxs-lookup"><span data-stu-id="1b539-132">This enables the user to dynamically create and modify vector graphics through a platform- and language-neutral interface.</span></span> <span data-ttu-id="1b539-133">Il DOM VML è conforme [Document Object Model](https://www.w3.org/TR/REC-DOM-Level-1/) specifica.</span><span class="sxs-lookup"><span data-stu-id="1b539-133">The VML DOM conforms to the [Document Object Model](https://www.w3.org/TR/REC-DOM-Level-1/) specification.</span></span>

<span data-ttu-id="1b539-134">VML usa [l'elemento Shape](#shape-element) come blocco predefinito di base per le immagini grafiche vettoriali.</span><span class="sxs-lookup"><span data-stu-id="1b539-134">VML uses the [Shape](#shape-element) element as the basic building block for vector graphic images.</span></span> <span data-ttu-id="1b539-135">Dopo aver creato una forma, è possibile modificarla tramite attributi o sottoelementi collegati.</span><span class="sxs-lookup"><span data-stu-id="1b539-135">Once a shape is created, you can modify the shape through attributes or by attached subelements.</span></span> <span data-ttu-id="1b539-136">Ad esempio, per modificare il colore di una forma, assegnare un valore di colore **all'attributo FillColor.**</span><span class="sxs-lookup"><span data-stu-id="1b539-136">For example, to change the color of a shape, assign a color value to the **FillColor** attribute.</span></span>


```HTML
myshape.fillcolor = "red"
```



<span data-ttu-id="1b539-137">Molti attributi di una forma sono anche [sottoelementi](/windows) e hanno i propri attributi, tra cui:</span><span class="sxs-lookup"><span data-stu-id="1b539-137">Several of the attributes of a shape are also [subelements](/windows) and have their own attributes, including the following:</span></span>

-   [<span data-ttu-id="1b539-138">Background</span><span class="sxs-lookup"><span data-stu-id="1b539-138">Background</span></span>](#background-element)
-   [<span data-ttu-id="1b539-139">Estrusione</span><span class="sxs-lookup"><span data-stu-id="1b539-139">Extrusion</span></span>](#extrusion-element)
-   [<span data-ttu-id="1b539-140">Fill</span><span class="sxs-lookup"><span data-stu-id="1b539-140">Fill</span></span>](#fill-element)
-   [<span data-ttu-id="1b539-141">Gruppo</span><span class="sxs-lookup"><span data-stu-id="1b539-141">Group</span></span>](#group-element)
-   [<span data-ttu-id="1b539-142">Imagedata</span><span class="sxs-lookup"><span data-stu-id="1b539-142">Imagedata</span></span>](#imagedata-element)
-   [<span data-ttu-id="1b539-143">Percorso</span><span class="sxs-lookup"><span data-stu-id="1b539-143">Path</span></span>](#path-element)
-   [<span data-ttu-id="1b539-144">Shadow</span><span class="sxs-lookup"><span data-stu-id="1b539-144">Shadow</span></span>](#shadow-element)
-   [<span data-ttu-id="1b539-145">Inclinazione</span><span class="sxs-lookup"><span data-stu-id="1b539-145">Skew</span></span>](#skew-element)
-   [<span data-ttu-id="1b539-146">infarto</span><span class="sxs-lookup"><span data-stu-id="1b539-146">Stroke</span></span>](#stroke-element)
-   [<span data-ttu-id="1b539-147">Percorso di testo</span><span class="sxs-lookup"><span data-stu-id="1b539-147">TextPath</span></span>](#textpath-element)

<span data-ttu-id="1b539-148">VmL OM usa diversi tipi [di dati](/windows) per definire i parametri.</span><span class="sxs-lookup"><span data-stu-id="1b539-148">The VML OM uses several [data types](/windows) to define parameters.</span></span> <span data-ttu-id="1b539-149">I tipi di dati preceduti da "Vg" sono enumerazioni e quelli preceduti da "IVg" sono oggetti .</span><span class="sxs-lookup"><span data-stu-id="1b539-149">Datatypes prefixed with "Vg" are enumerations and those prefixed with "IVg" are objects.</span></span> <span data-ttu-id="1b539-150">Fare clic qui per un elenco.</span><span class="sxs-lookup"><span data-stu-id="1b539-150">Click here for a list.</span></span> <span data-ttu-id="1b539-151">I tipi di dati secondari sono elencati con parametri specifici.</span><span class="sxs-lookup"><span data-stu-id="1b539-151">Minor datatypes are listed with specific parameters.</span></span>

## <a name="example"></a><span data-ttu-id="1b539-152">Esempio</span><span class="sxs-lookup"><span data-stu-id="1b539-152">Example</span></span>

<span data-ttu-id="1b539-153">Il codice VBScript seguente illustra come creare una forma semplice:</span><span class="sxs-lookup"><span data-stu-id="1b539-153">The following VBScript code shows how to create a simple shape:</span></span>


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



<span data-ttu-id="1b539-154">Nell'esempio precedente viene creata una forma usando il Document Object Model **createElement**.</span><span class="sxs-lookup"><span data-stu-id="1b539-154">In the above example, a shape is created by using the Document Object Model method **CreateElement**.</span></span> <span data-ttu-id="1b539-155">La forma è una forma Rect predefinita VML.</span><span class="sxs-lookup"><span data-stu-id="1b539-155">The shape is a VML predefined Rect shape.</span></span> <span data-ttu-id="1b539-156">Anche se l'oggetto esiste, non può far parte del documento fino a quando non viene allegato al documento.</span><span class="sxs-lookup"><span data-stu-id="1b539-156">Even though the object exists, it cannot be part of the document until it is attached to the document.</span></span> <span data-ttu-id="1b539-157">Usando il **metodo AppendChild,** Rect viene reso figlio di un **elemento DIV** denominato MyDiv.</span><span class="sxs-lookup"><span data-stu-id="1b539-157">Using the **AppendChild** method, the Rect is made a child of a **DIV** element called MyDiv.</span></span> <span data-ttu-id="1b539-158">Alcuni attributi di stile minimi (**Position**, **Width**, **Height**, **Top**, **Left**) sono impostati per assegnare alla forma una dimensione specifica.</span><span class="sxs-lookup"><span data-stu-id="1b539-158">A few minimum style attributes (**Position**, **Width**, **Height**, **Top**, **Left**) are set to give the shape a specific size.</span></span> <span data-ttu-id="1b539-159">Infine, un colore viene assegnato con **l'attributo FillColor.**</span><span class="sxs-lookup"><span data-stu-id="1b539-159">Finally, a color is assigned with the **FillColor** attribute.</span></span> <span data-ttu-id="1b539-160">Si noti che è possibile usare qualsiasi linguaggio di scripting o qualsiasi linguaggio che Document Object Model interfacce.</span><span class="sxs-lookup"><span data-stu-id="1b539-160">Note that any scripting language or any language that can work with Document Object Model interfaces can be used.</span></span>

## <a name="setting-up-vml"></a><span data-ttu-id="1b539-161">Configurazione di VML</span><span class="sxs-lookup"><span data-stu-id="1b539-161">Setting up VML</span></span>

<span data-ttu-id="1b539-162">Un'implementazione di VML è tramite Microsoft Internet Explorer 5.0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="1b539-162">One implementation of VML is through Microsoft Internet Explorer 5.0 or greater.</span></span> <span data-ttu-id="1b539-163">Per configurare correttamente l'oggetto di rendering in una pagina Web, è necessario eseguire le aggiunte seguenti:</span><span class="sxs-lookup"><span data-stu-id="1b539-163">To set up the rendering object correctly in a Web page, the following additions must be made:</span></span>

1.  <span data-ttu-id="1b539-164">Lo schema deve essere configurato nell'elemento iniziale</span><span class="sxs-lookup"><span data-stu-id="1b539-164">The schema must be set up in the initial</span></span> <HTML> <span data-ttu-id="1b539-165">come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="1b539-165">tag as follows:</span></span>
    ```HTML
    <HTML xmlns:v="urn:schemas-microsoft-com:vml">
    ```

    

2.  <span data-ttu-id="1b539-166">Il comportamento di rendering deve far parte dello stile del documento:</span><span class="sxs-lookup"><span data-stu-id="1b539-166">The rendering behavior must be part of the document's style:</span></span>
    ```HTML
    <STYLE>
    v\:* { behavior: url(#default#VML); display:inline-block}
    </STYLE>
    ```

    

<span data-ttu-id="1b539-167">Di seguito viene illustrata una pagina Web HTML di esempio configurata correttamente per VML che mostra la creazione dinamica di una forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-167">The following shows a sample HTML Web page set up correctly for VML showing the dynamic creation of a shape.</span></span>


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



<span data-ttu-id="1b539-168">Si noti che nelle versioni beta erano necessari un tag oggetto ActiveX e uno stile di comportamento diverso.</span><span class="sxs-lookup"><span data-stu-id="1b539-168">Note that in beta versions, an ActiveX object tag and a different behavior style was required.</span></span>

## <a name="vml-om-reference"></a><span data-ttu-id="1b539-169">Informazioni di riferimento su VML OM</span><span class="sxs-lookup"><span data-stu-id="1b539-169">VML OM Reference</span></span>

<span data-ttu-id="1b539-170">Questo riferimento definisce [l'elemento Shape,](#shape-element) [i sottoelementi](/windows) [e](/windows) i tipi di dati usati dal modello a oggetti di VML.</span><span class="sxs-lookup"><span data-stu-id="1b539-170">This reference defines the [Shape](#shape-element) element, [subelements](/windows), and [data types](/windows) that are used by the object model of VML.</span></span>

### <a name="shape-element"></a><span data-ttu-id="1b539-171">Elemento Shape</span><span class="sxs-lookup"><span data-stu-id="1b539-171">Shape element</span></span>

<span data-ttu-id="1b539-172">Le forme sono i blocchi predefiniti delle immagini grafiche definite da Vector Markup Language (VML).</span><span class="sxs-lookup"><span data-stu-id="1b539-172">Shapes are the building blocks of graphical images defined by Vector Markup Language (VML).</span></span> <span data-ttu-id="1b539-173">La forma è l'elemento di primo livello e diversi sottoelementi consentono di definire la natura di ogni forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-173">The shape is the top-level element and several subelements help define the nature of each shape.</span></span>

<span data-ttu-id="1b539-174">VML fornisce forme predefinite:</span><span class="sxs-lookup"><span data-stu-id="1b539-174">VML provides predefined shapes:</span></span>

<span data-ttu-id="1b539-175">**Attributi di forma**</span><span class="sxs-lookup"><span data-stu-id="1b539-175">**Shape Attributes**</span></span>

-   <span data-ttu-id="1b539-176">**Arc**</span><span class="sxs-lookup"><span data-stu-id="1b539-176">**Arc**</span></span>
-   <span data-ttu-id="1b539-177">**Curva**</span><span class="sxs-lookup"><span data-stu-id="1b539-177">**Curve**</span></span>
-   <span data-ttu-id="1b539-178">**Linea**</span><span class="sxs-lookup"><span data-stu-id="1b539-178">**Line**</span></span>
-   <span data-ttu-id="1b539-179">**Polilinea**</span><span class="sxs-lookup"><span data-stu-id="1b539-179">**PolyLine**</span></span>
-   <span data-ttu-id="1b539-180">**Rect**</span><span class="sxs-lookup"><span data-stu-id="1b539-180">**Rect**</span></span>
-   <span data-ttu-id="1b539-181">**RoundRect**</span><span class="sxs-lookup"><span data-stu-id="1b539-181">**RoundRect**</span></span>



|   <span data-ttu-id="1b539-182">Sottoelemento</span><span class="sxs-lookup"><span data-stu-id="1b539-182">Subelement</span></span>           |    <span data-ttu-id="1b539-183">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b539-183">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b539-184">Adj</span><span class="sxs-lookup"><span data-stu-id="1b539-184">Adj</span></span>          | <span data-ttu-id="1b539-185">[IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-185">[IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md).</span></span> <span data-ttu-id="1b539-186">Elenco delimitato da virgole di numeri che sono i parametri per le formule guida che definiscono il percorso della forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-186">A comma-delimited list of numbers that are the parameters for the guide formulas that define the path of the shape.</span></span> <span data-ttu-id="1b539-187">I valori possono essere omessi per consentire l'uso delle impostazioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="1b539-187">Values may be omitted to allow for using defaults.</span></span> <span data-ttu-id="1b539-188">Possono essere presenti fino a 8 valori di regolazione.</span><span class="sxs-lookup"><span data-stu-id="1b539-188">There can be up to 8 adjustment values.</span></span>                                                                                                   |
| <span data-ttu-id="1b539-189">ALT</span><span class="sxs-lookup"><span data-stu-id="1b539-189">Alt</span></span>          | <span data-ttu-id="1b539-190">Stringa.</span><span class="sxs-lookup"><span data-stu-id="1b539-190">String.</span></span> <span data-ttu-id="1b539-191">Testo alternativo associato alla forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-191">Alternative text associated with shape.</span></span> <span data-ttu-id="1b539-192">Usato per l'esplorazione non grafica.</span><span class="sxs-lookup"><span data-stu-id="1b539-192">Used for non-graphical browsing.</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="1b539-193">Pulsante</span><span class="sxs-lookup"><span data-stu-id="1b539-193">Button</span></span>       | <span data-ttu-id="1b539-194">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-194">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="1b539-195">Visualizza il comportamento del pulsante al clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="1b539-195">Displays button behavior on click.</span></span>                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="1b539-196">BWMode</span><span class="sxs-lookup"><span data-stu-id="1b539-196">BWMode</span></span>       | <span data-ttu-id="1b539-197">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-197">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="1b539-198">Determina la modalità di rendering della forma nella visualizzazione in bianco e nero nelle app o quando viene stampata su stampanti in bianco e nero.</span><span class="sxs-lookup"><span data-stu-id="1b539-198">Determines how shape will render in black-and-white view in apps or when printed to black-and-white printers.</span></span> <span data-ttu-id="1b539-199">I valori includono: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span><span class="sxs-lookup"><span data-stu-id="1b539-199">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="1b539-200">Impostazione predefinita: **Auto.**</span><span class="sxs-lookup"><span data-stu-id="1b539-200">Default: **Auto**.</span></span> |
| <span data-ttu-id="1b539-201">BWNormal</span><span class="sxs-lookup"><span data-stu-id="1b539-201">BWNormal</span></span>     | <span data-ttu-id="1b539-202">VgBlackWhiteMode.</span><span class="sxs-lookup"><span data-stu-id="1b539-202">VgBlackWhiteMode.</span></span> <span data-ttu-id="1b539-203">Quando BWMode è Auto, questa proprietà viene consultata per informazioni su come eseguire il rendering della forma in bianco e nero normale.</span><span class="sxs-lookup"><span data-stu-id="1b539-203">When BWMode is Auto, this property is consulted for how to render the shape in normal black and white.</span></span> <span data-ttu-id="1b539-204">I valori includono: **Color,** **Auto,** **GrayScale,** **LightGrayScale,** **InverseGray,** **GrayOutline,** **BlackTextAndLines,** **HighContrast,** **Black,** **White,** **Undrawn.**</span><span class="sxs-lookup"><span data-stu-id="1b539-204">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="1b539-205">Impostazione predefinita: **Auto.**</span><span class="sxs-lookup"><span data-stu-id="1b539-205">Default: **Auto**.</span></span>                                                |
| <span data-ttu-id="1b539-206">BWPure</span><span class="sxs-lookup"><span data-stu-id="1b539-206">BWPure</span></span>       | <span data-ttu-id="1b539-207">VgBlackWhiteMode.</span><span class="sxs-lookup"><span data-stu-id="1b539-207">VgBlackWhiteMode.</span></span> <span data-ttu-id="1b539-208">Quando BWMode è Auto, questa proprietà viene consultata per informazioni su come eseguire il rendering della forma in B/W puro.</span><span class="sxs-lookup"><span data-stu-id="1b539-208">When BWMode is Auto, this property is consulted for how to render the shape in pure B/W.</span></span> <span data-ttu-id="1b539-209">I valori includono: **Color,** **Auto,** **GrayScale,** **LightGrayScale,** **InverseGray,** **GrayOutline,** **BlackTextAndLines,** **HighContrast,** **Black,** **White,** **Undrawn.**</span><span class="sxs-lookup"><span data-stu-id="1b539-209">Values include: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**.</span></span> <span data-ttu-id="1b539-210">Impostazione predefinita: **Auto.**</span><span class="sxs-lookup"><span data-stu-id="1b539-210">Default: **Auto**.</span></span>                                                              |
| <span data-ttu-id="1b539-211">Forme figlio</span><span class="sxs-lookup"><span data-stu-id="1b539-211">ChildShapes</span></span>  | <span data-ttu-id="1b539-212">IVgGroupShapes.</span><span class="sxs-lookup"><span data-stu-id="1b539-212">IVgGroupShapes.</span></span> <span data-ttu-id="1b539-213">Raccolta di altre forme in questo gruppo.</span><span class="sxs-lookup"><span data-stu-id="1b539-213">A collection of other shapes in this group.</span></span> <span data-ttu-id="1b539-214">Questa raccolta supporta i metodi Standard Length e Item.</span><span class="sxs-lookup"><span data-stu-id="1b539-214">This collection supports the standard Length and Item methods.</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="1b539-215">Chromakey</span><span class="sxs-lookup"><span data-stu-id="1b539-215">Chromakey</span></span>    | <span data-ttu-id="1b539-216">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-216">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="1b539-217">Valore del colore che sarà trasparente e mostra tutto ciò che si nasconde dietro la forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-217">A color value that will be transparent and show anything behind the shape.</span></span>                                                                                                                                                                                                                                                             |
| <span data-ttu-id="1b539-218">Control1</span><span class="sxs-lookup"><span data-stu-id="1b539-218">Control1</span></span>     | <span data-ttu-id="1b539-219">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-219">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="1b539-220">Punto di controllo per la curva.</span><span class="sxs-lookup"><span data-stu-id="1b539-220">Control point for curve.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="1b539-221">Controllo2</span><span class="sxs-lookup"><span data-stu-id="1b539-221">Control2</span></span>     | <span data-ttu-id="1b539-222">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-222">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="1b539-223">Punto di controllo per la curva.</span><span class="sxs-lookup"><span data-stu-id="1b539-223">Control point for curve.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="1b539-224">CoordOrigin</span><span class="sxs-lookup"><span data-stu-id="1b539-224">CoordOrigin</span></span>  | <span data-ttu-id="1b539-225">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md) Coordinate nell'angolo superiore sinistro del rettangolo del contenitore.</span><span class="sxs-lookup"><span data-stu-id="1b539-225">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md) The coordinates at the top left corner of the container rectangle.</span></span> <span data-ttu-id="1b539-226">Intervallo compreso tra 0 e infinito.</span><span class="sxs-lookup"><span data-stu-id="1b539-226">Range from 0 to infinity.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="1b539-227">CoordSize</span><span class="sxs-lookup"><span data-stu-id="1b539-227">CoordSize</span></span>    | <span data-ttu-id="1b539-228">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-228">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="1b539-229">Larghezza e altezza dello spazio delle coordinate all'interno del rettangolo di riferimento di questa forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-229">The width and height of the coordinate space inside the reference rectangle of this shape.</span></span> <span data-ttu-id="1b539-230">Se non viene specificato, corrisponde alla larghezza e all'altezza del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="1b539-230">If it is not specified, it is the same as the width and height of the rectangle.</span></span> <span data-ttu-id="1b539-231">Intervallo compreso tra 0 e infinito.</span><span class="sxs-lookup"><span data-stu-id="1b539-231">Range from 0 to infinity.</span></span> <span data-ttu-id="1b539-232">Valore predefinito: "1000,1000".</span><span class="sxs-lookup"><span data-stu-id="1b539-232">Default: "1000,1000".</span></span>                                                                                               |
| <span data-ttu-id="1b539-233">EndAngle</span><span class="sxs-lookup"><span data-stu-id="1b539-233">EndAngle</span></span>     | <span data-ttu-id="1b539-234">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-234">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="1b539-235">Angolo finale della forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-235">End angle of shape.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="1b539-236">Estrusione</span><span class="sxs-lookup"><span data-stu-id="1b539-236">Extrusion</span></span>    | <span data-ttu-id="1b539-237">IVgExtrusion.</span><span class="sxs-lookup"><span data-stu-id="1b539-237">IVgExtrusion.</span></span> <span data-ttu-id="1b539-238">Specifica il valore dell'oggetto Extrusion per questa forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-238">Specifies the Extrusion object value for this shape.</span></span> <span data-ttu-id="1b539-239">Per informazioni dettagliate, vedere l'elemento [Estrusione.](msdn-online-vml-extrusion-element.md)</span><span class="sxs-lookup"><span data-stu-id="1b539-239">See the [Extrusion](msdn-online-vml-extrusion-element.md) element for details.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="1b539-240">Fill</span><span class="sxs-lookup"><span data-stu-id="1b539-240">Fill</span></span>         | <span data-ttu-id="1b539-241">VgFillFormat.</span><span class="sxs-lookup"><span data-stu-id="1b539-241">VgFillFormat.</span></span> <span data-ttu-id="1b539-242">Specifica il valore di riempimento per questa forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-242">Specifies the fill value for this shape.</span></span> <span data-ttu-id="1b539-243">Per altri [dettagli, vedere](msdn-online-vml-fill-element.md) l'elemento Fill.</span><span class="sxs-lookup"><span data-stu-id="1b539-243">See the [Fill](msdn-online-vml-fill-element.md) element for more details.</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="1b539-244">Fillcolor</span><span class="sxs-lookup"><span data-stu-id="1b539-244">FillColor</span></span>    | <span data-ttu-id="1b539-245">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-245">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="1b539-246">Colore principale del pennello da usare per riempire il percorso di questa forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-246">The primary color of the brush to use to fill the path of this shape.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="1b539-247">Riempito</span><span class="sxs-lookup"><span data-stu-id="1b539-247">Filled</span></span>       | <span data-ttu-id="1b539-248">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-248">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="1b539-249">Se True, il percorso che definisce la forma verrà riempito.</span><span class="sxs-lookup"><span data-stu-id="1b539-249">If True, the path defining the shape will be filled.</span></span> <span data-ttu-id="1b539-250">Per impostazione predefinita, verrà riempito con un colore a tinta unita a meno che non sia presente un sottoelemento Fill che specifica proprietà di riempimento più complesse.</span><span class="sxs-lookup"><span data-stu-id="1b539-250">By default, it will be filled using a solid color unless there is a Fill subelement that specifies more complex fill properties.</span></span> <span data-ttu-id="1b539-251">Se False, il riempimento è trasparente.</span><span class="sxs-lookup"><span data-stu-id="1b539-251">If False, the fill is transparent.</span></span>                                                                                                           |
| <span data-ttu-id="1b539-252">Flip</span><span class="sxs-lookup"><span data-stu-id="1b539-252">Flip</span></span>         | <span data-ttu-id="1b539-253">VgFlipOrientation.</span><span class="sxs-lookup"><span data-stu-id="1b539-253">VgFlipOrientation.</span></span> <span data-ttu-id="1b539-254">I valori sono: X Y XY YX</span><span class="sxs-lookup"><span data-stu-id="1b539-254">Values are: X Y XY YX</span></span>                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="1b539-255">ForceDash</span><span class="sxs-lookup"><span data-stu-id="1b539-255">ForceDash</span></span>    | <span data-ttu-id="1b539-256">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-256">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="1b539-257">Indica che deve essere eseguito il rendering di un contorno tratteggiato quando non è presente alcuna linea e nessun riempimento per una forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-257">Indication that a dashed outline should be rendered when there is no line and no fill for a shape.</span></span> <span data-ttu-id="1b539-258">Questo comportamento è in genere utile per rendere visibili le forme invisibili nelle applicazioni di modifica in modo che possano essere selezionate e gestite, ad esempio in una mappa immagine.</span><span class="sxs-lookup"><span data-stu-id="1b539-258">This behavior is generally useful for making invisible shapes visible in editing applications so they can be selected and operated on, such as in an image map.</span></span>                                                                 |
| <span data-ttu-id="1b539-259">Formule</span><span class="sxs-lookup"><span data-stu-id="1b539-259">Formulas</span></span>     | <span data-ttu-id="1b539-260">IVgFormulas.</span><span class="sxs-lookup"><span data-stu-id="1b539-260">IVgFormulas.</span></span> <span data-ttu-id="1b539-261">Matrice di formule che definisce una forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-261">An array of formulas that defines a shape.</span></span>                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="1b539-262">Da</span><span class="sxs-lookup"><span data-stu-id="1b539-262">From</span></span>         | <span data-ttu-id="1b539-263">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-263">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="1b539-264">Punto di partenza della linea.</span><span class="sxs-lookup"><span data-stu-id="1b539-264">Starting point of line.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="1b539-265">Href</span><span class="sxs-lookup"><span data-stu-id="1b539-265">HRef</span></span>         | <span data-ttu-id="1b539-266">[Stringa](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-266">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="1b539-267">URL a cui passare se si fa clic su questa forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-267">The URL to jump to if this shape is clicked.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="1b539-268">ImageData</span><span class="sxs-lookup"><span data-stu-id="1b539-268">ImageData</span></span>    | <span data-ttu-id="1b539-269">IVgImageData.</span><span class="sxs-lookup"><span data-stu-id="1b539-269">IVgImageData.</span></span> <span data-ttu-id="1b539-270">Informazioni sull'immagine se la forma è un'immagine.</span><span class="sxs-lookup"><span data-stu-id="1b539-270">Image information if the shape is a picture.</span></span> <span data-ttu-id="1b539-271">Per altre informazioni, vedere l'elemento ImageData.</span><span class="sxs-lookup"><span data-stu-id="1b539-271">See the ImageData element for more information.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="1b539-272">OnEd</span><span class="sxs-lookup"><span data-stu-id="1b539-272">OnEd</span></span>         | <span data-ttu-id="1b539-273">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-273">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="1b539-274">Nasconde tutti i punti di controllo tranne quelli in alto a sinistra e in basso a destra, come nei punti di manipolazione per un segmento di linea retta.</span><span class="sxs-lookup"><span data-stu-id="1b539-274">Hides all handles except the top left and bottom right, as in the handles for a straight line segment.</span></span>                                                                                                                                                                                                                             |
| <span data-ttu-id="1b539-275">Opacità</span><span class="sxs-lookup"><span data-stu-id="1b539-275">Opacity</span></span>      | <span data-ttu-id="1b539-276">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-276">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="1b539-277">Opacità dell'intera forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-277">The opacity of the entire shape.</span></span> <span data-ttu-id="1b539-278">Numero compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="1b539-278">A number between 0.0 and 1.0.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="1b539-279">Percorso</span><span class="sxs-lookup"><span data-stu-id="1b539-279">Path</span></span>         | <span data-ttu-id="1b539-280">IVgPath.</span><span class="sxs-lookup"><span data-stu-id="1b539-280">IVgPath.</span></span> <span data-ttu-id="1b539-281">Stringa contenente i comandi che definiscono il percorso.</span><span class="sxs-lookup"><span data-stu-id="1b539-281">A string containing the commands that define the path.</span></span>                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="1b539-282">Punti</span><span class="sxs-lookup"><span data-stu-id="1b539-282">Points</span></span>       | <span data-ttu-id="1b539-283">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-283">[IVgPoints](msdn-online-vml-ivgpoints-data-type.md).</span></span> <span data-ttu-id="1b539-284">Raccolta di punti che definiscono una forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-284">A collection of points defining a shape.</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="1b539-285">Stampa</span><span class="sxs-lookup"><span data-stu-id="1b539-285">Print</span></span>        | <span data-ttu-id="1b539-286">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-286">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="1b539-287">Se True, questa forma deve essere stampata.</span><span class="sxs-lookup"><span data-stu-id="1b539-287">If True, this shape is meant to be printed.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="1b539-288">Rotazione</span><span class="sxs-lookup"><span data-stu-id="1b539-288">Rotation</span></span>     | <span data-ttu-id="1b539-289">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-289">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="1b539-290">Imposta la rotazione della forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-290">Sets rotation of shape.</span></span> <span data-ttu-id="1b539-291">Il valore viene propagato allo stile della forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-291">Value is propagated to the shape style.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="1b539-292">Scalabilità</span><span class="sxs-lookup"><span data-stu-id="1b539-292">Scale</span></span>        | <span data-ttu-id="1b539-293">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-293">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="1b539-294">Scala della forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-294">Scale of shape.</span></span>                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="1b539-295">Ombreggiatura</span><span class="sxs-lookup"><span data-stu-id="1b539-295">Shadow</span></span>       | <span data-ttu-id="1b539-296">IVgShadow.</span><span class="sxs-lookup"><span data-stu-id="1b539-296">IVgShadow.</span></span> <span data-ttu-id="1b539-297">Specifica l'ombreggiatura per questa forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-297">Specifies the shadow for this shape.</span></span> <span data-ttu-id="1b539-298">Per informazioni [dettagliate, vedere l'elemento](msdn-online-vml-shadow-element.md) Shadow.</span><span class="sxs-lookup"><span data-stu-id="1b539-298">See the [Shadow](msdn-online-vml-shadow-element.md) element for details.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="1b539-299">Spt</span><span class="sxs-lookup"><span data-stu-id="1b539-299">Spt</span></span>          | <span data-ttu-id="1b539-300">Riservato.</span><span class="sxs-lookup"><span data-stu-id="1b539-300">Reserved.</span></span>                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="1b539-301">StartAngle</span><span class="sxs-lookup"><span data-stu-id="1b539-301">StartAngle</span></span>   | <span data-ttu-id="1b539-302">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-302">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span> <span data-ttu-id="1b539-303">Angolo iniziale della forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-303">Start angle of shape.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="1b539-304">Stroke</span><span class="sxs-lookup"><span data-stu-id="1b539-304">Stroke</span></span>       | <span data-ttu-id="1b539-305">VgStrokeFormat.</span><span class="sxs-lookup"><span data-stu-id="1b539-305">VgStrokeFormat.</span></span> <span data-ttu-id="1b539-306">Per informazioni dettagliate, vedere Elemento Stroke.</span><span class="sxs-lookup"><span data-stu-id="1b539-306">See Stroke element for details.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="1b539-307">StrokeColor</span><span class="sxs-lookup"><span data-stu-id="1b539-307">StrokeColor</span></span>  | <span data-ttu-id="1b539-308">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-308">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="1b539-309">Colore principale del pennello da usare per tracciare il percorso di questa forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-309">The primary color of the brush to use to stroke the path of this shape.</span></span>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="1b539-310">Accarezzò</span><span class="sxs-lookup"><span data-stu-id="1b539-310">Stroked</span></span>      | <span data-ttu-id="1b539-311">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-311">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="1b539-312">Se True, il tracciato che definisce la forma verrà tracciato.</span><span class="sxs-lookup"><span data-stu-id="1b539-312">If True, the path defining the shape will be stroked.</span></span>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="1b539-313">StrokeWeight</span><span class="sxs-lookup"><span data-stu-id="1b539-313">StrokeWeight</span></span> | <span data-ttu-id="1b539-314">[VGLength](msdn-online-vml-vglength.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-314">[VGLength](msdn-online-vml-vglength.md).</span></span> <span data-ttu-id="1b539-315">Larghezza del pennello da usare per tracciare il tracciato.</span><span class="sxs-lookup"><span data-stu-id="1b539-315">The width of the brush to use to stroke the path.</span></span> <span data-ttu-id="1b539-316">Intervalli compresi tra 0 e 1584.</span><span class="sxs-lookup"><span data-stu-id="1b539-316">Ranges between 0 and 1584.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="1b539-317">TextPath</span><span class="sxs-lookup"><span data-stu-id="1b539-317">TextPath</span></span>     | <span data-ttu-id="1b539-318">IVgTextPath.</span><span class="sxs-lookup"><span data-stu-id="1b539-318">IVgTextPath.</span></span> <span data-ttu-id="1b539-319">Specifica l'oggetto TextPath della forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-319">Specifies the TextPath object of the shape.</span></span> <span data-ttu-id="1b539-320">Per altre [informazioni, vedere l'elemento TextPath.](msdn-online-vml-textpath-element.md)</span><span class="sxs-lookup"><span data-stu-id="1b539-320">See the [TextPath](msdn-online-vml-textpath-element.md) element for more information.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="1b539-321">Per</span><span class="sxs-lookup"><span data-stu-id="1b539-321">To</span></span>           | <span data-ttu-id="1b539-322">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-322">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="1b539-323">Punto finale della linea.</span><span class="sxs-lookup"><span data-stu-id="1b539-323">End point of line.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="1b539-324">Tipo</span><span class="sxs-lookup"><span data-stu-id="1b539-324">Type</span></span>         | <span data-ttu-id="1b539-325">Stringa.</span><span class="sxs-lookup"><span data-stu-id="1b539-325">String.</span></span> <span data-ttu-id="1b539-326">Tipo di forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-326">Type of shape.</span></span>                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="subelements-of-the-shape-element"></a><span data-ttu-id="1b539-327">Sottoelementi dell'elemento Shape</span><span class="sxs-lookup"><span data-stu-id="1b539-327">Subelements of the Shape Element</span></span>

<span data-ttu-id="1b539-328">I sottoelementi seguenti fanno parte del modello a oggetti VML.</span><span class="sxs-lookup"><span data-stu-id="1b539-328">The following subelements are part of the VML object model.</span></span>

-   [<span data-ttu-id="1b539-329">Background</span><span class="sxs-lookup"><span data-stu-id="1b539-329">Background</span></span>](#background-element)
-   [<span data-ttu-id="1b539-330">Estrusione</span><span class="sxs-lookup"><span data-stu-id="1b539-330">Extrusion</span></span>](#extrusion-element)
-   [<span data-ttu-id="1b539-331">Fill</span><span class="sxs-lookup"><span data-stu-id="1b539-331">Fill</span></span>](#fill-element)
-   [<span data-ttu-id="1b539-332">Gruppo</span><span class="sxs-lookup"><span data-stu-id="1b539-332">Group</span></span>](#group-element)
-   [<span data-ttu-id="1b539-333">Imagedata</span><span class="sxs-lookup"><span data-stu-id="1b539-333">Imagedata</span></span>](#imagedata-element)
-   [<span data-ttu-id="1b539-334">Percorso</span><span class="sxs-lookup"><span data-stu-id="1b539-334">Path</span></span>](#path-element)
-   [<span data-ttu-id="1b539-335">Shadow</span><span class="sxs-lookup"><span data-stu-id="1b539-335">Shadow</span></span>](#shadow-element)
-   [<span data-ttu-id="1b539-336">Inclinazione</span><span class="sxs-lookup"><span data-stu-id="1b539-336">Skew</span></span>](#skew-element)
-   [<span data-ttu-id="1b539-337">infarto</span><span class="sxs-lookup"><span data-stu-id="1b539-337">Stroke</span></span>](#stroke-element)
-   [<span data-ttu-id="1b539-338">TextPath</span><span class="sxs-lookup"><span data-stu-id="1b539-338">TextPath</span></span>](#textpath-element)

### <a name="background-element"></a><span data-ttu-id="1b539-339">Elemento Background</span><span class="sxs-lookup"><span data-stu-id="1b539-339">Background element</span></span>

<span data-ttu-id="1b539-340">Descrive il riempimento dello sfondo di una pagina usando riempimenti VML.</span><span class="sxs-lookup"><span data-stu-id="1b539-340">Describes the fill of the background of a page using VML fills.</span></span>


|   <span data-ttu-id="1b539-341">Attributo</span><span class="sxs-lookup"><span data-stu-id="1b539-341">Attribute</span></span>        |   <span data-ttu-id="1b539-342">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b539-342">Description</span></span>                                                                                                                                                                                      |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b539-343">BWMode</span><span class="sxs-lookup"><span data-stu-id="1b539-343">BWMode</span></span>    | <span data-ttu-id="1b539-344">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-344">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="1b539-345">Determina la modalità di rendering della forma nella visualizzazione in bianco e nero nelle applicazioni o quando viene stampata.</span><span class="sxs-lookup"><span data-stu-id="1b539-345">Determines how shape will render in black-and-white view in applications or when printed.</span></span>                                     |
| <span data-ttu-id="1b539-346">BWNormal</span><span class="sxs-lookup"><span data-stu-id="1b539-346">BWNormal</span></span>  | <span data-ttu-id="1b539-347">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-347">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="1b539-348">Quando BWMode è Auto, questa proprietà viene consultata per informazioni su come eseguire il rendering della forma in bianco e nero normale.</span><span class="sxs-lookup"><span data-stu-id="1b539-348">When BWMode is Auto, this property is consulted for how to render the shape in normal black and white.</span></span>                        |
| <span data-ttu-id="1b539-349">BWPure</span><span class="sxs-lookup"><span data-stu-id="1b539-349">BWPure</span></span>    | <span data-ttu-id="1b539-350">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-350">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span> <span data-ttu-id="1b539-351">Quando BWMode è Auto, questa proprietà viene consultata per informazioni su come eseguire il rendering della forma in bianco e nero puro.</span><span class="sxs-lookup"><span data-stu-id="1b539-351">When BWMode is Auto, this property is consulted for how to render the shape in pure black and white.</span></span>                          |
| <span data-ttu-id="1b539-352">Fill</span><span class="sxs-lookup"><span data-stu-id="1b539-352">Fill</span></span>      | <span data-ttu-id="1b539-353">VgFillFormat.</span><span class="sxs-lookup"><span data-stu-id="1b539-353">VgFillFormat.</span></span> <span data-ttu-id="1b539-354">Specifica il riempimento per questa forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-354">Specifies the fill for this shape.</span></span> <span data-ttu-id="1b539-355">Per [altre informazioni,](msdn-online-vml-fill-element.md) vedere Elemento Fill.</span><span class="sxs-lookup"><span data-stu-id="1b539-355">See [Fill](msdn-online-vml-fill-element.md) element for more information.</span></span>                                                             |
| <span data-ttu-id="1b539-356">Fillcolor</span><span class="sxs-lookup"><span data-stu-id="1b539-356">FillColor</span></span> | <span data-ttu-id="1b539-357">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-357">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="1b539-358">Colore principale del pennello da usare per riempire il percorso di questa forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-358">The primary color of the brush to use to fill the path of this shape.</span></span> <span data-ttu-id="1b539-359">Duplicato del valore Color nell'elemento Fill.</span><span class="sxs-lookup"><span data-stu-id="1b539-359">Duplicate of the Color value in the Fill element.</span></span> <span data-ttu-id="1b539-360">Il valore predefinito è bianco.</span><span class="sxs-lookup"><span data-stu-id="1b539-360">The default is white.</span></span> |



 

### <a name="extrusion-element"></a><span data-ttu-id="1b539-361">Elemento Extrusion</span><span class="sxs-lookup"><span data-stu-id="1b539-361">Extrusion element</span></span>

<span data-ttu-id="1b539-362">Descrive un'estrusione 3D della forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-362">Describes a 3-D extrusion of the shape.</span></span>

<span data-ttu-id="1b539-363">**Attributes (Attributi)**</span><span class="sxs-lookup"><span data-stu-id="1b539-363">**Attributes**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b539-364">AutoRotationCenter</span><span class="sxs-lookup"><span data-stu-id="1b539-364">AutoRotationCenter</span></span></td>
<td><span data-ttu-id="1b539-365"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-365"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="1b539-366">Se True, il centro di rotazione del gruppo di oggetti 3D (in realtà è presente un solo oggetto nel gruppo) viene determinato automaticamente come il centro del gruppo; in caso contrario, è determinato dai parametri RotationCenter, che sono una frazione della forma con 0,0,0 come centro.</span><span class="sxs-lookup"><span data-stu-id="1b539-366">If True, the center of rotation of the group of 3-D objects (in fact there is only ever one object in the group) is determined automatically to be the center of the group; otherwise it is determined by the RotationCenter parameters, which are a fraction of the shape with 0,0,0 being the center.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-367">BackDepth</span><span class="sxs-lookup"><span data-stu-id="1b539-367">BackDepth</span></span></td>
<td><span data-ttu-id="1b539-368"><a href="msdn-online-vml-vglength.md"><strong>VgLength</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-368"><a href="msdn-online-vml-vglength.md"><strong>VgLength</strong></a>.</span></span> <span data-ttu-id="1b539-369">Quantità di estrusione all'indietro.</span><span class="sxs-lookup"><span data-stu-id="1b539-369">Amount of backward extrusion.</span></span> <span data-ttu-id="1b539-370">È compreso tra 0 e 32767.</span><span class="sxs-lookup"><span data-stu-id="1b539-370">Ranges from 0 to 32767.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-371">Luminosità</span><span class="sxs-lookup"><span data-stu-id="1b539-371">Brightness</span></span></td>
<td><span data-ttu-id="1b539-372"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-372"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="1b539-373">Luminosità complessiva della scena.</span><span class="sxs-lookup"><span data-stu-id="1b539-373">Overall brightness of the scene.</span></span> <span data-ttu-id="1b539-374">Il valore &quot; predefinito è 20.000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="1b539-374">Default is &quot;20,000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-375">Color</span><span class="sxs-lookup"><span data-stu-id="1b539-375">Color</span></span></td>
<td><span data-ttu-id="1b539-376"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-376"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="1b539-377">Colore dell'estrusione.</span><span class="sxs-lookup"><span data-stu-id="1b539-377">The color of the extrusion.</span></span> <span data-ttu-id="1b539-378">Usato solo se ColorMode è Custom.</span><span class="sxs-lookup"><span data-stu-id="1b539-378">Only used if ColorMode is Custom.</span></span> <span data-ttu-id="1b539-379">In caso contrario, Auto imposta il colore dell'effetto di estrusione sullo stesso colore di FillColor.</span><span class="sxs-lookup"><span data-stu-id="1b539-379">Otherwise, Auto sets the extrusion effect color to the same as FillColor.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-380">ColorMode</span><span class="sxs-lookup"><span data-stu-id="1b539-380">ColorMode</span></span></td>
<td><span data-ttu-id="1b539-381">Vg3DColorMode.</span><span class="sxs-lookup"><span data-stu-id="1b539-381">Vg3DColorMode.</span></span> <span data-ttu-id="1b539-382">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="1b539-382">Values are:</span></span>
<ul>
<li><span data-ttu-id="1b539-383">Auto (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1b539-383">Auto (default)</span></span></li>
<li><span data-ttu-id="1b539-384">Personalizzato</span><span class="sxs-lookup"><span data-stu-id="1b539-384">Custom</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-385">Diffusione</span><span class="sxs-lookup"><span data-stu-id="1b539-385">Diffusity</span></span></td>
<td><span data-ttu-id="1b539-386"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-386"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="1b539-387">Rapporto tra evento imprevisto e luce riflessa diffusamente.</span><span class="sxs-lookup"><span data-stu-id="1b539-387">The ratio of incident to diffusely reflected light.</span></span> <span data-ttu-id="1b539-388">I valori minori di 1,0 sono normali, ma i valori superiori a uno possono generare effetti interessanti.</span><span class="sxs-lookup"><span data-stu-id="1b539-388">Values less than 1.0 are normal but values higher than one can generate interesting effects.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-389">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1b539-389">Edge</span></span></td>
<td><span data-ttu-id="1b539-390"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-390"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="1b539-391">Imposta le dimensioni di un bordo smussato arrotondato simulato.</span><span class="sxs-lookup"><span data-stu-id="1b539-391">Sets the size of a simulated rounded beveled edge.</span></span> <span data-ttu-id="1b539-392">È compreso tra 0 e 32767 in pts a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="1b539-392">Ranges from 0 to 32767 in floating point pts.</span></span> <span data-ttu-id="1b539-393">Il valore predefinito &quot; è 1pt. &quot;</span><span class="sxs-lookup"><span data-stu-id="1b539-393">Default is &quot;1pt&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-394">Facet</span><span class="sxs-lookup"><span data-stu-id="1b539-394">Facet</span></span></td>
<td><span data-ttu-id="1b539-395"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-395"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="1b539-396">Imposta il facet della scena.</span><span class="sxs-lookup"><span data-stu-id="1b539-396">Sets the facet of the scene.</span></span> <span data-ttu-id="1b539-397">Il valore &quot; predefinito è 30.000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="1b539-397">Default is &quot;30,000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-398">ForeDepth</span><span class="sxs-lookup"><span data-stu-id="1b539-398">ForeDepth</span></span></td>
<td><span data-ttu-id="1b539-399"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-399"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="1b539-400">Quantità di estrusione in avanti.</span><span class="sxs-lookup"><span data-stu-id="1b539-400">Amount of forward extrusion.</span></span> <span data-ttu-id="1b539-401">È compreso tra 0 e 32767.</span><span class="sxs-lookup"><span data-stu-id="1b539-401">Ranges from 0 to 32767.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-402">LightFace</span><span class="sxs-lookup"><span data-stu-id="1b539-402">LightFace</span></span></td>
<td><span data-ttu-id="1b539-403"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-403"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="1b539-404">Determina se la parte anteriore dell'oggetto risponderà alle modifiche dell'illuminazione 3D, ad esempio quando un oggetto ruota.</span><span class="sxs-lookup"><span data-stu-id="1b539-404">Determimes whether the front face of the object will respond to changes in the 3-D lighting, e.g., when an object rotates.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-405">LightHarsh</span><span class="sxs-lookup"><span data-stu-id="1b539-405">LightHarsh</span></span></td>
<td><span data-ttu-id="1b539-406"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-406"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="1b539-407">Illuminazione dura per la sorgente di luce primaria.</span><span class="sxs-lookup"><span data-stu-id="1b539-407">Harsh lighting for the primary light source.</span></span> <span data-ttu-id="1b539-408">Il valore predefinito è False.</span><span class="sxs-lookup"><span data-stu-id="1b539-408">Default is False.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-409">LightHarsh2</span><span class="sxs-lookup"><span data-stu-id="1b539-409">LightHarsh2</span></span></td>
<td><span data-ttu-id="1b539-410"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-410"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="1b539-411">Illuminazione dura per la sorgente di luce secondaria.</span><span class="sxs-lookup"><span data-stu-id="1b539-411">Harsh lighting for the secondary light source.</span></span> <span data-ttu-id="1b539-412">Il valore predefinito è False.</span><span class="sxs-lookup"><span data-stu-id="1b539-412">Default is False.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-413">LightLevel</span><span class="sxs-lookup"><span data-stu-id="1b539-413">LightLevel</span></span></td>
<td><span data-ttu-id="1b539-414"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-414"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span></span> <span data-ttu-id="1b539-415">Intensità della sorgente di luce primaria.</span><span class="sxs-lookup"><span data-stu-id="1b539-415">Intensity of the primary light source.</span></span> <span data-ttu-id="1b539-416">Il valore predefinito &quot; è 38000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="1b539-416">Default is &quot;38000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-417">LightLevel2</span><span class="sxs-lookup"><span data-stu-id="1b539-417">LightLevel2</span></span></td>
<td><span data-ttu-id="1b539-418"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-418"><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>.</span></span> <span data-ttu-id="1b539-419">Intensità della sorgente di luce secondaria.</span><span class="sxs-lookup"><span data-stu-id="1b539-419">Intensity of the secondary light source.</span></span> <span data-ttu-id="1b539-420">Il valore predefinito &quot; è 38000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="1b539-420">Default is &quot;38000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-421">LightPosition</span><span class="sxs-lookup"><span data-stu-id="1b539-421">LightPosition</span></span></td>
<td><span data-ttu-id="1b539-422">Vector3d.</span><span class="sxs-lookup"><span data-stu-id="1b539-422">Vector3D.</span></span> <span data-ttu-id="1b539-423">Posizione della sorgente di luce primaria.</span><span class="sxs-lookup"><span data-stu-id="1b539-423">Position of the primary light source.</span></span> <span data-ttu-id="1b539-424">Il valore &quot; predefinito è 50000,0,10000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="1b539-424">Default is &quot;50000,0,10000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-425">LightPosition2</span><span class="sxs-lookup"><span data-stu-id="1b539-425">LightPosition2</span></span></td>
<td><span data-ttu-id="1b539-426">Vector3d.</span><span class="sxs-lookup"><span data-stu-id="1b539-426">Vector3D.</span></span> <span data-ttu-id="1b539-427">Posizione della sorgente di luce secondaria.</span><span class="sxs-lookup"><span data-stu-id="1b539-427">Position of the secondary light source.</span></span> <span data-ttu-id="1b539-428">Il valore &quot; predefinito è -50000,0,10000 &quot; .</span><span class="sxs-lookup"><span data-stu-id="1b539-428">Default is &quot;-50000,0,10000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-429">LockRotationCenter</span><span class="sxs-lookup"><span data-stu-id="1b539-429">LockRotationCenter</span></span></td>
<td><span data-ttu-id="1b539-430"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-430"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="1b539-431">&quot;Lockrotationcenter indica che la rotazione del gruppo è definita in base ai gradi rotation-angle[1] circa l'asse y nella pagina seguita da &quot; rotation-angle[0] gradi circa l'asse x.</span><span class="sxs-lookup"><span data-stu-id="1b539-431">&quot;Lockrotationcenter&quot; means that the rotation of the group is defined to be by rotation-angle[1] degrees about the y-axis on the page followed by rotation-angle[0] degrees about the x-axis.</span></span> <span data-ttu-id="1b539-432">Quando LockRotationCenter è False, la rotazione viene definita in base ai gradi dell'angolo di orientamento rispetto al vettore definito dall'orientamento.</span><span class="sxs-lookup"><span data-stu-id="1b539-432">When LockRotationCenter is False, the rotation is defined to be by orientation-angle degrees about the vector defined by orientation.</span></span> <span data-ttu-id="1b539-433">Ad esempio, lockrotationcenter=false orientationangle=45 orientation=(0,1,0) equivale a lockrotationcenter=true rotationangle=(0,45).</span><span class="sxs-lookup"><span data-stu-id="1b539-433">So, for example, lockrotationcenter=false orientationangle=45 orientation=(0,1,0) is equivalent to lockrotationcenter=true rotationangle=(0,45).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-434">Metallico</span><span class="sxs-lookup"><span data-stu-id="1b539-434">Metal</span></span></td>
<td><span data-ttu-id="1b539-435"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-435"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="1b539-436">Fa sì che la luce riflessa specularmente sia il colore del materiale anziché il colore della sorgente di luce, rendendo l'oggetto più metallico.</span><span class="sxs-lookup"><span data-stu-id="1b539-436">Causes specularly reflected light to be the material color instead of the light source color, making the object seem more metallic.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-437">On</span><span class="sxs-lookup"><span data-stu-id="1b539-437">On</span></span></td>
<td><span data-ttu-id="1b539-438"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-438"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="1b539-439">Attiva e disattiva la visualizzazione dell'effetto di estrusione.</span><span class="sxs-lookup"><span data-stu-id="1b539-439">Turns the display of the extrusion effect on and off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-440">Orientamento</span><span class="sxs-lookup"><span data-stu-id="1b539-440">Orientation</span></span></td>
<td><span data-ttu-id="1b539-441">Vector3d.</span><span class="sxs-lookup"><span data-stu-id="1b539-441">Vector3D.</span></span> <span data-ttu-id="1b539-442">Orientamento della fotocamera.</span><span class="sxs-lookup"><span data-stu-id="1b539-442">Orientation of the camera.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-443">OrientationAngle</span><span class="sxs-lookup"><span data-stu-id="1b539-443">OrientationAngle</span></span></td>
<td><span data-ttu-id="1b539-444"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-444"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="1b539-445">Angolo tra l'orientamento della fotocamera e il piano xy.</span><span class="sxs-lookup"><span data-stu-id="1b539-445">Angle between the orientation of the camera and the xy plane.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-446">Aereo</span><span class="sxs-lookup"><span data-stu-id="1b539-446">Plane</span></span></td>
<td><span data-ttu-id="1b539-447">Vg3DExtrudePlane.</span><span class="sxs-lookup"><span data-stu-id="1b539-447">Vg3DExtrudePlane.</span></span> <span data-ttu-id="1b539-448">Consente l'estrusione da piani ortogonali al piano dello schermo.</span><span class="sxs-lookup"><span data-stu-id="1b539-448">Allows extrusion from planes orthogonal to the screen plane.</span></span> <span data-ttu-id="1b539-449">Richiede che foreDepth e BackDepth siano specificati in unità di disegno anziché in emus.</span><span class="sxs-lookup"><span data-stu-id="1b539-449">Requires ForeDepth and BackDepth to be specified in drawing units instead of emus.</span></span> <span data-ttu-id="1b539-450">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="1b539-450">Values are:</span></span>
<ul>
<li><span data-ttu-id="1b539-451">Xy</span><span class="sxs-lookup"><span data-stu-id="1b539-451">XY</span></span></li>
<li><span data-ttu-id="1b539-452">Zx</span><span class="sxs-lookup"><span data-stu-id="1b539-452">ZX</span></span></li>
<li><span data-ttu-id="1b539-453">Yz</span><span class="sxs-lookup"><span data-stu-id="1b539-453">YZ</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-454">Rendering</span><span class="sxs-lookup"><span data-stu-id="1b539-454">Render</span></span></td>
<td><span data-ttu-id="1b539-455">Vg3DRenderMode.</span><span class="sxs-lookup"><span data-stu-id="1b539-455">Vg3DRenderMode.</span></span> <span data-ttu-id="1b539-456">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="1b539-456">Values are:</span></span>
<ul>
<li><span data-ttu-id="1b539-457">Solid (valore predefinito)</span><span class="sxs-lookup"><span data-stu-id="1b539-457">Solid (default)</span></span></li>
<li><span data-ttu-id="1b539-458">Wireframe</span><span class="sxs-lookup"><span data-stu-id="1b539-458">WireFrame</span></span></li>
<li><span data-ttu-id="1b539-459">BoundingCube</span><span class="sxs-lookup"><span data-stu-id="1b539-459">BoundingCube</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-460">RotationAngle</span><span class="sxs-lookup"><span data-stu-id="1b539-460">RotationAngle</span></span></td>
<td><span data-ttu-id="1b539-461"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-461"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="1b539-462">AngleX, AngleY o AngleZ è controllato dall'attributo ShapeRotation.</span><span class="sxs-lookup"><span data-stu-id="1b539-462">AngleX, AngleY, or AngleZ is controlled by the ShapeRotation attribute.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-463">RotationCenter</span><span class="sxs-lookup"><span data-stu-id="1b539-463">RotationCenter</span></span></td>
<td><span data-ttu-id="1b539-464">Vector3d.</span><span class="sxs-lookup"><span data-stu-id="1b539-464">Vector3D.</span></span> <span data-ttu-id="1b539-465">Centro di rotazione.</span><span class="sxs-lookup"><span data-stu-id="1b539-465">Center of rotation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-466">Luminosità</span><span class="sxs-lookup"><span data-stu-id="1b539-466">Shininess</span></span></td>
<td><span data-ttu-id="1b539-467"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-467"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="1b539-468">Determina la concentrazione o la diffusione della reflection speculare.</span><span class="sxs-lookup"><span data-stu-id="1b539-468">Determines how concentrated or spread out specular reflection is.</span></span> <span data-ttu-id="1b539-469">Un valore elevato è compreso tra 8 e 10 e si avvicina a uno mirror e un valore basso è compreso tra 2 e 3 e indica un abbigliamento con paillettes approssimativo.</span><span class="sxs-lookup"><span data-stu-id="1b539-469">A high value would be 8 to 10 and would approximate a mirror, and a low value would be 2 to 3 and would approximate sequined clothing.</span></span> <span data-ttu-id="1b539-470">Sono consigliati valori da 3 a 7.</span><span class="sxs-lookup"><span data-stu-id="1b539-470">Values of 3 to 7 are recommended.</span></span> <span data-ttu-id="1b539-471">I valori alti rifletteranno le sorgenti di luce di puntina.</span><span class="sxs-lookup"><span data-stu-id="1b539-471">High values will reflect pinpoint light sources.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-472">SkewAmt</span><span class="sxs-lookup"><span data-stu-id="1b539-472">SkewAmt</span></span></td>
<td><span data-ttu-id="1b539-473"><a href="#data-types-used-in-the-vml-object-model">VgPercentage</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-473"><a href="#data-types-used-in-the-vml-object-model">VgPercentage</a>.</span></span> <span data-ttu-id="1b539-474">Se Type è Parallel, l'attributo determina la quantità di agitazione.</span><span class="sxs-lookup"><span data-stu-id="1b539-474">If Type is Parallel, attribute determines the amount of skew.</span></span> <span data-ttu-id="1b539-475">È compreso tra 0 e 100.</span><span class="sxs-lookup"><span data-stu-id="1b539-475">Ranges from 0 to 100.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-476">SkewAngle</span><span class="sxs-lookup"><span data-stu-id="1b539-476">SkewAngle</span></span></td>
<td><span data-ttu-id="1b539-477"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-477"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="1b539-478">Se Type è Parallel, l'attributo determina il grado di agitazione.</span><span class="sxs-lookup"><span data-stu-id="1b539-478">If Type is Parallel, attribute determines the degree of skew.</span></span> <span data-ttu-id="1b539-479">Il valore predefinito &quot; è -45. &quot;</span><span class="sxs-lookup"><span data-stu-id="1b539-479">Default is &quot;-45&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-480">Specularità</span><span class="sxs-lookup"><span data-stu-id="1b539-480">Specularity</span></span></td>
<td><span data-ttu-id="1b539-481"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-481"><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>.</span></span> <span data-ttu-id="1b539-482">Rapporto tra evento imprevisto e luce riflessa in modo speculare.</span><span class="sxs-lookup"><span data-stu-id="1b539-482">The ratio of incident to specularly reflected light.</span></span> <span data-ttu-id="1b539-483">I valori minori di 1,0 sono normali, ma i valori superiori a uno possono generare effetti interessanti.</span><span class="sxs-lookup"><span data-stu-id="1b539-483">Values less than 1.0 are normal but values higher than one can generate interesting effects.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-484">Tipo</span><span class="sxs-lookup"><span data-stu-id="1b539-484">Type</span></span></td>
<td><span data-ttu-id="1b539-485">VgExtrusionType.</span><span class="sxs-lookup"><span data-stu-id="1b539-485">VgExtrusionType.</span></span> <span data-ttu-id="1b539-486">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="1b539-486">Values are:</span></span>
<ul>
<li><span data-ttu-id="1b539-487">Parallelo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1b539-487">Parallel (default)</span></span></li>
<li><span data-ttu-id="1b539-488">Prospettiva</span><span class="sxs-lookup"><span data-stu-id="1b539-488">Perspective</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-489">Vista</span><span class="sxs-lookup"><span data-stu-id="1b539-489">Viewpoint</span></span></td>
<td><span data-ttu-id="1b539-490">Vector3d.</span><span class="sxs-lookup"><span data-stu-id="1b539-490">Vector3D.</span></span> <span data-ttu-id="1b539-491">Punto da cui viene visualizzata la scena.</span><span class="sxs-lookup"><span data-stu-id="1b539-491">The point where the scene is being viewed from.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-492">ViewpointOrigin</span><span class="sxs-lookup"><span data-stu-id="1b539-492">ViewpointOrigin</span></span></td>
<td><span data-ttu-id="1b539-493"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-493"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="1b539-494">Può avere valori da 0,5 a -0,5 per posizionare l'origine del punto di vista all'interno del rettangolo di selezione della forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-494">Can have values from 0.5 to -0.5 to position the origin of the viewpoint within the shape bounding box.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="fill-element"></a><span data-ttu-id="1b539-495">Elemento Fill</span><span class="sxs-lookup"><span data-stu-id="1b539-495">Fill element</span></span>

<span data-ttu-id="1b539-496">Descrive come riempire un percorso per i riempimenti più complessi rispetto a un colore a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="1b539-496">Describes how a path should be filled for fills more complex than a solid color.</span></span>

<span data-ttu-id="1b539-497">**Attributes (Attributi)**</span><span class="sxs-lookup"><span data-stu-id="1b539-497">**Attributes**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b539-498">AlignShape</span><span class="sxs-lookup"><span data-stu-id="1b539-498">AlignShape</span></span></td>
<td><span data-ttu-id="1b539-499"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-499"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="1b539-500">Allineare l'immagine alla forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-500">Align the image with the shape.</span></span> <span data-ttu-id="1b539-501">Se False, allineare l'immagine alla finestra.</span><span class="sxs-lookup"><span data-stu-id="1b539-501">If False, align image with window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-502">Angle</span><span class="sxs-lookup"><span data-stu-id="1b539-502">Angle</span></span></td>
<td><span data-ttu-id="1b539-503"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-503"><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>.</span></span> <span data-ttu-id="1b539-504">Angolo lungo il quale va la sfumatura.</span><span class="sxs-lookup"><span data-stu-id="1b539-504">The angle along which the gradient goes.</span></span> <span data-ttu-id="1b539-505">0 gradi è lungo l'asse orizzontale da sinistra a destra.</span><span class="sxs-lookup"><span data-stu-id="1b539-505">0 degrees is along the horizontal axis from left to right.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-506">Aspetto</span><span class="sxs-lookup"><span data-stu-id="1b539-506">Aspect</span></span></td>
<td><span data-ttu-id="1b539-507"><strong>VgAspectType</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b539-507"><strong>VgAspectType</strong>.</span></span> <span data-ttu-id="1b539-508">L'attributo ImageSize verrà modificato per mantenere l'aspetto dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="1b539-508">ImageSize attribute will be adjusted to preserve the aspect of the image.</span></span> <span data-ttu-id="1b539-509">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="1b539-509">Values include:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1b539-510">Valore</span><span class="sxs-lookup"><span data-stu-id="1b539-510">Value</span></span></th>
<th><span data-ttu-id="1b539-511">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b539-511">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b539-512">Ignora</span><span class="sxs-lookup"><span data-stu-id="1b539-512">Ignore</span></span></td>
<td><span data-ttu-id="1b539-513">Ignorare i problemi relativi all'aspetto.</span><span class="sxs-lookup"><span data-stu-id="1b539-513">Ignore aspect issues.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-514">Atleast</span><span class="sxs-lookup"><span data-stu-id="1b539-514">AtLeast</span></span></td>
<td><span data-ttu-id="1b539-515">L'immagine è grande almeno quanto le dimensioni dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="1b539-515">Image is at least as big as the image size.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-516">AtMost</span><span class="sxs-lookup"><span data-stu-id="1b539-516">AtMost</span></span></td>
<td><span data-ttu-id="1b539-517">Le dimensioni dell'immagine non sono maggiori delle dimensioni dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="1b539-517">Image is no bigger than image size.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-518">Color</span><span class="sxs-lookup"><span data-stu-id="1b539-518">Color</span></span></td>
<td><span data-ttu-id="1b539-519"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> Colore di riempimento principale.</span><span class="sxs-lookup"><span data-stu-id="1b539-519"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> The main fill color.</span></span> <span data-ttu-id="1b539-520">Uguale all'attributo FillColor nella forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-520">Same as FillColor attribute in shape.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-521">Color2</span><span class="sxs-lookup"><span data-stu-id="1b539-521">Color2</span></span></td>
<td><span data-ttu-id="1b539-522"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-522"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="1b539-523">Colore secondario per un riempimento quando il tipo di immagine è Pattern o un riempimento sfumato.</span><span class="sxs-lookup"><span data-stu-id="1b539-523">The secondary color for a fill when image type is Pattern or a gradient fill.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-524">Colori</span><span class="sxs-lookup"><span data-stu-id="1b539-524">Colors</span></span></td>
<td><span data-ttu-id="1b539-525"><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-525"><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>.</span></span> <span data-ttu-id="1b539-526">Colori intermedi nella sfumatura e le relative posizioni lungo la sfumatura, ad esempio, &quot; 30% rosso, 70% blu, 90% &quot; verde.</span><span class="sxs-lookup"><span data-stu-id="1b539-526">Intermediate colors in the gradient and their relative positions along the gradient, e.g., &quot;30% red, 70% blue, 90% green&quot;.</span></span> <span data-ttu-id="1b539-527">Il colore primario (attributo Color nella forma) è 0% e il colore secondario (attributo Color2) è 100%.</span><span class="sxs-lookup"><span data-stu-id="1b539-527">Primary color (Color attribute in shape) is 0% and secondary color (Color2 attribute) is 100%.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-528">Focus</span><span class="sxs-lookup"><span data-stu-id="1b539-528">Focus</span></span></td>
<td><span data-ttu-id="1b539-529"><a href="#data-types-used-in-the-vml-object-model">VgSignedPercentage</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-529"><a href="#data-types-used-in-the-vml-object-model">VgSignedPercentage</a>.</span></span> <span data-ttu-id="1b539-530">Punto focale per il riempimento sfumato lineare.</span><span class="sxs-lookup"><span data-stu-id="1b539-530">Focal point for linear gradient fill.</span></span> <span data-ttu-id="1b539-531">I valori vanno da -100 a +100.</span><span class="sxs-lookup"><span data-stu-id="1b539-531">Values go from -100 to +100.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-532">FocusPosition</span><span class="sxs-lookup"><span data-stu-id="1b539-532">FocusPosition</span></span></td>
<td><span data-ttu-id="1b539-533"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-533"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="1b539-534">Posizione del rettangolo più interno per le sfumature radiali.</span><span class="sxs-lookup"><span data-stu-id="1b539-534">Position of the innermost rectangle for radial gradients.</span></span> <span data-ttu-id="1b539-535">Il vettore è una frazione (0,0 - 1,0) della larghezza e dell'altezza della forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-535">The vector is a fraction (0.0 - 1.0) of the shape's width and height.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-536">FocusSize</span><span class="sxs-lookup"><span data-stu-id="1b539-536">FocusSize</span></span></td>
<td><span data-ttu-id="1b539-537"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Dimensioni del rettangolo più interno per le sfumature radiali.</span><span class="sxs-lookup"><span data-stu-id="1b539-537"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Size of the innermost rectangle for radial gradients.</span></span> <span data-ttu-id="1b539-538">Il vettore è una frazione (da 0,0 a 1,0) della larghezza e dell'altezza della forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-538">The vector is a fraction (0.0 to 1.0) of the shape's width and height.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-539">Metodo</span><span class="sxs-lookup"><span data-stu-id="1b539-539">Method</span></span></td>
<td><span data-ttu-id="1b539-540">VgSigmaType.</span><span class="sxs-lookup"><span data-stu-id="1b539-540">VgSigmaType.</span></span> <span data-ttu-id="1b539-541">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="1b539-541">Values include:</span></span>
<ul>
<li><span data-ttu-id="1b539-542">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1b539-542">None</span></span></li>
<li><span data-ttu-id="1b539-543">Lineari</span><span class="sxs-lookup"><span data-stu-id="1b539-543">Linear</span></span></li>
<li><span data-ttu-id="1b539-544">Sigma</span><span class="sxs-lookup"><span data-stu-id="1b539-544">Sigma</span></span></li>
<li><span data-ttu-id="1b539-545">Qualsiasi</span><span class="sxs-lookup"><span data-stu-id="1b539-545">Any</span></span></li>
</ul>
<p><span data-ttu-id="1b539-546">Il valore predefinito è Sigma.</span><span class="sxs-lookup"><span data-stu-id="1b539-546">Default is Sigma.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-547">On</span><span class="sxs-lookup"><span data-stu-id="1b539-547">On</span></span></td>
<td><span data-ttu-id="1b539-548"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-548"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="1b539-549">Attiva la visualizzazione del riempimento.</span><span class="sxs-lookup"><span data-stu-id="1b539-549">Turns fill display on.</span></span> <span data-ttu-id="1b539-550">Uguale all'attributo Fill nella forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-550">Same as Fill attribute in shape.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-551">Opacità</span><span class="sxs-lookup"><span data-stu-id="1b539-551">Opacity</span></span></td>
<td><span data-ttu-id="1b539-552"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-552"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="1b539-553">Opacità del riempimento.</span><span class="sxs-lookup"><span data-stu-id="1b539-553">Opacity of the fill.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-554">Opacità2</span><span class="sxs-lookup"><span data-stu-id="1b539-554">Opacity2</span></span></td>
<td><span data-ttu-id="1b539-555"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-555"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="1b539-556">Opacità secondaria per le sfumature.</span><span class="sxs-lookup"><span data-stu-id="1b539-556">The secondary opacity for gradients.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-557">Origine</span><span class="sxs-lookup"><span data-stu-id="1b539-557">Origin</span></span></td>
<td><span data-ttu-id="1b539-558"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-558"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="1b539-559">Punto relativo all'angolo superiore sinistro dell'immagine considerata come origine dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="1b539-559">Point relative to upper left corner of the image that is treated as the origin of the image.</span></span> <span data-ttu-id="1b539-560">Il valore predefinito è il centro dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="1b539-560">Default is the center of the image.</span></span> <span data-ttu-id="1b539-561">Il vettore è una frazione (da 0,0 a 1,0) della larghezza e dell'altezza dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="1b539-561">The vector is a fraction (from 0.0 to 1.0) of the image's width and height.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-562">Posizione</span><span class="sxs-lookup"><span data-stu-id="1b539-562">Position</span></span></td>
<td><span data-ttu-id="1b539-563"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-563"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="1b539-564">Punto nel rettangolo di riferimento della forma per posizionare l'origine dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="1b539-564">Point in the reference rectangle of the shape to position the origin of the image.</span></span> <span data-ttu-id="1b539-565">Il valore predefinito è il centro del rettangolo del contenitore.</span><span class="sxs-lookup"><span data-stu-id="1b539-565">Default is the center of the container rectangle.</span></span> <span data-ttu-id="1b539-566">Il vettore è una frazione (0,0 - 1,0) della larghezza e dell'altezza dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="1b539-566">The vector is a fraction (0.0 - 1.0) of the image's width and height.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-567">Dimensione</span><span class="sxs-lookup"><span data-stu-id="1b539-567">Size</span></span></td>
<td><span data-ttu-id="1b539-568"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-568"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="1b539-569">Dimensioni dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="1b539-569">The size of the image.</span></span> <span data-ttu-id="1b539-570">Il valore predefinito è la dimensione in pixel dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="1b539-570">Default is pixel size of the image.</span></span> <span data-ttu-id="1b539-571">Può essere specificato in coordinate assolute o in percentuale.</span><span class="sxs-lookup"><span data-stu-id="1b539-571">May be specified in absolute coordinates or percentage.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-572">Src</span><span class="sxs-lookup"><span data-stu-id="1b539-572">Src</span></span></td>
<td><span data-ttu-id="1b539-573"><a href="#data-types-used-in-the-vml-object-model">Stringa</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-573"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="1b539-574">URL di un'immagine da caricare per i riempimenti di immagine e motivo.</span><span class="sxs-lookup"><span data-stu-id="1b539-574">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="1b539-575">Questo attributo deve essere sempre presente e puntare a dati immagine validi per visualizzare un'immagine.</span><span class="sxs-lookup"><span data-stu-id="1b539-575">This attribute must always be present and point to valid image data for a picture to appear.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-576">Tipo</span><span class="sxs-lookup"><span data-stu-id="1b539-576">Type</span></span></td>
<td><span data-ttu-id="1b539-577">VgFillType.</span><span class="sxs-lookup"><span data-stu-id="1b539-577">VgFillType.</span></span> <span data-ttu-id="1b539-578">indicati di seguito.</span><span class="sxs-lookup"><span data-stu-id="1b539-578">May be one of the following types:</span></span>
<ul>
<li><span data-ttu-id="1b539-579">Sfondo</span><span class="sxs-lookup"><span data-stu-id="1b539-579">Background</span></span></li>
<li><span data-ttu-id="1b539-580">Frame</span><span class="sxs-lookup"><span data-stu-id="1b539-580">Frame</span></span></li>
<li><span data-ttu-id="1b539-581">Sfumatura</span><span class="sxs-lookup"><span data-stu-id="1b539-581">Gradient</span></span></li>
<li><span data-ttu-id="1b539-582">GradientCenter</span><span class="sxs-lookup"><span data-stu-id="1b539-582">GradientCenter</span></span></li>
<li><span data-ttu-id="1b539-583">GradientRadial</span><span class="sxs-lookup"><span data-stu-id="1b539-583">GradientRadial</span></span></li>
<li><span data-ttu-id="1b539-584">GradientTitle</span><span class="sxs-lookup"><span data-stu-id="1b539-584">GradientTitle</span></span></li>
<li><span data-ttu-id="1b539-585">GradientUnscaled</span><span class="sxs-lookup"><span data-stu-id="1b539-585">GradientUnscaled</span></span></li>
<li><span data-ttu-id="1b539-586">Modello</span><span class="sxs-lookup"><span data-stu-id="1b539-586">Pattern</span></span></li>
<li><span data-ttu-id="1b539-587">Tinta unita</span><span class="sxs-lookup"><span data-stu-id="1b539-587">Solid</span></span></li>
<li><span data-ttu-id="1b539-588">Tile</span><span class="sxs-lookup"><span data-stu-id="1b539-588">Tile</span></span></li>
</ul>
<span data-ttu-id="1b539-589">Tile, Pattern e Frame richiedono che siano specificati gli attributi dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="1b539-589">Tile, Pattern, and Frame require the image attributes to be supplied.</span></span> <span data-ttu-id="1b539-590">Gradient e GradientRadial richiedono che siano specificati gli attributi della sfumatura.</span><span class="sxs-lookup"><span data-stu-id="1b539-590">Gradient and GradientRadial require the gradient attributes to be supplied.</span></span></td>
</tr>
</tbody>
</table>



 

### <a name="group-element"></a><span data-ttu-id="1b539-591">Group - elemento</span><span class="sxs-lookup"><span data-stu-id="1b539-591">Group element</span></span>

<span data-ttu-id="1b539-592">Un gruppo è una raccolta di singole forme che possono essere posizionate e trasformate come unità.</span><span class="sxs-lookup"><span data-stu-id="1b539-592">A group is a collection of individual shapes that can be positioned and transformed as a unit.</span></span>



|   <span data-ttu-id="1b539-593">Attributo</span><span class="sxs-lookup"><span data-stu-id="1b539-593">Attribute</span></span>        |   <span data-ttu-id="1b539-594">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b539-594">Description</span></span>                                                                                                                                                                                      |
|--------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b539-595">Elemento</span><span class="sxs-lookup"><span data-stu-id="1b539-595">Item</span></span>   | <span data-ttu-id="1b539-596">[IVgShape](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-596">[IVgShape](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="1b539-597">Elemento specificato nella matrice di forme.</span><span class="sxs-lookup"><span data-stu-id="1b539-597">Specified item in the array of shapes.</span></span> |
| <span data-ttu-id="1b539-598">Length</span><span class="sxs-lookup"><span data-stu-id="1b539-598">Length</span></span> | <span data-ttu-id="1b539-599">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-599">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="1b539-600">Numero di forme in questo gruppo.</span><span class="sxs-lookup"><span data-stu-id="1b539-600">Number of shapes in this group.</span></span>         |



 

### <a name="imagedata-element"></a><span data-ttu-id="1b539-601">Elemento Imagedata</span><span class="sxs-lookup"><span data-stu-id="1b539-601">Imagedata element</span></span>

<span data-ttu-id="1b539-602">Descrive un'immagine di cui eseguire il rendering sopra una forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-602">Describes a picture to be rendered on top of a shape.</span></span>



|   <span data-ttu-id="1b539-603">Attributo</span><span class="sxs-lookup"><span data-stu-id="1b539-603">Attribute</span></span>        |   <span data-ttu-id="1b539-604">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b539-604">Description</span></span>                                                                                                                                                                                      |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b539-605">Bilevel</span><span class="sxs-lookup"><span data-stu-id="1b539-605">BiLevel</span></span>     | <span data-ttu-id="1b539-606">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-606">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="1b539-607">Visualizzare l'immagine solo in due colori (in genere bianco e nero).</span><span class="sxs-lookup"><span data-stu-id="1b539-607">Display picture in only two colors (usually black and white).</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="1b539-608">BlackLevel</span><span class="sxs-lookup"><span data-stu-id="1b539-608">BlackLevel</span></span>  | <span data-ttu-id="1b539-609">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-609">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="1b539-610">Consente di impostare il livello in modo che i nero vengano visualizzati come veri neri e tutti gli altri colori siano visibili come sfumature sopra il nero.</span><span class="sxs-lookup"><span data-stu-id="1b539-610">Allows adjustment to set the level so that blacks appear as true blacks, and all other colors are visible as shades above black.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="1b539-611">Chromakey</span><span class="sxs-lookup"><span data-stu-id="1b539-611">Chromakey</span></span>   | <span data-ttu-id="1b539-612">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-612">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="1b539-613">Colore trasparente dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="1b539-613">Transparent color of picture.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="1b539-614">CropBottom</span><span class="sxs-lookup"><span data-stu-id="1b539-614">CropBottom</span></span>  | <span data-ttu-id="1b539-615">[VgNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-615">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="1b539-616">Distanza di ritaglio dalla parte inferiore dell'immagine espressa come percentuale delle dimensioni dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="1b539-616">Crop distance from bottom of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="1b539-617">CropLeft</span><span class="sxs-lookup"><span data-stu-id="1b539-617">CropLeft</span></span>    | <span data-ttu-id="1b539-618">[VgNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-618">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="1b539-619">Distanza di ritaglio dal bordo sinistro dell'immagine espressa come frazione delle dimensioni dell'immagine (da 0,0 a 1,0).</span><span class="sxs-lookup"><span data-stu-id="1b539-619">Crop distance from left edge of picture expressed as a fraction of picture size (from 0.0 to 1.0).</span></span> <span data-ttu-id="1b539-620">Tuttavia, il "ritaglio in uscita" è supportato e pertanto sono supportati valori minori di 0 e maggiori di 1. Ad esempio, -5, 20 potrebbe ritagliare i limiti 25X delle dimensioni dell'immagine con 4/5 su un lato dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="1b539-620">However, "out-cropping" is supported and thus values of less than 0 and greater than 1 are supported; e.g., -5, 20 would out-crop the bounds 25X the picture size with 4/5 on one side of the picture.</span></span> |
| <span data-ttu-id="1b539-621">CropRight</span><span class="sxs-lookup"><span data-stu-id="1b539-621">CropRight</span></span>   | <span data-ttu-id="1b539-622">[VgNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-622">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="1b539-623">Distanza di ritaglio da destra dell'immagine espressa come percentuale delle dimensioni dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="1b539-623">Crop distance from right of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="1b539-624">CropTop</span><span class="sxs-lookup"><span data-stu-id="1b539-624">CropTop</span></span>     | <span data-ttu-id="1b539-625">[VgNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-625">[VgNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="1b539-626">Distanza di ritaglio dall'inizio dell'immagine espressa come percentuale delle dimensioni dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="1b539-626">Crop distance from top of picture expressed as a percentage of picture size.</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="1b539-627">EmbossColor</span><span class="sxs-lookup"><span data-stu-id="1b539-627">EmbossColor</span></span> | <span data-ttu-id="1b539-628">[IVgColor](msdn-online-vml-ivgcolor.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-628">[IVgColor](msdn-online-vml-ivgcolor.md).</span></span> <span data-ttu-id="1b539-629">Questa proprietà è impostata su una percentuale del colore dell'ombreggiatura per creare un effetto immagine in rilievo.</span><span class="sxs-lookup"><span data-stu-id="1b539-629">This is set to a percentage of the shadow color to create an embossed picture effect.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="1b539-630">Guadagno</span><span class="sxs-lookup"><span data-stu-id="1b539-630">Gain</span></span>        | <span data-ttu-id="1b539-631">[VgPositiveNumber](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-631">[VgPositiveNumber](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="1b539-632">Regola l'intensità di tutti i colori.</span><span class="sxs-lookup"><span data-stu-id="1b539-632">Adjusts the intensity of all colors.</span></span> <span data-ttu-id="1b539-633">In sostanza, imposta il bianco brillante.</span><span class="sxs-lookup"><span data-stu-id="1b539-633">Essentially sets how bright white will be.</span></span> <span data-ttu-id="1b539-634">È compreso tra 0 e 32767.</span><span class="sxs-lookup"><span data-stu-id="1b539-634">Ranges from 0 to 32767.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="1b539-635">Gamma</span><span class="sxs-lookup"><span data-stu-id="1b539-635">Gamma</span></span>       | <span data-ttu-id="1b539-636">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-636">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="1b539-637">Correzione gamma.</span><span class="sxs-lookup"><span data-stu-id="1b539-637">Gamma correction.</span></span> <span data-ttu-id="1b539-638">Aumentandola si aumenta il contrasto di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="1b539-638">Increasing it gives an image more contrast.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="1b539-639">GrayScale</span><span class="sxs-lookup"><span data-stu-id="1b539-639">GrayScale</span></span>   | <span data-ttu-id="1b539-640">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-640">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="1b539-641">Visualizzare l'immagine in colori in scala di grigi.</span><span class="sxs-lookup"><span data-stu-id="1b539-641">Display picture in grayscale colors.</span></span>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="1b539-642">Src</span><span class="sxs-lookup"><span data-stu-id="1b539-642">Src</span></span>         | <span data-ttu-id="1b539-643">[Stringa](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-643">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="1b539-644">URL di un'immagine da caricare per riempimenti di immagini e motivi.</span><span class="sxs-lookup"><span data-stu-id="1b539-644">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="1b539-645">Questo attributo deve essere sempre presente e puntare a dati immagine validi per visualizzare un'immagine.</span><span class="sxs-lookup"><span data-stu-id="1b539-645">This attribute must always be present and point to valid image data for a picture to appear.</span></span>                                                                                                                                                           |



 

### <a name="path-element"></a><span data-ttu-id="1b539-646">Path - elemento</span><span class="sxs-lookup"><span data-stu-id="1b539-646">Path element</span></span>

<span data-ttu-id="1b539-647">Definisce il percorso che costituisce la forma, usando una stringa che contiene un set completo di comandi di "spostamento della penna".</span><span class="sxs-lookup"><span data-stu-id="1b539-647">Defines the path that makes up the shape, using a string that contains a rich set of "pen movement" commands.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b539-648">Limousine</span><span class="sxs-lookup"><span data-stu-id="1b539-648">Limo</span></span></td>
<td><span data-ttu-id="1b539-649"><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-649"><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>.</span></span> <span data-ttu-id="1b539-650">Definisce il punto in cui viene estesa la forma. Ad esempio, per una forma di giraffa, il punto di limousine si trova sul collo, quindi quando la forma viene ridimensionata, il collo si allunga e il resto della forma manterrà le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="1b539-650">Defines the point where the shape is stretched; e.g., for a giraffe shape, the limo point would be on the neck so when the shape is resized, the neck will stretch and the rest of the shape will maintain its dimensions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-651">TextBoxRect</span><span class="sxs-lookup"><span data-stu-id="1b539-651">TextBoxRect</span></span></td>
<td><span data-ttu-id="1b539-652"><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-652"><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>.</span></span> <span data-ttu-id="1b539-653">Matrice contenente i rettangoli che definiscono dove deve andare il testo.</span><span class="sxs-lookup"><span data-stu-id="1b539-653">Array containing the rectangles that define where text should go.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-654">V</span><span class="sxs-lookup"><span data-stu-id="1b539-654">V</span></span></td>
<td><span data-ttu-id="1b539-655"><a href="#data-types-used-in-the-vml-object-model">Stringa</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-655"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="1b539-656">Corrisponde all'attributo v nel tag Path.</span><span class="sxs-lookup"><span data-stu-id="1b539-656">Matches the v attribute on the Path tag.</span></span> <span data-ttu-id="1b539-657">Si noti che il percorso può corrispondere all'attributo o all'elemento Path.</span><span class="sxs-lookup"><span data-stu-id="1b539-657">Note that path may correspond to Path attribute or element.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-658">Valore</span><span class="sxs-lookup"><span data-stu-id="1b539-658">Value</span></span></td>
<td><span data-ttu-id="1b539-659"><a href="#data-types-used-in-the-vml-object-model">Stringa</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-659"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="1b539-660">Rappresentazione testuale dei comandi che definiscono il percorso.</span><span class="sxs-lookup"><span data-stu-id="1b539-660">A text representation of the commands that define the path.</span></span> <span data-ttu-id="1b539-661">I valori delle coordinate X o Y possono essere un riferimento a una formula nel formato in cui # è il numero ordinale della &quot; @# &quot; formula, ad esempio &quot; @2 &quot; .</span><span class="sxs-lookup"><span data-stu-id="1b539-661">X or y-coordinate values can be a reference to a formula in the form &quot;@#&quot; where # is the formula's ordinal number, e.g., &quot;@2&quot;.</span></span> <span data-ttu-id="1b539-662">Questa stringa di attributo è costituito da un set di comandi ricco, tra cui:</span><span class="sxs-lookup"><span data-stu-id="1b539-662">This attribute string is made up of a rich set of commands including the following:</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1b539-663">Comando</span><span class="sxs-lookup"><span data-stu-id="1b539-663">Command</span></span></th>
<th><span data-ttu-id="1b539-664">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b539-664">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b539-665">ae (angleellipseto)</span><span class="sxs-lookup"><span data-stu-id="1b539-665">ae (angleellipseto)</span></span></td>
<td><span data-ttu-id="1b539-666"><strong>center</strong>(x,y) <strong>size</strong>(w,h) <strong>start-angle</strong>, <strong>end-angle</strong></span><span class="sxs-lookup"><span data-stu-id="1b539-666"><strong>center</strong>(x,y) <strong>size</strong>(w,h) <strong>start-angle</strong>, <strong>end-angle</strong></span></span><br/> <span data-ttu-id="1b539-667">Disegnare un segmento di un'ellisse.</span><span class="sxs-lookup"><span data-stu-id="1b539-667">Draw a segment of an ellipse.</span></span> <span data-ttu-id="1b539-668">Una linea retta viene disegnata dal punto corrente al punto iniziale del segmento.</span><span class="sxs-lookup"><span data-stu-id="1b539-668">A straight line is drawn from the current point to the start point of the segment.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-669">al (angleelipse)</span><span class="sxs-lookup"><span data-stu-id="1b539-669">al (angleelipse)</span></span></td>
<td><span data-ttu-id="1b539-670">Uguale a ae, ad eccezione del fatto che è presente un m implicito al punto iniziale del segmento.</span><span class="sxs-lookup"><span data-stu-id="1b539-670">Same as ae except that there is an implied m to the starting point of the segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-671">ar (arco)</span><span class="sxs-lookup"><span data-stu-id="1b539-671">ar (arc)</span></span></td>
<td><span data-ttu-id="1b539-672">Come in .</span><span class="sxs-lookup"><span data-stu-id="1b539-672">Same as at.</span></span> <span data-ttu-id="1b539-673">Tuttavia, un nuovo sottopercorso viene avviato da un m implicito al punto iniziale dell'arco.</span><span class="sxs-lookup"><span data-stu-id="1b539-673">However, a new subpath is started by an implied m to the start point of the arc.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-674">at (arcto)</span><span class="sxs-lookup"><span data-stu-id="1b539-674">at (arcto)</span></span></td>
<td><span data-ttu-id="1b539-675"><strong>left</strong>, <strong>top</strong>, <strong>right</strong>, <strong>bottom</strong>, <strong>start</strong>(x,y) end (x,y) <strong>end</strong>(x,y)</span><span class="sxs-lookup"><span data-stu-id="1b539-675"><strong>left</strong>, <strong>top</strong>, <strong>right</strong>, <strong>bottom</strong>, <strong>start</strong>(x,y) <strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="1b539-676">I primi quattro valori definiscono il rettangolo di selezione di un'ellisse.</span><span class="sxs-lookup"><span data-stu-id="1b539-676">The first four values define the bounding box of an ellipse.</span></span> <span data-ttu-id="1b539-677">Gli ultimi quattro definiscono due vettori radiali.</span><span class="sxs-lookup"><span data-stu-id="1b539-677">The last four define two radial vectors.</span></span> <span data-ttu-id="1b539-678">Viene disegnato un segmento dell'ellisse che inizia in corrispondenza dell'angolo definito dal vettore del raggio iniziale e termina in corrispondenza dell'angolo definito dal vettore finale.</span><span class="sxs-lookup"><span data-stu-id="1b539-678">A segment of the ellipse is drawn that starts at the angle defined by the start radius vector and ends at the angle defined by the end vector.</span></span> <span data-ttu-id="1b539-679">Una linea retta viene disegnata dal punto corrente all'inizio dell'arco. L'arco viene sempre disegnato in senso antiorario.</span><span class="sxs-lookup"><span data-stu-id="1b539-679">A straight line is drawn from the current point to the start of the arc. The arc is always drawn in a counterclockwise direction.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-680">c (curveto)</span><span class="sxs-lookup"><span data-stu-id="1b539-680">c (curveto)</span></span></td>
<td><span data-ttu-id="1b539-681"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>a</strong>(x,y)</span><span class="sxs-lookup"><span data-stu-id="1b539-681"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>to</strong>(x,y)</span></span> <br/> <span data-ttu-id="1b539-682">Disegnare una curva di Bézier cubica dal punto corrente alla coordinata specificata dai due parametri finali, i punti di controllo specificati dai primi quattro parametri.</span><span class="sxs-lookup"><span data-stu-id="1b539-682">Draw a cubic bezier curve from the current point to the coordinate given by the final two parameters, the control points given by the first four parameters.</span></span> <span data-ttu-id="1b539-683">Il punto corrente diventa l'endpoint del bezier.</span><span class="sxs-lookup"><span data-stu-id="1b539-683">The current point becomes the endpoint of the bezier.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-684">e (end)</span><span class="sxs-lookup"><span data-stu-id="1b539-684">e (end)</span></span></td>
<td><span data-ttu-id="1b539-685">Terminare il set corrente di sottopercorso.</span><span class="sxs-lookup"><span data-stu-id="1b539-685">End the current set of subpaths.</span></span> <span data-ttu-id="1b539-686">Un determinato set di sottopercorso (delimitato da end) viene riempito usando eofill.</span><span class="sxs-lookup"><span data-stu-id="1b539-686">A given set of subpaths (as delimited by end) are filled using eofill.</span></span> <span data-ttu-id="1b539-687">I set successivi di sottopercorso vengono riempiti in modo indipendente e sovrapposti a quelli esistenti.</span><span class="sxs-lookup"><span data-stu-id="1b539-687">Subsequent sets of subpaths are filled independently and superimposed on existing ones.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-688">l (lineto)</span><span class="sxs-lookup"><span data-stu-id="1b539-688">l (lineto)</span></span></td>
<td><span data-ttu-id="1b539-689">x,y</span><span class="sxs-lookup"><span data-stu-id="1b539-689">x,y</span></span><br/> <span data-ttu-id="1b539-690">Disegnare una linea dal punto corrente alla coordinata x,y specificata, che diventa il nuovo punto corrente.</span><span class="sxs-lookup"><span data-stu-id="1b539-690">Draw a line from the current point to the given x,y-coordinate, which becomes the new current point.</span></span> <span data-ttu-id="1b539-691">È possibile impostare coppie di coordinate aggiuntive per formare una polilinea, ad esempio &quot; l 10,13,45,27,89,-12. &quot;</span><span class="sxs-lookup"><span data-stu-id="1b539-691">Additional coordinate pairs may be specified to form a polyline, e.g., &quot;l 10,13,45,27,89,-12&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-692">m (moveto)</span><span class="sxs-lookup"><span data-stu-id="1b539-692">m (moveto)</span></span></td>
<td><span data-ttu-id="1b539-693">x,y</span><span class="sxs-lookup"><span data-stu-id="1b539-693">x,y</span></span><br/> <span data-ttu-id="1b539-694">Avviare un nuovo sottopercorso in corrispondenza della coordinata x,y specificata.</span><span class="sxs-lookup"><span data-stu-id="1b539-694">Start a new subpath at the given x,y-coordinate.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-695">nf (nofill)</span><span class="sxs-lookup"><span data-stu-id="1b539-695">nf (nofill)</span></span></td>
<td><span data-ttu-id="1b539-696">Il set corrente di sottopercorso (delimitato dalla fine) non verrà riempito.</span><span class="sxs-lookup"><span data-stu-id="1b539-696">The current set of subpaths (delimited by end) will not be filled.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-697">ns (nostroke)</span><span class="sxs-lookup"><span data-stu-id="1b539-697">ns (nostroke)</span></span></td>
<td><span data-ttu-id="1b539-698">Il set corrente di sottopercorso (delimitato dalla fine) non verrà tracciato.</span><span class="sxs-lookup"><span data-stu-id="1b539-698">The current set of subpaths (delimited by end) will not be stroked.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-699">qb (quadraticbezier)</span><span class="sxs-lookup"><span data-stu-id="1b539-699">qb (quadraticbezier)</span></span></td>
<td><span data-ttu-id="1b539-700">(<strong>controlpoint</strong>(x, y))\*,<strong>end</strong>(x,y)</span><span class="sxs-lookup"><span data-stu-id="1b539-700">(<strong>controlpoint</strong>(x, y))\*,<strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="1b539-701">Definisce una o più curve di Bézier quadratica tramite punti di controllo e un endpoint.</span><span class="sxs-lookup"><span data-stu-id="1b539-701">Defines one or more quadratic bezier curves by means of control points and an endpoint.</span></span> <span data-ttu-id="1b539-702">I punti intermedi (su curva) vengono ottenuti tramite interpolazione tra punti di controllo successivi simili ai tipi di carattere TrueType.</span><span class="sxs-lookup"><span data-stu-id="1b539-702">Intermediate (on-curve) points are obtained by interpolation between successive control points similar to TrueType fonts.</span></span> <span data-ttu-id="1b539-703">Il sottopercorso non deve essere un inizio, nel qual caso il sottopercorso viene chiuso e l'ultimo punto definisce il punto iniziale.</span><span class="sxs-lookup"><span data-stu-id="1b539-703">The subpath need not be a start, in which case the subpath is closed and the last point defines the start point.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-704">qx (ellipticalquadrantx)</span><span class="sxs-lookup"><span data-stu-id="1b539-704">qx (ellipticalquadrantx)</span></span></td>
<td><span data-ttu-id="1b539-705"><strong>end</strong>(x,y)</span><span class="sxs-lookup"><span data-stu-id="1b539-705"><strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="1b539-706">Un quarto di ellisse viene disegnato dal punto corrente all'endpoint specificato.</span><span class="sxs-lookup"><span data-stu-id="1b539-706">A quarter ellipse is drawn from the current point to the given endpoint.</span></span> <span data-ttu-id="1b539-707">Il segmento ellittico è inizialmente tangente a una linea parallela all'asse x; ad esempio il segmento inizia orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="1b539-707">The elliptical segment is initially tangential to a line parallel to the x-axis; i.e., the segment starts out horizontal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-708">qy (ellipticalquadranty)</span><span class="sxs-lookup"><span data-stu-id="1b539-708">qy (ellipticalquadranty)</span></span></td>
<td><span data-ttu-id="1b539-709"><strong>end</strong>(x,y)</span><span class="sxs-lookup"><span data-stu-id="1b539-709"><strong>end</strong>(x,y)</span></span> <br/> <span data-ttu-id="1b539-710">Uguale a qx, ad eccezione del fatto che il segmento ellittico è inizialmente tangente a una linea parallela all'asse y; ad esempio il segmento inizia in verticale.</span><span class="sxs-lookup"><span data-stu-id="1b539-710">Same as qx except that the elliptical segment is initially tangential to a line parallel to the y-axis; i.e., the segment starts out vertical.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-711">r (rlineto)</span><span class="sxs-lookup"><span data-stu-id="1b539-711">r (rlineto)</span></span></td>
<td><span data-ttu-id="1b539-712">x,y</span><span class="sxs-lookup"><span data-stu-id="1b539-712">x,y</span></span> <br/> <span data-ttu-id="1b539-713">Disegnare una linea dal punto corrente alla coordinata relativa (cpx + x, cpy + y).</span><span class="sxs-lookup"><span data-stu-id="1b539-713">Draw a line from the current point to the relative coordinate (cpx + x, cpy + y).</span></span> <span data-ttu-id="1b539-714">Se vengono specificate coppie di coordinate aggiuntive, ogni nuovo punto viene calcolato rispetto all'ultimo.</span><span class="sxs-lookup"><span data-stu-id="1b539-714">If additional coordinate pairs are given, each new point is computed relative to the last one.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-715">t (rmoveto)</span><span class="sxs-lookup"><span data-stu-id="1b539-715">t (rmoveto)</span></span></td>
<td><span data-ttu-id="1b539-716">x,y</span><span class="sxs-lookup"><span data-stu-id="1b539-716">x,y</span></span><br/> <span data-ttu-id="1b539-717">Avviare un nuovo sottopercorso in corrispondenza delle coordinate relative ( cpx + x, cpy + y) dove cpx, cpy è la posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="1b539-717">Start a new subpath at the relative coordinates ( cpx + x, cpy + y) where cpx, cpy is the current position.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-718">v (curveto)</span><span class="sxs-lookup"><span data-stu-id="1b539-718">v (curveto)</span></span></td>
<td><span data-ttu-id="1b539-719"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>to</strong> (x,y)</span><span class="sxs-lookup"><span data-stu-id="1b539-719"><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>to</strong> (x,y)</span></span> <br/> <span data-ttu-id="1b539-720">Curva di Bézier cubica che usa le coordinate specificate relative al punto corrente.</span><span class="sxs-lookup"><span data-stu-id="1b539-720">Cubic bezier curve using the given coordinates relative to the current point.</span></span> <span data-ttu-id="1b539-721">Tutti i punti vengono calcolati in relazione allo stesso punto iniziale.</span><span class="sxs-lookup"><span data-stu-id="1b539-721">All the points are computed relative to the same starting point.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-722">wa (clockwisearcto)</span><span class="sxs-lookup"><span data-stu-id="1b539-722">wa (clockwisearcto)</span></span></td>
<td><span data-ttu-id="1b539-723">Uguale a , ma l'arco viene disegnato in senso orario.</span><span class="sxs-lookup"><span data-stu-id="1b539-723">Same as at but the arc is drawn in a clockwise direction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-724">wr (clockwisearc)</span><span class="sxs-lookup"><span data-stu-id="1b539-724">wr (clockwisearc)</span></span></td>
<td><span data-ttu-id="1b539-725">Uguale a ar, ma viene disegnato in senso orario.</span><span class="sxs-lookup"><span data-stu-id="1b539-725">Same as ar but is drawn in a clockwise direction.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-726">x (chiudi)</span><span class="sxs-lookup"><span data-stu-id="1b539-726">x (close)</span></span></td>
<td><span data-ttu-id="1b539-727">Chiudere il sottopercorso corrente tracciando una linea retta dal punto corrente al punto di spostamento originale.</span><span class="sxs-lookup"><span data-stu-id="1b539-727">Close the current subpath by drawing a straight line from the current point to the original moveto point.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="shadow-element"></a><span data-ttu-id="1b539-728">Elemento Shadow</span><span class="sxs-lookup"><span data-stu-id="1b539-728">Shadow element</span></span>

<span data-ttu-id="1b539-729">Descrive un effetto ombreggiatura su una forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-729">Describes a shadow effect on a shape.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b539-730">Color</span><span class="sxs-lookup"><span data-stu-id="1b539-730">Color</span></span></td>
<td><span data-ttu-id="1b539-731"><a href="msdn-online-vml-ivgcolor.md">Oggetto IVgColor.</a></span><span class="sxs-lookup"><span data-stu-id="1b539-731"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="1b539-732">Colore dell'ombreggiatura primaria.</span><span class="sxs-lookup"><span data-stu-id="1b539-732">Color of the primary shadow.</span></span> <span data-ttu-id="1b539-733">Il valore predefinito è RGB(128,128,128)</span><span class="sxs-lookup"><span data-stu-id="1b539-733">Default is RGB(128,128,128)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-734">Color2</span><span class="sxs-lookup"><span data-stu-id="1b539-734">Color2</span></span></td>
<td><span data-ttu-id="1b539-735"><a href="msdn-online-vml-ivgcolor.md">Oggetto IVgColor.</a></span><span class="sxs-lookup"><span data-stu-id="1b539-735"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="1b539-736">Colore della seconda ombreggiatura o evidenziazione in un'ombreggiatura in rilievo o in rilievo.</span><span class="sxs-lookup"><span data-stu-id="1b539-736">Color of the second shadow, or highlight in an embossed or engraved shadow.</span></span> <span data-ttu-id="1b539-737">Il valore predefinito è RGB(203,203,203).</span><span class="sxs-lookup"><span data-stu-id="1b539-737">Default is RGB(203,203,203).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-738">Matrice</span><span class="sxs-lookup"><span data-stu-id="1b539-738">Matrix</span></span></td>
<td><span data-ttu-id="1b539-739"><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-739"><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix</a>.</span></span> <span data-ttu-id="1b539-740">Matrice di trasformazione prospettica nel &quot; formato, sxx,sxy,syx,syy,px,py &quot; [s=scale, p=perspective].</span><span class="sxs-lookup"><span data-stu-id="1b539-740">A perspective transform matrix in the form, &quot;sxx,sxy,syx,syy,px,py&quot; [s=scale, p=perspective].</span></span> <span data-ttu-id="1b539-741">Gli elementi s specificano come deve essere ridimensionata l'ombreggiatura rispetto alla forma e gli elementi p specificano come l'ombreggiatura deve inclinarsi rispetto alla forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-741">The s items specify how the shadow should scale with respect to the shape, and the p items specify how the shadow should skew with respect to the shape.</span></span> <span data-ttu-id="1b539-742">Ad esempio, la matrice seguente ridimensiona la forma di un fattore 2 e la inclina di un fattore di 4 in tutte le direzioni:</span><span class="sxs-lookup"><span data-stu-id="1b539-742">For example, the following matrix resizes the shape by a factor of 2 and skews it by a factor of 4 in all directions:</span></span> <br/> <span data-ttu-id="1b539-743">&quot;2,2,2,2,4,4&quot;</span><span class="sxs-lookup"><span data-stu-id="1b539-743">&quot;2,2,2,2,4,4&quot;</span></span><br/> <span data-ttu-id="1b539-744">Questa matrice viene utilizzata solo se il tipo di ombreggiatura è impostato su perspective.</span><span class="sxs-lookup"><span data-stu-id="1b539-744">This matrix is only used if the type of the shadow is set to perspective.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-745">Oscurato</span><span class="sxs-lookup"><span data-stu-id="1b539-745">Obscured</span></span></td>
<td><span data-ttu-id="1b539-746"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-746"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="1b539-747">L'ombreggiatura può essere vista attraverso se non è presente alcun riempimento sulla forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-747">The shadow can be seen through if there is no fill on the shape.</span></span> <span data-ttu-id="1b539-748">Il valore predefinito è False.</span><span class="sxs-lookup"><span data-stu-id="1b539-748">Default is False.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-749">Offset</span><span class="sxs-lookup"><span data-stu-id="1b539-749">Offset</span></span></td>
<td><span data-ttu-id="1b539-750"><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-750"><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset</a>.</span></span> <span data-ttu-id="1b539-751">Quantità di offset x,y dalla posizione della forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-751">Amount of x,y offset from the shape's location.</span></span> <span data-ttu-id="1b539-752">Il valore predefinito &quot; è 2pt,2pt. &quot;</span><span class="sxs-lookup"><span data-stu-id="1b539-752">Default is &quot;2pt,2pt&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-753">Offset2</span><span class="sxs-lookup"><span data-stu-id="1b539-753">Offset2</span></span></td>
<td><span data-ttu-id="1b539-754"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-754"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="1b539-755">Quantità di offset x,y secondi dalla posizione della forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-755">Amount of x,y second offset from the shape?s location.</span></span> <span data-ttu-id="1b539-756">I valori sono una misura assoluta o un valore frazionario di forma (da -0,5 a +0,5).</span><span class="sxs-lookup"><span data-stu-id="1b539-756">Values are either an absolute measurement, or a fractional value of shape (-0.5 to +0.5).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-757">On</span><span class="sxs-lookup"><span data-stu-id="1b539-757">On</span></span></td>
<td><span data-ttu-id="1b539-758"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-758"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="1b539-759">Attiva e disattiva la visualizzazione dell'ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="1b539-759">Turns the display of the shadow on and off.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-760">Opacità</span><span class="sxs-lookup"><span data-stu-id="1b539-760">Opacity</span></span></td>
<td><span data-ttu-id="1b539-761"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-761"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="1b539-762">Opacità dell'effetto ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="1b539-762">Opacity of the shadow effect.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-763">Origine</span><span class="sxs-lookup"><span data-stu-id="1b539-763">Origin</span></span></td>
<td><span data-ttu-id="1b539-764"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Coppia di valori frazionari di forma da -0,5 a +0,5.</span><span class="sxs-lookup"><span data-stu-id="1b539-764"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> A pair of fractional values of shape from -0.5 to +0.5.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-765">Tipo</span><span class="sxs-lookup"><span data-stu-id="1b539-765">Type</span></span></td>
<td><span data-ttu-id="1b539-766"><a href="#data-types-used-in-the-vml-object-model">VgShadowType</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-766"><a href="#data-types-used-in-the-vml-object-model">VgShadowType</a>.</span></span> <span data-ttu-id="1b539-767">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="1b539-767">Values are:</span></span>
<ul>
<li><span data-ttu-id="1b539-768">Single (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1b539-768">Single (default)</span></span></li>
<li><span data-ttu-id="1b539-769">Double</span><span class="sxs-lookup"><span data-stu-id="1b539-769">Double</span></span></li>
<li><span data-ttu-id="1b539-770">Prospettiva</span><span class="sxs-lookup"><span data-stu-id="1b539-770">Perspective</span></span></li>
<li><span data-ttu-id="1b539-771">ShapeRelative</span><span class="sxs-lookup"><span data-stu-id="1b539-771">ShapeRelative</span></span></li>
<li><span data-ttu-id="1b539-772">DrawingRelative</span><span class="sxs-lookup"><span data-stu-id="1b539-772">DrawingRelative</span></span></li>
<li><span data-ttu-id="1b539-773">Rilievo</span><span class="sxs-lookup"><span data-stu-id="1b539-773">Emboss</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="skew-element"></a><span data-ttu-id="1b539-774">Elemento Skew</span><span class="sxs-lookup"><span data-stu-id="1b539-774">Skew element</span></span>

<span data-ttu-id="1b539-775">Descrive un effetto di inclinazione della prospettiva su una forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-775">Describes a perspective skew effect on a shape.</span></span> <span data-ttu-id="1b539-776">L'a inclinazione viene applicata ai dati grafici vettoriali, non ai dati di immagine.</span><span class="sxs-lookup"><span data-stu-id="1b539-776">The skew is applied to vector graphic data, not image data.</span></span>



|   <span data-ttu-id="1b539-777">Attributo</span><span class="sxs-lookup"><span data-stu-id="1b539-777">Attribute</span></span>        |   <span data-ttu-id="1b539-778">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b539-778">Description</span></span>                                                                                                                                                                                      |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b539-779">Matrice</span><span class="sxs-lookup"><span data-stu-id="1b539-779">Matrix</span></span> | <span data-ttu-id="1b539-780">[IVgSkewMatrix](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-780">[IVgSkewMatrix](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="1b539-781">Matrice di trasformazione della prospettiva nel formato "sxx,sxy,syx,syy,px,py" \[ s=scale, p=perspective \] .</span><span class="sxs-lookup"><span data-stu-id="1b539-781">A perspective transform matrix in the form, "sxx,sxy,syx,syy,px,py" \[ s=scale, p=perspective\].</span></span> <span data-ttu-id="1b539-782">Se offset è in unità assolute, px, py sono in emu ^ -1 unità; in caso contrario, sono una frazione inversa delle dimensioni della forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-782">If offset is in absolute units then px,py are in emu ^ -1 units; otherwise they are an inverse fraction of shape size.</span></span> |
| <span data-ttu-id="1b539-783">Offset</span><span class="sxs-lookup"><span data-stu-id="1b539-783">Offset</span></span> | <span data-ttu-id="1b539-784">[IvgSkewOffset](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-784">[IvgSkewOffset](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="1b539-785">Quantità di offset x,y dalla posizione della forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-785">Amount of x,y offset from the shape's location.</span></span> <span data-ttu-id="1b539-786">Il valore predefinito è "2pt,2pt".</span><span class="sxs-lookup"><span data-stu-id="1b539-786">Default is "2pt,2pt".</span></span>                                                                                                                                                   |
| <span data-ttu-id="1b539-787">On</span><span class="sxs-lookup"><span data-stu-id="1b539-787">On</span></span>     | <span data-ttu-id="1b539-788">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-788">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="1b539-789">Attiva o disattiva la visualizzazione dell'a inclinazione.</span><span class="sxs-lookup"><span data-stu-id="1b539-789">Turns the display of the skew on or off.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="1b539-790">Origine</span><span class="sxs-lookup"><span data-stu-id="1b539-790">Origin</span></span> | <span data-ttu-id="1b539-791">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-791">[Vector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="1b539-792">Coppia di valori frazionari di forma da -0,5 a +0,5.</span><span class="sxs-lookup"><span data-stu-id="1b539-792">A pair of fractional values of shape from -0.5 to +0.5.</span></span>                                                                                                                                                                     |



 

### <a name="stroke-element"></a><span data-ttu-id="1b539-793">Elemento Stroke</span><span class="sxs-lookup"><span data-stu-id="1b539-793">Stroke element</span></span>

<span data-ttu-id="1b539-794">Descrive come disegnare il tracciato se si desidera un elemento oltre una linea continua con un colore a tinta unita.</span><span class="sxs-lookup"><span data-stu-id="1b539-794">Describes how to draw the path if something beyond a solid line with a solid color is desired.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b539-795">Color</span><span class="sxs-lookup"><span data-stu-id="1b539-795">Color</span></span></td>
<td><span data-ttu-id="1b539-796"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-796"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="1b539-797">Colore della linea.</span><span class="sxs-lookup"><span data-stu-id="1b539-797">The color of the line.</span></span> <span data-ttu-id="1b539-798">Uguale all'attributo StrokeColor in Shape, ma ne esegue l'override.</span><span class="sxs-lookup"><span data-stu-id="1b539-798">Same as StrokeColor attribute in Shape but overrides it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-799">Color2</span><span class="sxs-lookup"><span data-stu-id="1b539-799">Color2</span></span></td>
<td><span data-ttu-id="1b539-800"><a href="msdn-online-vml-ivgcolor.md">Oggetto IVgColor.</a></span><span class="sxs-lookup"><span data-stu-id="1b539-800"><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>.</span></span> <span data-ttu-id="1b539-801">Colore secondario.</span><span class="sxs-lookup"><span data-stu-id="1b539-801">Secondary color.</span></span> <span data-ttu-id="1b539-802">Usato quando FillType è Pattern.</span><span class="sxs-lookup"><span data-stu-id="1b539-802">Used when FillType is Pattern.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-803">Dashstyle</span><span class="sxs-lookup"><span data-stu-id="1b539-803">DashStyle</span></span></td>
<td><span data-ttu-id="1b539-804"><strong>VgLineDashStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b539-804"><strong>VgLineDashStyle</strong>.</span></span> <span data-ttu-id="1b539-805">Formato dello stile dash.</span><span class="sxs-lookup"><span data-stu-id="1b539-805">Dash style format.</span></span> <span data-ttu-id="1b539-806">Può essere un valore specifico o una sequenza di numeri con un modello di trattino definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="1b539-806">May be a specific value or a sequence of numbers with a user-defined dash pattern.</span></span> <span data-ttu-id="1b539-807">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="1b539-807">Values are:</span></span>
<ul>
<li><span data-ttu-id="1b539-808">Solid (valore predefinito)</span><span class="sxs-lookup"><span data-stu-id="1b539-808">Solid (default)</span></span></li>
<li><span data-ttu-id="1b539-809">ShortDash</span><span class="sxs-lookup"><span data-stu-id="1b539-809">ShortDash</span></span></li>
<li><span data-ttu-id="1b539-810">ShortDot</span><span class="sxs-lookup"><span data-stu-id="1b539-810">ShortDot</span></span></li>
<li><span data-ttu-id="1b539-811">ShortDashDot</span><span class="sxs-lookup"><span data-stu-id="1b539-811">ShortDashDot</span></span></li>
<li><span data-ttu-id="1b539-812">ShortDashDotDot</span><span class="sxs-lookup"><span data-stu-id="1b539-812">ShortDashDotDot</span></span></li>
<li><span data-ttu-id="1b539-813">Punto</span><span class="sxs-lookup"><span data-stu-id="1b539-813">Dot</span></span></li>
<li><span data-ttu-id="1b539-814">Trattino</span><span class="sxs-lookup"><span data-stu-id="1b539-814">Dash</span></span></li>
<li><span data-ttu-id="1b539-815">DashDot</span><span class="sxs-lookup"><span data-stu-id="1b539-815">DashDot</span></span></li>
<li><span data-ttu-id="1b539-816">LongDash</span><span class="sxs-lookup"><span data-stu-id="1b539-816">LongDash</span></span></li>
<li><span data-ttu-id="1b539-817">LongDashDot</span><span class="sxs-lookup"><span data-stu-id="1b539-817">LongDashDot</span></span></li>
<li><span data-ttu-id="1b539-818">LongDashDotDot</span><span class="sxs-lookup"><span data-stu-id="1b539-818">LongDashDotDot</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-819">EndArrow</span><span class="sxs-lookup"><span data-stu-id="1b539-819">EndArrow</span></span></td>
<td><span data-ttu-id="1b539-820"><strong>VgArrowheadStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b539-820"><strong>VgArrowheadStyle</strong>.</span></span> <span data-ttu-id="1b539-821">Freccia per la fine della linea.</span><span class="sxs-lookup"><span data-stu-id="1b539-821">Arrowhead for the end of the line.</span></span> <span data-ttu-id="1b539-822">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="1b539-822">Values are:</span></span>
<ul>
<li><span data-ttu-id="1b539-823">Nessuno (valore predefinito)</span><span class="sxs-lookup"><span data-stu-id="1b539-823">None (default)</span></span></li>
<li><span data-ttu-id="1b539-824">Blocca</span><span class="sxs-lookup"><span data-stu-id="1b539-824">Block</span></span></li>
<li><span data-ttu-id="1b539-825">Classic</span><span class="sxs-lookup"><span data-stu-id="1b539-825">Classic</span></span></li>
<li><span data-ttu-id="1b539-826">Diamond</span><span class="sxs-lookup"><span data-stu-id="1b539-826">Diamond</span></span></li>
<li><span data-ttu-id="1b539-827">Ovale</span><span class="sxs-lookup"><span data-stu-id="1b539-827">Oval</span></span></li>
<li><span data-ttu-id="1b539-828">Apri</span><span class="sxs-lookup"><span data-stu-id="1b539-828">Open</span></span></li>
<li><span data-ttu-id="1b539-829">Frecce di espansione</span><span class="sxs-lookup"><span data-stu-id="1b539-829">Chevron</span></span></li>
<li><span data-ttu-id="1b539-830">DoubleChevron</span><span class="sxs-lookup"><span data-stu-id="1b539-830">DoubleChevron</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-831">EndArrowLength</span><span class="sxs-lookup"><span data-stu-id="1b539-831">EndArrowLength</span></span></td>
<td><span data-ttu-id="1b539-832"><strong>VgArrowHeadLength</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b539-832"><strong>VgArrowHeadLength</strong>.</span></span> <span data-ttu-id="1b539-833">Lunghezza della freccia per la fine della linea.</span><span class="sxs-lookup"><span data-stu-id="1b539-833">Arrowhead length for the end of the line.</span></span> <span data-ttu-id="1b539-834">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="1b539-834">Values are:</span></span>
<ul>
<li><span data-ttu-id="1b539-835">Short</span><span class="sxs-lookup"><span data-stu-id="1b539-835">Short</span></span></li>
<li><span data-ttu-id="1b539-836">Media (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1b539-836">Medium (default)</span></span></li>
<li><span data-ttu-id="1b539-837">long</span><span class="sxs-lookup"><span data-stu-id="1b539-837">Long</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-838">EndArrowWidth</span><span class="sxs-lookup"><span data-stu-id="1b539-838">EndArrowWidth</span></span></td>
<td><span data-ttu-id="1b539-839"><strong>VgArrowheadWidth</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b539-839"><strong>VgArrowheadWidth</strong>.</span></span> <span data-ttu-id="1b539-840">Larghezza della freccia per la fine della linea.</span><span class="sxs-lookup"><span data-stu-id="1b539-840">Arrowhead width for the end of the line.</span></span> <span data-ttu-id="1b539-841">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="1b539-841">Values are:</span></span>
<ul>
<li><span data-ttu-id="1b539-842">Stretta</span><span class="sxs-lookup"><span data-stu-id="1b539-842">Narrow</span></span></li>
<li><span data-ttu-id="1b539-843">Media (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1b539-843">Medium (default)</span></span></li>
<li><span data-ttu-id="1b539-844">Largo</span><span class="sxs-lookup"><span data-stu-id="1b539-844">Wide</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-845">Endcap</span><span class="sxs-lookup"><span data-stu-id="1b539-845">EndCap</span></span></td>
<td><span data-ttu-id="1b539-846"><strong>VgLineEndCapStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b539-846"><strong>VgLineEndCapStyle</strong>.</span></span> <span data-ttu-id="1b539-847">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="1b539-847">Values are:</span></span>
<ul>
<li><span data-ttu-id="1b539-848">Semplice</span><span class="sxs-lookup"><span data-stu-id="1b539-848">Flat</span></span></li>
<li><span data-ttu-id="1b539-849">Square</span><span class="sxs-lookup"><span data-stu-id="1b539-849">Square</span></span></li>
<li><span data-ttu-id="1b539-850">Round</span><span class="sxs-lookup"><span data-stu-id="1b539-850">Round</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-851">FillType</span><span class="sxs-lookup"><span data-stu-id="1b539-851">FillType</span></span></td>
<td><span data-ttu-id="1b539-852"><strong>VgLineFillType</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b539-852"><strong>VgLineFillType</strong>.</span></span> <span data-ttu-id="1b539-853">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="1b539-853">Values are:</span></span>
<ul>
<li><span data-ttu-id="1b539-854">Solid (valore predefinito)</span><span class="sxs-lookup"><span data-stu-id="1b539-854">Solid (default)</span></span></li>
<li><span data-ttu-id="1b539-855">Tile</span><span class="sxs-lookup"><span data-stu-id="1b539-855">Tile</span></span></li>
<li><span data-ttu-id="1b539-856">Modello</span><span class="sxs-lookup"><span data-stu-id="1b539-856">Pattern</span></span></li>
<li><span data-ttu-id="1b539-857">Frame</span><span class="sxs-lookup"><span data-stu-id="1b539-857">Frame</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-858">ImageAlignShape</span><span class="sxs-lookup"><span data-stu-id="1b539-858">ImageAlignShape</span></span></td>
<td><span data-ttu-id="1b539-859"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-859"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="1b539-860">Allineare l'immagine alla forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-860">Align the image with the shape.</span></span> <span data-ttu-id="1b539-861">Se False, allineare l'immagine alla finestra.</span><span class="sxs-lookup"><span data-stu-id="1b539-861">If False, align image with window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-862">ImageAspect</span><span class="sxs-lookup"><span data-stu-id="1b539-862">ImageAspect</span></span></td>
<td><span data-ttu-id="1b539-863"><strong>VgAspectType</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b539-863"><strong>VgAspectType</strong>.</span></span> <span data-ttu-id="1b539-864">L'attributo ImageSize verrà modificato per mantenere l'aspetto dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="1b539-864">ImageSize attribute will be adjusted to preserve the aspect of the image.</span></span> <span data-ttu-id="1b539-865">I possibili valori sono:</span><span class="sxs-lookup"><span data-stu-id="1b539-865">Values include:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1b539-866">Valore</span><span class="sxs-lookup"><span data-stu-id="1b539-866">Value</span></span></th>
<th><span data-ttu-id="1b539-867">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b539-867">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b539-868">Ignora</span><span class="sxs-lookup"><span data-stu-id="1b539-868">Ignore</span></span></td>
<td><span data-ttu-id="1b539-869">Ignorare i problemi relativi all'aspetto.</span><span class="sxs-lookup"><span data-stu-id="1b539-869">Ignore aspect issues.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-870">Atleast</span><span class="sxs-lookup"><span data-stu-id="1b539-870">AtLeast</span></span></td>
<td><span data-ttu-id="1b539-871">L'immagine è grande almeno quanto le dimensioni dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="1b539-871">Image is at least as big as the image size.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-872">AtMost</span><span class="sxs-lookup"><span data-stu-id="1b539-872">AtMost</span></span></td>
<td><span data-ttu-id="1b539-873">Le dimensioni dell'immagine non sono maggiori delle dimensioni dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="1b539-873">Image is no bigger than image size.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-874">Imagesize</span><span class="sxs-lookup"><span data-stu-id="1b539-874">ImageSize</span></span></td>
<td><span data-ttu-id="1b539-875"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-875"><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>.</span></span> <span data-ttu-id="1b539-876">Dimensioni dell'immagine con cui formare il pennello.</span><span class="sxs-lookup"><span data-stu-id="1b539-876">Size of the image to form the brush with.</span></span> <span data-ttu-id="1b539-877">Il valore predefinito è la dimensione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="1b539-877">Default is the size of the image.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-878">JoinStyle</span><span class="sxs-lookup"><span data-stu-id="1b539-878">JoinStyle</span></span></td>
<td><span data-ttu-id="1b539-879"><strong>VgLineJoinStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b539-879"><strong>VgLineJoinStyle</strong>.</span></span> <span data-ttu-id="1b539-880">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="1b539-880">Values are:</span></span>
<ul>
<li><span data-ttu-id="1b539-881">Round (giunto arrotondato)</span><span class="sxs-lookup"><span data-stu-id="1b539-881">Round (rounded joint)</span></span></li>
<li><span data-ttu-id="1b539-882">Smussatura (giunto smussato)</span><span class="sxs-lookup"><span data-stu-id="1b539-882">Bevel (beveled joint)</span></span></li>
<li><span data-ttu-id="1b539-883">Miter (miter joint)</span><span class="sxs-lookup"><span data-stu-id="1b539-883">Miter (miter joint)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-884">LineStyle</span><span class="sxs-lookup"><span data-stu-id="1b539-884">LineStyle</span></span></td>
<td><span data-ttu-id="1b539-885"><strong>VgLineStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b539-885"><strong>VgLineStyle</strong>.</span></span> <span data-ttu-id="1b539-886">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="1b539-886">Values are:</span></span>
<ul>
<li><span data-ttu-id="1b539-887">Single</span><span class="sxs-lookup"><span data-stu-id="1b539-887">Single</span></span></li>
<li><span data-ttu-id="1b539-888">ThinThin (1:1:1)</span><span class="sxs-lookup"><span data-stu-id="1b539-888">ThinThin (1:1:1)</span></span></li>
<li><span data-ttu-id="1b539-889">ThinThick (1:1:2)</span><span class="sxs-lookup"><span data-stu-id="1b539-889">ThinThick (1:1:2)</span></span></li>
<li><span data-ttu-id="1b539-890">ThickThin (2:1:1)</span><span class="sxs-lookup"><span data-stu-id="1b539-890">ThickThin (2:1:1)</span></span></li>
<li><span data-ttu-id="1b539-891">ThickBetweenThin (1:1:2:1:1)</span><span class="sxs-lookup"><span data-stu-id="1b539-891">ThickBetweenThin (1:1:2:1:1)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-892">MiterLimit</span><span class="sxs-lookup"><span data-stu-id="1b539-892">MiterLimit</span></span></td>
<td><span data-ttu-id="1b539-893"><a href="msdn-online-vml-vglength.md">Lunghezza .</a></span><span class="sxs-lookup"><span data-stu-id="1b539-893"><a href="msdn-online-vml-vglength.md">Length</a>.</span></span> <span data-ttu-id="1b539-894">Distanza massima tra il punto interno e il punto esterno di un'giunzione.</span><span class="sxs-lookup"><span data-stu-id="1b539-894">The maximum distance between the inner point and outer point of a joint.</span></span> <span data-ttu-id="1b539-895">Questo numero è un multiplo dello spessore della linea.</span><span class="sxs-lookup"><span data-stu-id="1b539-895">This number is a multiple of the thickness of the line.</span></span> <span data-ttu-id="1b539-896">È compreso tra 0 e 32.767.</span><span class="sxs-lookup"><span data-stu-id="1b539-896">Ranges from 0 to 32,767.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-897">On</span><span class="sxs-lookup"><span data-stu-id="1b539-897">On</span></span></td>
<td><span data-ttu-id="1b539-898"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-898"><a href="msdn-online-vml-vgtristate.md">VgTriState</a>.</span></span> <span data-ttu-id="1b539-899">Attiva e disattiva la visualizzazione della riga.</span><span class="sxs-lookup"><span data-stu-id="1b539-899">Turns the display of the line on and off.</span></span> <span data-ttu-id="1b539-900">Uguale all'attributo Stroke in Shape, ma ne esegue l'override.</span><span class="sxs-lookup"><span data-stu-id="1b539-900">Same as Stroke attribute in Shape but overrides it.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-901">Opacità</span><span class="sxs-lookup"><span data-stu-id="1b539-901">Opacity</span></span></td>
<td><span data-ttu-id="1b539-902"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-902"><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>.</span></span> <span data-ttu-id="1b539-903">Opacità del tratto.</span><span class="sxs-lookup"><span data-stu-id="1b539-903">Opacity of the stroke.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-904">Src</span><span class="sxs-lookup"><span data-stu-id="1b539-904">Src</span></span></td>
<td><span data-ttu-id="1b539-905">Stringa.</span><span class="sxs-lookup"><span data-stu-id="1b539-905">String.</span></span> <span data-ttu-id="1b539-906">URL di un'immagine da caricare per riempimenti di immagini e motivi.</span><span class="sxs-lookup"><span data-stu-id="1b539-906">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="1b539-907">Questo attributo deve essere sempre presente e puntare a dati immagine validi per visualizzare un'immagine.</span><span class="sxs-lookup"><span data-stu-id="1b539-907">This attribute must always be present and point to valid image data for a picture to appear.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-908">StartArrow</span><span class="sxs-lookup"><span data-stu-id="1b539-908">StartArrow</span></span></td>
<td><span data-ttu-id="1b539-909"><strong>VgArrowheadStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b539-909"><strong>VgArrowheadStyle</strong>.</span></span> <span data-ttu-id="1b539-910">Freccia per l'inizio della linea.</span><span class="sxs-lookup"><span data-stu-id="1b539-910">Arrowhead for the start of the line.</span></span> <span data-ttu-id="1b539-911">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="1b539-911">Values are:</span></span>
<ul>
<li><span data-ttu-id="1b539-912">Nessuno (valore predefinito)</span><span class="sxs-lookup"><span data-stu-id="1b539-912">None (default)</span></span></li>
<li><span data-ttu-id="1b539-913">Blocca</span><span class="sxs-lookup"><span data-stu-id="1b539-913">Block</span></span></li>
<li><span data-ttu-id="1b539-914">Classic</span><span class="sxs-lookup"><span data-stu-id="1b539-914">Classic</span></span></li>
<li><span data-ttu-id="1b539-915">Diamond</span><span class="sxs-lookup"><span data-stu-id="1b539-915">Diamond</span></span></li>
<li><span data-ttu-id="1b539-916">Ovale</span><span class="sxs-lookup"><span data-stu-id="1b539-916">Oval</span></span></li>
<li><span data-ttu-id="1b539-917">Apri</span><span class="sxs-lookup"><span data-stu-id="1b539-917">Open</span></span></li>
<li><span data-ttu-id="1b539-918">Frecce di espansione</span><span class="sxs-lookup"><span data-stu-id="1b539-918">Chevron</span></span></li>
<li><span data-ttu-id="1b539-919">DoubleChevron</span><span class="sxs-lookup"><span data-stu-id="1b539-919">DoubleChevron</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-920">StartArrowLength</span><span class="sxs-lookup"><span data-stu-id="1b539-920">StartArrowLength</span></span></td>
<td><span data-ttu-id="1b539-921">VgArrowHeadLength.</span><span class="sxs-lookup"><span data-stu-id="1b539-921">VgArrowHeadLength.</span></span> <span data-ttu-id="1b539-922">Lunghezza della freccia per l'inizio della linea.</span><span class="sxs-lookup"><span data-stu-id="1b539-922">Arrowhead length for the start of the line.</span></span> <span data-ttu-id="1b539-923">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="1b539-923">Values are:</span></span>
<ul>
<li><span data-ttu-id="1b539-924">Short</span><span class="sxs-lookup"><span data-stu-id="1b539-924">Short</span></span></li>
<li><span data-ttu-id="1b539-925">Media (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1b539-925">Medium (default)</span></span></li>
<li><span data-ttu-id="1b539-926">long</span><span class="sxs-lookup"><span data-stu-id="1b539-926">Long</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-927">StartArrowWidth</span><span class="sxs-lookup"><span data-stu-id="1b539-927">StartArrowWidth</span></span></td>
<td><span data-ttu-id="1b539-928">VgArrowheadWidth.</span><span class="sxs-lookup"><span data-stu-id="1b539-928">VgArrowheadWidth.</span></span> <span data-ttu-id="1b539-929">Larghezza della freccia per l'inizio della linea.</span><span class="sxs-lookup"><span data-stu-id="1b539-929">Arrowhead width for the start of the line.</span></span> <span data-ttu-id="1b539-930">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="1b539-930">Values are:</span></span>
<ul>
<li><span data-ttu-id="1b539-931">Narrow Medium (impostazione predefinita) Wide</span><span class="sxs-lookup"><span data-stu-id="1b539-931">Narrow Medium (default) Wide</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-932">Peso</span><span class="sxs-lookup"><span data-stu-id="1b539-932">Weight</span></span></td>
<td><span data-ttu-id="1b539-933"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-933"><a href="msdn-online-vml-vglength.md">VgLength</a>.</span></span> <span data-ttu-id="1b539-934">Larghezza della linea.</span><span class="sxs-lookup"><span data-stu-id="1b539-934">Width of line.</span></span> <span data-ttu-id="1b539-935">È compreso tra 0 e 1584.</span><span class="sxs-lookup"><span data-stu-id="1b539-935">Ranges from 0 to 1584.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="1b539-936">L'attributo DashStyle consente all'utente di specificare un modello di tratteggio personalizzato.</span><span class="sxs-lookup"><span data-stu-id="1b539-936">The DashStyle attribute allows the user to specify a custom-defined dash pattern.</span></span> <span data-ttu-id="1b539-937">Questa operazione viene eseguita usando una serie di numeri.</span><span class="sxs-lookup"><span data-stu-id="1b539-937">This is done using a series of numbers.</span></span> <span data-ttu-id="1b539-938">Gli stili dei trattini sono definiti in termini di lunghezza del trattino (la parte disegnata del tratto) e lunghezza dello spazio tra i trattini.</span><span class="sxs-lookup"><span data-stu-id="1b539-938">Dash styles are defined in terms of the length of the dash (the drawn part of the stroke) and the length of the space between the dashes.</span></span> <span data-ttu-id="1b539-939">Le lunghezze sono relative alla larghezza della linea. una lunghezza &quot; pari a 1 è uguale alla larghezza &quot; della riga.</span><span class="sxs-lookup"><span data-stu-id="1b539-939">The lengths are relative to the line width; a length of &quot;1&quot; is equal to the line width.</span></span> <span data-ttu-id="1b539-940">Lo stile EndCap viene applicato a ogni trattino, gli stili freccia no.</span><span class="sxs-lookup"><span data-stu-id="1b539-940">The EndCap style is applied to each dash, arrow styles are not.</span></span> <span data-ttu-id="1b539-941">La stringa definisce prima la lunghezza del trattino e quindi la lunghezza dello spazio.</span><span class="sxs-lookup"><span data-stu-id="1b539-941">The string first defines the length of the dash then the length of the space.</span></span> <span data-ttu-id="1b539-942">Questa operazione può essere ripetuta per formare stili trattini complessi.</span><span class="sxs-lookup"><span data-stu-id="1b539-942">This may be repeated to form complex dash styles.</span></span> <span data-ttu-id="1b539-943">La stringa deve contenere sempre una coppia di numeri. se contiene un numero dispari di numeri, l'ultimo può essere ignorato.</span><span class="sxs-lookup"><span data-stu-id="1b539-943">The string should always contain a pair of numbers; if it contains an odd number of numbers the last may be disregarded.</span></span> <span data-ttu-id="1b539-944">Nella tabella seguente sono elencati alcuni valori tipici e una descrizione dell'effetto desiderato.</span><span class="sxs-lookup"><span data-stu-id="1b539-944">The following table lists some typical values and a description of the intended effect.</span></span> <span data-ttu-id="1b539-945">&quot;0 implica un punto che deve essere simmetrico quattro volte (con estremità arrotondate &quot; deve essere un cerchio).</span><span class="sxs-lookup"><span data-stu-id="1b539-945">&quot;0&quot; implies a dot that should be fourfold symmetrical (with round endcaps it should be a circle).</span></span> <span data-ttu-id="1b539-946">Se l'estremità linea è Flat, un visualizzatore deve scegliere un trattino del sistema operativo predefinito, laddove possibile(ad esempio, qualcosa che è veloce da disegnare).</span><span class="sxs-lookup"><span data-stu-id="1b539-946">If the line endcap is Flat, a viewer should choose a built-in operating system dash where possible (i.e., something that is fast to draw).</span></span> <span data-ttu-id="1b539-947">Di seguito sono riportati alcuni esempi.</span><span class="sxs-lookup"><span data-stu-id="1b539-947">The following shows some examples.</span></span>
</blockquote>
</div>
<div>
 
</div>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b539-948">&quot;2 2&quot;</span><span class="sxs-lookup"><span data-stu-id="1b539-948">&quot;2 2&quot;</span></span></td>
<td><span data-ttu-id="1b539-949">trattini brevi (ogni trattino e lo spazio tra è il doppio della larghezza della linea)</span><span class="sxs-lookup"><span data-stu-id="1b539-949">short-dashes (each dash and the space in between is twice the width of the line)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-950">&quot;1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="1b539-950">&quot;1 2&quot;</span></span></td>
<td><span data-ttu-id="1b539-951">punto (ogni trattino è la larghezza della linea mentre ogni spazio è il doppio della larghezza della linea)</span><span class="sxs-lookup"><span data-stu-id="1b539-951">dot (each dash is the width of the line while each space is twice the width of the line)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-952">&quot;4 2&quot;</span><span class="sxs-lookup"><span data-stu-id="1b539-952">&quot;4 2&quot;</span></span></td>
<td><span data-ttu-id="1b539-953">trattino (ogni trattino è quattro volte la larghezza della linea mentre ogni spazio è doppio della larghezza della linea)</span><span class="sxs-lookup"><span data-stu-id="1b539-953">dash (each dash is four times the width of the line while each space is twice the width of the line)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-954">&quot;8 2&quot;</span><span class="sxs-lookup"><span data-stu-id="1b539-954">&quot;8 2&quot;</span></span></td>
<td><span data-ttu-id="1b539-955">trattino lungo</span><span class="sxs-lookup"><span data-stu-id="1b539-955">long-dash</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-956">&quot;4 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="1b539-956">&quot;4 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="1b539-957">trattino punto</span><span class="sxs-lookup"><span data-stu-id="1b539-957">dash dot</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-958">&quot;8 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="1b539-958">&quot;8 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="1b539-959">punto con trattino lungo</span><span class="sxs-lookup"><span data-stu-id="1b539-959">long-dash dot</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-960">&quot;8 2 1 2 1 2&quot;</span><span class="sxs-lookup"><span data-stu-id="1b539-960">&quot;8 2 1 2 1 2&quot;</span></span></td>
<td><span data-ttu-id="1b539-961">punto con trattino lungo</span><span class="sxs-lookup"><span data-stu-id="1b539-961">long-dash dot dot</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="textpath-element"></a><span data-ttu-id="1b539-962">Elemento TextPath</span><span class="sxs-lookup"><span data-stu-id="1b539-962">TextPath element</span></span>

<span data-ttu-id="1b539-963">Descrive un percorso vettoriale in base ai dati di testo, al tipo di carattere e agli stili forniti.</span><span class="sxs-lookup"><span data-stu-id="1b539-963">Describes a vector path based on the text data, font, and styles supplied.</span></span> <span data-ttu-id="1b539-964">Il percorso di testo viene wared in modo che sia conforme a un **elemento Path,** se specificato.</span><span class="sxs-lookup"><span data-stu-id="1b539-964">The text path is warped to conform to a **Path** element if supplied.</span></span>



|   <span data-ttu-id="1b539-965">Attributo</span><span class="sxs-lookup"><span data-stu-id="1b539-965">Attribute</span></span>        |   <span data-ttu-id="1b539-966">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b539-966">Description</span></span>                                                                                                                                                                                      |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b539-967">FitPath</span><span class="sxs-lookup"><span data-stu-id="1b539-967">FitPath</span></span>  | <span data-ttu-id="1b539-968">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-968">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="1b539-969">Ridimensiona il testo per riempire il percorso su cui si trova.</span><span class="sxs-lookup"><span data-stu-id="1b539-969">Sizes the text to fill the path it lies out on.</span></span>                                 |
| <span data-ttu-id="1b539-970">FitShape</span><span class="sxs-lookup"><span data-stu-id="1b539-970">FitShape</span></span> | <span data-ttu-id="1b539-971">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-971">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="1b539-972">Estende il percorso del testo ai bordi della casella della forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-972">Stretches the text path out to the edges of the shape box.</span></span>                      |
| <span data-ttu-id="1b539-973">On</span><span class="sxs-lookup"><span data-stu-id="1b539-973">On</span></span>       | <span data-ttu-id="1b539-974">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-974">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="1b539-975">Determina se i percorsi dei caratteri vengono visualizzati o meno.</span><span class="sxs-lookup"><span data-stu-id="1b539-975">Determines whether the character paths are displayed or not.</span></span>                    |
| <span data-ttu-id="1b539-976">Stringa</span><span class="sxs-lookup"><span data-stu-id="1b539-976">String</span></span>   | <span data-ttu-id="1b539-977">Stringa.</span><span class="sxs-lookup"><span data-stu-id="1b539-977">String.</span></span> <span data-ttu-id="1b539-978">Testo di cui eseguire il rendering come percorso di testo.</span><span class="sxs-lookup"><span data-stu-id="1b539-978">The text to render as a text path.</span></span>                                                                                    |
| <span data-ttu-id="1b539-979">Taglio</span><span class="sxs-lookup"><span data-stu-id="1b539-979">Trim</span></span>     | <span data-ttu-id="1b539-980">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-980">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="1b539-981">Rimuove qualsiasi spazio aggiuntivo riservato a ascendenti e discendenti se non viene usato.</span><span class="sxs-lookup"><span data-stu-id="1b539-981">Removes any additional space reserved for ascenders and descenders if not used.</span></span> |
| <span data-ttu-id="1b539-982">Xscale</span><span class="sxs-lookup"><span data-stu-id="1b539-982">XScale</span></span>   | <span data-ttu-id="1b539-983">[VgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-983">[VgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="1b539-984">Usare la misura straight x invece di misurare lungo il percorso.</span><span class="sxs-lookup"><span data-stu-id="1b539-984">Use straight x measurement instead of measuring along the path.</span></span>                 |



 

## <a name="data-types-used-in-the-vml-object-model"></a><span data-ttu-id="1b539-985">Tipi di dati usati nel modello a oggetti VML</span><span class="sxs-lookup"><span data-stu-id="1b539-985">Data Types Used in the VML Object Model</span></span>

<span data-ttu-id="1b539-986">I tipi di dati seguenti vengono usati dal modello a oggetti VML.</span><span class="sxs-lookup"><span data-stu-id="1b539-986">The following data types are used by the VML Object Model.</span></span>

-   [<span data-ttu-id="1b539-987">Double</span><span class="sxs-lookup"><span data-stu-id="1b539-987">Double</span></span>](/windows)
-   [<span data-ttu-id="1b539-988">Fisso</span><span class="sxs-lookup"><span data-stu-id="1b539-988">Fixed</span></span>](/windows)
-   [<span data-ttu-id="1b539-989">Integer</span><span class="sxs-lookup"><span data-stu-id="1b539-989">Integer</span></span>](/windows)
-   [<span data-ttu-id="1b539-990">IVgAdjustments</span><span class="sxs-lookup"><span data-stu-id="1b539-990">IVgAdjustments</span></span>](/windows)
-   [<span data-ttu-id="1b539-991">IVgColor</span><span class="sxs-lookup"><span data-stu-id="1b539-991">IVgColor</span></span>](/windows)
-   [<span data-ttu-id="1b539-992">IVgEquation</span><span class="sxs-lookup"><span data-stu-id="1b539-992">IVgEquation</span></span>](/windows)
-   [<span data-ttu-id="1b539-993">IVgFixedRectangle</span><span class="sxs-lookup"><span data-stu-id="1b539-993">IVgFixedRectangle</span></span>](/windows)
-   [<span data-ttu-id="1b539-994">IVgFixedRectangleArray</span><span class="sxs-lookup"><span data-stu-id="1b539-994">IVgFixedRectangleArray</span></span>](/windows)
-   [<span data-ttu-id="1b539-995">IVgFormula</span><span class="sxs-lookup"><span data-stu-id="1b539-995">IVgFormula</span></span>](/windows)
-   [<span data-ttu-id="1b539-996">IVgFormulas</span><span class="sxs-lookup"><span data-stu-id="1b539-996">IVgFormulas</span></span>](/windows)
-   [<span data-ttu-id="1b539-997">IVgGradientColorArray</span><span class="sxs-lookup"><span data-stu-id="1b539-997">IVgGradientColorArray</span></span>](/windows)
-   [<span data-ttu-id="1b539-998">IVgPoints</span><span class="sxs-lookup"><span data-stu-id="1b539-998">IVgPoints</span></span>](/windows)
-   [<span data-ttu-id="1b539-999">IVgSkewMatrix</span><span class="sxs-lookup"><span data-stu-id="1b539-999">IVgSkewMatrix</span></span>](/windows)
-   [<span data-ttu-id="1b539-1000">IVgSkewOffset</span><span class="sxs-lookup"><span data-stu-id="1b539-1000">IVgSkewOffset</span></span>](/windows)
-   [<span data-ttu-id="1b539-1001">IVgVector2D</span><span class="sxs-lookup"><span data-stu-id="1b539-1001">IVgVector2D</span></span>](/windows)
-   [<span data-ttu-id="1b539-1002">IVgVector3D</span><span class="sxs-lookup"><span data-stu-id="1b539-1002">IVgVector3D</span></span>](/windows)
-   [<span data-ttu-id="1b539-1003">Length</span><span class="sxs-lookup"><span data-stu-id="1b539-1003">Length</span></span>](/windows)
-   [<span data-ttu-id="1b539-1004">Measure</span><span class="sxs-lookup"><span data-stu-id="1b539-1004">Measure</span></span>](/windows)
-   [<span data-ttu-id="1b539-1005">Stringa</span><span class="sxs-lookup"><span data-stu-id="1b539-1005">String</span></span>](/windows)
-   [<span data-ttu-id="1b539-1006">VgBlackWhiteMode</span><span class="sxs-lookup"><span data-stu-id="1b539-1006">VgBlackWhiteMode</span></span>](/windows)
-   [<span data-ttu-id="1b539-1007">VgFraction</span><span class="sxs-lookup"><span data-stu-id="1b539-1007">VgFraction</span></span>](/windows)
-   [<span data-ttu-id="1b539-1008">VgTriState</span><span class="sxs-lookup"><span data-stu-id="1b539-1008">VgTriState</span></span>](/windows)

<span data-ttu-id="1b539-1009">**Tipo di dati Double**</span><span class="sxs-lookup"><span data-stu-id="1b539-1009">**Double data type**</span></span>

<span data-ttu-id="1b539-1010">Intero a precisione doppia con intervallo compreso tra -infinito e infinito.</span><span class="sxs-lookup"><span data-stu-id="1b539-1010">A double precision integer with range from -infinity to infinity.</span></span>

<span data-ttu-id="1b539-1011">**Tipo di dati fisso**</span><span class="sxs-lookup"><span data-stu-id="1b539-1011">**Fixed data type**</span></span>

<span data-ttu-id="1b539-1012">Numero a virgola mobile con intervallo compreso tra -32.766,0 e 32.766,0.</span><span class="sxs-lookup"><span data-stu-id="1b539-1012">Floating point number with range from -32,766.0 to 32,766.0.</span></span>

<span data-ttu-id="1b539-1013">**Tipo di dati Integer**</span><span class="sxs-lookup"><span data-stu-id="1b539-1013">**Integer data type**</span></span>

<span data-ttu-id="1b539-1014">Intero con un intervallo compreso tra -infinito e infinito.</span><span class="sxs-lookup"><span data-stu-id="1b539-1014">An integer with a range from -infinity to infinity.</span></span>

<span data-ttu-id="1b539-1015">**Tipo di dati IVgAdjustments**</span><span class="sxs-lookup"><span data-stu-id="1b539-1015">**IVgAdjustments data type**</span></span>

<span data-ttu-id="1b539-1016">Raccolta di modifiche a una forma che può essere utilizzata per modificare le dimensioni di una forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-1016">Collection of adjustments to a shape that can be used to change the dimensions of a shape.</span></span> <span data-ttu-id="1b539-1017">Le rettifiche possono essere usate come segnaposto temporanei o per qualsiasi motivo si usino le variabili.</span><span class="sxs-lookup"><span data-stu-id="1b539-1017">Adjustments can be used as temporary placeholders or for any reason you would use variables.</span></span> <span data-ttu-id="1b539-1018">Nella raccolta sono presenti solo 8 modifiche.</span><span class="sxs-lookup"><span data-stu-id="1b539-1018">There are only 8 adjustments in the collection.</span></span>



| <span data-ttu-id="1b539-1019">Attributo</span><span class="sxs-lookup"><span data-stu-id="1b539-1019">Attribute</span></span> | <span data-ttu-id="1b539-1020">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b539-1020">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b539-1021">Exists</span><span class="sxs-lookup"><span data-stu-id="1b539-1021">Exists</span></span>     | <span data-ttu-id="1b539-1022">[IVgTriState](msdn-online-vml-vgtristate.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-1022">[IVgTriState](msdn-online-vml-vgtristate.md).</span></span> <span data-ttu-id="1b539-1023">Determina se esiste una rettifica specificata.</span><span class="sxs-lookup"><span data-stu-id="1b539-1023">Determines whether a specified adjustment exists.</span></span> <span data-ttu-id="1b539-1024">Si noti che è necessario usare un indice. ovvero exists( item ) deve essere usato per recuperare l'esistenza di un elemento.</span><span class="sxs-lookup"><span data-stu-id="1b539-1024">Note that an index must be used; that is, exists( item ) must be used to retrieve the existence of an item.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="1b539-1025">Elemento</span><span class="sxs-lookup"><span data-stu-id="1b539-1025">Item</span></span>       | <span data-ttu-id="1b539-1026">[Long](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-1026">[Long](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="1b539-1027">Matrice di rettifiche indicizzate da 0 a 7.</span><span class="sxs-lookup"><span data-stu-id="1b539-1027">Array of adjustments indexed from 0 to 7.</span></span> <span data-ttu-id="1b539-1028">Si noti che le modifiche possono essere specificate con parsimonio. in altri, i valori intermedi delle matrici potrebbero non essere sempre riempiti.</span><span class="sxs-lookup"><span data-stu-id="1b539-1028">Note that adjustments may be sparcely specified; that is, intermediate array values may not always be filled.</span></span> <span data-ttu-id="1b539-1029">Ad esempio, l'elemento 1, 3 e 5 può avere valori per una lunghezza pari a 3, con item(0), item(2) e item(4) specificati.</span><span class="sxs-lookup"><span data-stu-id="1b539-1029">For example, item 1, 3, and 5 could have values for a length of 3, with item(0), item(2), and item(4) specified.</span></span> <span data-ttu-id="1b539-1030">Per verificare se esiste un elemento, usare l'attributo Exists.</span><span class="sxs-lookup"><span data-stu-id="1b539-1030">To see if an item exists, use the Exists attribute.</span></span> |
| <span data-ttu-id="1b539-1031">Length</span><span class="sxs-lookup"><span data-stu-id="1b539-1031">Length</span></span>     | <span data-ttu-id="1b539-1032">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-1032">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="1b539-1033">Numero di modifiche.</span><span class="sxs-lookup"><span data-stu-id="1b539-1033">Number of adjustments.</span></span> <span data-ttu-id="1b539-1034">Non può essere maggiore di 8.</span><span class="sxs-lookup"><span data-stu-id="1b539-1034">Can be no greater than 8.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="1b539-1035">Valore</span><span class="sxs-lookup"><span data-stu-id="1b539-1035">Value</span></span>      | <span data-ttu-id="1b539-1036">[Stringa](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-1036">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="1b539-1037">Rappresentazione testuale dei valori numerici, con virgole tra ogni numero.</span><span class="sxs-lookup"><span data-stu-id="1b539-1037">Text representation of numeric values, with commas between each number.</span></span>                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="1b539-1038">**IVgColor**</span><span class="sxs-lookup"><span data-stu-id="1b539-1038">**IVgColor**</span></span>

<span data-ttu-id="1b539-1039">Specifica un colore.</span><span class="sxs-lookup"><span data-stu-id="1b539-1039">Specifies a color.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1b539-1040">Attributi</span><span class="sxs-lookup"><span data-stu-id="1b539-1040">Attributes</span></span></th>
<th><span data-ttu-id="1b539-1041">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b539-1041">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b539-1042">RGB</span><span class="sxs-lookup"><span data-stu-id="1b539-1042">RGB</span></span></td>
<td><span data-ttu-id="1b539-1043"><strong>VgRGBType</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b539-1043"><strong>VgRGBType</strong>.</span></span> <span data-ttu-id="1b539-1044">Valore RGB (Long) del colore.</span><span class="sxs-lookup"><span data-stu-id="1b539-1044">RGB value (Long) of the color.</span></span> <span data-ttu-id="1b539-1045">Valido solo se Type è RGB.</span><span class="sxs-lookup"><span data-stu-id="1b539-1045">Only valid if Type is RGB.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-1046">R</span><span class="sxs-lookup"><span data-stu-id="1b539-1046">R</span></span></td>
<td><span data-ttu-id="1b539-1047"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-1047"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="1b539-1048">Componente rosso del colore.</span><span class="sxs-lookup"><span data-stu-id="1b539-1048">Red component of the color.</span></span> <span data-ttu-id="1b539-1049">Può essere compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="1b539-1049">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-1050">G</span><span class="sxs-lookup"><span data-stu-id="1b539-1050">G</span></span></td>
<td><span data-ttu-id="1b539-1051"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-1051"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="1b539-1052">Componente verde del colore.</span><span class="sxs-lookup"><span data-stu-id="1b539-1052">Green component of the color.</span></span> <span data-ttu-id="1b539-1053">Può essere compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="1b539-1053">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-1054">B</span><span class="sxs-lookup"><span data-stu-id="1b539-1054">B</span></span></td>
<td><span data-ttu-id="1b539-1055"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-1055"><a href="#data-types-used-in-the-vml-object-model">Integer</a>.</span></span> <span data-ttu-id="1b539-1056">Componente blu del colore.</span><span class="sxs-lookup"><span data-stu-id="1b539-1056">Blue component of the color.</span></span> <span data-ttu-id="1b539-1057">Può essere compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="1b539-1057">Can range between 0 and 255.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-1058">Stringa</span><span class="sxs-lookup"><span data-stu-id="1b539-1058">String</span></span></td>
<td><span data-ttu-id="1b539-1059"><a href="#data-types-used-in-the-vml-object-model">Stringa</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-1059"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="1b539-1060">Rappresentazione testuale del colore.</span><span class="sxs-lookup"><span data-stu-id="1b539-1060">Text representation of the color.</span></span> <span data-ttu-id="1b539-1061">Sono supportati i tipi di colore denominati seguenti:</span><span class="sxs-lookup"><span data-stu-id="1b539-1061">The following named color types are supported:</span></span>
<ul>
<li><span data-ttu-id="1b539-1062">Nero (#000000)</span><span class="sxs-lookup"><span data-stu-id="1b539-1062">Black (#000000)</span></span></li>
<li><span data-ttu-id="1b539-1063">Silver (#C0C0C0)</span><span class="sxs-lookup"><span data-stu-id="1b539-1063">Silver (#C0C0C0)</span></span></li>
<li><span data-ttu-id="1b539-1064">Grigio (#808080)</span><span class="sxs-lookup"><span data-stu-id="1b539-1064">Gray (#808080)</span></span></li>
<li><span data-ttu-id="1b539-1065">Bianco (#FFFFFF)</span><span class="sxs-lookup"><span data-stu-id="1b539-1065">White (#FFFFFF)</span></span></li>
<li><span data-ttu-id="1b539-1066">Maroon (#800000)</span><span class="sxs-lookup"><span data-stu-id="1b539-1066">Maroon (#800000)</span></span></li>
<li><span data-ttu-id="1b539-1067">Rosso (#FF0000)</span><span class="sxs-lookup"><span data-stu-id="1b539-1067">Red (#FF0000)</span></span></li>
<li><span data-ttu-id="1b539-1068">Viola (#800080)</span><span class="sxs-lookup"><span data-stu-id="1b539-1068">Purple (#800080)</span></span></li>
<li><span data-ttu-id="1b539-1069">Fucsia (#FF00FF)</span><span class="sxs-lookup"><span data-stu-id="1b539-1069">Fuchsia (#FF00FF)</span></span></li>
<li><span data-ttu-id="1b539-1070">Verde (#008000)</span><span class="sxs-lookup"><span data-stu-id="1b539-1070">Green (#008000)</span></span></li>
<li><span data-ttu-id="1b539-1071">Lime (#00FF00)</span><span class="sxs-lookup"><span data-stu-id="1b539-1071">Lime (#00FF00)</span></span></li>
<li><span data-ttu-id="1b539-1072">Olive (#808000)</span><span class="sxs-lookup"><span data-stu-id="1b539-1072">Olive (#808000)</span></span></li>
<li><span data-ttu-id="1b539-1073">Giallo (#FFFF00)</span><span class="sxs-lookup"><span data-stu-id="1b539-1073">Yellow (#FFFF00)</span></span></li>
<li><span data-ttu-id="1b539-1074">Navy (#000080)</span><span class="sxs-lookup"><span data-stu-id="1b539-1074">Navy (#000080)</span></span></li>
<li><span data-ttu-id="1b539-1075">Blu (#0000FF)</span><span class="sxs-lookup"><span data-stu-id="1b539-1075">Blue (#0000FF)</span></span></li>
<li><span data-ttu-id="1b539-1076">Teal (#008080)</span><span class="sxs-lookup"><span data-stu-id="1b539-1076">Teal (#008080)</span></span></li>
<li><span data-ttu-id="1b539-1077">Aqua (#00FFFF)</span><span class="sxs-lookup"><span data-stu-id="1b539-1077">Aqua (#00FFFF)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-1078">Tipo</span><span class="sxs-lookup"><span data-stu-id="1b539-1078">Type</span></span></td>
<td><span data-ttu-id="1b539-1079"><strong>VgColorType</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b539-1079"><strong>VgColorType</strong>.</span></span> <span data-ttu-id="1b539-1080">Tipo di colore.</span><span class="sxs-lookup"><span data-stu-id="1b539-1080">Type of color.</span></span> <span data-ttu-id="1b539-1081">Uno dei tipi seguenti:</span><span class="sxs-lookup"><span data-stu-id="1b539-1081">One of the following types:</span></span>
<ul>
<li><span data-ttu-id="1b539-1082">Mixed</span><span class="sxs-lookup"><span data-stu-id="1b539-1082">Mixed</span></span></li>
<li><span data-ttu-id="1b539-1083">denominata</span><span class="sxs-lookup"><span data-stu-id="1b539-1083">Named</span></span></li>
<li><span data-ttu-id="1b539-1084">RGB</span><span class="sxs-lookup"><span data-stu-id="1b539-1084">RGB</span></span></li>
<li><span data-ttu-id="1b539-1085">Schema</span><span class="sxs-lookup"><span data-stu-id="1b539-1085">Scheme</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1b539-1086">**IVgEquation**</span><span class="sxs-lookup"><span data-stu-id="1b539-1086">**IVgEquation**</span></span>

<span data-ttu-id="1b539-1087">Equazioni usate per le formule.</span><span class="sxs-lookup"><span data-stu-id="1b539-1087">Equations used for formulas.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b539-1088">Operazione</span><span class="sxs-lookup"><span data-stu-id="1b539-1088">Operation</span></span></td>
<td><span data-ttu-id="1b539-1089"><strong>VgEquationOperationType</strong> Nome dell'operazione da eseguire sui parametri.</span><span class="sxs-lookup"><span data-stu-id="1b539-1089"><strong>VgEquationOperationType</strong> Name of operation to perform on the parameters.</span></span> <span data-ttu-id="1b539-1090">In un'equazione è possibile usare le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="1b539-1090">The following operations can be used in an equation:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1b539-1091">Operazione</span><span class="sxs-lookup"><span data-stu-id="1b539-1091">Operation</span></span></th>
<th><span data-ttu-id="1b539-1092">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b539-1092">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b539-1093">Abs</span><span class="sxs-lookup"><span data-stu-id="1b539-1093">Abs</span></span></td>
<td><span data-ttu-id="1b539-1094">Valore assoluto.</span><span class="sxs-lookup"><span data-stu-id="1b539-1094">Absolute value.</span></span> <br/> <span data-ttu-id="1b539-1095"><strong>abs</strong>(v)</span><span class="sxs-lookup"><span data-stu-id="1b539-1095"><strong>abs</strong>(v)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-1096">Atan2</span><span class="sxs-lookup"><span data-stu-id="1b539-1096">Atan2</span></span></td>
<td><span data-ttu-id="1b539-1097">Aritmetica polare: risultati in unità fd (gradi moltiplicati per 65536).</span><span class="sxs-lookup"><span data-stu-id="1b539-1097">Polar arithmetic--results in fd units (degrees multiplied by 65536).</span></span><br/> <span data-ttu-id="1b539-1098"><strong>atan2</strong>(p1,v)</span><span class="sxs-lookup"><span data-stu-id="1b539-1098"><strong>atan2</strong>(p1,v)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-1099">Cos</span><span class="sxs-lookup"><span data-stu-id="1b539-1099">Cos</span></span></td>
<td><span data-ttu-id="1b539-1100">Coseno, argomento in unità fd (gradi moltiplicati per 65536).</span><span class="sxs-lookup"><span data-stu-id="1b539-1100">Cosine, argument in fd units (degrees multiplied by 65536).</span></span><br/> <span data-ttu-id="1b539-1101">v \* <strong>cos</strong>(p1)</span><span class="sxs-lookup"><span data-stu-id="1b539-1101">v \* <strong>cos</strong>(p1)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-1102">Cosatan2</span><span class="sxs-lookup"><span data-stu-id="1b539-1102">Cosatan2</span></span></td>
<td><span data-ttu-id="1b539-1103">Mantiene l'accuratezza completa nel calcolo intermedio.</span><span class="sxs-lookup"><span data-stu-id="1b539-1103">Preserves full accuracy in intermediate calculation.</span></span><br/> <span data-ttu-id="1b539-1104">v \* <strong>cos(atan2(</strong> p2,p1 <strong>))</strong></span><span class="sxs-lookup"><span data-stu-id="1b539-1104">v \* <strong>cos(atan2(</strong> p2,p1 <strong>))</strong></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-1105">Ellisse</span><span class="sxs-lookup"><span data-stu-id="1b539-1105">Ellipse</span></span></td>
<td><span data-ttu-id="1b539-1106">Ellisse</span><span class="sxs-lookup"><span data-stu-id="1b539-1106">Ellipse</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-1107">Se</span><span class="sxs-lookup"><span data-stu-id="1b539-1107">If</span></span></td>
<td><span data-ttu-id="1b539-1108">Se il test della condizione.</span><span class="sxs-lookup"><span data-stu-id="1b539-1108">If Condition test.</span></span> <span data-ttu-id="1b539-1109">v > 0 <strong>?</strong></span><span class="sxs-lookup"><span data-stu-id="1b539-1109">v > 0 <strong>?</strong></span></span> <span data-ttu-id="1b539-1110">p1 : p2</span><span class="sxs-lookup"><span data-stu-id="1b539-1110">p1 : p2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-1111">Max</span><span class="sxs-lookup"><span data-stu-id="1b539-1111">Max</span></span></td>
<td><span data-ttu-id="1b539-1112">Maggiore di due valori.</span><span class="sxs-lookup"><span data-stu-id="1b539-1112">The greater of two values.</span></span> <br/> <span data-ttu-id="1b539-1113"><strong>max</strong>(v,p1)</span><span class="sxs-lookup"><span data-stu-id="1b539-1113"><strong>max</strong>(v,p1)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-1114">Mid</span><span class="sxs-lookup"><span data-stu-id="1b539-1114">Mid</span></span></td>
<td><span data-ttu-id="1b539-1115">Media ( v + p1)/2</span><span class="sxs-lookup"><span data-stu-id="1b539-1115">Average ( v + p1)/2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-1116">Min</span><span class="sxs-lookup"><span data-stu-id="1b539-1116">Min</span></span></td>
<td><span data-ttu-id="1b539-1117">Minore di due valori.</span><span class="sxs-lookup"><span data-stu-id="1b539-1117">The lesser of two values.</span></span> <span data-ttu-id="1b539-1118"><strong>min</strong>(v,p1)</span><span class="sxs-lookup"><span data-stu-id="1b539-1118"><strong>min</strong>(v,p1)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-1119">Mod</span><span class="sxs-lookup"><span data-stu-id="1b539-1119">Mod</span></span></td>
<td><span data-ttu-id="1b539-1120">Modulo.</span><span class="sxs-lookup"><span data-stu-id="1b539-1120">Modulus.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-1121">Prodotto</span><span class="sxs-lookup"><span data-stu-id="1b539-1121">Product</span></span></td>
<td><span data-ttu-id="1b539-1122">Usato per la moltiplicazione e la divisione.</span><span class="sxs-lookup"><span data-stu-id="1b539-1122">Used for multiplication and division.</span></span> <span data-ttu-id="1b539-1123">v \* p1 /p2</span><span class="sxs-lookup"><span data-stu-id="1b539-1123">v \* p1 / p2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-1124">Sin</span><span class="sxs-lookup"><span data-stu-id="1b539-1124">Sin</span></span></td>
<td><span data-ttu-id="1b539-1125">Seno, argomento in unità fd (gradi moltiplicati per 65536).</span><span class="sxs-lookup"><span data-stu-id="1b539-1125">Sine, argument in fd units (degrees multiplied by 65536).</span></span> <br/> <span data-ttu-id="1b539-1126">v \* <strong>sin</strong>(p1)</span><span class="sxs-lookup"><span data-stu-id="1b539-1126">v \* <strong>sin</strong>(p1)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-1127">Sinatan2</span><span class="sxs-lookup"><span data-stu-id="1b539-1127">Sinatan2</span></span></td>
<td><span data-ttu-id="1b539-1128">Mantiene l'accuratezza completa nel calcolo intermedio.</span><span class="sxs-lookup"><span data-stu-id="1b539-1128">Preserves full accuracy in intermediate calculation.</span></span> <span data-ttu-id="1b539-1129">v \* <strong>sin</strong>(<strong>atan2</strong>(p2,p1))</span><span class="sxs-lookup"><span data-stu-id="1b539-1129">v \* <strong>sin</strong>(<strong>atan2</strong>(p2,p1))</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-1130">Sqrt</span><span class="sxs-lookup"><span data-stu-id="1b539-1130">Sqrt</span></span></td>
<td><span data-ttu-id="1b539-1131">Il risultato è positivo e viene arrotondato per e per intero.</span><span class="sxs-lookup"><span data-stu-id="1b539-1131">Result is positive and rounds down.</span></span> <br/> <span data-ttu-id="1b539-1132"><strong>sqrt</strong>(v)</span><span class="sxs-lookup"><span data-stu-id="1b539-1132"><strong>sqrt</strong>(v)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-1133">Sum</span><span class="sxs-lookup"><span data-stu-id="1b539-1133">Sum</span></span></td>
<td><span data-ttu-id="1b539-1134">Usato per l'addizione e la sottrazione.</span><span class="sxs-lookup"><span data-stu-id="1b539-1134">Used for addition and subtraction.</span></span><br/> <span data-ttu-id="1b539-1135">v + p1 p2</span><span class="sxs-lookup"><span data-stu-id="1b539-1135">v + p1 p2</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-1136">Sumangle</span><span class="sxs-lookup"><span data-stu-id="1b539-1136">Sumangle</span></span></td>
<td><span data-ttu-id="1b539-1137">Angolo esistente (ridimensionato di 65536), dove p1 e p2 sono in gradi.</span><span class="sxs-lookup"><span data-stu-id="1b539-1137">Existing angle (scaled by 65536), where p1 and p2 are in degrees.</span></span><br/> <span data-ttu-id="1b539-1138">v + p1 \* 65536 + p2 \* 65536</span><span class="sxs-lookup"><span data-stu-id="1b539-1138">v + p1 \* 65536 + p2 \* 65536</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-1139">Tan</span><span class="sxs-lookup"><span data-stu-id="1b539-1139">Tan</span></span></td>
<td><span data-ttu-id="1b539-1140">Tangente, l'argomento è in unità fd (gradi moltiplicati per 65536).</span><span class="sxs-lookup"><span data-stu-id="1b539-1140">Tangent, argument is in fd units (degrees multiplied by 65536).</span></span> <br/> <span data-ttu-id="1b539-1141">v \* tan( p1 )</span><span class="sxs-lookup"><span data-stu-id="1b539-1141">v \* tan( p1 )</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-1142">Val</span><span class="sxs-lookup"><span data-stu-id="1b539-1142">Val</span></span></td>
<td><span data-ttu-id="1b539-1143">Definisce un valore guida da un altro valore.</span><span class="sxs-lookup"><span data-stu-id="1b539-1143">Defines a guide value from some other value.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-1144">Param1</span><span class="sxs-lookup"><span data-stu-id="1b539-1144">Param1</span></span></td>
<td><span data-ttu-id="1b539-1145"><strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b539-1145"><strong>Integer</strong>.</span></span> <span data-ttu-id="1b539-1146">Primo parametro.</span><span class="sxs-lookup"><span data-stu-id="1b539-1146">The first parameter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-1147">Paramtype1</span><span class="sxs-lookup"><span data-stu-id="1b539-1147">Paramtype1</span></span></td>
<td><span data-ttu-id="1b539-1148"><strong>VgFormulaParamType</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b539-1148"><strong>VgFormulaParamType</strong>.</span></span> <span data-ttu-id="1b539-1149">Tipo del primo parametro.</span><span class="sxs-lookup"><span data-stu-id="1b539-1149">The type of the first parameter.</span></span> <span data-ttu-id="1b539-1150">Sono supportati i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="1b539-1150">The following values are supported:</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1b539-1151">Tipo</span><span class="sxs-lookup"><span data-stu-id="1b539-1151">Type</span></span></th>
<th><span data-ttu-id="1b539-1152">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b539-1152">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b539-1153">Valore</span><span class="sxs-lookup"><span data-stu-id="1b539-1153">Value</span></span></td>
<td><span data-ttu-id="1b539-1154">Il parametro è un valore semplice.</span><span class="sxs-lookup"><span data-stu-id="1b539-1154">Parameter is simple value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-1155">AdjustmentReference</span><span class="sxs-lookup"><span data-stu-id="1b539-1155">AdjustmentReference</span></span></td>
<td><span data-ttu-id="1b539-1156">Il parametro è un riferimento a una rettifica.</span><span class="sxs-lookup"><span data-stu-id="1b539-1156">Parameter is a reference to an adjustment.</span></span> <span data-ttu-id="1b539-1157">Ad esempio, se il primo parametro è 1, verrà usato il valore della prima rettifica.</span><span class="sxs-lookup"><span data-stu-id="1b539-1157">For example, if the first parameter is 1, then the value of the first adjustment will be used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-1158">FormulaReference</span><span class="sxs-lookup"><span data-stu-id="1b539-1158">FormulaReference</span></span></td>
<td><span data-ttu-id="1b539-1159">Il parametro è il risultato di un riferimento al risultato di una formula precedente.</span><span class="sxs-lookup"><span data-stu-id="1b539-1159">Parameter is the result of a reference to the result of a previous formula.</span></span> <span data-ttu-id="1b539-1160">Ad esempio, se il primo parametro è 2, verrà usato il risultato della formula 2.</span><span class="sxs-lookup"><span data-stu-id="1b539-1160">For example, if the first parameter is 2, then the result of formula 2 will be used.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-1161">Param2</span><span class="sxs-lookup"><span data-stu-id="1b539-1161">Param2</span></span></td>
<td><span data-ttu-id="1b539-1162"><strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b539-1162"><strong>Integer</strong>.</span></span> <span data-ttu-id="1b539-1163">Secondo parametro.</span><span class="sxs-lookup"><span data-stu-id="1b539-1163">The second parameter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-1164">Paramtype2</span><span class="sxs-lookup"><span data-stu-id="1b539-1164">Paramtype2</span></span></td>
<td><span data-ttu-id="1b539-1165"><strong>VgFormulaParamType</strong> Tipo del parametro 2.</span><span class="sxs-lookup"><span data-stu-id="1b539-1165"><strong>VgFormulaParamType</strong> The type of parameter 2.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-1166">Val</span><span class="sxs-lookup"><span data-stu-id="1b539-1166">Val</span></span></td>
<td><span data-ttu-id="1b539-1167"><strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b539-1167"><strong>Integer</strong>.</span></span> <span data-ttu-id="1b539-1168">Risultato.</span><span class="sxs-lookup"><span data-stu-id="1b539-1168">The result.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-1169">Valtype2</span><span class="sxs-lookup"><span data-stu-id="1b539-1169">Valtype2</span></span></td>
<td><span data-ttu-id="1b539-1170"><strong>VgFormulaParamType</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b539-1170"><strong>VgFormulaParamType</strong>.</span></span> <span data-ttu-id="1b539-1171">Tipo del risultato.</span><span class="sxs-lookup"><span data-stu-id="1b539-1171">The type of the result.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1b539-1172">**IVgFixedRectangle**</span><span class="sxs-lookup"><span data-stu-id="1b539-1172">**IVgFixedRectangle**</span></span>

<span data-ttu-id="1b539-1173">Specifica un rettangolo fisso.</span><span class="sxs-lookup"><span data-stu-id="1b539-1173">Specifies a fixed rectangle.</span></span>



| <span data-ttu-id="1b539-1174">Attributo</span><span class="sxs-lookup"><span data-stu-id="1b539-1174">Attribute</span></span> | <span data-ttu-id="1b539-1175">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b539-1175">Description</span></span>                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b539-1176">Valore</span><span class="sxs-lookup"><span data-stu-id="1b539-1176">Value</span></span>      | <span data-ttu-id="1b539-1177">[Stringa](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-1177">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="1b539-1178">Valore di testo che specifica il percorso.</span><span class="sxs-lookup"><span data-stu-id="1b539-1178">Text value specifying the path.</span></span>         |
| <span data-ttu-id="1b539-1179">Sinistra</span><span class="sxs-lookup"><span data-stu-id="1b539-1179">Left</span></span>       | <span data-ttu-id="1b539-1180">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-1180">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="1b539-1181">Coordinata più a sinistra del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="1b539-1181">Leftmost coordinate of the rectangle.</span></span>   |
| <span data-ttu-id="1b539-1182">Inizio</span><span class="sxs-lookup"><span data-stu-id="1b539-1182">Top</span></span>        | <span data-ttu-id="1b539-1183">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-1183">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="1b539-1184">Coordinata superiore del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="1b539-1184">Topmost coordinate of the rectangle.</span></span>    |
| <span data-ttu-id="1b539-1185">Destra</span><span class="sxs-lookup"><span data-stu-id="1b539-1185">Right</span></span>      | <span data-ttu-id="1b539-1186">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-1186">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="1b539-1187">Coordinata più a destra del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="1b539-1187">Rightmost coordinate of the rectangle.</span></span>  |
| <span data-ttu-id="1b539-1188">Ultimo</span><span class="sxs-lookup"><span data-stu-id="1b539-1188">Bottom</span></span>     | <span data-ttu-id="1b539-1189">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-1189">[Double](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="1b539-1190">Coordinata più in basso del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="1b539-1190">Bottommost coordinate of the rectangle.</span></span> |



 

<span data-ttu-id="1b539-1191">**IVgFixedRectangleArray**</span><span class="sxs-lookup"><span data-stu-id="1b539-1191">**IVgFixedRectangleArray**</span></span>

<span data-ttu-id="1b539-1192">Matrice di rettangoli fissi.</span><span class="sxs-lookup"><span data-stu-id="1b539-1192">Array of fixed rectangles.</span></span>



| <span data-ttu-id="1b539-1193">Attributo</span><span class="sxs-lookup"><span data-stu-id="1b539-1193">Attribute</span></span> | <span data-ttu-id="1b539-1194">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b539-1194">Description</span></span>                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b539-1195">Valore</span><span class="sxs-lookup"><span data-stu-id="1b539-1195">Value</span></span>      | <span data-ttu-id="1b539-1196">[Stringa](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-1196">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="1b539-1197">Rappresentazione testuale della matrice.</span><span class="sxs-lookup"><span data-stu-id="1b539-1197">Text representation of array.</span></span>                           |
| <span data-ttu-id="1b539-1198">Length</span><span class="sxs-lookup"><span data-stu-id="1b539-1198">Length</span></span>     | <span data-ttu-id="1b539-1199">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-1199">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="1b539-1200">Numero di rettangoli in questa matrice.</span><span class="sxs-lookup"><span data-stu-id="1b539-1200">Number of rectangles in this array.</span></span>                    |
| <span data-ttu-id="1b539-1201">Elemento</span><span class="sxs-lookup"><span data-stu-id="1b539-1201">Item</span></span>       | <span data-ttu-id="1b539-1202">[Oggetto IVgFixedRectangle.](#data-types-used-in-the-vml-object-model)</span><span class="sxs-lookup"><span data-stu-id="1b539-1202">[IVgFixedRectangle](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="1b539-1203">Oggetto rettangolo in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="1b539-1203">The rectangle object at the specified index.</span></span> |



 

<span data-ttu-id="1b539-1204">**Tipo di dati IVgFormula**</span><span class="sxs-lookup"><span data-stu-id="1b539-1204">**IVgFormula** data type</span></span>

<span data-ttu-id="1b539-1205">Definizioni per formule che possono variare il percorso di una forma o essere usate per altri scopi di calcolo.</span><span class="sxs-lookup"><span data-stu-id="1b539-1205">Definitions for formulas that can vary the path of a shape or be used for other calculation purposes.</span></span> <span data-ttu-id="1b539-1206">Le formule possono essere basate **sull'attributo Adj** di una forma, che può cambiare.</span><span class="sxs-lookup"><span data-stu-id="1b539-1206">Formulas can be based on the **Adj** attribute of a shape, which can change.</span></span> <span data-ttu-id="1b539-1207">Le formule possono fare riferimento anche ad altre formule.</span><span class="sxs-lookup"><span data-stu-id="1b539-1207">Formulas can reference other formulas as well.</span></span>



| <span data-ttu-id="1b539-1208">Attributo</span><span class="sxs-lookup"><span data-stu-id="1b539-1208">Attribute</span></span>| <span data-ttu-id="1b539-1209">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b539-1209">Description</span></span>                                           |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b539-1210">Eqn</span><span class="sxs-lookup"><span data-stu-id="1b539-1210">Eqn</span></span>        | <span data-ttu-id="1b539-1211">[IVgEquation](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-1211">[IVgEquation](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="1b539-1212">Ogni formula definisce un singolo valore come risultato della valutazione dell'espressione.</span><span class="sxs-lookup"><span data-stu-id="1b539-1212">Each formula defines a single value as the result of the evaluation of the expression.</span></span> <span data-ttu-id="1b539-1213">L'espressione è definita da questo attributo e ha la forma generale di un'operazione seguita da un massimo di tre argomenti, che possono essere valori di rettifica (ad esempio, 2), i risultati di formule precedenti (ad esempio, ), numeri fissi o valori \# @2 predefiniti.</span><span class="sxs-lookup"><span data-stu-id="1b539-1213">The expression is defined by this attribute and has the general form of an operation followed by up to three arguments, which may be adjustment values (e.g., \#2), the results of earlier formulas (e.g., @2), fixed numbers, or predefined values.</span></span> |



 

<span data-ttu-id="1b539-1214">**Tipo di dati IVgFormulas**</span><span class="sxs-lookup"><span data-stu-id="1b539-1214">**IVgFormulas data type**</span></span>

<span data-ttu-id="1b539-1215">Raccolta di oggetti formula.</span><span class="sxs-lookup"><span data-stu-id="1b539-1215">A collection of formula objects.</span></span>



| <span data-ttu-id="1b539-1216">Attributo</span><span class="sxs-lookup"><span data-stu-id="1b539-1216">Attribute</span></span> | <span data-ttu-id="1b539-1217">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b539-1217">Description</span></span>                                                                                                                                  |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b539-1218">Length</span><span class="sxs-lookup"><span data-stu-id="1b539-1218">Length</span></span>     | <span data-ttu-id="1b539-1219">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-1219">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="1b539-1220">Numero di oggetti formula nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="1b539-1220">Number of formula objects in collection.</span></span>                                                |
| <span data-ttu-id="1b539-1221">Elemento</span><span class="sxs-lookup"><span data-stu-id="1b539-1221">Item</span></span>       | <span data-ttu-id="1b539-1222">[IVgFormula](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-1222">[IVgFormula](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="1b539-1223">Formula specifica.</span><span class="sxs-lookup"><span data-stu-id="1b539-1223">A specific formula.</span></span> <span data-ttu-id="1b539-1224">Si noti che la matrice della formula può essere ereditata in base al tipo di forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-1224">Note that the formula array may be inherited fom the shape type.</span></span> |



 

<span data-ttu-id="1b539-1225">**Oggetto IVgGradientColorArray**</span><span class="sxs-lookup"><span data-stu-id="1b539-1225">**IVgGradientColorArray**</span></span>

<span data-ttu-id="1b539-1226">Matrice di colori che definiscono una sfumatura (intervallo di colori misto).</span><span class="sxs-lookup"><span data-stu-id="1b539-1226">An array of colors that define a gradient (blended range of colors).</span></span>



| <span data-ttu-id="1b539-1227">Attributo</span><span class="sxs-lookup"><span data-stu-id="1b539-1227">Attribute</span></span> | <span data-ttu-id="1b539-1228">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b539-1228">Description</span></span>                                                                                                                  |
|------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b539-1229">Valore</span><span class="sxs-lookup"><span data-stu-id="1b539-1229">Value</span></span>      | <span data-ttu-id="1b539-1230">[Stringa](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-1230">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="1b539-1231">Specifica la matrice di colori. ad esempio "red .2; verde .4; black .7"</span><span class="sxs-lookup"><span data-stu-id="1b539-1231">Specifies the array of colors; for example, "red .2; green .4; black .7"</span></span> |
| <span data-ttu-id="1b539-1232">Length</span><span class="sxs-lookup"><span data-stu-id="1b539-1232">Length</span></span>     | <span data-ttu-id="1b539-1233">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-1233">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="1b539-1234">Numero di colori nella matrice.</span><span class="sxs-lookup"><span data-stu-id="1b539-1234">Number of colors in the array.</span></span>                                          |



 



| <span data-ttu-id="1b539-1235">Metodo</span><span class="sxs-lookup"><span data-stu-id="1b539-1235">Method</span></span>     | <span data-ttu-id="1b539-1236">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b539-1236">Description</span></span>                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b539-1237">AddColor</span><span class="sxs-lookup"><span data-stu-id="1b539-1237">AddColor</span></span>    | <span data-ttu-id="1b539-1238">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-1238">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="1b539-1239">Aggiunge un nuovo colore all'endpoint specificato da fraction.</span><span class="sxs-lookup"><span data-stu-id="1b539-1239">Adds new color at endpoint specified by fraction.</span></span> <span data-ttu-id="1b539-1240">Il nuovo colore è bianco per impostazione predefinita e è il valore restituito.</span><span class="sxs-lookup"><span data-stu-id="1b539-1240">The new color is white by default and is the return value.</span></span> <span data-ttu-id="1b539-1241">Il colore può quindi essere modificato per riferimento.</span><span class="sxs-lookup"><span data-stu-id="1b539-1241">The color can then be changed by reference.</span></span> |
| <span data-ttu-id="1b539-1242">RemoveColor</span><span class="sxs-lookup"><span data-stu-id="1b539-1242">RemoveColor</span></span> | <span data-ttu-id="1b539-1243">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-1243">[VgFraction](msdn-online-vml-vgfraction-data-type.md).</span></span> <span data-ttu-id="1b539-1244">Rimuove un colore in corrispondenza dell'endpoint specificato da fraction.</span><span class="sxs-lookup"><span data-stu-id="1b539-1244">Removes a color at endpoint specified by fraction.</span></span> <span data-ttu-id="1b539-1245">Nota: se 0.0 o 1.0 non esiste, viene implicito e a questo punto viene usato il colore bianco.</span><span class="sxs-lookup"><span data-stu-id="1b539-1245">Note: if 0.0 or 1.0 does not exist, it is implied and the color white is used at that point.</span></span>          |



 

<span data-ttu-id="1b539-1246">**Tipo di dati IVgPoints**</span><span class="sxs-lookup"><span data-stu-id="1b539-1246">**IVgPoints datatype**</span></span>

<span data-ttu-id="1b539-1247">Matrice di punti che definiscono una forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-1247">Array of points that define a shape.</span></span>



| <span data-ttu-id="1b539-1248">Attributo</span><span class="sxs-lookup"><span data-stu-id="1b539-1248">Attribute</span></span> | <span data-ttu-id="1b539-1249">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b539-1249">Description</span></span>                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b539-1250">Valore</span><span class="sxs-lookup"><span data-stu-id="1b539-1250">Value</span></span>      | <span data-ttu-id="1b539-1251">[Stringa](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-1251">[String](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="1b539-1252">Rappresentazione testuale della matrice.</span><span class="sxs-lookup"><span data-stu-id="1b539-1252">Text representation of array.</span></span>           |
| <span data-ttu-id="1b539-1253">Length</span><span class="sxs-lookup"><span data-stu-id="1b539-1253">Length</span></span>     | <span data-ttu-id="1b539-1254">[Integer](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-1254">[Integer](#data-types-used-in-the-vml-object-model).</span></span> <span data-ttu-id="1b539-1255">Numero di punti in questa matrice.</span><span class="sxs-lookup"><span data-stu-id="1b539-1255">Number of points in this array.</span></span>        |
| <span data-ttu-id="1b539-1256">Elemento</span><span class="sxs-lookup"><span data-stu-id="1b539-1256">Item</span></span>       | <span data-ttu-id="1b539-1257">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="1b539-1257">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span> <span data-ttu-id="1b539-1258">Punto in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="1b539-1258">The point at the specified index.</span></span> |



 

<span data-ttu-id="1b539-1259">**Tipo di dati IVgSkewMatrix**</span><span class="sxs-lookup"><span data-stu-id="1b539-1259">**IVgSkewMatrix datatype**</span></span>

<span data-ttu-id="1b539-1260">Matrice usata per forme a inclinazione, matrice di trasformazione prospettica nel formato "*sxx,sxy,syx,syy,px,py* " \[ *s* =scale, *p* =perspective \] .</span><span class="sxs-lookup"><span data-stu-id="1b539-1260">A matrix used for skewing shapes, a perspective transform matrix in the form, "*sxx,sxy,syx,syy,px,py* " \[*s* =scale, *p* =perspective\].</span></span> <span data-ttu-id="1b539-1261">Se offset è in unità assolute, *px,py* sono in unità emu ^-1; in caso contrario, sono una frazione inversa delle dimensioni della forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-1261">If offset is in absolute units, then *px,py* are in emu ^-1 units; otherwise they are an inverse fraction of shape size.</span></span>



| <span data-ttu-id="1b539-1262">Attributo</span><span class="sxs-lookup"><span data-stu-id="1b539-1262">Attribute</span></span>   | <span data-ttu-id="1b539-1263">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b539-1263">Description</span></span>                                         |
|--------------|-----------------------------------------------------|
| <span data-ttu-id="1b539-1264">XtoX</span><span class="sxs-lookup"><span data-stu-id="1b539-1264">XtoX</span></span>         | <span data-ttu-id="1b539-1265">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-1265">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="1b539-1266">YtoX</span><span class="sxs-lookup"><span data-stu-id="1b539-1266">YtoX</span></span>         | <span data-ttu-id="1b539-1267">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-1267">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="1b539-1268">Xtoy</span><span class="sxs-lookup"><span data-stu-id="1b539-1268">XtoY</span></span>         | <span data-ttu-id="1b539-1269">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-1269">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="1b539-1270">AAA</span><span class="sxs-lookup"><span data-stu-id="1b539-1270">YtoY</span></span>         | <span data-ttu-id="1b539-1271">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-1271">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="1b539-1272">PerspectiveX</span><span class="sxs-lookup"><span data-stu-id="1b539-1272">PerspectiveX</span></span> | <span data-ttu-id="1b539-1273">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-1273">[Double](#data-types-used-in-the-vml-object-model).</span></span> |
| <span data-ttu-id="1b539-1274">PerspectiveY</span><span class="sxs-lookup"><span data-stu-id="1b539-1274">PerspectiveY</span></span> | <span data-ttu-id="1b539-1275">[Double](#data-types-used-in-the-vml-object-model).</span><span class="sxs-lookup"><span data-stu-id="1b539-1275">[Double](#data-types-used-in-the-vml-object-model).</span></span> |



 

<span data-ttu-id="1b539-1276">**IVgSkewOffset**</span><span class="sxs-lookup"><span data-stu-id="1b539-1276">**IVgSkewOffset**</span></span>

<span data-ttu-id="1b539-1277">Specifica l'offset dell'a inclinazione.</span><span class="sxs-lookup"><span data-stu-id="1b539-1277">Specifies the offset of the skew.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1b539-1278">Attributi</span><span class="sxs-lookup"><span data-stu-id="1b539-1278">Attributes</span></span></th>
<th><span data-ttu-id="1b539-1279">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b539-1279">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b539-1280">Valore</span><span class="sxs-lookup"><span data-stu-id="1b539-1280">Value</span></span></td>
<td><span data-ttu-id="1b539-1281"><a href="#data-types-used-in-the-vml-object-model">Stringa</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-1281"><a href="#data-types-used-in-the-vml-object-model">String</a>.</span></span> <span data-ttu-id="1b539-1282">Rappresentazione testuale dell'offset.</span><span class="sxs-lookup"><span data-stu-id="1b539-1282">Text representation of offset.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-1283">X</span><span class="sxs-lookup"><span data-stu-id="1b539-1283">X</span></span></td>
<td><span data-ttu-id="1b539-1284"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-1284"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="1b539-1285">Componente X.</span><span class="sxs-lookup"><span data-stu-id="1b539-1285">X component.</span></span> <span data-ttu-id="1b539-1286">Percentuale o misura.</span><span class="sxs-lookup"><span data-stu-id="1b539-1286">Percentage or measure.</span></span> <span data-ttu-id="1b539-1287">Se non sono presenti unità, il tipo ShapeRelative è implicito. in caso contrario, il tipo assoluto è implicito.</span><span class="sxs-lookup"><span data-stu-id="1b539-1287">If no units, then ShapeRelative type is implied; otherwise Absolute type is implied.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-1288">S</span><span class="sxs-lookup"><span data-stu-id="1b539-1288">Y</span></span></td>
<td><span data-ttu-id="1b539-1289"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-1289"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="1b539-1290">Componente Y.</span><span class="sxs-lookup"><span data-stu-id="1b539-1290">Y component.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-1291">Tipo</span><span class="sxs-lookup"><span data-stu-id="1b539-1291">Type</span></span></td>
<td><span data-ttu-id="1b539-1292"><strong>VgSkewTransformType</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b539-1292"><strong>VgSkewTransformType</strong>.</span></span> <span data-ttu-id="1b539-1293">Specifica il tipo di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="1b539-1293">Specifies the type of transformation.</span></span> <span data-ttu-id="1b539-1294">I valori validi sono punti interi compresi tra -infinity e infinity.</span><span class="sxs-lookup"><span data-stu-id="1b539-1294">Valid values are integer points ranging between -infinity and infinity.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1b539-1295">Tipo</span><span class="sxs-lookup"><span data-stu-id="1b539-1295">Type</span></span></th>
<th><span data-ttu-id="1b539-1296">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b539-1296">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b539-1297">ShapeRelative</span><span class="sxs-lookup"><span data-stu-id="1b539-1297">ShapeRelative</span></span></td>
<td><span data-ttu-id="1b539-1298">I valori dell'offset sono percentuali (rapporti) delle dimensioni della forma originale. Ad esempio, un valore pari a 0,5 indica un offset della metà delle dimensioni della forma.</span><span class="sxs-lookup"><span data-stu-id="1b539-1298">The values of the offset are percentages (ratios) of the original shape's size; e.g., a value of 0.5 means an offset half the size of the shape.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-1299">Assoluto</span><span class="sxs-lookup"><span data-stu-id="1b539-1299">Absolute</span></span></td>
<td><span data-ttu-id="1b539-1300">I valori sono unità assolute.</span><span class="sxs-lookup"><span data-stu-id="1b539-1300">The values are absolute units.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1b539-1301">**Tipo di dati IVgVector2D**</span><span class="sxs-lookup"><span data-stu-id="1b539-1301">**IVgVector2D data type**</span></span>

<span data-ttu-id="1b539-1302">Specifica un vettore bidimensionale costituito da due **numeri Double.**</span><span class="sxs-lookup"><span data-stu-id="1b539-1302">Specifies a two-dimensional vector consisting of two **Double** numbers.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1b539-1303">Attributi</span><span class="sxs-lookup"><span data-stu-id="1b539-1303">Attributes</span></span></th>
<th><span data-ttu-id="1b539-1304">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b539-1304">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b539-1305">Valore</span><span class="sxs-lookup"><span data-stu-id="1b539-1305">Value</span></span></td>
<td><span data-ttu-id="1b539-1306"><strong>Stringa</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b539-1306"><strong>String</strong>.</span></span> <span data-ttu-id="1b539-1307">Rappresentazione testuale di entrambi i numeri di vettore separati da uno spazio.</span><span class="sxs-lookup"><span data-stu-id="1b539-1307">Text representation of both vector numbers separated by a space.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-1308">X</span><span class="sxs-lookup"><span data-stu-id="1b539-1308">X</span></span></td>
<td><span data-ttu-id="1b539-1309"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-1309"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="1b539-1310">Componente X di questo vettore.</span><span class="sxs-lookup"><span data-stu-id="1b539-1310">X component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-1311">S</span><span class="sxs-lookup"><span data-stu-id="1b539-1311">Y</span></span></td>
<td><span data-ttu-id="1b539-1312"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-1312"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="1b539-1313">Componente Y di questo vettore.</span><span class="sxs-lookup"><span data-stu-id="1b539-1313">Y component of this vector.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-1314">Tipo</span><span class="sxs-lookup"><span data-stu-id="1b539-1314">Type</span></span></td>
<td><span data-ttu-id="1b539-1315"><strong>VgVectorType</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b539-1315"><strong>VgVectorType</strong>.</span></span> <span data-ttu-id="1b539-1316">Unità previste per questo vettore.</span><span class="sxs-lookup"><span data-stu-id="1b539-1316">Expected units for this vector.</span></span> <span data-ttu-id="1b539-1317">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="1b539-1317">Values are:</span></span>
<ul>
<li><span data-ttu-id="1b539-1318">Misura</span><span class="sxs-lookup"><span data-stu-id="1b539-1318">Measure</span></span></li>
<li><span data-ttu-id="1b539-1319">Length</span><span class="sxs-lookup"><span data-stu-id="1b539-1319">Length</span></span></li>
<li><span data-ttu-id="1b539-1320">AngleInDegrees</span><span class="sxs-lookup"><span data-stu-id="1b539-1320">AngleInDegrees</span></span></li>
<li><span data-ttu-id="1b539-1321">Fraction</span><span class="sxs-lookup"><span data-stu-id="1b539-1321">Fraction</span></span></li>
<li><span data-ttu-id="1b539-1322">Number Percentage Integer</span><span class="sxs-lookup"><span data-stu-id="1b539-1322">Number Percentage Integer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1b539-1323">**Tipo di dati IVgVector3D**</span><span class="sxs-lookup"><span data-stu-id="1b539-1323">**IVgVector3D data type**</span></span>

<span data-ttu-id="1b539-1324">Specifica un vettore tridimensionale costituito da tre **numeri Double.**</span><span class="sxs-lookup"><span data-stu-id="1b539-1324">Specifies a three-dimensional vector consisting of three **Double** numbers.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b539-1325">Valore</span><span class="sxs-lookup"><span data-stu-id="1b539-1325">Value</span></span></td>
<td><span data-ttu-id="1b539-1326"><strong>Stringa</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b539-1326"><strong>String</strong>.</span></span> <span data-ttu-id="1b539-1327">Rappresentazione testuale di tre numeri vettoriali separati da uno spazio.</span><span class="sxs-lookup"><span data-stu-id="1b539-1327">Text representation of three vector numbers separated by a space.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-1328">X</span><span class="sxs-lookup"><span data-stu-id="1b539-1328">X</span></span></td>
<td><span data-ttu-id="1b539-1329"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-1329"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="1b539-1330">Componente X di questo vettore.</span><span class="sxs-lookup"><span data-stu-id="1b539-1330">X component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-1331">S</span><span class="sxs-lookup"><span data-stu-id="1b539-1331">Y</span></span></td>
<td><span data-ttu-id="1b539-1332"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-1332"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="1b539-1333">Componente Y di questo vettore.</span><span class="sxs-lookup"><span data-stu-id="1b539-1333">Y component of this vector.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b539-1334">Z</span><span class="sxs-lookup"><span data-stu-id="1b539-1334">Z</span></span></td>
<td><span data-ttu-id="1b539-1335"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span><span class="sxs-lookup"><span data-stu-id="1b539-1335"><a href="#data-types-used-in-the-vml-object-model">Double</a>.</span></span> <span data-ttu-id="1b539-1336">Componente Z di questo vettore.</span><span class="sxs-lookup"><span data-stu-id="1b539-1336">Z component of this vector.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b539-1337">Tipo</span><span class="sxs-lookup"><span data-stu-id="1b539-1337">Type</span></span></td>
<td><span data-ttu-id="1b539-1338"><strong>VgVectorType</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b539-1338"><strong>VgVectorType</strong>.</span></span> <span data-ttu-id="1b539-1339">Unità previste per questo vettore.</span><span class="sxs-lookup"><span data-stu-id="1b539-1339">Expected units for this vector.</span></span> <span data-ttu-id="1b539-1340">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="1b539-1340">Values are:</span></span>
<ul>
<li><span data-ttu-id="1b539-1341">Misura</span><span class="sxs-lookup"><span data-stu-id="1b539-1341">Measure</span></span></li>
<li><span data-ttu-id="1b539-1342">Length</span><span class="sxs-lookup"><span data-stu-id="1b539-1342">Length</span></span></li>
<li><span data-ttu-id="1b539-1343">AngleInDegrees</span><span class="sxs-lookup"><span data-stu-id="1b539-1343">AngleInDegrees</span></span></li>
<li><span data-ttu-id="1b539-1344">Fraction</span><span class="sxs-lookup"><span data-stu-id="1b539-1344">Fraction</span></span></li>
<li><span data-ttu-id="1b539-1345">Numero</span><span class="sxs-lookup"><span data-stu-id="1b539-1345">Number</span></span></li>
<li><span data-ttu-id="1b539-1346">Percentuale</span><span class="sxs-lookup"><span data-stu-id="1b539-1346">Percentage</span></span></li>
<li><span data-ttu-id="1b539-1347">Intero</span><span class="sxs-lookup"><span data-stu-id="1b539-1347">Integer</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="1b539-1348">**Tipo di dati Length**</span><span class="sxs-lookup"><span data-stu-id="1b539-1348">**Length data type**</span></span>

<span data-ttu-id="1b539-1349">Numero a virgola mobile con un intervallo compreso tra 0 e infinito.</span><span class="sxs-lookup"><span data-stu-id="1b539-1349">A floating point number with a range from 0 to infinity.</span></span>

<span data-ttu-id="1b539-1350">**Tipo di dati measure**</span><span class="sxs-lookup"><span data-stu-id="1b539-1350">**Measure data type**</span></span>

<span data-ttu-id="1b539-1351">Numero a virgola mobile da -infinity a infinito.</span><span class="sxs-lookup"><span data-stu-id="1b539-1351">A floating point number from -infinity to infinity.</span></span>

<span data-ttu-id="1b539-1352">**Tipo di dati String**</span><span class="sxs-lookup"><span data-stu-id="1b539-1352">**String data type**</span></span>

<span data-ttu-id="1b539-1353">Dati di tipo carattere di qualsiasi lunghezza.</span><span class="sxs-lookup"><span data-stu-id="1b539-1353">Character data of any length.</span></span>

<span data-ttu-id="1b539-1354">**VgBlackWhiteMode**</span><span class="sxs-lookup"><span data-stu-id="1b539-1354">**VgBlackWhiteMode**</span></span>

<span data-ttu-id="1b539-1355">Modalità di rendering per il bianco e nero.</span><span class="sxs-lookup"><span data-stu-id="1b539-1355">Rendering mode for black and white.</span></span> <span data-ttu-id="1b539-1356">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="1b539-1356">Possible values are:</span></span>

-   <span data-ttu-id="1b539-1357">**Colore**</span><span class="sxs-lookup"><span data-stu-id="1b539-1357">**Color**</span></span>
-   <span data-ttu-id="1b539-1358">**Auto**</span><span class="sxs-lookup"><span data-stu-id="1b539-1358">**Auto**</span></span>
-   <span data-ttu-id="1b539-1359">**Grigi**</span><span class="sxs-lookup"><span data-stu-id="1b539-1359">**GrayScale**</span></span>
-   <span data-ttu-id="1b539-1360">**LightGrayScale**</span><span class="sxs-lookup"><span data-stu-id="1b539-1360">**LightGrayScale**</span></span>
-   <span data-ttu-id="1b539-1361">**InverseGray**</span><span class="sxs-lookup"><span data-stu-id="1b539-1361">**InverseGray**</span></span>
-   <span data-ttu-id="1b539-1362">**GrayOutline**</span><span class="sxs-lookup"><span data-stu-id="1b539-1362">**GrayOutline**</span></span>
-   <span data-ttu-id="1b539-1363">**BlackTextAndLines**</span><span class="sxs-lookup"><span data-stu-id="1b539-1363">**BlackTextAndLines**</span></span>
-   <span data-ttu-id="1b539-1364">**HighContrast**</span><span class="sxs-lookup"><span data-stu-id="1b539-1364">**HighContrast**</span></span>
-   <span data-ttu-id="1b539-1365">**Nero**</span><span class="sxs-lookup"><span data-stu-id="1b539-1365">**Black**</span></span>
-   <span data-ttu-id="1b539-1366">**White**</span><span class="sxs-lookup"><span data-stu-id="1b539-1366">**White**</span></span>
-   <span data-ttu-id="1b539-1367">**Non ridisegnato**</span><span class="sxs-lookup"><span data-stu-id="1b539-1367">**Undrawn**</span></span>

<span data-ttu-id="1b539-1368">**Tipo di dati VgFraction**</span><span class="sxs-lookup"><span data-stu-id="1b539-1368">**VgFraction data type**</span></span>

<span data-ttu-id="1b539-1369">Numero a virgola mobile con intervallo compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="1b539-1369">Floating point number with range from 0.0 to 1.0.</span></span> <span data-ttu-id="1b539-1370">Le frazioni possono anche essere specificate come percentuale. ad esempio "50%".</span><span class="sxs-lookup"><span data-stu-id="1b539-1370">Fractions can also be specified as a percentage; e.g., "50%".</span></span>

<span data-ttu-id="1b539-1371">**Tipo di dati VgTriState**</span><span class="sxs-lookup"><span data-stu-id="1b539-1371">**VgTriState datatype**</span></span>

<span data-ttu-id="1b539-1372">Enumerazione utilizzata per i valori che possono essere uno dei tre stati seguenti:</span><span class="sxs-lookup"><span data-stu-id="1b539-1372">Enumeration used for values that can be one of three states:</span></span>

-   <span data-ttu-id="1b539-1373">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="1b539-1373">**TRUE**</span></span>
-   <span data-ttu-id="1b539-1374">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="1b539-1374">**FALSE**</span></span>
-   <span data-ttu-id="1b539-1375">**MIXED**</span><span class="sxs-lookup"><span data-stu-id="1b539-1375">**MIXED**</span></span>
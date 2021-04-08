---
title: Attributo Type (Shape) (la)
description: Attributo Type (Shape) (la)
ms.assetid: 41f0d1d3-3a2c-47cf-b2ec-d983b14aea87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e53b275d6b6327b3d3783704dbd06156e643f6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046902"
---
# <a name="type-attribute-shapevml"></a><span data-ttu-id="fbe87-103">Attributo Type (Shape) (la)</span><span class="sxs-lookup"><span data-stu-id="fbe87-103">Type Attribute (Shape)(VML)</span></span>

<span data-ttu-id="fbe87-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="fbe87-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="fbe87-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="fbe87-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="fbe87-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="fbe87-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="fbe87-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="fbe87-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="fbe87-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="fbe87-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="fbe87-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="fbe87-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="fbe87-110">Definisce un riferimento all'ID di un elemento [TipoForma](msdn-online-vml-shapetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="fbe87-110">Defines a reference to the ID of a [ShapeType](msdn-online-vml-shapetype-element.md) element.</span></span> <span data-ttu-id="fbe87-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="fbe87-111">Read/write.</span></span> <span data-ttu-id="fbe87-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="fbe87-112">**String**.</span></span>

<span data-ttu-id="fbe87-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="fbe87-113">**Applies To**</span></span>

[<span data-ttu-id="fbe87-114">Con forme</span><span class="sxs-lookup"><span data-stu-id="fbe87-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="fbe87-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="fbe87-115">**Tag Syntax**</span></span>

``` syntax
<v:
          element 
          type=" expression ">
```

<span data-ttu-id="fbe87-116">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="fbe87-116">**Script Syntax**</span></span>

``` syntax
element 
          .type="#expression"
```

``` syntax
expression=element .type
```

<span data-ttu-id="fbe87-117">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="fbe87-117">**Remarks**</span></span>

<span data-ttu-id="fbe87-118">Se l'attributo **Type** fa riferimento all'ID di un elemento **TipoForma** , i riempimenti, i percorsi e i tratti di **TipoForma** vengono usati come modelli per creare la forma.</span><span class="sxs-lookup"><span data-stu-id="fbe87-118">If the **Type** attribute references the ID of a **ShapeType** element, the fills, paths, and strokes of the **ShapeType** are used as templates to create the shape.</span></span> <span data-ttu-id="fbe87-119">I valori derivati da **TipoForma** possono essere sottoposti a override dai singoli valori della forma.</span><span class="sxs-lookup"><span data-stu-id="fbe87-119">Values derived from **ShapeType** can be overridden by individual shape values.</span></span>

<span data-ttu-id="fbe87-120">Se usato nei tag, il valore della stringa deve iniziare con un simbolo di cancelletto ( \# ).</span><span class="sxs-lookup"><span data-stu-id="fbe87-120">If used in tags, the string value must begin with a number sign (\#) symbol.</span></span>

<span data-ttu-id="fbe87-121">**Attributo standard la**</span><span class="sxs-lookup"><span data-stu-id="fbe87-121">**VML Standard Attribute**</span></span>

<span data-ttu-id="fbe87-122">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="fbe87-122">**Example**</span></span>

<span data-ttu-id="fbe87-123">Una forma **TipoForma** viene creata con "MyType" come ID.</span><span class="sxs-lookup"><span data-stu-id="fbe87-123">A **ShapeType** shape is created with the "mytype" as an ID.</span></span>


```HTML
   <v:shapetype id="mytype"
   fillcolor="red" strokecolor="blue"
   coordorigin="0 0" coordsize="200 200">
   <v:path v="m 0,0 l 0,200, 200,200, 200,0 x e"/>
   </v:shapetype>
```



<span data-ttu-id="fbe87-124">Se quindi si crea una forma usando i valori **TipoForma** , la forma avrà gli attributi di "MyType" **TipoForma**; ovvero "shape01" avrà un riempimento rosso con un tratto blu.</span><span class="sxs-lookup"><span data-stu-id="fbe87-124">Then if you create a shape using the **ShapeType** values, the shape will have the attributes of the "mytype" **ShapeType**; that is, "shape01" will have a red fill with a blue stroke.</span></span>


```HTML
   <v:shape id="shape01" type="#mytype"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



<span data-ttu-id="fbe87-125">È possibile eseguire l'override dei valori ereditati, ad esempio, modificando il colore in verde.</span><span class="sxs-lookup"><span data-stu-id="fbe87-125">You can override the inherited values, for example, by changing the color to green.</span></span>


```HTML
   <v:shape id="shape02" type="#mytype"
   fillcolor="green"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:shape>
```



<span data-ttu-id="fbe87-126">[Esempio di attributo Type](/previous-versions/bb264099(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fbe87-126">[Type Attribute Example](/previous-versions/bb264099(v=vs.85)).</span></span> <span data-ttu-id="fbe87-127">(Richiede Microsoft Internet Explorer 5 o versione successiva).</span><span class="sxs-lookup"><span data-stu-id="fbe87-127">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 
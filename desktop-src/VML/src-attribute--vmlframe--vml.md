---
title: Attributo src (VMLFrame) (la)
description: Attributo src (VMLFrame) (la)
ms.assetid: 6ac7a3b5-3c1d-43a0-ab92-a03e3bd45733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a9c3ec4849098c9469fba56f26d4c3dd514746
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337951"
---
# <a name="src-attribute-vmlframevml"></a><span data-ttu-id="1174c-103">Attributo src (VMLFrame) (la)</span><span class="sxs-lookup"><span data-stu-id="1174c-103">Src Attribute (VMLFrame)(VML)</span></span>

<span data-ttu-id="1174c-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="1174c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1174c-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="1174c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1174c-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="1174c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1174c-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="1174c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1174c-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1174c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1174c-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1174c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1174c-110">Definisce l'origine dei dati per il frame.</span><span class="sxs-lookup"><span data-stu-id="1174c-110">Defines the source of data for the frame.</span></span> <span data-ttu-id="1174c-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="1174c-111">Read/write.</span></span> <span data-ttu-id="1174c-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="1174c-112">**String**.</span></span>

<span data-ttu-id="1174c-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="1174c-113">**Applies To**</span></span>

[<span data-ttu-id="1174c-114">VMLFrame</span><span class="sxs-lookup"><span data-stu-id="1174c-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="1174c-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="1174c-115">**Tag Syntax**</span></span>

<span data-ttu-id="1174c-116"><v: *element* src = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="1174c-116"><v: *element* src=" *expression* "></span></span>

<span data-ttu-id="1174c-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="1174c-117">**Script Syntax**</span></span>

<span data-ttu-id="1174c-118">*element* . src = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="1174c-118">*element* .src="*expression*"</span></span>

<span data-ttu-id="1174c-119">*espressione* = *elemento*. src</span><span class="sxs-lookup"><span data-stu-id="1174c-119">*expression*=*element*.src</span></span>

<span data-ttu-id="1174c-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="1174c-120">**Remarks**</span></span>

<span data-ttu-id="1174c-121">L'attributo **src** può includere le seguenti sintassi:</span><span class="sxs-lookup"><span data-stu-id="1174c-121">The **Src** attribute can involve the following syntaxes:</span></span>

-   <span data-ttu-id="1174c-122">URL del file esterno.</span><span class="sxs-lookup"><span data-stu-id="1174c-122">URL to external file.</span></span> <span data-ttu-id="1174c-123">Il file deve essere un file XML con il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="1174c-123">The file must be an XML file with the following format:</span></span>
    ```HTML
       <xml xmlns:v = "urn:schemas-microsoft-com:vml">
       .
       .
       .
       </xml>
    ```

    

-   <span data-ttu-id="1174c-124">All'interno del file è necessario disporre di una o più forme la con ID validi a cui è possibile fare riferimento utilizzando questa sintassi:</span><span class="sxs-lookup"><span data-stu-id="1174c-124">Inside the file you must have one or more VML shapes with valid IDs that can be referenced by using this syntax:</span></span>
    ```HTML
       filename#shapename
    ```

    

-   <span data-ttu-id="1174c-125">Nel seguente riferimento, i file esterni hanno l'estensione. la, ma è possibile usare qualsiasi estensione:</span><span class="sxs-lookup"><span data-stu-id="1174c-125">In the following reference, external files have the .vml extension, but any extension can be used:</span></span>
    ```HTML
       external.vml#image01
    ```

    

-   <span data-ttu-id="1174c-126">È possibile fare riferimento a una forma nello stesso file usando la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="1174c-126">You can reference a shape within the same file by using the following syntax:</span></span>
    ```HTML
       #shapename
    ```

    

<span data-ttu-id="1174c-127">Se il **clip** è **false**, la forma verrà ridimensionata in base al frame.</span><span class="sxs-lookup"><span data-stu-id="1174c-127">If **Clip** is **False**, the shape will scale to fit the frame.</span></span> <span data-ttu-id="1174c-128">Se **true**, tutte le parti della forma che si trovano all'esterno del frame non verranno visualizzate.</span><span class="sxs-lookup"><span data-stu-id="1174c-128">If **True**, any parts of the shape that are outside the frame will not be displayed.</span></span>

<span data-ttu-id="1174c-129">Si noti che l' [origine](origin-attribute--vmlframe--vml.md) e le [dimensioni](size-attribute--vmlframe.md) non verranno utilizzate a meno che la **clip** non sia **true**.</span><span class="sxs-lookup"><span data-stu-id="1174c-129">Note that [Origin](origin-attribute--vmlframe--vml.md) and [Size](size-attribute--vmlframe.md) won't be used unless **Clip** is **True**.</span></span>

<span data-ttu-id="1174c-130">**Attributo standard la**</span><span class="sxs-lookup"><span data-stu-id="1174c-130">**VML Standard Attribute**</span></span>

<span data-ttu-id="1174c-131">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="1174c-131">**Example**</span></span>

<span data-ttu-id="1174c-132">L'immagine definita nel file esterno verrà ritagliata.</span><span class="sxs-lookup"><span data-stu-id="1174c-132">The image defined in the external file will be clipped.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 
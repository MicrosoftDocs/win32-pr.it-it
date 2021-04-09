---
title: Attributo Master la
description: Attributo Master la
ms.assetid: ec661dc6-8e1c-47a3-ad3a-e1ee7e64c840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d6c34fe49c107ed7ee1b4c1fb90d31bb07f17a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118426"
---
# <a name="vml-master-attribute"></a><span data-ttu-id="fee0d-103">Attributo Master la</span><span class="sxs-lookup"><span data-stu-id="fee0d-103">VML Master Attribute</span></span>

<span data-ttu-id="fee0d-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="fee0d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="fee0d-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="fee0d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="fee0d-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="fee0d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="fee0d-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="fee0d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="fee0d-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="fee0d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="fee0d-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="fee0d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="fee0d-110">Determina se un elemento **TipoForma** è un elemento Master.</span><span class="sxs-lookup"><span data-stu-id="fee0d-110">Determines whether a **ShapeType** element is a master element.</span></span> <span data-ttu-id="fee0d-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="fee0d-111">Read/write.</span></span> <span data-ttu-id="fee0d-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="fee0d-112">**VgTriState**.</span></span>

<span data-ttu-id="fee0d-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="fee0d-113">**Applies To**</span></span>

[<span data-ttu-id="fee0d-114">TipoForma</span><span class="sxs-lookup"><span data-stu-id="fee0d-114">ShapeType</span></span>](msdn-online-vml-shapetype-element.md)

<span data-ttu-id="fee0d-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="fee0d-115">**Tag Syntax**</span></span>

<span data-ttu-id="fee0d-116"><v: *element* o:Master = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="fee0d-116"><v: *element* o:master=" *expression* "></span></span>

<span data-ttu-id="fee0d-117">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="fee0d-117">**Remarks**</span></span>

<span data-ttu-id="fee0d-118">Se **true**, la forma **TipoForma** viene sottoposta a rendering dal motore di rendering.</span><span class="sxs-lookup"><span data-stu-id="fee0d-118">If **True**, the **ShapeType** shape is rendered by the rendering engine.</span></span> <span data-ttu-id="fee0d-119">Il valore predefinito è **False**.</span><span class="sxs-lookup"><span data-stu-id="fee0d-119">The default value is **False**.</span></span>

<span data-ttu-id="fee0d-120">*Attributo Microsoft Office Extensions*</span><span class="sxs-lookup"><span data-stu-id="fee0d-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="fee0d-121">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="fee0d-121">**Example**</span></span>

<span data-ttu-id="fee0d-122">L'elemento **TipoForma** è una forma master.</span><span class="sxs-lookup"><span data-stu-id="fee0d-122">The **ShapeType** element is a master shape.</span></span>


```HTML
   <v:shapetype id="laure"
   coordorigin= "0 0" coordsize="200 200"
   fillcolor= "red" o:master="True"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shapetype>
```



 

 
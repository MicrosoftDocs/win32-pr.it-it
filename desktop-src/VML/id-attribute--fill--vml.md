---
title: Attributo ID (Fill) (la)
description: Attributo ID (Fill) (la)
ms.assetid: 56865772-51bd-4729-8e56-6b00e3c6bed0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4820c4f7a23cf940c199f27243d8ad5601390a84
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047018"
---
# <a name="id-attribute-fillvml"></a><span data-ttu-id="803dd-103">Attributo ID (Fill) (la)</span><span class="sxs-lookup"><span data-stu-id="803dd-103">ID Attribute (Fill)(VML)</span></span>

<span data-ttu-id="803dd-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="803dd-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="803dd-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="803dd-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="803dd-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="803dd-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="803dd-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="803dd-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="803dd-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="803dd-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="803dd-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="803dd-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="803dd-110">Nome che fornisce un identificatore univoco per un riempimento.</span><span class="sxs-lookup"><span data-stu-id="803dd-110">A name that provides a unique identifier for a fill.</span></span> <span data-ttu-id="803dd-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="803dd-111">Read/write.</span></span> <span data-ttu-id="803dd-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="803dd-112">**String**.</span></span>

<span data-ttu-id="803dd-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="803dd-113">**Applies To**</span></span>

[<span data-ttu-id="803dd-114">Fill</span><span class="sxs-lookup"><span data-stu-id="803dd-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="803dd-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="803dd-115">**Tag Syntax**</span></span>

<span data-ttu-id="803dd-116"><v: *element* ID = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="803dd-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="803dd-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="803dd-117">**Script Syntax**</span></span>

<span data-ttu-id="803dd-118">*element* . ID = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="803dd-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="803dd-119">*espressione* = *elemento*. ID</span><span class="sxs-lookup"><span data-stu-id="803dd-119">*expression*=*element*.id</span></span>

<span data-ttu-id="803dd-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="803dd-120">**Remarks**</span></span>

<span data-ttu-id="803dd-121">Usare **ID** per fare riferimento a un riempimento specifico.</span><span class="sxs-lookup"><span data-stu-id="803dd-121">Use **ID** to refer to a specific fill.</span></span> <span data-ttu-id="803dd-122">Una volta creato un riempimento e fornito un ID, è possibile utilizzare il nome ID quando si desidera modificare il riempimento.</span><span class="sxs-lookup"><span data-stu-id="803dd-122">Once you have created a fill and given it an ID, you can use the ID name when you want to manipulate the fill.</span></span>

<span data-ttu-id="803dd-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="803dd-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="803dd-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="803dd-124">**Example**</span></span>

<span data-ttu-id="803dd-125">La forma dispone di un ID di riempimento denominato "riempimento".</span><span class="sxs-lookup"><span data-stu-id="803dd-125">The shape has a fill ID called "myfill".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill id="myfill"/>
   </v:shape>
```



 

 
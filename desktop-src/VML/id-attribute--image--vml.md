---
title: Attributo ID (Image) (la)
description: Attributo ID (Image) (la)
ms.assetid: d85a6d56-5896-4ac0-85c7-0edc72928c62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40ac489331699ca6fe040cddc0bebb408d524de7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399682"
---
# <a name="id-attribute-imagevml"></a><span data-ttu-id="17a74-103">Attributo ID (Image) (la)</span><span class="sxs-lookup"><span data-stu-id="17a74-103">ID Attribute (Image)(VML)</span></span>

<span data-ttu-id="17a74-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="17a74-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="17a74-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="17a74-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="17a74-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="17a74-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="17a74-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="17a74-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="17a74-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="17a74-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="17a74-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="17a74-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="17a74-110">Definisce un nome che fornisce un identificatore univoco per un'immagine.</span><span class="sxs-lookup"><span data-stu-id="17a74-110">Defines a name that provides a unique identifier for an image.</span></span> <span data-ttu-id="17a74-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="17a74-111">Read/write.</span></span> <span data-ttu-id="17a74-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="17a74-112">**String**.</span></span>

<span data-ttu-id="17a74-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="17a74-113">**Applies To**</span></span>

[<span data-ttu-id="17a74-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="17a74-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="17a74-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="17a74-115">**Tag Syntax**</span></span>

<span data-ttu-id="17a74-116"><v: *element* ID = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="17a74-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="17a74-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="17a74-117">**Script Syntax**</span></span>

<span data-ttu-id="17a74-118">*element* . ID = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="17a74-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="17a74-119">*espressione* = *elemento*. ID</span><span class="sxs-lookup"><span data-stu-id="17a74-119">*expression*=*element*.id</span></span>

<span data-ttu-id="17a74-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="17a74-120">**Remarks**</span></span>

<span data-ttu-id="17a74-121">Usare **ID** per fare riferimento a un'immagine specifica.</span><span class="sxs-lookup"><span data-stu-id="17a74-121">Use **ID** to refer to a specific image.</span></span> <span data-ttu-id="17a74-122">Dopo aver creato un'immagine e avergli assegnato un ID, è possibile usare il nome ID quando si vuole modificare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="17a74-122">Once you have created an image and given it an ID, you can use the ID name when you want to manipulate the image.</span></span>

<span data-ttu-id="17a74-123">**Attributo standard la**</span><span class="sxs-lookup"><span data-stu-id="17a74-123">**VML Standard Attribute**</span></span>

<span data-ttu-id="17a74-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="17a74-124">**Example**</span></span>

<span data-ttu-id="17a74-125">La forma ha un ID **ImageData** denominato "immagine".</span><span class="sxs-lookup"><span data-stu-id="17a74-125">The shape has an **ImageData** ID called "myimage".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata id="myimage" src="kids.jpg"/>
   </v:shape>
```



 

 
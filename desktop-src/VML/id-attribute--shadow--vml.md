---
title: Attributo ID (Shadow) (la)
description: Attributo ID (Shadow) (la)
ms.assetid: ca20b6b9-a41c-4073-9178-77eb0f918327
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d51a5917f9ef71e3c4acea7ec1ed2e5cf90aef8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728343"
---
# <a name="id-attribute-shadowvml"></a><span data-ttu-id="afd82-103">Attributo ID (Shadow) (la)</span><span class="sxs-lookup"><span data-stu-id="afd82-103">ID Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="afd82-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="afd82-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="afd82-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="afd82-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="afd82-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="afd82-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="afd82-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="afd82-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="afd82-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="afd82-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="afd82-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="afd82-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="afd82-110">Specifica un nome che fornisce un identificatore univoco per un'ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="afd82-110">Specifies a name that provides a unique identifier for a shadow.</span></span> <span data-ttu-id="afd82-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="afd82-111">Read/write.</span></span> <span data-ttu-id="afd82-112">**Stringa**.</span><span class="sxs-lookup"><span data-stu-id="afd82-112">**String**.</span></span>

<span data-ttu-id="afd82-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="afd82-113">**Applies To**</span></span>

[<span data-ttu-id="afd82-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="afd82-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="afd82-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="afd82-115">**Tag Syntax**</span></span>

<span data-ttu-id="afd82-116"><v: *element* ID = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="afd82-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="afd82-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="afd82-117">**Script Syntax**</span></span>

<span data-ttu-id="afd82-118">*element* . ID = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="afd82-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="afd82-119">*espressione* = *elemento*. ID</span><span class="sxs-lookup"><span data-stu-id="afd82-119">*expression*=*element*.id</span></span>

<span data-ttu-id="afd82-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="afd82-120">**Remarks**</span></span>

<span data-ttu-id="afd82-121">Usare **ID** per fare riferimento a un'ombreggiatura specifica.</span><span class="sxs-lookup"><span data-stu-id="afd82-121">Use **ID** to refer to a specific shadow.</span></span> <span data-ttu-id="afd82-122">Dopo aver creato un'ombreggiatura e dato un ID, è possibile usare il nome ID quando si desidera modificare l'ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="afd82-122">Once you have created a shadow and given it an ID, you can use the ID name when you want to manipulate the shadow.</span></span>

<span data-ttu-id="afd82-123">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="afd82-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="afd82-124">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="afd82-124">**Example**</span></span>

<span data-ttu-id="afd82-125">Alla forma è associato un ID ombreggiatura denominato "ombreggiatura".</span><span class="sxs-lookup"><span data-stu-id="afd82-125">The shape has a shadow ID called "myshadow".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow id="myshadow" on="True"/>
   </v:shape>
```



 

 
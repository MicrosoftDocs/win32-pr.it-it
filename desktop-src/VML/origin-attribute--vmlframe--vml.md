---
title: Attributo Origin (VMLFrame) (la)
description: Attributo Origin (VMLFrame) (la)
ms.assetid: 317c027e-5054-4543-ad98-2c21d1cf7154
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9341eecea9ec1eae8aaf1d7b1ad729986a8249
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729991"
---
# <a name="origin-attribute-vmlframevml"></a><span data-ttu-id="d65a6-103">Attributo Origin (VMLFrame) (la)</span><span class="sxs-lookup"><span data-stu-id="d65a6-103">Origin Attribute (VMLFrame)(VML)</span></span>

<span data-ttu-id="d65a6-104">In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d65a6-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d65a6-105">Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.</span><span class="sxs-lookup"><span data-stu-id="d65a6-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d65a6-106">Al 2011 dicembre, questo argomento è stato archiviato.</span><span class="sxs-lookup"><span data-stu-id="d65a6-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d65a6-107">Di conseguenza, non viene più gestita attivamente.</span><span class="sxs-lookup"><span data-stu-id="d65a6-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d65a6-108">Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d65a6-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d65a6-109">Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d65a6-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d65a6-110">Definisce l'origine dell'area di visualizzazione del frame.</span><span class="sxs-lookup"><span data-stu-id="d65a6-110">Defines the origin of the clipping region of the frame.</span></span> <span data-ttu-id="d65a6-111">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d65a6-111">Read/write.</span></span> <span data-ttu-id="d65a6-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="d65a6-112">**VgVector2D**.</span></span>

<span data-ttu-id="d65a6-113">**Si applica a**</span><span class="sxs-lookup"><span data-stu-id="d65a6-113">**Applies To**</span></span>

[<span data-ttu-id="d65a6-114">VMLFrame</span><span class="sxs-lookup"><span data-stu-id="d65a6-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="d65a6-115">**Sintassi Tag**</span><span class="sxs-lookup"><span data-stu-id="d65a6-115">**Tag Syntax**</span></span>

<span data-ttu-id="d65a6-116"><v: *element* Origin = " *Expression* " ></span><span class="sxs-lookup"><span data-stu-id="d65a6-116"><v: *element* origin=" *expression* "></span></span>

<span data-ttu-id="d65a6-117">**Sintassi dello script**</span><span class="sxs-lookup"><span data-stu-id="d65a6-117">**Script Syntax**</span></span>

<span data-ttu-id="d65a6-118">*element* . Origin = "*Expression*"</span><span class="sxs-lookup"><span data-stu-id="d65a6-118">*element* .origin="*expression*"</span></span>

<span data-ttu-id="d65a6-119">*espressione* = *elemento*. Origin</span><span class="sxs-lookup"><span data-stu-id="d65a6-119">*expression*=*element*.origin</span></span>

<span data-ttu-id="d65a6-120">**Osservazioni:**</span><span class="sxs-lookup"><span data-stu-id="d65a6-120">**Remarks**</span></span>

<span data-ttu-id="d65a6-121">Il valore predefinito è 0,0.</span><span class="sxs-lookup"><span data-stu-id="d65a6-121">The default value is 0,0.</span></span> <span data-ttu-id="d65a6-122">Si noti che l' **origine** funziona solo se il [clip](msdn-online-vml-clip-attribute.md) è **true**.</span><span class="sxs-lookup"><span data-stu-id="d65a6-122">Note that **Origin** only works if [Clip](msdn-online-vml-clip-attribute.md) is **True**.</span></span> <span data-ttu-id="d65a6-123">In questo attributo l'origine è definita come angolo superiore sinistro del frame.</span><span class="sxs-lookup"><span data-stu-id="d65a6-123">In this attribute, the origin is defined as the upper left corner of the frame.</span></span>

<span data-ttu-id="d65a6-124">*Attributo standard la*</span><span class="sxs-lookup"><span data-stu-id="d65a6-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="d65a6-125">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="d65a6-125">**Example**</span></span>

<span data-ttu-id="d65a6-126">L'origine dell'area di ridimensionamento è 100PT, 100pt.</span><span class="sxs-lookup"><span data-stu-id="d65a6-126">The origin of the clipping region is 100pt,100pt.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'
   </v:vmlframe>
```



 

 
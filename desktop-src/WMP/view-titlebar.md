---
title: Visualizza. barra del titolo
description: L'attributo barra del titolo recupera un valore che indica se la barra del titolo della finestra è visualizzata.
ms.assetid: 996aa2e0-0313-4a48-adcb-b82f76f38b6a
keywords:
- VIEW. barra del titolo Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.titleBar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea225103913e3906cf6cd3b129943fbf9b9f165
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326710"
---
# <a name="viewtitlebar"></a><span data-ttu-id="e4a68-104">Visualizza. barra del titolo</span><span class="sxs-lookup"><span data-stu-id="e4a68-104">VIEW.titleBar</span></span>

<span data-ttu-id="e4a68-105">L'attributo **barra** del titolo recupera un valore che indica se la barra del titolo della finestra è visualizzata.</span><span class="sxs-lookup"><span data-stu-id="e4a68-105">The **titleBar** attribute retrieves a value indicating whether the window title bar is shown.</span></span>

``` syntax
        elementID.titleBar
```

## <a name="possible-values"></a><span data-ttu-id="e4a68-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="e4a68-106">Possible Values</span></span>

<span data-ttu-id="e4a68-107">Questo attributo è un **valore booleano** di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e4a68-107">This attribute is a read-only **Boolean**.</span></span>



| <span data-ttu-id="e4a68-108">Valore</span><span class="sxs-lookup"><span data-stu-id="e4a68-108">Value</span></span> | <span data-ttu-id="e4a68-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4a68-109">Description</span></span>                             |
|-------|-----------------------------------------|
| <span data-ttu-id="e4a68-110">true</span><span class="sxs-lookup"><span data-stu-id="e4a68-110">true</span></span>  | <span data-ttu-id="e4a68-111">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="e4a68-111">Default.</span></span> <span data-ttu-id="e4a68-112">Viene visualizzata la barra del titolo della finestra.</span><span class="sxs-lookup"><span data-stu-id="e4a68-112">The window title bar is shown.</span></span> |
| <span data-ttu-id="e4a68-113">false</span><span class="sxs-lookup"><span data-stu-id="e4a68-113">false</span></span> | <span data-ttu-id="e4a68-114">La barra del titolo della finestra non viene visualizzata.</span><span class="sxs-lookup"><span data-stu-id="e4a68-114">The window title bar is not shown.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="e4a68-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e4a68-115">Remarks</span></span>

<span data-ttu-id="e4a68-116">Se viene visualizzata la barra del titolo, verranno visualizzati i pulsanti casella di controllo, Riduci a icona e Chiudi.</span><span class="sxs-lookup"><span data-stu-id="e4a68-116">If the title bar is shown, the control box, minimize, and close buttons will be shown.</span></span> <span data-ttu-id="e4a68-117">Il titolo della finestra sarà il titolo dell'elemento di **visualizzazione** .</span><span class="sxs-lookup"><span data-stu-id="e4a68-117">The title of the window will be the title of the **VIEW** element.</span></span>

<span data-ttu-id="e4a68-118">Se la **barra** del titolo è impostata su true e l'utente tenta di modificare il valore di **video. zoom**, la modifica non verrà eseguita a meno che non venga eseguito il monitoraggio dello **Zoom** e si intraprenda un'azione appropriata per il ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="e4a68-118">If **titleBar** is set to true and the user attempts to change the value of **Video.zoom**, the change will not take place unless the skin monitors **zoom** and takes appropriate action to resize itself.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4a68-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4a68-119">Requirements</span></span>



| <span data-ttu-id="e4a68-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4a68-120">Requirement</span></span> | <span data-ttu-id="e4a68-121">Valore</span><span class="sxs-lookup"><span data-stu-id="e4a68-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="e4a68-122">Versione</span><span class="sxs-lookup"><span data-stu-id="e4a68-122">Version</span></span><br/> | <span data-ttu-id="e4a68-123">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="e4a68-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e4a68-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4a68-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4a68-125">**Elemento VIEW**</span><span class="sxs-lookup"><span data-stu-id="e4a68-125">**VIEW Element**</span></span>](view-element.md)
</dt> <dt>

[<span data-ttu-id="e4a68-126">**Visualizza. titolo**</span><span class="sxs-lookup"><span data-stu-id="e4a68-126">**VIEW.title**</span></span>](view-title.md)
</dt> <dt>

[<span data-ttu-id="e4a68-127">**VIDEO. zoom**</span><span class="sxs-lookup"><span data-stu-id="e4a68-127">**VIDEO.zoom**</span></span>](video-zoom.md)
</dt> </dl>

 

 






---
title: AmbientAttributes. tabStop
description: L'attributo tabStop specifica o recupera un valore che indica se il controllo è nell'ordine di tabulazione. Per impostare l'ordine di tabulazione, inserire il controllo nello script generale prima o dopo altri tag di controllo.
ms.assetid: 3d4b7fe4-1032-44e1-bae5-f253d00881bf
keywords:
- Media Player di Windows AmbientAttributes. tabStop
topic_type:
- apiref
api_name:
- AmbientAttributes.tabStop
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4005fc26a2bc5f928cde0f5ed67ec2098cf3e6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332146"
---
# <a name="ambientattributestabstop"></a><span data-ttu-id="d9299-105">AmbientAttributes. tabStop</span><span class="sxs-lookup"><span data-stu-id="d9299-105">AmbientAttributes.tabStop</span></span>

<span data-ttu-id="d9299-106">L'attributo **TabStop** specifica o recupera un valore che indica se il controllo è nell'ordine di tabulazione.</span><span class="sxs-lookup"><span data-stu-id="d9299-106">The **tabStop** attribute specifies or retrieves a value indicating whether the control is in the tabbing order.</span></span> <span data-ttu-id="d9299-107">Per impostare l'ordine di tabulazione, inserire il controllo nello script generale prima o dopo altri tag di controllo.</span><span class="sxs-lookup"><span data-stu-id="d9299-107">You set the tabbing order by placing the control in the overall script before or after other control tags.</span></span>

``` syntax
        elementID.tabStop
```

## <a name="possible-values"></a><span data-ttu-id="d9299-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="d9299-108">Possible Values</span></span>

<span data-ttu-id="d9299-109">Questo attributo è un **valore booleano** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d9299-109">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="d9299-110">Valore</span><span class="sxs-lookup"><span data-stu-id="d9299-110">Value</span></span> | <span data-ttu-id="d9299-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9299-111">Description</span></span>                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9299-112">true</span><span class="sxs-lookup"><span data-stu-id="d9299-112">true</span></span>  | <span data-ttu-id="d9299-113">Il controllo è nell'ordine di tabulazione (il controllo avrà una tabulazione: requisito di accessibilità).</span><span class="sxs-lookup"><span data-stu-id="d9299-113">Control is in the tabbing order (control will have a tab stop: accessibility requirement).</span></span> |
| <span data-ttu-id="d9299-114">false</span><span class="sxs-lookup"><span data-stu-id="d9299-114">false</span></span> | <span data-ttu-id="d9299-115">Il controllo non è nell'ordine di tabulazione.</span><span class="sxs-lookup"><span data-stu-id="d9299-115">Control is not in the tabbing order.</span></span>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="d9299-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="d9299-116">Remarks</span></span>

<span data-ttu-id="d9299-117">L'attributo **TabStop** non è applicabile all'elemento **Effects** .</span><span class="sxs-lookup"><span data-stu-id="d9299-117">The **tabStop** attribute is not applicable to the **EFFECTS** element.</span></span>

<span data-ttu-id="d9299-118">Il valore predefinito di questo attributo è true per tutti gli elementi eccetto **menu** e **testo**, il cui valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="d9299-118">The default value for this attribute is true for all elements except **AUTOMENU** and **TEXT**, which have a default value of false.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9299-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9299-119">Requirements</span></span>



| <span data-ttu-id="d9299-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9299-120">Requirement</span></span> | <span data-ttu-id="d9299-121">Valore</span><span class="sxs-lookup"><span data-stu-id="d9299-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="d9299-122">Versione</span><span class="sxs-lookup"><span data-stu-id="d9299-122">Version</span></span><br/> | <span data-ttu-id="d9299-123">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="d9299-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d9299-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9299-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9299-125">**Attributi di ambiente**</span><span class="sxs-lookup"><span data-stu-id="d9299-125">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 






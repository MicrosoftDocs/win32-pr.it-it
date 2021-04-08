---
description: Un file di icona può avere diverse dimensioni della stessa immagine dell'icona.
ms.assetid: 2d4d3689-a45a-4088-b466-e2b3bf4c8fb5
title: Attributo di controllo IconSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cb615a53c589ebc2ad2cafb8a2ff7dec902865e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049901"
---
# <a name="iconsize-control-attribute"></a><span data-ttu-id="7daf8-103">Attributo di controllo IconSize</span><span class="sxs-lookup"><span data-stu-id="7daf8-103">IconSize Control Attribute</span></span>

<span data-ttu-id="7daf8-104">Un file di icona può avere diverse dimensioni della stessa immagine dell'icona.</span><span class="sxs-lookup"><span data-stu-id="7daf8-104">An icon file can hold several different sizes of the same icon image.</span></span> <span data-ttu-id="7daf8-105">Questi bit specificano le dimensioni dell'immagine dell'icona da caricare.</span><span class="sxs-lookup"><span data-stu-id="7daf8-105">These bits specify which size of the icon image to load.</span></span> <span data-ttu-id="7daf8-106">Se non è impostato alcun bit, viene caricata la prima immagine.</span><span class="sxs-lookup"><span data-stu-id="7daf8-106">If none of the bits are set, the first image is loaded.</span></span> <span data-ttu-id="7daf8-107">Se viene impostato solo **msidbControlAttributesIconSize16** , viene caricata la prima immagine di 16x16.</span><span class="sxs-lookup"><span data-stu-id="7daf8-107">If only **msidbControlAttributesIconSize16** is set, the first 16x16 image is loaded.</span></span> <span data-ttu-id="7daf8-108">Se è impostato solo **msidbControlAttributesIconSize32** , viene caricata la prima immagine di 32x32.</span><span class="sxs-lookup"><span data-stu-id="7daf8-108">If only the **msidbControlAttributesIconSize32** is set, the first 32x32 image is loaded.</span></span> <span data-ttu-id="7daf8-109">Se è impostato **msidbControlAttributesIconSize48** , viene caricata la prima immagine di 48x48.</span><span class="sxs-lookup"><span data-stu-id="7daf8-109">If **msidbControlAttributesIconSize48** is set, the first 48x48 image is loaded.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="7daf8-110">Controlli validi</span><span class="sxs-lookup"><span data-stu-id="7daf8-110">Valid Controls</span></span>

[<span data-ttu-id="7daf8-111">CheckBox</span><span class="sxs-lookup"><span data-stu-id="7daf8-111">CheckBox</span></span>](checkbox-control.md)

[<span data-ttu-id="7daf8-112">Icona</span><span class="sxs-lookup"><span data-stu-id="7daf8-112">Icon</span></span>](icon-control.md)

[<span data-ttu-id="7daf8-113">Pulsante</span><span class="sxs-lookup"><span data-stu-id="7daf8-113">PushButton</span></span>](pushbutton-control.md)

[<span data-ttu-id="7daf8-114">RadioButtonGroup</span><span class="sxs-lookup"><span data-stu-id="7daf8-114">RadioButtonGroup</span></span>](radiobuttongroup-control.md)

## <a name="value"></a><span data-ttu-id="7daf8-115">Valore</span><span class="sxs-lookup"><span data-stu-id="7daf8-115">Value</span></span>



| <span data-ttu-id="7daf8-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="7daf8-116">Decimal</span></span> | <span data-ttu-id="7daf8-117">Valore esadecimale</span><span class="sxs-lookup"><span data-stu-id="7daf8-117">Hexadecimal</span></span> | <span data-ttu-id="7daf8-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7daf8-118">Description</span></span>                          |
|---------|-------------|--------------------------------------|
| <span data-ttu-id="7daf8-119">2097152</span><span class="sxs-lookup"><span data-stu-id="7daf8-119">2097152</span></span> | <span data-ttu-id="7daf8-120">0x00200000</span><span class="sxs-lookup"><span data-stu-id="7daf8-120">0x00200000</span></span>  | <span data-ttu-id="7daf8-121">**msidbControlAttributesIconSize16**</span><span class="sxs-lookup"><span data-stu-id="7daf8-121">**msidbControlAttributesIconSize16**</span></span> |
| <span data-ttu-id="7daf8-122">4194304</span><span class="sxs-lookup"><span data-stu-id="7daf8-122">4194304</span></span> | <span data-ttu-id="7daf8-123">0x00400000</span><span class="sxs-lookup"><span data-stu-id="7daf8-123">0x00400000</span></span>  | <span data-ttu-id="7daf8-124">**msidbControlAttributesIconSize32**</span><span class="sxs-lookup"><span data-stu-id="7daf8-124">**msidbControlAttributesIconSize32**</span></span> |
| <span data-ttu-id="7daf8-125">6291456</span><span class="sxs-lookup"><span data-stu-id="7daf8-125">6291456</span></span> | <span data-ttu-id="7daf8-126">0x00600000</span><span class="sxs-lookup"><span data-stu-id="7daf8-126">0x00600000</span></span>  | <span data-ttu-id="7daf8-127">**msidbControlAttributesIconSize48**</span><span class="sxs-lookup"><span data-stu-id="7daf8-127">**msidbControlAttributesIconSize48**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7daf8-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="7daf8-128">Remarks</span></span>

<span data-ttu-id="7daf8-129">Per impostare questo attributo su un controllo, includere i bit IconSize nella colonna Attributes del record del controllo nella tabella del [controllo](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="7daf8-129">To set this attribute on a control, include the IconSize bits in the Attributes column of the control's record in the [Control table](control-table.md).</span></span>

<span data-ttu-id="7daf8-130">Se il bit [FixedSize](fixedsize-control-attribute.md) non è impostato, l'immagine caricata viene compattata o estesa per adattarsi al controllo icona.</span><span class="sxs-lookup"><span data-stu-id="7daf8-130">If the [FixedSize](fixedsize-control-attribute.md) bit is not set, the loaded image is shrunk or stretched to fit the icon control.</span></span> <span data-ttu-id="7daf8-131">Se il bit [FixedSize](fixedsize-control-attribute.md) è impostato e l'immagine caricata è inferiore al controllo Icon, l'immagine viene visualizzata al centro all'interno del controllo.</span><span class="sxs-lookup"><span data-stu-id="7daf8-131">If the [FixedSize](fixedsize-control-attribute.md) bit is set, and the loaded image is smaller than the icon control, the picture is displayed centered inside the control.</span></span> <span data-ttu-id="7daf8-132">Se il bit [FixedSize](fixedsize-control-attribute.md) è impostato e l'immagine caricata è più grande del controllo Icon, l'immagine viene ridotta per adattarsi al controllo.</span><span class="sxs-lookup"><span data-stu-id="7daf8-132">If the [FixedSize](fixedsize-control-attribute.md) bit is set, and the loaded image is larger than the icon control, the picture is reduced to fit the control.</span></span>

<span data-ttu-id="7daf8-133">Vedere [gli attributi del controllo](control-attributes.md) e il controllo che è necessario creare sotto i [controlli](controls.md).</span><span class="sxs-lookup"><span data-stu-id="7daf8-133">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 




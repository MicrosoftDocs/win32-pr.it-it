---
title: Elemento color
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. | Elemento color
ms.assetid: 36fafe16-b708-4dc1-9325-d4f39265069a
keywords:
- Finestra elementi colori Media Player
topic_type:
- apiref
api_name:
- Color Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6c73aa9fe2c7f731e872c4a2e235bf9c0e29ce05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331763"
---
# <a name="color-element"></a><span data-ttu-id="77933-105">Elemento color</span><span class="sxs-lookup"><span data-stu-id="77933-105">Color Element</span></span>

> [!Note]  
> <span data-ttu-id="77933-106">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="77933-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="77933-107">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="77933-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="77933-108">L'elemento color specifica il colore di sfondo per i pulsanti di spostamento online, il testo del pulsante e la barra delle applicazioni delle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="77933-108">The Color element specifies the background color for online store navigation buttons, button text, and the Features taskbar.</span></span>

``` syntax
<Color
    MediaPlayer = "#FFFFFF"
    MediaPlayerText = "#FFFFFF"
/>
```

## <a name="attributes"></a><span data-ttu-id="77933-109">Attributi</span><span class="sxs-lookup"><span data-stu-id="77933-109">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="77933-110"><span id="MediaPlayer__required_"></span><span id="mediaplayer__required_"></span><span id="MEDIAPLAYER__REQUIRED_"></span>**MediaPlayer** (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="77933-110"><span id="MediaPlayer__required_"></span><span id="mediaplayer__required_"></span><span id="MEDIAPLAYER__REQUIRED_"></span>**MediaPlayer** (required)</span></span>
</dt> <dd>

<span data-ttu-id="77933-111">Valore di colore RGB esadecimale.</span><span class="sxs-lookup"><span data-stu-id="77933-111">Hexadecimal RGB color value.</span></span> <span data-ttu-id="77933-112">Specifica il colore di sfondo per i pulsanti e la barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="77933-112">Specifies the background color for buttons and the taskbar.</span></span>

</dd> <dt>

<span data-ttu-id="77933-113"><span id="MediaPlayerText__required_"></span><span id="mediaplayertext__required_"></span><span id="MEDIAPLAYERTEXT__REQUIRED_"></span>**MediaPlayerText** (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="77933-113"><span id="MediaPlayerText__required_"></span><span id="mediaplayertext__required_"></span><span id="MEDIAPLAYERTEXT__REQUIRED_"></span>**MediaPlayerText** (required)</span></span>
</dt> <dd>

<span data-ttu-id="77933-114">Valore di colore RGB esadecimale.</span><span class="sxs-lookup"><span data-stu-id="77933-114">Hexadecimal RGB color value.</span></span> <span data-ttu-id="77933-115">Specifica il colore per il testo del pulsante.</span><span class="sxs-lookup"><span data-stu-id="77933-115">Specifies the color for the button text.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="77933-116">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="77933-116">Parent/Child Elements</span></span>



| <span data-ttu-id="77933-117">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="77933-117">Hierarchy</span></span>       | <span data-ttu-id="77933-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="77933-118">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="77933-119">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="77933-119">Parent elements</span></span> | <span data-ttu-id="77933-120">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="77933-120">**ServiceInfo**</span></span> |
| <span data-ttu-id="77933-121">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="77933-121">Child elements</span></span>  | <span data-ttu-id="77933-122">nessuno</span><span class="sxs-lookup"><span data-stu-id="77933-122">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="77933-123">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="77933-123">Remarks</span></span>

<span data-ttu-id="77933-124">Il valore predefinito per **MediaPlayer** è \# 7C9AD6.</span><span class="sxs-lookup"><span data-stu-id="77933-124">The default value for **MediaPlayer** is \#7C9AD6.</span></span> <span data-ttu-id="77933-125">Il valore predefinito per **MediaPlayerText** è \# FFFFFF.</span><span class="sxs-lookup"><span data-stu-id="77933-125">The default value for **MediaPlayerText** is \#FFFFFF.</span></span>

<span data-ttu-id="77933-126">Assicurarsi di usare i colori che semplificano la lettura del testo del pulsante da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="77933-126">Be sure to use colors that make it easy for the user to read the button text.</span></span> <span data-ttu-id="77933-127">Ad esempio, è consigliabile evitare di usare il testo del pulsante bianco sui pulsanti di colore chiaro.</span><span class="sxs-lookup"><span data-stu-id="77933-127">For example, you should avoid using white button text on light colored buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="77933-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="77933-128">Requirements</span></span>



| <span data-ttu-id="77933-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="77933-129">Requirement</span></span> | <span data-ttu-id="77933-130">Valore</span><span class="sxs-lookup"><span data-stu-id="77933-130">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="77933-131">Versione</span><span class="sxs-lookup"><span data-stu-id="77933-131">Version</span></span><br/> | <span data-ttu-id="77933-132">Windows Media Player 10 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="77933-132">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="77933-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="77933-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77933-134">**Documento ServiceInfo di esempio per un negozio online di tipo 1**</span><span class="sxs-lookup"><span data-stu-id="77933-134">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="77933-135">**Documento ServiceInfo di esempio per un negozio online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="77933-135">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="77933-136">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="77933-136">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 






---
title: STARTTIME (elemento)
description: L'elemento STARTTIME definisce un indice temporale da cui Windows Media Player avvierà il rendering del flusso.
ms.assetid: 9b0199c8-5c95-4b4e-a943-e3bd037bf0bc
keywords:
- Elemento STARTTIME Media Player Windows
topic_type:
- apiref
api_name:
- STARTTIME Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a882da6c07ec76a94c8e214fe1da11c71680b0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326296"
---
# <a name="starttime-element"></a><span data-ttu-id="dee35-104">STARTTIME (elemento)</span><span class="sxs-lookup"><span data-stu-id="dee35-104">STARTTIME Element</span></span>

<span data-ttu-id="dee35-105">L'elemento **StartTime** definisce un indice temporale da cui Windows Media Player avvierà il rendering del flusso.</span><span class="sxs-lookup"><span data-stu-id="dee35-105">The **STARTTIME** element defines a time index from which Windows Media Player will start rendering the stream.</span></span>

``` syntax
<STARTTIME
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a><span data-ttu-id="dee35-106">Attributi</span><span class="sxs-lookup"><span data-stu-id="dee35-106">Attributes</span></span>

<span data-ttu-id="dee35-107">**Valore** (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="dee35-107">**VALUE** (required)</span></span>

<span data-ttu-id="dee35-108">Indice temporale (in ore, minuti, secondi e centesimi di secondo) dal quale Windows Media Player avvia la riproduzione di un flusso definito nell'elemento associato.</span><span class="sxs-lookup"><span data-stu-id="dee35-108">The time index (in hours, minutes, seconds, and hundredths of a second) from which Windows Media Player starts playing a stream defined in the associated element.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="dee35-109">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="dee35-109">Parent/Child Elements</span></span>



| <span data-ttu-id="dee35-110">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="dee35-110">Hierarchy</span></span>       | <span data-ttu-id="dee35-111">Elementi</span><span class="sxs-lookup"><span data-stu-id="dee35-111">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="dee35-112">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="dee35-112">Parent elements</span></span> | <span data-ttu-id="dee35-113">**voce**, **ref**</span><span class="sxs-lookup"><span data-stu-id="dee35-113">**ENTRY**, **REF**</span></span> |
| <span data-ttu-id="dee35-114">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="dee35-114">Child elements</span></span>  | <span data-ttu-id="dee35-115">nessuno</span><span class="sxs-lookup"><span data-stu-id="dee35-115">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="dee35-116">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="dee35-116">Remarks</span></span>

<span data-ttu-id="dee35-117">Questo elemento definisce un indice temporale nel contenuto in cui Windows Media Player deve avviare il rendering del flusso.</span><span class="sxs-lookup"><span data-stu-id="dee35-117">This element defines a time index into the content where Windows Media Player is to start rendering the stream.</span></span> <span data-ttu-id="dee35-118">Questo elemento può essere usato solo con contenuto archiviato su richiesta che è stato indicizzato.</span><span class="sxs-lookup"><span data-stu-id="dee35-118">This element can be used only with stored, on-demand content that has been indexed.</span></span>

## <a name="examples"></a><span data-ttu-id="dee35-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="dee35-119">Examples</span></span>


```XML
<STARTTIME VALUE="1:30.0" />
```



## <a name="requirements"></a><span data-ttu-id="dee35-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dee35-120">Requirements</span></span>



| <span data-ttu-id="dee35-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="dee35-121">Requirement</span></span> | <span data-ttu-id="dee35-122">Valore</span><span class="sxs-lookup"><span data-stu-id="dee35-122">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="dee35-123">Versione</span><span class="sxs-lookup"><span data-stu-id="dee35-123">Version</span></span><br/> | <span data-ttu-id="dee35-124">Windows Media Player versione 70 o successiva</span><span class="sxs-lookup"><span data-stu-id="dee35-124">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dee35-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dee35-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dee35-126">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="dee35-126">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="dee35-127">**Informazioni di riferimento sui metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="dee35-127">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 






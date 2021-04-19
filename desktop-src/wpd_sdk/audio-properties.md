---
description: I dispositivi portatili Windows supportano le proprietà audio seguenti.
ms.assetid: 5d6c6a95-abb7-4191-a961-bcb30ca96bb6
title: Proprietà audio (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Audio
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1bdab201fc987d5bc1aff3638fbb57358115fdce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325947"
---
# <a name="audio-properties"></a><span data-ttu-id="c1351-103">Proprietà audio</span><span class="sxs-lookup"><span data-stu-id="c1351-103">Audio Properties</span></span>

<span data-ttu-id="c1351-104">I dispositivi portatili Windows supportano le proprietà audio seguenti.</span><span class="sxs-lookup"><span data-stu-id="c1351-104">Windows Portable Devices supports the following audio properties.</span></span>



| <span data-ttu-id="c1351-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c1351-105">Property</span></span>                         | <span data-ttu-id="c1351-106">VarType</span><span class="sxs-lookup"><span data-stu-id="c1351-106">VarType</span></span>     | <span data-ttu-id="c1351-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1351-107">Description</span></span>                                                                                                                                                                                                        |
|----------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1351-108">**\_ \_ profondità bit audio \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="c1351-108">**WPD\_AUDIO\_BIT\_DEPTH**</span></span>       | <span data-ttu-id="c1351-109">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="c1351-109">**VT\_UI4**</span></span> | <span data-ttu-id="c1351-110">Profondità di bit dell'audio.</span><span class="sxs-lookup"><span data-stu-id="c1351-110">The bit-depth of the audio.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="c1351-111">**\_velocità in \_ bit audio WPD**</span><span class="sxs-lookup"><span data-stu-id="c1351-111">**WPD\_AUDIO\_BITRATE**</span></span>          | <span data-ttu-id="c1351-112">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="c1351-112">**VT\_UI4**</span></span> | <span data-ttu-id="c1351-113">Velocità in bit dell'audio, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="c1351-113">The bit rate of the audio, in bits per second.</span></span>                                                                                                                                                                     |
| <span data-ttu-id="c1351-114">**\_ \_ allineamento blocchi audio \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="c1351-114">**WPD\_AUDIO\_BLOCK\_ALIGNMENT**</span></span> | <span data-ttu-id="c1351-115">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="c1351-115">**VT\_UI4**</span></span> | <span data-ttu-id="c1351-116">Allineamento del blocco del file audio, in byte.</span><span class="sxs-lookup"><span data-stu-id="c1351-116">The block alignment of the audio file, in bytes.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="c1351-117">**\_numero di \_ canali \_ audio WPD**</span><span class="sxs-lookup"><span data-stu-id="c1351-117">**WPD\_AUDIO\_CHANNEL\_COUNT**</span></span>   | <span data-ttu-id="c1351-118">**\_R4 VT**</span><span class="sxs-lookup"><span data-stu-id="c1351-118">**VT\_R4**</span></span>  | <span data-ttu-id="c1351-119">Il numero di canali in questo file audio, ad esempio 1, 2 o 5,1.</span><span class="sxs-lookup"><span data-stu-id="c1351-119">The number of channels in this audio file, for example, 1, 2, or 5.1.</span></span>                                                                                                                                              |
| <span data-ttu-id="c1351-120">**\_codice del \_ formato \_ audio WPD**</span><span class="sxs-lookup"><span data-stu-id="c1351-120">**WPD\_AUDIO\_FORMAT\_CODE**</span></span>     | <span data-ttu-id="c1351-121">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="c1351-121">**VT\_UI4**</span></span> | <span data-ttu-id="c1351-122">Numero di codice del formato WAVE registrato.</span><span class="sxs-lookup"><span data-stu-id="c1351-122">The registered WAVE format code number.</span></span> <span data-ttu-id="c1351-123">Per un elenco dei formati WAVE registrati, vedere l'articolo [codici FourCC registrati e formati Wave](https://msdn2.microsoft.com/library/ms867195.aspx) nel sito Web MSDN.</span><span class="sxs-lookup"><span data-stu-id="c1351-123">For a listing of registered WAVE formats, see the article [Registered FOURCC Codes and WAVE Formats](https://msdn2.microsoft.com/library/ms867195.aspx) on the MSDN Web site.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="c1351-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1351-124">Requirements</span></span>



| <span data-ttu-id="c1351-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1351-125">Requirement</span></span> | <span data-ttu-id="c1351-126">Valore</span><span class="sxs-lookup"><span data-stu-id="c1351-126">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1351-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c1351-127">Header</span></span><br/> | <dl> <span data-ttu-id="c1351-128"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1351-128"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1351-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1351-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1351-130">**Proprietà e attributi di WPD**</span><span class="sxs-lookup"><span data-stu-id="c1351-130">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 





---
title: Volume scalare
description: Volume scalare
ms.assetid: a9fe2c35-9109-4697-9ffa-a31debbe72c8
keywords:
- MIDI (Musical Instrument Digital Interface), volume Scalar
- MIDI (Musical Instrument Digital Interface), volume Scalar
- Mapper MIDI, volume Scalar
- volume scalare
- Mapper MIDI, regolazione del livello di output
- regolazione di livelli di output
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d39566a10ca909030b60ff197f009b6afe05ce51
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045373"
---
# <a name="the-volume-scalar"></a><span data-ttu-id="51380-109">Volume scalare</span><span class="sxs-lookup"><span data-stu-id="51380-109">The Volume Scalar</span></span>

<span data-ttu-id="51380-110">Lo scopo del volume scalare è consentire le regolazioni tra i livelli di output relativi di patch diverse in un sintetizzatore.</span><span class="sxs-lookup"><span data-stu-id="51380-110">The purpose of the volume scalar is to allow adjustments between the relative output levels of different patches on a synthesizer.</span></span> <span data-ttu-id="51380-111">Se, ad esempio, la patch Bass in un sintetizzatore è troppo alta rispetto alla patch del piano, è possibile modificare la mappa di installazione per ridimensionare il volume di bassi o il volume del piano.</span><span class="sxs-lookup"><span data-stu-id="51380-111">For example, if the bass patch on a synthesizer is too loud compared with its piano patch, you can change the setup map to scale the bass volume down or the piano volume up.</span></span>

<span data-ttu-id="51380-112">Volume Scalar specifica un valore percentuale per la modifica di tutti i messaggi del controller di volume principale MIDI che seguono un messaggio di modifica del programma associato.</span><span class="sxs-lookup"><span data-stu-id="51380-112">The volume scalar specifies a percentage value for changing all MIDI main-volume controller messages that follow an associated program-change message.</span></span> <span data-ttu-id="51380-113">Se, ad esempio, il valore scalare del volume è 50%, il mapper MIDI modifica i messaggi del controller principale del volume MIDI, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="51380-113">For example, if the volume scalar value is 50%, the MIDI Mapper modifies MIDI main-volume controller messages as shown in the following illustration.</span></span>

![immagine del mapper MIDI](images/mmap-a04.gif)

 

 





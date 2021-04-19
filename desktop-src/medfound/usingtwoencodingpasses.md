---
description: La codifica a due passaggi può essere usata per la velocità in bit costante (CBR) e per la codifica con velocità in bit variabile (VBR) con alcuni codec Windows Media.
ms.assetid: eec5085c-9441-496a-8127-cf5d2686d917
title: Uso della codifica Two-Pass (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993af0015452db410b5a9f2c13233566fc17a3a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310167"
---
# <a name="using-two-pass-encoding-microsoft-media-foundation"></a><span data-ttu-id="4c4db-103">Uso della codifica Two-Pass (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="4c4db-103">Using Two-Pass Encoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="4c4db-104">La codifica a due passaggi può essere usata per la velocità in bit costante (CBR) e per la codifica con velocità in bit variabile (VBR) con alcuni codec Windows Media.</span><span class="sxs-lookup"><span data-stu-id="4c4db-104">Two-pass encoding can be used for constant bit rate (CBR) and for variable bit rate (VBR) encoding with some of the Windows Media codecs.</span></span> <span data-ttu-id="4c4db-105">È possibile trovare il numero massimo di passaggi di codifica supportati da un codec recuperando la proprietà [MFPKEY di \_ PASSESRECOMMENDED](mfpkey-passesrecommendedproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="4c4db-105">You can find the maximum number of encoding passes supported by a codec by retrieving the [MFPKEY\_PASSESRECOMMENDED](mfpkey-passesrecommendedproperty.md) property.</span></span> <span data-ttu-id="4c4db-106">Nessuno dei codec supporta più di due passaggi.</span><span class="sxs-lookup"><span data-stu-id="4c4db-106">None of the codecs supports more than two passes.</span></span> <span data-ttu-id="4c4db-107">Configurare DMO per l'utilizzo di due passaggi impostando la proprietà [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) su 2.</span><span class="sxs-lookup"><span data-stu-id="4c4db-107">Configure the DMO to use two passes by setting the [MFPKEY\_PASSESUSED](mfpkey-passesusedproperty.md) property to 2.</span></span>

<span data-ttu-id="4c4db-108">Recapitare gli esempi al codificatore DMO uno alla volta, come si farebbe in una modalità con un solo passaggio.</span><span class="sxs-lookup"><span data-stu-id="4c4db-108">Deliver the samples to the encoder DMO one at a time, as you would in a one-pass mode.</span></span> <span data-ttu-id="4c4db-109">Quando si elaborano gli esempi di input per il passaggio di pre-elaborazione, le chiamate a [**IMediaObject::P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) o [**IMFTransform::P Rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) restituiranno **S \_ false** per indicare che non viene prodotto alcun output.</span><span class="sxs-lookup"><span data-stu-id="4c4db-109">When you process the input samples for your preprocessing pass, the calls to [**IMediaObject::ProcessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) or [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) will return **S\_FALSE**, to indicate that no output is produced.</span></span>

<span data-ttu-id="4c4db-110">Alla fine del primo passaggio (dopo l'elaborazione dell'ultimo input per la prima volta), è necessario impostare la proprietà [MFPKEY \_ ENDOFPASS](mfpkey-endofpassproperty.md) per notificare al codec che l'input successivo elaborato è il primo input del secondo passaggio.</span><span class="sxs-lookup"><span data-stu-id="4c4db-110">At the end of the first pass (after the last input is processed for the first time), you then must set the [MFPKEY\_ENDOFPASS](mfpkey-endofpassproperty.md) property to notify the codec that the next input processed is the first input of the second pass.</span></span> <span data-ttu-id="4c4db-111">Per questa proprietà non è necessario alcun valore, quindi è necessario usare una struttura **Variant** vuota.</span><span class="sxs-lookup"><span data-stu-id="4c4db-111">No value is required for this property, so you should use an empty **VARIANT** structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c4db-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4c4db-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c4db-113">Codec Windows Media</span><span class="sxs-lookup"><span data-stu-id="4c4db-113">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> </dl>

 

 

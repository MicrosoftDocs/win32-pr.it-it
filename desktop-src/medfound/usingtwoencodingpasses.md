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
# <a name="using-two-pass-encoding-microsoft-media-foundation"></a>Uso della codifica Two-Pass (Microsoft Media Foundation)

La codifica a due passaggi può essere usata per la velocità in bit costante (CBR) e per la codifica con velocità in bit variabile (VBR) con alcuni codec Windows Media. È possibile trovare il numero massimo di passaggi di codifica supportati da un codec recuperando la proprietà [MFPKEY di \_ PASSESRECOMMENDED](mfpkey-passesrecommendedproperty.md) . Nessuno dei codec supporta più di due passaggi. Configurare DMO per l'utilizzo di due passaggi impostando la proprietà [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) su 2.

Recapitare gli esempi al codificatore DMO uno alla volta, come si farebbe in una modalità con un solo passaggio. Quando si elaborano gli esempi di input per il passaggio di pre-elaborazione, le chiamate a [**IMediaObject::P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) o [**IMFTransform::P Rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) restituiranno **S \_ false** per indicare che non viene prodotto alcun output.

Alla fine del primo passaggio (dopo l'elaborazione dell'ultimo input per la prima volta), è necessario impostare la proprietà [MFPKEY \_ ENDOFPASS](mfpkey-endofpassproperty.md) per notificare al codec che l'input successivo elaborato è il primo input del secondo passaggio. Per questa proprietà non è necessario alcun valore, quindi è necessario usare una struttura **Variant** vuota.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codec Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 

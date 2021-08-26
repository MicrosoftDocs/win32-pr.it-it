---
description: La codifica a due passi può essere usata per la velocità in bit costante (CBR) e per la codifica VBR (Variable Bit Rate) con alcuni dei codec Windows Media.
ms.assetid: eec5085c-9441-496a-8127-cf5d2686d917
title: Uso Two-Pass codifica (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58a79678e3b4396dfe87b93dfda7c9fd26487b8fdba83d2214509675ee742951
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887111"
---
# <a name="using-two-pass-encoding-microsoft-media-foundation"></a>Uso Two-Pass codifica (Microsoft Media Foundation)

La codifica a due passi può essere usata per la velocità in bit costante (CBR) e per la codifica VBR (Variable Bit Rate) con alcuni dei codec Windows Media. È possibile trovare il numero massimo di passaggi di codifica supportati da un codec recuperando la [proprietà MFPKEY \_ PASSESRECOMMENDED.](mfpkey-passesrecommendedproperty.md) Nessuno dei codec supporta più di due passaggi. Configurare la DMO per l'uso di due passaggi impostando la [proprietà MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) su 2.

Distribuire gli esempi al codificatore DMO uno alla volta, come si farebbe in modalità a passaggio singolo. Quando si elaborano gli esempi di input per il passaggio di pre-elaborazione, le chiamate [**a IMediaObject::P rocessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) o [**IMFTransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) restituiranno **S \_ FALSE** per indicare che non viene prodotto alcun output.

Alla fine del primo passaggio (dopo che l'ultimo input è stato elaborato per la prima volta), è quindi necessario impostare la proprietà [MFPKEY \_ ENDOFPASS](mfpkey-endofpassproperty.md) per notificare al codec che l'input successivo elaborato è il primo input del secondo passaggio. Non è necessario alcun valore per questa proprietà, pertanto è consigliabile usare una **struttura VARIANT** vuota.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codec Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 

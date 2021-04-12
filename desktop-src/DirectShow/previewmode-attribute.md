---
description: L'attributo PreviewMode specifica la modalità di anteprima per il gruppo. Se il valore è TRUE, i frame potrebbero essere eliminati durante l'anteprima. In caso contrario, non viene eliminato alcun frame durante l'anteprima. Il valore predefinito è TRUE.
ms.assetid: 5e4f4407-b43e-4b31-8676-1e12b6b70034
title: Attributo PreviewMode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3b589b279a11b8ec329641ea2522a6a46dfa0e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401199"
---
# <a name="previewmode-attribute"></a>Attributo PreviewMode

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `previewmode` attributo specifica la modalità di anteprima per il gruppo. Se il valore è **true**, i frame potrebbero essere eliminati durante l'anteprima. In caso contrario, non viene eliminato alcun frame durante l'anteprima. Il valore predefinito è **true**.

## <a name="possible-values"></a>Valori possibili

I valori seguenti sono definiti come TRUE: y, Y, t, T, 1. I valori seguenti sono definiti come FALSE: n, N, f, F, 0 (zero).

## <a name="applies-to"></a>Si applica a

[**gruppo**](group-element.md)

## <a name="remarks"></a>Commenti

Con l'impostazione predefinita, i frame vengono rilasciati durante l'anteprima degli effetti o delle transizioni lente, per sincronizzare il video con l'audio. Il video potrebbe sembrare frammentato come risultato. Se si imposta questo attributo su **false** , viene eseguito il rendering di ogni fotogramma durante l'anteprima, causando probabilmente la mancata sincronizzazione del video con l'audio. I frame non vengono mai eliminati durante la scrittura in un file.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Attributi XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineGroup:: SetPreviewMode**](iamtimelinegroup-setpreviewmode.md)
</dt> </dl>

 

 




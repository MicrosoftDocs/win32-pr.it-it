---
description: L'attributo previewmode specifica la modalità di anteprima per il gruppo. Se il valore è TRUE, i frame potrebbero essere eliminati durante l'anteprima. In caso contrario, non vengono eliminati fotogrammi durante l'anteprima. Il valore predefinito è TRUE.
ms.assetid: 5e4f4407-b43e-4b31-8676-1e12b6b70034
title: Attributo previewmode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6baed13417539432a3a2958b96b214c3c63ae12f2802586ca220669b1497d91f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748271"
---
# <a name="previewmode-attribute"></a>Attributo previewmode

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

`previewmode`L'attributo specifica la modalità di anteprima per il gruppo. Se il valore è **TRUE,** i frame potrebbero essere eliminati durante l'anteprima. In caso contrario, non vengono eliminati fotogrammi durante l'anteprima. Il valore predefinito è **TRUE.**

## <a name="possible-values"></a>Valori possibili

I valori seguenti sono definiti come TRUE: y, Y, t, T, 1. I valori seguenti sono definiti come FALSE: n, N, f, F, 0 (zero).

## <a name="applies-to"></a>Si applica a

[**Gruppo**](group-element.md)

## <a name="remarks"></a>Commenti

Con l'impostazione predefinita, i fotogrammi vengono eliminati durante l'anteprima di effetti lenti o transizioni, per mantenere il video sincronizzato con l'audio. Di conseguenza, il video potrebbe risultare insodetta. L'impostazione di questo **attributo su FALSE** forza il rendering di ogni fotogramma durante l'anteprima, causando probabilmente la non sincronizzazione del video con l'audio. I frame non vengono mai eliminati durante la scrittura in un file.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Attributi XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineGroup::SetPreviewMode**](iamtimelinegroup-setpreviewmode.md)
</dt> </dl>

 

 




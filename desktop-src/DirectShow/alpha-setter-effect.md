---
description: Effetto setter alfa
ms.assetid: dd3ab119-328b-4782-811a-f06909c17dec
title: Effetto setter alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e599b314dced175188d77dad1ae93259a23b8eb892471d047afab218add9a664
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586761"
---
# <a name="alpha-setter-effect"></a>Effetto setter alfa

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

L'effetto Setter alfa imposta i bit alfa su un'immagine video.

ID classe (CLSID): {506D89AE-909A-44f7-9444-ABD575896E35}

Nome variabile CLSID: CLSID \_ DxtAlphaSetter

Nome descrittivo: "DxtAlphaSetter"

### <a name="properties"></a>Proprietà



| Proprietà  | Type   | Predefinito | Descrizione                                                 |
|-----------|--------|---------|-------------------------------------------------------------|
| Alfa     | BYTE   | -1      | Imposta il valore alfa per l'intera immagine.                        |
| AlphaRamp | double | -1.0    | Imposta il valore alfa come percentuale del valore alfa originale. |



 

## <a name="remarks"></a>Commenti

Una proprietà con un valore negativo viene ignorata. Solo una proprietà può avere un valore non negativo. La proprietà Alpha specifica un valore alfa costante per ogni pixel nell'immagine. Questa proprietà sovrascrive i valori alfa dell'immagine originale. La proprietà AlphaRamp specifica il valore alfa di ogni pixel come percentuale del valore originale del pixel, da 0,0 a 1,0.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Fusione alfa](alpha-blending.md)
</dt> </dl>

 

 




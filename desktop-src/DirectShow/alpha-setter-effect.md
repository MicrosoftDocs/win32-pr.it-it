---
description: Effetto Setter Alpha
ms.assetid: dd3ab119-328b-4782-811a-f06909c17dec
title: Effetto Setter Alpha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372ec018a9cfb8fe15307ae44f5a905bf1eb3440
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746370"
---
# <a name="alpha-setter-effect"></a>Effetto Setter Alpha

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L'effetto Alpha Setter imposta i bit alfa su un'immagine video.

ID classe (CLSID): {506D89AE-909A-44f7-9444-ABD575896E35}

Nome variabile CLSID: CLSID \_ DxtAlphaSetter

Nome descrittivo: "DxtAlphaSetter"

### <a name="properties"></a>Proprietà



| Proprietà  | Type   | Predefinito | Descrizione                                                 |
|-----------|--------|---------|-------------------------------------------------------------|
| Alfa     | BYTE   | -1      | Imposta l'alfa per l'intera immagine.                        |
| AlphaRamp | double | -1.0    | Imposta l'alfa come percentuale del valore alfa originale. |



 

## <a name="remarks"></a>Commenti

Una proprietà con un valore negativo viene ignorata. Una sola proprietà può avere un valore non negativo. La proprietà Alpha specifica un valore alfa costante per ogni pixel nell'immagine. Questa proprietà sovrascrive i valori alfa dall'immagine originale. La proprietà AlphaRamp specifica il valore alfa di ogni pixel come percentuale del valore originale del pixel, da 0,0 a 1,0.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Fusione alfa](alpha-blending.md)
</dt> </dl>

 

 



